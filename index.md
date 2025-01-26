<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>period_tracker_app</title>
  <style>
    :root {
      /* color variables */
      --soft-rose: #ffe2e2;
      --dark-rose: #b30059;
      --white: #fff;
      --text-color: #333;
    }

    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: var(--soft-rose);
      color: var(--text-color);
    }

    /* NAVIGATION */
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
      position: relative;
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

    /* SECTIONS */
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
      background: var(--white);
      border-radius: 8px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
      padding: 20px;
      margin-top: 20px;
    }
    .box p {
      line-height: 1.6;
      margin-bottom: 15px;
    }
    .buttons-row {
      text-align: center;
      margin-top: 20px;
    }
    .buttons-row a {
      display: inline-block;
      margin: 0 10px;
      padding: 10px 15px;
      background: var(--dark-rose);
      color: var(--white);
      text-decoration: none;
      border-radius: 4px;
      font-weight: bold;
    }
    .buttons-row a:hover {
      background: #a10050;
    }

    /* TEAM */
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

    /* APP SECTION */
    .app-container {
      display: flex;
      flex-direction: column;
      gap: 30px;
    }
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

    /* Hide forms/menus by default */
    #register-form, #app-menu {
      display: none;
    }

    .app-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 20px;
      justify-content: center;
    }
    .app-buttons button {
      flex: 1 0 180px;
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

    /* CALENDAR */
    #calendar-section {
      display: none; /* hidden until user clicks 'Register My Period' */
      margin-top: 20px;
      text-align: center;
    }
    .calendar-grid {
      display: grid;
      grid-template-columns: repeat(7, 40px);
      gap: 10px;
      justify-content: center;
      margin-bottom: 20px;
      margin-top: 20px;
    }
    .day {
      width: 40px;
      height: 40px;
      line-height: 40px;
      background: #fff;
      border-radius: 4px;
      cursor: pointer;
      box-shadow: 0 0 2px rgba(0,0,0,0.2);
      text-align: center;
      font-weight: bold;
      color: var(--dark-rose);
    }
    .day:hover {
      background-color: #fcd8d8;
    }
    .highlighted {
      background-color: #ffd8e8; /* highlight selected days */
    }

    footer {
      text-align: center;
      padding: 20px;
      font-size: 0.9rem;
      color: #777;
      margin-top: 50px;
    }

    /* Hide sections except home by default */
    #home-section, #mission-section, #team-section, #app-section {
      display: none;
    }
  </style>
