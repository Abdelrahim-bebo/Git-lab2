# Git Lab 2

## Overview

This lab demonstrates basic Git operations including:

* Creating a local repository and pushing it to a remote repository
* Creating and managing branches
* Merging branches into the main branch
* Deleting branches locally and remotely
* Switching branches without committing changes
* Creating and managing tags
* Adding images to the README file

---

# 1. Create a Local Repository and Push to Remote

Initialize a new Git repository:

```bash
mkdir git-lab2
cd git-lab2
git init
```

Create a README file and commit it:

```bash
touch README.md
git add .
git commit -m "Initial commit"
```

Add the remote repository:

```bash
git remote add origin https://github.com/USERNAME/REPOSITORY.git
```

Push the project to the main branch:

```bash
git branch -M main
git push -u origin main
```

---

# 2. Create Branches and Add Files

Create the **dev branch**:

```bash
git checkout -b dev
touch dev.txt
git add dev.txt
git commit -m "Add dev file"
git push origin dev
```

Create the **test branch**:

```bash
git checkout -b test
touch test.txt
git add test.txt
git commit -m "Add test file"
git push origin test
```

---

# 3. Merge Changes into Main Branch

Switch to the main branch:

```bash
git checkout main
```

Merge the branches:

```bash
git merge dev
git merge test
```

Push the updated main branch:

```bash
git push origin main
```

---

# 4. Removing Branches Locally and Remotely

### Delete a Local Branch

To remove a branch from your local machine:

```bash
git branch -d dev
git branch -d test
```

### Delete a Remote Branch

To remove the branch from the remote repository:

```bash
git push origin --delete dev
git push origin --delete test
```

---

# 5. Switching Branches Without Committing Changes

### Save the Changes Temporarily

```bash
git stash
```

This command stores your uncommitted changes and restores your working directory to a clean state.

### Switch to Another Branch

```bash
git checkout branch-name
```

### Restore the Stashed Changes

After switching branches, you can restore the saved changes:

```bash
git stash pop
```

This reapplies the previously saved changes to your working directory.

---

# 6. Create an Annotated Tag

Create an annotated tag named **v1.7**:

```bash
git tag -a v1.7 -m "Version 1.7"
```

---

# 7. Push the Tag to the Remote Repository

```bash
git push origin v1.7
```


# 8. List Tags

To display all tags in the repository:

```bash
git tag
```

---

# 9. Delete a Tag Locally and Remotely

Delete the tag locally:

```bash
git tag -d v1.7
```

Delete the tag from the remote repository:

```bash
git push origin --delete v1.7
```

---

# 10. Add an Image to README

Place the image inside the repository folder and reference it in the README file.

![Dog Image](dog.jpg)

git add .
git commit -m "add image to readme"
git push
