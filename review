<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Senior Reviews – Job & Internship</title>

  <style>
    * { box-sizing: border-box; }

    body {
      margin: 0;
      font-family: "Segoe UI", sans-serif;
      background: linear-gradient(135deg, #4f46e5, #22c55e);
      min-height: 100vh;
      padding: 30px;
      color: #fff;
    }

    .container {
      max-width: 900px;
      margin: auto;
      background: rgba(255,255,255,0.15);
      backdrop-filter: blur(15px);
      border-radius: 20px;
      padding: 30px;
      box-shadow: 0 20px 40px rgba(0,0,0,0.3);
    }

    h1 {
      text-align: center;
      margin-bottom: 10px;
    }

    p.subtitle {
      text-align: center;
      opacity: 0.9;
      margin-bottom: 25px;
    }

    .reviews {
      display: grid;
      gap: 15px;
    }

    .card {
      background: rgba(0,0,0,0.35);
      padding: 18px;
      border-radius: 14px;
      animation: fadeIn 0.4s ease;
    }

    .card h3 {
      margin: 0;
    }

    .role {
      font-size: 14px;
      opacity: 0.85;
    }

    .type {
      display: inline-block;
      margin-top: 6px;
      font-size: 12px;
      padding: 4px 10px;
      border-radius: 20px;
      background: rgba(255,255,255,0.2);
    }

    .stars {
      color: gold;
      margin: 8px 0;
    }

    .add-btn {
      margin-top: 25px;
      width: 100%;
      padding: 14px;
      border-radius: 14px;
      border: none;
      font-size: 16px;
      font-weight: bold;
      background: #22c55e;
      color: #000;
      cursor: pointer;
    }

    .add-btn:hover {
      opacity: 0.9;
    }

    .form-box {
      display: none;
      margin-top: 25px;
      background: rgba(255,255,255,0.2);
      padding: 20px;
      border-radius: 14px;
    }

    input, textarea, select {
      width: 100%;
      padding: 10px;
      margin-top: 10px;
      border-radius: 8px;
      border: none;
      font-family: inherit;
    }

    textarea {
      resize: none;
      height: 80px;
    }

    .submit {
      margin-top: 15px;
      padding: 12px;
      background: #4f46e5;
      color: white;
      border: none;
      border-radius: 10px;
      font-weight: bold;
      cursor: pointer;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(10px); }
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>

<body>

<div class="container">
  <h1>🎓 Senior Experience Reviews</h1>
  <p class="subtitle">Learn from seniors about jobs & internships</p>

  <!-- Dummy Reviews -->
  <div class="reviews" id="reviews">
    <div class="card">
      <h3>Rohit Sharma</h3>
      <div class="role">Software Intern – Google</div>
      <div class="type">Internship</div>
      <div class="stars">★★★★★</div>
      <p>Great learning environment. Mentors were very supportive and projects were real-world.</p>
    </div>

    <div class="card">
      <h3>Ananya Verma</h3>
      <div class="role">Frontend Developer – StartupX</div>
      <div class="type">Job</div>
      <div class="stars">★★★★☆</div>
      <p>Fast-paced work culture. Learned a lot about production-level React applications.</p>
    </div>

    <div class="card">
      <h3>Vikas Mehta</h3>
      <div class="role">Data Analyst Intern – Infosys</div>
      <div class="type">Internship</div>
      <div class="stars">★★★★☆</div>
      <p>Good exposure to SQL and dashboards. Work-life balance was decent.</p>
    </div>
  </div>

  <button class="add-btn" onclick="showForm()">➕ Add Your Review</button>

  <!-- Review Form -->
  <div class="form-box" id="formBox">
    <input id="name" placeholder="Your Name">
    <input id="company" placeholder="Company Name">
    <input id="role" placeholder="Role">
    
    <select id="type">
      <option>Internship</option>
      <option>Job</option>
    </select>

    <select id="rating">
      <option value="5">★★★★★ (5)</option>
      <option value="4">★★★★☆ (4)</option>
      <option value="3">★★★☆☆ (3)</option>
      <option value="2">★★☆☆☆ (2)</option>
      <option value="1">★☆☆☆☆ (1)</option>
    </select>

    <textarea id="review" placeholder="Write your experience..."></textarea>

    <button class="submit" onclick="addReview()">Submit Review</button>
  </div>
</div>

<script>
  function showForm() {
    document.getElementById("formBox").style.display = "block";
    document.getElementById("formBox").scrollIntoView({ behavior: "smooth" });
  }

  function addReview() {
    const name = document.getElementById("name");
    const company = document.getElementById("company");
    const role = document.getElementById("role");
    const type = document.getElementById("type");
    const rating = document.getElementById("rating");
    const review = document.getElementById("review");

    if (!name.value || !company.value || !role.value || !review.value) {
      alert("Please fill all fields");
      return;
    }

    const stars = "★★★★★☆☆☆☆☆".slice(5 - rating.value, 10 - rating.value);

    const card = document.createElement("div");
    card.className = "card";
    card.innerHTML = `
      <h3>${name.value}</h3>
      <div class="role">${role.value} – ${company.value}</div>
      <div class="type">${type.value}</div>
      <div class="stars">${stars}</div>
      <p>${review.value}</p>
    `;

    document.getElementById("reviews").prepend(card);

    /* reset form */
    name.value = "";
    company.value = "";
    role.value = "";
    review.value = "";
    rating.value = "5";
    type.value = "Internship";

    alert("✅ Review added successfully!");
  }
</script>

</body>
</html>
