# vuesetup

This repo accompanies the following blog post:  
[Vue.js - Setting up Auth0](https://medium.com/@bradfmd/vue-js-setting-up-auth0-6eb26cbbc48a)

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# run unit tests
npm run unit

# run e2e tests
npm run e2e

# run all tests
npm test
```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

## Configuration

You will need to supply the jwtCheck function 2 variables: secret and audience. The audience is your client id from your client dashboard in Auth0 and the secret is the client secret from the same screen. For a more complete server backend example, check out the [node Auth0 express example repo](https://github.com/auth0/node-auth0).

## TODO