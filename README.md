<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Sorry Zilya 🥺</title>

<style>

body{
    margin:0;
    font-family: Arial, sans-serif;
    text-align:center;
    background: linear-gradient(135deg,#ffb6c1,#ffd1dc);
    overflow:hidden;
}

.container{
    margin-top:150px;
}

h1{
    font-size:50px;
}

button{
    padding:12px 25px;
    font-size:18px;
    margin:10px;
    border:none;
    border-radius:12px;
    cursor:pointer;
}

#yes{
    background:#7CFC00;
}

#no{
    background:#ff4d4d;
    position:absolute;
}

#question{
    display:none;
}

.heart{
    position:absolute;
    font-size:24px;
    animation: float 6s linear infinite;
}

@keyframes float{
    0%{transform:translateY(100vh);opacity:1;}
    100%{transform:translateY(-10vh);opacity:0;}
}

</style>
</head>

<body>

<div class="container">

<h1>ME SORRYYY 🥺🥺</h1>

<button onclick="showQuestion()">Click</button>

<div id="question">
    <h2>Will you please forgive me my future wifey 🥺😁🥹🙏</h2>

    <button id="yes" onclick="yesAnswer()">Yes</button>
    <button id="no">No</button>
</div>

</div>

<script>

function showQuestion(){
    document.getElementById("question").style.display="block";
}

const noBtn = document.getElementById("no");

noBtn.addEventListener("mouseover", moveButton);

function moveButton(){
    const x = Math.random() * window.innerWidth;
    const y = Math.random() * window.innerHeight;

    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";
}

function yesAnswer(){
    document.body.innerHTML = `
    <h1 style="margin-top:200px;font-size:50px;">
    YAYAYAYAY I LOVEE YOUU SOO MUCHHH ZILYAA ❤️🥹<br>
    ME NO EVER DO THAT AGAIN
    </h1>`;
}

function createHeart(){
    const heart=document.createElement("div");
    heart.className="heart";
    heart.innerHTML="❤️";

    heart.style.left=Math.random()*100+"vw";
    heart.style.fontSize=(20+Math.random()*30)+"px";

    document.body.appendChild(heart);

    setTimeout(()=>{heart.remove()},6000);
}

setInterval(createHeart,500);

</script>

</body>
</html>
