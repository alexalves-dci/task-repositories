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