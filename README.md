# scrapingNews
 Need your quick CNN news Fix? Well it's here, an application that pulls all the lastest news articles and lets users leave comments.

 ## What is going on around the World?

 View website [here](https://stormy-crag-43705.herokuapp.com)


# Technologies Used
* Mongo
* mongoose
* Node.js
* HTML
* CSS

# How to Deploy on Heroku

## Prerequisites
1. Install [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli)
2. Create a [Heroku account](https://signup.heroku.com/)
3. Have a MongoDB database (you can use [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) free tier)

## Deployment Steps

### 1. Login to Heroku
```bash
heroku login
```

### 2. Create a new Heroku app
```bash
heroku create your-app-name
```
Or let Heroku generate a name:
```bash
heroku create
```

### 3. Set up MongoDB
If you're using MongoDB Atlas or another MongoDB service:
```bash
heroku config:set MONGODB_URI="your-mongodb-connection-string"
```

**Note:** Update `server.js` line 33 to use the environment variable:
```javascript
mongoose.connect(process.env.MONGODB_URI || "mongodb://localhost/scrapingnews");
```

### 4. Deploy to Heroku
```bash
git push heroku main
```
Or if you're on a different branch:
```bash
git push heroku your-branch:main
```

### 5. Open your app
```bash
heroku open
```

## Additional Heroku Commands

### View logs
```bash
heroku logs --tail
```

### Run commands on Heroku
```bash
heroku run bash
```

### Scale your app
```bash
heroku ps:scale web=1
```

### Restart your app
```bash
heroku restart
```

## Local Development

### Install dependencies
```bash
npm install
```

### Run locally
```bash
npm start
```
The app will run on `http://localhost:3000`
