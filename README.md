# Exercise Tracker REST API

[![N|Solid](https://images.pexels.com/photos/416778/pexels-photo-416778.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260)](https://your-fitness-tracker.glitch.me/)

Welcome to this incredible Exercise Tracker REST API!

This is an API that will help you keep track of each user exercise session.

#### User Stories

1. I can create a user by posting form data username to /api/exercise/new-user and returned will be an object with username and _id.
2. I can get an array of all users by getting api/exercise/users with the same info as when creating a user.
3. I can add an exercise to any user by posting form data userId(_id), description, duration, and optionally date to /api/exercise/add. If no date supplied it will use current date. Returned will be the user object with also with the exercise fields added.
4. I can retrieve a full exercise log of any user by getting /api/exercise/log with a parameter of userId(_id). Return will be the user object with added array log and count (total exercise count).
5. I can retrieve part of the log of any user by also passing along optional parameters of from & to or limit. (Date format yyyy-mm-dd, limit = int)

### The API allows you to:

  - Post and Get users and user´s sessions.
  - Get all the information you need about any user´s exercise sessions, like description, duration, and date.
  - Search user exercise sessions by user id, you can also specify dates between which to search and limit the number of responses.
  - Search for all users.
  
  This is a welcome message from the developer of this API:

> I hope you enjoy using this amazing API 
> and I would love for you to tell me  
> what projects you are working on.
> Have fun!

### Get Started

This API requires [Node.js](https://nodejs.org/) to run.
This API uses MongoDB Atlas, so the database is on the cloud.

Clone the repository and then start the server with:

```sh
$ npm run dev
```

Please take a look at the dependencies that this API uses.

### Tech

Superhero API uses:

* [Body-Parser](https://www.npmjs.com/package/body-parser) - Node.js body parsing middleware.
* [Express](https://expressjs.com/es/) - fast node.js network app framework [@tjholowaychuk]
* [Mongoose](https://mongoosejs.com/docs/index.html) - HTML to Markdown converter
* [MongoDB Atlas](https://www.mongodb.com/cloud/atlas/lp/try2?utm_source=google&utm_campaign=gs_americas_argentina_search_brand_atlas_desktop&utm_term=atlas%20mongodb&utm_medium=cpc_paid_search&utm_ad=e&utm_ad_campaign_id=6498554093&gclid=Cj0KCQiA48j9BRC-ARIsAMQu3WTEWnXofFAEvEqDDqkhq7va6Zl8MnTTfX4fd6OFK0bzSrUI_hI5SjUaAiZtEALw_wcB) - Cloud-hosted MongoDB service
* [node.js](https://nodejs.org/es/docs/) - for the backend

And of course, Exercise Tracker REST API itself is open source with a [public repository](https://github.com/arganarazalvaro/Excercise-Tracker) on GitHub.


### How to use it?

These are the main routes you may want to use.


| Action | Route |
| ------ | ------ |
| Home Page - You can post the data| http://localhost:3000/ |
| New User has been created | http://localhost:3000/api/exercise/new-user |
| New session has been created | http://localhost:3000/api/exercise/add |
| Get all the users | http://localhost:3000/api/exercise/users|
| Get user´s full exercises list| http://localhost:3000/api/exercise/log?userId=USER_ID |
| Get user´s exercises list filtered *1| http://localhost:3000/api/exercise/log?userId=USER_ID&from=DATE1&to=DATE2&limit=LIMIT_OF_RESPONSES |

(*1) Limit: number of excercises per page (max 50). DATE1: initial date. DATE2: final date. Both dates with format: MM/DD/YYYY
Remember that ? and &: means a query is meant to be used.

[![Build Status](https://avatars-03.gitter.im/group/iv/6/57542cf4c43b8c6019778297)](https://www.freecodecamp.org/) 

This was a microservice project for Free Code Camp.  You can see the freecodecamp test [here](https://www.freecodecamp.org/learn/apis-and-microservices/apis-and-microservices-projects/exercise-tracker)

License
----

MIT
