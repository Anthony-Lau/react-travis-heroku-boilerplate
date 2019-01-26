This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

# Steps to deploy React app to Heroku from Github using Travis CI

## 1. Connect travis to Github

- Go to the [travis website](travis-ci.org) and click the `+` to add your projects repository.

#### Add your heroku api key to travis environment variables

- Select your repository in travis and click the `more options` dropdown 

- Under settings add your heroku api key

## 2. Connect Heroku to Github

#### This assumes you have connected your github account to heroku

- Go to the [heroku site](https://www.heroku.com/) and click the `new` dropdown

- Select `Create new app` and enter name of new app (your domain will be `appname`.herokuapp.com)

- Click the `deploy` tab

- Under deployment method select `Github` as your preferred method

- Under `Connect to Github` enter the name of your repo you want to deploy

- Under `Automatic Deploys` select wait for CI to pass before deploy

## 3. Edit your .travis.yml file

- In the .travis.yml file, under `deploy` `app` edit your appname to be whatever you called it in heroku.

# Hooray you're done!

- Every push to master will deploy your react app.