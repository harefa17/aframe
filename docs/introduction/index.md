<html>
  <head>
    <meta charset="utf-8">
    <title>Tur Virtual Pegunungan Indonesia</title>
    <script src="https://aframe.io/releases/1.5.0/aframe.min.js"></script>
  </head>
  <body>
    <a-scene>
      <!-- Panorama 360° -->
      <a-sky id="sky" src="https://example.com/bromo.jpg" rotation="0 -130 0"></a-sky>

      <!-- Tombol Navigasi -->
      <a-entity position="0 1.6 -2">
        <a-box id="btnRinjani" position="-1 0 0" depth="0.2" height="0.5" width="1" color="#4CC3D9"></a-box>
        <a-text value="Gunung Rinjani" position="-1 0.6 0" align="center" color="#000"></a-text>

        <a-box id="btnPuncakJaya" position="1 0 0" depth="0.2" height="0.5" width="1" color="#EF2D5E"></a-box>
        <a-text value="Puncak Jaya" position="1 0.6 0" align="center" color="#000"></a-text>
      </a-entity>

      <!-- Kamera dan Kursor -->
      <a-camera>
        <a-cursor></a-cursor>
      </a-camera>
    </a-scene>

    <script>
      // Fungsi untuk mengganti panorama
      document.querySelector('#btnRinjani').addEventListener('click', function () {
        document.querySelector('#sky').setAttribute('src', 'https://example.com/rinjani.jpg');
      });

      document.querySelector('#btnPuncakJaya').addEventListener('click', function () {
        document.querySelector('#sky').setAttribute('src', 'https://example.com/puncakjaya.jpg');
      });
    </script>
  </body>
</html>
