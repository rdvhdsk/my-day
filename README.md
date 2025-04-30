<!DOCTYPE html>
<html lang="zh-Hant">
<head>
<meta charset="UTF-8">
<title>《遺忘月台的米香記憶》活動簡章</title>
<style>
body {
font-family: "Noto Sans TC", sans-serif;
line-height: 1.8;
margin: 0;
padding: 0;
background-color: #f9f6f2;
color: #333;
}

.container {
max-width: 800px;
margin: 40px auto;
padding: 30px;
background-color: #fff;
box-shadow: 0 0 10px rgba(0,0,0,0.1);
border-radius: 10px;
}

.banner img {
width: 100%;
border-radius: 8px;
margin-bottom: 20px;
}

h1 {
text-align: center;
font-size: 28px;
margin-bottom: 20px;
color: #7a5313;
}

.content p {
margin-bottom: 20px;
}

.time-info {
background-color: #f4e4ca;
padding: 15px;
border-left: 5px solid #c08b45;
margin-bottom: 30px;
border-radius: 5px;
}

.btn {
display: block;
width: 200px;
margin: 0 auto;
background-color: #d28800;
color: #fff;
text-align: center;
padding: 15px;
border-radius: 8px;
text-decoration: none;
font-size: 16px;
}

.btn:hover {
background-color: #b06e00;
}
</style>
</head>
<body>
<div class="container">
<h1>《遺忘月台的米香記憶》活動簡章</h1>

<div class="banner">
<img src="圖.png" alt="活動形象圖"> <!-- ← 請替換為你的圖片檔名 -->
</div>

<div class="content">
<p>在被時間遺落的 0 蛋月台，我們拾起一段段屬於土地的記憶，也用創意翻轉對「米」的想像。</p>

<p><strong>《遺忘月台的米香記憶》</strong>是一場融合懷舊場景與創新米食的體驗活動。透過車站的老空間，我們邀請你走進時光縫隙，品嚐傳統與創意的交會。</p>

<p>這裡有來自長輩記憶中的古早味米點心，也有令人驚喜的米料理新吃法——米做的甜品，讓你重新認識米的可能性。</p>

<p>可以動手體驗米食創作，並寫下一句話留給未來的自己，將它封存進時光膠囊，待下一次重返月台。</p>

<p>這不只是味蕾的探索之旅，更是一次關於記憶、創意與土地的對話。</p>
</div>

<div class="time-info">
<strong>活動時間：</strong><br>
每逢例假日與國定假日<br>
上午場 11:00｜下午場 13:30<br>
每場限額 20 人，額滿為止。
</div>

<a class="btn" href="報名表.html" target="_blank">我要報名</a>

</div>
</body>
</html>
<!DOCTYPE html>
<html lang="zh-Hant">
<head>
  <meta charset="UTF-8">
  <title>《遺忘月台的米香記憶》活動報名</title>
  <style>
    body {
      margin: 0;
      font-family: "Noto Sans TC", sans-serif;
      background-color: #f9f6f2;
    }

    .container {
      max-width: 500px;
      margin: 80px auto;
      padding: 30px;
      background-color: rgba(255, 255, 255, 0.95);
      border-radius: 10px;
      box-shadow: 0 0 15px rgba(0,0,0,0.1);
    }

    h2 {
      text-align: center;
      margin-bottom: 20px;
      color: #7a5313;
    }

    p {
      font-size: 14px;
      color: #333;
      text-align: center;
      margin-bottom: 30px;
    }

    label {
      display: block;
      margin: 10px 0 5px;
    }

    input, select {
      width: 100%;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
      margin-bottom: 15px;
    }

    button {
      background-color: #d28800;
      color: white;
      padding: 12px;
      width: 100%;
      border: none;
      border-radius: 5px;
      font-size: 16px;
      cursor: pointer;
    }

    button:hover {
      background-color: #b06e00;
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>《遺忘月台的米香記憶》活動報名</h2>
    <p>僅限例假日與國定假日<br>上午 11:00／下午 1:30<br>每場最多 20 人，額滿為止</p>

    <form>
      <label for="name">姓名</label>
      <input type="text" id="name" name="name" required>

      <label for="email">Email</label>
      <input type="email" id="email" name="email" required>

      <label for="date">選擇報名日期</label>
      <input type="date" id="date" name="date" required>

      <label for="time">選擇場次</label>
      <select id="time" name="time" required>
        <option value="">請選擇</option>
        <option value="11:00">上午 11:00</option>
        <option value="13:30">下午 1:30</option>
      </select>

      <button type="submit">送出報名</button>
    </form>
  </div>

  <script>
    // 限制日期只能選擇假日（六日）和指定國定假日
    const dateInput = document.getElementById("date");

    const nationalHolidays = [
      "2025-05-01", // 勞動節
      "2025-06-09", // 端午節
      "2025-09-17", // 中秋節
      "2025-10-10"  // 國慶日
    ];

    dateInput.addEventListener("input", function () {
      const selected = new Date(this.value);
      const day = selected.getDay(); // 0: Sunday, 6: Saturday

      const formatted = this.value;
      const isHoliday = nationalHolidays.includes(formatted);
      const isWeekend = day === 0 || day === 6;

      if (!isWeekend && !isHoliday) {
        alert("僅限報名例假日或國定假日！");
        this.value = ""; // 清除不合法日期
      }
    });
  </script>
</body>
</html>
