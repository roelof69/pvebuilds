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
    margin: 57px 0 0; /* <<< gives room for the navbar */
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
        margin: 57px 0 0; /* <<< gives room for the navbar */
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
      #twitch {
        border-radius: 0.25rem !important;
        position: fixed;
        bottom: 5px;
        right: 5px;
        outline: 2px solid #121212;
        width: 432px;
        height: 243px;
        overflow: hidden;
        z-index:10;
      }
      
      #twitch object,
      #twitch iframe{
        border-radius: 0.25rem !important;
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        z-index:10;
      }   

        #ttvclose input{
        position: fixed;
        right:8px;
        bottom:220px;
        float:right;
        z-index:11;
        background:transparent;
        color:white;
        border:none;  
      }  

</style> 

<!-- Twitch Video Embed -->
<script src="https://player.twitch.tv/js/embed/v1.js"></script>

<div id="ttvclose" class="hide"><input type="button" value="X" onclick="removeTTV()"></input></div>

<div id="twitch" class="hide"></div>




<script>
    function removeTTV() {
        twitch.remove();
        handleOffline();
    }

  if (window.innerWidth > 500) {
    var options = {
    channel: "genedictb", // TODO: Change this to the streamsusername you want to embed
    width: 640,
    height: 360,
    parent: ["pvebuilds.xyz"],
    };
    var player = new Twitch.Player("twitch", options);

    player.addEventListener(Twitch.Player.READY, initiate)

    function initiate() {
      player.addEventListener(Twitch.Player.ONLINE, handleOnline);
      player.addEventListener(Twitch.Player.OFFLINE, handleOffline);
      player.removeEventListener(Twitch.Player.READY, initiate);
    }

    function handleOnline() {
      document.getElementById("ttvclose").classList.remove('hide');
      document.getElementById("hide").classList.remove('hide');
      player.removeEventListener(Twitch.Player.ONLINE, handleOnline);
      player.addEventListener(Twitch.Player.OFFLINE, handleOffline);
      player.setMuted(false);
    }

    function handleOffline() {
      document.getElementById("twitch").classList.add('hide');
      document.getElementById("ttvclose").classList.add('hide');
      player.removeEventListener(Twitch.Player.OFFLINE, handleOffline);
      player.addEventListener(Twitch.Player.ONLINE, handleOnline);
      player.setMuted(true);
    }
  }
</script>

  <div id="iframe-container">
    <iframe scrolling="no" frameborder="0" marginheight="0" marginwidth="0"
      src="https://docs.google.com/spreadsheets/d/e/2PACX-1vTnVjb3srmOBZoXm6VKs05dSJDED1qJM6A6miMgsCG8Hb7kH37biLYRzKkUIVZGwNyjiKZtXyBnSLy5/pubhtml?headers=false&gridlines=false"></iframe>
  </div>
