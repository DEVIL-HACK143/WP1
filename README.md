# <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Landing Page</title>
  <style>
    body, html {
      margin: 0;
      padding: 0;
      height: 100%;
      overflow: hidden;
      background: black;
    }
    .overlay {
      position: absolute;
      top: 0;
      left: 0;
      height: 100%;
      width: 100%;
      background: rgba(0, 0, 0, 0.5);
    }
    .content {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      color: white;
      font-size: 2rem;
      text-align: center;
    }
    video.bg-video {
      position: absolute;
      top: 0;
      left: 0;
      width: 100vw;
      height: 100vh;
      object-fit: cover;
      z-index: -1;
    }
  </style>
</head>
<body>
  <video class="bg-video" autoplay muted loop>
    <source src="your-video.mp4" type="video/mp4" />
    Your browser does not support the video tag.
  </video>

  <div class="overlay"></div>

  <div class="content">
    <p>Welcome to My Website</p>
  </div>

  <script>
    // Optional: You can read the "code" from the URL
    const params = new URLSearchParams(window.location.search);
    const code = params.get('code');
    console.log("Code in URL:", code);
  </script>
</body>
</html>
