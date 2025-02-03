
# NLW Copa Server

The **NLW Copa Server** is a backend server built to support the [NLW Copa](https://www.nlw.dev) application. This server handles API requests, manages user data, and supports features related to the Copa do Mundo (World Cup) experience, including teams, matches, and user participation in the event.

## Features

- Manage teams, players, and matches for the Copa do Mundo.
- User registration and authentication.
- API for submitting and tracking predictions.
- Real-time updates for match results and standings.
- RESTful API endpoints for interaction with the frontend.

## Requirements

Before you start, ensure you have the following installed:

- [Node.js](https://nodejs.org/) (version 14.x or later)
- [npm](https://www.npmjs.com/) (Node Package Manager, comes with Node.js)
- A database like **PostgreSQL** (or another database if configured differently)

## Installation

### Clone the repository:

```bash
git clone https://github.com/dantls/nlw-copa-server.git
cd nlw-copa-server
```

### Install dependencies:

Run the following command to install the required dependencies:

```bash
npm install
```

### Environment Configuration

You’ll need to configure environment variables to set up the database connection and other settings.

1. Copy the `.env.example` file to `.env`:

```bash
cp .env.example .env
```

2. Update the `.env` file with your environment-specific values:

- `DATABASE_URL`: The connection string to your database (e.g., PostgreSQL).
- `JWT_SECRET`: The secret key used for JWT authentication.
- Other environment variables as specified in `.env.example`.

### Database Setup

1. **Create and migrate the database**:

```bash
npm run migrate
```

This will set up the necessary tables in the database.

2. Optionally, seed the database with initial data:

```bash
npm run seed
```

## Running the Server

Once you have the environment set up and the database ready, you can start the server using:

```bash
npm run dev
```

This will start the server in development mode, and you can access the API at [http://localhost:3000](http://localhost:3000).

### Running in Production

To run the server in production mode, use:

```bash
npm run build
npm start
```

## API Documentation

This server exposes a RESTful API to interact with the Copa do Mundo data.

### Example API Endpoints:

- **POST /users/register**: Register a new user.
- **POST /users/login**: Log in and get a JWT token.
- **GET /teams**: Get a list of all teams.
- **GET /matches**: Get a list of all matches.
- **POST /predictions**: Submit a prediction for a match.
  
For more details on the available endpoints, refer to the API documentation (if available) or the source code in the `src/routes` directory.

## Running Tests

To run tests for this project, use:

```bash
npm test
```

This will run the unit and integration tests to ensure the server works as expected.

## Contributing

We welcome contributions! If you’d like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit them (`git commit -am 'Add new feature'`).
4. Push to your branch (`git push origin feature-branch`).
5. Open a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Rocketseat](https://rocketseat.com.br) for the NLW (Next Level Week) content and inspiration.
- All contributors to this project.


