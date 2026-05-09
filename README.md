<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Addlin Akinyi Portfolio</title>

<style>

*{
  margin:0;
  padding:0;
  box-sizing:border-box;
  font-family:Arial, sans-serif;
  scroll-behavior:smooth;
}

body{
  background:#f4f7fb;
  color:#111;
}

/* HEADER */

header{
  background:linear-gradient(135deg,#6C63FF,#8B5CF6);
  color:white;
  padding:20px;
  position:sticky;
  top:0;
}

nav{
  display:flex;
  justify-content:center;
  gap:20px;
  flex-wrap:wrap;
}

nav a{
  color:white;
  text-decoration:none;
  font-weight:bold;
}

.hero{
  text-align:center;
  padding:60px 20px;
}

.hero h1{
  font-size:40px;
}

.hero p{
  margin-top:10px;
  opacity:0.9;
}

/* SECTIONS */

section{
  padding:60px 10%;
}

.card{
  background:white;
  padding:20px;
  border-radius:12px;
  box-shadow:0 5px 15px rgba(0,0,0,0.08);
  margin-top:20px;
}

/* PROJECTS */

.projects{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
  gap:15px;
}

.project{
  background:#eef2ff;
  padding:15px;
  border-radius:10px;
}

/* CONTACT */

input, textarea{
  width:100%;
  padding:12px;
  margin-top:8px;
  margin-bottom:15px;
  border:1px solid #ccc;
  border-radius:8px;
}

button{
  padding:12px 18px;
  background:#6C63FF;
  color:white;
  border:none;
  border-radius:8px;
  cursor:pointer;
}

button:hover{
  opacity:0.9;
}

/* FOOTER */

footer{
  text-align:center;
  padding:20px;
  background:#111827;
  color:white;
  margin-top:40px;
}

/* MESSAGE BOX */

.msg{
  margin-top:10px;
  font-weight:bold;
}

.success{ color:green; }
.error{ color:red; }

</style>
</head>

<body>

<header>

  <h2 style="text-align:center;">Addlin Akinyi's Portfolio</h2>

  <nav>
    <a href="#home">Home</a>
    <a href="#about">About</a>
    <a href="#projects">Project</a>
    <a href="#contact">Contact</a>
  </nav>

</header>

<!-- HOME -->

<section id="home" class="hero">

  <h1>Welcome to My Portfolio</h1>
  <p>I am Addlin Akinyi — Passionate Web Developer & Designer</p>

</section>

<!-- ABOUT -->

<section id="about">

  <h2>About Me</h2>

  <div class="card">

    <p>
      I am a creative developer passionate about building modern, responsive,
      and user-friendly websites. I enjoy turning ideas into real digital products.
    </p>

  </div>

</section>

<!-- PROJECTS -->

<section id="projects">

  <h2>Projects</h2>

  <div class="projects">

    <div class="project">
      <h3>Portfolio Website</h3>
      <p>Modern responsive personal website.</p>
    </div>

    <div class="project">
      <h3>Community Hub</h3>
      <p>Social platform with posts and chat system.</p>
    </div>

    <div class="project">
      <h3>Todo App</h3>
      <p>Task manager with local storage.</p>
    </div>

  </div>

</section>

<!-- CONTACT -->

<section id="contact">

  <h2>Contact Me</h2>

  <div class="card">

    <p>Feel free to reach out using the form below!</p>

    <label>Name:</label>
    <input type="text" id="name" placeholder="Enter your name">

    <label>Email:</label>
    <input type="email" id="email" placeholder="email@example.com">

    <label>Message:</label>
    <textarea id="message" placeholder="Your message (at least 10 characters)"></textarea>

    <button onclick="submitForm()">Submit</button>

    <div id="msg" class="msg"></div>

  </div>

</section>

<!-- FOOTER -->

<footer>
  © 2026 Addlin Akinyi
</footer>

<script>

function submitForm(){

  let name = document.getElementById("name").value;
  let email = document.getElementById("email").value;
  let message = document.getElementById("message").value;
  let msg = document.getElementById("msg");

  if(name === "" || email === "" || message === ""){

    msg.innerText = "❌ Please fill all fields";
    msg.className = "msg error";
    return;

  }

  if(message.length < 10){

    msg.innerText = "❌ Message must be at least 10 characters";
    msg.className = "msg error";
    return;

  }

  msg.innerText = "✅ Message sent successfully!";
  msg.className = "msg success";

  document.getElementById("name").value = "";
  document.getElementById("email").value = "";
  document.getElementById("message").value = "";

}

</script>

</body>
</html>
