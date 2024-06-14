<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Lato:400,700|Montserrat:900">
    <title>Countdown Widget</title>
    <style>
        body {
            background-color: #add8e6; /* 하늘색 배경 */
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        #timer {
            color: #00462A;
            text-align: center;
            text-transform: uppercase;
            font-family: 'Lato', sans-serif;
            letter-spacing: 5px;
        }

        .days, .hours {
            display: inline-block;
            padding: 20px;
            width: 100px;
            border-radius: 5px;
            background: #276FBF; /* 파랑색 */
        }

        .numbers {
            font-family: 'Montserrat', sans-serif;
            color:  #00462A;
            font-size: 4em;
            text-align: center;
        }
    </style>
</head>
<body>
    <div id="timer">
        <div class="days"> 
            <div id="days" class="numbers "> </div>days</div> 
        <div class="hours"> 
            <div id="hours" class="numbers"> </div>hours</div> 
    </div>
</body>
<script>
    const myDate = new Date('June 26, 2025 00:00:00');

    // countdown
    let timer = setInterval(function() {
        // get today's date
        const today = new Date().getTime();
        // get the difference
        const diff = myDate - today;
        // math
        let days = Math.floor(diff / (1000 * 60 * 60 * 24));
        let hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        // display
        document.getElementById("days").innerHTML = days;
        document.getElementById("hours").innerHTML = hours;
    }, 1);
</script>
</html>
