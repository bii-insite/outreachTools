<style>
html, body { min-height: 100%; }
#wheel {
  animation-name: rotation;
  animation-duration: 0s;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
}

  #textbox {
    display: none;
    border: 10px solid gold;
    border-radius: 100px;
    width: 80%;
    margin-left: 10%;
  }

@keyframes rotation {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(1080deg);
  }
}

  #formm {
    display:grid;
    justify-content:center;
  }

  #text {
    text-align:center;
    font-size:35px;
  }

  section {
    background-color: palegoldenrod;
  }
  
</style>
<div style="display:grid;grid-template-columns:1fr 1fr;">
<div id="colleft" style="display:grid;align-content:center;">
<div style="padding-top:10px;">
  <h1 style="text-align:center;font-size:51px;">Spin the wheel!</h1>
  <p style="text-align:center;font-size:40px;">Sign up for our mailing list to spin the wheel and see what prize you get</p>
</div>

<iframe name="dummyframe" id="dummyframe" style="display: none;"></iframe>

<form method="POST" action="https://script.google.com/macros/s/AKfycbwDJVbqGlpgprnTWN5g1fKATCazyaiYcHozVXeap1u6P2K3flwHOyfpQmfEKI9H2gxACQ/exec" id="formm" target="dummyframe" autocomplete="off">
  <label for="em" style="font-size:35px;">Email:</label>
  <input style="font-size:35px;" type="email" id="em" name="Email" placeholder="me@fun.com" required>
  <br>
  <label style="font-size:35px;" for="nam">Name:</label>
  <input style="font-size:35px;" type="text" id="nam" name="Name" placeholder="John Doe" required>
  <br>
  <button style="font-size:35px;" type="submit">Send</button>
</form> 
<br>
</div>
<div id="colright">
<div style="display:grid;justify-content:center;">
  <img src="{{site.baseurl}}/images/wheel.png" id="wheel" style="height:460px;margin-top:20px;">
  <div id="textbox"><p id="text"> blank </p> </div>
</div>
</div>
</div>
<script>
    const image = document.getElementById('wheel');
    const form = document.getElementById('formm');
    const text = document.getElementById('text');
    const textbox = document.getElementById('textbox');
    form.addEventListener('submit', () => {
    image.style.animationDuration = "2s";
    var rando;
    rando = Math.random();
    setTimeout(function() {
    if (rando > 0 && rando <= 0.1)
    {
      image.src = "{{site.baseurl}}/images/notepad.png";
      image.style.animationDuration = "0s";
      text.innerHTML = "A notepad!";
      textbox.style.display="block";
    } else if (rando > 0.1 && rando <= 0.2)
    {
      image.src = "{{site.baseurl}}/images/lanyard.png";
      image.style.animationDuration = "0s";
      text.innerHTML = "A lanyard!";
      textbox.style.display="block";
    } 
    else if (rando > 0.2 && rando <= 0.3)
    {
      image.src = "{{site.baseurl}}/images/sticker.png";
      image.style.animationDuration = "0s";
      text.innerHTML = "A sticker!";
      textbox.style.display="block";
    } 
    else if (rando > 0.3 && rando <= 0.4)
    {
      image.src = "{{site.baseurl}}/images/notebook.png";
      image.style.animationDuration = "0s";
      text.innerHTML = "A notebook!";
      textbox.style.display="block";
    } 
    else if (rando > 0.4 && rando <= 0.5)
    {
      image.src = "{{site.baseurl}}/images/waterbottle.png";
      image.style.animationDuration = "0s";
      text.innerHTML = "A water bottle!";
      textbox.style.display="block";
    } 
    else if (rando > 0.5 && rando <= 0.6)
    {
      image.src = "{{site.baseurl}}/images/straw.png";
      image.style.animationDuration = "0s";
      text.innerHTML = "A straw!";
      textbox.style.display="block";
    } 
    else if (rando > 0.6 && rando <= 1)
    {
      image.src = "{{site.baseurl}}/images/bar.png";
      image.style.animationDuration = "0s";
      text.innerHTML = "A Kind Bar!";
      textbox.style.display="block";
    } 
}, 2000);
   setTimeout(function() {
   image.src = "{{site.baseurl}}/images/wheel.png";
   document.getElementById("em").value = "";
   document.getElementById("nam").value = "";
   document.getElementById("textbox").style.display = "none";
     
}, 5000);
  });
</script>
