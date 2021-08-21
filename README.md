# Breweries API ETL

This API returns a list of Breweries using the data source: https://api.openbrewerydb.org/breweries

It has one endpoint
```
localhost:3000/breweries
```
using:
 - Jest as the testing framework
 - Typescript 4.29
 - node 14.16
 - eslint 
 - prettier

 The endpoint processes data in a series of steps which can ve viewed in here
 https://excalidraw.com/#json=6157246362812416,y0_zaxZ_arRzSE4xq-IrGQ

Each ETL step was separated into its own file inside /src/brewery/logic
each file has its own test file

the agregation of the steps is made inside /src/brewery/routes.ts

it is secured using basic authenticacion which is hardcoded for this demo project but it can be updated in the future.

### things that can be added in the future:

The project is not production ready, depending on where we are planning to host it we can then create a CI/CD pipeline

Improve autorization since it is now hardcoded into the index.ts file (user: admin, pass: admin)

as the project grows we might need an IoC library, didn't use it on this project because it will take more time to build and it is not needed for the current size

## Contribute
To contribute first clone this project using 
```
git clone
```
when the download is complete run:
```
cd autocloud
npm install
npm run start
```
you are now running the project on your machine on port 3000

to execute the tests use
```
npm run test
```

to check for lint issues use
```
npm run lint
```
to format the code use
```
npm run prettier
```

I have also uploaded a postman collection to test this specific api:
https://www.getpostman.com/collections/2df8aa92eebcb067cd82