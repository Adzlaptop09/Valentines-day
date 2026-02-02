<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Be My Valentine?</title>
  <style>
    body {
      height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      font-family: Arial, sans-serif;
      background: #ffe6eb;
      text-align: center;
    }

    h1 {
      margin-bottom: 30px;
    }

    .buttons {
      position: relative;
    }

    button {
      font-size: 20px;
      padding: 15px 30px;
      margin: 10px;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      transition: all 0.3s ease;
    }

    #yes {
      background-color: #ff4d6d;
      color: white;
    }

    #no {
      background-color: #adb5bd;
      color: black;
    }
  </style>
</head>
<body>

  <h1>Will you be my Valentine? 💖</h1>

  <div class="buttons">
    <button id="yes" onclick="yesClicked()">Yes 💘</button>
    <button id="no" onclick="noClicked()">No 💔</button>
  </div>

  <script>
    let yesSize = 1;
    let noSize = 1;

    function noClicked() {
      yesSize += 0.2;
      noSize -= 0.15;

      document.getElementById("yes").style.transform = `scale(${yesSize})`;
      document.getElementById("no").style.transform = `scale(${Math.max(noSize, 0.3)})`;
    }

    function yesClicked() {
      document.body.innerHTML = "<h1>YAY!!! 💕🥰💍</h1><p>Best decision ever.</p>";
    }
  </script>

</body>
</html>
