# NestJS Authentication System

A secure authentication system built with NestJS featuring JWT-based authentication.

## Features

- JWT-based authentication
- User registration and login
- Password hashing with bcrypt
- Role-based access control
- Protected routes with JWT guards
- User management endpoints

## Tech Stack

- NestJS ^10.0.0
- TypeScript ^5.0.0
- Node.js ^18.0.0
- SQLite (TypeORM)
- JWT (JSON Web Tokens)
- bcrypt (Password hashing)

## Installation

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file with the following variables:
   ```env
   JWT_SECRET=your-secret-key
   DATABASE_URL=sqlite:./database.sqlite
   ```

4. Run migrations:
   ```bash
   npm run typeorm migration:run
   ```

5. Start the development server:
   ```bash
   nest start
   ```

## API Endpoints

### Auth

- `POST /auth/register` - Register a new user
- `POST /auth/login` - Login and get JWT token
- `GET /auth/profile` - Get user profile (protected)

### Users

- `GET /users` - Get all users (admin only)
- `GET /users/:id` - Get user by ID (admin/moderator only)
- `POST /users` - Create new user (admin only)
- `PATCH /users/:id` - Update user (admin/moderator only)
- `DELETE /users/:id` - Delete user (admin only)

## Security Features

- Passwords are hashed using bcrypt
- JWT tokens with configurable expiration
- Protected routes using JWT guards
- Role-based access control
- Environment-based configuration

## Development

### Running the app

```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```

### Running tests

```bash
# unit tests
$ npm run test

# e2e tests
$ npm run test:e2e

# test coverage
$ npm run test:cov
```

## License

This project is licensed under the MIT License - see the LICENSE file for details.