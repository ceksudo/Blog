# TexkLab Blog Webpage
AI Research Lab

# How to Contribute

We would love to accept contribution from your weekly research paper reading in the form of blog post. The following guid will help you to know how to contribute under the blog page session of the our website.




## Contribution process

We follow the [fork and branch workflow][workflow].

There will be three Git repositories involved:

1.  *upstream* - the resolution repository on GitHub.
2.  *origin* - your GitHub fork of `upstream`. This repository
    will typically be at a URL that looks like `github.com/_your_user_name_/DAIRLab`
3.  *local* - your local clone of `origin`

### First time setup

Follow these steps to get ready for making changes to ServiceWeaver.  These
steps are only needed once and not for subsequent changes you might want to
make:

1.  Fork the `DAIRLab` repository on GitHub to create `origin`.
    Visit [Blog](https://github.com/ceksudo/Blog) GitHub repository and click the `Fork` button.

2.  Make a `local` clone of your fork.

    ```shell
    git clone git@github.com:_your_user_name_/Blog.git
    ```

3.  Add a remote pointing from `local` to `upstream`.

    ```shell
    cd Blog
    git remote add upstream git@github.com:ceksudo/Blog.git
    ```
### Making changes

Here is a detailed outline of the steps needed to make changes to Blog.


1. Make a local branch in your clone and pull any recent changes into it.

   ```shell
   git switch -c my_branch  # Pick a name appropriate to your work
   git pull upstream main
   ```

2. Make changes and commit to local branch.

   ```shell
   # ... editing, testing, ... 
   git commit ...
   ```

3. Pull any changes that may have been made in the upstream repository
   main branch.

   ```shell
   git switch my_branch
   git pull --rebase upstream main
   ```

   Note that this command may result in merge conflicts. Fix those if
   needed.

4. Push your branch to the corresponding branch in your fork (the `origin` repository).

   ```shell
   git switch my_branch
   git push origin my_branch
   ```

5. Select the branch you are working on in the drop-down menu of branches on
   https://github.com/_your_user_name_/Blog . Then hit the `Compare and pull
   request` button.

6. Respond to feedback, which may involve making new commits.
   If you made any changes, push them to github again.

   ```shell
   git switch my_branch
   git push origin my_branch
   ```

   Repeat as necessary until all feedback has been handled.

   Note: the preceding approach will cause the pull request to become a sequence
   of commits. Some people like to keep just a single commit that is amended as
   changes are made. If you are amending commits that had already been pushed,
   you will have to add `--force` to the `git push` command above.

7. Once reviewers are happy, pull any main branch changes that may
   have happened since step 3.
   
    ```shell
    git switch my_branch
    git pull --rebase upstream main
    ```

    If some changes were pulled, push again to the PR, but this time you will
    need to force push since the rebase above will have rewritten your commits.

    ```shell
    git switch my_branch
    git push --force origin my_branch
    ```

8.  Ask somebody who has permissions (or do it yourself if you
    have permissions) to merge your branch into the main branch
    of the `upstream` repository. The reviewer may do this without
    being asked.

    Select the `Squash and merge` option on https://github.com/ceksudo/Blog
    or use the command line instructions found on that page. Edit the commit message
    as appropriate for the squashed commit.

9.  Delete the branch from `origin`:

    ```
    git push origin --delete my_branch
    ```

10. Delete the branch from `local`

    ```
    git switch main
    git branch -D my_branch
    ```

### Code Reviews

All submissions, including weekend paper reading contribution from each member and general resolution blog post from members, require review. We
use GitHub pull requests for this purpose. 


## What to contribute to?
Weekend Paper Reading Contribution
   - change into `web-page` directory
   - change into `blog`
   - change into the current week `[date-month-number]` directory, eg: `2025-03-08-may` folder
   - create a markdown file using this naming converstion (index count start from 1) `[paper-paperType-AbbreviatedTitle-indexNUMBER].md` for example `paper-acl-ABCD-1.md`
   - Inside file you state your the paper title and your name using markdown styling and Then you go on to write your contribution and understanting after reading the research paper in a form that you write, revise, and restructure to showcase your thinking and understanding. eg:
   ```sh
    ---
      title: Hello Research
      authors: [ceksudo]
   ---

   Hello World
   ```
   





