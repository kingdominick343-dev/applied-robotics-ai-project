# Applied Robotics and AI Project

Workspace and project management documentation for Assignment 1.

## Project board
[Trello: Applied Robotics and AI Project](https://trello.com/b/itvwndWJ/applied-robotics-and-ai-project)

## Setup
```sh
git clone https://github.com/kingdominick343-dev/applied-robotics-ai-project.git
cd applied-robotics-ai-project
git remote -v
```
Git must be installed. Configure your own Git author name and email before making local commits, and authenticate to GitHub before pushing. Never commit passwords, tokens or private data.

## Add, Commit and Push
- **Add** stages selected working-file changes for the next commit: `git add README.md`. If you edit again, stage again.
- **Commit** records staged changes in local history: `git commit -m "Describe the change"`. It does not upload them.
- **Push** sends local commits to GitHub: `git push`. It does not include uncommitted files.

Working directory -> Add -> staging area -> Commit -> local history -> Push -> remote repository. Add and Commit work offline; Push requires access to the remote.

## Branching and review workflow
Keep `main` as the reviewed baseline. Use one short-lived branch per task, with a descriptive name such as `docs/workspace-demo`.
```sh
git switch -c docs/workspace-demo
# Edit and save README.md in a text editor.
git status
git diff
git add README.md
git diff --staged
git commit -m "Add verified workspace demonstration progress"
git push -u origin docs/workspace-demo
```
Open a pull request into `main`, review the changes, then merge when ready. Link the PR on its Trello card. These commands are a demonstration guide, not evidence that the terminal steps have already been run.

## Trello workflow
- **To Do:** defined tasks with acceptance criteria, labels and due dates.
- **In Progress:** work actually underway; aim for a maximum of two cards.
- **Done:** verified completed work, with repository or PR links.

Update cards and make meaningful commits throughout the project. Keep genuine dated screenshots and brief retrospectives. Setup activity on one day does not establish earlier continuous use.

## Assignment checklist
- [x] Create repository and initial README.
- [x] Document setup, Git stages and branching workflow.
- [ ] Confirm lecturer invitations/access to Trello and GitHub.
- [ ] Record a 5-10 minute video demonstrating Trello and Git, including Clone, Edit, Add, Commit, Push and branching.
- [ ] Present genuine evidence of ongoing tool use.
- [ ] Submit video and written discussion by 20 October 2026, 11:30 pm.
