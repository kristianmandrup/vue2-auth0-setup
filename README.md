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

## Auth Providers

- Google
- Facebook
- Twitter

### Google

- [Connect to Google](https://auth0.com/docs/connections/social/google)

To connect your Auth0 client to Google, you will need to generate a Client ID and Client Secret in a Google project, copy these keys into your Auth0 settings, and enable the Connection.

#### Generate the Google Client ID and Client Secret

While logged in to your Google account, go to the [API Manager](https://console.developers.google.com/projectselector/apis/credentials)

Create your new app by navigating to Credentials using the left-hand menu:

While you are on the Credentials page, click on Create a project.

In the dialog box that appears, provide a Project name, answer Google's email- and privacy-related questions, and click Create:

Google will take a moment to create your project. When the process completes, Google will prompt you to create the credentials you need.

Click on Create credentials to display a pop-up menu listing the types of credentials you can create. Select the OAuth client ID option.

At this point, Google will display a warning banner that says, "To create an OAuth client ID, you must first set a product name on the consent screen." Click Configure consent screen to begin this process.

Provide a Product Name that will be shown to users when they log in through Google.

Click Save.

At this point, you will be prompted to provide additional information about your newly-created app.

Select Web application, and provide a name for your app.

Under Restrictions, enter the following information:

- Authorized JavaScript origins: https://tecla5.eu.auth0.com
- Authorized redirect URI: https://tecla5.eu.auth0.com/login/callback

Click Create. Your Client Id and Client Secret will be displayed:

Save your Client Id and Client Secret to enter into the [Connection settings in Auth0](https://manage.auth0.com/#/connections/social)

ie. click on `Google` social connection settings.

- `112107055068-m6llle2duh09jgoechtjcdgotnerntp9.apps.googleusercontent.com`
- `Frg8EJN2r6u8mXTILZyl9YpM`

Click `Try`. If it works, go back and click `Save`

### Enable the Connection in Auth0

Log in to the Auth0 Dashboard and select Connections > Social in the left navigation.

Select the connection with the Google logo to access this connection's Settings page:

Select each of your existing Auth0 Clients for which you want to enable this connection. Click Save when you're done.

Switch over to the Settings tab. Copy the Client Id and Client Secret from the Credentials page of your project in the Google API Manager into the fields on this page on Auth0.

Select the Permissions for each of the features you want to allow your app to access. Click Save when you're done.

Go back to the Connections > Social section of the Auth0 dashboard. If you have configured your connection correctly, you will see a Try icon next to the Google logo:

Click Try.

Click Allow in the permissions pop-up screen:

If you have configured everything correctly, you will see the It works!!! page: