# Mr.75.com

<html lang="bn">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Shakib Al Hasan - Cricket History</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background: #f0f8ff;
      margin: 0;
      padding: 0;
      transition: 0.3s;
    }
    header {
      background-color: #00695c;
      color: #fff;
      padding: 20px;
      text-align: center;
      position: relative;
    }
    .toggle-btn {
      position: absolute;
      top: 15px;
      right: 15px;
      background: #004d40;
      color: white;
      border: none;
      padding: 10px 15px;
      border-radius: 5px;
      cursor: pointer;
    }
    .profile {
      text-align: center;
      padding: 20px;
    }
    .profile img {
      width: 160px;
      border-radius: 50%;
      border: 4px solid #009688;
    }
    section {
      max-width: 900px;
      margin: auto;
      background: #ffffff;
      padding: 20px;
      margin-bottom: 20px;
      border-radius: 10px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }
    h3 {
      border-bottom: 2px solid #009688;
      padding-bottom: 5px;
      color: #009688;
    }
    table {
      width: 100%;
      border-collapse: collapse;
      margin-top: 15px;
    }
    th, td {
      padding: 10px;
      border-bottom: 1px solid #ddd;
    }
    .timeline-item {
      margin: 10px 0;
      padding: 10px;
      background-color: #e0f2f1;
      border-left: 5px solid #00796b;
    }
    iframe {
      width: 100%;
      height: 300px;
      border: none;
      border-radius: 8px;
    }
    .counter {
      font-size: 18px;
      text-align: center;
      margin-top: 10px;
      color: #444;
    }
    footer {
      background: #ccc;
      text-align: center;
      padding: 10px;
      font-size: 14px;
    }
  </style>
</head>
<body>

  <header>
    <h1 id="title">সাকিব আল হাসান</h1>
    <p id="subtitle">বাংলাদেশ ক্রিকেটের কিংবদন্তি - A to Z ইতিহাস</p>
    <button class="toggle-btn" onclick="toggleLanguage()">ENGLISH</button>
  </header>

  <section class="profile">
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d4/Shakib_Al_Hasan_%28cropped%29.jpg/330px-Shakib_Al_Hasan_%28cropped%29.jpg" alt="Shakib Al Hasan">
    <h2 id="name">সাকিব আল হাসান</h2>
    <p id="birth"><strong>জন্ম:</strong> ২৪ মার্চ ১৯৮৭, মাগুরা</p>
    <p id="role"><strong>ভূমিকা:</strong> অলরাউন্ডার (বাম-হাতি ব্যাটসম্যান, বাম-হাতি স্পিনার)</p>
  </section>

  <section>
    <h3 id="stat_title">সংক্ষিপ্ত পরিসংখ্যান</h3>
    <table>
      <thead>
        <tr>
          <th id="format">ফরম্যাট</th>
          <th id="match">ম্যাচ</th>
          <th id="run">রান</th>
          <th id="wicket">উইকেট</th>
        </tr>
      </thead>
      <tbody>
        <tr><td>টেস্ট</td><td>৬৬</td><td>৪৪৫৪</td><td>২৩৩</td></tr>
        <tr><td>ওডিআই</td><td>২৪৭</td><td>৭৩৮৪</td><td>৩১৭</td></tr>
        <tr><td>টি-২০</td><td>১২২</td><td>২৩৮২</td><td>১৪০</td></tr>
      </tbody>
    </table>
  </section>

  <section>
    <h3 id="history_title">ঐতিহাসিক অর্জনসমূহ</h3>
    <div id="timeline"></div>
  </section>

  <section>
    <h3 id="video_title">হাইলাইটস ভিডিও</h3>
    <iframe src="https://www.youtube.com/embed/rVtx1cXbfyU" allowfullscreen></iframe>
  </section>

  <section>
    <h3>🔥 ভিজিটর কাউন্ট</h3>
    <p class="counter" id="visitorCount">আপনি এই পেজটি <span id="count">1</span> বার দেখেছেন।</p>
  </section>

  <footer>
    &copy; ২০২৫ | SF.com | তৈরি করেছেন Sharea Sobuj
  </footer>

  <script>
    // ঐতিহাসিক তথ্য
    const timelineData = [
      { year: 2006, event: "বাংলাদেশের হয়ে আন্তর্জাতিক ক্রিকেটে অভিষেক" },
      { year: 2009, event: "বিশ্বের সেরা অলরাউন্ডার হন আইসিসি র‍্যাঙ্কিংয়ে" },
      { year: 2011, event: "বিশ্বকাপ ২০১১ অধিনায়ক হিসেবে অংশগ্রহণ" },
      { year: 2019, event: "বিশ্বকাপে একমাত্র খেলোয়াড় হিসেবে ৬০০+ রান ও ১০+ উইকেট" },
      { year: 2021, event: "সব ফরম্যাটে ১০০০+ রান ও ১০০+ উইকেট" },
      { year: 2024, event: "৫০০০+ রান ও ৩০০+ উইকেট নিয়ে ইতিহাস গড়েন" }
    ];

    const container = document.getElementById("timeline");
    timelineData.forEach(item => {
      const div = document.createElement("div");
      div.className = "timeline-item";
      div.innerHTML = `<strong>${item.year}:</strong> ${item.event}`;
      container.appendChild(div);
    });

    // ভাষা পরিবর্তন
    let isBangla = true;
    function toggleLanguage() {
      isBangla = !isBangla;
      document.querySelector(".toggle-btn").innerText = isBangla ? "ENGLISH" : "বাংলা";

      document.getElementById("title").innerText = isBangla ? "সাকিব আল হাসান" : "Shakib Al Hasan";
      document.getElementById("subtitle").innerText = isBangla ? "বাংলাদেশ ক্রিকেটের কিংবদন্তি - A to Z ইতিহাস" : "Bangladesh Cricket Legend - A to Z History";
      document.getElementById("name").innerText = isBangla ? "সাকিব আল হাসান" : "Shakib Al Hasan";
      document.getElementById("birth").innerHTML = isBangla ? "<strong>জন্ম:</strong> ২৪ মার্চ ১৯৮৭, মাগুরা" : "<strong>Born:</strong> March 24, 1987, Magura";
      document.getElementById("role").innerHTML = isBangla ? "<strong>ভূমিকা:</strong> অলরাউন্ডার (বাম-হাতি ব্যাটসম্যান, বাম-হাতি স্পিনার)" : "<strong>Role:</strong> All-rounder (Left-handed batsman, Left-arm spinner)";
      document.getElementById("stat_title").innerText = isBangla ? "সংক্ষিপ্ত পরিসংখ্যান" : "Career Statistics";
      document.getElementById("format").innerText = isBangla ? "ফরম্যাট" : "Format";
      document.getElementById("match").innerText = isBangla ? "ম্যাচ" : "Match";
      document.getElementById("run").innerText = isBangla ? "রান" : "Runs";
      document.getElementById("wicket").innerText = isBangla ? "উইকেট" : "Wickets";
      document.getElementById("history_title").innerText = isBangla ? "ঐতিহাসিক অর্জনসমূহ" : "Historical Achievements";
      document.getElementById("video_title").innerText = isBangla ? "হাইলাইটস ভিডিও" : "Highlights Video";
    }

    // লোকাল ভিজিটর কাউন্টার (LocalStorage)
    let count = localStorage.getItem("visitCount") || 0;
    count++;
    localStorage.setItem("visitCount", count);
    document.getElementById("count").innerText = count;
  </script>

</body>
</html>
