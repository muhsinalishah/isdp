<!DOCTYPE html>
<html>
<head>
  <title>Counter</title>
  <style>
    /* CSS code to style the counter */
    #counter {
      font-size: 24px;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <p id="counter">0</p>
  <script>
    // JavaScript code to increment the counter
    let counter = document.getElementById("counter");
    let count = localStorage.getItem("count") || 0;
    count++;
    localStorage.setItem("count", count);
    counter.textContent = count;
  </script>
</body>
</html>
