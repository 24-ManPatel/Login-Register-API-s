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



## Testing API Endpoints with Postman

You can use [Postman](https://www.postman.com/) to easily test your API endpoints:

### 1. Register a User

- **Method:** `POST`
- **URL:** `http://localhost:5000/register`
- **Body:** Select `raw` and choose `JSON` format. Enter:
  ```json
  {
    "email": "test@example.com",
    "password": "yourpassword"
  }
  ```

- Click **Send**. You should receive a success message or user data response.

### 2. Login a User

- **Method:** `POST`
- **URL:** `http://localhost:5000/login`
- **Body:** Select `raw` and choose `JSON` format. Enter:
  ```json
  {
    "email": "test@example.com",
    "password": "yourpassword"
  }
  ```

- Click **Send**. On success, you will receive a login token or success response.

***

**Tip:** Make sure your backend server is running locally while testing with Postman.

This helps users quickly verify and interact with the API endpoints using a graphical interface, with no coding required!Certainly! Here’s the revised section for testing with **Postman** instead of fetch/Axios:

***

## Testing API Endpoints with Postman

You can use Postman to test the API endpoints without any frontend code.

### **Register**

1. Open Postman.
2. Set the request type to **POST**.
3. Enter the URL: `http://localhost:5000/register`
4. Go to the **Body** tab, select **raw** and choose **JSON** as the format.
5. Enter the data:
    ```json
    {
      "email": "test@example.com",
      "password": "yourpassword"
    }
    ```
6. Click **Send** to test registration.

### **Login**

1. Set the request type to **POST**.
2. Enter the URL: `http://localhost:5000/login`
3. In the **Body** tab, select **raw** and choose **JSON**.
4. Enter:
    ```json
    {
      "email": "test@example.com",
      "password": "yourpassword"
    }
    ```
5. Click **Send** to test login.


## Contributing

Fork the repo, make your changes, and submit a pull request!

***

**This API is plug-and-play for any project. Simply configure your MongoDB Atlas URI and start authenticating users instantly in your app.**
