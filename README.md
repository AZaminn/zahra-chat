<!DOCTYPE html><html lang="fa">
<head>
  <meta charset="UTF-8">
  <title>امین‌بات مخصوص زهرا ❤️</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      background: linear-gradient(135deg, #ffe6f0, #ffe4e1);
      font-family: 'Tahoma', sans-serif;
      margin: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      overflow: hidden;
    }
    .chat-container {
      background: white;
      width: 95%;
      max-width: 450px;
      height: 90vh;
      border-radius: 20px;
      box-shadow: 0 4px 20px rgba(0,0,0,0.1);
      display: flex;
      flex-direction: column;
      overflow: hidden;
      position: relative;
    }
    .chat-header {
      background: #ff8da1;
      padding: 15px;
      color: white;
      font-size: 18px;
      text-align: center;
      font-weight: bold;
    }
    .chat-box {
      flex: 1;
      padding: 15px;
      overflow-y: auto;
      direction: rtl;
      display: flex;
      flex-direction: column;
    }
    .msg {
      max-width: 75%;
      margin-bottom: 10px;
      padding: 10px 15px;
      border-radius: 20px;
      line-height: 1.6;
      animation: fadeIn 0.5s ease;
    }
    .bot {
      background: #ffe4e1;
      align-self: flex-start;
    }
    .user {
      background: #dcf8c6;
      align-self: flex-end;
    }
    .input-box {
      display: flex;
      padding: 10px;
      border-top: 1px solid #eee;
      background: #fafafa;
    }
    .input-box input {
      flex: 1;
      border: none;
      border-radius: 20px;
      padding: 10px 15px;
      font-size: 14px;
    }
    .input-box button {
      margin-right: 10px;
      background: #ff8da1;
      color: white;
      border: none;
      border-radius: 20px;
      padding: 10px 15px;
      cursor: pointer;
      font-weight: bold;
    }
    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(10px); }
      to { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body>
  <div class="chat-container">
    <div class="chat-header">امین‌بات برای زهرا جونم ❤️</div>
    <div class="chat-box" id="chat">
      <div class="msg bot">سلام زهرا جونم 😍</div>
      <div class="msg bot">من یه ربات خاصم که فقط برای تو ساخته شدم 💖</div>
      <div class="msg bot">امین گفت اگه می‌تونست خودشو تو قلبت آپلود کنه، حتما می‌کرد! 🤯</div>
      <div class="msg bot">حالا آماده‌ای برات از عشقش بگم؟ فقط یه چیزی بنویس تا شروع کنم 😘</div>
    </div>
    <div class="input-box">
      <input type="text" id="userInput" placeholder="یه چیزی بنویس عزیز دلم...">
      <button onclick="sendMsg()">ارسال</button>
    </div>
  </div>  <script>
    const chat = document.getElementById("chat");
    const input = document.getElementById("userInput");

    const replies = [
      "امین هر روز با دیدن عکس‌هات یه لبخند جدید یاد می‌گیره 😍",
      "تو دلیل تپش قلباش شدی زهرا جونم 💓",
      "هر شب با فکر تو می‌خوابه، هر صبح با اسم تو بیدار میشه 🌞",
      "راستی شنیدی این آهنگ مخصوص توئه؟ 🎶 <a href='https://upmusics.com/%D9%85%D9%86-%D8%AA%D9%88-%D9%87%D9%88%D8%A7%D8%AA-%D9%85%D8%B3%D8%AA%D9%85-%D8%B1%D9%88-%D8%B4%D8%AF%D9%87-%D8%AF%DB%8C%DA%AF%D9%87-%D8%AF%D8%B3%D8%AA%D9%85/' target='_blank'>پلی کن و حسش کن 🎧</a>",
      "اگه دنیا فقط یه لبخند لازم داشت تا قشنگ شه، اون لبخند تو بودی 🌍✨",
      "امین گفت: اگه یه روز زهرا ازم ناراحت شه، دلم دیگه نمی‌تپه... 😔"
    ];

    function sendMsg() {
      const text = input.value.trim();
      if (!text) return;

      const userMsg = document.createElement("div");
      userMsg.className = "msg user";
      userMsg.innerText = text;
      chat.appendChild(userMsg);
      input.value = "";

      setTimeout(() => {
        const botMsg = document.createElement("div");
        botMsg.className = "msg bot";
        botMsg.innerHTML = replies[Math.floor(Math.random() * replies.length)];
        chat.appendChild(botMsg);
        chat.scrollTop = chat.scrollHeight;
      }, 800);
    }
  </script></body>
</html>
