# Change log

> **Tags:**
>
> - :boom: [Breaking Change]
> - :eyeglasses: [Spec Compliancy]
> - :rocket: [New Feature]
> - :bug: [Bug Fix]
> - :memo: [Documentation]
> - :nail_care: [Polish]

---

## [1.3.0] - 2021-10-31

#### - :nail_care: [Polish]

- Update packages

## [1.2.0] - 2021-08-26

#### - :rocket: [New Feature]

- Used user_login for uid when importing users

## [1.1.0] - 2021-05-29

#### - :rocket: [New Feature]

- Added support for secondary Realtime database

## [1.0.0] - 2021-04-21

#### - :rocket: [New Feature]

- Updated import users from WordPress logic
- Used randomized string for UID when importing users

## [0.20.0] - 2021-04-02

#### - :nail_care: [Polish]

- Refactored firebase functions service
- Updated packages
- Clear logs

## [0.19.0] - 2021-02-20

#### - :rocket: [New Feature]

- Added delete document endpoint

## [0.18.0] - 2021-01-23

#### - :rocket: [New Feature]

- Added getUser endpoint (with fields params)

## [0.17.0] - 2021-01-16

#### - :nail_care: [Polish]

- Update packages

## [0.16.0] - 2020-11-21

#### - :nail_care: [Polish]

- Update packages
- Require node 12 for cloud functions

## [0.15.0] - 2020-11-08

#### - :rocket: [New Feature]

- Added import users endpoint
- Allowed to signout with frontend token

## [0.14.0] - 2020-08-29

#### - :nail_care: [Polish]

- Update packages

#### - :rocket: [New Feature]

- Prevent writing data via API with frontend token
- Added update document feature

## [0.13.0] - 08-06-2020

#### - :rocket: [New Feature]

- Added ability to deploy cloud functions to different regions

## [0.12.0] - 2020-05-26

#### - :rocket: [New Feature]

- Added debug emulator
- Added update / create for when saving to firestore

## [0.11.1] - 2020-04-12

#### - :bug: [Bug Fix]

- Removed custom claims when empty

## [0.11.0] - 2020-04-10

#### - :rocket: [New Feature]

- Get all users (> 1000 users)

## [0.10.0] - 2020-04-02

#### - :rocket: [New Feature]

- Added sign-out to frontend functions list

## [0.9.0] - 2020-04-01

#### - :rocket: [New Feature]

- Added validation for firebase environment
- Added list for public collections
- Added protection for method from frontend

## [0.8.0] - 2020-03-28

#### - :rocket: [New Feature]

- Save data with or with out document id

## [0.7.0] - 2020-03-21

#### - :rocket: [New Feature]

- Added source requests to headers
- Replaced dashboardToken & frontendToken by token only
- Added user sign out api

## [0.6.0] - 2020-03-01

#### - :rocket: [New Feature]

- Added create send message to topic feature (/v1/sendMessage)

## [0.5.6] - 2020-02-23

#### - :bug: [Bug Fix]

- Separated frontend token for create new data

## [0.5.5] - 2020-02-20

#### - :nail_care: [Polish]

- Updated packages

#### - :boom: [Breaking Change]

- Changed get document method name (/v1/doc -> /v1/getDoc)
- Change token to dashboard_token and frontend_token

#### - :rocket: [New Feature]

- Added create document feature (/v1/createDoc)

## [0.5.4] - 2019-12-01

#### - :rocket: [New Feature]

- Move Realtime & Firestore rules to Firebase console
- Added Add New User and Update User functions

#### - :nail_care: [Polish]

- Remove development project from package.json

## [0.5.3] - 2019-10-14

#### - :nail_care: [Polish]

- Added change log
- Restructure project
- Added Database API
- Added User API
