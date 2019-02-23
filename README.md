# Next.js (React) + Redux + Express REST API + Postgres SQL boilerplate

## Why is this awesome?

This is a great starting point for a any project where you want **React + Redux** (with server-side rendering, powered by [Next.js](https://github.com/zeit/next.js)) as frontend and **Express/Postgres** as a REST API backend.
Lightning fast, all JavaScript.

## Demo

See [**nextjs-sql-rest-api-boilerplate** running on Heroku here](https://nextjs-express-mongoose.herokuapp.com/).

![nextjs-sql-rest-api-boilerplate demo on Heroku](docs/demo.gif)

## How to use

Clone this repository:

	git clone https://github.com/tomsoderlund/nextjs-sql-rest-api-boilerplate.git [MY_APP]

Install dependencies:

	cd [MY_APP]
	yarn  # or npm install

Start it by doing the following:

	export DATABASE_URL=[your Postgres URL]
	yarn dev

In production:

	yarn build
	yarn start

If you navigate to `http://localhost:3123/` you will see a [Next.js](https://github.com/zeit/next.js) page with a list of kittens (or an empty list if you haven't added one).

You have your API server running at `http://localhost:3123/api/kittens`


## Deploying

### Deploying on Heroku

	heroku create [MY_APP]
	heroku addons:add postgres
	git push heroku master

### Deploying on Now

(Coming)
