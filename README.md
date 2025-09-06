# Ch-huy-n
Yêu chị
<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>Lời tỏ tình 💌</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: "Segoe UI", sans-serif;
      background: linear-gradient(135deg, #ffe5ec, #fff9f0);
    }
    .card {
      background: #fff;
      padding: 30px 40px;
      border-radius: 16px;
      box-shadow: 0 10px 30px rgba(0,0,0,.1);
      text-align: center;
      max-width: 400px;
    }
    h1 {
      color: #ff4d6d;
    }
    p {
      font-size: 18px;
      margin: 16px 0 24px;
    }
    button {
      margin: 6px;
      padding: 10px 20px;
      border-radius: 999px;
      border: none;
      font-size: 16px;
      cursor: pointer;
      transition: 0.2s;
    }
    #yesBtn {
      background: #ff4d6d;
      color: white;
      font-weight: bold;
    }
    #noBtn {
      background: white;
      border: 2px solid #ff4d6d;
      color: #ff4d6d;
    }
    #final {
      display: none;
      margin-top: 20px;
      animation: fadeIn 0.8s ease forwards;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(10px); }
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body>
  <div class="card">
    <h1>Xin chào 💖</h1>
    <p id="ques">Cậu có đồng ý làm người yêu tớ không?</p>
    <div>
      <button id="yesBtn">Có 🥰</button>
      <button id="noBtn">Không 🙈</button>
    </div>
    <div id="final">
      <h2>Yay! 💘</h2>
      <p>Từ hôm nay tớ hứa sẽ làm cậu cười mỗi ngày!</p>
    </div>
  </div>

  <script>
    const yes = document.getElementById("yesBtn");
    const no = document.getElementById("noBtn");
    const final = document.getElementById("final");
    const ques = document.getElementById("ques");

    // Nút "Không" chạy trốn
    no.addEventListener("mouseenter", () => {
      const x = (Math.random() * 120 - 60);
      const y = (Math.random() * 60 - 30);
      no.style.transform = `translate(${x}px, ${y}px)`;
    });

    // Nút "Có" hiện thông điệp
    yes.addEventListener("click", () => {
      final.style.display = "block";
      ques.style.display = "none";
      no.style.display = "none";
      yes.style.display = "none";
    });
  </script>
</body>
</html>
