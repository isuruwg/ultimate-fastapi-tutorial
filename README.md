# ultimate-fastapi-tutorial <!-- omit in toc -->

- [1. Keeping this repo upto date with original upstream repo](#1-keeping-this-repo-upto-date-with-original-upstream-repo)

The Ultimate FastAPI Tutorial

For detailed explanations and to follow along:

- Read the [blog post series](https://christophergs.com/tutorials/ultimate-fastapi-tutorial-pt-1-hello-world/)
- [Pre-order the course](https://academy.christophergs.com/courses/fastapi-for-busy-engineers/)

# 1. Keeping this repo upto date with original upstream repo

1. Add upstream repo as an additional remote
    ```bash
    git remote add tmpl git@github.com:ChristopherGS/ultimate-fastapi-tutorial.git
    ```
2. Fetch all branches
    ```sh
    git fetch tmpl
    ```
3. List the commits from this repository

    ```sh
    git log tmpl/main
    ```

4. There are two methods to bring changes from template in here: 
   
   4.1. Pick the commit you want to bring over to your repository

    ```sh
    git cherry-pick ce67a3c
    ```

   4.2. Use difftool to compare latest with the current repo and add changes manually

   ```bash
   git difftool tmpl/main
   ```

   If a new file that was not present in my local main was added to the template, Meld (difftool) wouldn't be able to save that file. If this is the case, you'll get an error when trying to save. for these files find the file location with `git diff tmpl/main` and do `git checkout tmpl/main path/to/new/file` to get the new file. 


5. Push the changes up to your Git remote

    ```sh
    git push origin main
    ```