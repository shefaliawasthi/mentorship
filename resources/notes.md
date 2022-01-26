Repository = used to organize a single project
Can contain folders, files, images, videos, spreadsheets, data sets
README = file with information about your project

hello-world repository = place where you store ideas, resources, or discuss with others
- Use the + drop-down menu, and select New repository
- In the Repository name box, enter hello-world
- In the Description box, write a short description
- Select Add a README file
- Click Create repository

Branch - version of a repository at one time, work on it and merge back to main
Create a branch
- Click the Code tab of your hello-world repository.
- Click the drop down at the top of the file list that says main.
- Type a branch name, readme-edits, into the text box.
- Click Create branch: readme-edits from main.

Commits = saved changes
Commit message = description explaining why change was made, captures edit history
Making and committing changes
- Click the README.md file.
- Click PENCIL ICON to edit the file.
- In the editor, write a bit about yourself.
- In the Commit changes box, write a commit message that describes changes.
- Click Commit changes.

Pull request = proposing change + requesting reviewer + possibly merge branch back
@mention feature asks feedback from specific people or teams
Opening a pull request
- Click the Pull requests tab of your hello-world repository.
- Click New pull request.
- In the Example Comparisons box, select the branch you made, readme-edits, to compare with main (the original).
- Look over your changes in the diffs on the Compare page, make sure they're what you want to submit.
- Click Create pull request.
- Give your pull request a title and write a brief description of your changes. You can include emojis and drag and drop images and gifs.
- Click Create pull request.
Merging your pull request
- Click Merge pull request to merge the changes into main.
- Click Confirm merge.
- Go ahead and delete the branch, since its changes have been incorporated, by clicking Delete branch.

Project boards: issues, pull requests, notes categorized as cards in columns
- PB Cards contain relevant metadata for issues and pull requests, like labels, assignees, the status, and who opened it.
- Notes = task reminders, references to issues and pull requests
- Create a reference card for another PB by adding a link to a note.
- If the note isn't sufficient for your needs, you can convert it to an issue.

Types of project boards:
- User-owned PBs: contain issues and pull requests from personal repository
- Organization-wide PBs: contain issues and pull requests from any repository that belongs to an organization. Link up to 25 repositories
- Repository PBs: scoped to issues and pull requests within a single repository.

Creating and viewing project boards:
- To create a PB for your organization, you must be a member
- If you don't have permission to view, the card will be redacted.
- Activity view = recent history, such as cards someone created or moved between columns. To access the activity view, click Menu and scroll down.
  - Filter PB cards
  - Archive cards
  - Disable PBs
  - Use GitHub's API to import a PB

Templates for PB:
- Template - Description
- Basic kanban - Track your tasks with To do, In progress, and Done columns
- Automated kanban - Cards automatically move between To do, In progress, and Done.
- Automated kanban with review - Cards automatically move between To do, In progress, and Done, with additional triggers for pull request review status
- Bug triage - Triage and prioritize bugs with To do, High priority, Low priority, and Closed


LEARN GIT BRANCHING
git commit
git branch bugFix
git checkout bugFix

if you want to create a new branch AND check it out at the same time, you can simply type git checkout -b [yourbranchname]

git merge bugFix
git rebase main

Relative commits are powerful, but we will introduce two simple ones here:
Moving upwards one commit at a time with ^
Moving upwards a number of times with ~<num>

git checkout main^ = main~1
git checkout main^^ = main~2
git checkout HEAD~4

Branch forcing with git branch -f main HEAD~3

git reset HEAD~1
git revert HEAD
git cherry-pick C2 C4

Git commit --amend to make the slight modification
git rebase -i HEAD~2
git rebase caption main

git tag v2 C3
The command git describe main would output: v1_2_gC2
Whereas git describe side would output: v2_1_gC4

git describe <ref>
<tag>_<numCommits>_g<hash> where tag is the closest ancestor tag in history, numCommits is how many commits away that tag is, and <hash> is the hash of the commit being described.

travel up commit tree: git checkout main~2
travel up+sideways to second parent: git checkout main^2
