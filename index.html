<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>SpyFlix - Demo & Locked Videos</title>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;500;700&display=swap" rel="stylesheet" />
  <style>
    /* Background image from https://unsplash.com/photos/2JIvboGLeho (blurred dark) */
    body {
      margin: 0;
      font-family: 'Roboto', sans-serif;
      background: url('https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=1470&q=80') no-repeat center center fixed;
      background-size: cover;
      color: #fff;
      backdrop-filter: brightness(0.4);
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }

    header {
      background-color: rgba(0, 0, 0, 0.85);
      padding: 0.8rem 2rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: sticky;
      top: 0;
      z-index: 10;
      box-shadow: 0 2px 8px rgba(0,0,0,0.8);
    }

    /* Logo merged inside login button */
    #loginBtn {
      background-color: #e50914;
      border: none;
      color: white;
      font-weight: 700;
      padding: 0.5rem 1.5rem;
      font-size: 1.3rem;
      border-radius: 6px;
      cursor: pointer;
      display: flex;
      align-items: center;
      gap: 0.7rem;
      user-select: none;
      transition: background-color 0.3s ease;
    }
    #loginBtn:hover {
      background-color: #f40612;
    }
    #loginBtn svg {
      fill: white;
      width: 28px;
      height: 28px;
      flex-shrink: 0;
    }

    /* Navigation buttons separate container */
    .nav-buttons {
      display: flex;
      gap: 1rem;
    }
    .nav-buttons button {
      background-color: transparent;
      border: 2px solid #e50914;
      color: #e50914;
      padding: 0.4rem 1.2rem;
      font-weight: 600;
      font-size: 1rem;
      border-radius: 6px;
      cursor: pointer;
      transition: background-color 0.3s ease, color 0.3s ease;
    }
    .nav-buttons button:hover {
      background-color: #e50914;
      color: white;
    }

    main {
      max-width: 1000px;
      margin: 2rem auto 3rem auto;
      padding: 0 1rem;
      flex-grow: 1;
      background: rgba(0,0,0,0.7);
      border-radius: 12px;
      box-shadow: 0 0 15px #e50914aa;
    }

    h2 {
      border-left: 5px solid #e50914;
      padding-left: 0.5rem;
      margin-bottom: 1rem;
    }

    .videos-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 1.5rem;
    }

    .video-card {
      background: #222;
      border-radius: 8px;
      overflow: hidden;
      box-shadow: 0 2px 10px rgba(0,0,0,0.7);
      position: relative;
      padding-bottom: 56.25%; /* 16:9 ratio */
      height: 0;
    }

    .video-card iframe,
    .video-card video {
      position: absolute;
      top: 0; left: 0;
      width: 100%; height: 100%;
      border: none;
      border-radius: 8px;
      background: black;
    }

    /* Locked video overlay */
    .locked-video {
      background: #111;
      border-radius: 8px;
      padding: 1rem;
      position: relative;
      box-shadow: 0 2px 10px rgba(0,0,0,0.8);
    }

    .locked-video img {
      width: 100%;
      border-radius: 8px;
      margin-bottom: 0.7rem;
      cursor: pointer;
      height: 160px;
      object-fit: cover;
      transition: transform 0.3s ease;
    }
    .locked-video img:hover {
      transform: scale(1.03);
    }

    .locked-video video {
      display: none;
      margin-top: 0.7rem;
      border-radius: 8px;
      width: 100%;
      height: 180px;
      background: black;
    }

    .locked-video .price {
      font-weight: bold;
      color: #e50914;
      margin-bottom: 0.7rem;
      text-align: center;
      font-size: 1.1rem;
    }

    .locked-video input[type="password"] {
      width: 100%;
      padding: 0.5rem;
      font-size: 1rem;
      border-radius: 4px;
      border: none;
      margin-bottom: 0.5rem;
      outline: none;
      box-sizing: border-box;
    }

    .locked-video button.submit-pass-btn {
      width: 100%;
      padding: 0.5rem;
      background-color: #e50914;
      color: white;
      border: none;
      border-radius: 4px;
      font-weight: 600;
      cursor: pointer;
      margin-bottom: 0.5rem;
      transition: background-color 0.3s ease;
    }
    .locked-video button.submit-pass-btn:hover {
      background-color: #f40612;
    }

    .locked-video button.pay-btn {
      width: 100%;
      padding: 0.5rem;
      background-color: #222;
      color: #e50914;
      border: 2px solid #e50914;
      border-radius: 4px;
      font-weight: 600;
      cursor: pointer;
      margin-bottom: 0.5rem;
      transition: background-color 0.3s ease, color 0.3s ease;
    }
    .locked-video button.pay-btn:hover {
      background-color: #e50914;
      color: white;
    }

    .locked-video #unlockMsg {
      margin-top: 0.5rem;
      min-height: 1.2em;
      font-weight: 600;
      text-align: center;
    }

    /* Payment Modal */
    #paymentModal {
      position: fixed;
      top: 0; left: 0;
      width: 100vw;
      height: 100vh;
      background: rgba(0,0,0,0.85);
      display: none;
      justify-content: center;
      align-items: center;
      z-index: 100;
      padding: 1rem;
      box-sizing: border-box;
    }
    #paymentModal.active {
      display: flex;
    }
    #paymentContent {
      background: #222;
      padding: 2rem;
      border-radius: 10px;
      max-width: 400px;
      width: 100%;
      text-align: center;
      color: white;
      box-shadow: 0 0 15px #e50914;
    }
    #paymentContent h3 {
      margin-top: 0;
      color: #e50914;
    }
    #paymentContent img {
      max-width: 250px;
      margin: 1rem 0;
      border-radius: 8px;
      box-shadow: 0 0 8px #e50914;
    }
    #paymentContent p {
      margin-bottom: 1rem;
      font-weight: 500;
    }
    #paymentContent .warning {
      margin-top: 1rem;
      padding: 0.8rem;
      background: #660000;
      border-radius: 6px;
      font-weight: 600;
      color: #ff6666;
      border: 1.5px solid #ff3333;
    }
    #paymentContent button.closeBtn {
      background: #e50914;
      border: none;
      color: white;
      padding: 0.5rem 1.2rem;
      font-weight: 600;
      cursor: pointer;
      border-radius: 5px;
      margin-top: 1rem;
      transition: background-color 0.3s ease;
    }
    #paymentContent button.closeBtn:hover {
      background: #f40612;
    }

    /* Responsive */
    @media (max-width: 600px) {
      .videos-grid {
        grid-template-columns: 1fr;
      }
      #paymentContent {
        max-width: 90vw;
      }
      header {
        flex-wrap: wrap;
        gap: 1rem;
      }
      .nav-buttons {
        flex: 1 1 100%;
        justify-content: center;
      }
    }
  </style>
