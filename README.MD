# Shoppingo E-commerce API Documentation

Welcome to the documentation for the Shoppingo E-commerce API. This guide will walk you through setting up, configuring, and utilizing the various features of the Shoppingo API.

## Hosted Project

[Shoppingo API Render URL](https://node-course-e-commerce.onrender.com/)

## Setup Basic Express Server

### Import Express and Setup Server

- [ ] Import `express` and assign it to a variable.
- [ ] Setup a starting port variable (default: 5000) and start the server function.

### Connect to Database

- [ ] Get connection string.
- [ ] Setup `.env` with `MONGO_URL` variable and assign the value.
- [ ] Import `dotenv` and setup the package.
- [ ] Import `connect()` and invoke it in the starter.
- [ ] Note: Mongoose V6 info should be considered.

## Basic Routes and Middleware

- [ ] Setup `/` GET Route.
- [ ] Setup `express.json()` middleware.
- [ ] Setup 404 and errorHandler middleware.
- [ ] Import `express-async-errors` package.

## Morgan Package

- [Morgan Package](https://www.npmjs.com/package/morgan)

## User Model

- [ ] Create a `models` folder and `User.js` file.
- [ ] Create schema with `name`, `email`, `password` (all type: String).
- [ ] Export Mongoose model.

## Validator Package

- [Validator](https://www.npmjs.com/package/validator)

## Auth Routes Structure

- [ ] Create `controllers` folder.
- [ ] Add `authController` file.
- [ ] Export `register`, `login`, `logout` functions.
- [ ] Create `routes` folder.
- [ ] Setup `authRoutes` file.
- [ ] Import all controllers.
- [ ] Setup three routes: `post('/register')`, `post('/login')`, `get('/logout')`.
- [ ] Import `authRoutes` as `authRouter` in the `app.js`.
- [ ] Setup `app.use('/api/v1/auth', authRouter)`.

## Test Routes in Postman

Make sure to test all routes in Postman.

## Register Controller

- [ ] Create user.
- [ ] Send response with entire user (only while testing).
- [ ] Check if email already in use (schema and controller).
- [ ] Ignore 'role'.
- [ ] Alternative 'admin' setup.

## Handle Password

- [ ] `UserSchema.pre('save')` - hook.
- [ ] Use `bcrypt.genSalt` and `bcrypt.hash` for password encryption.

## JWT

- [ ] Require `jsonwebtoken` package.
- [ ] Create JWT - `jwt.sign(payload, secret, options)`.
- [ ] Verify JWT - `jwt.verify(token, secret)`.
- [ ] Add variables in `.env`: `JWT_SECRET`, `JWT_LIFETIME`.
- [ ] Refactor code, create JWT functions in utils.
- [ ] Setup func `attachCookiesToResponse`.
- [ ] Accept payload (res, tokenUser).
- [ ] Create token, setup cookie.
- [ ] Optionally, send back the response.

## Login Route

- [ ] Check if email and password exist, if one is missing return 400.
- [ ] Find user, if no user return 401.
- [ ] Check password, if it does not match return 401.
- [ ] If everything is correct, attach cookie and send back the same response as in register.

## Logout Route

- [ ] Set token cookie equal to some string value.
- [ ] Set `expires: new Date(Date.now())`.

## User Routes Structure

- [ ] Add `userController` file.
- [ ] Export `getAllUsers`, `getSingleUser`, `showCurrentUser`, `updateUser`, `updateUserPassword` functions.
- [ ] Setup `userRoutes` file.
- [ ] Import all controllers.
- [ ] Setup just one route - `router.route('/').get(getAllUsers)`.
- [ ] Import `userRoutes` as `userRouter` in the `app.js`.
- [ ] Setup `app.use('/api/v1/users', userRouter)`.
