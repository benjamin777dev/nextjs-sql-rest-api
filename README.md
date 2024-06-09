# Next.js (React) + Redux + Express REST API + Postgres SQL boilerplate

_Note: this is my v2 boilerplate for React web apps. See also my [Firebase and React Hooks boilerplate](https://github.com/tomsoderlund/nextjs-pwa-firebase-boilerplate) and [REST + MongoDB boilerplate](https://github.com/tomsoderlund/nextjs-express-mongoose-crudify-boilerplate)._


## How to use

Clone this repository:

	git clone https://github.com/tomsoderlund/nextjs-sql-rest-api-boilerplate.git [MY_APP]

Install dependencies:

	cd [MY_APP]
	yarn  # or npm install

Install Postgres and set up the database:

	psql postgres  # Start the Postgres command-line client
	
	CREATE DATABASE "nextjs-sql-rest-api-boilerplate";  -- You can also use \connect to connect to existing database
	CREATE TABLE kitten (id serial, name text);  -- Create a blank table
	INSERT INTO kitten (name) VALUES ('Pugget');  -- Add example data
	SELECT * FROM kitten;  -- Check data exists
	\q

Start it by doing the following:

	export DATABASE_URL=[your Postgres URL]  # Or use a .env file
	yarn dev

In production:

	yarn build
	yarn start

If you navigate to `http://localhost:3123/` you will see a [Next.js](https://github.com/zeit/next.js) page with a list of kittens (or an empty list if you haven’t added one).

Your API server is running at `http://localhost:3123/api/kittens`


## Deploying

### Deploying on Heroku

	heroku create [MY_APP]
	heroku addons:create heroku-postgresql:hobby-dev
	git push heroku master

### Deploying on Now

(Coming)
