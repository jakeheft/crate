![Crate](https://raw.githubusercontent.com/atulmy/atulmy.github.io/master/images/crate/hero-with-link.png)

# Crate 👕👖📦

#### Get monthly subscription of trendy clothes and accessories.
- **API** built with Node, GraphQL, Express, Sequelize (MySQL) and JWT Auth
- **WebApp** built with React and Redux along with Server Side Rendering (SSR) / SEO friendly
- **Mobile** (Android and iOS) Native App build with React Native
- Written in ES6+ using Babel + Webpack
- Designed using Adobe Experience Design. Preview it [here](https://xd.adobe.com/view/a662a49f-57e7-4ffd-91bd-080b150b0317/).


## Features
- Modular and easily scalable code structure
- Emphasis on developer experience
- UI components in separate folder which can be swapped for your favorite UI framework easily
- Responsive UI for React Native to support Mobile and Tablet
- GraphQL schema with associations
- Database migration and data seeding
- User authentication using JSON Web Tokens with GraphQL API
- File upload feature with GraphQL
- React storybook demonstrating UI components for web
- Server side rendering
- Multi-package setup and dev scripts for an automated dev experiance


## Useful for
- Developers with basic knowledge on React exploring advance React projects
- Developers learning React Native
- Exploring GraphQL
- Scalable project structure and code
- Starter application for Mobile and Web along with SSR
- Multi-package scripts
- Sample project with combination of all above


## Screenshots and GIFs
Click on image to view fullscreen and zoom

### Desktop
[IMAGE](https://github.com/atulmy/atulmy.github.io/blob/master/images/crate/desktop-all-with-link.png)

![Crate Desktop](https://raw.githubusercontent.com/atulmy/atulmy.github.io/master/images/crate/desktop-all-with-link.png)

### Mobile
[IMAGE](https://github.com/atulmy/atulmy.github.io/blob/master/images/crate/mobile-all-with-link.png) · [GIF](https://github.com/atulmy/atulmy.github.io/blob/master/images/crate/mobile.gif)

![Crate Mobile](https://raw.githubusercontent.com/atulmy/atulmy.github.io/master/images/crate/mobile-all-with-link.png)

### Tablet
[IMAGE](https://github.com/atulmy/atulmy.github.io/blob/master/images/crate/tablet-all-with-link.png) · [GIF](https://github.com/atulmy/atulmy.github.io/blob/master/images/crate/tablet.gif)

![Crate Tablet](https://raw.githubusercontent.com/atulmy/atulmy.github.io/master/images/crate/tablet-all-with-link.png)


## Core Structure
    code
      ├── package.json
      │
      ├── api (api.example.com)
      │   ├── public
      │   ├── src
      │   │   ├── config
      │   │   ├── migrations
      │   │   ├── modules
      │   │   ├── seeders
      │   │   ├── setup
      │   │   └── index.js
      │   │
      │   └── package.json
      │
      ├── mobile (Android, iOS)
      │   ├── assets
      │   ├── src
      │   │   ├── modules
      │   │   ├── setup
      │   │   ├── ui
      │   │   └── index.js
      │   │
      │   └── package.json
      │
      ├── web (example.com)
      │   ├── public
      │   ├── src
      │   │   ├── modules
      │   │   ├── setup
      │   │   ├── ui
      │   │   └── index.js
      │   ├── storybook
      │   │
      │   └── package.json
      │
      ├── .gitignore
      └── README.md


## Setup and Running
- Prerequisites
  - Node
  - Postgres
- Clone repo `git clone git@github.com:jakeheft/crate.git` and `cd` into the repository
- Switch to `code` directory `cd code`
- Configurations
  - Configure $PATH variable
    - Add the following to your `.zshrc` file (or `.bash_profile` if using bash):
    ```
    export PATH="/Applications/Postgres.app/Contents/Versions/<your postgresql verson i.e. 12.3>/bin:$PATH"
    ```
    - Close or reload your terminal window
    - Type `which psql` in terminal and verify you see the following output:
    ```
    /Applications/Postgres.app/Contents/Versions/latest/bin/psql
    ```
  - Modify `/api/.env` for PORT (optional)
  - Modify `/web/.env` for PORT / API URL (optional)
  - Modify `/mobile/src/setup/config.json` for API URL (tip: use `ifconfig` to get your local IP address)
- Setup
  - Run your PostgreSQL interactive terminal (`psql`)
  - Run `CREATE DATABASE crate;` to create your database in PostgreSQL and then exit out of the PostgreSQL interactive terminal (`\q`)
  - API: Install packages and database setup (migrations and seed) `cd api` and `npm run setup`
      - If you receive the error `please install pg package manually`, run `npm install pg --save`, then run `npm run setup` again
  - Webapp: Install packages `cd web` and `npm install`
- Development
  - Run API `cd api` and `npm start`, browse GraphiQL at http://localhost:8000/
  - Run Webapp `cd web` and `npm start`, browse webapp at http://localhost:3000/
- Production
  - Run API `cd api` and `npm run start:prod`, creates an optimized build in `build` directory and runs the server
  - Run Webapp `cd web` and `npm start -prod`, creates an optimized build in `build` directory and runs the server
      - If you receive the error `sh: babel: command not found`, run the following:
        - `npm install @babel/cli -g`
        - `npm install @babel/core -g`
      - Now run `npm start -prod` again to run your production server

## Multi-package automation
- New developers are advised to run through the above 'setup and running' process before reading further.
- Optional multi-package automation for faster setup and easier dev environment initiation.
- No need to cd to sub-folders unless working with mobile or running a production build.
- Once Node, MySQL, repo clone and configuration are setup correctly
    - Switch to `code` directory `cd code`
    - Setup
        - Setup API, Webapp and Mobile with a single command `npm run setup`
    - Development
        - Run API and Webapp `npm start`, browse GraphiQL at http://localhost:8000/ and Webapp at http://localhost:8000/
        - Run API alone `npm start:api`, browse GraphiQL at http://localhost:8000/
        - Run Webapp alone `npm start:web`, browse webapp at http://localhost:3000/

## Resources and Inspirations
- ✍️ Opinionated project architecture for Full-Stack JavaScript Applications - [GitHub](https://github.com/atulmy/fullstack-javascript-architecture)
- 🌈 Simple Fullstack GraphQL Application - [GitHub](https://github.com/atulmy/fullstack-graphql)
- 🌐 Universal react application with server side rendering - [GitHub](https://github.com/atulmy/universal-react)
- Container Components - [Medium Post](https://medium.com/@learnreact/container-components-c0e67432e005)
- Zero to GraphQL in 30 Minutes - [YouTube](https://www.youtube.com/watch?v=UBGzsb2UkeY&list=PLkuiMQfg5DujhOSZ1A8kDl0hKV_ICTjp-)
- Building a GraphQL Server [YouTube Playlist](https://www.youtube.com/playlist?list=PLillGF-RfqbYZty73_PHBqKRDnv7ikh68)
- Universal JavaScript Web Applications with React by [Luciano Mammino](https://github.com/lmammino) - [YouTube](https://www.youtube.com/watch?v=0VEwRFP8WtI)
- Building Youtube UI in React Native in 30 Mins - [YouTube](https://www.youtube.com/watch?v=LdKtugH-sb8)
- Building Stellar Mobile UX With React Native - [YouTube](https://www.youtube.com/watch?v=ssXB9RMTpTs)
- Free MySQL hosting https://remotemysql.com


## Why open source a project and not a boilerplate or framework?
- While building a new project with Node, you can basically start scratch, adding libraries and tools as you go on building it further.
- Comparing with any other languague, you usually start with a framework, for example, Laravel (PHP), Django (Python) or Ruby on Rails (Ruby) which includes a ton of features and codebase which you never end up using.
- I've personally found, learning by going through a good project codebase step by step while building your own project helps in ease of understanding and remembering


## Author
- Atul Yadav - [GitHub](https://github.com/atulmy) · [Twitter](https://twitter.com/atulmy)


## Contributors
- Ebou Jobe - [GitHub](https://github.com/ebouJ)
- Nenad Radovanovic - [GitHub](https://github.com/nrcloud) · [Twitter](https://twitter.com/publicshone)
- Nicholas Drew - [GitHub](https://github.com/nickdrew)
- Mateus Abdala - [GitHub](https://github.com/mateusabdala)
- Hossein Nedaee - [GitHub](https://github.com/hosseinnedaee)
- Mohammad Afzal - [GitHub](https://github.com/afzalex)
- [YOUR NAME HERE] - Feel free to contribute to the codebase by resolving any open issues, refactoring, adding new features, writing test cases or any other way to make the project better and helpful to the community. Feel free to fork and send pull requests.


## Donate
If you liked this project, you can donate to support it ❤️

[![Donate via PayPal](https://raw.githubusercontent.com/atulmy/atulmy.github.io/master/images/mix/paypal-me-smaller.png)](http://paypal.me/atulmy) [![Become a Patreon](https://raw.githubusercontent.com/atulmy/atulmy.github.io/master/images/mix/patreon.png?v=1)](https://www.patreon.com/atulmy)


## Hire me
Looking for a developer to build your next idea or need a developer to work remotely? Get in touch: [atul.12788@gmail.com](mailto:atul.12788@gmail.com)


## License
Copyright (c) 2018 Atul Yadav http://github.com/atulmy

The MIT License (http://www.opensource.org/licenses/mit-license.php)

## Backend Additions
The backend team was assigned the task of creating a new attribute for a user, style, which is obtained via user survey, that informs the application as to what style of clothing should be included in their crate subscription. To accomplish this, first a migration was added and the attribute was included in the user module directory in the model file.

<img src="https://raw.githubusercontent.com/jakeheft/crate/user_style/code/api/public/images/uploads/Screen%20Shot%202021-02-13%20at%201.43.35%20PM.png" width="600" height="250">

The user types.js also needed to be updated:

<img src="https://raw.githubusercontent.com/jakeheft/crate/user_style/code/api/public/images/uploads/Screen%20Shot%202021-02-13%20at%202.21.57%20PM.png" width="600" height="250">

Next a mutation and resolver were implemented to allow the attribute to be updated via GraphQL query. Logic was included in the resolver to take in all answers from the user's survey sent in the request, find the most common, and update the style column for that user with the string. If there is a tie between two styles, a custom string with the two values interpolated is inserted in the column. 

<img src="https://raw.githubusercontent.com/jakeheft/crate/user_style/code/api/public/images/uploads/Screen%20Shot%202021-02-13%20at%202.22.26%20PM.png" width="600" height="250">

Tests were implemented to ensure everything is functioning as expected:

<img src="https://raw.githubusercontent.com/jakeheft/crate/user_style/code/api/public/images/uploads/Screen%20Shot%202021-02-13%20at%202.33.43%20PM.png" width="600" height="250">

To test the functionality of these changes in Postman, first obtain an auth token for a user in the db by making a query via GraphiQL:

<img src="https://raw.githubusercontent.com/jakeheft/crate/user_style/code/api/public/images/uploads/Screen%20Shot%202021-02-13%20at%202.55.49%20PM.png" width="600" height="250">

Then in Postman start a new POST request, under Auth, select Bearer Token and paste the token obtained from the GraphiQL request:

<img src="https://raw.githubusercontent.com/jakeheft/crate/user_style/code/api/public/images/uploads/Screen%20Shot%202021-02-13%20at%202.56.22%20PM.png" width="600" height="250">

Finally, under Body, select GraphQL and type in the query as shown below:

<img src="https://raw.githubusercontent.com/jakeheft/crate/user_style/code/api/public/images/uploads/Screen%20Shot%202021-02-13%20at%202.56.39%20PM.png" width="600" height="250">

## Frontend Additions
The frontend team was tasked with creating a new view for Crate users who were navigating the site specifically to subscribe. 
When a user selects any crate subscription the new lifestyle survey loads and captures thier selections. Currently we have coded only three styles, but more could be added in future iterations for greater variety. 

Initally we started with wireframing out the new component as well as some directions we could go once the survey was made and each style preference was stored in the database.

<img src="https://raw.githubusercontent.com/jakeheft/crate/main/code/web/public/images/Crate-Wireframe.png">

The view of the style survey with each survey card being hardcoded with one images and one id that held the style value. Once the user has logged in we check if they have a value in the database for "style", if that returns as null the survey loads once they select a crate to subscribe to. Initally we began with a literal clothing survey divided by gender and here pivoted to the lifestyle survey format.

<img src="https://raw.githubusercontent.com/jakeheft/crate/main/code/web/public/images/Main%20survey-view.png">

Once the user has made all four selections and clicked submit they are informed of their style and given a button to navigate to thier subscriptions page. This action sends the survey style results to the backend where it is associated with that user. Currently once a user has taken the survey and still has active subscriptions, they cannot take the survey again. In future we'd add a feature so that they can redo the survey if they don't agree with the results or want to change it up.

Here is the submitted survey message with a single style in the majority:

<img src="https://github.com/jakeheft/crate/blob/main/code/web/public/images/Highlander-style-summary.png">

Here is the submitted survey message with two tied styles:

<img src="https://github.com/jakeheft/crate/blob/main/code/web/public/images/Tied-style-summary.png">
