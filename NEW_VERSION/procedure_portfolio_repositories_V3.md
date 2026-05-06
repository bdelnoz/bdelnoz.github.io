# Procedure V3 - Portfolio repositories / Markdown / PDF

**Project:** GitHub and local repositories portfolio analysis  
**Owner:** Bruno DELNOZ  
**Generated:** 2026-05-06 10:57:42  
**Scope:** local repositories under `/mnt/data2_78g/Security/scripts` and GitHub repositories under `bdelnoz`

---

## 0. Purpose

This procedure replaces the previous draft workflow.

The goal is to rebuild the technical portfolio from scratch after local repository cleanup, repository additions, and repository changes.

Final expected outputs:

- `portfolio_repositories_bdelnoz_analyse_filtered_V3.md`
- `portfolio_repositories_bdelnoz_analyse_filtered_V3.pdf`

This procedure must produce a reliable local corpus first.  
The portfolio must be generated only after the corpus is validated.

---

## 1. Important rules

### 1.1 No Codex generation in this procedure

This procedure must **not** ask Codex CLI to create or modify files.

Allowed operations:

- read files;
- compare files;
- list repositories;
- inspect metadata;
- collect documentation files;
- generate inventory reports;
- create local ZIP archives for upload.

Forbidden operations in this procedure:

- no `codex exec`;
- no creation of `README.codex.md`;
- no creation of `WHY.codex.md`;
- no modification of repository files;
- no commit;
- no push;
- no destructive command.

If some repositories have poor or missing documentation, they must be listed as problematic.  
A separate task/chat may later decide whether Codex should be used to generate missing documentation.

---

## 2. Source priority rules

For each repository, the master sources for portfolio analysis are:

1. `README.md`
2. `WHY.md`

Fallback sources:

3. `README.codex.md`, only if:
   - `README.md` is absent;
   - or `README.md` exists but is too poor to be useful.

4. `WHY.codex.md`, only if:
   - `WHY.md` is absent;
   - or `WHY.md` exists but is too poor to be useful.

Optional supporting source:

5. `SPECIFICATIONS_GLOBAL.md`, when present.

### 2.1 Definition of "too poor"

A documentation file is considered too poor when it is:

- absent;
- empty;
- only a title;
- only a metadata block;
- only generic boilerplate;
- not related to repository content;
- unable to explain what the repository does;
- unable to support a portfolio description.

### 2.2 Problematic repository rule

If both the master source and fallback source are absent or too poor, the repository must be added to:

```text
problematic_repos.md
```

No automatic Codex generation is performed in this procedure.

---

## 3. Phase 0 - Local and GitHub inventory

This phase does not modify repositories.

It creates a timestamped report in `/tmp`, opens it in Kate, and helps identify:

- local Git repositories;
- configured remotes;
- guessed GitHub repository names;
- public/private state from GitHub;
- fork/source state from GitHub;
- main GitHub language when available;
- presence of documentation files;
- documentation file sizes;
- documentation poverty flags;
- possible local duplicate clones.

### 3.1 Command

Run this locally:

