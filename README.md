# Node Stripe Membership SaaS

This project is a fork/update of the Repo by [ChickenKyiv/stripe-recurring-membership](https://github.com/ChickenKyiv/stripe-recurring-membership). I did it because it was not updated, several dependencies were really outdated and in general I wanted to maintain it adding new features.

It is a boilerplate express app for creating a membership/subscription site with [Stripe](https://stripe.com), mongodb and pug. It also handles stripe webhooks.

Demo: Coming soon!

## Running Locally

Make sure you have [Node.js](http://nodejs.org/). If you want to deploy it to Heroku, be sure to have the [Heroku CLI](https://cli.heroku.com/) installed.

```sh
$ git clone https://github.com/NautaDev/node-stripe-membership-saas.git # or clone your own fork
$ cd node-stripe-membership-saas
$ npm install
$ npm start
```


### System Requirements

- mongodb
- nodejs

Your app should now be running on [localhost:3000](http://localhost:3000/).



### Getting Started

First update `/server/config/secrets.js` with the following credentials:

- Stripe [API keys](https://dashboard.stripe.com/account/apikeys) and [plan info](https://dashboard.stripe.com/test/plans)
- [Mailgun](https://mailgun.com/signup) for sending forgot/reset password confirmations.
- session secret (you can use a long random string)
- google analytics id

Install dependencies with `npm install`.

Start the server with `node server`.

Note: Stripe webhooks can be recieved at `https://your-url.com/stripe/events`.


https://stripe.com/docs/subscriptions/quickstart
https://stripe.com/docs/testing

### create .env file for storing information 
### install dotenv package: npm install dotenv --save


## Deploying to Heroku

```
$ heroku create
$ git push heroku master
$ heroku open
```
or

[![Deploy to Heroku](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

## Documentation

For more information about using Node.js on Heroku, see these Dev Center articles:

- [Getting Started with Node.js on Heroku](https://devcenter.heroku.com/articles/getting-started-with-nodejs)
- [Heroku Node.js Support](https://devcenter.heroku.com/articles/nodejs-support)
- [Node.js on Heroku](https://devcenter.heroku.com/categories/nodejs)
- [Best Practices for Node.js Development](https://devcenter.heroku.com/articles/node-best-practices)
- [Using WebSockets on Heroku with Node.js](https://devcenter.heroku.com/articles/node-websockets)

### Heroku Deployment

```
heroku create your-awesome-saas-product
heroku addons:add mlab
heroku config:set SESSION_SECRET='your_secret';
heroku config:set STRIPE_TEST_KEY='sk_test_example'
heroku config:set STRIPE_TEST_PUB_KEY='pk_test_example'
heroku config:set MAILGUN_USER='example.org'
heroku config:set MAILGUN_PASSWORD='key-secret'
heroku config:set GOOGLE_ANALYTICS='UA-XXXXXX-1'
heroku config:set MONGODB_URI='mongodb://heroku_pl3qcvnq'

```

Want add a heroku deploy button? Pull requests welcome :]

Project scheme
![alt text](https://github.com/atherdon/stripe-recurring-membership/blob/master/docs/162f6342b3ee45ae9c5f338212d554dc.png)


![demo](https://github.com/atherdon/stripe-recurring-membership/blob/master/docs/localhost-3000-billing-form.png)

![demo](https://github.com/atherdon/stripe-recurring-membership/blob/master/docs/localhost-3000-profile-update.png)

![demo](https://github.com/atherdon/stripe-recurring-membership/blob/master/docs/stripe-a.herokuapp.com-profile.png)

![demo](https://github.com/atherdon/stripe-recurring-membership/blob/master/docs/stripe-a.herokuapp.com-signup2.png)

![demo](https://github.com/atherdon/stripe-recurring-membership/blob/master/docs/stripe-a.herokuapp.com-update-card.png)

![demo](https://github.com/atherdon/stripe-recurring-membership/blob/master/docs/stripe-a.herokuapp.com-user-password.png)

![demo](https://github.com/atherdon/stripe-recurring-membership/blob/master/docs/stripe-a.herokuapp.com-whois.png)