#  Git & GitHub — The Complete Handbook  
### *From "what is a commit?" to "yes, I actually understand rebase now"*

---

> *Once upon a time, a developer opened a terminal, typed `git push --force`, and destroyed 3 days of their team's work.*
> *That developer was not me. But I watched it happen in real time.*
> *This handbook exists so neither of us becomes that person.* 

---

##  The Origin Story (a.k.a. Why This Exists)

You know that feeling when you've been staring at a `CONFLICT` message for 45 minutes,  
your tea has gone cold, your girlfriend has texted "you coming or not?",  
and Stack Overflow has 12 tabs open — all saying something different?

Yeah. That's called **being a software engineer**. Welcome to the club. There's no exit.

I'm a developer who got tired of Googling the same Git commands every Monday morning  
like some kind of goldfish with a laptop. So I built the notes I *wish* existed when I started.

Not copy-pasted docs. Not a YouTube video that's "6 hours but trust me bro."  
Just **real notes, real examples, real pain** — written like a friend who's already  
stepped on all the landmines and wants to warn you before you do too.

---

###  What's Inside This Vault of Suffering and Wisdom

| Topic | Reality Check |
|-------|---------------|
| Every Git command you'll actually use | With examples that aren't `git commit -m "fix"` (we have standards) |
| Windows  Linux  Mac  specific steps | Because "just type this" never works the same on all three |
| Authentication — PAT classic, fine-grained, SSH, GitHub CLI | GitHub changed auth *again*. Yes, again. It's fine. It's fine. |
| Branching, merging, rebasing, cherry-picking | The Four Horsemen of "wait what just happened to my code" |
| Undoing mistakes | The most-used feature in software engineering, don't @ me |
| Git hooks, submodules, bare repos, `git bisect` | The stuff seniors mention to sound smart at standups |
| Full GitLens + VS Code guide | Commit Graph is free since v14. The senior devs are shook. |
| Team workflows, branch protection, PR review cycles | How to not get roasted in code review |
| Troubleshooting — 8 real errors with exact fixes | Because `fatal: not a git repository` has ruined more mornings than Mondays |
| Pro tips, aliases, best practices | So you stop typing `git status` 17 times a day |

> **Tone:** Beginner-friendly + aggressively funny. Because life's too short for dry documentation.

---

##  Repository Structure

*Organised like a senior dev's brain: everything has a place, and the place actually makes sense.*

```
git-and-github/

  README.md                          ← You are here. The whole map.

  00_cheatsheet/
    01_quick_reference.ipynb         ←  All commands on one page (bookmark this NOW)

  01_basics/
    01_what_is_git.ipynb             ← Git vs GitHub — yes they're different, no you're not dumb
    02_installation.ipynb            ← Install on Windows / Linux / Mac (with zero drama)
    03_core_concepts.ipynb           ← Key terms: repo, commit, branch, HEAD, staging...

  02_setup/
    01_configuration.ipynb           ← git config, aliases, identity (tell Git who you are)
    02_authentication.ipynb          ← PAT classic & fine-grained, SSH, gh CLI — all explained

  03_workflow/
    01_complete_workflow.ipynb       ← Clone/init → edit → add → commit → push. The daily loop.
    02_team_workflow.ipynb           ← Multi-dev sync, branch protection, review hell cycles

  04_commands/
    01_status_log_diff.ipynb         ← status, log, diff, blame, reflog
    02_add_commit.ipynb              ← add, commit, amend, writing commits that don't say "fix"
    03_push_pull_remote.ipynb        ← push, pull, fetch, remote juggling
    04_stash_tags_clean.ipynb        ← stash (panic mode), tags, clean, rm, mv
    05_submodules_bare.ipynb         ← git init --bare, submodules (advanced stuff, flex worthy)
    06_hooks_bisect.ipynb            ← pre-commit hooks, git bisect (find who broke prod)

  05_branching/
    01_branches.ipynb                ← Create, switch, rename, delete — branch like a pro
    02_merging.ipynb                 ← Merge + conflict resolution (the CONFLICT moment)
    03_rebase_cherrypick.ipynb       ← Rebase + interactive -i + cherry-pick (power moves)

  06_undoing/
    01_recovery.ipynb               ← restore, reset, revert, reflog — undo everything

  07_github_features/
    01_pull_requests_forks.ipynb    ← PRs, forks, open source contribution flow
    02_gitignore_actions.ipynb      ← .gitignore patterns, GitHub Actions CI/CD

  08_gitlens_vscode/
    01_gitlens_guide.ipynb          ← GitLens: blame, branches, free Commit Graph (v14+)

  09_troubleshooting/
    01_errors_fixes.ipynb           ← 8 common errors + exact fixes. You'll need this.

  10_pro_tips/
     01_tips.ipynb                   ← Aliases, strategies, golden rules — the good stuff
```

