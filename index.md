<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
p {
  text-align: center;
  font-size: 60px;
  margin-top: 0px;
}
</style>
</head>
<body>

<p id="Shutong_quarantine"></p>

<script>
// Set the date we're counting down to
var countDownDate = new Date("Dec 28, 2020 00:00:00 GMT+08:00").getTime();

// Update the count down every 1 second
var x = setInterval(function() {

  // Get today's date and time
  var now = new Date().getTime();
    
  // Find the distance between now and the count down date
  var distance = countDownDate - now;
    
  // Time calculations for days, hours, minutes and seconds
  var days = Math.floor(distance / (1000 * 60 * 60 * 24));
  var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
  var seconds = Math.floor((distance % (1000 * 60)) / 1000);
    
  // Output the result in an element with id="demo"
  document.getElementById("Shutong_quarantine").innerHTML = 
  " ♫.(◕∠◕).♫ ♫.(◕∠◕).♫ " + "<br />"  + "距離 Dec 28th 姝彤出閘剩餘" + "<br />"  + days + "d " + hours + "h "
  + minutes + "m " + seconds + "s " + "<br />"  + "請村民到指定場合避難" + "<br />" + "♫.(◕∠◕).♫ ♫.(◕∠◕).♫"
    
  // If the count down is over, write some text 
  if (distance < 0) {
    clearInterval(x);
    document.getElementById("Shutong_quarantine").innerHTML = "٩(●˙▿˙●)۶…⋆ฺ٩(●˙▿˙●)۶…⋆ " + "<br />" + "恭喜姝彤，賀喜姝彤" + "<br />" + " ฺ٩(●˙▿˙●)۶…⋆ฺ٩(●˙▿˙●)۶…⋆ฺ";
  }
}, 1000);
</script>

</body>
</html>
