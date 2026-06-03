[index (2).html](https://github.com/user-attachments/files/28531299/index.2.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Task Hawk — Building the Future of Service Operations</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Barlow+Condensed:ital,wght@0,200;0,300;0,400;0,500;0,600;1,300&family=Barlow:wght@300;400&display=swap" rel="stylesheet">
<style>
*,*::before,*::after{margin:0;padding:0;box-sizing:border-box}
:root{
  --bg:#080808;
  --surface:#0f0f0f;
  --border:rgba(255,255,255,0.07);
  --border-md:rgba(255,255,255,0.12);
  --tp:#f0f0f0;
  --ts:#a8a8a8;
  --tt:#686868;
}
html{scroll-behavior:smooth}
body{background:var(--bg);color:var(--tp);font-family:'Barlow',sans-serif;font-weight:300;overflow-x:hidden}

/* DOT GRID */
body::before{
  content:'';position:fixed;inset:0;
  background-image:radial-gradient(circle,rgba(255,255,255,0.055) 1px,transparent 1px);
  background-size:28px 28px;pointer-events:none;z-index:0
}

/* NAV */
nav{
  position:fixed;top:0;left:0;right:0;height:60px;
  display:flex;align-items:center;justify-content:space-between;
  padding:0 52px;
  border-bottom:0.5px solid var(--border);
  background:rgba(8,8,8,0.88);
  backdrop-filter:blur(12px);
  -webkit-backdrop-filter:blur(12px);
  z-index:200
}
.nav-left{display:flex;align-items:center;gap:12px}
.nav-logo-img{height:22px;width:auto;mix-blend-mode:screen;opacity:0.9}
.nav-word{
  font-family:'Bebas Neue',sans-serif;font-size:19px;
  letter-spacing:0.15em;color:var(--tp)
}
.nav-sep{width:0.5px;height:18px;background:var(--border-md);margin:0 4px}
.nav-tag{
  font-family:'Barlow Condensed',sans-serif;font-size:10px;
  letter-spacing:0.3em;text-transform:uppercase;color:var(--ts)
}
.nav-right{display:flex;align-items:center;gap:36px}
.nav-link{
  font-family:'Barlow Condensed',sans-serif;font-size:11px;
  letter-spacing:0.25em;text-transform:uppercase;color:var(--ts);
  text-decoration:none;transition:color .2s
}
.nav-link:hover{color:var(--tp)}
.nav-btn{
  font-family:'Barlow Condensed',sans-serif;font-size:11px;
  letter-spacing:0.22em;text-transform:uppercase;
  color:var(--tp);border:0.5px solid var(--border-md);
  padding:8px 20px;text-decoration:none;
  transition:background .2s,border-color .2s
}
.nav-btn:hover{background:rgba(255,255,255,0.06);border-color:rgba(255,255,255,0.25)}

/* HERO */
#hero{
  min-height:100vh;display:grid;
  grid-template-columns:1fr 1fr;
  align-items:center;
  padding:100px 52px 80px;
  position:relative;z-index:1;gap:40px
}
.hero-left{display:flex;flex-direction:column;justify-content:center}
.hero-status{
  display:inline-flex;align-items:center;gap:10px;
  font-family:'Barlow Condensed',sans-serif;font-size:10px;
  letter-spacing:0.35em;text-transform:uppercase;color:var(--tt);
  margin-bottom:48px
}
.status-dot{
  width:5px;height:5px;border-radius:50%;background:rgba(255,255,255,0.3);
  animation:pulse 2.5s ease-in-out infinite
}
@keyframes pulse{0%,100%{opacity:.3}50%{opacity:1}}
.hero-eyebrow{
  font-family:'Barlow Condensed',sans-serif;font-size:11px;
  letter-spacing:0.4em;text-transform:uppercase;color:var(--tt);
  margin-bottom:20px
}
.hero-title{
  font-family:'Bebas Neue',sans-serif;
  font-size:clamp(72px,9vw,128px);
  line-height:.88;color:var(--tp);
  letter-spacing:0.02em;margin-bottom:32px
}
.hero-tagline{
  font-family:'Barlow Condensed',sans-serif;font-size:clamp(16px,1.8vw,22px);
  font-weight:300;color:var(--ts);letter-spacing:0.12em;
  text-transform:uppercase;margin-bottom:20px;
  border-left:1px solid var(--border-md);padding-left:16px
}
.hero-desc{
  font-size:15px;font-weight:300;color:var(--ts);
  line-height:1.75;max-width:440px;margin-bottom:48px
}
.hero-actions{display:flex;align-items:center;gap:20px;flex-wrap:wrap}
.btn-primary{
  font-family:'Barlow Condensed',sans-serif;font-size:12px;
  letter-spacing:0.28em;text-transform:uppercase;
  color:#080808;background:#f0f0f0;
  padding:14px 32px;border:none;cursor:pointer;
  text-decoration:none;display:inline-block;
  transition:background .2s
}
.btn-primary:hover{background:#cecece}
.btn-ghost{
  font-family:'Barlow Condensed',sans-serif;font-size:12px;
  letter-spacing:0.28em;text-transform:uppercase;
  color:var(--ts);text-decoration:none;
  display:inline-flex;align-items:center;gap:8px;
  transition:color .2s
}
.btn-ghost:hover{color:var(--tp)}

/* HERO RIGHT — large logo mark */
.hero-right{
  display:flex;align-items:center;justify-content:center;
  position:relative
}
.hero-logo-wrap{position:relative}
.hero-logo-bg{
  position:absolute;inset:-60px;
  background:radial-gradient(ellipse at center,rgba(255,255,255,0.025) 0%,transparent 70%);
  pointer-events:none
}
.hero-logo-img{
  width:min(380px,38vw);height:auto;
  mix-blend-mode:screen;
  opacity:0.85;
  display:block
}

/* STATS */
.stats-row{
  display:flex;gap:48px;
  padding-top:48px;margin-top:48px;
  border-top:0.5px solid var(--border);
}
.stat-item{}
.stat-val{
  font-family:'Bebas Neue',sans-serif;font-size:36px;
  color:var(--tp);letter-spacing:0.05em;line-height:1
}
.stat-lbl{
  font-family:'Barlow Condensed',sans-serif;font-size:10px;
  letter-spacing:0.3em;text-transform:uppercase;color:var(--tt);
  margin-top:4px
}

/* SECTION COMMON */
.section-eyebrow{
  font-family:'Barlow Condensed',sans-serif;font-size:10px;
  letter-spacing:0.45em;text-transform:uppercase;color:var(--tt);
  margin-bottom:16px
}
.section-title{
  font-family:'Bebas Neue',sans-serif;
  font-size:clamp(52px,7vw,96px);
  line-height:.88;color:var(--tp);
  letter-spacing:0.02em
}

/* FEATURES */
#features{
  padding:120px 52px;
  position:relative;z-index:1;
  border-top:0.5px solid var(--border)
}
.features-header{margin-bottom:72px}
.features-grid{
  display:grid;grid-template-columns:repeat(2,1fr);
  gap:0;border:0.5px solid var(--border)
}
.feat{
  padding:52px 48px;
  border:0.5px solid var(--border);
  position:relative;
  transition:background .3s
}
.feat:hover{background:rgba(255,255,255,0.02)}
/* corner accent top-left */
.feat::before{
  content:'';position:absolute;top:0;left:0;
  width:24px;height:24px;
  border-top:1px solid rgba(255,255,255,0.18);
  border-left:1px solid rgba(255,255,255,0.18)
}
.feat-num{
  font-family:'Bebas Neue',sans-serif;font-size:11px;
  letter-spacing:0.45em;color:var(--tt);
  margin-bottom:36px;display:block
}
.feat-title{
  font-family:'Bebas Neue',sans-serif;font-size:40px;
  letter-spacing:0.03em;color:var(--tp);
  line-height:.95;margin-bottom:20px
}
.feat-desc{
  font-size:14px;font-weight:300;color:var(--ts);
  line-height:1.75;max-width:380px
}

