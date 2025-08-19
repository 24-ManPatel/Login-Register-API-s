# Login/Register API

A **simple, reusable Node.js API** for login and registration. Clone this repository, install the dependencies, and connect instantly with your frontend framework. No custom backend coding required!

## Features

- User registration with secure password storage
- User login authentication
- Works with MongoDB Atlas cloud database
- Can be integrated with any frontend framework (React, Angular, Vue, etc.)

## Getting Started

### Clone the Repository

```bash
git clone https://github.com/24-ManPatel/Login-Register-API-s.git
cd Login-Register-API-s
```

### Install Required Dependencies

Make sure you have Node.js and npm installed.
```bash
npm install
```

### Set Up MongoDB Atlas

1. **Create a MongoDB Atlas Account**
   - Go to [MongoDB Atlas](https://www.mongodb.com/cloud/atlas).
   - Sign up and create a free cluster.

2. **Configure Your Database**
   - Add your IP address to whitelist (for local development).
   - Create a database user and password.

3. **Get Your Connection String**
   - In Atlas, click "Connect" → "Drivers".
   - Copy the connection string, which should look like:
     ```
     mongodb+srv://:@/?retryWrites=true&w=majority
     ```

4. **Create a `.env` File**
   - At the project root, create a file named `.env`.
   - Add your connection string:
     ```
     MONGODB_URL=your_copied_connection_string
     ```
   - Example:
     ```
     MONGODB_URL=mongodb+srv://legend:yourpassword@cluster0.sscvg.mongodb.net/your-db-name
     ```

### Running the API

```bash
npm start
```
The API will start on the configured port (default is usually 5000 or 3000).

## API Endpoints

- `POST /register` — Register a new user (send user data in the body)
- `POST /login` — Login with email and password

Integrate these endpoints with any frontend framework! Just send POST requests with the required user data.

## Usage Example (with fetch/Axios)

**Register:**
```javascript
fetch('http://localhost:5000/register', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({ email, password })
})
```

**Login:**
```javascript
fetch('http://localhost:5000/login', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({ email, password })
})
```

## Contributing

Fork the repo, make your changes, and submit a pull request!

***

**This API is plug-and-play for any project. Simply configure your MongoDB Atlas URI and start authenticating users instantly in your app.**
