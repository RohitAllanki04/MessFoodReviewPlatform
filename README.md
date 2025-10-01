# MessFoodReviewPlatform (Frontend Only)

## Overview
A **React + Firebase** frontend application that displays **daily mess menus** and allows students to provide **feedback and reviews** on meals.  
This project focuses entirely on the **frontend implementation**, with Firebase used for **authentication** and **real-time data storage**.

---

## Features
* 📅 **Daily & Date-wise Menus** – View current and past menus.  
* ⭐ **Meal Feedback** – Users can submit ratings and comments for dishes.  
* 🔒 **Secure Login** – Firebase Authentication with Email/Google login.  
* ⚡ **Real-Time Updates** – Feedback stored and synced with Firebase Firestore.  
* 📱 **Responsive UI** – Built with React hooks and reusable components.  

---

## Project Structure
```
messfood-review-platform/
├── src/
│ ├── components/ # Reusable UI components (Menu, FeedbackForm, ReviewList)
│ ├── pages/ # Page-level views (Home, Login, Dashboard)
│ ├── firebaseConfig.js # Firebase setup
│ └── App.js # Main React app
├── public/
├── package.json
└── README.md
```

---

## Getting Started

### Clone Repository
```bash
git clone https://github.com/RohitAllanki04/MessFoodReviewPlatform.git
cd MessFoodReviewPlatform
```

### Install Dependencies
```bash
npm install
```

### Configure Firebase
1. Create a Firebase project at [console.firebase.google.com](https://console.firebase.google.com).
2. Enable **Firestore Database** and **Authentication** (with Google and Email providers).
3. Copy your Firebase config into `src/firebaseConfig.js`:

```javascript
import { initializeApp } from "firebase/app";
import { getAuth } from "firebase/auth";
import { getFirestore } from "firebase/firestore";

const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_PROJECT_ID.appspot.com",
  messagingSenderId: "YOUR_SENDER_ID",
  appId: "YOUR_APP_ID"
};

const app = initializeApp(firebaseConfig);
export const auth = getAuth(app);
export const db = getFirestore(app);
```

### Run Application
```bash
npm start
```

The app will run on `http://localhost:3000`.

---

## Tech Stack
- **Frontend**: React, React Router, Context API/Hooks
- **Backend (as-a-service)**: Firebase Firestore
- **Authentication**: Firebase Auth

---

## Example Use Cases

| Action              | Description                              |
|---------------------|------------------------------------------|
| View Daily Menu     | Displays the mess menu for today.        |
| Select Date         | Fetch menu from Firestore by date.       |
| Submit Feedback     | Write review + star rating.              |
| Real-Time Updates   | See feedback instantly without refresh.  |

---

## Contributing
Feel free to fork the repo and submit pull requests for improvements or bug fixes.
