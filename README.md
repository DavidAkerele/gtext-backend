# GText Backend

This is the backend of the GText project, responsible for handling all server-side operations.

## Features

- Authentication
- User management
- Data storage and retrieval
- API endpoints for interaction with the frontend

## Installation

To get started with the project, follow the steps below:

1. Clone the repository:
    ```bash
    git clone https://github.com/DavidAkerele/gtext-backend.git
    ```

2. Install the required dependencies:
    ```bash
    cd gtext-backend
    npm install  # Or `yarn install` if you're using Yarn
    ```

3. Start the development server:
    ```bash
    npm start  # Or `yarn start` if you're using Yarn
    ```

## Technologies Used

- Node.js
- Express
- MongoDB (or your chosen database)
- JWT for authentication

## API Endpoints

- `POST /login` - Login endpoint for user authentication
- `POST /register` - Register a new user
- `GET /profile` - Get user profile details (protected)

## Contributing

Contributions are welcome! Please fork this repository and submit a pull request for any changes.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
