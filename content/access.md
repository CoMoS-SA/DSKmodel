---
title: GitHub Repositories
pager: false
full_width: true
---

<style>
.prose > p:first-of-type{
  text-align:center !important;
}

.repo-grid{
  display:grid;
  grid-template-columns:1fr;
  max-width:700px;
  gap:1.8rem;
  margin-top:2rem;
}

.repo-card{
  border:1px solid #e5e7eb;
  border-radius:12px;
  padding:1.8rem;
  background:#fff;
  min-height:190px;                 /* FLAT rectangle */
  display:flex;                     /* allow vertical control */
  flex-direction:column;
  justify-content:space-between;    /* button stays bottom */
  transition:transform .15s ease, box-shadow .15s ease;
}

.repo-card:hover{
  transform:translateY(-3px);
  box-shadow:0 10px 25px rgba(0,0,0,.08);
}

.repo-main{
  border:2px solid #4338CA;
}

.repo-title{
  font-size:1.25rem;
  font-weight:700;
  margin-bottom:.4rem;
}

.repo-desc{
  font-size:.95rem;
  color:#555;
  margin-bottom:1rem;
}

.repo-btn{
  align-self:flex-start;
  padding:.55rem 1.2rem;
  background:#4F46E5;
  color:white;
  border-radius:6px;
  text-decoration:none;
  font-weight:600;
}
.repo-btn:hover{
  background:#4338CA;
}

/* Mobile */
@media (max-width: 640px){
  .repo-grid{
    grid-template-columns:1fr;
  }
}

/* Dark mode */
html.dark .repo-card{
  background:#1f2027;
  border-color:#3f3f46;
}
html.dark .repo-card:hover{
  box-shadow:0 10px 25px rgba(0,0,0,.4);
}
html.dark .repo-main{
  border-color:#818cf8;
}
html.dark .repo-desc{
  color:#a1a1aa;
}
</style>

Below you can find the main **DSK model** repositories.

<div class="repo-grid">

<div class="repo-card repo-main">
  <div>
    <div class="repo-title">DSK Model (Main)</div>
    <div class="repo-desc">
      This repository allows access to the main DSK model as originally developed by Lamperti et al. (2018) and with the latest integrations for stock flow consistency developed by Reissl et al. (2025). 
    </div>
  </div>
  <a class="repo-btn" href="https://github.com/CoMoS-SA/Reissl_2025" target="_blank">
    View repository →
  </a>
</div>
<div class="repo-card">
  <div>
    <div class="repo-title">
      Model version used in the paper by Wieners et al. (2025). 
    </div>
    <div class="repo-desc">
      The model includes a range of policy tools, such as green industrial policies, subsidies and carbon pricing.  
    </div>
  </div>
  <a class="repo-btn" href="https://github.com/CoMoS-SA/Wieners_2025" target="_blank">
    View repository →
  </a>
</div>