---

##  Full Chapter Navigation

*Because scrolling through folders is what we do at 2am when we should be sleeping.*

| # | Chapter | File | What You'll Learn |
|---|---------|------|-------------------|
|  | **Quick Reference** | [00_cheatsheet/01_quick_reference](00_cheatsheet/01_quick_reference.ipynb) | Every command in one place. Print it. Put it on your wall. |
| 1 | What is Git? | [01_basics/01_what_is_git](01_basics/01_what_is_git.ipynb) | Git vs GitHub. Yes they're different. No, "the cloud" is not Git. |
| 2 | Installation | [01_basics/02_installation](01_basics/02_installation.ipynb) | Install on Windows/Linux/Mac. Different pain, same destination. |
| 3 | Core Concepts | [01_basics/03_core_concepts](01_basics/03_core_concepts.ipynb) | Repo, commit, branch, HEAD, staging — the vocab that unlocks everything |
| 4 | Configuration | [02_setup/01_configuration](02_setup/01_configuration.ipynb) | `git config` — first date with Git. Tell it your name. Be honest. |
| 5 | Authentication | [02_setup/02_authentication](02_setup/02_authentication.ipynb) | PAT classic & fine-grained, SSH, gh CLI. GitHub's bouncer is strict. |
| 6 | Complete Workflow | [03_workflow/01_complete_workflow](03_workflow/01_complete_workflow.ipynb) | Clone → edit → add → commit → push. The loop you'll do 500 times. |
| 7 | Team Workflow | [03_workflow/02_team_workflow](03_workflow/02_team_workflow.ipynb) | Multi-dev sync. How to not step on each other's code (mostly). |
| 8 | Status, Log, Diff | [04_commands/01_status_log_diff](04_commands/01_status_log_diff.ipynb) | `git status`, `git log`, `git diff`, `git blame` — detective toolkit |
| 9 | Add & Commit | [04_commands/02_add_commit](04_commands/02_add_commit.ipynb) | Stage files, write commits that aren't "final final v3 REAL FINAL" |
| 10 | Push, Pull, Remote | [04_commands/03_push_pull_remote](04_commands/03_push_pull_remote.ipynb) | `git push`, `git pull`, `git fetch` — syncing with the mothership |
| 11 | Stash, Tags, Clean | [04_commands/04_stash_tags_clean](04_commands/04_stash_tags_clean.ipynb) | Stash = panic button. Tags = official milestone. Clean = delete everything scary. |
| 12 | Submodules & Bare | [04_commands/05_submodules_bare](04_commands/05_submodules_bare.ipynb) | Advanced stuff. Mention in standup for +5 respect. |
| 13 | Hooks & Bisect | [04_commands/06_hooks_bisect](04_commands/06_hooks_bisect.ipynb) | Hooks = automatic code police. Bisect = find who broke prod (it was you). |
| 14 | Branches | [05_branching/01_branches](05_branching/01_branches.ipynb) | Create, switch, rename, delete branches. Your code has a multiverse now. |
| 15 | Merging | [05_branching/02_merging](05_branching/02_merging.ipynb) | Merge + conflict resolution. CONFLICT is not the end of the world. Probably. |
| 16 | Rebase & Cherry-pick | [05_branching/03_rebase_cherrypick](05_branching/03_rebase_cherrypick.ipynb) | Rebase, interactive -i, cherry-pick. Power moves that impress seniors. |
| 17 | Undoing & Recovery | [06_undoing/01_recovery](06_undoing/01_recovery.ipynb) | `git restore`, `git reset`, `git revert`, `git reflog` — Git's undo button(s) |
| 18 | Pull Requests & Forks | [07_github_features/01_pull_requests_forks](07_github_features/01_pull_requests_forks.ipynb) | PRs, forks, contributing to open source like a professional |
| 19 | .gitignore & Actions | [07_github_features/02_gitignore_actions](07_github_features/02_gitignore_actions.ipynb) | Stop committing `node_modules`. Please. I'm begging you. |
| 20 | GitLens in VS Code | [08_gitlens_vscode/01_gitlens_guide](08_gitlens_vscode/01_gitlens_guide.ipynb) | Blame, tracking, free Commit Graph (v14+). See who wrote that terrible code. |
| 21 | Troubleshooting | [09_troubleshooting/01_errors_fixes](09_troubleshooting/01_errors_fixes.ipynb) | 8 real errors + exact fixes. Bookmark this. You'll be back. |
| 22 | Pro Tips | [10_pro_tips/01_tips](10_pro_tips/01_tips.ipynb) | Aliases, strategies, golden rules — the stuff no one tells you in tutorials |

