<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Visitor Counter</title>
<style>
    body {
        font-family: Arial, sans-serif;
        text-align: center;
    }
    .counter {
        display: inline-block;
        padding: 10px;
        border: 2px solid black;
        font-size: 24px;
    }
</style>
</head>
<body>
    <h1>Visitor Counter</h1>
    <div class="counter" id="counter">0</div>

    <script>
        // Function to fetch current count from localStorage or initialize if not present
        function getCount() {
            let count = localStorage.getItem('visitCount');
            if (!count) {
                count = 0;
            } else {
                count = parseInt(count);
            }
            return count;
        }

        // Function to update the counter and store in localStorage
        function updateCounter() {
            let counter = document.getElementById('counter');
            let count = getCount();
            count++;
            counter.textContent = count;
            localStorage.setItem('visitCount', count);
        }

        // Initialize counter on page load
        window.onload = function() {
            updateCounter();
        };
    </script>
</body>
</html>
