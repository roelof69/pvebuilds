---

Title: ""
description: "New World M10 World Records."
lead: "The World's Fastest M10 Gold Clear Times."
weight: 600
toc: false
---

<!-- 1. The <iframe> (video player) will replace this <div> tag. -->
  <div style="position:fixed;top:0;left:0;height:100vh;width:100vw;z-index:-1;">
    <div id="player"></div>
  </div>
  
  <style>
    #player {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      width: 118%;
      height: 118%;
      pointer-events: none;
    }
  
    @media screen and (max-width:1000px) {
      #player {
        width: 165%;
        height: 165%;
      }
    }
  
    @media screen and (max-width:500px) {
      #player {
        width: 400%;
        height: 400%;
      }
    }
  </style>
  
  
  <script>
    // 2. This code loads the IFrame Player API code asynchronously.
    var tag = document.createElement('script');
  
    tag.src = "https://www.youtube.com/iframe_api";
    var firstScriptTag = document.getElementsByTagName('script')[0];
    firstScriptTag.parentNode.insertBefore(tag, firstScriptTag);
  
    // 3. This function creates an <iframe> (and YouTube player)
    //    after the API code downloads.
    var player;
    function onYouTubeIframeAPIReady() {
      player = new YT.Player('player', {
        height: '100%',
        width: '100%',
        videoId: 'ZHO0ZnXQrww',
        playerVars: { 'autoplay': 1, 'playsinline': 1, 'loop': 1, 'list': "PLn2kD3sUIiokXPgqH53FUkZPcq3EA90ix" },
        events: {
          'onReady': onPlayerReady
        }
      });
    }
    // 4. The API will call this function when the video player is ready.
    function onPlayerReady(event) {
      event.target.mute();
      event.target.playVideo();
    }
  </script>
<!-- Twitch Embed Styling -->
<style>
    .hide {
        display: none
      }
      
      
      /* The following css just makes sure the twitch video stays responsive */
      #twitch,
      #twitch2 {
        border-radius: 0.25rem !important;
        z-index: 1000;
        position: fixed;
        bottom: 5px;
        right: 5px;
        outline: 2px solid #121212;
        width: 432px;
        height: 243px;
        overflow: hidden;
      }
      
      #twitch object,
      #twitch iframe,
      #twitch2 object,
      #twitch2 iframe {
        z-index: 1000;
        border-radius: 0.25rem !important;
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
      }
      @media screen and (max-width:600px) {
        #twitch,
        #twitch2 {
          width: 208px;
          height: 117px;
          bottom:75px;
        }
      }
    
      
</style>
<!-- Twitch Video Embed -->
<script src="https://player.twitch.tv/js/embed/v1.js"></script>

<div id="twitch" class="hide">
</div>
<div id="twitch2" class="hide">
</div>

<!-- Twitch Video Embed genedictb m11-->
<script>
  var options = {
    channel: "igraphici",
    width: 1280,
    height: 720,
    parent: ["pvebuilds.xyz"]
  };
  var options2 = {
    channel: "chun",
    width: 1280,
    height: 720,
    parent: ["pvebuilds.xyz"]
  };
  var player2 = new Twitch.Player("twitch2", options2);
  var player = new Twitch.Player("twitch", options);
  player.addEventListener(Twitch.Player.READY, initiate)
  player.addEventListener(Twitch.Player.OFFLINE, initiate2);

  function initiate() {
    player.addEventListener(Twitch.Player.ONLINE, handleOnline);
    player.addEventListener(Twitch.Player.OFFLINE, handleOffline);
    player.removeEventListener(Twitch.Player.READY, initiate);
  }

  function handleOnline() {
    document.getElementById("twitch").classList.remove('hide');
    player.removeEventListener(Twitch.Player.ONLINE, handleOnline);
    player.addEventListener(Twitch.Player.OFFLINE, handleOffline);
    player2.pause();
    player2.setMuted(true);
    player.setMuted(false);
    player.setVolume(0.1);
  }

  function handleOffline() {
    player.setMuted(true);
    document.getElementById("twitch").classList.add('hide');
    player.removeEventListener(Twitch.Player.OFFLINE, handleOffline);
  }
  function initiate2() {
    player2.addEventListener(Twitch.Player.ONLINE, handleOnline2);
    player2.addEventListener(Twitch.Player.OFFLINE, handleOffline2);
    player2.removeEventListener(Twitch.Player.READY, initiate2);
  }

  function handleOnline2() {
    document.getElementById("twitch2").classList.remove('hide');
    player2.removeEventListener(Twitch.Player.ONLINE, handleOnline2);
    player2.addEventListener(Twitch.Player.OFFLINE, handleOffline2);
    player2.setMuted(false);
    player2.setVolume(0.1);
  }

  function handleOffline2() {
    document.getElementById("twitch2").classList.add('hide');
    player2.removeEventListener(Twitch.Player.OFFLINE, handleOffline2);
    player2.addEventListener(Twitch.Player.ONLINE, handleOnline2);
    player2.setMuted(true);
  }
