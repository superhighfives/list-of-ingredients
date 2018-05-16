![List of Ingredients](https://i.imgur.com/30bgJWe.png)

# List of Ingredients

**Update, 16 May 2018:**

First off, thank you to everyone who has taken the time to give feedback, share their experiments, and star this repo. Since I finished it last year I joined Heroku, and with their help I've rewritten it to iron out the bugs, implement your feedback, and to include support for Rails 5.2.0, React Router, and Yarn.

You can also find latest repo, including a Heroku button you can automagically deploy with, here: https://github.com/heroku/list-of-ingredients

You can also find version 2.0 of the tutorial here: https://blog.heroku.com/a-rock-solid-modern-web-stack

Once again, I could not be more appreciative of your support and feedback. 🙌

---

This repo serves as a companion to the tutorial [Rails 5 API + ActiveAdmin + create-react-app on Heroku, over on Medium](https://medium.com/superhighfives/rails-5-api-activeadmin-create-react-app-on-heroku-de5481b7ec0b), and the end result should look something like this:

![An example of the List of Ingredients app](http://i.imgur.com/as3HMYP.png)

## Getting started

``` shell
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

Once you're ready to deploy to [Heroku](https://surge.sh), run:

``` shell
heroku apps:create
heroku buildpacks:add heroku/nodejs --index 1
heroku buildpacks:add heroku/ruby --index 2
git push heroku master
heroku run rake db:migrate
heroku run rake db:seed
heroku open
```

Success!

## Suggestions, problems, typos?

Let me know in the [issues](https://github.com/superhighfives/list-of-ingredients/issues).
