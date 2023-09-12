# Step 0. Empty repo

![image](https://github.com/liquidcarbon/fastbuilder/assets/47034358/e15f6f32-fb49-4757-aef3-26510d27d953)

## 0.1. Clone and create a new branch

```bash
a@SNAVVV:~/code$ git clone https://github.com/liquidcarbon/fastbuilder.git
Cloning into 'fastbuilder'...
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (4/4), done.
remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (4/4), 2.13 KiB | 2.13 MiB/s, done.
a@SNAVVV:~/code$ cd fastbuilder/
a@SNAVVV:~/code/fastbuilder$ git checkout -b 00
Switched to a new branch '00'
a@SNAVVV:~/code/fastbuilder$ git status
On branch 00
nothing to commit, working tree clean
a@SNAVVV:~/code/fastbuilder$ git push -u origin 00
Total 0 (delta 0), reused 0 (delta 0)
remote:
remote: Create a pull request for '00' on GitHub by visiting:
remote:      https://github.com/liquidcarbon/fastbuilder/pull/new/00
remote:
To https://github.com/liquidcarbon/fastbuilder.git
 * [new branch]      00 -> 00
Branch '00' set up to track remote branch '00' from 'origin'.
```


## 0.2. Edit README.md

Editing README file in the browser makes it easy to add images.  Simply hit "Paste" while in the editor:
![image](https://github.com/liquidcarbon/fastbuilder/assets/47034358/224976b4-7b80-43da-bf5a-bed8cec99086)

The image gets uploaded into a special place on Github.  A markdown link appears in the web editor.
![image](https://github.com/liquidcarbon/fastbuilder/assets/47034358/340ed960-ae35-444f-8298-e9c25c010a98)

Now press "Commit changes".
![image](https://github.com/liquidcarbon/fastbuilder/assets/47034358/fff67f6c-f8d0-45a9-969d-18a854e53b0c)


## 0.3. Pull the changes locally

`git pull`
