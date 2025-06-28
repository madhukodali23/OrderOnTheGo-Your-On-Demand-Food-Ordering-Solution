# OrderOnTheGo — Your On-Demand Food Ordering Solution

A modern food delivery website built with a React frontend and Node.js/Express backend with MongoDB integration.

##  Features

- 🍽️ **Beautiful Food Website** — Modern, responsive design with Bootstrap
- ⚛️ **React Frontend** — Component-based architecture with hooks
- 🔐 **User Authentication** — Secure login and registration system
- 🗄️ **MongoDB Integration** — Persistent user data storage
- 🔒 **JWT Authentication** — Secure token-based authentication
- 📱 **Responsive Design** — Works on all devices
- 🎨 **Modern UI** — Beautiful gradients and animations
- 🔄 **JSON Data** — Menu items extracted to reusable JSON structure

## ✅ Prerequisites

Before running this application, make sure you have the following installed:

- **Node.js** (v14 or higher)
- **MongoDB** (v4.4 or higher)
- **npm** (comes with Node.js)

## ⚙️ Installation & Setup

### 1️⃣ Clone or download the project files

### 2️⃣ Install Backend Dependencies

```bash
cd server
npm install
```

### 3️⃣ Install Frontend Dependencies

```bash
cd client
npm install
```

### 4️⃣ Start MongoDB

- Make sure MongoDB is running on your system.
- The application will connect to `mongodb://localhost:27017/`

### 5️⃣ Start the Backend Server

```bash
cd server
npm start
```

The server will run on `http://localhost:5000`

### 6️⃣ Start the Frontend Development Server

```bash
cd client
npm start
```

The React app will run on `http://localhost:3000`

## 🔗 API Endpoints

### Authentication

- `POST /api/register` — User registration
- `POST /api/login` — User login
- `GET /api/profile` — Get user profile (protected)

## 🗄️ Database Schema

### User Collection

```javascript
{
  username: String (required, unique, min 3 chars),
  email: String (required, unique, lowercase),
  password: String (required, min 6 chars, hashed),
  createdAt: Date (auto-generated)
}
```

## ⚛️ React Components

### Core Components

- **Navbar** — Navigation with authentication state management
- **Home** — Main landing page with all sections
- **Login** — User login form
- **Register** — User registration form
- **MenuItem** — Reusable menu item card component
- **WcuCard** — Reusable "Why Choose Us" card component

### Data Structure

All menu items, social links, and other data are stored in `client/src/data/menuItems.js` as JSON arrays that can be easily iterated over:

```javascript
export const menuItems = [
  {
    id: 1,
    title: "Non-Veg Starters",
    image: "...",
    link: "#"
  },
  // ... more items
];
```

## 🔒 Security Features

- **Password Hashing** — Passwords are hashed using bcryptjs
- **JWT Tokens** — Secure authentication tokens
- **Input Validation** — Server-side validation using express-validator
- **CORS** — Cross-origin resource sharing enabled
- **Environment Variables** — Support for .env file configuration

## 📚 Usage

1. **Registration** — New users can create an account with username, email, and password.
2. **Login** — Existing users can log in with email and password.
3. **Authentication State** — The website automatically shows login/register buttons or user info based on authentication status.
4. **Logout** — Users can log out using the logout button in the navigation.
5. **Menu Items** — All menu items are dynamically rendered from JSON data.

## ⚡ MongoDB Connection

The application connects to MongoDB using the connection string:

```
mongodb://localhost:27017/
```

Make sure MongoDB is running on your local machine on the default port (27017).

## 🔑 Environment Variables

Create a `.env` file in the `server` directory:

```env
PORT=5000
JWT_SECRET=your-secret-key-here
MONGODB_URI=mongodb://localhost:27017/
```

## 🛠️ Troubleshooting

### MongoDB Connection Issues

- Ensure MongoDB is installed and running
- Check if the MongoDB service is started
- Verify the connection string in `server/server.js`

### Port Already in Use

- Change the PORT in the `.env` file or `server/server.js`
- Kill any existing processes using port 5000 (backend) or 3000 (frontend)

### Dependencies Issues

- Delete `node_modules` folder and run `npm install` again
- Ensure you're using Node.js v14 or higher

## 🧰 Technologies Used

### Frontend

- **React 18** with Hooks
- **React Router** for navigation
- **Axios** for API calls
- **Bootstrap 4** for styling
- **Font Awesome** for icons

### Backend

- **Node.js** with Express.js
- **MongoDB** with Mongoose ODM
- **JWT** for authentication
- **bcryptjs** for password hashing
- **express-validator** for validation

## 📄 License

This project is open source and available under the **MIT License**.

## 🙌 Support

If you encounter any issues or have questions, please check the troubleshooting section above or create an issue in the project repository.
```
