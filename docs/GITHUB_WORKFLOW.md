# Guided GitHub collaboration workflow

## Roles
- **Issue owner / author:** Implements and tests the assigned feature, opens a PR, responds to feedback.
- **Reviewer:** Reads changed code, runs or traces tests, asks questions, requests corrections, and approves only when ready.
- Switch roles naturally between PRs; both partners must review at least one substantive PR per phase.

## A. Plan in GitHub Issues
1. Open **Issues → New issue** and choose **Feature task** (or paste the issue template manually if templates are unavailable).
2. Title it `Phase 1: Implement Grade` or similar. Assign one partner.
3. Write the expected methods, acceptance criteria, dependencies, and tests.
4. Use labels such as `phase-1`, `in-progress`, `needs-review`, `blocked`, `done` if available. Labels are optional; an Issue checklist and comments are sufficient.
5. Comment when blocked; mention the partner with `@username` and describe what is needed.

## B. Branch and code
Starting from the current `main`:
```bash
git switch main
git pull origin main
git switch -c feature/grade-class
# edit files, compile, test
git add src/Grade.java
git commit -m "Implement numeric and letter grade conversion"
git push -u origin feature/grade-class
```
Use your own branch name and filenames. Never work directly on `main`.

## C. Open a pull request
1. GitHub → **Pull requests → New pull request**.
2. Set **base** to `main`, **compare** to your feature branch.
3. Summarize changes, link the Issue (`Closes #NUMBER`), and list tests/results.
4. Request your partner as reviewer. If GitHub review requests are unavailable, tag them in a PR comment.
5. Wait for review before merging.

## D. Review a pull request
1. Open the PR → **Files changed**; read all relevant changes.
2. Confirm required methods and class responsibilities; trace at least one normal and one edge case.
3. Check that the code compiles and the author has tested it. Run tests locally when possible.
4. Leave at least one **specific, useful comment**: identify a line, ask a question, propose a test, or explain a logic concern.
5. Submit **Comment**, **Request changes**, or **Approve** as appropriate. Approval without substantive review is not sufficient for this project.

Examples of useful comments:
- “What happens when the target array has only one grade? Does `getAverageMinusLow()` divide by zero?”
- “Could this class call `myGrades.getSum()` instead of recomputing the total?”
- “I tested a score of 89.9; it correctly returns B.”

## E. Respond, update, and merge
1. Author replies to comments and pushes any fixes to the same branch; the PR updates automatically.
2. Reviewer checks the changes and approves when requirements are met.
3. Confirm the branch builds and the integrated behavior is correct.
4. Merge the PR into `main` using GitHub's **Merge pull request** control. Prefer **Squash and merge** only if the teacher directs it; ordinary merge preserves the individual commits for review.
5. Confirm the linked Issue closes or close it manually; update the phase checkpoint.

## F. Update a branch when main changes
```bash
git switch main
git pull origin main
git switch feature/grades-class
git merge main
# resolve conflicts if prompted, compile and test
git push
```
If a merge conflict occurs, inspect both versions and discuss the intended behavior before resolving it. Do not blindly choose “ours” or “theirs.”

## Suggested status vocabulary
`To do` → `In progress` → `Ready for review` → `Changes requested` (if needed) → `Approved` → `Merged`.
Use Issues/PRs to make status visible. A GitHub Project board is optional, not required.

## Phase checkpoint
Create one Issue titled `Phase N checkpoint` and comment with:
- Merged PR links and Issues completed.
- Which sample cases passed and any known limitations.
- Which partner performed the final integration test.
- One integration problem encountered and how it was resolved (or “none”).