</script>


<div style="background-color:rgba(0, 0, 0, 0.75);padding-top:125px;margin-top:-125px;padding-bottom:50px;color:white;">

<h1>M10 Gold World Records</h1>

Listed in order of fastest -> slowest expedition.

---

## 08:58 - Garden of Genesis
**<a href="https://www.youtube.com/watch?v=dDpG-hSfmJ0" target="_blank">VOD1</a> || <a href="https://www.youtube.com/watch?v=-eG2SRCqnGY" target="_blank">VOD2</a>**

Server: **Nysa (EU)**

Company: **Benedicat**

**Snajl | Benedict G. | Hrodgir | Drexen | Corisita**

Hatchet+IG | Hatchet+Spear | Hatchet+GA | Hatchet+VG | LS+VG

---

## 12:37 - Dynasty Shipyard
**<a href="https://www.youtube.com/watch?v=lps2Wz4dOjY" target="_blank">VOD</a>**

Server: **Nysa (EU)**

Company: **Benedicat**

**Drexen | Benedict G. | Hrodgir | Riasq | Corisita**

SnS+WH | Hatchet+Spear | Rapier+IG | Hatchet+GA | LS+VG

---

## 13:04 - The Lazarus Instrumentality

**<a href="https://www.reddit.com/r/newworldgame/comments/xuuljv/wr_lazarus_m10_speedrun_13m04/" target="_blank">Reddit</a> || <a href="https://www.youtube.com/watch?v=yrjU7_QVRmE" target="_blank">VOD</a>**

Server: **Nysa (EU)**

Company: **Benedicat**

**Drexen | Benedict G. | Hrodgir | Riasq | Corisita**

Sns+WH | Rapier+Spear | Rapier+IG | WH+GA | LS+VG

---

## 13:11 - The Depths

**<a href="https://www.youtube.com/watch?v=x8oNOUMBZE0" target="_blank">VOD</a>**

Server: **Nysa (EU)**

**Drexen | Benedict G. | Hrodgir | Riasq | Corisita**

SnS+WH | Hatchet+GA | Hatchet+Spear | Hatchet+GA | LS+VG

---

## 18:15 - Barnacles and Blackpowder
**<a href="https://gyazo.com/614ca973056571e5fc422d6bab04d6f5" target="_blank">IMG</a> || <a href="https://www.twitch.tv/videos/1600744357" target="_blank">VOD</a>**

Server: **Delos (AP)**

Company: **M11**

**Dopple | Perihelia | Lohqq | bigWino | Roelof xd**

Sword+WH/Hatchet | Hatchet+IG | WH+GA | Hatchet+GA | LS+VG

---

## 22:10 - Tempest's Heart
**<a href="https://www.reddit.com/r/newworldgame/comments/xpdbie/wr_tempest_m10_speedrun_22m10/" target="_blank">IMG</a> || <a href="https://www.youtube.com/watch?v=FytVRgBbwmI" target="_blank">VOD</a>**


Server: **Nysa (EU)**

Company: **Benedicat**

**Drexen | Benedict G. | Hrodgir | Riasq | Corisita**

Sword+WH | Hatchet+GA | Rapier+IG | Hatchet+GA | LS+VG





