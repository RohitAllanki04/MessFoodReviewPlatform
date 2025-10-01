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
messfood-review-platform/
├── src/
│ ├── components/ # Reusable UI components (Menu, FeedbackForm, ReviewList)
│ ├── pages/ # Page-level views (Home, Login, Dashboard)
│ ├── firebaseConfig.js # Firebase setup
│ └── App.js # Main React app
├── public/
├── package.json
└── README.md

**Clone Repository** ```bash
https://github.com/RohitAllanki04/MessFoodReviewPlatform.git
# Install Dependencies

npm install


# Configure Firebase

Create a Firebase project.

Enable Firestore Database and Authentication (Google/Email).

Copy your Firebase config into src/firebaseConfig.js:

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


# Run Application

npm start

# Tech Stack

Frontend: React, React Router, Context API/Hooks

Backend (as-a-service): Firebase Firestore

Authentication: Firebase Auth

# Example Use Cases
Action	Description
View-- Daily Menu	Displays the mess menu for today.
Select --Date	Fetch menu from Firestore by date.
Submit-- Feedback	Write review + star rating.
Real-Time-- Updates	See feedback instantly without refresh.
