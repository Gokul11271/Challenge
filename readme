# MERN Backend Setup

![Node.js](https://img.shields.io/badge/Node.js-v22.13.0-green)
![Express](https://img.shields.io/badge/Express-v5.1.0-blue)
![MongoDB](https://img.shields.io/badge/MongoDB-v8.19.0-brightgreen)
![Nodemon](https://img.shields.io/badge/Nodemon-v3.1.10-orange)

---

## Overview

This is a **backend setup** for a MERN stack project using:

* **Node.js** + **Express.js** for server
* **MongoDB** + **Mongoose** for database
* **dotenv** for environment variables
* **Nodemon** for auto-reloading during development
* **CORS** enabled for frontend-backend communication

The server is ready to handle API routes, controllers, and MongoDB models.

---

## Features

* REST API ready
* MongoDB connection using Mongoose
* Environment variables support via `.env`
* Auto-reloading with Nodemon
* CORS enabled
* Clean folder structure for scalability

---

## Prerequisites

* [Node.js](https://nodejs.org/) >= 18.x
* [npm](https://www.npmjs.com/) >= 9.x
* MongoDB database (local or Atlas)

---

## Getting Started

### 1. Clone the repository

```bash
git clone <your-git-repo-url>
cd back-end
```

### 2. Install dependencies

```bash
npm install
```

### 3. Create `.env` file

Create a `.env` file in the **root directory** with the following content:

```env
MONGO_URI=<your_mongodb_connection_string>
PORT=5000
```

* Replace `<your_mongodb_connection_string>` with your MongoDB URI.
* For local MongoDB:

```env
MONGO_URI=mongodb://127.0.0.1:27017/myDatabase
PORT=5000
```

---

## NPM Scripts

| Command       | Description                                     |
| ------------- | ----------------------------------------------- |
| `npm run dev` | Start the server with **nodemon** (auto-reload) |
| `npm start`   | Start the server without nodemon                |
| `npm test`    | Run tests (currently a placeholder)             |

---

## Folder Structure

```
back-end/
│
├─ src/
│  ├─ server.js        # Main server file
│  ├─ routes/          # API routes
│  ├─ controllers/     # Route handlers / business logic
│  └─ models/          # Mongoose models
│
├─ package.json
├─ package-lock.json
└─ .env
```

* **server.js** – Initializes the server, middleware, routes, and MongoDB connection.
* **routes/** – Define API endpoints.
* **controllers/** – Handle the business logic for routes.
* **models/** – Define Mongoose schemas and models.

---

## Example Server Test

Start the server:

```bash
npm run dev
```

Test the API using a browser or Postman:

```
GET http://localhost:5000/
```

Expected response:

```text
Server is running!
```

---

## Notes & Best Practices

* **Remove deprecated options** from Mongoose v8+:

```javascript
mongoose.connect(process.env.MONGO_URI)
  .then(() => console.log("MongoDB connected ✅"))
  .catch((err) => console.error("MongoDB connection error:", err));
```

* **Suppress dotenv tips** (optional):

```javascript
import dotenv from "dotenv";
dotenv.config({ silent: true });
```

* **Do not commit `.env`** to GitHub. Add it to `.gitignore`.
* Use `nodemon.json` to ignore unnecessary file changes:

```json
{
  "watch": ["src"],
  "ext": "js,json",
  "ignore": ["node_modules", ".env"]
}
```

* Ensure **MONGO_URI** is correctly set in `.env` to connect to MongoDB.

---

## Connecting to Frontend

1. Ensure CORS is enabled in `server.js`:

```javascript
import cors from "cors";
app.use(cors());
```

2. In frontend (React, Vue, etc.), make API calls to:

```
http://localhost:5000/api/your-route
```

---

## Author

* **Your Name**
* GitHub: [YourGitHubUsername](https://github.com/YourGitHubUsername)
* Email: [youremail@example.com](mailto:youremail@example.com)

---

## License

This project is licensed under the MIT License.
