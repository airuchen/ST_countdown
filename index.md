<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
p {
  text-align: center;
  font-size: 30px;
  margin-top: 0px; 
  font-family: "Microsoft JhengHei", Arial, serif;
}
.base-timer {
    position: relative;
    height: 400px;
    width: 400px;
  }
.base-timer__circle {
  fill: none;
  stroke: none;
}
.base-timer__path-elapsed_0 {
  stroke-width: 7px;
  stroke: green;
}
.base-timer__path-elapsed_1 {
  stroke-width: 7px;
  stroke: yellow;
}
.base-timer__path-elapsed_2 {
  stroke-width: 7px;
  stroke: red;
}
.base-timer__label {
  position: absolute;
  width: 400px;
  height: 400px;
  top: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 35px;
}
</style>
</head>
<body>

<p id="Shutong_quarantine"></p>

<script>

// Set the date we're counting down to
var countDownDate = new Date("Dec 28, 2020 11:51:00 GMT+08:00").getTime();

// Update the count down every 1 second
var x = setInterval(function() {

  // Get today's date and time
  var now = new Date().getTime();
    
  // Find the distance between now and the count down date
  var distance = countDownDate - now;

  // Backdoor test 
  // distance = -1

    
  // Time calculations for days, hours, minutes and seconds
  var days = Math.floor(distance / (1000 * 60 * 60 * 24));
  var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
  var seconds = Math.floor((distance % (1000 * 60)) / 1000);
  function formatTimeLeft() {
    return `${days} D, ${hours} H, ${minutes} M, ${seconds} S`;
  }

  // Backdoor test 
  // days = 0;
  // hours = 0;
  // minutes = 0;
  // seconds = 0;

  if (days > 0 || hours > 5) {
    if ((seconds%10) < 5){
      document.getElementById("Shutong_quarantine").innerHTML = 
    `
      <div class="base-timer">
        <svg class="base-timer__svg" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
          <g class="base-timer__circle">
            <circle class="base-timer__path-elapsed_0" cx="50" cy="50" r="46"></circle>
          </g>
        </svg>
        <span id="base-timer-label" class="base-timer__label">
        ${"姝彤出閘倒數 <br />" + formatTimeLeft() + "<br /> ﾚ(ﾟ∀ﾟ;)ﾍ"}
        </span>
      </div>
    `
    }
    else{
      document.getElementById("Shutong_quarantine").innerHTML = 
    `
      <div class="base-timer">
        <svg class="base-timer__svg" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
          <g class="base-timer__circle">
            <circle class="base-timer__path-elapsed_1" cx="50" cy="50" r="46"></circle>
          </g>
        </svg>
        <span id="base-timer-label" class="base-timer__label">
        ${"姝彤出閘倒數 <br />" + formatTimeLeft() + "<br />　ﾍ( ﾟ∀ﾟ;)ﾉ"}
        </span>
      </div>
    `}
  }
  else if (hours <= 5 && hours >=0){
    if ((seconds%2) == 1){
      document.getElementById("Shutong_quarantine").innerHTML = 
    `
      <div class="base-timer">
        <svg class="base-timer__svg" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
          <g class="base-timer__circle">
            <circle class="base-timer__path-elapsed_0" cx="50" cy="50" r="46"></circle>
          </g>
        </svg>
        <span id="base-timer-label" class="base-timer__label">
        ${"姝彤出閘倒數 <br />" + formatTimeLeft() + "<br /> ﾚ(ﾟ∀ﾟ;)ﾍ"}
        </span>
      </div>
    `
    }
    else{
      document.getElementById("Shutong_quarantine").innerHTML = 
    `
      <div class="base-timer">
        <svg class="base-timer__svg" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
          <g class="base-timer__circle">
            <circle class="base-timer__path-elapsed_2" cx="50" cy="50" r="46"></circle>
          </g>
        </svg>
        <span id="base-timer-label" class="base-timer__label">
        ${"姝彤出閘倒數 <br />" + formatTimeLeft() + "<br />　ﾍ( ﾟ∀ﾟ;)ﾉ"}
        </span>
      </div>
    `}
  }

  // If the count down is over, write some text 
  if (distance < 0) {
    clearInterval(x);
    document.getElementById("Shutong_quarantine").innerHTML = "٩(●˙▿˙●)۶…⋆ฺ " + "<br />" + "恭喜姝彤，賀喜姝彤" + "<br />" + `<iframe src="https://giphy.com/embed/3oz8xAFtqoOUUrsh7W" width="480" height="320" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/studiosoriginals-3oz8xAFtqoOUUrsh7W">via GIPHY</a></p>` + "<br />" + `<iframe src="https://giphy.com/embed/3o6fJ1BM7R2EBRDnxK" width="480" height="234" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p><a href="https://giphy.com/gifs/congratulations-congrats-3o6fJ1BM7R2EBRDnxK">via GIPHY</a></p>`;
  }
}, 1000);
</script>

</body>
</html>
