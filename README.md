# SmartBrain-api - v1
Final project for Udemy course

1. Clone this repo
2. Run `npm install`
3. Run `npm start`

** Make sure you use postgreSQL instead of mySQL for this code base.

# to connect to postgresql

1. Run `brew install postgresql`
2. Run `brew services start postgresql`
3. Create database, run `createdb 'smart-brain'` 
4. Run `psql 'smart-brain'`. PS: Run `\q` to quit from PostgreSQL command line utility psql
5. Create two tables for database:
   Run `CREATE TABLE users (
   		id serial PRIMARY KEY, 
   		name VARCHAR(100), 
   		email text UNIQUE NOT NULL, 
   		entries BIGINT DEFAULT 0,
   		joined TIMESTAMP NOT NULL);`
   Run `CREATE TABLE login (
   		id serial PRIMARY KEY, 
   		hash VARCHAR(100) NOT NULL, 
   		email text UNIQUE NOT NULL);`
6. Run `\d` to list relations, update owner name in db in server.js
