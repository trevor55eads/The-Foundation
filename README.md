<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>The Foundation — University of Kentucky</title>
<meta name="description" content="The Foundation is an invite-only accountability brotherhood for University of Kentucky men — weekly pods, faith, workouts, and speaker events.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,500;0,600;0,700;1,400;1,500&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --navy: #0a1f44;
    --navy-deep: #061530;
    --white: #ffffff;
    --off-white: #f6f4ee;
    --gold: #b08d2a;
    --gold-light: #d8ccae;
    --ink: #16233f;
    --line: rgba(10,31,68,0.12);
    --max: 1080px;
  }
  *{box-sizing:border-box;margin:0;padding:0;}
  html{scroll-behavior:smooth;overflow-x:hidden;}
  body{
    font-family:'Inter', -apple-system, sans-serif;
    color:var(--ink);
    background:var(--white);
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
    overflow-x:hidden;
    width:100%;
  }
  h1,h2,h3{font-family:'Playfair Display', Georgia, serif;letter-spacing:-0.01em;}
  a{color:inherit;text-decoration:none;}
  img{max-width:100%;display:block;}
  .wrap{max-width:var(--max);margin:0 auto;padding:0 28px;}

  /* ---------- Nav ---------- */
  .nav{
    position:sticky;top:0;z-index:50;
    background:var(--navy);
    border-bottom:1px solid rgba(255,255,255,0.08);
  }
  .nav .wrap{
    display:flex;align-items:center;justify-content:space-between;
    height:64px;
  }
  .nav-mark{
    display:flex;align-items:center;gap:10px;
    color:var(--white);font-weight:600;font-size:15px;letter-spacing:0.06em;
    text-transform:uppercase;
  }
  .nav-mark .rule{width:1px;height:16px;background:var(--gold);}
  .nav-links{display:flex;gap:32px;list-style:none;}
  .nav-links li + li{margin-left:32px;}
  .nav-links{gap:0;}
  .nav-links span{
    color:rgba(255,255,255,0.72);font-size:13px;font-weight:500;
    letter-spacing:0.03em;text-transform:uppercase;
  }
  .nav-cta{
    background:var(--gold);color:var(--navy-deep);
    padding:9px 18px;border-radius:2px;font-size:12.5px;font-weight:700;
    letter-spacing:0.04em;text-transform:uppercase;
    transition:opacity 0.2s ease;
  }
  .nav-cta:hover{opacity:0.85;}
  .nav-toggle{display:none;background:none;border:none;color:var(--white);font-size:24px;cursor:pointer;}

  /* ---------- Hero ---------- */
  .hero{
    background:
      radial-gradient(ellipse 900px 500px at 15% -10%, rgba(176,141,42,0.14), transparent 60%),
      radial-gradient(ellipse 700px 500px at 100% 0%, rgba(255,255,255,0.05), transparent 55%),
      linear-gradient(180deg, var(--navy) 0%, var(--navy-deep) 100%);
    color:var(--white);
    padding:110px 0 100px;
    position:relative;
    overflow:hidden;
  }
  .hero::after{
    content:"";position:absolute;left:0;right:0;bottom:0;height:1px;
    background:linear-gradient(90deg, transparent, var(--gold), transparent);
    opacity:0.5;
  }
  .hero-eyebrow{
    display:flex;align-items:center;gap:10px;
    font-size:12.5px;letter-spacing:0.14em;text-transform:uppercase;
    color:var(--gold-light);font-weight:600;margin-bottom:26px;
  }
  .hero-eyebrow .dot{width:5px;height:5px;background:var(--gold);border-radius:50%;}
  .hero h1{
    font-size:clamp(48px, 8vw, 84px);
    font-weight:600;line-height:0.98;
    max-width:780px;
    margin-bottom:26px;
  }
  .hero h1 em{font-style:italic;font-weight:400;color:var(--gold-light);}
  .hero p{
    font-size:clamp(16px, 2vw, 19px);
    color:rgba(255,255,255,0.78);
    max-width:560px;
    margin-bottom:42px;
    font-weight:400;
  }
  .hero-actions{display:flex;gap:16px;flex-wrap:wrap;align-items:center;}
  .btn-primary{
    background:var(--gold);color:var(--navy-deep);
    padding:15px 30px;border-radius:2px;
    font-size:13.5px;font-weight:700;letter-spacing:0.04em;text-transform:uppercase;
    transition:transform 0.2s ease, opacity 0.2s ease;
    display:inline-block;
  }
  .btn-primary:hover{transform:translateY(-1px);opacity:0.92;}
  .btn-ghost{
    color:var(--white);padding:15px 6px;
    font-size:13.5px;font-weight:600;letter-spacing:0.04em;text-transform:uppercase;
    border-bottom:1px solid rgba(255,255,255,0.35);
    transition:border-color 0.2s ease;
  }
  .btn-ghost:hover{border-color:var(--gold);}

  /* ---------- Section shared ---------- */
  section{padding:96px 0;}
  .eyebrow{
    display:flex;align-items:center;gap:10px;
    font-size:12px;letter-spacing:0.13em;text-transform:uppercase;
    color:var(--gold);font-weight:700;margin-bottom:18px;
  }
  .eyebrow .stem{width:22px;height:1px;background:var(--gold);}
  .section-title{
    font-size:clamp(30px, 4vw, 42px);
    font-weight:600;color:var(--navy);
    max-width:640px;
    margin-bottom:20px;
  }
  .section-lede{
    font-size:17px;color:#4a5573;max-width:600px;
  }

  /* ---------- Intro ---------- */
  .intro{background:var(--white);}
  .intro-grid{
    display:grid;grid-template-columns:1fr 1fr;gap:64px;align-items:start;
  }
  .intro-mission p{
    font-size:18px;line-height:1.75;color:#37426b;margin-bottom:18px;
  }
  .intro-mission p:last-child{margin-bottom:0;}
  .intro-mission strong{color:var(--navy);font-weight:600;}

  /* ---------- How it works cards ---------- */
  .how{background:var(--off-white);}
  .card-grid{
    display:grid;grid-template-columns:repeat(3, 1fr);gap:2px;
    margin-top:56px;
    background:var(--line);
    border:1px solid var(--line);
  }
  .card{
    background:var(--white);
    padding:44px 34px;
  }
  .card-icon{
    width:44px;height:44px;margin-bottom:26px;
    display:flex;align-items:center;justify-content:center;
  }
  .card-icon svg{width:100%;height:100%;}
  .card h3{
    font-size:22px;font-weight:600;color:var(--navy);margin-bottom:12px;
  }
  .card p{font-size:15px;color:#4a5573;line-height:1.7;}
  .card .cadence{
    display:inline-block;margin-top:18px;
    font-size:11px;letter-spacing:0.12em;text-transform:uppercase;
    color:var(--gold);font-weight:700;
    border-top:1px solid var(--line);padding-top:14px;width:100%;
  }
  .leadership-note{
    margin-top:2px;
    background:var(--navy);
    padding:30px 34px;
    border-left:3px solid var(--gold);
  }
  .leadership-note p{
    color:rgba(255,255,255,0.88);font-size:15px;line-height:1.7;max-width:720px;
  }
  .leadership-note strong{color:var(--gold-light);}

  /* ---------- Pillars ---------- */
  .pillars{background:var(--white);}
  .pillar-grid{
    display:grid;grid-template-columns:repeat(3, 1fr);gap:40px 36px;
    margin-top:48px;
  }
  .pillar-icon{
    width:40px;height:40px;margin-bottom:20px;
  }
  .pillar-icon svg{width:100%;height:100%;}
  .pillar h3{font-size:20px;font-weight:600;color:var(--navy);margin-bottom:10px;}
  .pillar p{font-size:14.5px;color:#4a5573;line-height:1.7;}

  /* ---------- Train banner (text-only) ---------- */
  .train-banner{
    background:var(--navy-deep);
    padding:88px 0;
    text-align:center;
  }
  .train-banner .wrap{max-width:640px;}
  .train-banner .eyebrow{color:var(--gold-light);justify-content:center;}
  .train-banner .eyebrow .stem{background:var(--gold-light);}
  .train-banner h2{
    font-size:clamp(28px, 3.4vw, 38px);color:var(--white);margin-bottom:20px;font-weight:600;
  }
  .train-banner p{
    color:rgba(255,255,255,0.75);font-size:16px;line-height:1.75;
  }

  /* ---------- Sign up ---------- */
  .signup{
    background:var(--white);
    text-align:center;
    padding:80px 0;
  }
  .signup .wrap{max-width:520px;}
  .signup .eyebrow{justify-content:center;}
  .signup .eyebrow .stem{display:none;}
  .signup h2{font-size:clamp(30px, 4vw, 42px);color:var(--navy);margin-bottom:16px;}
  .signup p{font-size:16px;color:#4a5573;margin-bottom:32px;}
  .btn-navy{
    background:var(--navy);color:var(--white);
    padding:14px 30px;border-radius:2px;
    font-size:13.5px;font-weight:700;letter-spacing:0.04em;text-transform:uppercase;
    transition:opacity 0.2s ease;
  }
  .btn-navy:hover{opacity:0.85;}
  .ig-btn{
    display:inline-flex;align-items:center;gap:9px;
  }
  .subscribe-form{
    display:flex;gap:10px;justify-content:center;flex-wrap:wrap;
    max-width:420px;margin:36px auto 0;
  }
  .subscribe-form input{
    flex:1;min-width:200px;
    border:1px solid var(--line);border-radius:2px;
    padding:13px 16px;font-size:14px;font-family:'Inter',sans-serif;
    color:var(--ink);background:var(--off-white);
  }
  .subscribe-form input:focus{outline:2px solid var(--gold);outline-offset:1px;}
  .subscribe-form button{
    background:var(--gold);color:var(--navy-deep);border:none;border-radius:2px;
    padding:13px 24px;font-size:13px;font-weight:700;letter-spacing:0.03em;text-transform:uppercase;
    cursor:pointer;transition:opacity 0.2s ease;
  }
  .subscribe-form button:hover{opacity:0.85;}
  .signup-note{
    margin-top:18px;font-size:13px;color:#8a92ab;
  }
  .contact-emails{
    display:flex;gap:12px;justify-content:center;flex-wrap:wrap;
    align-items:center;margin-top:32px;
  }
  .contact-emails span:not(.contact-divider){
    font-size:15px;font-weight:600;color:var(--navy);
  }
  .contact-divider{color:#c3c9d9;}
  @media (max-width:480px){
    .contact-emails{flex-direction:column;gap:8px;}
    .contact-divider{display:none;}
  }

  /* ---------- Footer ---------- */
  footer{
    background:var(--navy-deep);color:rgba(255,255,255,0.6);
    padding:44px 0;
  }
  footer .wrap{
    display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:16px;
  }
  .footer-brand{color:var(--white);font-weight:600;font-size:14px;letter-spacing:0.08em;}
  .footer-tag{color:var(--gold);font-size:11px;letter-spacing:0.12em;font-weight:700;margin-top:4px;}
  .footer-meta{font-size:12.5px;text-align:right;line-height:1.6;}

  /* ---------- Responsive ---------- */
  @media (max-width:860px){
    .nav-links{display:none;}
    .intro-grid{grid-template-columns:1fr;gap:36px;}
    .card-grid{grid-template-columns:1fr;}
    .pillar-grid{grid-template-columns:repeat(2, 1fr);gap:32px;}
    section{padding:64px 0;}
    footer .wrap{flex-direction:column;align-items:flex-start;text-align:left;}
    .footer-meta{text-align:left;}
  }
  @media (max-width:520px){
    .pillar-grid{grid-template-columns:1fr;}
  }

  /* ---------- Print / PDF safety ---------- */
  @media print{
    .nav{position:static;}
    section, header, footer, .card-grid, .pillar-grid, .leadership-note{
      break-inside:avoid;page-break-inside:avoid;
    }
    section{padding:48px 0;}
  }
</style>
</head>
<body>

<nav class="nav">
  <div class="wrap">
    <div class="nav-mark">THE<span class="rule"></span>FOUNDATION</div>
  </div>
</nav>

<header class="hero" id="top">
  <div class="wrap">
    <div class="hero-eyebrow"><span class="dot"></span>University of Kentucky · Invite Only</div>
    <h1>Every strong man<br>needs a <em>foundation.</em></h1>
    <p>An accountability brotherhood built on faith, discipline, and brothers who won't let you drift. Weekly pods, weekly workouts, and a brotherhood that shows up.</p>
  </div>
</header>

<section class="intro">
  <div class="wrap">
    <div class="intro-grid">
      <div>
        <div class="eyebrow"><span class="stem"></span>Who We Are</div>
        <h2 class="section-title">Most men leave college having drifted. We exist to flip that.</h2>
      </div>
      <div class="intro-mission">
        <p>The Foundation is a small, invite-only brotherhood for UK men committed to growing — in faith, in fitness, and in character. This isn't a club you join for the resume line. It's a group of guys who hold each other to a higher standard, every single week.</p>
        <p><strong>You are invited or referred in.</strong> Every man completes a trial period with his pod before becoming a full member — because the culture here is built by men who chose it, not men who wandered in.</p>
      </div>
    </div>
  </div>
</section>

<section class="how" id="pod">
  <div class="wrap">
    <div>
      <div class="eyebrow"><span class="stem"></span>How It Works</div>
      <h2 class="section-title">Three things happen every week — without exception.</h2>
      <p class="section-lede">No app, no algorithm, no substitute for men in a room together.</p>
    </div>

    <div class="card-grid">
      <div class="card">
        <div class="card-icon">
          <svg viewBox="0 0 44 44" fill="none" stroke="#b08d2a" stroke-width="1.6">
            <circle cx="15" cy="14" r="5"/>
            <circle cx="29" cy="14" r="5"/>
            <path d="M6 34c0-6 4-10 9-10s9 4 9 10"/>
            <path d="M20 34c0-6 4-10 9-10s9 4 9 10"/>
          </svg>
        </div>
        <h3>The Pod</h3>
        <p>Four to six men, same day, same time, every week. You set real goals together — weekly, semester, and long-term — then your pod holds you to them. No sugarcoating, no showing up unprepared. Prove you can hold the standard, and you're next in line to lead your own pod.</p>
        <span class="cadence">Weekly · Goals &amp; Accountability</span>
      </div>

      <div class="card">
        <div class="card-icon">
          <svg viewBox="0 0 44 44" fill="none" stroke="#b08d2a" stroke-width="1.6">
            <path d="M6 22h4M34 22h4M12 22h20"/>
            <rect x="3" y="17" width="6" height="10" rx="1"/>
            <rect x="35" y="17" width="6" height="10" rx="1"/>
            <rect x="9" y="19" width="4" height="6" rx="1"/>
            <rect x="31" y="19" width="4" height="6" rx="1"/>
          </svg>
        </div>
        <h3>The Work</h3>
        <p>Pods train together every week — pushing each other physically, not just holding each other accountable on paper. Health &amp; fitness is a pillar here, not an afterthought.</p>
        <span class="cadence">Weekly · Group Workouts</span>
      </div>

      <div class="card">
        <div class="card-icon">
          <svg viewBox="0 0 44 44" fill="none" stroke="#b08d2a" stroke-width="1.6">
            <path d="M8 18v8a2 2 0 0 0 2 2h4l9 7V9l-9 7H10a2 2 0 0 0-2 2z"/>
            <path d="M30 16c2 2 2 10 0 12M35 12c4 4 4 16 0 20"/>
          </svg>
        </div>
        <h3>The Gathering</h3>
        <p>Every month, the full brotherhood comes together — a guest speaker or motivational talk, org updates, and a shared moment to refocus and recharge.</p>
        <span class="cadence">Monthly · Speaker Events</span>
      </div>
    </div>

    <div class="leadership-note">
      <p><strong>Every pod leader started as a pod member.</strong> The men who run these groups aren't appointed from outside — they're guys who showed up, held the standard, and earned the trust of the men next to them. If that's you, leading a pod is the next step.</p>
    </div>
  </div>
</section>

<section class="pillars">
  <div class="wrap">
    <div class="eyebrow"><span class="stem"></span>Our Pillars</div>
    <h2 class="section-title">Everything we do runs through five things.</h2>
    <div class="pillar-grid">
      <div class="pillar">
        <div class="pillar-icon">
          <svg viewBox="0 0 44 44" fill="none" stroke="#b08d2a" stroke-width="1.6">
            <path d="M22 6c-3 6-9 9-9 17a9 9 0 0 0 18 0c0-4-2-6-3-8 0 3-2 5-4 5 1-4-1-8-2-14z"/>
          </svg>
        </div>
        <h3>Faith</h3>
        <p>Growing your relationship with God through consistent, intentional devotion — not just on Sunday.</p>
      </div>
      <div class="pillar">
        <div class="pillar-icon">
          <svg viewBox="0 0 44 44" fill="none" stroke="#b08d2a" stroke-width="1.6">
            <path d="M6 22h4M34 22h4M12 22h20"/>
            <rect x="3" y="17" width="6" height="10" rx="1"/>
            <rect x="35" y="17" width="6" height="10" rx="1"/>
          </svg>
        </div>
        <h3>Fitness</h3>
        <p>Building the discipline of showing up physically, every week, with the same men who hold you accountable.</p>
      </div>
      <div class="pillar">
        <div class="pillar-icon">
          <svg viewBox="0 0 44 44" fill="none" stroke="#b08d2a" stroke-width="1.6">
            <path d="M22 8 8 15v6c0 9 6 15 14 17 8-2 14-8 14-17v-6L22 8z"/>
          </svg>
        </div>
        <h3>Relationships</h3>
        <p>Showing up for your family, your friends, and your partner — with honesty and integrity, no matter what.</p>
      </div>
      <div class="pillar">
        <div class="pillar-icon">
          <svg viewBox="0 0 44 44" fill="none" stroke="#b08d2a" stroke-width="1.6">
            <circle cx="22" cy="22" r="15"/>
            <path d="M22 7v30M7 22h30"/>
          </svg>
        </div>
        <h3>Balance</h3>
        <p>Making time to have fun and make memories — being the man your future needs while still enjoying today.</p>
      </div>
      <div class="pillar">
        <div class="pillar-icon">
          <svg viewBox="0 0 44 44" fill="none" stroke="#b08d2a" stroke-width="1.6">
            <path d="M8 30 18 20l6 6 12-14"/>
            <path d="M28 12h8v8"/>
          </svg>
        </div>
        <h3>Provision</h3>
        <p>Investing in your future — in the classroom, in your career, and in the man other people will one day depend on.</p>
      </div>
    </div>
  </div>
</section>

<section class="train-banner" id="train">
  <div class="wrap">
    <div class="eyebrow"><span class="stem"></span>Train Together</div>
    <h2>The body is part of the foundation too.</h2>
    <p>Every pod hits the gym together — because accountability isn't just a conversation, it's a rep count. You show up for your brothers here the same way you show up in the pod: consistently, and without excuses.</p>
  </div>
</section>

<section class="signup" id="signup">
  <div class="wrap">
    <div class="eyebrow">Stay Connected</div>
    <h2>Hold the line with us.</h2>
    <p>Follow along for pod updates, event announcements, and a look at the brotherhood in action.</p>

    <a href="https://instagram.com/the_foundation_men" class="btn-navy ig-btn">
      <svg viewBox="0 0 24 24" width="18" height="18" fill="none" stroke="currentColor" stroke-width="1.8"><rect x="3" y="3" width="18" height="18" rx="5"/><circle cx="12" cy="12" r="4"/><circle cx="17.5" cy="6.5" r="1"/></svg>
      @the_foundation_men
    </a>

    <div class="contact-emails">
      <span>Trevor.eads1@gmail.com</span>
      <span class="contact-divider">&middot;</span>
      <span>Jackmarsella3@gmail.com</span>
    </div>
    <div class="signup-note">Reach out directly — we'll get back to you.</div>
  </div>
</section>

<footer>
  <div class="wrap">
    <div>
      <div class="footer-brand">THE FOUNDATION</div>
      <div class="footer-tag">HOLD THE LINE</div>
    </div>
    <div class="footer-meta">
      University of Kentucky<br>
      &copy; 2026 The Foundation
    </div>
  </div>
</footer>

</body>
</html>