</head>
<body>
  <!-- NAV -->
  <nav>
    <div class="brand">period_tracker_app</div>
    <ul>
      <li><a href="#home" onclick="showSection('home-section')">Home</a></li>
      <li><a href="#mission" onclick="showSection('mission-section')">Mission</a></li>
      <li><a href="#team" onclick="showSection('team-section')">Team</a></li>
      <li><a href="#app" onclick="showSection('app-section')">Try Our App</a></li>
    </ul>
  </nav>

  <!-- HOME SECTION -->
  <section id="home-section">
    <h1>Welcome to period_tracker_app</h1>
    <div class="box">
      <p>
        <strong>period_tracker_app</strong> is designed to help you understand, track, and manage your menstrual cycle in a way that’s especially didactic, organized, and supportive for teens and college students. Unlike other period-tracking apps, we focus on making content engaging and accessible—so you can learn how to use your hormones to your advantage rather than just cope with them.
      </p>
      <p>
        We believe that hormones don’t have to be the source of pain or discomfort; with the right knowledge, they can boost your productivity, creativity, and overall well-being. Our goal is to empower girls and women to approach their cycles with confidence. By shedding the mystery and providing clear, age-appropriate info, we hope to turn what’s often seen as a burden into a powerful ally.
      </p>
      <p><strong>The story:</strong></p>
      <p>
        The idea for this app was born when my little sister first started her period. I wanted to help her feel informed, comfortable, and prepared—yet every period-tracking app I found was overwhelming, dense, or simply not designed for younger audiences. As I spoke with more women, from teenagers to college students, I realized they too were dissatisfied with existing apps. Many struggled to understand their cycles, and the information they received in schools or at home felt incomplete.
      </p>
      <p>
        Parents also voiced their concerns. Some wanted to share more detailed knowledge about topics like sexual health, hormones, and cycle tracking; others preferred a more gradual approach. They needed a resource that could adapt to each family’s comfort level. Seeing this universal need for a teen-friendly, parent-approved, and truly empowering platform, I decided to build an app that would close these gaps—one that balances in-depth knowledge with a thoughtful presentation for young minds.
      </p>
      <div class="buttons-row">
        <a href="#mission" onclick="showSection('mission-section')">Our Mission</a>
        <a href="#team" onclick="showSection('team-section')">Meet the Team</a>
      </div>
    </div>
  </section>

  <!-- MISSION SECTION -->
  <section id="mission-section">
    <h2>Our Mission</h2>
    <div class="box">
      <p>
        Our mission is to offer high-quality resources for teens and families navigating menstrual health. We strive to empower young people with the right tools and knowledge—while respecting each family’s comfort level for educational detail. By helping teens learn how to harness their hormones for wellness, productivity, and self-care, we believe we can close the gap between confusion and clarity.
      </p>
      <p>
        Ultimately, we aim to foster healthier, more informed communities—one cycle at a time.
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
          <p>Founder of period_tracker_app, dedicated to creating a safe, educational platform for teens.</p>
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
    <div class="app-container">

      <!-- LOGIN FORM -->
      <div id="login-form">
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
        <br /><br />
        <button class="btn" onclick="toggleRegister()">Register</button>
      </div>

      <!-- REGISTER FORM -->
      <div id="register-form">
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
        <br /><br />
        <button class="btn" onclick="toggleRegister()">Back to Login</button>
      </div>

      <!-- MAIN MENU AFTER LOGIN -->
      <div id="app-menu">
        <h3>Welcome, <span id="user-welcome"></span>!</h3>
        <p>Your unique ID: <span id="user-id"></span></p>

        <div class="app-buttons">
          <button onclick="toggleCalendar()">Register My Period</button>
          <button>Learning My Cycle</button>
          <button>Protecting Myself</button>
          <button>My Mental Health</button>
          <button>Ring-Health</button>
          <button>Productivity</button>
        </div>

        <!-- CALENDAR SECTION -->
        <div id="calendar-section">
          <h4>Click on any date(s) to register your period days</h4>
          <div class="calendar-grid" id="calendar-grid"></div>
        </div>

      </div>
    </div>
  </section>

  <footer>
    &copy; 2025 period_tracker_app. All Rights Reserved.
  </footer>

  <script>
    /*************************
     * NAV SHOW/HIDE SECTIONS
     *************************/
    function showSection(id) {
      document.getElementById('home-section').style.display = 'none';
      document.getElementById('mission-section').style.display = 'none';
      document.getElementById('team-section').style.display = 'none';
      document.getElementById('app-section').style.display = 'none';

      document.getElementById(id).style.display = 'block';
    }

    // Show Home by default on page load
    showSection('home-section');

    /******************************
     * LOGIN / REGISTER LOGIC
     ******************************/
    const loginForm    = document.getElementById('login-form');
    const registerForm = document.getElementById('register-form');
    const appMenu      = document.getElementById('app-menu');

    // In a real app, you'd use a server/database. For demo, we store in localStorage:
    let users = JSON.parse(localStorage.getItem('users')) || {};

    function toggleRegister() {
      // Hide login, show register or vice versa
      if (registerForm.style.display === 'none') {
        registerForm.style.display = 'block';
        loginForm.style.display    = 'none';
      } else {
        registerForm.style.display = 'none';
        loginForm.style.display    = 'block';
      }
    }

    function registerUser() {
      const username = document.getElementById('reg-username').value.trim();
      const password = document.getElementById('reg-password').value.trim();
      if (!username || !password) {
        alert('Please enter a username and password.');
        return;
      }
      if (users[username]) {
        alert('Username already exists. Choose another.');
        return;
      }
      const userId = 'ID-' + Math.floor(Math.random() * 1000000);
      users[username] = { password, id: userId, periods: [] };
      localStorage.setItem('users', JSON.stringify(users));

      alert(`Welcome, ${username}! Your account is created. Your ID: ${userId}`);
      toggleRegister();
    }

    function loginUser() {
      const username = document.getElementById('login-username').value.trim();
      const password = document.getElementById('login-password').value.trim();

      if (users[username] && users[username].password === password) {
        // Successful login
        document.getElementById('user-welcome').textContent = username;
        document.getElementById('user-id').textContent = users[username].id;

        loginForm.style.display    = 'none';
        registerForm.style.display = 'none';
        appMenu.style.display      = 'block';
      } else {
        alert('Invalid username or password.');
      }
    }

    /******************************
     * CALENDAR LOGIC
     ******************************/
    const calendarGrid = document.getElementById('calendar-grid');
    let currentUser    = null;
    const daysInMonth  = 31; // Example of a 31-day month

    function initCalendar() {
      calendarGrid.innerHTML = ''; // Clear previous days
      for (let d = 1; d <= daysInMonth; d++) {
        const dayCell = document.createElement('div');
        dayCell.className = 'day';
        dayCell.textContent = d;
        dayCell.addEventListener('click', () => toggleDaySelection(d));
        calendarGrid.appendChild(dayCell);
      }
    }

    function renderSelectedDays() {
      currentUser = document.getElementById('user-welcome').textContent;
      if (!currentUser || !users[currentUser]) return;

      const selectedDays = users[currentUser].periods || [];
      const dayCells = calendarGrid.querySelectorAll('.day');
      dayCells.forEach(cell => {
        cell.classList.remove('highlighted');
      });
      selectedDays.forEach(day => {
        const cell = dayCells[day - 1];
        if (cell) cell.classList.add('highlighted');
      });
    }

    function toggleDaySelection(day) {
      currentUser = document.getElementById('user-welcome').textContent;
      if (!currentUser) {
        alert('Please log in first.');
        return;
      }
      let selectedDays = users[currentUser].periods;
      if (selectedDays.includes(day)) {
        selectedDays = selectedDays.filter(d => d !== day);
      } else {
        selectedDays.push(day);
      }
      users[currentUser].periods = selectedDays;
      localStorage.setItem('users', JSON.stringify(users));
      renderSelectedDays();
    }

    function toggleCalendar() {
      const calendarSection = document.getElementById('calendar-section');
      if (calendarSection.style.display === 'none') {
        calendarSection.style.display = 'block';
        initCalendar();
        renderSelectedDays();
      } else {
        calendarSection.style.display = 'none';
      }
    }
  </script>
</body>
</html>
