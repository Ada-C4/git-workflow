# Git Workflow Exercise - Monthly Observances
In this exercise we will split the class into twelve groups of two. Each group will be responsible for entering a random set of monthly observances into text files for each month of the year. Each group will have their own branch for this work, allowing them to make all updates in isolation from the other groups.

Once all groups have committed their changes and pushed them to this GitHub repo, then each group will be assigned a specific month. At this point the groups will `fetch` the branches from all other groups and merge their changes in for just the single month file that they 'own'.

At the end of this merging process we should have converged on a singular final version of the files that everyone has.


## Setup
Each team will work in a Pair Programming style with one driver and one navigator. Use the following commands to get your repository setup for the exercise:
```bash
$ cd class-exercises
$ git clone git@github.com:Ada-C4/git-workflow.git`
$ cd git-workflow
$ git branch <your-team-name> initial
$ git checkout <your-team-name>
$ git push -u origin <your-team-name>
```

## Monthly Observances
I will pass these out on paper to each team. Once you have your worksheet, please enter each observance into the appropriate month's file (`January.txt`, `February.txt`, etc.) and use `git add <month-file>` and `git commit` _after each file has been updated_.

## Merging
I will provide a list of all team branch names on the projector. Use `git fetch origin` to download all of these branches to your team's computer. Once the branches have been fetched, I will assign your team a specific month to organize.

Use the following commands to get setup for the merging stage:
```bash
$ git branch complete initial
$ git checkout complete
```

Once your team is on the `complete` branch, you can start merging in every team branch's changes _for just your month file_. Use the following commands to do so:
```bash
$ git merge <team-branch-name>
$ git reset HEAD .
$ git add <your-month-file>
$ git commit -m "Adding <team-branch-name> changes to <your-month-file>"
```

This process will likely result in a merge conflict! That's the point. You will need to open the month file in Atom and determine how to retain all of the monthly observances. Key points:
- There may be duplicates! I've added multiples of many observances to different teams' worksheets.
- The final result of your month file should be in _alphabetical order_.
