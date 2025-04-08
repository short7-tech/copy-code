<!DOCTYPE html>
<html>
<head>
  <title>Salin Angka</title>
  <style>
    .copy-box {
      display: inline-block;
      padding: 20px 40px;
      border: 1px solid #ccc;
      font-family: Arial, sans-serif;
    }

    .copy-text {
      color: green;
      font-size: 28px;
      font-weight: bold;
      cursor: pointer;
      user-select: none;
    }

    .copy-text.blink {
      animation: blinkFast 0.2s ease-in-out 3;
    }

    @keyframes blinkFast {
      0% { color: green; }
      50% { color: white; }
      100% { color: green; }
    }
  </style>
</head>
<body>

<center>
  <div class="copy-box">
    <span class="copy-text" onclick="copyToClipboard(this, '258159')">258159</span>
  </div>
</center>

<script>
  function copyToClipboard(el, text) {
    navigator.clipboard.writeText(text).then(() => {
      el.classList.add('blink');
      setTimeout(() => {
        el.classList.remove('blink');
      }, 600); // durasi total blink
    });
  }
</script>

</body>
</html>
