# Step 1.  Add a file.

## 1.1. Switch back to branch `main` and create a new branch.

```bash
git checkout main
git checkout -b 01
```

## 1.2. Open VSCode

```bash
code .
```

Notice that the `README.md` file that we edited in the previous step is back to what it was in the empty repo.  This is because we made the changes in a separate branch.  When collaborating on a project, making changes in separate branches protects the `main`, working branch of the project, and the changes are reviewed and merged with previous code through the pull request process.  Here, we do not intend to merge the branches - rather, they serve as a time machine to go forward and back to follow and retrace our steps of building the project.

## 1.3. Open VSCode Terminal (```Ctrl + ` ```)

Run the commands shown in the screenshot to create two folders.

![first file added to repo](assets/images/01-VSCode.png)

## 1.4. Make a screenshot and paste into the README file.

Like in Github editor, the image is pasted as a new file, and a link to new file appears in the editor.  Rename this file and move it to `assets/images`.