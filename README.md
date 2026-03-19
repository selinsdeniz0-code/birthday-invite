<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width,initial-scale=1.0" />
<title>Birthday Invitation</title>
<style>
body{margin:0;display:flex;align-items:center;justify-content:center;height:100vh;background:#f5efe8;font-family:Arial}
.container{position:relative;width:320px;height:220px;cursor:pointer}
.envelope{position:absolute;width:100%;height:100%;background:#d9cfc4;border-radius:8px;box-shadow:0 10px 25px rgba(0,0,0,.15);overflow:hidden}
.flap{position:absolute;width:100%;height:100%;background:#cfc3b7;clip-path:polygon(0 0,100% 0,50% 60%);transform-origin:top;transition:transform 0.8s ease}
.letter{position:absolute;top:20px;left:10px;width:300px;height:420px;background:white;border-radius:10px;box-shadow:0 10px 20px rgba(0,0,0,.2);transform:translateY(120px);transition:transform 0.9s ease}
.open .flap{transform:rotateX(180deg)}
.open .letter{transform:translateY(-60px)}
.invite-img{width:100%;height:100%;object-fit:contain;border-radius:10px}
</style>
</head>
<body>
<div class="container" onclick="openEnvelope()">
  <div class="envelope">
    <div class="flap"></div>
  </div>
  <div class="letter">
    <img class="invite-img" src="invitation.png" alt="Invitation" />
  </div>
</div>
<script>
function openEnvelope(){
 document.querySelector('.container').classList.add('open');
}
</script>
</body>
</html>