/* CONTACT */
#contact{
  padding:120px 52px;
  border-top:0.5px solid var(--border);
  position:relative;z-index:1;
  display:grid;grid-template-columns:1fr 1fr;
  gap:80px;align-items:start
}
.contact-left{}
.contact-desc{
  font-size:15px;font-weight:300;color:var(--ts);
  line-height:1.75;max-width:400px;margin-top:24px
}
.contact-right{padding-top:60px}
.contact-entry{
  display:flex;flex-direction:column;gap:6px;
  padding:32px 0;border-bottom:0.5px solid var(--border);
}
.contact-entry:first-child{border-top:0.5px solid var(--border)}
.c-label{
  font-family:'Barlow Condensed',sans-serif;font-size:10px;
  letter-spacing:0.4em;text-transform:uppercase;color:var(--tt)
}
.c-val{
  font-family:'Barlow Condensed',sans-serif;font-size:22px;
  letter-spacing:0.05em;color:var(--ts);
  text-decoration:none;
  transition:color .2s
}
.c-val:hover{color:var(--tp)}

/* FOOTER */
footer{
  padding:28px 52px;
  border-top:0.5px solid var(--border);
  display:flex;justify-content:space-between;align-items:center;
  position:relative;z-index:1
}
.footer-left{display:flex;align-items:center;gap:10px}
.footer-logo{height:16px;mix-blend-mode:screen;opacity:0.5}
.footer-word{
  font-family:'Bebas Neue',sans-serif;font-size:15px;
  letter-spacing:0.15em;color:var(--tt)
}
.footer-copy{
  font-family:'Barlow Condensed',sans-serif;font-size:10px;
  letter-spacing:0.25em;text-transform:uppercase;color:var(--tt)
}

