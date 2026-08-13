<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Lungani Mncwango - Cloud Engineer, IT Infrastructure Lead, Azure & AWS Specialist">
<title>Lungani Mncwango | Cloud & Infrastructure Portfolio</title>

<style>
:root{
  --bg:#070b12;
  --panel:#0d1420;
  --panel2:#111b2a;
  --line:#203044;
  --text:#edf5ff;
  --muted:#91a4ba;
  --cyan:#45d9ff;
  --blue:#5b7cff;
  --green:#4ade80;
  --purple:#a78bfa;
}
*{box-sizing:border-box;scroll-behavior:smooth}
body{
  margin:0;
  font-family:Inter,Segoe UI,Arial,sans-serif;
  color:var(--text);
  background:
    radial-gradient(circle at 15% 10%,rgba(69,217,255,.12),transparent 28%),
    radial-gradient(circle at 85% 25%,rgba(91,124,255,.12),transparent 30%),
    var(--bg);
}
body:before{
  content:"";
  position:fixed;inset:0;pointer-events:none;opacity:.22;
  background-image:linear-gradient(rgba(255,255,255,.025) 1px,transparent 1px),
                   linear-gradient(90deg,rgba(255,255,255,.025) 1px,transparent 1px);
  background-size:40px 40px;
}
a{text-decoration:none;color:inherit}
.nav{
  position:sticky;top:0;z-index:20;
  display:flex;justify-content:space-between;align-items:center;
  padding:16px 6%;background:rgba(7,11,18,.82);
  backdrop-filter:blur(16px);border-bottom:1px solid var(--line);
}
.logo{font-weight:800;letter-spacing:.08em}
.logo span{color:var(--cyan)}
.navlinks{display:flex;gap:8px;flex-wrap:wrap}
.navlinks a,.btn{
  border:1px solid var(--line);background:#0c1420;color:var(--text);
  padding:9px 14px;border-radius:9px;font-size:13px;cursor:pointer;
  transition:.25s;
}
.navlinks a:hover,.btn:hover{border-color:var(--cyan);transform:translateY(-2px);box-shadow:0 0 22px rgba(69,217,255,.12)}
.hero{
  min-height:92vh;display:grid;grid-template-columns:1.25fr .75fr;
  gap:50px;align-items:center;padding:80px 8%;
}
.eyebrow{color:var(--cyan);font-family:monospace;letter-spacing:.12em}
h1{font-size:clamp(42px,7vw,78px);line-height:.98;margin:14px 0}
.gradient{background:linear-gradient(90deg,var(--cyan),var(--blue),var(--purple));-webkit-background-clip:text;background-clip:text;color:transparent}
.hero p{max-width:720px;color:var(--muted);font-size:18px;line-height:1.8}
.actions{display:flex;gap:12px;flex-wrap:wrap;margin-top:25px}
.primary{background:linear-gradient(90deg,#1c83a6,#4b61d7);border:0}
.terminal{
  border:1px solid var(--line);background:rgba(13,20,32,.9);border-radius:18px;
  box-shadow:0 25px 80px rgba(0,0,0,.35);overflow:hidden;
}
.termhead{padding:12px 16px;border-bottom:1px solid var(--line);display:flex;gap:7px}
.dot{width:10px;height:10px;border-radius:50%;background:#46556a}
.termbody{padding:24px;font:14px/1.9 monospace;color:#c9d7e8}
.green{color:var(--green)}.cyan{color:var(--cyan)}.purple{color:var(--purple)}
.profile-wrap{display:flex;justify-content:center}
.profile{
  width:min(340px,75vw);aspect-ratio:1;border-radius:50%;object-fit:cover;
  border:4px solid #263a52;box-shadow:0 0 0 12px rgba(69,217,255,.04),0 0 70px rgba(69,217,255,.18);
}
section{padding:90px 8%;position:relative}
.section-title{font-size:36px;margin:0 0 12px}
.section-sub{color:var(--muted);max-width:720px;line-height:1.7}
.grid{display:grid;grid-template-columns:repeat(3,1fr);gap:18px;margin-top:35px}
.card{
  background:linear-gradient(145deg,rgba(17,27,42,.95),rgba(10,16,26,.95));
  border:1px solid var(--line);border-radius:16px;padding:24px;
  transition:.3s;position:relative;overflow:hidden;
}
.card:hover{transform:translateY(-6px);border-color:#365273}
.card h3{margin:0 0 10px;color:var(--cyan)}
.card p,.card li{color:var(--muted);line-height:1.7}
.tags{display:flex;gap:8px;flex-wrap:wrap;margin-top:16px}
.tag{padding:6px 9px;border-radius:999px;background:#162234;border:1px solid #263a52;color:#c8d8ea;font:12px monospace}
.pipeline{
  display:grid;grid-template-columns:repeat(5,1fr);gap:10px;margin-top:35px;align-items:center;
}
.node{
  text-align:center;padding:20px 10px;background:#0d1725;border:1px solid #263a52;border-radius:12px;
  position:relative;
}
.node:after{content:"→";position:absolute;right:-17px;top:28px;color:var(--cyan);font-size:20px}
.node:last-child:after{display:none}
.node b{display:block;color:var(--cyan);margin-bottom:6px}
.timeline{border-left:1px solid #29415b;margin-top:35px;padding-left:28px}
.role{margin-bottom:35px;position:relative}
.role:before{content:"";position:absolute;left:-35px;top:5px;width:11px;height:11px;border-radius:50%;background:var(--cyan);box-shadow:0 0 18px var(--cyan)}
.role .date{color:var(--cyan);font:12px monospace}
.role h3{margin:7px 0}.role p{color:var(--muted);line-height:1.7}
.contact{
  display:grid;grid-template-columns:1fr 1fr;gap:25px;align-items:center;
  background:linear-gradient(120deg,rgba(69,217,255,.08),rgba(167,139,250,.06));
  border:1px solid var(--line);border-radius:20px;padding:35px;
}
footer{padding:35px 8%;border-top:1px solid var(--line);color:var(--muted);text-align:center}
@media(max-width:850px){
  .hero,.contact{grid-template-columns:1fr}
  .grid{grid-template-columns:1fr 1fr}
  .pipeline{grid-template-columns:1fr}
  .node:after{content:"↓";right:50%;top:auto;bottom:-25px}
  .node:last-child:after{display:none}
}
@media(max-width:560px){
  .nav{align-items:flex-start;gap:10px;flex-direction:column}
  .grid{grid-template-columns:1fr}
  section{padding:65px 6%}
  .hero{padding:65px 6%}
}
</style>
</head>

<body>
<nav class="nav">
  <div class="logo">LUNGANI<span>.OPS</span></div>
  <div class="navlinks">
    <a href="#skills">Skills</a>
    <a href="#automation">Automation</a>
    <a href="#projects">Projects</a>
    <a href="#experience">Experience</a>
    <a href="#contact">Contact</a>
  </div>
</nav>

<header class="hero">
  <div>
    <div class="eyebrow">// CLOUD • INFRASTRUCTURE • AUTOMATION</div>
    <h1>Engineering <span class="gradient">resilient</span> infrastructure.</h1>
    <p>
      Lungani Mncwango — Cloud Engineer, IT Infrastructure Lead, Azure & AWS Specialist,
      IT Support L3, Network Infrastructure and Cyber Security L3.
      10+ years of experience across cloud, hybrid infrastructure, security,
      disaster recovery and enterprise service operations.
    </p>
    <div class="actions">
      <a class="btn primary" href="#projects">Explore My Work</a>
      <a class="btn" href="Lungani-Mncwango-CV.docx" download>Download CV</a>
      <a class="btn" href="mailto:Lungani.godsent.mncwango@gmail.com">Email Me</a>
    </div>
  </div>

  <div class="profile-wrap">
    <img src="C:\lungani-portfolio\assets\profile.png">
  </div>
</header>

<section id="skills">
  <div class="eyebrow">// TECH_STACK</div>
  <h2 class="section-title">Core Engineering Skills</h2>
  <p class="section-sub">Skills represented from the uploaded CV, organised into an engineering-focused portfolio.</p>

  <div class="grid">
    <article class="card">
      <h3>☁ Cloud & Infrastructure</h3>
      <p>Design, administration and support of enterprise cloud and hybrid environments.</p>
      <div class="tags"><span class="tag">Azure</span><span class="tag">AWS</span><span class="tag">Microsoft 365</span><span class="tag">Entra ID</span><span class="tag">Intune</span><span class="tag">AVD</span></div>
    </article>
    <article class="card">
      <h3>⚙ Automation</h3>
      <p>Automation and scripting used to improve operational efficiency and reduce repetitive work.</p>
      <div class="tags"><span class="tag">PowerShell</span><span class="tag">Python</span><span class="tag">Bash</span><span class="tag">Ansible</span></div>
    </article>
    <article class="card">
      <h3>🔐 Cybersecurity</h3>
      <p>Security operations, monitoring, hardening, vulnerability management and governance.</p>
      <div class="tags"><span class="tag">SIEM</span><span class="tag">EDR/XDR</span><span class="tag">Fortinet</span><span class="tag">ISO 27001</span><span class="tag">POPIA</span><span class="tag">GDPR</span></div>
    </article>
    <article class="card">
      <h3>🖥 Virtualisation</h3>
      <p>Enterprise server and virtualisation administration supporting resilient infrastructure.</p>
      <div class="tags"><span class="tag">VMware</span><span class="tag">Hyper-V</span><span class="tag">Windows Server</span><span class="tag">Active Directory</span></div>
    </article>
    <article class="card">
      <h3>🛡 Backup & DR</h3>
      <p>Business continuity, recovery planning, backup verification and disaster recovery testing.</p>
      <div class="tags"><span class="tag">Veeam</span><span class="tag">Azure Backup</span><span class="tag">RTO/RPO</span><span class="tag">DR Testing</span></div>
    </article>
    <article class="card">
      <h3>🌐 Networking</h3>
      <p>Enterprise connectivity, network security and infrastructure troubleshooting.</p>
      <div class="tags"><span class="tag">Firewalls</span><span class="tag">VPN</span><span class="tag">VLAN</span><span class="tag">TCP/IP</span><span class="tag">LAN/WAN</span><span class="tag">DNS/DHCP</span></div>
    </article>
  </div>
</section>

<section id="automation">
  <div class="eyebrow">// AUTOMATION_FLOW</div>
  <h2 class="section-title">Infrastructure Automation</h2>
  <p class="section-sub">A visual representation of how automation can connect code, configuration, infrastructure and monitoring.</p>

  <div class="pipeline">
    <div class="node"><b>01</b>Code<br>Python / Bash</div>
    <div class="node"><b>02</b>Configure<br>Ansible</div>
    <div class="node"><b>03</b>Provision<br>Cloud / IaC</div>
    <div class="node"><b>04</b>Secure<br>IAM / SIEM</div>
    <div class="node"><b>05</b>Monitor<br>Operations</div>
  </div>

  <div class="terminal" style="margin-top:35px">
    <div class="termhead"><span class="dot"></span><span class="dot"></span><span class="dot"></span></div>
    <div class="termbody">
      <div>$ <span class="cyan">automation</span> --environment production</div>
      <div>[<span class="green">OK</span>] validating infrastructure</div>
      <div>[<span class="green">OK</span>] applying configuration</div>
      <div>[<span class="green">OK</span>] security controls checked</div>
      <div>[<span class="green">OK</span>] monitoring enabled</div>
      <div>$ <span class="purple">deployment complete</span></div>
    </div>
  </div>
</section>

<section id="projects">
  <div class="eyebrow">// SELECTED_PROJECTS</div>
  <h2 class="section-title">Infrastructure & Cloud Projects</h2>
  <div class="grid">
    <article class="card">
      <h3>Azure & Microsoft 365 Modernisation</h3>
      <p>Migrated users and workloads to Microsoft 365, managed Entra ID integrations and implemented MFA and Conditional Access.</p>
      <div class="tags"><span class="tag">Azure</span><span class="tag">M365</span><span class="tag">Entra ID</span><span class="tag">MFA</span></div>
    </article>
    <article class="card">
      <h3>Azure Virtual Desktop</h3>
      <p>Configured AVD environments and secure remote access while supporting centralised desktop management.</p>
      <div class="tags"><span class="tag">AVD</span><span class="tag">Azure</span><span class="tag">Remote Access</span></div>
    </article>
    <article class="card">
      <h3>Veeam Backup & DR</h3>
      <p>Designed and maintained backup environments, recovery verification and simulations aligned with RTO/RPO objectives.</p>
      <div class="tags"><span class="tag">Veeam</span><span class="tag">DR</span><span class="tag">RTO/RPO</span></div>
    </article>
    <article class="card">
      <h3>AWS Cloud Infrastructure</h3>
      <p>Provisioned and managed AWS workloads, cloud networking and security controls supporting hybrid environments.</p>
      <div class="tags"><span class="tag">AWS</span><span class="tag">Networking</span><span class="tag">Security</span></div>
    </article>
    <article class="card">
      <h3>Cybersecurity & Hardening</h3>
      <p>Implemented SIEM monitoring and threat detection controls, improved incident response and supported ISO 27001 initiatives.</p>
      <div class="tags"><span class="tag">SIEM</span><span class="tag">Security</span><span class="tag">ISO 27001</span></div>
    </article>
    <article class="card">
      <h3>Infrastructure Modernisation</h3>
      <p>Supported server migrations and cloud onboarding, including Active Directory, Intune, Exchange Online and SharePoint migrations.</p>
      <div class="tags"><span class="tag">Migration</span><span class="tag">Intune</span><span class="tag">Exchange</span></div>
    </article>
  </div>
</section>

<section id="experience">
  <div class="eyebrow">// CAREER_TIMELINE</div>
  <h2 class="section-title">Experience</h2>
  <div class="timeline">
    <div class="role">
      <div class="date">AUG 2025 — PRESENT</div>
      <h3>24/7 Senior Service Engineer — Network Infrastructure Support [EMEA]</h3>
      <p>Wavenet. Complex IT troubleshooting, Microsoft 365, SharePoint, Intune, Azure/Entra ID/AVD, Active Directory, networking, firewalls, VPN, VMware/Hyper-V and Veeam. Mentors junior engineers and supports SLA compliance.</p>
    </div>
    <div class="role">
      <div class="date">FEB 2024 — AUG 2025</div>
      <h3>Regional Support Engineer — Contract</h3>
      <p>Ardagh Group. Managed Office 365, Azure, SharePoint, Teams and desktop systems; supported infrastructure, servers, Active Directory, Group Policy, disaster recovery and Intune.</p>
    </div>
    <div class="role">
      <div class="date">AUG 2022 — FEB 2024</div>
      <h3>IT Infrastructure & Security Manager</h3>
      <p>Nketu Projects LTD. Led IT strategy, infrastructure, cybersecurity, risk management, disaster recovery, project delivery, governance, budgeting and vendor engagement.</p>
    </div>
    <div class="role">
      <div class="date">SEP 2019 — AUG 2022</div>
      <h3>Support Technician</h3>
      <p>Altron Bytes Managed Solutions. Technical support, backup monitoring, restore requests, audits, asset recovery documentation and field support across client environments.</p>
    </div>
  </div>
</section>

<section id="contact">
  <div class="contact">
    <div>
      <div class="eyebrow">// LET'S_CONNECT</div>
      <h2 class="section-title">Build resilient infrastructure.</h2>
      <p class="section-sub">Interested in cloud engineering, infrastructure, automation, cybersecurity or enterprise operations?</p>
    </div>
    <div class="actions">
      <a class="btn primary" href="mailto:Lungani.godsent.mncwango@gmail.com">Email Me</a>
      <a class="btn" href="tel:0840419402">Call Me</a>
      <a class="btn" href="Lungani-Mncwango-CV.docx" download>Download CV</a>
    </div>
  </div>
</section>

<footer>
  © 2026 Lungani Mncwango · Cloud Engineer · IT Infrastructure · Automation · Cybersecurity
</footer>
</body>
</html>
    
