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
/* ===== INTERACTIVE ENGINEERING DASHBOARD ===== */
.hero-dashboard{
  width:min(470px,100%);
  margin-left:auto;
  padding:18px;
  border:1px solid var(--line);
  border-radius:24px;
  background:linear-gradient(145deg,rgba(15,27,42,.96),rgba(7,13,22,.96));
  box-shadow:var(--shadow);
  position:relative;
  overflow:hidden;
}
.hero-dashboard:before{
  content:"";
  position:absolute;inset:-35%;
  background:conic-gradient(from 180deg,transparent,rgba(67,217,255,.13),transparent,rgba(169,139,255,.10),transparent);
  animation:spinGlow 12s linear infinite;
}
@keyframes spinGlow{to{transform:rotate(360deg)}}
.dashboard-inner{position:relative;z-index:1}
.dash-top{display:flex;justify-content:space-between;align-items:center;margin-bottom:16px}
.dash-label{font:700 10px ui-monospace,monospace;color:var(--muted);letter-spacing:.14em}
.status{display:inline-flex;align-items:center;gap:7px;font-size:11px;color:var(--green);font-weight:800}
.status i{width:7px;height:7px;border-radius:50%;background:var(--green);box-shadow:0 0 12px var(--green)}
.dash-tabs{display:grid;grid-template-columns:repeat(3,1fr);gap:7px;margin-bottom:14px}
.dash-tab{
  border:1px solid var(--line);background:#0a1420;color:var(--muted);
  padding:9px 5px;border-radius:9px;cursor:pointer;font-size:11px;font-weight:800;
}
.dash-tab.active,.dash-tab:hover{color:var(--text);border-color:var(--cyan);background:rgba(67,217,255,.08)}
.dash-panel{display:none}
.dash-panel.active{display:block;animation:dashIn .3s ease}
@keyframes dashIn{from{opacity:0;transform:translateY(5px)}to{opacity:1;transform:none}}
.metric-grid{display:grid;grid-template-columns:1fr 1fr;gap:9px}
.metric{
  padding:14px;border:1px solid var(--line);border-radius:12px;
  background:rgba(7,14,23,.76)
}
.metric small{display:block;color:var(--muted);font-size:10px}
.metric strong{display:block;margin-top:5px;font-size:21px;letter-spacing:-.03em}
.metric em{display:block;margin-top:3px;color:var(--green);font-style:normal;font-size:10px}
.chart{
  height:108px;display:flex;align-items:flex-end;gap:7px;
  padding:13px 4px 0;border-bottom:1px solid var(--line);margin-bottom:11px;
}
.bar{
  flex:1;min-width:9px;border-radius:5px 5px 2px 2px;
  background:linear-gradient(to top,var(--blue),var(--cyan));
  box-shadow:0 0 12px rgba(67,217,255,.12);
  animation:grow .8s ease both;transform-origin:bottom;
}
@keyframes grow{from{transform:scaleY(0)}to{transform:scaleY(1)}}
.chart-caption{display:flex;justify-content:space-between;color:var(--muted);font-size:10px}
.stack{display:grid;gap:9px}
.stack-row{display:grid;grid-template-columns:90px 1fr 40px;align-items:center;gap:8px;font-size:10px}
.stack-row span:first-child{color:var(--muted)}
.track{height:7px;background:#101d2c;border-radius:99px;overflow:hidden;border:1px solid #1c3044}
.fill{height:100%;border-radius:99px;background:linear-gradient(90deg,var(--cyan),var(--blue))}
.insight{
  margin-top:12px;padding:11px 12px;border-radius:11px;
  background:rgba(67,217,255,.06);border:1px solid rgba(67,217,255,.18);
  color:#bcd0e4;font-size:11px;line-height:1.55;
}
.insight b{color:var(--cyan)}
.dashboard-section{
  display:grid;grid-template-columns:.75fr 1.25fr;gap:20px;align-items:stretch;
}
.dashboard-card{
  border:1px solid var(--line);border-radius:20px;padding:24px;
  background:linear-gradient(145deg,rgba(14,25,39,.94),rgba(7,13,22,.94));
  box-shadow:0 16px 55px rgba(0,0,0,.2);
}
.dashboard-card h3{margin:0 0 7px;font-size:20px}
.dashboard-card>p{margin:0;color:var(--muted);line-height:1.65;font-size:13px}
.full-dash{margin-top:18px}
.dash-control{
  display:flex;justify-content:space-between;align-items:center;gap:12px;
  margin-bottom:18px;flex-wrap:wrap
}
.dash-filter{
  display:flex;gap:6px;flex-wrap:wrap
}
.filter-btn{
  border:1px solid var(--line);background:#0a1420;color:var(--muted);
  padding:7px 10px;border-radius:8px;font-size:10px;font-weight:800;cursor:pointer
}
.filter-btn.active,.filter-btn:hover{color:var(--text);border-color:var(--cyan)}
.project-detail{display:none}
.project-detail.active{display:block}
.detail-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:10px;margin-top:16px}
.detail-box{padding:13px;border:1px solid var(--line);border-radius:11px;background:#09121e}
.detail-box small{display:block;color:var(--muted);font-size:9px}
.detail-box strong{display:block;margin-top:4px;font-size:15px}
.detail-list{margin:16px 0 0;padding:0;list-style:none;display:grid;gap:8px}
.detail-list li{padding:9px 10px;border-left:2px solid var(--cyan);background:#09121e;color:#b7c9db;font-size:11px}
@media(max-width:1000px){.hero{display:block}.hero-dashboard{margin:45px 0 0}.dashboard-section{grid-template-columns:1fr}}
@media(max-width:600px){.metric-grid,.detail-grid{grid-template-columns:1fr 1fr}.hero-dashboard{padding:14px}}

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


<section id="insights">
  <div class="eyebrow">// ENGINEERING_INSIGHTS</div>
  <h2 class="section-title">A dashboard, not just a résumé.</h2>
  <p class="section-sub">Click through the views to see how the different engineering disciplines connect. The percentages below are presentation indicators, not measured production KPIs.</p>

  <div class="dashboard-section" style="margin-top:35px">
    <article class="dashboard-card">
      <h3>Engineering Focus</h3>
      <p>Move from “I know these tools” to “I understand how the pieces work together.”</p>
      <div class="stack" style="margin-top:22px">
        <div class="stack-row"><span>Cloud</span><div class="track"><div class="fill" style="width:92%"></div></div><b>92%</b></div>
        <div class="stack-row"><span>Infrastructure</span><div class="track"><div class="fill" style="width:95%"></div></div><b>95%</b></div>
        <div class="stack-row"><span>Automation</span><div class="track"><div class="fill" style="width:88%"></div></div><b>88%</b></div>
        <div class="stack-row"><span>Security</span><div class="track"><div class="fill" style="width:86%"></div></div><b>86%</b></div>
      </div>
      <div class="insight"><b>WHY IT MATTERS:</b> Strong infrastructure engineering connects deployment, security, observability and recovery.</div>
    </article>

    <article class="dashboard-card">
      <div class="dash-control">
        <div>
          <h3>Interactive Project Intelligence</h3>
          <p>Select a project to reveal its engineering story.</p>
        </div>
        <div class="dash-filter">
          <button class="filter-btn active" data-project="modernisation">Modernisation</button>
          <button class="filter-btn" data-project="avd">AVD</button>
          <button class="filter-btn" data-project="dr">Backup & DR</button>
          <button class="filter-btn" data-project="aws">AWS</button>
        </div>
      </div>

      <div class="project-detail active" id="project-modernisation">
        <h3>Azure & Microsoft 365 Modernisation</h3>
        <div class="detail-grid">
          <div class="detail-box"><small>PLATFORM</small><strong>Azure + M365</strong></div>
          <div class="detail-box"><small>IDENTITY</small><strong>Entra ID</strong></div>
          <div class="detail-box"><small>SECURITY</small><strong>MFA + CA</strong></div>
        </div>
        <ul class="detail-list"><li>Modernise cloud and productivity workloads.</li><li>Strengthen identity and access controls.</li><li>Make user and workload management more centralised.</li></ul>
      </div>

      <div class="project-detail" id="project-avd">
        <h3>Azure Virtual Desktop</h3>
        <div class="detail-grid">
          <div class="detail-box"><small>PLATFORM</small><strong>Azure AVD</strong></div>
          <div class="detail-box"><small>ACCESS</small><strong>Secure Remote</strong></div>
          <div class="detail-box"><small>MODEL</small><strong>Centralised</strong></div>
        </div>
        <ul class="detail-list"><li>Support secure remote desktop environments.</li><li>Centralise desktop management.</li><li>Connect endpoint operations with cloud infrastructure.</li></ul>
      </div>

      <div class="project-detail" id="project-dr">
        <h3>Veeam Backup & Disaster Recovery</h3>
        <div class="detail-grid">
          <div class="detail-box"><small>PLATFORM</small><strong>Veeam</strong></div>
          <div class="detail-box"><small>OBJECTIVE</small><strong>Resilience</strong></div>
          <div class="detail-box"><small>FOCUS</small><strong>RTO / RPO</strong></div>
        </div>
        <ul class="detail-list"><li>Maintain reliable backup environments.</li><li>Verify recovery readiness.</li><li>Align recovery planning with business objectives.</li></ul>
      </div>

      <div class="project-detail" id="project-aws">
        <h3>AWS Cloud Infrastructure</h3>
        <div class="detail-grid">
          <div class="detail-box"><small>PLATFORM</small><strong>AWS</strong></div>
          <div class="detail-box"><small>FOCUS</small><strong>Cloud Workloads</strong></div>
          <div class="detail-box"><small>DESIGN</small><strong>Hybrid Ready</strong></div>
        </div>
        <ul class="detail-list"><li>Provision and manage cloud workloads.</li><li>Support cloud networking and security controls.</li><li>Integrate cloud services into hybrid environments.</li></ul>
      </div>
    </article>
  </div>
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
document.querySelectorAll('.dash-tab').forEach(button => {
  button.addEventListener('click', () => {
    document.querySelectorAll('.dash-tab').forEach(b => b.classList.remove('active'));
    document.querySelectorAll('.dash-panel').forEach(p => p.classList.remove('active'));
    button.classList.add('active');
    document.getElementById('dash-' + button.dataset.tab).classList.add('active');
  });
});

document.querySelectorAll('.filter-btn').forEach(button => {
  button.addEventListener('click', () => {
    document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
    document.querySelectorAll('.project-detail').forEach(p => p.classList.remove('active'));
    button.classList.add('active');
    document.getElementById('project-' + button.dataset.project).classList.add('active');
  });
});
</script>

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
    