/* SCROLL FADE */
.reveal{
  opacity:0;transform:translateY(24px);
  transition:opacity .9s ease,transform .9s ease
}
.reveal.in{opacity:1;transform:translateY(0)}
.reveal-delay-1{transition-delay:.1s}
.reveal-delay-2{transition-delay:.2s}
.reveal-delay-3{transition-delay:.3s}
.reveal-delay-4{transition-delay:.4s}
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-left">
    <img class="nav-logo-img" src="data:image/png;base64,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" alt="TH">
    <div class="nav-sep"></div>
    <span class="nav-word">TASK HAWK</span>
    <div class="nav-sep"></div>
    <span class="nav-tag">Automotive SaaS</span>
  </div>
  <div class="nav-right">
    <a href="#features" class="nav-link">Capabilities</a>
    <a href="#contact" class="nav-link">Contact</a>
    <a href="#contact" class="nav-btn">Request Access →</a>
  </div>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-left">
    <div class="hero-status">
      <div class="status-dot"></div>
      Platform in Development &nbsp;·&nbsp; Est. 2026
    </div>

    <p class="hero-eyebrow">Automotive Service Technology</p>

    <h1 class="hero-title">TASK<br>HAWK</h1>

    <p class="hero-tagline">Building the Future of Service Operations</p>

    <p class="hero-desc">
      A SaaS platform engineered to modernize automotive service centers — eliminating inefficiency, digitizing repair orders, and giving operators real-time visibility into every job on the floor.
    </p>

    <div class="hero-actions">
      <a href="#contact" class="btn-primary">Request Early Access</a>
      <a href="#features" class="btn-ghost">View Capabilities →</a>
    </div>

    <div class="stats-row">
      <div class="stat-item">
        <div class="stat-val">$10B+</div>
        <div class="stat-lbl">Total Addressable Market</div>
      </div>
      <div class="stat-item">
        <div class="stat-val">25%+</div>
        <div class="stat-lbl">Admin Overhead Reduction</div>
      </div>
      <div class="stat-item">
        <div class="stat-val">30+</div>
        <div class="stat-lbl">Prototype Iterations</div>
      </div>
    </div>
  </div>

  <div class="hero-right">
    <div class="hero-logo-wrap">
      <div class="hero-logo-bg"></div>
      <img class="hero-logo-img" src="data:image/png;base64,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AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAP//Z" alt="Task Hawk">
    </div>
  </div>
</section>

<!-- FEATURES -->
<section id="features">
  <div class="features-header">
    <p class="section-eyebrow reveal">Platform Capabilities</p>
    <h2 class="section-title reveal reveal-delay-1">BUILT FOR<br>PERFORMANCE</h2>
  </div>

  <div class="features-grid">
    <div class="feat reveal">
      <span class="feat-num">01 / CORE</span>
      <h3 class="feat-title">Repair Order Management</h3>
      <p class="feat-desc">Digital repair orders that eliminate paper, reduce error rates, and create a centralized record of every service transaction across your shop floor.</p>
    </div>
    <div class="feat reveal reveal-delay-1">
      <span class="feat-num">02 / VISIBILITY</span>
      <h3 class="feat-title">Service Tracking</h3>
      <p class="feat-desc">Real-time visibility into every vehicle — from intake to delivery. Know exactly where each job stands, which bay it's in, and when it's ready.</p>
    </div>
    <div class="feat reveal reveal-delay-2">
      <span class="feat-num">03 / INTELLIGENCE</span>
      <h3 class="feat-title">Workflow Automation</h3>
      <p class="feat-desc">Intelligent task routing assigns the right technician to the right job automatically — cutting wait times and maximizing floor throughput.</p>
    </div>
    <div class="feat reveal reveal-delay-3">
      <span class="feat-num">04 / INSIGHT</span>
      <h3 class="feat-title">Analytics</h3>
      <p class="feat-desc">Data-driven intelligence on shop performance, technician efficiency, and revenue metrics — giving operators the visibility to make smarter decisions, faster.</p>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="contact-left">
    <p class="section-eyebrow reveal">Connect</p>
    <h2 class="section-title reveal reveal-delay-1">GET IN<br>TOUCH</h2>
    <p class="contact-desc reveal reveal-delay-2">
      Interested in early access, a partnership, or just want to discuss the platform? Reach out directly — always open to the right conversation.
    </p>
  </div>
  <div class="contact-right reveal reveal-delay-1">
    <div class="contact-entry">
      <span class="c-label">Email</span>
      <a href="mailto:dylanjennings06@gmail.com" class="c-val">dylanjennings06@gmail.com</a>
    </div>
    <div class="contact-entry">
      <span class="c-label">LinkedIn</span>
      <a href="https://www.linkedin.com/in/dylan-m-jennings" target="_blank" class="c-val">linkedin.com/in/dylan-m-jennings</a>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-left">
    <img class="footer-logo" src="data:image/png;base64,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" alt="TH">
    <span class="footer-word">TASK HAWK</span>
  </div>
  <p class="footer-copy">© 2026 Task Hawk · All Rights Reserved</p>
</footer>

<script>
const observer = new IntersectionObserver(entries => {
  entries.forEach(e => { if(e.isIntersecting) e.target.classList.add('in') });
},{threshold:0.12});
document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
</script>
</body>
</html>
