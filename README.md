# CookNShare - FullStack Social Media App

A complete fullstack responsive MERN (MongoDB, Express.js, React.js, Node.js) social media application with authentication, likes, dark mode, and more.

## 🚀 Features

- **User Authentication**: Secure login and registration with JWT tokens
- **Social Features**: Add/remove friends, like posts, view user profiles
- **Post Management**: Create, view, and interact with posts
- **Dark Mode**: Toggle between light and dark themes
- **Responsive Design**: Mobile-friendly interface using Material-UI
- **File Uploads**: Upload and display user images and post media
- **Real-time Updates**: Dynamic content updates without page refresh

## 🛠️ Tech Stack

### Frontend

- **React.js** - UI library
- **Material-UI (MUI)** - Component library and theming
- **Redux Toolkit** - State management
- **React Router** - Client-side routing
- **Formik & Yup** - Form handling and validation
- **React Dropzone** - File upload handling

### Backend

- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - NoSQL database
- **Mongoose** - ODM for MongoDB
- **JWT** - Authentication tokens
- **bcrypt** - Password hashing
- **Multer** - File upload middleware
- **GridFS** - File storage in MongoDB

## 📁 Project Structure

```
cookNshare/
├── client/                 # React frontend
│   ├── public/
│   │   ├── index.html
│   │   ├── manifest.json
│   │   └── assets/
│   └── src/
│       ├── components/     # Reusable UI components
│       │   ├── FlexBetween.jsx
│       │   ├── Friend.jsx
│       │   ├── UserImage.jsx
│       │   └── WidgetWrapper.jsx
│       ├── scenes/         # Page components
│       │   ├── homePage/
│       │   ├── loginPage/
│       │   ├── navbar/
│       │   ├── profilePage/
│       │   └── widgets/    # Widget components
│       ├── state/          # Redux store
│       ├── App.js
│       ├── index.js
│       ├── theme.js
│       └── index.css
├── server/                 # Node.js backend
│   ├── controllers/        # Route controllers
│   │   ├── auth.js
│   │   ├── posts.js
│   │   └── users.js
│   ├── data/               # Database utilities
│   ├── middleware/         # Custom middleware
│   │   └── auth.js
│   ├── models/             # Mongoose models
│   │   ├── Post.js
│   │   └── User.js
│   ├── public/assets/      # Static file storage
│   ├── routes/             # API routes
│   │   ├── auth.js
│   │   ├── posts.js
│   │   └── users.js
│   ├── index.js            # Server entry point
│   └── package.json
└── README.md
```

## 🏃‍♂️ Getting Started

### Prerequisites

- Node.js (v14 or higher)
- MongoDB (local or Atlas)
- npm or yarn

### Installation

1. **Clone the repository**

   ```bash
   git clone <repository-url>
   cd cookNshare
   ```

2. **Install server dependencies**

   ```bash
   cd server
   npm install
   ```

3. **Install client dependencies**

   ```bash
   cd ../client
   npm install
   ```

4. **Environment Setup**

   Create a `.env` file in the `server` directory:

   ```env
   MONGO_URL=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret_key
   PORT=3001
   ```

   Create a `.env` file in the `client` directory:

   ```env
   REACT_APP_SERVER_URL=http://localhost:3001
   ```

5. **Start the development servers**

   **Terminal 1 - Start the backend server:**

   ```bash
   cd server
   npm start
   ```

   **Terminal 2 - Start the frontend:**

   ```bash
   cd client
   npm start
   ```

6. **Access the application**

   Open [http://localhost:3000](http://localhost:3000) in your browser.

## 📡 API Endpoints

### Authentication

- `POST /auth/login` - User login
- `POST /auth/register` - User registration

### Users

- `GET /users/:id` - Get user by ID
- `GET /users/:id/friends` - Get user's friends
- `PATCH /users/:id/:friendId` - Add/remove friend

### Posts

- `GET /posts` - Get all posts
- `GET /posts/:userId/posts` - Get posts by user
- `POST /posts` - Create new post
