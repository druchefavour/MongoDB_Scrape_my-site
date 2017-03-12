# MongoDB Scrape My Website Project

* In this project, a web app that lets users leave comments on the latest news is created. The app will use Mongoose and Cheerio to scrape news from Houston Chronicles.
* In the app, whenever a user visits the site, the app will scrape stories from Houston Chronicles. The data include a link to the story and a headline, and possible other content: (photos, bylines, and so on).
* The app uses Cheerio to grab the site content and Mongoose to save it to the MongoDB database.

* All users can leave comments on the stories collected. They could delete whatever comments they want removed. All stored comments should be visible to every user.

* Mongoose's model system would be used to associate comments with particular articles.

* To begin, run npm init and save the following packages: express, express-handlebars, mongoose, body-parser, cheerio and
request

# THE APP

* Create server.js
* In server.js, require the following npm packages: express, mongojs, request and cheerio
* Initialize express
* Configure Database: Database URL - "scrapper"; collection - crapedData 
* Install npm package - mongo js 
* Connect mongojs configuration to the db variable
* require the routing files: html and api route js files 

# HEROKU DEPLOYMENT
* The app will be deployed to heroku: In order to do this, mLab provision would be set up. (mLab is remote MongoDB database that Heroku supports natively).
	* Create a Heroku app in the project directory - called drangusmongodb
	* Run this command in the Terminal/Bash window:
	heroku addons:create mongolab
	* To find the URI string that connects Mongoose to mLab, run this command: heroku config | grep MONGODB_URI
	* In order to connect Mongoose with the remote database, paste the URI string as the lone argument of the mongoose.connect() function. 