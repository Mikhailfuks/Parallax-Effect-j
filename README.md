<!DOCTYPE html>
<html>
<head>
  <title>Parallax Effect</title>
  <style>
    body {
      margin: 0;
      overflow-x: hidden; /* Prevent horizontal scrolling */
    }

    .section {
      position: relative;
      height: 600px; /* Adjust height as needed */
      overflow: hidden;
    }

    .section::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
      z-index: -1;
    }

    .section.one::before {
      background-image: url('https://images.unsplash.com/photo-1519681393784-d1202679900a?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1950&q=80');
      background-attachment: fixed; /* Parallax effect on background */
    }

    .section.two::before {
      background-image: url('https://images.unsplash.com/photo-1563492065552-13a2072f0ce8?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1950&q=80');
      background-attachment: scroll; /* Normal scrolling on background */
    }

    .section.three::before {
      background-image: url('https://images.unsplash.com/photo-1533740126741-b5c607a74835?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1950&q=80');
      background-attachment: fixed;
      background-position: center;
      background-repeat: no-repeat;
      z-index: -1;
    }

    .section-content {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      text-align: center;
      color: white;
      z-index: 1; /* Place content on top of background */
    }

    .section-content h1 {
      margin-bottom: 20px;
    }

    /* Optional: Add some visual separation between sections */
    .section + .section {
      margin-top: -20px;
    }
  </style>
</head>
<body>
  <div class="section one">
    <div class="section-content">
      <h1>Section One</h1>
      <p>This section demonstrates a parallax background with fixed attachment.</p>
    </div>
  </div>

  <div class="section two">
    <div class="section-content">
      <h1>Section Two</h1>
      <p>This section has a normal scrolling background.</p>
    </div>
  </div>

  <div class="section three">
    <div class="section-content">
      <h1>Section Three</h1>
      <p>This section demonstrates a fixed background for a more static effect.</p>
    </div>
  </div>
</body>
</html>
