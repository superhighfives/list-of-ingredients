![List of Ingredients](https://i.imgur.com/30bgJWe.png)

# List of Ingredients

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
