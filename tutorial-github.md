# Welcome to the GitHub tutorial
We will go over some basic forking and pull requests in this short tutorial. Forks are used to either propose changes to someone else's project or to use someone else's project as a starting point for your own idea.

In this tutorial, you will fork this repository, propose some changes, and then create a `pull request` to merge the changes back into this document.

# 1. Forking
Forking means making a copy of a GitHub repository into your own account. Here's a link to the GitHub documentation on forking: https://help.github.com/articles/fork-a-repo/ for further information.

> A fork is a copy of a repository. Forking a repository allows you to freely experiment with changes without affecting the original project.

To fork the `ubcchemecar/beginners-tutorial` repository, follow these steps:

1. Go to the main page of the `beginners-tutorial` repository: https://github.com/ubcchemecar/beginners-tutorial
2. Click the Fork icon on the top right corner of the page.
3. Once the screen finishes loading, you will be redirected to a copy of the repository in your own GitHub account.

The top left corner of your screen should say

* username/beginners-tutorial
* forked from ubcchemecar/beginners-tutorial

# 2. Keeping your fork in sync
Your copy of the repository will not be automatically updated whenever the original repository (more commonly called the `upstream` repository) changes. If there are any updates to the upstream repository, your copy will not receive these changes until you sync your fork.

You will know if your fork needs to be synced if you see a similar message in your repository: 

> This branch is 4 commits behind ubcchemecar:master.

If you do not see that message (which is very likely if you just forked the repository, as there are no changes yet), skip ahead to Step 3.

To sync your fork, follow these [steps outlined in this website](http://www.hpique.com/2013/09/updating-a-fork-directly-from-github/), as follows:

1. Open the main page of your fork in GitHub
2. Click the 'Pull Request' icon
3. Click the 'Switching the Base' link
4. Click on the green 'Create a Pull Request' button
5. Type a title of your choice and the green button again
6. Scroll down and click the green 'Merge Pull Request' button and 'Confirm Merge'

**Note: ** If you do not see a 'Switching the Base' link, select your repository as the base fork (base fork means the repository you'd like to merge changes into) and ubcchemecar/beginners-tutorial as the main for (main fork means the repository you want to compare with, in this case, the upstream repository).

Your fork will now be synced with the upstream repository.

# 3. Make Modifications in Your Repository
1. Open the `tutorial-github.md` file in your fork. If you scroll down to the end of this document, you will see a section called 'Contributors'. Your task is to edit the file and add your name to the list of contributors.
2. Click on the pencil icon on the top right corner of the screen.
3. You will now be allowed to edit the file. The file is in a format called Markdown, read the side note below before you continue.
4. Scroll down and add your **name**, **your website**, a **note (if you want to)** and **today's date** to the list, using the same format as the other names.
5. When you're done, click 'Preview Changes' to make sure that the formatting is correct.
6. Type in a description and click the green 'Commit Changes' button.

Side note: Markdown is a way to style text in GitHub files. The `.md` extension in these tutorials stand for Markdown. Here are some examples of common syntax:

```
# A single hashtag is an <h1> tag
**Double stars means bolded text**
* Single star with a space means a bullet point
```

Read this guide for further information on Markdown: https://guides.github.com/features/mastering-markdown/

# 4. Create a Pull Request
1. In the main page of your fork, click on the pull request button
2. Click the green 'Create Pull Request' button
3. Type in a short and descriptive summary of what you've changed in the title and click the green 'Create Pull Request' button again.
4. If everything looks okay, we will merge your proposed changes on our side and you will see the list of Contributors updated in this repository.

**Final Note:** Always sync your fork before proposing any changes to our projects to prevent or minimize conflicts. 

# Further Steps and Reading
Here's a summary of what you've done:

1. Forked this (upstream) repository to your account: https://github.com/ubcchemecar/beginners-tutorial/
2. Made sure that your fork is sync with the upstream repository
3. Modified some text in the `tutorial-github.md` file in your fork
4. Created a pull request to propose changes to the upstream repository

![https://github.com/ubcchemecar/beginners-tutorial/blob/master/res/forked.png](https://github.com/ubcchemecar/beginners-tutorial/blob/master/res/forked.png)

Now that you know how to fork projects and create pull requests, if you see any mistakes/typos or unclear sections in these tutorials, feel free to fix them and then create a pull request! 

- The Learn Enough to Be Dangerous site provides excellent tutorials on many topics. Read the Learn Enough Git Tutorial: https://www.learnenough.com/git-tutorial and familiarize yourself with forks, pull requests and other commands such as `git commit`, `git pull` and `git push`.

# Contributors

This is a table with 4 columns, don't mess up the table. [Read this section](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#tables) and preview your changes before committing.
 
| Name          | Website                                               | Notes        | Date                 |
| ------------- |:-----------------------------------------------------:|:------------:|:--------------------:|
| Siang         | [Fire](http://siang.ubcchemecar.com/)                 | LOL          | 28th December 2016   |
| Daniel        | [Link to website](http://pengpops.ubcchemecar.com/)   | Not fire     | 29th December 2016   |

# Next Tutorial
When you're done with the Learn Enough Git tutorial, move on to the Bootstrap tutorial: https://github.com/ubcchemecar/beginners-tutorial/blob/master/tutorial-bootstrap.md
