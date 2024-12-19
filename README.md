# User Management App

A simple React app for managing users with features such as user login, viewing users' list, editing, and deleting users. The app communicates with a backend API to fetch, update, and delete user data.

## Features

- **Login Page**: Users can log in with their credentials (email and password).
- **Users List Page**: Displays a paginated list of users with options to edit or delete users.
- **Edit User**: Users can edit their first name, last name, and email.
- **Delete User**: Users can delete users from the list.
- **API Integration**: Uses Axios for API requests to a mock backend API.

## Technologies Used

- React
- Axios (for API requests)
- React Router (for routing between pages)
- Tailwind CSS (for styling)
- React Toastify (for notifications)
- LocalStorage (for storing login token)

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/user-management-app.git
cd user-management-app
```

### 2. Install Dependencies

Install the required dependencies using npm or yarn:

```bash
npm install
```

### 3. Configure API

The app is set up to use a mock API (`https://reqres.in/api`). You can modify the `src/config/api.js` file to point to your own API if needed.

### 4. Run the App Locally

To start the development server, run:

```bash
npm start
```

This will start the app on [http://localhost:3000](http://localhost:3000).

### 5. Build the App for Production

To create a production build of the app, run:

```bash
npm run build
```

This will generate a `build/` folder containing the production-ready code.

### 6. Deployment

You can deploy the app to a cloud provider like [Vercel](https://vercel.com/) or [Netlify](https://www.netlify.com/). Simply follow their documentation to deploy React applications.

## API Endpoints Used

- **Login**: `POST /api/login`
  - Request body: `{ "email": "user@example.com", "password": "password123" }`
  - Response: `{ "token": "some-token" }`

- **Users List**: `GET /api/users`
  - Fetches a paginated list of users.

- **Get User by ID**: `GET /api/users/{id}`
  - Fetches a user’s details by their ID.

- **Edit User**: `PUT /api/users/{id}`
  - Request body: `{ "first_name": "John", "last_name": "Doe", "email": "john.doe@example.com" }`
  - Response: `{ "message": "User updated successfully" }`

- **Delete User**: `DELETE /api/users/{id}`
  - Response: `{ "message": "User deleted successfully" }`

## File Structure

```
src/
  components/
    EditUser.js           # Edit user form component
    Login.js              # Login form component
    UsersList.js          # List of users with edit and delete buttons
  config/
    api.js                # Axios instance for making API requests
  pages/
    LoginPage.js          # Login page
    UsersListPage.js      # Users list page
  App.js                  # Main app component with routing
  index.css               # Global styles with Tailwind CSS
```

## Notes

- This app uses `reqres.in` as a mock API for users. You can replace the API endpoints with your own in the `api.js` file.
- The app uses React Router for navigation between pages.
- It stores the login token in `localStorage`. If the token is not available, the app will redirect the user to the login page.

## Screenshots

### Login Page
![Login Page](screenshots/login-page.png)

### Users List Page
![Users List Page](screenshots/users-list.png)

### Edit User Page
![Edit User Page](screenshots/edit-user.png)

## Contributing

Feel free to fork the repository and submit pull requests. All contributions are welcome!

## License

This project is open-source and available under the [MIT License](LICENSE).

