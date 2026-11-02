![List of Ingredients](https://i.imgur.com/30bgJWe.png)

# List of ingredients

An example app that pairs a Rails 5 API and ActiveAdmin with a Create React App front end, all deployed to Heroku.

Status: archived. Made in 2017, not maintained. A lot has moved on since: Create React App is deprecated, Heroku's free tier is gone, and Rails 5 is well past end of life. The steps below still show how the pieces fit together, but don't expect them to run as written.

Write-up: https://www.heroku.com/blog/a-rock-solid-modern-web-stack/

## Update, May 16, 2018

Thank you to everyone who took the time to give feedback, share their experiments, and star this repo. After I finished it I joined Heroku, and with their help I rewrote it to iron out the bugs, take in your feedback, and add support for Rails 5.2.0, React Router, and Yarn.

That newer version is at https://github.com/heroku/list-of-ingredients (also archived now), and version 2.0 of the tutorial is the Heroku blog post linked above.

## The original tutorial

This repo is the companion to the original tutorial, [Rails 5 API + ActiveAdmin + create-react-app on Heroku](https://medium.com/superhighfives/rails-5-api-activeadmin-create-react-app-on-heroku-de5481b7ec0b), and the end result should look something like this:

![An example of the List of Ingredients app](https://i.imgur.com/as3HMYP.png)

## Getting started

```shell
git clone https://github.com/superhighfives/list-of-ingredients.git
cd list-of-ingredients
bundle
cd client
npm install
cd ..
rake db:migrate
rake db:seed
rake start
```

When you're ready to deploy to [Heroku](https://www.heroku.com), run:

```shell
heroku apps:create
heroku buildpacks:add heroku/nodejs --index 1
heroku buildpacks:add heroku/ruby --index 2
git push heroku master
heroku run rake db:migrate
heroku run rake db:seed
heroku open
```

Success. Note that Heroku no longer has a free tier, so this will need a paid plan.

## Suggestions, problems, typos?

This repo is archived, so issues are closed. The code is here to read and borrow from.
