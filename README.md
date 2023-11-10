# Lab 15a

## Problem Domain

Merge conflicts occur when files get out of sync between GitHub and a user’s local code base, and Git becomes unsure of where HEAD really is.

Let’s describe and experience how a pretend team would get into that situation and then extricate themselves from it.

## Instructions

* One team member should create a repository within GitHub called mc-exercise and add all other teammates as collaborators
(in the ‘Settings’ tab, look for ‘Collaborators’ in the nav on the left of the screen.)
* Assign a member of your team to each character, and then do what they do. And do ONLY what they do.

* **Our sample team has four members**: Bob, Carol, Ted, and Alice. Add a file called `FUBAR.md` to the main branch of the repo.
When we start, everyone is totally in sync and freshly pulled from main on their individual laptops, and has `FUBAR.md`. Bob and
Carol are pair-programming one feature in `FUBAR.md` on Carol’s laptop in a new feature branch, and Ted and Alice are working on
another feature in a different non-main feature branch on Ted’s laptop, also in `FUBAR.md`.

Do this exercise four times, following the steps below: once with each team member in each role.

For the purposes of this exercise, the work you’re doing on a feature, always in FUBAR.md, consists of adding a sentence or two of
“This is what Bob & Carol did on Bob’s computer when working on the first feature” and maybe a joke or something to keep your teammates amused.

Bob and Carol get their feature finished and do a A-C-P of their branch from Carol’s laptop and make a PR.
Ted & Alice review the feature, approve that it is good and subsequently merge it.
Ted & Alice then do a git pull origin main into their feature branch on Ted’s laptop ONLY and continue working on that feature.
In the meantime…

Bob & Carol have switched to Bob’s laptop, started a new feature branch in FUBAR.md, and started working on it. They did not do a git pull
origin main and will live to regret it.
They finish that feature at the same time that Ted & Alice finish their feature.
Each team does an A-C-P and makes a PR.
They review each other’s PRs and attempt to merge them.
Merge Conflicts…

To sort out a merge conflict, check all of your project files for the markers that indicate merge conflicts, the >>>>>>>>> and HEAD lines of code.
Edit the code to remove the redundancies causing the merge conflict, and eliminate the markers.
Get everyone’s individual laptop back in sync by doing a git pull origin main into main until Git stops no longer sees any conflicts.
Then they switch partners, of course. Bob & Alice start a quick new feature on her laptop in the main branch and Ted & Carol start another new
feature of their own, also in main.
They finish these quick features, and attempt to A-C-P and create/merge PRs.
Resolve any merge conflicts in the same manner as above if there are any pending.

How could these problems have been prevented?

Review the workflow on Bob & Carol & Ted & Alice and try to identify all of the individual things that they did wrong AND all of the things that they
should have done but failed to do. Write up descriptions of those things and put those into the README of the repo.

## Description of Errors

Let's break down the problems that occurred in each scenario and discuss what each individual did wrong and what they should have done differently:

### Scenario 1: Bob and Carol

1. **Creating a Feature Branch without Pulling Main:**
   - **What they did wrong:** Bob and Carol started a new feature branch without pulling the latest changes from the main branch.
   - **What they should have done:** Before starting a new feature branch, they should have done a `git pull origin main` to ensure they have the latest changes.

2. **Pull Request and Merge:**
   - **What they did wrong:** They created a pull request and merged without waiting for Ted and Alice to review their changes.
   - **What they should have done:** Wait for Ted and Alice to review and approve their changes before merging.

### Scenario 2: Ted and Alice

1. **Reviewing and Merging Without Updating Feature Branch:**
   - **What they did wrong:** Ted and Alice reviewed and merged Bob and Carol's changes without updating their own feature branch.
   - **What they should have done:** After merging changes from the pull request, they should have done a `git pull origin main` into their feature branch to stay in sync.

### Scenario 3: Bob and Carol (Switched laptops)

1. **Starting a New Feature Branch without Pulling Main:**
   - **What they did wrong:** Bob and Carol switched to a new laptop, started a new feature branch, but did not pull the latest changes from the main branch.
   - **What they should have done:** Before starting a new feature branch on the new laptop, they should have done a `git pull origin main` to get the latest changes.

### Scenario 4: Ted and Alice (Switched laptops)

1. **Merge Conflicts:**
   - **What they did wrong:** Ted and Alice finished their feature without pulling the latest changes from the main branch, resulting in merge conflicts.
   - **What they should have done:** Before finishing their feature, they should have done a `git pull origin main` to avoid merge conflicts.

