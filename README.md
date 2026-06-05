<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>I'm Sorry, Najwa ❤️</title>

<style>
body{
    margin:0;
    font-family:'Segoe UI',sans-serif;
    background:linear-gradient(135deg,#ffb6c1,#ffd6e8);
    overflow:hidden;
    text-align:center;
}

.container{
    position:relative;
    z-index:2;
    margin-top:80px;
}

h1{
    color:white;
    font-size:50px;
}

p{
    color:white;
    font-size:20px;
    width:80%;
    margin:auto;
    line-height:1.8;
}

button{
    padding:15px 30px;
    border:none;
    border-radius:30px;
    font-size:18px;
    cursor:pointer;
    margin:15px;
    transition:.3s;
}

#yes{
    background:white;
    color:#ff4d88;
}

#no{
    background:#ff4d88;
    color:white;
    position:absolute;
}

#letterBtn{
    background:#fff;
    color:#ff4d88;
}

.popup{
    display:none;
    position:fixed;
    top:50%;
    left:50%;
    transform:translate(-50%,-50%);
    background:white;
    width:80%;
    max-width:500px;
    padding:30px;
    border-radius:20px;
    box-shadow:0 10px 30px rgba(0,0,0,.3);
    z-index:10;
}

.close{
    background:#ff4d88;
    color:white;
}

.heart{
    position:absolute;
    color:white;
    animation:float 6s linear infinite;
}

@keyframes float{
    0%{
        transform:translateY(100vh);
        opacity:1;
    }
    100%{
        transform:translateY(-100px);
        opacity:0;
    }
}
</style>
</head>
<body>

<div class="container">
    <h1>I'm Sorry, Najwa ❤️</h1>

    <p>
        I know I may have hurt you, and I truly regret it.
        You mean so much to me, and the last thing I ever want
        is to make you sad. Thank you for giving me a chance
        to love you, and I hope you'll let me make things right.
        🥺💕
    </p>

    <br>

    <button id="yes" onclick="forgive()">Yes, I forgive you ❤️</button>
    <button id="no">No 😤</button>

    <br><br>

    <button id="letterBtn" onclick="showLetter()">
        💌 Open Secret Letter
    </button>
</div>

<div class="popup" id="popup">
    <h2>To My Beautiful Najwa ❤️</h2>

    <p style="color:#444;">
        Thank you for being patient with me.
        I know I'm not perfect, but my feelings for you are genuine.
        No matter what happens, I will always appreciate every smile,
        every laugh, and every moment we've shared together.
        I hope we can continue making beautiful memories together.
        I love you so much. ❤️
    </p>

    <button class="close" onclick="closeLetter()">Close</button>
</div>

<script>

// Moving No button
let noBtn = document.getElementById("no");

noBtn.addEventListener("mouseover", function(){
    let x = Math.random()*(window.innerWidth-150);
    let y = Math.random()*(window.innerHeight-100);

    noBtn.style.left = x + "px";
    noBtn.style.top = y + "px";
});

function forgive(){
    document.body.innerHTML = `
    <div style="margin-top:150px;">
        <h1 style="color:white;font-size:60px;">
        YAYYY!! ❤️🥹
        </h1>

        <h2 style="color:white;">
        Thank you for forgiving me, Najwa 💕
        </h2>

        <p style="color:white;font-size:22px;">
        I promise to cherish you and do better every day.
        Forever my favorite person ❤️
        </p>
    </div>`;
}

function showLetter(){
    document.getElementById("popup").style.display="block";
}

function closeLetter(){
    document.getElementById("popup").style.display="none";
}

// Floating hearts
setInterval(()=>{
    let heart=document.createElement("div");
    heart.classList.add("heart");
    heart.innerHTML="❤";
    heart.style.left=Math.random()*100+"vw";
    heart.style.fontSize=(20+Math.random()*30)+"px";
    document.body.appendChild(heart);

    setTimeout(()=>{
        heart.remove();
    },6000);

},300);

</script>

</body>
</html>
