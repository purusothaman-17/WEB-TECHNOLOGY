# WEB-TECHNOLOGY
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Animated CSS Box Model</title>

  <style>
    body {
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      font-family: Arial, sans-serif;
      background: linear-gradient(270deg, #0f2027, #203a43, #2c5364);
      background-size: 600% 600%;
      animation: bgMove 10s ease infinite;
    }

    /* MARGIN */
    .margin {
      background: rgba(255, 100, 100, 0.15);
      padding: 30px;
      animation: pulse 3s infinite;
    }

    /* BORDER */
    .border {
      background: rgba(100, 150, 255, 0.2);
      padding: 20px;
      border: 3px solid #6fa8ff;
    }

    /* PADDING */
    .padding {
      background: rgba(100, 255, 150, 0.2);
      padding: 20px;
    }

    /* CONTENT */
    .content {
      background: #111;
      color: white;
      padding: 20px;
      width: 260px;
      text-align: center;
      border-radius: 6px;
      animation: glow 2.5s infinite alternate;
    }

    h3 {
      margin: 5px 0;
      letter-spacing: 1px;
    }

    p {
      font-size: 14px;
      color: #ccc;
    }

    /* ANIMATIONS */
    @keyframes bgMove {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    @keyframes pulse {
      0% { box-shadow: 0 0 0 rgba(255,100,100,0.2); }
      50% { box-shadow: 0 0 25px rgba(255,100,100,0.4); }
      100% { box-shadow: 0 0 0 rgba(255,100,100,0.2); }
    }

    @keyframes glow {
      from { box-shadow: 0 0 10px #00ffd5; }
      to { box-shadow: 0 0 25px #00ffd5; }
    }
  </style>
</head>

<body>

  <div class="margin">
    <div class="border">
      <div class="padding">
        <div class="content">
          <h3>CSS BOX MODEL</h3>
          <p>
            Content is surrounded by padding, border, and margin.
            Each layer is visually animated.
          </p>
        </div>
      </div>
    </div>
  </div>

</body>
</html>
