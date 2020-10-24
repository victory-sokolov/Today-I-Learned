# Refusing to pull to local repo

I got this error when i set up locall repository first and then i create a new Github repository and run

```
git remote add origin <repository url>
```

When i do pull i got the error:
```
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
```

Error fixed by doing:
```
git pull origin master --allow-unrelated-histories
```
