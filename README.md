# Chat Application

A real-time chat application built with React for the frontend and Node.js with Express for the backend. This application allows users to register, log in, and chat with each other in real-time.

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Folder Structure](#folder-structure)
- [Contributing](#contributing)
- [License](#license)

## Features

- User registration and authentication
- Real-time messaging using Socket.IO
- User avatars
- Responsive design
- Emoji support in chat

## Technologies Used

- **Frontend:**
  - React
  - React Router
  - Styled Components
  - Axios
  - Socket.IO Client

- **Backend:**
  - Node.js
  - Express
  - MongoDB (with Mongoose)
  - Socket.IO
  - Bcrypt for password hashing
  - CORS for cross-origin requests

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/chat-app.git
   cd chat-app
   ```

2. Navigate to the backend directory and install dependencies:
   ```bash
   cd server
   npm install
   ```

3. Navigate to the frontend directory and install dependencies:
   ```bash
   cd ../public
   npm install
   ```

4. Create a `.env` file in the `server` directory and add your MongoDB connection string and other environment variables:
   ```plaintext
   MONGO_URL=your_mongodb_connection_string
   PORT=8008
   REACT_APP_LOCALHOST_KEY=your_localhost_key
   ```

## Usage

1. Start the backend server:
   ```bash
   cd server
   npm start
   ```

2. Start the frontend application:
   ```bash
   cd public
   npm start
   ```

3. Open your browser and navigate to `http://localhost:3000` to access the application.

## API Endpoints

### Authentication
- **POST** `/api/auth/login` - Log in a user
- **POST** `/api/auth/register` - Register a new user
- **GET** `/api/auth/allusers/:id` - Get all users except the logged-in user
- **POST** `/api/auth/setavatar/:id` - Set user avatar
- **GET** `/api/auth/logout/:id` - Log out a user

### Messaging
- **POST** `/api/messages/addmsg` - Add a new message
- **POST** `/api/messages/getmsg` - Get messages between two users

## Folder Structure

```
chat-app/
├── public/                # Frontend code
│   ├── src/              # React components and pages
│   ├── assets/           # Static assets (images, icons, etc.)
│   ├── App.js            # Main application component
│   ├── index.js          # Entry point for React
│   └── package.json      # Frontend dependencies
└── server/               # Backend code
    ├── controllers/      # Controllers for handling requests
    ├── models/           # Mongoose models
    ├── routes/           # API routes
    ├── index.js          # Entry point for the server
    └── package.json      # Backend dependencies
```

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue for any suggestions or improvements.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
