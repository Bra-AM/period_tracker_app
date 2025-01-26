<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Period Tracker App</title>
  <style>
    :root {
      --soft-rose: #ffe2e2;   /* background */
      --dark-rose: #b30059;  /* accent color */
      --white: #fff;
      --text-color: #333;
      --box-bg: #fff;
    }

    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: var(--soft-rose);
      color: var(--text-color);
    }

    /***************
     * NAVIGATION  *
     ***************/
    nav {
      background-color: var(--white);
      border-bottom: 2px solid #f5c6d6;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 0 20px;
      position: sticky;
      top: 0;
    }

    nav .brand {
      font-weight: bold;
      font-size: 1.2rem;
      color: var(--dark-rose);
      padding: 10px 0;
    }

    nav ul {
      list-style: none;
      display: flex;
      gap: 20px;
      margin: 0;
    }

    nav li {
      position: relative; /* for dropdown */
    }

    nav a {
      text-decoration: none;
      color: var(--dark-rose);
      font-weight: bold;
      padding: 10px;
    }

    nav a:hover {
      text-decoration: underline;
    }

    /* Dropdown styling */
    .dropdown {
      display: none;
      position: absolute;
      background: var(--white);
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
      border: 1px solid #f2f2f2;
      top: 40px; /* just below the nav item */
      left: 0;
      z-index: 999;
    }

    .dropdown li {
      display: block;
      margin: 0;
      white-space: nowrap;
    }

    .dropdown li a {
      display: block;
      padding: 10px;
      color: var(--dark-rose);
    }

    nav li:hover .dropdown {
      display: block;
    }

    /***************
     *   SECTIONS  *
     ***************/
    section {
      padding: 40px 20px;
      max-width: 900px;
      margin: 0 auto;
    }

    h1, h2 {
      text-align: center;
      color: var(--dark-rose);
      margin-bottom: 20px;
    }

    .box {
      background: var(--box-bg);
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
      padding: 20px;
      margin-top: 20px;
    }

    .box p {
      line-height: 1.6;
    }

    .inline-links {
      text-align: center;
      margin-top: 20px;
    }

    /************************
     * TEAM SECTION STYLES  *
     ************************/
    .team-member {
      display: flex;
      align-items: center;
      gap: 20px;
      margin-bottom: 20px;
    }

    .team-photo {
      width: 100px;
      height: 100px;
      background: #ddd url('https://via.placeholder.com/100') center/cover no-repeat;
      border-radius: 50%;
      flex-shrink: 0;
    }

    /************************
     *  APP SECTION STYLES  *
     ************************/
    .form-group {
      margin-bottom: 15px;
    }

    .form-group label {
      display: block;
      margin-bottom: 8px;
      font-weight: bold;
    }

    .form-group input {
      width: 100%;
      padding: 8px;
      border: 1px solid #ccc;
      border-radius: 4px;
    }

    .btn {
      background-color: var(--dark-rose);
      color: var(--white);
      padding: 10px 15px;
      border: none;
      border-radius: 4px;
      cursor: pointer;
      font-weight: bold;
    }

    .btn:hover {
      background-color: #a10050;
    }

    .app-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 20px;
    }

    .app-buttons button {
      flex: 1 0 220px;
      padding: 15px;
      border: none;
      border-radius: 8px;
      background-color: var(--dark-rose);
      color: var(--white);
      font-weight: bold;
      cursor: pointer;
    }

    .app-buttons button:hover {
      background-color: #a10050;
    }

    .calendar-section {
      margin-top: 20px;
    }

    .calendar-section label {
      font-weight: bold;
    }

    .mood-select, .pain-select {
      margin-left: 10px;
      margin-right: 20px;
    }

    /* Hide sections by default; JavaScript can show/hide them if desired */
    /* If you'd rather show them all at once, remove these lines.
       Or replace with .hidden { display: none; } and toggle via JS. */
    #about-section, #mission-section, #team-section, #app-section {
      display: none;
    }

    footer {
      text-align: center;
      padding: 20px;
      font-size: 0.9rem;
      color: #777;
      margin-top: 50px;
    }
  </style>
