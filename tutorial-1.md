# Welcome to Tutorial 1 - Introduction
Please follow this guide if you're interested in working with the software/electrical team. We are assuming that you'll be using a Windows machine but the steps are very similar for Macs too.

# 1. Download Tools
Please install the following tools:

- Sublime Text 3: https://www.sublimetext.com/3
- Github Desktop: https://desktop.github.com/

# 2. Set Up GitHub Repository
1. Sign up for a free account at www.github.com
2. Create a new repository (use the '+' plus icon at the top right corner of your screen), name your repository `<username>.github.io` (without the brackets <>, replace username with your Github username). Use the following settings: Public and tick 'Initialize this repository with a README'.
3. Navigate to the repository and create a new empty file called `index.html`.

# 3. Clone the repository
1. Navigate back to the repository and click the green `Clone or Download` button and select 'Open in Desktop'.
2. Select a folder to save the repository into.

# 4. Edit the index.html file
1. Using Sublime Text, go to 'File' and select 'Open Folder', then choose the folder where you saved the repository in.
2. Open the index.html file
3. Type in the code below.
4. Save the file and open index.html in your browser. You should see a webpage with the title `My first site` and `Hello world` as the contents.

```html
<html>
<head>
  <title>My first site</title>
</head>
<body>
  Hello World
</body>
</html>
```

# 5. Git Commit and Git Push
1. Go back to GitHub Desktop and select your repository.
2. It'll show that you have uncommitted changes. Type in a short description and click commit.
3. Click the sync button.
4. Navigate to your the GitHub.com repository in your browser and click on the index.html file.
5. If it shows the new code instead of a blank file then you've successfully `pushed` the changes to GitHub from your computer

![Source: https://www.developereconomics.com/](https://github.com/ubcchemecar/beginners-tutorial/blob/master/res/joke.png)
*Source: https://www.developereconomics.com/*

# 6. Remote Website
1. Navigate to `http://<username>.github.io/` (again without the brackets <>) and you should see your site.

# 7. Chem-E-Car Subdomain
1. Create a new file called `CNAME` in your repository.
2. In the CNAME file, type in `<username>.ubcchemecar.com`
3. Contact Siang to link your `http://<username>.github.io/` site to a Chem-E-Car subdomain, `http://<username>.ubcchemecar.com/`

**Note**: After creating the CNAME file, you'll not be able to access your site at `http://<username>.github.io/` until we have linked your site to the ChemECar sub-domain.

# 8. Further Reading
1. Read up on HTML and make a better website, something similar to http://ngaito.ubcchemecar.com/ More specifically, figure out how to change text size, bold/underline text, make horizontal lines, align text left/right/center, add images and create links.
  * Thimble by Mozilla Firefox updates in realtime the changes that you make to an .html file: https://thimble.mozilla.org/en-GB/
2. Read the Learn Enough Git tutorial: https://www.learnenough.com/git-tutorial and find out what's `git commit`, `git pull` and `git push`. 

# 9. Tutorial 2
Once you're comfortable with the basics, move on to tutorial 2: https://github.com/ubcchemecar/beginners-tutorial/blob/master/tutorial-2.md





