Download this repository by using `git clone`. Do not use the "Download Zip" function in GitHub. In general, you should never ever use that button:

![Do not press "Download Zip"](/img/github_do_not.png)

The command you should use is `git clone`. Copy the box highlighted above in green, and add it to the end of `git clone`. For instance:

```
git clone https://github.com/pravi-samaratunga/git_tutorial.git
```

This copies the **git repository** to your computer. A git repository contains the history of the code here. The history is recorded in a folder called `.git`, and it holds the differences between each version of the repository.

The repository versions that are kept track of are called **commits**. Each commit holds a record of the defference between it and the last commit. In general, you should commit as often as you can. Any code that you commit is safe, and can always be recovered as long as you have access to the repository.

It is important to understand that **git** and **GitHub** are not the same thing. GitHub is a website that hosts many git repositories. Git itself is simply a version control system. Git repositories do not depend on GitHub in any way, but it is often convenient to use GitHub as a central server on which to host repositories.

## git status, git add, git commit

Make a folder within the `git_tutorial` folder. Add a file to that folder. Write 3 short lines in that file. It doesn't really matter what else that file contains.

Run `git status` to see the files in the working directory. You'll notice that the file you just added is not shown, because it is inside of a folder.

We need to **add** the new file to the git index, so that git knows that it should keep track of this file:

```
git add path/to/your/file
```

You can run `git status` again to make sure that the right files have been added to the commit. Then finally, you need to commit the changes that have been made.


```
git commit
```

At this point, your terminal's text editor will pop up. Write a description of your file, then save and exit.

If you do not want to use the terminal text editor, you can instead use `git commit -m "Description of file"`. That's what I usually do.

## git remote

Run `git remote -v`. You will see two **remote** addresses for this repository. It should look something like this:

```
origin  git@github.com:pravi-samaratunga/git_tutorial.git (fetch)
origin  git@github.com:pravi-samaratunga/git_tutorial.git (push)
```

This is usually what we want. However, I'm currently a little annoyed with GitHub and do not want to host this code there.