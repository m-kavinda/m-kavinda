<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>YouTube Music Player</title>
  <style>
    body { display: flex; justify-content: center; align-items: center; height: 100vh; margin: 0; background: #f0f0f0; font-family: Arial, sans-serif; }
    .player { background: #333; padding: 20px; border-radius: 10px; box-shadow: 0 0 10px rgba(0,0,0,0.3); text-align: center; color: white; }
    .progress-bar { width: 100%; height: 5px; background: #555; border-radius: 5px; margin: 10px 0; overflow: hidden; }
    .progress { width: 0; height: 100%; background: #ff0000; transition: width 0.1s linear; }
    .controls button { background: #ff0000; border: none; padding: 10px 20px; margin: 5px; border-radius: 5px; color: white; cursor: pointer; transition: transform 0.2s; }
    .controls button:hover { transform: scale(1.1); }
    #player { display: none; }
    .volume { margin: 10px 0; }
  </style>
</head>
<body>
  <div class="player">
    <h2 id="track-title">YouTube Music Player</h2>
    <div id="player"></div>
    <div class="progress-bar"><div class="progress" id="progress"></div></div>
    <div class="controls">
      <button onclick="playPause()">Play/Pause</button>
      <button onclick="restart()">Restart</button>
    </div>
    <div class="volume">
      <label for="volume">Volume:</label>
      <input type="range" id="volume" min="0" max="100" value="100" onchange="setVolume(this.value)">
    </div>
  </div>
  <script src="https://www.youtube.com/iframe_api"></script>
  <script>
    let player;
    function onYouTubeIframeAPIReady() {
      player = new YT.Player('player', {
        height: '0',
        width: '0',
        videoId: 'iBlpUYogVTw',
        playerVars: { 'autoplay': 0, 'controls': 0 },
        events: {
          'onReady': onPlayerReady,
          'onStateChange': onPlayerStateChange
        }
      });
    }
    function onPlayerReady(event) {
      document.getElementById('track-title').textContent = 'Loading title...';
      // YouTube Data API එකෙන් title එක ගන්න පුළුවන් (API key එකක් ඕන)
    }
    function onPlayerStateChange(event) {
      if (event.data == YT.PlayerState.PLAYING) {
        updateProgress();
      }
    }
    function playPause() {
      if (player.getPlayerState() == 1) {
        player.pauseVideo();
      } else {
        player.playVideo();
      }
    }
    function restart() {
      player.seekTo(0);
      player.playVideo();
    }
    function setVolume(value) {
      player.setVolume(value);
    }
    function updateProgress() {
      const progress = document.getElementById('progress');
      const duration = player.getDuration();
      const update = () => {
        if (player.getPlayerState() == 1) {
          const currentTime = player.getCurrentTime();
          const percent = (currentTime / duration) * 100;
          progress.style.width = percent + '%';
          requestAnimationFrame(update);
        }
      };
      requestAnimationFrame(update);
    }
  </script>
</body>
</html>

[![YouTube Now Playing: Kiyadun premaya](https://img.shields.io/badge/YouTube%20Now%20Playing-Kiyadun%20premaya-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/watch?v=syoslCy-q1o)

[![Now Playing](https://img.youtube.com/vi/iBlpUYogVTw/hqdefault.jpg)](https://www.youtube.com/watch?v=iBlpUYogVTw)


[![Google Dev](https://img.shields.io/badge/Google%20Dev-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://developers.google.com/profile/u/mrkaviyaa)
[![Spotify](https://img.shields.io/badge/Spotify-1ED760?&style=for-the-badge&logo=spotify&logoColor=white)](https://open.spotify.com/user/22jg2nzzjqglq2mzjqznopmba?si=1oxx6irkQf-81q4RMkK6mg)  
[![X](https://img.shields.io/badge/Twitter-000000?style=for-the-badge&logo=x&logoColor=white)](https://x.com/mkaviyaa) 
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/m-kavinda)  
[![TikTok](https://img.shields.io/badge/TikTok-010101?style=for-the-badge&logo=tiktok&logoColor=white)](https://www.tiktok.com/@mkaviyaa) 
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/m.r.kaviyaa/)  
[![Facebook](https://img.shields.io/badge/Facebook-0866FF?style=for-the-badge&logo=facebook&logoColor=white)](https://www.facebook.com/m.r.kaviyaa/) 
[![YouTube](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://youtube.com/@mr-kaviyaa)

<details>
  <summary>Languages & Database</summary>
ㅤ
  
[![Go](https://img.shields.io/badge/go-%2308afd8.svg?style=for-the-badge&logo=go&logoColor=white)](https://golang.org/) [![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)](https://www.java.com/) [![JavaScript](https://img.shields.io/badge/javascript-%23f0dc55.svg?style=for-the-badge&logo=javascript&logoColor=black)](https://www.javascript.com/) [![Kotlin](https://img.shields.io/badge/kotlin-%237F52FF.svg?style=for-the-badge&logo=kotlin&logoColor=white)](https://kotlinlang.org/) [![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)](https://www.python.org/)

[![Firebase](https://img.shields.io/badge/firebase-a08021?style=for-the-badge&logo=firebase&logoColor=ffcd34)](https://firebase.google.com/) [![MySQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/) [![SQLite](https://img.shields.io/badge/sqlite-%2308425c.svg?style=for-the-badge&logo=sqlite&logoColor=white)](https://www.sqlite.org/)

</details>

<details>
  <summary>Softwares & Services</summary>
ㅤ
  
[![Adobe](https://img.shields.io/badge/adobe-%23fa1408.svg?style=for-the-badge&logo=adobe&logoColor=white)](https://www.adobe.com/) [![Affinity](https://img.shields.io/badge/Affinity-222324.svg?style=for-the-badge&logo=Affinity&logoColor=white)](https://affinity.serif.com/) [![Figma](https://img.shields.io/badge/figma-%23f25425.svg?style=for-the-badge&logo=figma&logoColor=white)](https://www.figma.com/) [![Gimp](https://img.shields.io/badge/Gimp-605949?style=for-the-badge&logo=gimp&logoColor=FFFFFF)](https://www.gimp.org/) [![Sketch](https://img.shields.io/badge/Sketch-fdb008?style=for-the-badge&logo=sketch&logoColor=black)](https://www.sketch.com/)

[![Android Studio](https://img.shields.io/badge/Android%20Studio-072F41.svg?style=for-the-badge&logo=android-studio&logoColor=3DDB83)](https://developer.android.com/studio) [![GoLand](https://img.shields.io/badge/GoLand-0f0f0f?&style=for-the-badge&logo=goland&logoColor=white)](https://www.jetbrains.com/go/) 	[![IntelliJ IDEA](https://img.shields.io/badge/IntelliJIDEA-000000.svg?style=for-the-badge&logo=intellij-idea&logoColor=white)](https://www.jetbrains.com/idea/) [![Neovim](https://img.shields.io/badge/NeoVim-%234e8b3a.svg?&style=for-the-badge&logo=neovim&logoColor=white)](https://neovim.io/) [![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-097dcd.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white)](https://code.visualstudio.com/) [![Zed](https://img.shields.io/badge/Zed-white?style=for-the-badge&logo=zedindustries&logoColor=084CCF)](https://zed.dev/)

[![CMake](https://img.shields.io/badge/CMake-%23086c6b.svg?style=for-the-badge&logo=cmake&logoColor=white)](https://cmake.org/) [![Git](https://img.shields.io/badge/GIT-f05539?style=for-the-badge&logo=git&logoColor=white)](https://git-scm.com/) [![MD](https://img.shields.io/badge/material%20design-6c55a7?style=for-the-badge&logo=material%20design&logoColor=white)](https://m3.material.io/) [![Ant-Design](https://img.shields.io/badge/Ant%20Design-0170FE.svg?style=for-the-badge&logo=Ant-Design&logoColor=white)](https://ant.design/)

[![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=for-the-badge&logo=Cloudflare&logoColor=white)](https://www.cloudflare.com/) [![Firebase](https://img.shields.io/badge/firebase-a08021?style=for-the-badge&logo=firebase&logoColor=ffcd34)](https://firebase.google.com/) [![Google Cloud](https://img.shields.io/badge/GoogleCloud-%234889f4.svg?style=for-the-badge&logo=google-cloud&logoColor=white)](https://cloud.google.com/)

[![GitHub Actions](https://img.shields.io/badge/github%20actions-%23161b22.svg?style=for-the-badge&logo=githubactions&logoColor=white)](https://github.com/features/actions)

</details>

<details>
  <summary>Systems</summary>
ㅤ
  
[![Android](https://img.shields.io/badge/Android-3aab58?style=for-the-badge&logo=android&logoColor=white)](https://www.android.com/) [![iOS](https://img.shields.io/badge/iOS-000000?style=for-the-badge&logo=ios&logoColor=white)](https://www.apple.com/ios/)

[![Fedora](https://img.shields.io/badge/Fedora-51A2DA?style=for-the-badge&logo=fedora&logoColor=white)](https://getfedora.org/) [![Gnome](https://img.shields.io/badge/GNOME-080808.svg?style=for-the-badge&logo=GNOME&logoColor=white)](https://www.gnome.org/) [![Windows](https://img.shields.io/badge/Windows-087cd5?style=for-the-badge&logo=windows&logoColor=white)](https://www.microsoft.com/windows/)

</details>



## 🕶️ Philosophy
> _“I don’t build apps. I build moods.”_  
> _“Every pixel must earn its place.”_

---

## 📫 Connect
Feel free to fork, remix, or just observe in silence.  
No stars needed—just resonance.