---

##  How to Actually Use This

*Like reading a textbook but written by someone who was also confused once.*

1. **Open the repo in VS Code** — you're already here, so good job, 10/10 start
2. **Jump into any folder** using the table above — it's all linked, no scrolling needed
3. **Open any `.ipynb` file** — all cells are plain readable notes, nothing to run
4. **Try every command in your own terminal** as you read — muscle memory > theory
5. **When something breaks** — go to `09_troubleshooting/` immediately, then panic

**If you're brand new and have no idea where to start (same tbh):**

```
01_basics/01_what_is_git.ipynb
  → 01_basics/02_installation.ipynb
    → 02_setup/01_configuration.ipynb
      → 03_workflow/01_complete_workflow.ipynb
        → (you're dangerous now)
```

>  **Pro tip:** Don't try to memorize everything. Learn the *pattern*, use the cheatsheet for the rest.  
> Seniors don't memorize commands — they just know where to look faster.

---

##  Tools That Power This Handbook

| Tool | What It Does | Hot Take |
|------|-------------|----------|
| **Git** | Version control system | The reason your job exists |
| **GitHub** | Cloud hosting + collaboration | Tinder for code, but the matches actually work |
| **VS Code** | Editor | Your second home. Your first home is questionable. |
| **GitLens** | Visual Git superpowers in VS Code | Like X-ray vision for your codebase. For FREE (v14+). |
| **Jupyter Notebooks** | Readable, organised notes | Markdown + code in one. The engineer's diary. |

---

##  Real Talk — Chapters You'll Definitely Skip Then Come Back to Crying

| Chapter | When You'll Actually Open It |
|---------|------------------------------|
| `01_recovery.ipynb` | 11:47pm. Deadline tomorrow. You just did `git reset --hard`. |
| `06_hooks_bisect.ipynb` | After getting roasted in code review for the 4th time this week |
| `02_authentication.ipynb` | Every time GitHub rejects your push and your token expired AGAIN |
| `02_merging.ipynb` | The moment you see `<<<<<<< HEAD` and your soul leaves your body |
| `01_errors_fixes.ipynb` | Immediately after any `fatal:` message at 1am |
| `01_tips.ipynb` | Never. Then suddenly at 3am you're reading the whole thing. Same. |

---

##  Quick Command Reference (The "I Need This NOW" Section)

*For when you're mid-panic and don't have time to open a notebook.*

```bash
# === SURVIVAL KIT ===
git status                        # What's going on? (Ask this constantly)
git add .                         # Stage everything (like "select all" but for files)
git commit -m "your message"      # Save a checkpoint  
git push                          # Upload to GitHub
git pull                          # Download latest changes

# === UNDO PANIC KIT ===
git restore <file>                # Undo changes in a file (before staging)
git reset HEAD~1                  # Undo last commit (keep changes)
git stash                         # Hide messy work temporarily
git reflog                        # Find literally any commit ever (time machine)

# === BRANCH KIT ===
git branch feature-name           # Create branch
git switch feature-name           # Switch to it
git merge feature-name            # Merge it back
git branch -d feature-name        # Delete after merge

# === THE "WHAT DID I DO" KIT ===
git log --oneline                 # Short history
git diff                          # What changed?
git blame <file>                  # Who wrote this line? (find the culprit)
```

---

*Made with  frustration,  coffee, and the iron will to never Google*  
*"how to undo a git commit" more than once. (Reader, I Googled it 47 more times.)*
