# Git Troubleshooting Overview

<br>

```Bash
user@cloudshell:~/repo$ git push origin main 
To https://github.com/user/repo
 ! [rejected]        main -> main (non-fast-forward)
error: failed to push some refs to 'https://github.com/user/repo' 
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. If you want to integrate the remote changes,
hint: use 'git pull' before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```

Solution:
```Bash
git pull origin main --rebase
git push origin main
```