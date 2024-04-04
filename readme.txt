
### 1. `userRoutes.js`
This file defines the routes for user-related operations.

- **Routes:**
  - `POST /register`: Register a new user.
  - `POST /auth`: Authenticate user login.
  - `GET /get-profile`: Get user's profile information.
  - `POST /add-address`: Add a new address for the user.
  - `POST /logout`: Logout the user.

- **Middlewares:**
  - `protect`: Middleware to protect routes requiring authentication.
  - `loginBlockCheck`: Middleware to check if user login is blocked.
  - `authUserValidation`: Middleware to validate user authentication request body.
  - `addAddressValidation`: Middleware to validate request body for adding address.
  - `validate`: General validation middleware.

### 2. `app.js`
This file configures the Express application and sets up middleware.

- **Middleware Used:**
  - `helmet`: Provides security headers for the HTTP responses.
  - `express.json()`: Parses incoming request bodies in JSON format.
  - `express.urlencoded()`: Parses incoming request bodies in URL-encoded format.
  - `cookieParser`: Parses cookies attached to the client request.
  - `cors`: Middleware to enable Cross-Origin Resource Sharing.
  - Custom API rate and speed limiters.

- **Routes:**
  - `/api/v1`: Mounts version 1 APIs.

### 3. `userController.js`
This file contains controller functions for user-related operations.

- **Controller Methods:**
  - `registerUser`: Registers a new user.
  - `authUser`: Authenticates user login.
  - `getProfile`: Retrieves user's profile information.
  - `addAddress`: Adds a new address for the user.
  - `logout`: Logs out the user.

### 4. `UserService.js`
This file contains service methods for user-related operations.

- **Service Methods:**
  - `registerUser`: Registers a new user.
  - `userLogin`: Authenticates user login.
  - `getUser`: Retrieves user's profile information.
  - `addAddress`: Adds a new address for the user.

### 5. `UserRepository.js`
This file contains methods to interact with the user data in the database.

- **Methods:**
  - `createUser`: Creates a new user in the database.
  - `findByEmail`: Finds a user by email in the database.
  - `findUserById`: Finds a user by ID in the database.
  - `matchPasswords`: Compares entered password with stored hashed password.
  - `getUser`: Retrieves user by ID.
  - `addAddress`: Adds address for a user.

### Overall
- The application follows a typical MVC (Model-View-Controller) architecture.
- Controllers handle HTTP requests, services encapsulate business logic, and repositories interact with the database.
- Middleware is used for request processing, validation, and security.
- Error handling and logging are implemented throughout the application.

