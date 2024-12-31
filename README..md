# DIGITAL ART GALLERY

## Overview
The Image Viewer and Upload Portal is a web application designed to provide users with functionality to view images in a modal viewer, upload their work, and manage uploaded images interactively. It features a image zoom capabilities, and integration with a MySQL database for user authentication and image storage.

---

## Features

### Image Viewer
- *View images in a full-screen modal*: Allows users to see images in an expanded view.
- *Navigate through images using *Next and Previous buttons**: Easily cycle through images.
- *Zoom functionality to magnify images*: Zoom in on the image for better details.
- *Close the viewer by clicking outside the image or using the *Close button**: Close the modal when done viewing.

### Image Upload
- *Upload images directly from the browser*: Easily upload images from your local system.
- *Preview uploaded images dynamically in a flex*: See images in a grid format after uploading.
- *Store uploaded image paths in the database for future retrieval*: Ensure uploaded images are stored in the database for later use.

### User Authentication
- *Sign Up*: Register a new account securely to access the portal.
- *Sign In*: Log in using your email and password.
- *Session Management*: Maintain user sessions securely so users stay logged in.

---

## Project Structure

### Frontend
1. *PHP*:
   - Core structure provided in index.php,indx.php,about.php,category,php and profile.php. These files define the layout and structure of the web pages.
2. *CSS*:
   - Styling implemented in style.css,styles.css Controls the visual appearance and layout.
3. *JavaScript*:
   - Logic and interactivity handled in image-viewer.js. Manages the viewer functions like image zoom and navigation.

### Backend
1. *PHP*:
   - Handles server-side logic for authentication, image uploads, and session management.
   - Files: connect.php, register.php, upload.php, logout.php
2. *MySQL Database*:
   - Stores user credentials and uploaded image paths.
   - Database: login.
   - file: login.sql

---

## Installation

### Prerequisites
- *XAMPP*: Install a local server environment (https://www.apachefriends.org/).
- *MySQL*: Set up a database for storing user information and images.

### Steps

1. *Clone the repository*:

*Set up the database:*

Open phpMyAdmin in your browser (http://localhost/dashboard).
Create a database named login.
Import the provided SQL schema file login.sql to create necessary tables.


*Configure Backend:*

Place the project files in the htdocs folder of your local server (C:\xampp\htdocs).
Start Apache and MySQL services from the XAMPP control panel.
Access the application at http://localhost/login in your browser.



*Usage*

Image Viewer
Click on any image in the grid: Opens the full-screen viewer for detailed view.
Navigate using the Next and Previous buttons: Move between images in the viewer.
Zoom by clicking on the image: Magnify the image for a closer look.
Close the viewer by clicking outside the image or using the Close button: Close the viewer when you're done.


Uploading Images
Log in to your account: Ensure you're signed in to upload images.
Click the Upload Your Work button: Opens the file upload dialog.
Select files and confirm the upload: Choose the images to upload.
View the uploaded images in the grid: The uploaded images will appear in the profile.


API Endpoints
Authentication
Register: Handles user sign-up.

Endpoint: register.php
Method: POST
Fields: fName, email, password, confirm-password
Login: Handles user sign-in.

Endpoint: register.php
Method: POST
Fields: email, password
Image Upload
Upload: Handles image uploads.


Endpoint: upload.php
Method: POST
Fields: my_image


*Troubleshooting*
Common Errors
1. "Failed to connect DB":
Ensure the database server is running.
Verify the database credentials in connect.php match your MySQL setup.
2. "Email Address Already Exists":
Try using a unique email address during registration.
3. "An unknown error occurred!":
Check file size and format before uploading.
Ensure the uploads/ directory has the correct write permissions.