```bash
OUT="/tmp/output4ChatGPT.$(date +%F_%H%M%S).md"
BASE="/mnt/data2_78g/Security/scripts"
TMP_GH="/tmp/bdelnoz_gh_repos.$(date +%F_%H%M%S).tsv"

gh repo list bdelnoz --limit 500 --json name,nameWithOwner,isPrivate,isFork,url,primaryLanguage,updatedAt --jq '.[] | [.nameWithOwner, (if .isPrivate then "PRIV" else "PUB" end), (if .isFork then "FORK" else "SOURCE" end), (.primaryLanguage.name // "unknown"), .updatedAt, .url] | @tsv' > "$TMP_GH"

{
  echo "# Local and GitHub repositories inventory"
  echo
  echo "- Date: $(date -Is)"
  echo "- Host: $(hostname)"
  echo "- Base: $BASE"
  echo "- GitHub TSV: $TMP_GH"
  echo

  echo "## 1. GitHub repositories visible via gh"
  echo
  echo '| GitHub repo | PUB/PRIV | Kind | Main language | Updated at | URL |'
  echo '|---|---:|---:|---|---|---|'
  awk -F '\t' '{ printf "| `%s` | %s | %s | %s | %s | %s |\n", $1, $2, $3, $4, $5, $6 }' "$TMP_GH"

  echo
  echo "## 2. Local Git repositories"
  echo
  echo '| # | Local path | Basename | Remote origin | GitHub repo guessed | PUB/PRIV | Kind | GH language | README.md | WHY.md | README.codex.md | WHY.codex.md | SPEC_GLOBAL |'
  echo '|---:|---|---|---|---|---:|---:|---|---:|---:|---:|---:|---:|'

  i=0
  find "$BASE" -type d -name .git -prune -print | sed 's#/?\.git$##' | sort | while IFS= read -r repo; do
    i=$((i+1))
    base="$(basename "$repo")"
    remote="$(git -C "$repo" remote get-url origin 2>/dev/null || true)"

    ghrepo=""
    case "$remote" in
      https://github.com/*/*.git) ghrepo="$(printf '%s' "$remote" | sed -E 's#https://github.com/([^/]+/[^.]+)\.git#\1#')" ;;
      git@github.com:*.git) ghrepo="$(printf '%s' "$remote" | sed -E 's#git@github.com:([^/]+/[^.]+)\.git#\1#')" ;;
      https://github.com/*/*) ghrepo="$(printf '%s' "$remote" | sed -E 's#https://github.com/([^/]+/[^/]+).*#\1#')" ;;
    esac

    ghline="$(awk -F '\t' -v r="$ghrepo" '$1 == r { print $0; exit }' "$TMP_GH")"
    pubpriv="$(printf '%s' "$ghline" | awk -F '\t' '{print $2}')"
    kind="$(printf '%s' "$ghline" | awk -F '\t' '{print $3}')"
    ghlang="$(printf '%s' "$ghline" | awk -F '\t' '{print $4}')"

    [ -n "$pubpriv" ] || pubpriv="unknown"
    [ -n "$kind" ] || kind="unknown"
    [ -n "$ghlang" ] || ghlang="unknown"

    doc_status() {
      f="$1"
      if [ ! -f "$f" ]; then
        echo "absent"
        return
      fi
      bytes="$(wc -c < "$f" 2>/dev/null || echo 0)"
      lines="$(wc -l < "$f" 2>/dev/null || echo 0)"
      if [ "$bytes" -eq 0 ]; then
        echo "empty"
      elif [ "$lines" -le 5 ] || [ "$bytes" -lt 300 ]; then
        echo "poor:${bytes}B/${lines}L"
      else
        echo "present:${bytes}B/${lines}L"
      fi
    }

    readme="$(doc_status "$repo/README.md")"
    why="$(doc_status "$repo/WHY.md")"
    readmec="$(doc_status "$repo/README.codex.md")"
    whyc="$(doc_status "$repo/WHY.codex.md")"
    specg="$(doc_status "$repo/SPECIFICATIONS_GLOBAL.md")"

    printf '| %s | `%s` | `%s` | `%s` | `%s` | %s | %s | %s | %s | %s | %s | %s | %s |\n' "$i" "$repo" "$base" "$remote" "$ghrepo" "$pubpriv" "$kind" "$ghlang" "$readme" "$why" "$readmec" "$whyc" "$specg"
  done

  echo
  echo "## 3. Possible duplicate local clones by remote"
  echo
  echo '```text'
  find "$BASE" -type d -name .git -prune -print | sed 's#/?\.git$##' | sort | while IFS= read -r repo; do
    remote="$(git -C "$repo" remote get-url origin 2>/dev/null || true)"
    [ -n "$remote" ] && printf '%s\t%s\n' "$remote" "$repo"
  done | sort | awk -F '\t' '
    {
      count[$1]++
      paths[$1]=paths[$1] "\n  - " $2
    }
    END {
      for (r in count) {
        if (count[r] > 1) {
          print r " (" count[r] " local copies)" paths[r] "\n"
        }
      }
    }'
  echo '```'

  echo
  echo "## 4. Git status summary for local repos"
  echo
  echo '| Local path | Current branch | Dirty | Untracked count |'
  echo '|---|---|---:|---:|'
  find "$BASE" -type d -name .git -prune -print | sed 's#/?\.git$##' | sort | while IFS= read -r repo; do
    branch="$(git -C "$repo" branch --show-current 2>/dev/null || true)"
    [ -n "$branch" ] || branch="detached_or_unknown"
    dirty="no"
    git -C "$repo" diff --quiet --ignore-submodules -- 2>/dev/null || dirty="yes"
    untracked="$(git -C "$repo" ls-files --others --exclude-standard 2>/dev/null | wc -l)"
    printf '| `%s` | `%s` | %s | %s |\n' "$repo" "$branch" "$dirty" "$untracked"
  done

} > "$OUT"

