# CampusAura 🎓

> A comprehensive college social media and community platform designed to connect students, share resources, and foster academic collaboration.

**Live Link:** [https://CampusAura.onrender.com](https://CampusAura.onrender.com)

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Available Scripts](#available-scripts)
- [Configuration](#configuration)
- [Contributing](#contributing)

---

## 🌟 Overview

CampusAura is a full-stack web application that brings together students, faculty, and staff on a single platform. It combines social networking features with academic tools to create a vibrant college community where users can connect, share knowledge, collaborate on assignments, and stay updated with institutional announcements.

---

## ✨ Features

### Social Features
- 📝 **Posts & Feed** - Share thoughts, images, and updates with the community
- 💬 **Real-time Messaging** - Direct messaging between users with live notifications
- 👥 **Follow System** - Connect with friends and follow interesting profiles
- ❤️ **Likes & Comments** - Engage with community content

### Academic Tools
- 📚 **Assignments** - Create, submit, and track assignments
- ✅ **Submissions** - Upload and manage assignment submissions
- 📋 **Quizzes** - Take and complete quizzes
- 📅 **Schedules** - View class schedules and important dates
- 📢 **Notices** - Stay updated with college announcements

### Additional Features
- 🔐 **User Authentication** - Secure signup and login
- 👤 **User Profiles** - Customizable user profiles with bio and profile picture
- 📊 **Admin Dashboard** - Administrative controls and moderation
- 🔔 **Notifications** - Real-time notifications for interactions
- 📱 **Responsive Design** - Works seamlessly on desktop and mobile devices

---

## 🛠 Tech Stack

### Frontend
- **React** - UI library
- **Vite** - Build tool and development server
- **Recoil** - State management
- **Socket.io Client** - Real-time communication
- **CSS3** - Styling

### Backend
- **Node.js** - JavaScript runtime
- **Express.js** - Web framework
- **MongoDB** - NoSQL database
- **Socket.io** - Real-time communication
- **JWT** - Authentication

---

## 📦 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v14.0 or higher) - [Download](https://nodejs.org/)
- **npm** (v6.0 or higher) - Comes with Node.js
- **MongoDB** (local or cloud instance) - [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
- **Git** - [Download](https://git-scm.com/)

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/pranitkolhe/CampusAura.git
cd CampusAura
```

### 2. Install Server Dependencies

```bash
cd server
npm install
```

### 3. Configure Server Environment

Create a `.env` file in the `server` directory with the following variables:

```env
PORT=5000
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/campusaura
JWT_SECRET=your_jwt_secret_key_here
NODE_ENV=development
FRONTEND_URL=http://localhost:5173
```

### 4. Install Client Dependencies

```bash
cd ../client
npm install
```

### 5. Configure Client Environment (Optional)

Create a `.env` file in the `client` directory if needed for API configuration:

```env
VITE_API_URL=http://localhost:5000
```

### 6. Start the Server

```bash
cd server
npm start
```

The server will run on `http://localhost:5000`

### 7. Start the Client (in a new terminal)

```bash
cd client
npm run dev
```

The client will run on `http://localhost:5173`

---

## 📁 Project Structure

```
CampusAura/
├── client/                          # React frontend
│   ├── src/
│   │   ├── components/             # Reusable components
│   │   ├── pages/                  # Page components
│   │   ├── atoms/                  # Recoil atoms (state)
│   │   ├── hooks/                  # Custom React hooks
│   │   ├── context/                # React context providers
│   │   ├── assets/                 # Images, sounds, media
│   │   ├── App.jsx                 # Main app component
│   │   └── main.jsx                # Entry point
│   ├── package.json
│   ├── vite.config.js
│   └── index.html
│
├── server/                          # Express backend
│   ├── controllers/                # Route handlers
│   ├── models/                     # MongoDB schemas
│   ├── routes/                     # API routes
│   ├── middlewares/                # Custom middleware
│   ├── socket/                     # Socket.io setup
│   ├── database/                   # DB connection
│   ├── utils/                      # Helper functions
│   ├── server.js                   # Server entry point
│   └── package.json
│
└── readme.md                        # Project documentation
```

---

## 📝 Available Scripts

### Client Scripts

```bash
# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

### Server Scripts

```bash
# Start server
npm start

# Start with nodemon (auto-reload)
npm run dev
```

---

## ⚙️ Configuration

### Database Setup

1. **MongoDB Atlas (Cloud)**
   - Create account at [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
   - Create a new cluster
   - Get connection string and add to `.env`

2. **Local MongoDB**
   - Install MongoDB locally
   - Update `MONGODB_URI` to `mongodb://localhost:27017/campusaura`

### JWT Configuration

Generate a secure JWT secret:

```bash
node -e "console.log(require('crypto').randomBytes(32).toString('hex'))"
```

Add this to your `.env` file as `JWT_SECRET`

---

## 🔌 API Endpoints

### Authentication
- `POST /api/users/signup` - Register new user
- `POST /api/users/login` - Login user
- `POST /api/users/logout` - Logout user

### Posts
- `GET /api/posts` - Get all posts
- `POST /api/posts` - Create new post
- `PUT /api/posts/:id` - Update post
- `DELETE /api/posts/:id` - Delete post

### Messages
- `GET /api/messages` - Get conversations
- `POST /api/messages` - Send message

### Assignments
- `GET /api/assignments` - Get all assignments
- `POST /api/assignments` - Create assignment
- `POST /api/assignments/:id/submit` - Submit assignment

*For complete API documentation, refer to the route files in the server directory.*

---

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

---

## 👨‍💻 Authors

- **Your Name** - Initial work - [GitHub](https://github.com/yourusername)

---

## 📧 Support

For support, email your-email@example.com or open an issue on GitHub.

---

## 🙏 Acknowledgments

- Thanks to all contributors who have helped with this project
- Special thanks to the college community for their feedback

---

**Happy Coding! 🚀**
