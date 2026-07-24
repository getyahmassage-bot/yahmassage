# yahmassage<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />
<meta name="theme-color" content="#0a0a0a" />
<title>Yah Massage — Premium Home Service | Mumbai</title>
<meta name="description" content="Full massage service for females only at home. Mumbai & nearby areas. Starts at ₹399." />
<style>
  ,::before,*::after{box-sizing:border-box;margin:0;padding:0}
  html,body{height:100%;overflow-x:hidden}
  body{
    font-family:'Helvetica Neue',Arial,sans-serif;
    background:#0a0a0a;
    color:#fff;
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
    overflow-y:auto;
    position:relative;
  }
  a{color:inherit;text-decoration:none}
  button{font-family:inherit;cursor:pointer;border:none;background:none;color:inherit}

  /* RAIN CONTAINER */
  .rain-container{
    position:fixed;
    top:0;
    left:0;
    width:100%;
    height:100%;
    pointer-events:none;
    z-index:50;
    overflow:hidden;
  }
  .raindrop{
    position:absolute;
    width:2px;
    height:15px;
    background:linear-gradient(180deg, rgba(174, 194, 224, 0.6), rgba(174, 194, 224, 0.1));
    border-radius:0 0 2px 2px;
    animation:fall linear infinite;
    opacity:0.4;
  }
  @keyframes fall{
    0%{transform:translateY(-100px)}
    100%{transform:translateY(100vh)}
  }

  /* NAV */
  nav{
    position:fixed;top:0;left:0;right:0;
    padding:14px 20px;
    background:rgba(10,10,10,0.75);
    backdrop-filter:blur(14px);
    -webkit-backdrop-filter:blur(14px);
    z-index:100;
    display:flex;align-items:center;justify-content:space-between;
    border-bottom:1px solid rgba(255,255,255,0.08);
  }
  .logo{
    font-weight:700;
    font-size:26px;
    letter-spacing:1px;
  }
  .nav-links{display:flex;gap:6px;font-size:13px;font-weight:500}
  .nav-links button{
    color:#fff;opacity:0.7;transition:all .3s;
    padding:6px 10px;border-radius:20px;
  }
  .nav-links button:hover,.nav-links button.active{
    opacity:1;background:rgba(255,255,255,0.1);
  }

  /* PAGES */
  .page{
    min-height:100vh;
    padding:90px 22px 120px;
    display:none;
    position:relative;
    z-index:1;
    animation:pageIn .7s ease;
  }
  .page.active{display:block}
  @keyframes pageIn{
    from{opacity:0;transform:translateY(20px)}
    to{opacity:1;transform:translateY(0)}
  }

  /* ===== HERO WITH BACKGROUND IMAGE ===== */
  .hero{
    position:relative;
    text-align:center;
    padding:60px 20px 50px;
    border-radius:24px;
    overflow:hidden;
    margin-bottom:40px;
    background:
      linear-gradient(180deg, rgba(10,10,10,0.55) 0%, rgba(10,10,10,0.75) 50%, rgba(10,10,10,0.95) 100%),
      url('https://images.unsplash.com/photo-1544161515-4ab6ce6db874?w=1200&q=80') center/cover no-repeat;
    background-attachment: fixed;
    min-height: 520px;
    display:flex;
    flex-direction:column;
    align-items:center;
    justify-content:center;
    box-shadow:0 20px 60px rgba(0,0,0,0.5);
  }
  .hero::before{
    content:"";
    position:absolute;inset:0;
    background:radial-gradient(circle at 50% 30%, rgba(255,255,255,0.08), transparent 60%);
    pointer-events:none;
  }
  .hero-logo{
    font-size:120px;
    display:inline-block;
    animation:heroFloat 3s ease-in-out infinite;
    margin-bottom:16px;
    position:relative;
    z-index:2;
    filter:drop-shadow(0 10px 30px rgba(0,0,0,0.5));
  }
  @keyframes heroFloat{
    0%,100%{transform:translateY(0)}
    50%{transform:translateY(-15px)}
  }
  .hero h1{
    font-size:64px;
    font-weight:800;
    letter-spacing:-1px;
    margin-bottom:14px;
    background:linear-gradient(90deg,#fff,#e0e0e0,#fff);
    background-size:200% auto;
    -webkit-background-clip:text;
    background-clip:text;
    -webkit-text-fill-color:transparent;
    animation:shine 3s linear infinite;
    position:relative;
    z-index:2;
  }
  @keyframes shine{to{background-position:200% center}}
  .hero p.tagline{
    font-size:16px;
    opacity:0.9;
    margin-bottom:28px;
    letter-spacing:0.5px;
    position:relative;
    z-index:2;
    text-shadow:0 2px 10px rgba(0,0,0,0.6);
  }
  .price-badge{
    display:inline-block;
    padding:12px 26px;
    border:1px solid rgba(255,255,255,0.3);
    border-radius:50px;
    font-size:16px;
    font-weight:600;
    margin-bottom:28px;
    background:rgba(255,255,255,0.1);
    backdrop-filter:blur(10px);
    animation:pulseBadge 2s ease-in-out infinite;
    position:relative;
    z-index:2;
  }
  @keyframes pulseBadge{
    0%,100%{box-shadow:0 0 0 0 rgba(255,255,255,0.3)}
    50%{box-shadow:0 0 0 12px rgba(255,255,255,0)}
  }

  /* ========== MESSENGER-STYLE BOOK NOW BUTTON ========== */
  .messenger-btn{
    display:inline-flex;align-items:center;gap:10px;
    padding:18px 36px;
    background:linear-gradient(135deg, #0099FF 0%, #006AFF 50%, #A033FF 100%);
    color:#fff;
    border-radius:50px;
    font-weight:700;
    font-size:16px;
    letter-spacing:0.5px;
    transition:all .3s;
    box-shadow:0 10px 30px rgba(0, 132, 255, 0.4);
    position:relative;
    z-index:2;
    animation:btnFloat 3s ease-in-out infinite;
  }
  .messenger-btn:hover{
    transform:translateY(-3px) scale(1.05);
    box-shadow:0 15px 40px rgba(0, 132, 255, 0.6);
  }
  .messenger-btn:active{transform:scale(0.97)}
  .messenger-btn .msg-icon{
    width:26px;
    height:26px;
    fill:#fff;
  }
  @keyframes btnFloat{
    0%,100%{transform:translateY(0)}
    50%{transform:translateY(-4px)}
  }

  /* FEATURES */
  .features{
    display:grid;
    grid-template-columns:1fr;
    gap:14px;
    margin-top:20px;
  }
  .feature{
    padding:22px;
    border:1px solid rgba(255,255,255,0.1);
    border-radius:18px;
    background:rgba(255,255,255,0.02);
    transition:all .4s;
    animation:slideUp .6s ease backwards;
  }
  .feature:nth-child(1){animation-delay:.1s}
  .feature:nth-child(2){animation-delay:.2s}
  .feature:nth-child(3){animation-delay:.3s}
  .feature:nth-child(4){animation-delay:.4s}
  @keyframes slideUp{
    from{opacity:0;transform:translateY(30px)}
    to{opacity:1;transform:translateY(0)}
  }
  .feature:hover{
    border-color:rgba(255,255,255,0.3);
    transform:translateY(-4px);
    background:rgba(255,255,255,0.05);
  }
  .feature h3{font-size:16px;margin-bottom:6px;font-weight:600}
  .feature p{font-size:13px;opacity:0.65}

  /* SERVICES */
  .section-title{
    text-align:center;
    font-size:30px;
    font-weight:800;
    margin-bottom:10px;
    letter-spacing:-0.5px;
  }
  .section-sub{
    text-align:center;
    opacity:0.55;
    font-size:14px;
    margin-bottom:35px;
  }
  .service-card{
    padding:24px;
    border:1px solid rgba(255,255,255,0.1);
    border-radius:20px;
    margin-bottom:16px;
    background:linear-gradient(135deg,rgba(255,255,255,0.025),rgba(255,255,255,0.008));
    transition:all .4s;
    position:relative;
    overflow:hidden;
  }
  .service-card::before{
    content:"";
    position:absolute;top:-50%;left:-50%;
    width:200%;height:200%;
    background:linear-gradient(45deg,transparent,rgba(255,255,255,0.04),transparent);
    transform:translateX(-100%);
    transition:transform .8s;
  }
  .service-card:hover::before{transform:translateX(100%)}
  .service-card:hover{border-color:rgba(255,255,255,0.3);transform:translateY(-3px)}
  .service-head{display:flex;justify-content:space-between;align-items:center;margin-bottom:8px}
  .service-head h3{font-size:17px;font-weight:600}
  .service-head .price{font-size:18px;font-weight:700;opacity:0.9}
  .service-card p{font-size:13px;opacity:0.6}

  /* CONTACT */
  .contact-box{
    text-align:center;
    padding:40px 24px;
    border:1px solid rgba(255,255,255,0.12);
    border-radius:24px;
    background:rgba(255,255,255,0.02);
    margin-bottom:20px;
  }
  .contact-box h2{font-size:24px;margin-bottom:10px}
  .contact-box p{opacity:0.6;font-size:14px;margin-bottom:20px}
  .info-list{text-align:left;margin-top:24px}
  .info-list div{
    padding:14px 0;
    border-bottom:1px solid rgba(255,255,255,0.06);
    display:flex;align-items:center;gap:12px;
    font-size:14px;
  }
  .info-list div:last-child{border-bottom:none}

  /* ========== FB MESSENGER STYLE FLOATING BUTTON (RIGHT SIDE) ========== */
  .float-msg{
    position:fixed;
    bottom:24px;
    right:20px;
    z-index:99;
    display:flex;
    align-items:center;
    gap:10px;
    padding:14px 20px;
    border-radius:50px;
    background:linear-gradient(135deg, #0099FF 0%, #006AFF 50%, #A033FF 100%);
    color:#fff;
    font-weight:700;
    font-size:15px;
    box-shadow:
      0 8px 24px rgba(0, 132, 255, 0.5),
      0 2px 8px rgba(0, 0, 0, 0.3);
    animation:floatBtn 3s ease-in-out infinite;
    transition:transform .2s, box-shadow .3s;
  }
  .float-msg:hover{
    transform:translateY(-4px) scale(1.05);
    box-shadow:
      0 12px 32px rgba(0, 132, 255, 0.6),
      0 4px 12px rgba(0, 0, 0, 0.4);
  }
  .float-msg:active{
    transform:scale(0.95);
  }
  .float-msg .messenger-icon{
    width:28px;
    height:28px;
    fill:#fff;
    filter:drop-shadow(0 2px 4px rgba(0,0,0,0.2));
  }
  .float-msg::before{
    content:"";
    position:absolute;
    inset:-4px;
    border-radius:50px;
    background:linear-gradient(135deg, #0099FF, #A033FF);
    opacity:0.4;
    animation:ripple 2.2s ease-out infinite;
    z-index:-1;
  }
  @keyframes floatBtn{
    0%,100%{transform:translateY(0)}
    50%{transform:translateY(-6px)}
  }
  @keyframes ripple{
    0%{transform:scale(1);opacity:0.5}
    100%{transform:scale(1.4);opacity:0}
  }

  footer{
    text-align:center;
    padding:30px 20px 100px;
    opacity:0.4;
    font-size:12px;
    letter-spacing:0.5px;
  }

  @media(min-width:640px){
    .features{grid-template-columns:1fr 1fr}
    .hero h1{font-size:72px}
    .hero-logo{font-size:140px}
    .hero{min-height:580px}
  }
  @media(min-width:900px){
    .page{padding:110px 60px 140px;max-width:900px;margin:0 auto}
  }
  @media(max-width:480px){
    .float-msg{
      padding:12px 16px;
      font-size:14px;
      bottom:20px;
      right:16px;
    }
    .float-msg .messenger-icon{
      width:24px;
      height:24px;
    }
    .messenger-btn{
      padding:16px 28px;
      font-size:15px;
    }
    .logo{
      font-size:22px;
    }
    .hero h1{
      font-size:56px;
    }
    .hero-logo{
      font-size:100px;
    }
  }

  ::-webkit-scrollbar{width:6px}
  ::-webkit-scrollbar-track{background:#0a0a0a}
  ::-webkit-scrollbar-thumb{background:#333;border-radius:3px}
</style>
</head>
<body>

<!-- RAIN CONTAINER -->
<div class="rain-container" id="rainContainer"></div>

<!-- RAIN SOUND AUDIO -->
<audio id="rainSound" preload="auto">
  <source src="https://assets.mixkit.co/sfx/preview/mixkit-light-rain-loop-364.mp3" type="audio/mpeg">
</audio>

<!-- NAV -->
<nav>
  <div class="logo">Yah Massage</div>
  <div class="nav-links">
    <button data-page="services">Services</button>
    <button data-page="contact">Contact</button>
  </div>
</nav>

<!-- PAGE 1: HOME -->
<section class="page active" id="home">
  <div class="hero">
    <div class="hero-logo">💆‍♀️</div>
    <h1>Yah Massage</h1>
    <p class="tagline">महिलाओं के लिए घर पर मसाज सेवा<br>Mumbai &amp; nearby areas only</p>
    <div class="price-badge">Starts at just ₹399</div>
    <br>
    <a href="https://messenger.com/t/YahMassage" target="_blank" class="messenger-btn">
      <svg class="msg-icon" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
        <path d="M12 2C6.36 2 2 6.13 2 11.7c0 2.91 1.44 5.48 3.71 7.19v3.11l3.42-1.9c.9.25 1.86.39 2.87.39 5.64 0 10-4.13 10-9.7S17.64 2 12 2zm1.01 12.47l-2.55-2.72-4.97 2.72 5.47-5.81 2.61 2.72 4.91-2.72-5.47 5.81z"/>
      </svg>
      <span>CHAT ON MESSENGER</span>
    </a>
  </div>

  <div class="features">
    <div class="feature">
      <h3>At Your Doorstep</h3>
      <p>Professional service in the comfort of your home</p>
    </div>
    <div class="feature">
      <h3>Females Only</h3>
      <p>Safe, private &amp; exclusively for women</p>
    </div>
    <div class="feature">
      <h3>Full Body Massage</h3>
      <p>Relax, unwind &amp; rejuvenate every muscle</p>
    </div>
    <div class="feature">
      <h3>Mumbai &amp; Nearby</h3>
      <p>Serving Mumbai city + nearest areas</p>
    </div>
  </div>

  <footer>© 2026 Yah Massage • made in ❤️ with mumbai</footer>
</section>

<!-- PAGE 2: SERVICES -->
<section class="page" id="services">
  <h2 class="section-title">Our Services</h2>
  <p class="section-sub">All services at your home • Females only</p>

  <div class="service-card">
    <div class="service-head">
      <h3>Full Body Massage</h3>
      <span class="price">₹399</span>
    </div>
    <p>Complete relaxation therapy — head to toe</p>
  </div>

  <div class="service-card">
    <div class="service-head">
      <h3>Oil Massage</h3>
      <span class="price">₹499</span>
    </div>
    <p>Premium aromatic oils for deep nourishment</p>
  </div>

  <div class="service-card">
    <div class="service-head">
      <h3>Premium Spa</h3>
      <span class="price">₹799</span>
    </div>
    <p>Luxury spa experience at your home</p>
  </div>

  <div class="service-card">
    <div class="service-head">
      <h3>Couple Package</h3>
      <span class="price">₹1299</span>
    </div>
    <p>Special package for her &amp; her loved one</p>
  </div>

  <div style="text-align:center;margin-top:30px">
    <a href="https://messenger.com/t/YahMassage" target="_blank" class="messenger-btn">
      <svg class="msg-icon" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
        <path d="M12 2C6.36 2 2 6.13 2 11.7c0 2.91 1.44 5.48 3.71 7.19v3.11l3.42-1.9c.9.25 1.86.39 2.87.39 5.64 0 10-4.13 10-9.7S17.64 2 12 2zm1.01 12.47l-2.55-2.72-4.97 2.72 5.47-5.81 2.61 2.72 4.91-2.72-5.47 5.81z"/>
      </svg>
      <span>CHAT ON MESSENGER</span>
    </a>
  </div>

  <footer>Mumbai &amp; nearby areas only • Prices may vary by location</footer>
</section>

<!-- PAGE 3: CONTACT -->
<section class="page" id="contact">
  <h2 class="section-title">Get in Touch</h2>
  <p class="section-sub">We'd love to hear from you</p>

  <div class="contact-box">
    <h2>Chat with us on Messenger</h2>
    <p>Send a message to book your session or ask anything</p>
    <a href="https://messenger.com/t/YahMassage" target="_blank" class="messenger-btn">
      <svg class="msg-icon" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
        <path d="M12 2C6.36 2 2 6.13 2 11.7c0 2.91 1.44 5.48 3.71 7.19v3.11l3.42-1.9c.9.25 1.86.39 2.87.39 5.64 0 10-4.13 10-9.7S17.64 2 12 2zm1.01 12.47l-2.55-2.72-4.97 2.72 5.47-5.81 2.61 2.72 4.91-2.72-5.47 5.81z"/>
      </svg>
      <span>CHAT ON MESSENGER</span>
    </a>

    <div class="info-list">
      <div>Mumbai &amp; nearest areas</div>
      <div>Service for females only</div>
      <div>Starting at ₹399</div>
      <div>Available 9 AM – 9 PM</div>
      <div>Home service only</div>
    </div>
  </div>

  <footer>© 2026 Yah Massage • made in ❤️ with mumbai</footer>
</section>

<!-- FB MESSENGER STYLE FLOATING BUTTON (RIGHT SIDE) -->
<a href="https://messenger.com/t/YahMassage" target="_blank" class="float-msg" aria-label="Chat on Messenger">
  <svg class="messenger-icon" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
    <path d="M12 2C6.36 2 2 6.13 2 11.7c0 2.91 1.44 5.48 3.71 7.19v3.11l3.42-1.9c.9.25 1.86.39 2.87.39 5.64 0 10-4.13 10-9.7S17.64 2 12 2zm1.01 12.47l-2.55-2.72-4.97 2.72 5.47-5.81 2.61 2.72 4.91-2.72-5.47 5.81z"/>
  </svg>
  <span>CHAT NOW</span>
</a>

<script>
/* ========== RAIN EFFECT ========== */
function createRain(){
  const container = document.getElementById('rainContainer');
  const dropCount = 40;
  
  for(let i = 0; i < dropCount; i++){
    const drop = document.createElement('div');
    drop.className = 'raindrop';
    
    const left = Math.random() * 100;
    const delay = Math.random() * 3;
    const duration = 0.8 + Math.random() * 0.7;
    const opacity = 0.2 + Math.random() * 0.4;
    
    drop.style.left = left + '%';
    drop.style.animationDelay = delay + 's';
    drop.style.animationDuration = duration + 's';
    drop.style.opacity = opacity;
    
    container.appendChild(drop);
  }
}
createRain();

/* ========== RAIN SOUND AFTER 5 SECONDS FOR 5 SECONDS ========== */
setTimeout(() => {
  const rainAudio = document.getElementById('rainSound');
  if(rainAudio){
    rainAudio.volume = 0.4; 
    rainAudio.play().catch(e => console.log('Audio play failed:', e));
    
    setTimeout(() => {
      rainAudio.pause();
      rainAudio.currentTime = 0; 
    }, 5000);
  }
}, 5000);

/* PAGE NAVIGATION */
const pages = document.querySelectorAll('.page');
const navBtns = document.querySelectorAll('.nav-links button');
navBtns.forEach(btn=>{
  btn.addEventListener('click',()=>{
    const target = btn.dataset.page;
    pages.forEach(p=>p.classList.toggle('active', p.id===target));
    navBtns.forEach(b=>b.classList.toggle('active', b===btn));
    window.scrollTo({top:0,behavior:'smooth'});
  });
});

/* HAPTIC VIBRATION - AUTOMATIC ON FIRST SCROLL, 2 SECONDS ONLY */
let vibrated = false;

function onScroll(){
  if(vibrated) return;
  vibrated = true;
  
  if(navigator.vibrate){
    navigator.vibrate(2000);
  }
  
  document.body.style.animation = 'shake .5s';
  setTimeout(()=>document.body.style.animation='', 500);
}

window.addEventListener('scroll', onScroll, {passive:true, once:true});

const shakeStyle = document.createElement('style');
shakeStyle.textContent = `
@keyframes shake{
  0%,100%{transform:translateX(0)}
  20%{transform:translateX(-6px)}
  40%{transform:translateX(6px)}
  60%{transform:translateX(-4px)}
  80%{transform:translateX(4px)}
}`;
document.head.appendChild(shakeStyle);
</script>
</body>
</html>
