# Synchronization log

So far I learned that:
- I created an empty repository on GitHub called `task-repositories` with no README.md
- I copied the SSH URL: `git@github.com:alexalves-dci/task-repositories.git`
- In WSL, I used `cd ..` to leave `test-repo` and return to `04-github`
- I used `mkdir task-repositories` to create the local folder and `cd task-repositories/` to enter it
- I run `git init` to make the folder a local Git repository
- With `git status`, I saw that I was on `main`, with no commits yet
- I used `git remote add origin git@github.com:alexalves-dci/task-repositories.git` to connect my local repository to the GitHub address
- With `git remote -v`, I checked that the address was saved for fetching and pushing
- I learned that `origin` is a nickname for the remote repository, not my GitHub username
- In my first repository, I used `git clone`, which downloaded the repository and automatically set up `origin`
- This time I used `git init`, which only created the local repository, so I needed to add the remote connection myself
- I created README.md and sync-log.md locally and used `code .` to open the folder in VS Code
- VS Code updated its WSL server before opening the folder. It was an update and did not remove my project files

What worked well:
- I created the local repository and added the remote without errors
- I checked the remote URL and it matched my GitHub repository

What confused me:
- I did not remember using `origin` before, but now I understand that `git clone` had set it up automatically
- I thought the VS Code update might affect my files, but it was only updating the server inside WSL

Second phase:
- I corrected the filename from `synch-log.md` to `sync-log.md`
- I staged README.md and sync-log.md, then used `git status` to check that both files were ready to be committed
- I used `git commit -m "1st Commit"` to save my first local snapshot
- With `git status`, I saw that the working tree was clean
- I used `git push -u origin main` to send my commits to GitHub and set up tracking between my local `main` and `origin/main`
- I refreshed GitHub and saw both files there

Third phase:
- I edited README.md directly on GitHub, added a sentence and committed the change
- I noticed that GitHub showed both sentences in one paragraph. I learned that Markdown needs an empty line between separate paragraphs
- I used `git pull` to bring the new GitHub commit into my local repository
- I checked README.md locally and saw the new sentence
- With `git status`, I saw that my branch was up to date with `origin/main` and the working tree was clean

What worked well:
- My first push sent both files to GitHub
- The pull brought my GitHub change into my local copy without errors

What confused me:
- I confused the repository name and my username with `origin`. Now I understand that `origin` is the saved nickname for the remote address
- I confused push and pull. `git push` sends local commits to GitHub, while `git pull` brings changes from GitHub into my local branch

Fourth phase:
- I updated sync-log.md locally in VS Code with my progress and what confused me
- With `git status`, I saw that sync-log.md was modified but not staged
- I used `git add sync-log.md` to prepare the changes
- I used `git commit -m "Added 2nd phase"` to save a new snapshot locally
- With `git status`, I saw that my branch was ahead of `origin/main` by one commit. This meant that the new commit was still only on my computer
- I used `git push` to send that commit to GitHub
- I refreshed GitHub and checked that my updated notes appeared there

Reflection:
- A remote is another repository that my local repository can exchange commits with. In this task, it is hosted on GitHub and its nickname is `origin`
- `git push` sends my local commits to GitHub
- `git pull` brings changes from GitHub into my local branch
- As a Brazilian, I confused push with “puxar” because they sound similar! Now I remember: push means “empurrar” and pull means “puxar”
- With test-repo, I created the repository on GitHub first, then used `git clone` to copy it locally and automatically set up `origin`
- With task-repositories, I started locally with `git init`, added the remote myself and pushed my first commit to the empty GitHub repository
- Both ways let me use push and pull afterward. The difference is how I started
