---
title: "Builds"
description: "M11 Builds."
weight: 10
---
<style>#iframe-container {
    position: fixed;
    left: 0;
    top: 0;            /* <<< No offset */
    bottom: 0;         /* <<< Pull to the bottom for height */
    right:0;
    margin: 60px 0 0; /* <<< gives room for the navbar */
    overflow: hidden;
}

#iframe-container iframe {
  position: relative;
  display:flex;
  height:100%;
  width:100%;
  overflow:hidden;
}

@media screen and (max-width:500px) {
      #iframe-container {
        position:absolute;
        top:0;
        left:0;
        height:250%;
        width:250%;
        margin: 60px 0 0; /* <<< gives room for the navbar */
        overflow: hidden;
      }
}
</style>


<!-- Twitch Embed Styling -->
<style>
    .hide {
        display: none
      }
      
      
      /* The following css just makes sure the twitch video stays responsive */
      #twitch,
      #twitch2,
      #twitch3 {
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
      #twitch2 iframe,
      #twitch3 object,
      #twitch3 iframe {
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
        #twitch2,
        #twitch3 {
          width: 208px;
          height: 117px;
          top:175px;
          right: 5px;
        }
      }
    
      
</style>

<!-- Twitch Video Embed -->
<script src="https://player.twitch.tv/js/embed/v1.js"></script>

<div id="twitch" class="hide">
</div>
<div id="twitch2" class="hide">
</div>
<div id="twitch3" class="hide">
</div>

<!-- Twitch Video Embed m11-->

<script>
  var options = {
    channel: "m11pve",
    width: 1280,
    height: 720,
    parent: ["pvebuilds.xyz"]
  };
  var options2 = {
    channel: "genedictb",
    width: 1280,
    height: 720,
    parent: ["pvebuilds.xyz"]
  };
  var options3 = {
    channel: "olddirtydaz",
    width: 1280,
    height: 720,
    parent: ["pvebuilds.xyz"]
  };
  var player3 = new Twitch.Player("twitch3", options3);
  var player2 = new Twitch.Player("twitch2", options2);
  var player = new Twitch.Player("twitch", options);
  player.addEventListener(Twitch.Player.READY, initiate)
  player.addEventListener(Twitch.Player.OFFLINE, initiate2);
  player.addEventListener(Twitch.Player.OFFLINE, initiate3);

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
  


  function initiate3() {
    player3.addEventListener(Twitch.Player.ONLINE, handleOnline3);
    player3.addEventListener(Twitch.Player.OFFLINE, handleOffline3);
    player3.removeEventListener(Twitch.Player.READY, initiate3);
  }

  function handleOnline3() {
    document.getElementById("twitch3").classList.remove('hide');
    player3.removeEventListener(Twitch.Player.ONLINE, handleOnline3);
    player3.addEventListener(Twitch.Player.OFFLINE, handleOffline3);
    player3.setMuted(false);
    player3.setVolume(0.1);
  }

  function handleOffline3() {
    document.getElementById("twitch3").classList.add('hide');
    player3.removeEventListener(Twitch.Player.OFFLINE, handleOffline3);
    player3.addEventListener(Twitch.Player.ONLINE, handleOnline3);
    player3.setMuted(true);
  }
</script>

  <div id="iframe-container">
    <iframe scrolling="no" frameborder="0" marginheight="0" marginwidth="0"
      src="https://docs.google.com/spreadsheets/d/e/2PACX-1vTnVjb3srmOBZoXm6VKs05dSJDED1qJM6A6miMgsCG8Hb7kH37biLYRzKkUIVZGwNyjiKZtXyBnSLy5/pubhtml?headers=false&gridlines=false"></iframe>
  </div>
