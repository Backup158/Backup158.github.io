# Changing Author
```
git filter-branch --env-filter '
   OLD_EMAIL="bad@email.com"
   NEW_EMAIL="good@email.com"
   NEW_NAME="Name"
 
   if test "$GIT_AUTHOR_EMAIL" = "$OLD_EMAIL"
   then
     GIT_AUTHOR_EMAIL=$NEW_EMAIL
     GIT_AUTHOR_NAME=$NEW_NAME
   fi
 
   if test "$GIT_COMMITTER_EMAIL" = "$OLD_EMAIL"
   then
     GIT_COMMITTER_EMAIL=$NEW_EMAIL
     GIT_COMMITTER_NAME=$NEW_NAME
   fi
 ' -- --all
```

> [!NOTE]  
> git filter-branch is outdated and scuffed. Generally, it's recommended to use `git filter-repo`. I just don't know how to install that in VS Code and I wanted to keep these within that environment, since mixing stuff up ended up leading to me needing this anyways.

Then run `git push --force`

For VS Code, run this in its terminal.

Alt:
```
git filter-repo --commit-callback '
    if commit.author_email == b"bad@email.com":
        commit.author_email = b"good@email.com" 
        commit.author_name = b"GoodName"
        commit.committer_email = b"good@email.com" 
        commit.committer_name = b"GoodName"
' 
```