</head>
<body>
  <header>
    <!-- Login Button with SpyFlix logo merged -->
    <button id="loginBtn" onclick="alert('Login feature coming soon!')" aria-label="Login to SpyFlix">
      <!-- SpyFlix SVG logo - simple 'S' shaped flame -->
      <svg viewBox="0 0 64 64" aria-hidden="true" focusable="false" >
        <path d="M32 2C22 16 18 29 18 42c0 11 9 20 14 20s14-9 14-20c0-13-10-30-14-40z" />
      </svg>
      SpyFlix Login
    </button>

    <!-- Navigation buttons separate -->
    <nav class="nav-buttons" role="navigation" aria-label="Main Navigation">
      <button onclick="document.getElementById('demoVideos').scrollIntoView({behavior:'smooth'})">Demo Videos</button>
      <button onclick="document.getElementById('lockedVideos').scrollIntoView({behavior:'smooth'})">Locked Videos</button>
    </nav>
  </header>

  <main>
    <section id="demoVideos">
      <h2>🎬 Demo Videos (Free to Watch)</h2>
      <div class="videos-grid">
        <div class="video-card">
        <iframe allow="fullscreen" allowfullscreen height="400" src="https://streamable.com/e/ux528m?" width="256" style="border:none;"></iframe>
      </div>
        <div class="video-card">
         <iframe allow="fullscreen" allowfullscreen height="352" src="https://streamable.com/e/aq12xb?" width="640" style="border:none;"></iframe>
        </div>
         <div class="video-card">
         <iframe allow="fullscreen" allowfullscreen height="848" src="https://streamable.com/e/z1prtm?" width="464" style="border:none;"></iframe>
         </div>
         <div class="video-card">
         <iframe allow="fullscreen" allowfullscreen height="1280" src="https://streamable.com/e/ruvhfb?" width="720" style="border:none;"></iframe>
         </div>
         <div class="video-card">
         <iframe allow="fullscreen" allowfullscreen height="854" src="https://streamable.com/e/1d3fja?" width="480" style="border:none;"></iframe>
         </div>
         <div class="videos-card">
         <iframe allow="fullscreen" allowfullscreen height="624" src="https://streamable.com/e/h48lc3?" width="352" style="border:none;"></iframe>
         </div>
    </section>

    <section id="lockedVideos" style="margin-top: 3rem;">
      <h2>🔒 Locked Videos (₹100 each to Unlock)</h2>
      <div class="videos-grid">
        <!-- Video 1 -->
        <div class="locked-video" data-password="PASS123" data-video-src="ht">
          <img src="https://i.postimg.cc/DwLsWHNs/images.jpg" alt="Locked Video 1" title="Click to pay and unlock" />
          <div class="price">Price: ₹100</div>
          <button class="pay-btn">Pay ₹100 & Get Password</button>
          <input type="password" placeholder="Enter unlock password" aria-label="Password to unlock Video 1"/>
          <button class="submit-pass-btn">Unlock Video</button>
          <div id="unlockMsg"></div>
          <video controls></video>
        </div>

        <!-- Video 2 -->
        <div class="locked-video" data-password="PASS456" data-video-src="https://www.w3schools.com/html/movie.mp4#t=45,75">
          <img src="https://i.postimg.cc/DwLsWHNs/images.jpg" alt="Locked Video 2" title="Click to pay and unlock" />
          <div class="price">Price: ₹100</div>
          <button class="pay-btn">Pay ₹100 & Get Password</button>
          <input type="password" placeholder="Enter unlock password" aria-label="Password to unlock Video 2" />
          <button class="submit-pass-btn">Unlock Video</button>
          <div id="unlockMsg"></div>
          <video controls></video>
        </div>

        <!-- Video 3 -->
        <div class="locked-video" data-password="PASS789" data-video-src="https://interactive-examples.mdn.mozilla.net/media/cc0-videos/bee.webm#t=20,50">
          <img src="https://i.postimg.cc/DwLsWHNs/images.jpg" alt="Locked Video 3" title="Click to pay and unlock" />
          <div class="price">Price: ₹100</div>
          <button class="pay-btn">Pay ₹100 & Get Password</button>
          <input type="password" placeholder="Enter unlock password" aria-label="Password to unlock Video 3" />
          <button class="submit-pass-btn">Unlock Video</button>
          <div id="unlockMsg"></div>
          <video controls></video>
        </div>

        <!-- Video 4 -->
        <div class="locked-video" data-password="PASS000" data-video-src="https://interactive-examples.mdn.mozilla.net/media/cc0-videos/butterfly.webm#t=10,40">
          <img src="https://i.postimg.cc/DwLsWHNs/images.jpg" alt="Locked Video 4" title="Click to pay and unlock" />
          <div class="price">Price: ₹100</div>
          <button class="pay-btn">Pay ₹100 & Get Password</button>
          <input type="password" placeholder="Enter unlock password" aria-label="Password to unlock Video 4" />
          <button class="submit-pass-btn">Unlock Video</button>
          <div id="unlockMsg"></div>
          <video controls></video>
        </div>

        <!-- Video 5 -->
        <div class="locked-video" data-password="PASS555" data-video-src="https://interactive-examples.mdn.mozilla.net/media/cc0-videos/flower.webm#t=15,45">
          <img src="https://i.postimg.cc/DwLsWHNs/images.jpg" alt="Locked Video 5" title="Click to pay and unlock" />
          <div class="price">Price: ₹100</div>
          <button class="pay-btn">Pay ₹100 & Get Password</button>
          <input type="password" placeholder="Enter unlock password" aria-label="Password to unlock Video 5" />
          <button class="submit-pass-btn">Unlock Video</button>
          <div id="unlockMsg"></div>
          <video controls></video>
        </div>
        
          <!-- Video 6 -->
        <div class="locked-video" data-password="PASS555" data-video-src="https://interactive-examples.mdn.mozilla.net/media/cc0-videos/flower.webm#t=15,45">
          <img src="https://i.postimg.cc/DwLsWHNs/images.jpg" alt="Locked Video 5" title="Click to pay and unlock" />
          <div class="price">Price: ₹100</div>
          <button class="pay-btn">Pay ₹100 & Get Password</button>
          <input type="password" placeholder="Enter unlock password" aria-label="Password to unlock Video 5" />
          <button class="submit-pass-btn">Unlock Video</button>
          <div id="unlockMsg"></div>
          <video controls></video>
        </div>
        
 <!-- Video 7 -->
        <div class="locked-video" data-password="PASS555" data-video-src="https://interactive-examples.mdn.mozilla.net/media/cc0-videos/flower.webm#t=15,45">
          <img src="https://i.postimg.cc/DwLsWHNs/images.jpg" alt="Locked Video 5" title="Click to pay and unlock" />
          <div class="price">Price: ₹100</div>
          <button class="pay-btn">Pay ₹100 & Get Password</button>
          <input type="password" placeholder="Enter unlock password" aria-label="Password to unlock Video 5" />
          <button class="submit-pass-btn">Unlock Video</button>
          <div id="unlockMsg"></div>
          <video controls></video>
        </div>
        
 <!-- Video 8 -->
        <div class="locked-video" data-password="PASS555" data-video-src="https://interactive-examples.mdn.mozilla.net/media/cc0-videos/flower.webm#t=15,45">
          <img src="https://i.postimg.cc/DwLsWHNs/images.jpg" alt="Locked Video 5" title="Click to pay and unlock" />
          <div class="price">Price: ₹100</div>
          <button class="pay-btn">Pay ₹100 & Get Password</button>
          <input type="password" placeholder="Enter unlock password" aria-label="Password to unlock Video 5" />
          <button class="submit-pass-btn">Unlock Video</button>
          <div id="unlockMsg"></div>
          <video controls></video>
        </div>
      </div>
    </section>
  </main>

  <!-- Payment Modal -->
  <div id="paymentModal" role="dialog" aria-modal="true" aria-labelledby="paymentTitle" tabindex="-1">
    <div id="paymentContent">
      <h3 id="paymentTitle">Payment Instructions</h3>
      <p>To unlock this video, please pay ₹100 using UPI:</p>
      <p><strong>UPI ID:</strong> Dhamapayhere@fam</p>
      <img src="https://i.postimg.cc/fWpKxr4B/Screenshot-20250206-190148-Fam-App.jpg" alt="Scan QR code to pay" />
      <p>After payment, you will receive the unlock password via Telegram or email.</p>
      <div class="warning">
        ⚠️ Please send your <strong>payment screenshot</strong> to Telegram ID <strong>@sleepyspybot</strong> to receive the password for unlocking the video.
      </div>
      <button class="closeBtn" onclick="closePaymentModal()">Close</button>
    </div>
  </div>

  <script>
    // Show Payment Modal on pay-btn click
    document.querySelectorAll('.locked-video').forEach(lv => {
      const payBtn = lv.querySelector('.pay-btn');
      const submitBtn = lv.querySelector('.submit-pass-btn');
      const input = lv.querySelector('input[type="password"]');
      const unlockMsg = lv.querySelector('#unlockMsg');
      const videoElem = lv.querySelector('video');
      const imgElem = lv.querySelector('img');
      const priceElem = lv.querySelector('.price');

      payBtn.addEventListener('click', () => {
        // Show payment modal
        currentLockedVideo = lv; // save ref to this video
        showPaymentModal();
      });

      submitBtn.addEventListener('click', () => {
        const correctPassword = lv.getAttribute('data-password');
        const entered = input.value.trim();
        if (entered === '') {
          unlockMsg.style.color = '#ff5555';
          unlockMsg.textContent = 'Please enter a password.';
          return;
        }
        if (entered === correctPassword) {
          unlockMsg.style.color = '#4caf50';
          unlockMsg.textContent = 'Password correct! Enjoy your video.';
          videoElem.style.display = 'block';
          videoElem.src = lv.getAttribute('data-video-src');
          input.style.display = 'none';
          submitBtn.style.display = 'none';
          payBtn.style.display = 'none';
          priceElem.style.display = 'none';
          imgElem.style.display = 'none';
        } else {
          unlockMsg.style.color = '#ff5555';
          unlockMsg.textContent = 'Incorrect password. Please try again.';
        }
      });
    });

    // Payment Modal functions
    const paymentModal = document.getElementById('paymentModal');
    let currentLockedVideo = null;

    function showPaymentModal() {
      paymentModal.classList.add('active');
      paymentModal.focus();
    }
    function closePaymentModal() {
      paymentModal.classList.remove('active');
    }

    // Close modal on Escape key
    document.addEventListener('keydown', (e) => {
      if (e.key === 'Escape' && paymentModal.classList.contains('active')) {
        closePaymentModal();
      }
    });
  </script>
</body>
</html>
