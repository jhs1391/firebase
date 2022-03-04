# Firebase WordPress Functions

Function helpers for [Integrate Firebase PRO version](https://github.com/dalenguyen/integrate-firebase-PRO).

## Getting started

You need to install [firebase-tools](https://firebase.google.com/docs/cli) and use **firebase** login to login to Firebase.

## Deploying to your Firebase

Replace the project name from .firebaserc file before deploying the project.

```sh
npm run deploy
yarn deploy
```

Options for deploying:

```sh
--only hosting	Firebase Hosting content
--only database	Firebase Realtime Database rules
--only storage	Cloud Storage for Firebase rules
--only firestore	Cloud Firestore rules and indexes
--only firestore:rules	Cloud Firestore rules
--only firestore:indexes	Cloud Firestore indexes
--only functions	Cloud Functions for Firebase (more specific versions of this flag are possible)
```

## Create apiToken

```sh
node -e "console.log(require('crypto').randomBytes(20).toString('hex'))"
```

Then copy them to firebase environment.

```sh
firebase functions:config:set api.dashboard_token=your-dashboard-key --project project-id
firebase functions:config:set api.frontend_token=your-frontend-key --project project-id
```

You can verify your secret key by using get from the command

```sh
firebase functions:config:get api --project project-id
```

Then from your function, you can assign it to a variable in order to secure your request.

```sh
const apiToken = functions.config().api.dashboard_token
```

After that, remember to add the token to your Firebase Settinsg in **WordPress Dashboard > Firebase**

## Testing

Add GOOGLE_APPLICATION_CREDENTIALS

```sh
export GOOGLE_APPLICATION_CREDENTIALS=/Users/dnguyen/Projects/firebase-wordpress-plugin/firebase-wordpress-functions/functions/service-account.json
```

## API lists

### USERS

- GET: api-user/v1/users: get a list of users from firebase
- GET: api-user/v1/users/:userId: get a user (with fields params)
- POST: api-user/v1/users: add new user
- DELETE: api-user/v1/users/userId: delete a user
- PATCH: api-user/v1/users/userId: update a user
- POST: api-user/v1/users/sign-out: signout everywhere
- POST: api-user/v1/users/import: import Wordpress Users

### DATABASE

- POST: api-database/v1/getDoc: get a document from firestore or realtime database
- POST: api-database/v1/createDoc: create / update a document to firestore or realtime database

### MESSAGE

- POST: api-message/v1/sendMessage: send a message to devices