chown nox:nox "$OUT" 2>/dev/null || true
kate "$OUT" >/dev/null 2>&1 & disown
echo "$OUT"
```

---

## 4. Phase 1 - Human validation of final repository list

After Phase 0, review the inventory report.

Decide:

- repositories to include;
- repositories to exclude;
- duplicate local clones to ignore;
- forks to exclude;
- sensitive repositories to exclude or anonymize;
- empty / test / backup repositories to exclude.

Expected output after review:

```text
LISTE_FINALE_REPOS_A_ANALYSER
```

Format: one local path per line.

---

## 5. Phase 2 - Source selection and problem detection

For each repository from `LISTE_FINALE_REPOS_A_ANALYSER`, select sources with this order:

| Needed source | Preferred | Fallback |
|---|---|---|
| Project usage / behavior | `README.md` | `README.codex.md` |
| Rationale / purpose | `WHY.md` | `WHY.codex.md` |
| Global constraints | `SPECIFICATIONS_GLOBAL.md` | none |

If preferred source is present but too poor, use fallback.

If both preferred and fallback are absent or too poor, mark repository as problematic.

No Codex generation happens here.

---

## 6. Phase 3 - Collect source corpus and ZIP

This phase collects documentation files into a stable folder and creates a ZIP to upload into ChatGPT.

### 6.1 Prepare `selected_repos.txt`

Create a file containing the final validated repository list:

```bash
SELECTED="/tmp/selected_repos_for_portfolio.txt"
kate "$SELECTED" >/dev/null 2>&1 & disown
```

Paste the validated local paths into this file, one path per line.

### 6.2 Collect documentation sources

```bash
STAMP="$(date +%F_%H%M%S)"
SELECTED="/tmp/selected_repos_for_portfolio.txt"
COLLECT="/tmp/portfolio_collect.$STAMP"
ZIP="/tmp/portfolio_collect.$STAMP.zip"

mkdir -p "$COLLECT/repos"

{
  echo "# Portfolio source collection inventory"
  echo
  echo "- Date: $(date -Is)"
  echo "- Selected list: $SELECTED"
  echo "- Collection dir: $COLLECT"
  echo
  echo '| # | Repo slug | Local path | GitHub remote | PUB/PRIV | README source | WHY source | SPEC_GLOBAL | Status |'
  echo '|---:|---|---|---|---:|---|---|---:|---|'
} > "$COLLECT/inventory.md"

: > "$COLLECT/problematic_repos.md"
echo "# Problematic repositories" > "$COLLECT/problematic_repos.md"
echo >> "$COLLECT/problematic_repos.md"

doc_quality() {
  f="$1"
  if [ ! -f "$f" ]; then
    echo "absent"
    return
  fi
  bytes="$(wc -c < "$f" 2>/dev/null || echo 0)"
  lines="$(wc -l < "$f" 2>/dev/null || echo 0)"
  if [ "$bytes" -eq 0 ]; then
    echo "poor"
  elif [ "$lines" -le 5 ] || [ "$bytes" -lt 300 ]; then
    echo "poor"
  else
    echo "good"
  fi
}

choose_source() {
  master="$1"
  fallback="$2"
  qm="$(doc_quality "$master")"
  qf="$(doc_quality "$fallback")"
  if [ "$qm" = "good" ]; then
    echo "$master"
  elif [ "$qf" = "good" ]; then
    echo "$fallback"
  else
    echo ""
  fi
}

i=0
while IFS= read -r repo; do
  [ -z "$repo" ] && continue
  i=$((i+1))

  if [ ! -d "$repo/.git" ]; then
    printf -- '- `%s`: not a Git repository\n' "$repo" >> "$COLLECT/problematic_repos.md"
    continue
  fi

  slug="$(basename "$repo" | tr -c 'A-Za-z0-9._-' '_')"
  dest="$COLLECT/repos/$slug"
  mkdir -p "$dest"

  remote="$(git -C "$repo" remote get-url origin 2>/dev/null || true)"
  pubpriv="unknown"

  if printf '%s' "$remote" | grep -q 'github.com'; then
    ghrepo="$(printf '%s' "$remote" | sed -E 's#.*github.com[:/]([^/]+/[^/.]+)(\.git)?#\1#')"
    if [ -n "$ghrepo" ]; then
      vis="$(gh repo view "$ghrepo" --json visibility --jq '.visibility' 2>/dev/null || true)"
      case "$vis" in
        PUBLIC) pubpriv="PUB" ;;
        PRIVATE) pubpriv="PRIV" ;;
      esac
    fi
  fi

  readme_src="$(choose_source "$repo/README.md" "$repo/README.codex.md")"
  why_src="$(choose_source "$repo/WHY.md" "$repo/WHY.codex.md")"

  status="OK"
  [ -n "$readme_src" ] || status="PROBLEM"
  [ -n "$why_src" ] || status="PROBLEM"

  if [ -n "$readme_src" ]; then cp -a "$readme_src" "$dest/$(basename "$readme_src")"; fi
  if [ -n "$why_src" ]; then cp -a "$why_src" "$dest/$(basename "$why_src")"; fi
  if [ -f "$repo/SPECIFICATIONS_GLOBAL.md" ]; then cp -a "$repo/SPECIFICATIONS_GLOBAL.md" "$dest/SPECIFICATIONS_GLOBAL.md"; fi

  {
    echo "repo_slug=$slug"
    echo "local_path=$repo"
    echo "remote=$remote"
    echo "pubpriv=$pubpriv"
    echo "readme_source=$readme_src"
    echo "why_source=$why_src"
    echo "specifications_global=$([ -f "$repo/SPECIFICATIONS_GLOBAL.md" ] && echo yes || echo no)"
  } > "$dest/metadata.txt"

  printf '| %s | `%s` | `%s` | `%s` | %s | `%s` | `%s` | %s | %s |\n' "$i" "$slug" "$repo" "$remote" "$pubpriv" "$readme_src" "$why_src" "$([ -f "$repo/SPECIFICATIONS_GLOBAL.md" ] && echo yes || echo no)" "$status" >> "$COLLECT/inventory.md"

  if [ "$status" = "PROBLEM" ]; then
    {
      echo "## $repo"
      echo
      echo "- README.md quality: $(doc_quality "$repo/README.md")"
      echo "- README.codex.md quality: $(doc_quality "$repo/README.codex.md")"
      echo "- WHY.md quality: $(doc_quality "$repo/WHY.md")"
      echo "- WHY.codex.md quality: $(doc_quality "$repo/WHY.codex.md")"
      echo
    } >> "$COLLECT/problematic_repos.md"
  fi

