# Keep Secrets
 Secrets Logger - This project showcases a web application that allows users to register, log in, and share secrets. It's built using Express.js and integrates local authentication as well as Google OAuth 2.0 for user login.

# Features
- User Registration and Authentication: Users can register with a unique username and password. Passport.js is used with the Local Strategy for secure user authentication.
- Google OAuth 2.0: Users can also log in using their Google accounts through OAuth 2.0. The GoogleStrategy from Passport.js is employed to handle Google authentication.
- Share and Display Secrets: Authenticated users can submit their secrets, which are stored and displayed on the "Secrets" page.
- User Session Management: The app manages user sessions, allowing users to remain logged in across different pages until they choose to log out.

# Tech Stack
- Node.js: The server-side runtime environment for running JavaScript code.
- Express.js: A web application framework for building robust and scalable applications.
- MongoDB: A NoSQL database used to store user information and secrets.
- Passport.js: An authentication middleware for Node.js that supports various authentication strategies.
- EJS: A templating engine for rendering dynamic HTML pages.
- Google OAuth 2.0: OAuth 2.0 authentication using Google accounts.

# Local Setup
Follow these steps to set up the application locally on your machine:

1. Clone the Repository: Start by cloning this repository to your local machine using Git.

git clone <repository-url>

2. Install Dependencies: Navigate to the project directory and install the required dependencies.

npm install

3. Configure Google OAuth: Create a Google OAuth 2.0 credentials in the Google Developer Console:
- Set the authorized redirect URI to http://localhost:3000/auth/google/secrets.

4. Set Environment Variables: Create a .env file in the project root and add your Google OAuth credentials:

CLIENT_ID=<your-client-id>
CLIENT_SECRET=<your-client-secret>

5. Start the Server: Launch the application by running the following command:

npm start

6. Usage:
- Visit http://localhost:3000 in your web browser to access the home page.
- Click "Login with Google" to authenticate via Google OAuth 2.0.
- Once authenticated, you can submit your own secrets and view secrets submitted by other users.
- Logout by clicking the "Logout" button.

# Implementation Details
- The app uses Express.js to handle routing and server setup.
- Passport.js is used to manage authentication. It employs both local authentication (username and password) and Google OAuth 2.0.
- User data is stored in a MongoDB database. Mongoose is used for schema modeling and interaction with the database.
- EJS templates are used for rendering dynamic HTML pages, such as login, registration, and secrets display.

# Folder Structure
- public/: Static assets (CSS, images, etc.).
- views/: EJS templates for rendering HTML.
- models/: Mongoose schema models.
- app.js: Main Express application setup.

# Routes
- /: Home page.
- /auth/google: Initiate Google OAuth 2.0 authentication.
- /auth/google/secrets: Google OAuth 2.0 callback URL.
- /login: User login page.
- /register: User registration page.
- /secrets: Display secrets submitted by users.
- /submit: Submit a secret.
- /logout: Log out the user.