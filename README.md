# TOOLTIK


ToolTok Full-Stack Structure (Solo MVP)
tooltok/
├── backend/                  # Node.js + Express backend
│   ├── config/
│   │   └── db.js             # MongoDB connection
│   ├── controllers/
│   │   ├── authController.js
│   │   ├── userController.js
│   │   └── videoController.js
│   ├── middleware/
│   │   └── authMiddleware.js
│   ├── models/
│   │   ├── User.js
│   │   └── Video.js
│   ├── routes/
│   │   ├── authRoutes.js
│   │   ├── userRoutes.js
│   │   └── videoRoutes.js
│   ├── seed/
│   │   └── seed.js           # Seed fake users + videos
│   ├── uploads/              # For video uploads (dev only)
│   ├── .env
│   ├── package.json
│   └── server.js
│
├── frontend/                 # React Native (Expo) frontend
│   ├── assets/
│   │   ├── images/
│   │   └── videos/           # Sample videos for local testing
│   ├── components/           # Reusable UI components
│   │   ├── VideoCard.js
│   │   ├── ProfileCard.js
│   │   └── Navbar.js
│   ├── navigation/           # React Navigation setup
│   │   └── AppNavigator.js
│   ├── screens/              # App screens
│   │   ├── LoginScreen.js
│   │   ├── RegisterScreen.js
│   │   ├── FeedScreen.js
│   │   ├── ProfileScreen.js
│   │   └── UploadScreen.js
│   ├── services/             # API requests
│   │   └── api.js
│   ├── App.js
│   ├── package.json
│   └── app.json
│
├── README.md
└── .gitignore

Explanation of Each Folder
1. Backend

config/db.js → Connect to MongoDB (Atlas or local)

controllers/ → Business logic (auth, videos, users)

middleware/ → JWT verification for secure endpoints

models/ → Mongoose schemas for Users and Videos

routes/ → API routes for frontend to consume

seed/seed.js → Add fake users and videos to DB

uploads/ → Temporarily store uploaded videos (development)

server.js → Entry point

2. Frontend

assets/ → Store images/videos used in the app (for testing or seed content)

components/ → Reusable components like VideoCard, ProfileCard, Navbar

navigation/ → React Navigation stack and bottom tabs

screens/ → App pages: Feed, Profile, Login, Register, Upload

services/api.js → Axios or fetch requests to backend endpoints

App.js → Main app entry

3. Example Folder Use
Backend

backend/routes/videoRoutes.js → /api/videos/ endpoints

backend/seed/seed.js → Adds 5–10 fake users + 20 sample videos

Frontend

frontend/screens/FeedScreen.js → Fetch videos from backend and display scrollable feed

frontend/components/VideoCard.js → Plays video + shows likes + save button

frontend/services/api.js → Handles Axios requests to your Node.js backend
