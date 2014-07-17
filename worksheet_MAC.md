Here are some quick exercises that will help you get a feel for github.  For all of these exercises, you will want your terminal open (Applications --> Utilities --> Terminal).  These instructions are for MAC users.

Exercise 1: Make a repository, and add your first file to it.

There are several ways to make your first repository.  You can either make your repository locally (i.e. on your computer) and then "push" it to github's online repository, or you can make it online and copy it to your computer.  We'll try both, so you can decide which way you like best.

## Starting locally

First, let's try making one from a local folder.  First we need to make a local git repository.  This is essentially the folder you'll be using on your computer to save your work.  We'll call our folder "myrepo".  The "cd" commany tells our terminal to go in to the folder.  (The default is for terminal to be in "home").
```
git init myrepo
cd myrepo
```
It's standard practice to add a readme file to your repository upon creation.  Our echo command has created a file called "README.md" with "My first repo" as a line of text within it.
```
echo "My first repo" >> README.md
```
Github uses the "[github flavored markdown](https://github.github.com/github-flavored-markdown/)" (similar to markdown) for text files, but you can open an .md file in any text editor.  [This](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) is a useful cheat sheet, if you want your text files to be fancy.  Otherwise, just type as if it's a text file.

Now we should probably add a file to our folder, to give it some purpose.  We have several options as to how to do this.

1. We can drag and drop an existing file

   To do this, you can quickly open your current folder by first stepping "out" of the folder using the cd command, and then opening it.
   
        cd ~
        open myrepo
       
2. We can use the mv command to rename an existing file (and by doing so move it)

   The code below moves a file from my desktop called file.m to my directory
   
        mv ~/desktop/file.m file.m
        
3. We can create a brank spanking new file.

   Of course, keep in mind that this file will be empty when you first make it.  Don't forget to include a file extension.
   
        touch file.m

   If you want to open your file, to edit it, feel free
   
        open file.m


When you're ready to save your changes and make your very first commit, go ahead and do so.  First you need to tell github what files you want to keep track of.  Using the command `git add -A .` will add absolutely everything that has changed since your last commit to your current commit (which is what we will do for our initial commit) whereas naming the file with `git add file.m` will add only the files specified.

For your first commit, and in general, you'll want to use `git add -A .`, like so:

```
git add -A .
git commit -m "Initial commit"
```

Almost done.  Now we need to make the remote repository on github.  Open up github.com and create Of course, use your username where the code says "username".

```
git remote add origin https://github.com/username/myrepo.git
```
One last step; you need to push your changes to github.com, so that they're stored online for you and others to download.

```
git push origin master
```

Done!

## Starting on Github.com
_Note: I find this way a lot easier._

Navigate to github.com on your web browser.

Click `+ New Repository`.

Name your repository myrepo, and check "Initialize this repository with a README"

You can go and edit your readme if you want, but you don't have to.  (It's a good idea to do it soon, however).

Now open your terminal and what you're going to do is clone your remote repository (the one on github.com) into a local repository.

```
git clone https://github.com/username/myrepo.git
```
In order to work in this repository, you want to change your directory in terminal
```
cd ~/myrepo
```

Now you want to add your first file. We've outlined the different ways above, so we'll jump right in here.

```
touch file.m
```

If you want to edit your file, go ahead and use `open file.m` and edit it.  *(Note: you'll need matlab if its a m-file..)*

Now let's commit those changes and share them with the world

```
git add -A .
git commit -m "Initial commit"
git push
```
*Notice how, since this is no longer our first push, we can go ahead and just write `git push` rather than `git push origin master`.  If you write `git push origin master` it'll work, but you're allowed the shortcut here on in.*

Done!
