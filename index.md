---
title: Period Tracker
layout: default
---

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Period Tracker - Home</title>
  <style>
    /* Basic Reset & Body */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      font-family: Arial, sans-serif;
    }

    /* Container for sidebar + main content */
    .container {
      display: flex;
      min-height: 100vh; /* Stretch full browser height */
    }

    /* Sidebar styling */
    .sidebar {
      background-color: #f9f9f9;
      width: 220px;
      padding: 20px;
      border-right: 1px solid #ccc;
    }
    .logo {
      width: 100%;
      height: auto;
      margin-bottom: 20px; /* Space between logo and title */
    }
    /* Vertical Title */
    .sidebar h1 {
      writing-mode: vertical-rl; /* Vertical text (right-to-left) */
      transform: rotate(180deg); /* Flip it upright */
      font-size: 1.5rem;
      margin: 0 auto 20px;       /* Center and space below */
      text-align: center;
    }

    /* Navigation in the sidebar */
    .nav-links {
      list-style: none;
      padding: 0;
    }
    .nav-links li {
      margin-bottom: 10px;
    }
    .nav-links a {
      display: inline-block;
      padding: 10px 15px;
      background-color: #ccc;
      color: #000;
      text-decoration: none;
      border-radius: 4px;
      font-weight: bold;
    }
    .nav-links a:hover {
      background-color: #bbb;
    }

    /* Main content area */
    .main-content {
      flex: 1;
      padding: 20px;
    }
    /* Video placeholder box */
    .video-placeholder {
      width: 80%;
      height: 350px;
      margin: 0 auto;
      background-color: #eee;
      display: flex;
      align-items: center;
      justify-content: center;
      color: #666;
      font-size: 1.2rem;
      border: 2px dashed #ccc;
    }

  </style>
</head>
<body>
  <div class="container">
    <!-- Sidebar -->
    <div class="sidebar">
      <!-- Replace this with your actual logo image URL if desired -->
      <img src="https://via.placeholder.com/200x100?text=Logo" alt="Logo" class="logo">
      <h1>Period Tracker</h1>

      <ul class="nav-links">
        <li><a href="index.md">Home</a></li>
        <li><a href="about.md">About</a></li>
        <li><a href="try-our-app.md">Try our App</a></li>
      </ul>
    </div>

    <!-- Main content -->
    <div class="main-content">
      <div class="video-placeholder">
        Insert Videos Here
      </div>
    </div>
  </div>
</body>
</html>
