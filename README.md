<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>はやはや応援サイト</title>

  <style>
    body {
      background-color: #111;
      color: white;
      font-family: sans-serif;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }

    .box {
      text-align: center;
    }

    h1 {
      margin-bottom: 30px;
    }

    button {
      padding: 15px 25px;
      border: none;
      border-radius: 12px;
      font-size: 18px;
      cursor: pointer;
    }

    #message {
      margin-top: 30px;
      font-size: 24px;
      min-height: 40px;
    }
  </style>
</head>

<body>

  <div class="box">
    <h1>はやはや応援システム</h1>

    <button id="button">
      押してね
    </button>

    <div id="message"></div>
  </div>

  <script>
    const button = document.getElementById("button");
    const message = document.getElementById("message");

    const messages = [
      "はやはや勉強頑張れー！",
      "ご褒美あります",
      "なにしてんの？",
      "集中しろ",
      "えらい！",
      "寝てない？",
      "監視されています"
    ];

    button.addEventListener("click", () => {

      const random =
        messages[Math.floor(Math.random() * messages.length)];

      message.innerText = random;
    });
  </script>

</body>
</html>
