# Welcome to Tutorial x: Server-side Scripts

In this tutorial, we will implement a simplified version of Doge Weather. http://dogeweather.com/

We will be using [Node.js](https://www.tutorialspoint.com/nodejs/nodejs_introduction.htm), a JavaScript platform for building web apps. We will then upload the web app to [Heroku](https://www.heroku.com/), a free hosting service.

# 1: Install Node.js on your computer
1. Download link available here: https://nodejs.org/en/download/
2. Follow the instructions to set up a simple Hello World program: http://blog.gvm-it.eu/post/20404719601/getting-started-with-nodejs-on-windows
3. Once you've successfully installed Node.js and have run your Hello World program, move on to the next step.


Nodejs is a whole topic in itself. It is covered well [here by Daniel Shiffman](https://www.youtube.com/watch?v=P-Upi9TMrBk&list=PLRqwX-V7Uu6Yyn-fBtGHfN0_xCtBwUkBp) . In the Youtube URL, there is a written guide there that is very helpful.


# 2: Sign Up For a Free Heroku Account
1. https://signup.heroku.com/
2. Login to your Heroku account and go to the [Dashboard](https://dashboard.heroku.com/)
3. Go to the [setup](https://devcenter.heroku.com/articles/getting-started-with-nodejs#set-up) and follow the steps on that page. 

# 3: Setting Up Git and Nodejs
1. Go to Github and create a new repository. Download to the desktop.
2. Open command shell/line and navigate to your repository
3. type ```npm init``` to create the 'package.json' and intialize nodejs; press enter for every prompt.
4. type ```npm install express --save``` to set the express module as a dependency
5. Add a file named index.js and paste this code:
```
var express = require('express');
var app = express();

app.set('port', (process.env.PORT || 5000));

app.use(express.static(__dirname + '/public'));

// views is directory for all template files
app.set('views', __dirname + '/views');
app.set('view engine', 'ejs');

app.get('/', function(request, response) {
  response.render('pages/index');
});

app.listen(app.get('port'), function() {
  console.log('Node app is running on port', app.get('port'));
});
```
6. Add a folder named 'public' and add 'index.html' inside the public folder.
7. Push these additions to the github server with: ```git add > git commit > git push origin master``` 

You've just created a node server. It differs slightly from the tutorial in step 1 but the basis is the same. Using express, you will be serving your website from the public folder. You can add other html pages there, and create any kind of front-end scripts here. You may also make changes to index.js to create RESTful routes which will be in another tutorial. As a final note. in step 3. 'index.js' is usually renamed as 'server.js'. 

#6 Deploying Heroku Web Server
1. In the command shell/line, type ```heroku create```
2. Type ```git push heroku master```
3. View your website with ```heroku open```

Any time you make changes to your web server, you will need to push it to github, and heroku. you will be using ```git push``` and ```git push heroku master``` to keep your webserver updated.



