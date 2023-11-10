Our sample team has four members: Bob, Carol, Ted, and Alice. Add a file called FUBAR.md to the main branch of the repo. When we start, everyone is totally in sync and freshly pulled from main on their individual laptops, and has FUBAR.md. Bob and Carol are pair-programming one feature in FUBAR.md on Carol’s laptop in a new feature branch, and Ted and Alice are working on another feature in a different non-main feature branch on Ted’s laptop, also in FUBAR.md.

Do this exercise four times, following the steps below: once with each team member in each role.

For the purposes of this exercise, the work you’re doing on a feature, always in FUBAR.md, consists of adding a sentence or two of “This is what Bob & Carol did on Bob’s computer when working on the first feature” and maybe a joke or something to keep your teammates amused.

Bob and Carol get their feature finished and do a A-C-P of their branch from Carol’s laptop and make a PR.
Ted & Alice review the feature, approve that it is good and subsequently merge it.
Ted & Alice then do a git pull origin main into their feature branch on Ted’s laptop ONLY and continue working on that feature.