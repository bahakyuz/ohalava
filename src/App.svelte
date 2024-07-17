<script>
  function onAdClick() {
    const overlay = document.querySelector('.overlay');
    // @ts-ignore
    overlay.style.display = 'block';
    // @ts-ignore
    overlay.style.opacity = 0;
    let opacity = 0;
    const interval = setInterval(() => {
      if (opacity < 1) {
        playSound();
        opacity += 1;
        // @ts-ignore
        overlay.style.opacity = opacity;
      } else {
        clearInterval(interval);
        alert('★ Tebrikler 1.000.000 $ kazandınız! ★');
        fadeOutOverlay(overlay);
      }
    }, 50);
  }

  function fadeOutOverlay(overlay) {
    let opacity = 1;
    const interval = setInterval(() => {
      if (opacity > 0) {
        opacity -= .5;
        // @ts-ignore
        overlay.style.opacity = opacity;
      } else {
        clearInterval(interval);
        // @ts-ignore
        overlay.style.display = 'none';
      }
    }, 50);
  }

  function playSound() {
    const audio = new Audio('./win.mp3');
    audio.play();
  }

  function randomCatVids() {
    const links = [
      "https://www.youtube.com/watch?v=qwhhy2eAbCE",
      "https://www.youtube.com/watch?v=uOjNyGqEPjY",
      "https://www.youtube.com/watch?v=rFJvPT0uGBk",
      "https://www.youtube.com/watch?v=T1UlDyOVUlo",
      "https://www.youtube.com/watch?v=R-wQ4Bs_iAE",
      "https://www.youtube.com/watch?v=7UTeNODzLjE",
      "https://www.youtube.com/watch?v=wZe2AXYaYSA",
      "https://www.youtube.com/watch?v=GliqWXL-u_8",
      "https://www.youtube.com/watch?v=BGFxf04d8Rg",
      "https://www.youtube.com/watch?v=Yilh2nNxQuQ"
    ];

    const randomIndex = Math.floor(Math.random() * links.length);

    window.open(links[randomIndex], '.blank').focus();
  }
</script>

<!-- svelte-ignore a11y-click-events-have-key-events -->
<link href="https://db.onlinewebfonts.com/c/d4269475e6f4cf16ad166d5b2e11988b?family=Golden+Age+Regular" rel="stylesheet">

<div class="overlay" style="display:none; position:fixed; top:0; left:0; width:100%; height:100%; background-color:rgba(0,0,0,0.5); z-index:999;"></div>

<div class="container">
  <!-- svelte-ignore a11y-click-events-have-key-events -->
  <!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
  <img src="../ad1.gif" alt="ad" id="ad2" on:click={onAdClick}>
  <div class="acrylic-effect">
    <div class="alt">
      <div class="profile">
        <img src="../sqrLava.png" alt="pfp">
        <h1>@ohalava</h1>
      </div>
      <div class="row">
        <div class="support">
          <h3><i class="fa-regular fa-folder-open"></i> Destekle </h3>
          <a href="https://www.papara.com/donate/OhaLava" target="_blank"><p><i class="fa-solid fa-arrow-turn-up"></i> <i class="fa-solid fa-dollar-sign"></i> Papara</p></a>
          <a href="https://www.bynogame.com/tr/destekle/ohalava" target="_blank"><p><i class="fa-solid fa-arrow-turn-up"></i> <i class="fa-solid fa-dollar-sign"></i> ByNoGame</p></a>
        </div>
          <a href="https://www.instagram.com/ohalava/" target="_blank"><p><i class="fa-brands fa-instagram"></i>Instagram</p></a>
          <a href="http://twitch.tv/ohalava" target="_blank"><p><i class="fa-brands fa-twitch"></i>Twitch</p></a>
          <a href="https://youtube.com/@OhaLava" target="_blank"><p><i class="fa-brands fa-youtube"></i>Youtube</p></a>
          <a href="https://discord.com/invite/RwzBsMTpc9" target="_blank"><p><i class="fa-brands fa-discord"></i>Discord</p></a>
          <a href="https://twitter.com/ohalava" target="_blank"><p><i class="fa-brands fa-x-twitter"></i>Twitter</p></a>
          <a href="https://www.behance.net/gallery/170092175/My-Portfolio" target="_blank"><p><i class="fa-brands fa-behance"></i>Behance</p></a>
        </div>
  </div>

    </div>
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
    <img src="../ad2.gif" alt="ad" id="ad1" on:click={randomCatVids}>
  </div>

<style>

  .container {
    display: flex;
    margin: 0 auto;
    justify-content: center;
    align-items: center;
    height: 100vh;
    color: black;
  }

  .alt {
    box-sizing: border-box;
    width: 350px;
    display: flex;
    flex-direction: column;
    border-radius: 2%;
    justify-content: center;
    align-items: center;
    min-height: auto;
    overflow: hidden;
    width: 400px;
  }

  .acrylic-effect {
    background-color: rgba(223, 223, 223, 0.5); 
    backdrop-filter: blur(15px);
    border: 0px solid rgba(0, 0, 0, 0.2);
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); 
    padding: 10px;
    border-radius: 2%;
  }

  .profile {
    padding-top: 15px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .profile h1 {
    font-family: "Golden Age Regular", sans-serif;
    font-size: 2em;
    font-weight: 600;
  }

  .profile img {
    border-radius: 50%;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    width: 128px;
  }

  .row p {
    font-family: "San Francisco", sans-serif;
    font-size: 1.1rem;
    color: black;

  }

  .support h3 {
    font-family: "San Francisco", sans-serif;
    font-weight: 600;
  }

  a {
    text-decoration: none;
    color: black;
  }

  .support {
    width: fit-content;
  }
  
  .support p {
    margin-left: 20px;
  }

  .fa-regular.fa-folder-open {
    font-size: .8em;
  }

  i {
    padding-right: 10px;
    margin: 0%;
    padding-bottom: 0%;
    font-size: 1.3rem;
  }

  #ad1, #ad2 {
    cursor: pointer;
    -webkit-user-drag: none;
    user-select: none;
    position: absolute;
  }

  #ad1 {
    right: 5px;
  }

  #ad2 {
    left: 5px;
  }

  .fa-solid.fa-arrow-turn-up {
    rotate: 90deg;
    margin-right: 10px;
    pointer-events: none;
    font-size: 1rem;
  }

  .fa-regular.fa-folder-open {
    color: #FFD152;
    font-size: 1.3rem;
  }

  .fa-solid.fa-dollar-sign {
    color: #85BB65;
  }

  .fa-brands.fa-instagram {
    background: radial-gradient(circle at 30% 107%, #fdf497 0%, #fdf497 5%, #fd5949 45%, #d6249f 60%, #285AEB 90%);
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
    display: inline-block;
  }

  .fa-brands.fa-twitch {
    color: #9146FF;
  }

  .fa-brands.fa-youtube {
    color: #FF0000;
  }

  .fa-brands.fa-discord {
    color: #5865F2;
  }

  .fa-brands.fa-x-twitter {
    color: black;
  }

  .fa-brands.fa-behance {
    color: #1769FF;
  }
</style>