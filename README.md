# EliteEstate
The code is pvt for interviews/discussions, but I'm adding additional link here for visitors to checkout the site as a user/client. I've created this project to showcase my programming skills. Enjoy your time here!

A real estate web application built with the MERN stack, designed to make browsing, creating, and managing property listings simple and intuitive.

MERN Estate brings together a clean user interface, secure authentication, and image handling in one full-stack project. It started as a way to put my React, Node.js, and MongoDB skills into practice and grew into a hands-on exploration of how a real-world web application works from frontend to backend.

**Live Demo:** [View MERN Estate](YOUR_RENDER_LIVE_URL)

**Source Code:** [GitHub Repository](https://github.com/YOUR_GITHUB_USERNAME/mern-estate)

---

## ✨ Features

- **User Authentication** — Create an account, sign in, and manage your profile.
- **Google Sign-In** — Google authentication integration using Firebase.
- **Property Listings** — Create, update, and delete property listings.
- **Advanced Search** — Browse listings using filters such as location, property type, and price.
- **Image Uploads** — Upload multiple property images, stored using MongoDB GridFS.
- **Listing Details** — View property information, pricing, and images in one place.
- **Responsive UI** — A layout designed to work across desktop and mobile screens.
- **Protected Routes** — Restrict listing management actions to authenticated users.

## 🛠️ Tech Stack

| Layer | Technologies |
|---|---|
| Frontend | React, Vite, Tailwind CSS |
| Backend | Node.js, Express.js |
| Database | MongoDB Atlas, Mongoose |
| Image Storage | MongoDB GridFS |
| Authentication | JWT, cookies, Firebase integration |
| Deployment | Render |
| Version Control | Git, GitHub |

## 🖥️ Getting Started

Want to run the project locally? Follow the steps below.

### Prerequisites

Make sure you have these installed:

- [Node.js](https://nodejs.org/)
- npm
- A [MongoDB Atlas](https://www.mongodb.com/products/platform/atlas-database) cluster or local MongoDB instance
- A Firebase project if you want to configure Google authentication

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_GITHUB_USERNAME/mern-estate.git
cd mern-estate
```

### 2. Set up the backend

```bash
cd api
npm install
```

Create a `.env` file inside the `api` directory:

```env
MONGO=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
```

Add any other environment variables required by your current configuration. Keep all secrets out of version control.

Start the backend using the script defined in `api/package.json`. If your project has a `dev` script, run:

```bash
npm run dev
```

### 3. Set up the frontend

Open another terminal:

```bash
cd client
npm install
npm run dev
```

Vite will display the local URL where the frontend is available.

> **Note:** Configure the frontend's API URL and Firebase settings for your local environment as needed. Google authentication also requires valid Firebase and OAuth configuration.

## 📁 Project Structure

```text
mern-estate/
├── api/
│   ├── controllers/     # Request handling and business logic
│   ├── models/          # Mongoose schemas
│   ├── routes/          # API endpoints
│   ├── utils/           # Shared utilities and GridFS setup
│   └── index.js         # Express server entry point
│
├── client/
│   └── src/
│       ├── components/  # Reusable UI components
│       ├── pages/       # Application pages
│       ├── utils/       # Formatting and helper functions
│       └── firebase.js # Firebase initialization
│
└── README.md
```

## 🖼️ Image Storage

Property images are stored in MongoDB using **GridFS**, rather than relying on a separate file-storage service.

The backend handles image uploads, stores file metadata, and serves images through dedicated API routes. Listings keep references to the uploaded image URLs, allowing property details and images to work together.

Uploads are restricted by file size and image type, helping keep the application manageable.

## 🔐 Authentication & Security

The application uses JSON Web Tokens (JWT) and cookies for authenticated requests. Protected backend routes verify the user's token before allowing operations that require authentication.

Firebase is also integrated for Google authentication. The OAuth configuration must be valid for Google sign-in to work in a deployed environment.

**Security note:** Never commit `.env` files, database credentials, JWT secrets, or private API keys to GitHub.

## 🚀 Deployment

The application is deployed on Render, with MongoDB Atlas providing the database.

For a production deployment, configure the following:

- MongoDB connection string
- JWT secret
- Frontend and backend URLs, where applicable
- Firebase configuration and authorized OAuth domains
- Correct build and start commands for the deployed services

After changing environment variables, redeploy or restart the relevant service so the new configuration takes effect.

## 🧠 What I Learned

Building MERN Estate gave me practical experience with:

- Connecting a React frontend to an Express API
- Designing REST endpoints and Mongoose models
- Implementing JWT-based authentication
- Handling multipart uploads with Multer and storing files with GridFS
- Managing application state and forms in React
- Configuring environment variables and deploying a full-stack application
- Debugging the small integration issues that appear when separate parts of a stack meet

## 🗺️ What's Next

There is plenty of room to build on the current version. Some improvements I'd like to explore include:

- Better listing discovery and sorting
- More robust form validation and error handling
- Image cleanup when listings or uploaded images are removed
- Improved accessibility and loading states
- Automated testing for important API routes and user flows

## 👋 About

MERN Estate is a personal full-stack development project built to explore the MERN ecosystem through a practical application.

If you have feedback, spot a bug, or have an idea for an improvement, feel free to open an issue or reach out.

**Thanks for checking out MERN Estate!**