</head>
<body>
  <!-- NAV BAR -->
  <nav>
    <div class="brand">period_tracker_app</div>
    <ul>
      <li><a href="#home" onclick="showSection('home-section')">Home</a></li>
      <li>
        <a href="#">About</a>
        <!-- Dropdown -->
        <ul class="dropdown">
          <li><a href="#mission" onclick="showSection('mission-section')">Mission</a></li>
          <li><a href="#team" onclick="showSection('team-section')">Team</a></li>
        </ul>
      </li>
      <li><a href="#app" onclick="showSection('app-section')">Try Our App</a></li>
    </ul>
  </nav>

  <!-- HOME SECTION -->
  <section id="home-section">
    <h1>Welcome to period_tracker_app</h1>
    <div class="box">
      <p>
        period_tracker_app is designed to help you understand, track, and manage your menstrual cycle in a way that’s especially friendly for teens (and their families). We want to simplify this journey and empower you to feel confident about your body—every step of the way.
      </p>
      <p>
        The idea for this app was born when my little sister first started her period. I wanted to help her feel informed, comfortable, and prepared—yet every period-tracking app I found was overwhelming, dense, or simply not designed for younger audiences. As I spoke with more women, from teenagers to college students, I realized they too were dissatisfied with existing apps. Many struggled to understand their cycles, and the information they received in schools or at home felt incomplete.
      </p>
      <p>
        Parents also voiced their concerns. Some wanted to share more detailed knowledge about topics like sexual health, hormones, and cycle tracking; others preferred a more gradual approach. They needed a resource that could adapt to each family’s comfort level. Seeing this universal need for a teen-friendly, parent-approved, and truly empowering platform, I decided to build an app that would close these gaps—one that balances in-depth knowledge with a thoughtful presentation for young minds.
      </p>
    </div>
  </section>

  <!-- MISSION SECTION -->
  <section id="mission-section">
    <h2>Mission</h2>
    <div class="box">
      <p>
        Our mission is to offer high-quality resources for teens and families navigating menstrual health. We strive to empower young people with the right tools and knowledge—while respecting each family’s comfort level for educational detail. By helping teens learn how to harness their hormones for wellness, productivity, and self-care, we believe we can close the gap between confusion and clarity, and ultimately foster healthier, more informed communities.
      </p>
    </div>
  </section>

  <!-- TEAM SECTION -->
  <section id="team-section">
    <h2>Team</h2>
    <div class="box">
      <div class="team-member">
        <div class="team-photo"></div>
        <div>
          <p><strong>Brady</strong></p>
          <p>Founder of period_tracker_app. Passionate about accessible menstrual health education for teens.</p>
        </div>
      </div>
      <p>We’re looking for:</p>
      <ul>
        <li>A Software Engineer to help grow and maintain the app’s features</li>
        <li>A Health Specialist to transform medical information into digestible, teen-friendly content</li>
        <li>A Marketing Advisor to reach more families and spread the word about our mission</li>
      </ul>
    </div>
  </section>

  <!-- TRY OUR APP SECTION -->
  <section id="app-section">
    <h2>Try Our App</h2>
    <div class="box">
      <!-- LOGIN / REGISTER FORMS -->
      <div id="auth-forms">
        <h3>Log In</h3>
        <div class="form-group">
          <label for="login-username">Username:</label>
          <input type="text" id="login-username" placeholder="Enter username" />
        </div>
        <div class="form-group">
          <label for="login-password">Password:</label>
          <input type="password" id="login-password" placeholder="Enter password" />
        </div>
        <button class="btn" onclick="loginUser()">Log In</button>

        <hr />
        <h3>Register</h3>
        <div class="form-group">
          <label for="reg-username">Nickname (Username):</label>
          <input type="text" id="reg-username" placeholder="Create a username" />
        </div>
        <div class="form-group">
          <label for="reg-password">Password:</label>
          <input type="password" id="reg-password" placeholder="Create a password" />
        </div>
        <button class="btn" onclick="registerUser()">Create Account</button>
      </div>

      <!-- APP MAIN MENU (hidden until logged in) -->
      <div id="app-menu" style="display:none;">
        <h3>Welcome, <span id="user-welcome"></span>!</h3>
        <p>Your unique ID is <span id="user-id"></span></p>

        <div class="app-buttons">
          <button onclick="showRegisterPeriod()">Register My Period</button>
          <button>Learning My Cycle</button>
          <button>Protecting Myself</button>
          <button>My Mental Health</button>
          <button>Ring-Health</button>
          <button>Productivity</button>
        </div>

        <!-- Period Registration Interface -->
        <div id="register-period-section" class="calendar-section" style="display:none;">
          <h4>Register Your Period</h4>
          <label>Select Period Dates:</label>
          <input type="date" id="period-start" /> to
          <input type="date" id="period-end" />
          <br/><br/>
          <label>Mood:</label>
          <select id="mood" class="mood-select">
            <option value="Calm">Calm</option>
            <option value="Happy">Happy</option>
            <option value="Sad">Sad</option>
            <option value="Anxious">Anxious</option>
          </select>

          <label>Pain Level (0-5):</label>
          <select id="pain" class="pain-select">
            <option value="0">0</option><option value="1">1</option>
            <option value="2">2</option><option value="3">3</option>
            <option value="4">4</option><option value="5">5</option>
          </select>
          <br/><br/>
          <button class="btn" onclick="savePeriodData()">Save Period Info</button>
        </div>
      </div>
    </div>
  </section>

  <footer>
    &copy; 2025 period_tracker_app. All Rights Reserved.
  </footer>

  <script>
    /**************************************
     * Show/Hide Sections from Nav Clicks *
     **************************************/
    function showSection(sectionId) {
      // Hide all sections
      document.getElementById('home-section').style.display = 'none';
      document.getElementById('mission-section').style.display = 'none';
      document.getElementById('team-section').style.display = 'none';
      document.getElementById('app-section').style.display = 'none';

      // Show the selected one
      document.getElementById(sectionId).style.display = 'block';
    }

    // By default, show Home
    showSection('home-section');


    /**************************************
     * Simple Registration / Login Logic  *
     *    (Local Storage Demonstration)   *
     **************************************/
    const authForms = document.getElementById('auth-forms');
    const appMenu   = document.getElementById('app-menu');

    // For demonstration, store user info in localStorage
    // Format: localStorage.setItem('users', JSON.stringify({ username: {password, id, ...} }))
    let users = JSON.parse(localStorage.getItem('users')) || {};

    function registerUser() {
      const username = document.getElementById('reg-username').value.trim();
      const password = document.getElementById('reg-password').value.trim();
      if (!username || !password) {
        alert('Please enter a valid username and password.');
        return;
      }
      if (users[username]) {
        alert('Username already exists. Please choose another.');
        return;
      }

      // Create a unique ID
      const userId = 'ID-' + Math.floor(Math.random() * 1000000);

      users[username] = {
        password: password,
        id: userId,
        periodData: []
      };

      localStorage.setItem('users', JSON.stringify(users));
      alert(`User '${username}' registered successfully! Your ID is ${userId}.`);
    }

    function loginUser() {
      const username = document.getElementById('login-username').value.trim();
      const password = document.getElementById('login-password').value.trim();

      if (users[username] && users[username].password === password) {
        // Successful login
        document.getElementById('user-welcome').textContent = username;
        document.getElementById('user-id').textContent = users[username].id;

        authForms.style.display = 'none';
        appMenu.style.display   = 'block';
      } else {
        alert('Invalid username or password.');
      }
    }

    /********************************************
     * Period Registration (attached to user ID) *
     ********************************************/
    function showRegisterPeriod() {
      const registerSection = document.getElementById('register-period-section');
      registerSection.style.display = registerSection.style.display === 'none' ? 'block' : 'none';
    }

    function savePeriodData() {
      const currentUser = document.getElementById('user-welcome').textContent;
      if (!currentUser) {
        alert('No user logged in.');
        return;
      }
      const startDate = document.getElementById('period-start').value;
      const endDate   = document.getElementById('period-end').value;
      const mood      = document.getElementById('mood').value;
      const pain      = document.getElementById('pain').value;

      if (!startDate || !endDate) {
        alert('Please select start and end dates for your period.');
        return;
      }

      // Save to localStorage
      const userObj = users[currentUser];
      if (!userObj) return;

      userObj.periodData.push({
        start: startDate,
        end: endDate,
        mood: mood,
        pain: pain
      });

      users[currentUser] = userObj;
      localStorage.setItem('users', JSON.stringify(users));
      alert('Period info saved!');
    }
  </script>
</body>
</html>
