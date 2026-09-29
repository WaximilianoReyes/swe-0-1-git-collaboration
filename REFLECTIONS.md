Reflection Questions:
Where does your code live? Describe (or sketch and include an image of) where your changes exist after each step: after you save the file, after git add, after git commit, after git push, and after your partner runs git pull. At which point can your partner see your work?

Your predictions vs. reality. In Round 1, step 5, you each predicted what would happen when Partner B pushed. What did each of you predict, and what actually happened? Using what you know now, explain why git rejected the push. Then explain what git pull did that the push couldn't.

Resolving a conflict. Pick one of the two conflicts you resolved (Round 1 or Round 2). How did you and your partner decide what to keep? How did you confirm the resolution was correct before pushing?

Getting unstuck. Describe one moment when something didn't work or didn't match what you expected, in the warm-up or while writing the story. What was the exact message or result? What did you check first (for example git status or git remote -v), and what fixed it?

Commit messages for a team. Look at your commit history on GitHub. Pick the most useful commit message and the least useful one, and rewrite the weak one here (you don't need to change the message on GitHub). Then explain: if five people were working in this repo instead of two, why would clear commit messages and pulling before you start matter even more?

1. The code lives in both our local repository and our remote repository. When configuring and editing the code, we make these changes in our local repo, but once we want those changes applied to the public remote repo, we must git add, git commit, and git push to that remote repo. The remote repo is a copy of our local code, but saved on a server like GitHub, where anyone can see or fork it. When code is configured and saved locally, it is saved in the local repo before being sent to the remote repo. In this project, all changes were made to files inside the swe-0-1-git-collaboration repo, and the main changes were in main.py. The path is development/mod-0/swe-0-1-git-collaboration. To save these changes to the remote repo, you use git add {file name}, or git add -A for all edited files, which adds them to the staging area. From the staging area, you use git commit -m "", which commits the change to the local repo and saves a snapshot of that moment with a message. You then have to push these changes and the snapshot to the remote repo using git push. The partner then pulls those changes from the remote repo to his local repo using git pull, and at this point he can see all the changes that were made.

2. Our predictions about the merge conflict were similar to the results. We predicted that once we had different code written on the same line, there would be some kind of conflict when we both tried to push. We predicted that GitHub wouldn't be able to read our files due to the different lines of code. When one of us pushed, nothing happened, but when Partner B tried pushing with different edits on the same line, there was an error stating that they had to pull to match the main branch, since they didn't have the up-to-date version of the repo or file. It got rejected because there was a mismatch between the file versions in the local and remote repos. When we pulled, we got the option to keep the changes made by Partner A, keep the changes made by Partner B, or combine them. We then decided what to keep and what to remove and pushed it to Git accordingly. Git pulled those changes, while pushing would only have created more conflicts on the same lines in the remote repo.

3. We had a conflict with the title, where we both entered different title names. I pushed after his initial push, which gave me the merge conflict. I then pulled and was given the option to combine the two edits or choose one of them. We decided not to choose either one; instead, we scrapped both ideas and created a new title. We then ran the file using python3 to make sure it ran and output what we needed.

4. After we switched positions and one of us tried to pull the merged changes, we received this error: "Your local changes to the following files would be overwritten by merge: main.py." We ran git status, which gave us:
Your branch is behind 'origin/main' by 4 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   main.py

At this point, pulling wasn't working, so we restored the main.py file to discard the changes in the working directory. This resolved the issue and let us pull the updated repo.

5. One commit message we could rewrite is "adding another line to the story." This commit message is very broad and not specific enough for others to work with. I would rewrite it as "added a print string line to line ()," including a short description of what was added to the story on that line. A clearer, more specific commit message would help other people working on the repo understand exactly what that change was, or what changes that snapshot made to the code or files. An unclear message can cause confusion and leave people with more questions than necessary when working on the repo. Nobody wants to look through every line of code to figure out what changes you made.