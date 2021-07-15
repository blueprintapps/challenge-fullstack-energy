# Welcome to SmallVille

SmallVille is a small town with around 100 residents. Most houses have a smart meter installed that can save and send information about how much power a house is drawing/using.

There are three major providers of energy in town that charge different amounts for the power they supply.

- _Dr Evil's Dark Energy_ : 0.15$/Kw for the first 20Kw consumed in the month, then 0.40$/Kw
- _The Green Eco_ : 0.25$/Kw for the first 150Kw consumed in the month, then 0.3$/Kw
- _Power for Everyone_ : 0.175$/Kw for the first 50Kw consumed in the month, then 0.25$

# Introducing MyEnergy

MyEnergy is a new start-up in the energy industry. Rather than selling energy they want to differentiate themselves from the market by recording their customers' energy usage (either from the web-app or directly from their smart meters) and recommending the best supplier to meet their needs.

You have been placed into their development team, whose current goal is to produce a web application and API which their customers and smart meters will interact with.

Unfortunately, two members of the team are on annual leave, and another one has called in sick! You are left with another Blueprinter to start working on the project. This is your chance to make an impact on the business and deliver value.


## What are we building

We're going to create a full-stack web application that should allow : 

- ALL the users to visit the homepage and calculate the best provider by just typing in their monthly electricity consumption (in Kw), even if they're not signed up.
- ALL the users to sign up/create an account
- The registered user to login and access their private dashboard
- The registered users to create/read/update/delete _readings_ in their private dashboard
- The registered users to see the total amount of energy consumed in a month (in Kw), the total cost and the estimation of the cost with other providers.
- The _smart-meters_ to send the electricity consumption reading to the API (Optional)
- The registered users to see the list of readings updating in real-time if while they're in the dashboard the smart-meter sends a reading to the server. (Optional)


## Requirements

### Tech Stack

The project can make use of :
- Frontend app : [React JS](https://reactjs.org)
- Stylesheets : [SaSS](https://sass-lang.com/) OR CSSinJS solutions ( [StyledComponents](https://styled-components.com/),  [Emotion](https://emotion.sh/) etc.)
Note : Although we'd love to see your ability to architect clean, optimized CSS/SaSS code, feel free to use any UI framework of your choice (Bootstrap, Bulma, ChakraUI, MaterialUI etc.) if this will allow you to complete more important parts of the project or make it all faster.
- State management : [Redux](https://reduxjs.org) OR [ContextAPI](https://reactjs.org/docs/context.html) combined with [useReducer](https://reactjs.org/docs/hooks-reference.html#usereducer) hook
- Authentication : [JSON Web Tokens](https://jwt.io/) or third-party OAuth providers (Auth0, Google, Facebook, Github, etc)
- API Server : [NodeJS](https://nodejs.org) (vanilla) OR in a framework like [Express JS](http://expressjs.com/) / [NestJS](https://nestjs.com/)
- Testing suite : [Jest](https://jestjs.io/)
- Caching : [Redis](https://redis.io)
- ORM Libraries : Prisma, Knex, Sequelize etc. Feel free to pick your favorite ORM, we don't mind.
- SQL Database : You can use any RDBMS using SQL (MySQL, PostgreSQL, SQL Server etc.)
- DevOps : [Docker](https://www.docker.com/)

The following are not strictly required but will be considered bonus points :
- SSR ( Server side rendering ) - You can either use a framework like [NextJS](https://nextjs.org) OR pure NodeJS + React Hydration
- If you've chosen Redux as state management library, [Redux Toolkit](https://redux-toolkit.js.org/) is preferrable.
- [TypeScript](https://www.typescriptlang.org/)
- [WebSockets](https://en.wikipedia.org/wiki/WebSocket) - Native WebAPI or via libraries like [Socket.IO](https://socket.io/)
- [GraphQL](https://graphql.org/) -  An extra bonus point if other than Queries and Mutations you implement Subscriptions with WebSockets.

### Coding Style

We _LOVE_ self-documenting code but whereas this is not possible to achieve, we appreciate comments that allow the rest of the team to quickly understand the choices you made without reading 100 lines of code... ;-)

### Workload

We expect you to work on this project for around 5-6hrs only and we're totally aware that implementing all of the above features/technologies below might take longer than that.
It's totally okay for you to complete/integrate only some of them, as long as you'll provide the users with a functioning application they can actually use. 
Please just show us all you can do in 5-6hrs at the best of your capabilities.

## Notes :

### Frontend

- Create a public home page that can be accessed by any user and allows them to calculate the best provider based on the amount of Kw they type in a input field.

- Create a public login/signup page that moves onto a private Dashboard area, which cannot be accessed without being logged in. 
NOTE : Once the users have succesfully logged in, they should be redirected to their private dashboard automatically.
If they close the window and open it again, they should remain authenticated for 30minutes.
If multiple windows/tabs are open, when the user log in/out they should log in/out in the other window as well.

- Create a dashboard page that allows the registered users to create a new reading for the house, read,edit and delete the previously created readings.


### Backend

You should create at least :
- an endpoint for authenticating users
- all the endpoints you need to provide the CRUD operations for the readings in the frontend.
- all the endpoints you need to provide the cost calculation / best provider recommendations in the frontend

If you're also implementing WebSockets or Graphql Subscriptions in a PubSub architecture, you can add extra endpoints for the smart-meters to consume directly.
