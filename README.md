# Analog-Clock-using-HTML-CSS-AND-JS
Here is the analog clock using html,css and javascript
#source code
HTML:
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CLOCK - USING HTML,CSS AND JS</title>
    <link rel="stylesheet"href="style.css">
    <script src="script2.js"></script>
</head>
<body>
    <div id="ClockContainer">
        <div id="hour"></div>
        <div id="minute"></div>
        <div id="second"></div>
    </div>
</body>
</html>

CSS:
#clockContainer{  
    position: relative;
    margin: auto;
    height: 40vw;
    width: 40vw; 
    background: url(clock.png) no-repeat;
    background-size: 100%;
}

#hour, #minute, #second{
    position: absolute;
    background: black;
    border-radius: 10px; 
    transform-origin: bottom;
}
#hour{
    width: 1.8%;
    height: 25%;
    top: 25%;
    left: 48.85%;
    opacity: 0.8;  
}
#minute{
    width: 1.6%;
    height: 30%;
    top: 19%;
    left: 48.9%;
    opacity: 0.8;  
}
#second{
    width: 1%;
    height: 40%;
    top: 9%;
    left: 49.25%;
    opacity: 0.8; 
    
}

JAVASCRIPT:
setInterval(() => {
    d = new Date();
    htime = d.getHours();
    mtime = d.getMinutes();
    stime = d.getSeconds();
    hrotation = 30*htime + mtime/2;
    mrotation = 6*mtime;
    srotation = 6*stime;

    hour.style.transform = `rotate(${hrotation}deg)`;
    minute.style.transform = `rotate(${mrotation}deg)`;
    second.style.transform = `rotate(${srotation}deg)`;
}, 1000);
