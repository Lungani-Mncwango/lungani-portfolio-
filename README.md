<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Lungani Mncwango - Cloud Engineer, IT Infrastructure Lead, Azure & AWS Specialist">
<title>Lungani Mncwango | Cloud & Infrastructure Portfolio</title>

<style>
:root{
  --bg:#05080d;
  --bg2:#08101a;
  --panel:rgba(12,20,31,.82);
  --panel-solid:#0c1521;
  --line:#1c2b3c;
  --line-bright:#30465f;
  --text:#f4f8fc;
  --muted:#9aacbf;
  --cyan:#43d9ff;
  --blue:#667cff;
  --purple:#a98bff;
  --green:#52e18b;
  --shadow:0 24px 80px rgba(0,0,0,.42);
}
*{box-sizing:border-box;scroll-behavior:smooth}
html{scroll-padding-top:88px}
body{
  margin:0;
  color:var(--text);
  font-family:Inter,ui-sans-serif,system-ui,-apple-system,BlinkMacSystemFont,"Segoe UI",sans-serif;
  background:
    radial-gradient(circle at 12% 8%,rgba(67,217,255,.12),transparent 25%),
    radial-gradient(circle at 88% 18%,rgba(102,124,255,.12),transparent 28%),
    linear-gradient(180deg,var(--bg),var(--bg2) 50%,var(--bg));
  overflow-x:hidden;
}
body:before{
  content:"";
  position:fixed;inset:0;pointer-events:none;z-index:-1;opacity:.18;
  background-image:
    linear-gradient(rgba(255,255,255,.025) 1px,transparent 1px),
    linear-gradient(90deg,rgba(255,255,255,.025) 1px,transparent 1px);
  background-size:44px 44px;
}
a{text-decoration:none;color:inherit}
.nav{
  position:sticky;top:0;z-index:50;
  display:flex;justify-content:space-between;align-items:center;gap:20px;
  padding:15px 6%;
  background:rgba(5,8,13,.72);
  backdrop-filter:blur(20px);
  border-bottom:1px solid rgba(48,70,95,.55);
}
.logo{font-weight:900;letter-spacing:.1em;font-size:14px}
.logo span{color:var(--cyan)}
.navlinks{display:flex;gap:7px;flex-wrap:wrap;justify-content:flex-end}
.navlinks a,.btn{
  border:1px solid var(--line);
  background:rgba(12,21,33,.72);
  color:var(--text);
  padding:10px 14px;border-radius:10px;
  font-size:13px;font-weight:700;
  transition:transform .25s,border-color .25s,box-shadow .25s,background .25s;
}
.navlinks a:hover,.navlinks a.active,.btn:hover{
  border-color:var(--cyan);
  background:rgba(67,217,255,.08);
  transform:translateY(-2px);
  box-shadow:0 0 25px rgba(67,217,255,.12);
}
.hero{
  min-height:calc(100vh - 72px);
  display:flex;align-items:center;
  padding:90px 8% 100px;
  position:relative;
}
.hero>div{max-width:980px}
.eyebrow{
  color:var(--cyan);
  font:700 12px/1.5 ui-monospace,SFMono-Regular,Menlo,monospace;
  letter-spacing:.16em;
  text-transform:uppercase;
}
h1{
  max-width:1000px;
  font-size:clamp(48px,8vw,96px);
  line-height:.94;
  letter-spacing:-.055em;
  margin:18px 0 24px;
}
.gradient{
  background:linear-gradient(90deg,var(--cyan),var(--blue),var(--purple));
  -webkit-background-clip:text;background-clip:text;color:transparent;
}
.hero p{
  max-width:780px;
  color:var(--muted);
  font-size:19px;
  line-height:1.8;
  margin:0;
}
.actions{display:flex;gap:12px;flex-wrap:wrap;margin-top:30px}
.btn{display:inline-flex;align-items:center;justify-content:center;min-height:44px}
.primary{
  color:#041017;
  background:linear-gradient(100deg,var(--cyan),#7182ff);
  border:0;
  box-shadow:0 12px 35px rgba(67,217,255,.16);
}
.impact{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:12px;
  padding:0 8% 35px;
}
.impact-item{
  padding:20px;
  border:1px solid var(--line);
  border-radius:15px;
  background:linear-gradient(145deg,rgba(17,29,44,.85),rgba(8,14,23,.82));
}
.impact-item strong{display:block;font-size:24px;color:var(--text);letter-spacing:-.03em}
.impact-item span{display:block;margin-top:4px;color:var(--muted);font-size:13px}
section{padding:95px 8%;position:relative}
.section-title{font-size:clamp(32px,4vw,48px);letter-spacing:-.04em;margin:8px 0 12px}
.section-sub{color:var(--muted);max-width:780px;line-height:1.8;margin:0}
.grid{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:18px;
  margin-top:38px;
}
.card{
  min-height:220px;
  background:linear-gradient(145deg,rgba(17,28,43,.94),rgba(8,14,23,.94));
  border:1px solid var(--line);
  border-radius:18px;
  padding:26px;
  transition:.3s;
  position:relative;
  overflow:hidden;
  box-shadow:0 12px 40px rgba(0,0,0,.16);
}
.card:before{
  content:"";
  position:absolute;inset:0;
  background:linear-gradient(120deg,rgba(67,217,255,.06),transparent 45%);
  opacity:0;transition:.3s;
}
.card:hover{transform:translateY(-7px);border-color:var(--line-bright);box-shadow:var(--shadow)}
.card:hover:before{opacity:1}
.card h3{position:relative;margin:0 0 12px;color:var(--text);font-size:19px}
.card p,.card li{position:relative;color:var(--muted);line-height:1.75}
.tags{position:relative;display:flex;gap:8px;flex-wrap:wrap;margin-top:18px}
.tag{
  padding:6px 9px;border-radius:999px;
  background:#101d2c;border:1px solid #22364d;
  color:#c9d9e9;font:12px ui-monospace,SFMono-Regular,Menlo,monospace;
}
.pipeline{
  display:grid;grid-template-columns:repeat(5,1fr);
  gap:12px;margin-top:38px;align-items:stretch;
}
.node{
  text-align:center;padding:24px 12px;
  background:var(--panel);border:1px solid var(--line);
  border-radius:14px;position:relative;
}
.node:after{
  content:"→";position:absolute;right:-18px;top:29px;
  color:var(--cyan);font-size:21px;
}
.node:last-child:after{display:none}
.node b{display:block;color:var(--cyan);font:700 11px ui-monospace,monospace;margin-bottom:8px}
.terminal{
  border:1px solid var(--line);background:#070d15;border-radius:18px;
  box-shadow:var(--shadow);overflow:hidden;
}
.termhead{padding:13px 16px;border-bottom:1px solid var(--line);display:flex;gap:7px}
.dot{width:10px;height:10px;border-radius:50%;background:#42546a}
.termbody{padding:25px;font:14px/2 ui-monospace,SFMono-Regular,Menlo,monospace;color:#c9d7e8}
.green{color:var(--green)}.cyan{color:var(--cyan)}.purple{color:var(--purple)}
.timeline{border-left:1px solid #29415b;margin-top:40px;padding-left:32px}
.role{margin-bottom:42px;position:relative}
.role:before{
  content:"";position:absolute;left:-39px;top:4px;width:12px;height:12px;
  border-radius:50%;background:var(--cyan);box-shadow:0 0 20px rgba(67,217,255,.65);
}
.role .date{color:var(--cyan);font:700 11px ui-monospace,monospace;letter-spacing:.1em}
.role h3{margin:8px 0 9px;font-size:20px}
.role p{color:var(--muted);line-height:1.8;max-width:900px;margin:0}
.contact{
  display:grid;grid-template-columns:1fr auto;gap:30px;align-items:center;
  background:linear-gradient(120deg,rgba(67,217,255,.08),rgba(169,139,255,.08));
  border:1px solid var(--line);border-radius:22px;padding:42px;
  box-shadow:var(--shadow);
}
.contact .actions{margin-top:0;justify-content:flex-end}
footer{padding:38px 8%;border-top:1px solid var(--line);color:var(--muted);text-align:center;font-size:13px}
@media(max-width:900px){
  .hero{padding-top:70px}
  .grid{grid-template-columns:1fr 1fr}
  .impact{grid-template-columns:1fr 1fr}
  .pipeline{grid-template-columns:1fr}
  .node:after{content:"↓";right:50%;top:auto;bottom:-27px}
  .node:last-child:after{display:none}
  .contact{grid-template-columns:1fr}
  .contact .actions{justify-content:flex-start}
}
@media(max-width:600px){
  .nav{align-items:flex-start;flex-direction:column}
  .navlinks{justify-content:flex-start}
  .hero{padding:60px 6% 70px}
  h1{font-size:clamp(44px,14vw,68px)}
  .hero p{font-size:17px}
  section{padding:70px 6%}
  .grid,.impact{grid-template-columns:1fr}
  .impact{padding:0 6% 25px}
  .contact{padding:28px}
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
    <h1>I build <span class="gradient">secure, scalable</span> infrastructure that works.</h1>
    <p>
      I’m Lungani Mncwango — a Cloud & Infrastructure Engineer focused on
      Azure, AWS, automation, cybersecurity and resilient enterprise operations.
      I turn complex infrastructure into environments that are easier to deploy,
      secure, monitor and support.
    </p>
    <div class="actions">
      <a class="btn primary" href="#projects">Explore My Work</a>
      <a class="btn" href="Lungani-Mncwango-CV.docx" download>Download CV</a>
      <a class="btn" href="mailto:Lungani.godsent.mncwango@gmail.com">Email Me</a>
    </div>
  </div>
  

<section class="impact">
  <div class="impact-item"><strong>10+</strong><span>Years in IT</span></div>
  <div class="impact-item"><strong>Cloud</strong><span>Azure + AWS</span></div>
  <div class="impact-item"><strong>IaC</strong><span>Automation mindset</span></div>
  <div class="impact-item"><strong>24/7</strong><span>Enterprise operations</span></div>
</section>

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
  <h2 class="section-title">A decade of solving infrastructure problems.</h2>
  <p class="section-sub">From frontline technical support to senior cloud and infrastructure operations, the focus has stayed the same: keep systems secure, available and moving forward.</p>

  <div class="timeline">
    <div class="role">
      <div class="date">AUG 2025 — PRESENT</div>
      <h3>Senior Service Engineer — Network Infrastructure Support [EMEA]</h3>
      <p><strong>Wavenet</strong> · Complex IT troubleshooting across Microsoft 365, SharePoint, Intune, Azure, Entra ID, AVD, Active Directory, networking, firewalls, VPN, VMware, Hyper-V and Veeam. Own complex incidents through resolution while supporting SLA compliance and service resilience.</p>
    </div>

    <div class="role">
      <div class="date">FEB 2024 — AUG 2025</div>
      <h3>Regional Support Engineer — Contract</h3>
      <p><strong>Ardagh Group</strong> · Managed Office 365, Azure, SharePoint, Teams, desktop systems, servers, Active Directory, Group Policy, disaster recovery and Intune across regional environments.</p>
    </div>

    <div class="role">
      <div class="date">AUG 2022 — FEB 2024</div>
      <h3>IT Infrastructure &amp; Security Manager</h3>
      <p><strong>Nketu Projects LTD</strong> · Led IT strategy, infrastructure, cybersecurity, risk management, disaster recovery, governance, project delivery, budgeting and vendor engagement.</p>
    </div>

    <div class="role">
      <div class="date">SEP 2019 — AUG 2022</div>
      <h3>Support Technician</h3>
      <p><strong>Altron Bytes Managed Solutions</strong> · Delivered technical support, backup monitoring, restore requests, audits, asset recovery documentation and field support across client environments.</p>
    </div>

    <div class="role">
      <div class="date">FEB 2018 — APR 2019</div>
      <h3>Field Service Engineer</h3>
      <p><strong>Gijima Technology People</strong> · Supported financial-sector retail and POS environments through installations, configuration, maintenance, asset verification, data restoration and system imaging. Supported FNB and Capitec initiatives while maintaining SLA-focused field operations.</p>
    </div>

    <div class="role">
      <div class="date">FEB 2015 — FEB 2018</div>
      <h3>IT Technician — Permanent</h3>
      <p><strong>Matrix Warehouse Computers</strong> · Delivered Office 365, Azure, Windows, Linux, Windows Server, networking and printer support. Implemented automated backup schedules and recovered client systems from OS failures and data corruption using verified backups.</p>
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
  © 2026 Lungani Mncwango · Cloud · Infrastructure · Automation · Cybersecurity
</footer>

<script>
  // Smooth active-section navigation
  const links = [...document.querySelectorAll('.navlinks a')];
  const sections = links
    .map(link => document.querySelector(link.getAttribute('href')))
    .filter(Boolean);

  const observer = new IntersectionObserver(entries => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        links.forEach(link => link.classList.remove('active'));
        const active = links.find(link => link.getAttribute('href') === '#' + entry.target.id);
        if (active) active.classList.add('active');
      }
    });
  }, { rootMargin: '-35% 0px -55% 0px' });

  sections.forEach(section => observer.observe(section));
</script>
</body>
</html>
    
