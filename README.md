# `git` common root

This project serves as a common root, or initial commit,
for all
future projects
that I start.

## Problem

The problem that this `git` repo seeks to solve is that of no common root to repos.
When you have no common root, you cannot merge two repositories,
and this has been an issue for me in the past
when I realized that two projects were more related than previously thought
or I otherwise wanted to combine two previously unrelated projects.

## Solution

The solution is
a repository such as this,
which contains the common root for all future projects.

## How to help

I do not recommend using this common root because it will have me as the contributor.
Instead:
1. Create your own `git` common root project.
2. Then, I recommend giving it an empty commit.
   The message should describe that this is the first commit of the project.
   ```bash
   git commit --allow-empty -m "initial commit"
   ```
   I named mine "started project", which is not the most ideal name,
   but I didn't know that it would be used for this at the time, and it has hence been repurposed.
   Also, I don't recommend referring
   to the branch because
   any commit
   can be copied to another branch in the future. 
3. Proceed with more commits for the common root as you would.
   However the reason I recommend an empty commit is because
   it's very unlikely that there will be any templating content
   that will be a useful initial for every single project you create. However, if you do, please feel free to use it.
4. Tag the root to make it easy to which to return.
   ```bash
   git tag -m "the common root" ROOT
   ```
4. Make a second commit with an explanatory message such as this one, and
5. go ahead and push to the `master` branch, but also push the ROOT tag.
   ```bash
   git push origin ROOT
   ```

When starting a new project, you can then
1. Clone your own `git` common root.
   ```bash
   git clone <url to your common root remote.git> <new project directory>
   ```
2. Change the remote to your new repository.
   ```bash
   cd <new project directory>
   git remote set-url remote <url to your new project remote.git>
   ```
3. Reset to the root.
   ```bash
   git reset --hard ROOT
   ```

From there you could continue as normal.

## Started which project?

Now this refers to this project.
However originally "my the project" referred
to a JavaScript Mad Libs laboratory assignment that I did completed in college.
This was my earlier project that I could find since I found out that you can create empty commits.