done < "$SELECTED"

cp "$SELECTED" "$COLLECT/selected_repos.txt"
cd /tmp && zip -qr "$ZIP" "$(basename "$COLLECT")"

chown -R nox:nox "$COLLECT" "$ZIP" 2>/dev/null || true
kate "$COLLECT/inventory.md" >/dev/null 2>&1 & disown

echo "$COLLECT"
echo "$ZIP"
```

Upload the resulting ZIP here.

---

## 7. Phase 4 - ChatGPT analysis from ZIP

After upload, ChatGPT must work only from the collected corpus.

Analysis inputs:

- `inventory.md`
- `selected_repos.txt`
- `problematic_repos.md`
- collected source files under `repos/*/`
- metadata files

No guessing from previous chat memory.

---

## 8. Phase 5 - Markdown portfolio generation

Create:

```text
portfolio_repositories_bdelnoz_analyse_filtered_V3.md
```

Required structure:

```text
# Technical Portfolio - Bruno DELNOZ

## Executive summary

## Technology map

## Repository overview table

## Detailed repository notes

## Appendix - problematic or excluded repositories

## Appendix - source selection rules
```

No LinkedIn draft section.

---

## 9. Phase 6 - Repository overview table

The overview table must be sorted by **Main tech**.

Required columns:

| Column | Description |
|---|---|
| Repository | Repository name, without `bdelnoz/` prefix |
| Project type | Security, System, AI, Web, Multimedia, etc. |
| Main tech | Main technology |
| Secondary tech | Other relevant technologies |
| Short purpose | Short useful summary |
| Source used | README, WHY, codex fallback, spec |
| Confidence | High / Medium / Low |
| PUB/PRIV | Short flag from GitHub visibility |

Visibility values:

```text
PUB
PRIV
```

---

## 10. Phase 7 - Detailed repository notes

Detailed notes must be grouped and sorted by project type.

Suggested project types:

```text
AI / LLM / Local AI
Security / Network / Wi-Fi
System / Kali / Linux administration
Web / Browser extensions
Multimedia / Audio / Video
Backup / Storage / Disk
Utility / Developer tooling
Raspberry Pi / Embedded
Documentation / Repository governance
Other / unclear
```

Local folder names may help classification:

```text
AI_Projects
Projects_security
Projects_system
Projects_web
Projects_multimedia
Projects_utility
Projects_backup
Projects_backup_data
Projects_network
Projects_py
Projects_installation
Projects_divers
REPO2PLACE
```

Each repository note should include:

```text
Repository
Project type
Main tech
Secondary tech
PUB/PRIV
Source used
Confidence
What it does
Why it matters
Portfolio wording
Limitations / caution
```

---

## 11. Phase 8 - Colored PDF generation

Create:

```text
portfolio_repositories_bdelnoz_analyse_filtered_V3.pdf
```

PDF requirements:

- professional layout;
- readable colors;
- colored section titles;
- colored badges for `PUB` and `PRIV`;
- readable tables;
- no clipped text;
- no broken layout;
- suitable for sharing as a portfolio document.

---

## 12. Phase 9 - PDF quality control

After PDF generation:

1. render PDF pages to PNG;
2. check at least:
   - first page;
   - repository overview table page;
   - detailed notes page;
   - last page;
3. verify:
   - no text cut off;
   - no table overflow;
   - no unreadable colors;
   - no broken pagination;
   - no raw local paths in public-facing sections unless intentionally kept.

---

## 13. Phase 10 - Final deliverables

Expected final files:

```text
portfolio_repositories_bdelnoz_analyse_filtered_V3.md
portfolio_repositories_bdelnoz_analyse_filtered_V3.pdf
```

Optional support file:

```text
portfolio_collect_used_for_V3.zip
```

---

## 14. Next action

Run Phase 0 first.

Then paste/upload the generated report for validation before collecting the final ZIP.
