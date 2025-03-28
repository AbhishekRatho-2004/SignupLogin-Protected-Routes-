# IndexedDB Authentication App

## Overview
This is a simple authentication application that uses IndexedDB for user signup, login, and authentication management. The application includes:
- User signup and login system.
- Storing user data in IndexedDB.
- Protected routes using localStorage.
- A simple homepage with a navbar, welcome message, and logout functionality.

## Features
- **Signup & Login**: Users can create an account and log in.
- **IndexedDB Storage**: User credentials are stored securely in IndexedDB.
- **Protected Routes**: Only authenticated users can access protected pages.
- **LocalStorage Session**: User session data is managed using localStorage.
- **Responsive UI**: A clean UI with a navbar and hero section.

## Technologies Used
- React.js
- IndexedDB
- React Router
- LocalStorage
- JavaScript (ES6+)
- Vanilla CSS

## Installation & Setup
1. Clone the repository:
   ```sh
   git clone https://github.com/your-username/indexeddb-auth-app.git
   cd indexeddb-auth-app
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Start the development server:
   ```sh
   npm start
   ```

## Usage
1. Navigate to `/signup` to create an account.
2. Login at `/login` with your registered credentials.
3. Once logged in, you will be redirected to `/home`.
4. Click on the logout button to end the session.

## File Structure
```
/src
  ├── pages
  │   ├── Home.jsx
  │   ├── Login.jsx
  │   ├── Signup.jsx
  ├── IndexedDB.jsx
  ├── App.jsx
  ├── index.js
  ├──ProtectedRoute.jsx
```

## Protected Route Implementation
A `ProtectedRoute` component is used to restrict access to authenticated users.
```jsx
import { Navigate, Outlet } from "react-router-dom";

const ProtectedRoute = () => {
  const isAuthenticated = localStorage.getItem("username");
  return isAuthenticated ? <Outlet /> : <Navigate to="/login" />;
};

export default ProtectedRoute;
```

## License
This project is open-source and available under the [MIT License](LICENSE).

