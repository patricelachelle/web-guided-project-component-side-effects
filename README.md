# Side Effects

## About the setup

This project is set up with [Parcel Bundler](https://parceljs.org/), an npm package
that compiles our frontend assets and comes with an integrated development server.

The dev server runs on port `1234` by default, but will use another if `1234` is
being used by another application.

## Running this project

- Clone the repo.
- Navigate into the project folder.
- Run `npm i` to download the project's dependencies listed in the `package.json`.
- Run `npm run server` to start an API running on `http://localhost:4000`
- Run `npm start` to compile the React project and serve the page on `http://localhost:1234`.

If you get a `EADDRINUSE` error, because there is something already running on port `4000`, then run
it again with a `PORT` environment variable set. Here's an example:
```
$ PORT=4001 npm run server
```

## Server API Reference

### Base URL
```
http://localhost:4000
```

### Authentication

Include query parameter of `api_key` with your request. Otherwise you will get a status `403` error.

Example:
```
GET /friends?api_key=xyz
```

### Resources

##### Friends
```
GET /friends
```
#### Friend
```
GET /friends/:id
```
