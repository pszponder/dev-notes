# First Steps
1. Go to GitHub and select the option to create a new repository
2. You will be prompted to create a name for your remote repository
3. If you haven't created a local git repository yet, go to **Option 1**
4. If you already have a local git repository, go to **Option 2**

**NOTE:** The only difference between using SSH and HTTPS is the address of the remote repository in the line of code ```git remote add origin ...```


# Option 1: Create a New Reposityory on the Command Line

## Using HTTPS
```
echo "# yourReadmeText" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/myUsername/myRepoName.git
git push -u origin main
```

## Using SSH
```
echo "# yourReadmeText" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:myUsername/myRepoName.git
git push -u origin main
```


# Option 2: Push an Existing Repository from the Command Line

## Using HTTPS
```
git remote add origin https://github.com/myUsername/myRepoName.git
git branch -M main
git push -u origin main
```

## Using SSH
```
git remote add origin git@github.com:myUsername/myRepoName.git
git branch -M main
git push -u origin main
```
