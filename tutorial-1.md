# Welcome to Tutorial 1 - Introduction
Please follow this guide if you're interested in working with the software/electrical team. We are assuming that you'll be using a Windows machine but the steps are very similar for Macs too.

# 1. Download Tools
Please install the following tools:

- Sublime Text 3: https://www.sublimetext.com/3
- Github Desktop: https://desktop.github.com/

Check out the Student Developer Pack by Github, which includes FREE access to many developer tools: https://education.github.com/pack

# 2. Set Up GitHub Repository
1. Sign up for a free account at www.github.com
2. Create a new repository (use the '+' plus icon at the top right corner of your screen for Windows/ top left corner for Macs), name your repository `<username>.github.io` (without the brackets <>, replace username with your Github username). Use the following settings: Public and tick 'Initialize this repository with a README'.
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
2. It'll show that you have uncommitted changes (blue dot next to 'Changes' button located at the top for Windows/'Uncommitted Changes' for Macs). Type in a short description and click commit.
3. Click the sync button.
4. Navigate to your the GitHub.com repository in your browser and click on the index.html file.
5. If it shows the new code instead of a blank file then you've successfully `pushed` the changes to GitHub from your computer

![Source: https://www.developereconomics.com/](https://github.com/ubcchemecar/beginners-tutorial/blob/master/res/joke.png)
*Source: https://www.developereconomics.com/*

# 6. Remote Website
1. Navigate to `http://<username>.github.io/` (again without the brackets <>) and you should see your site.

# 7. Chem-E-Car Subdomain
We will link your `http://<username>.github.io/` to a Chem-E-Car subdomain at `<USERNAME>.ubcchemecar.com`. Your `<USERNAME>` for the Chem-E-Car sub-domain can be the same as your GitHub username, or something different if you want to change it.

1. Create a new file called `CNAME` (this file should have no extension, easier to do on Github website by clicking the 'Create new file' button) in your repository.
2. In the CNAME file, type in `<username>.ubcchemecar.com`
3. Contact Siang to link your `http://<username>.github.io/` site to a Chem-E-Car subdomain, `http://<username>.ubcchemecar.com/`

**Note**: After creating the CNAME file, you'll not be able to access your site at `http://<username>.github.io/` until we have linked your site to the ChemECar sub-domain. DNS propagation can take up to 24 hours or more (but it's usually an hour or less), while waiting for your site to load, read up on [DNS Propagation](https://support.managed.com/kb/a604/dns-propagation-and-why-it-takes-so-long-explained.aspx).

# 8. Beyond Hello World
Read up on HTML and make a better website, something similar to http://ngaito.ubcchemecar.com/ 

More specifically, 

1. Figure out how to change text size, bold/underline text, make horizontal lines, align text left/right/center, add images and create links.
2. For each change that you make, practice making new commits and pushing them to your GitHub repository.
3. Google is your friend, but if you can't find something or if you're stuck, message us in the FB group chat.

Here are some good sources to get you started:
  * If you're using Chrome, press Ctrl+U to view the source of a web page. For example, navigate to http://ngaito.ubcchemecar.com/ then click Ctrl+U. For other browsers, Google for the shortcut key.
  * [Find out what is HTML](http://www.yourhtmlsource.com/starthere/whatishtml.html)
  * [Find out what is CSS](http://html.net/tutorials/css/lesson1.php)
  * Handy tool: Thimble by Mozilla Firefox updates in realtime the changes that you make to an .html file: https://thimble.mozilla.org/en-GB/
  
### Important Notes 

1. Files uploaded to GitHub are case sensitive, `myphoto.jpg` is not the same as `myphoto.JPG`. To avoid potential headaches, always use lower case for the file extensions (i.e. jpg, not JPG) and the file names `myphoto.jpg` not `Myphoto.jpg`, unless you have a good reason not to.

2. There are a few rules and conventions for naming and organising files for websites:

- Use lowercase exclusively when naming files, as some web servers are sensitive to case.
- Use alphanumerics only in page names. That is, a-z, 0-9. The only exceptions are: -(dash), _(underscore) and ~ (tilde).
- Never use spaces in the file name of anything destined for the web, as spaces will be encoded by the server, producing long and ugly URLs. Replace spaces with hyphens.
- When planning a site, create a naming convention for files and stick to it without exception.

Source: https://thenewcode.com/30/HTML-naming-conventions-and-file-management
  
# 9. Next Tutorial
Once you're comfortable with the basics, work through our (short) GitHub tutorial: https://github.com/ubcchemecar/beginners-tutorial/blob/master/tutorial-github.md




