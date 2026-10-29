---
title: Documentation
pager: false
full_width: true
---
<style>
.doc-layout{
  display:flex;
  align-items:flex-start;
  gap:2.5rem;
  margin-top:1rem;
}

/* Sidebar table of contents */
.doc-toc{
  flex:0 0 260px;
  width:260px;
  position:sticky;
  top:90px;
  max-height:calc(100vh - 110px);
  overflow-y:auto;
  background:#fff;
  border:1px solid #e5e7eb;
  border-radius:12px;
  padding:1.25rem 1.1rem;
  font-size:.92rem;
  text-align:left !important;
}
.doc-toc *{
  text-align:left !important;
}
.doc-toc .doc-toc-title{
  font-weight:700;
  text-transform:uppercase;
  letter-spacing:.04em;
  font-size:.78rem;
  color:#6b7280;
  margin-bottom:.75rem;
}
.doc-toc ul{
  list-style:none;
  margin:0;
  padding:0;
}
.doc-toc > ul{
  counter-reset: toc-sec;
}
.doc-toc > ul > li{
  margin-bottom:.15rem;
  counter-increment: toc-sec;
}
.doc-toc > ul > li > a::before{
  content: counter(toc-sec) ". ";
  color:#142E94;
  font-weight:700;
}
.doc-toc a{
  display:block;
  padding:.3rem .5rem;
  border-radius:6px;
  color:#374151;
  text-decoration:none;
  line-height:1.3;
}
.doc-toc a:hover{
  background:#E9ECF7;
  color:#142E94;
}
.doc-toc > ul > li > a{
  font-weight:600;
}
.doc-toc ul ul{
  margin:.1rem 0 .4rem .65rem;
  border-left:2px solid #e5e7eb;
  counter-reset: toc-subsec;
}
.doc-toc ul ul li{
  counter-increment: toc-subsec;
}
.doc-toc ul ul a{
  font-weight:400;
  font-size:.88rem;
  color:#4b5563;
  padding:.22rem .5rem;
}
.doc-toc ul ul a::before{
  content: counter(toc-sec) "." counter(toc-subsec) " ";
  color:#6b7280;
  font-weight:600;
}

/* Content column */
.doc-content{
  flex:1 1 auto;
  min-width:0;
  background:#fff;
  border:1px solid #e5e7eb;
  border-radius:12px;
  padding:2rem 2.5rem;
}
.doc-content{
  counter-reset: doc-sec;
}
.doc-content section{
  margin-bottom:2.75rem;
  scroll-margin-top:90px;
  counter-increment: doc-sec;
  counter-reset: doc-subsec;
}
.doc-content section:last-child{
  margin-bottom:0;
}
.doc-content h2{
  font-size:1.6rem;
  font-weight:800;
  margin:0 0 1rem 0;
  padding-bottom:.5rem;
  border-bottom:2px solid #E9ECF7;
  color:#0F1E57;
}
.doc-content h2::before{
  content: counter(doc-sec) ". ";
}
.doc-content h3{
  font-size:1.2rem;
  font-weight:700;
  margin:1.75rem 0 .6rem 0;
  color:#142E94;
  scroll-margin-top:90px;
  counter-increment: doc-subsec;
}
.doc-content h3::before{
  content: counter(doc-sec) "." counter(doc-subsec) " ";
}
.doc-content p{
  margin:0 0 1rem 0;
  text-align:justify;
  hyphens:auto;
}
.doc-content ul, .doc-content ol{
  margin:0 0 1rem 1.4rem;
  padding:0;
}
.doc-content li{
  margin-bottom:.35rem;
}
.doc-eq{
  display:block;
  background:#F3F4F6;
  border-left:3px solid #142E94;
  border-radius:6px;
  padding:1rem 1.3rem .6rem 1.3rem;
  margin:0 0 1.2rem 0;
  overflow-x:auto;
  text-align:center;
}
.doc-eq .katex-display{
  margin:0;
}
.doc-note{
  background:#F3F4F6;
  border-radius:8px;
  padding:1rem 1.2rem;
  font-size:.92rem;
  color:#4b5563;
  margin:0 0 1rem 0;
}
.doc-flow-groups{
  display:grid;
  grid-template-columns:repeat(3, 1fr);
  gap:1.25rem;
  margin:0 0 1.2rem 0;
}
.doc-flow-group{
  background:#F3F4F6;
  border-radius:10px;
  padding:1.2rem 1.3rem;
}
.doc-flow-group h4{
  margin:0 0 .9rem 0;
  font-size:.82rem;
  font-weight:700;
  text-transform:uppercase;
  letter-spacing:.03em;
  color:#6b7280;
}
.doc-flow-group ul{
  list-style:none;
  margin:0;
  padding:0;
}
.doc-flow-group li{
  margin:0 0 .9rem 0;
}
.doc-flow-group li:last-child{
  margin-bottom:0;
}
.doc-flow-label{
  display:block;
  font-size:.92rem;
  font-weight:700;
  color:#142E94;
}
.doc-flow-desc{
  display:block;
  font-size:.88rem;
  color:#4b5563;
}
@media (max-width: 900px){
  .doc-flow-groups{
    grid-template-columns:1fr;
  }
}
.doc-source{
  margin-top:3rem;
  padding-top:1.25rem;
  border-top:1px solid #e5e7eb;
  font-size:.9rem;
  color:#6b7280;
}

/* Mobile */
@media (max-width: 900px){
  .doc-layout{
    flex-direction:column;
  }
  .doc-toc{
    position:static;
    width:100%;
    max-height:none;
  }
  .doc-content{
    padding:1.5rem;
    width:100%;
  }
}

/* Dark mode */
html.dark .doc-toc,
html.dark .doc-content{
  background:#1f2027;
  border-color:#3f3f46;
}
html.dark .doc-toc .doc-toc-title{
  color:#9ca3af;
}
html.dark .doc-toc a{
  color:#d1d5db;
}
html.dark .doc-toc a:hover{
  background:#112573;
  color:#A0AFE9;
}
html.dark .doc-toc ul ul{
  border-left-color:#3f3f46;
}
html.dark .doc-toc ul ul a{
  color:#9ca3af;
}
html.dark .doc-content h2{
  color:#A0AFE9;
  border-bottom-color:#112573;
}
html.dark .doc-content h3{
  color:#6981E2;
}
html.dark .doc-eq{
  background:#17181c;
  border-left-color:#6981E2;
  color:#d1d5db;
}
html.dark .doc-note{
  background:#17181c;
  color:#9ca3af;
}
html.dark .doc-flow-group{
  background:#17181c;
}
html.dark .doc-flow-label{
  color:#A0AFE9;
}
html.dark .doc-flow-desc{
  color:#9ca3af;
}
html.dark .doc-source{
  border-top-color:#3f3f46;
  color:#9ca3af;
}
</style>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.16.9/katex.min.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.16.9/katex.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.16.9/contrib/auto-render.min.js"></script>
<script>
document.addEventListener("DOMContentLoaded", function() {
  if (window.renderMathInElement) {
    renderMathInElement(document.querySelector(".doc-content"), {
      delimiters: [
        {left: "$$", right: "$$", display: true},
        {left: "$", right: "$", display: false}
      ],
      throwOnError: false
    });
  }
});
</script>

<p style="text-align:justify;">
This page documents the <strong>DSK&#8209;SFC</strong> model &mdash; the stock&#8209;flow consistent, agent&#8211;based integrated assessment model developed at the Institute of Economics of the Scuola Superiore Sant'Anna. It summarises the model's structure, the behavioural rules of each class of agent, its accounting framework and its climate module, drawing on the full model description published in Reissl, Fierro, Lamperti &amp; Roventini (2025), <em>"The DSK stock&#8211;flow consistent agent&#8211;based integrated assessment model"</em>, Ecological Economics.
</p>

<div class="doc-layout">

<nav class="doc-toc">
<div class="doc-toc-title">Contents</div>
<ul>
<li><a href="#overview">Overview</a></li>
<li><a href="#structure">Model structure &amp; sequence of events</a></li>
<li><a href="#households">Households</a></li>
<li><a href="#kfirms">Capital good firms (K&#8209;Firms)</a>
<ul>
<li><a href="#kfirms-production">Production &amp; labour demand</a></li>
<li><a href="#kfirms-market">Capital good market dynamics</a></li>
<li><a href="#kfirms-techchange">Technological change</a></li>
<li><a href="#kfirms-profits">Profits, dividends &amp; exit</a></li>
</ul>
</li>
<li><a href="#cfirms">Consumption good firms (C&#8209;Firms)</a>
<ul>
<li><a href="#cfirms-production">Desired production &amp; investment</a></li>
<li><a href="#cfirms-pricing">Pricing &amp; production cost</a></li>
<li><a href="#cfirms-credit">Credit &amp; financing</a></li>
<li><a href="#cfirms-market">Competitiveness &amp; the consumption good market</a></li>
<li><a href="#cfirms-exit">Profits, dividends &amp; failure</a></li>
</ul>
</li>
<li><a href="#entry-exit">Firm exit &amp; entry</a></li>
<li><a href="#banks">Banks</a></li>
<li><a href="#government">Government</a></li>
<li><a href="#centralbank">Central bank</a></li>
<li><a href="#energy">Energy sector</a></li>
<li><a href="#fossil">Fossil fuel sector</a></li>
<li><a href="#climate">Climate</a>
<ul>
<li><a href="#climate-modules">The two climate modules</a></li>
<li><a href="#climate-shocks">Climate impact shocks</a></li>
</ul>
</li>
<li><a href="#aggregation">Aggregation &amp; stock&#8209;flow consistency</a></li>
<li><a href="#calibration">Calibration &amp; validation</a></li>
<li><a href="#further">Further reading</a></li>
</ul>
</nav>

<div class="doc-content">

<section id="overview">
<h2>Overview</h2>
<p>
DSK&#8209;SFC is an updated, fully stock&#8211;flow consistent version of the <em>"Dystopian Schumpeter meeting Keynes"</em> (DSK) agent&#8211;based integrated assessment model, part of the wider <em>"Schumpeter meeting Keynes"</em> (K+S) family of models. It is, to date, the first integrated assessment model to combine full stock&#8211;flow consistency, heterogeneous interacting agents, bottom&#8211;up (micro&#8211;level) climate damages, and endogenous GDP growth with cyclical fluctuations.
</p>
<p>
Unlike conventional, equilibrium&#8211;based integrated assessment models, DSK&#8209;SFC does not assume perfect foresight, rational expectations or market clearing. Instead, heterogeneous firms, banks, households, the energy sector and the government follow bounded&#8211;rational behavioural rules and interact directly in decentralised markets, so that business cycles, financial fragility and climate&#8211;economy feedbacks all emerge endogenously from the bottom up. Embedding the model in a fully specified accounting system makes it possible to track every balance sheet item and financial flow explicitly and consistently throughout a simulation, enabling a systemic analysis of how climate change and climate policy affect sectoral balance sheets and financial stability.
</p>
<p>
The model economy consists of nine types of agents / sectors: a household sector, heterogeneous capital&#8211;good firms, heterogeneous consumption&#8211;good firms, a heterogeneous banking sector, a government, a central bank, an energy sector, a fossil fuel sector, and a climate module. The rest of this page walks through each of these building blocks, the accounting structure that ties them together, and the climate shock channels through which physical and transition risks feed back into the economy.
</p>
</section>

<section id="structure">
<h2>Model structure &amp; sequence of events</h2>
<p>
Capital&#8211;good firms (K&#8211;Firms) sell heterogeneous capital goods to consumption&#8211;good firms (C&#8211;Firms), which combine capital, labour and energy to produce a homogeneous consumption good purchased by households. Firms finance production and investment out of retained earnings and, for C&#8211;Firms, bank loans. Households supply labour, consume, and hold their savings as bank deposits. The government levies taxes and pays unemployment benefits (and, where activated, a carbon tax), while the central bank sets the policy rate and supplies the reserves needed to settle interbank payments. An energy sector supplies both firm sectors with green or brown energy, purchasing fossil fuel inputs from a dedicated fossil fuel sector when brown generation is used. A climate module translates the economy's cumulative emissions into a global temperature anomaly, which in turn determines the size and frequency of climate damage shocks fed back into the real economy.
</p>
<p>The main flows connecting sectors are:</p>
<div class="doc-flow-groups">
<div class="doc-flow-group">
<h4>Climate &amp; resources</h4>
<ul>
<li><span class="doc-flow-label">Emissions</span><span class="doc-flow-desc">firms &amp; energy sector &rarr; climate</span></li>
<li><span class="doc-flow-label">Climate shocks</span><span class="doc-flow-desc">climate &rarr; firms, energy, households</span></li>
<li><span class="doc-flow-label">Energy</span><span class="doc-flow-desc">energy sector &rarr; K&#8211;Firms &amp; C&#8211;Firms</span></li>
<li><span class="doc-flow-label">Fossil fuels</span><span class="doc-flow-desc">fossil fuel sector &rarr; energy sector</span></li>
</ul>
</div>
<div class="doc-flow-group">
<h4>Goods &amp; labour</h4>
<ul>
<li><span class="doc-flow-label">Labour</span><span class="doc-flow-desc">households &rarr; firms &amp; energy sector</span></li>
<li><span class="doc-flow-label">Consumption goods</span><span class="doc-flow-desc">C&#8211;Firms &rarr; households</span></li>
<li><span class="doc-flow-label">Capital goods</span><span class="doc-flow-desc">K&#8211;Firms &rarr; C&#8211;Firms</span></li>
</ul>
</div>
<div class="doc-flow-group">
<h4>Financial flows</h4>
<ul>
<li><span class="doc-flow-label">Deposits</span><span class="doc-flow-desc">all sectors &harr; banks</span></li>
<li><span class="doc-flow-label">Loans</span><span class="doc-flow-desc">banks &rarr; C&#8211;Firms</span></li>
<li><span class="doc-flow-label">Bonds</span><span class="doc-flow-desc">government &harr; banks &amp; central bank</span></li>
<li><span class="doc-flow-label">Reserves &amp; advances</span><span class="doc-flow-desc">central bank &harr; banks</span></li>
</ul>
</div>
</div>
<p>
Within every simulated period, events unfold in a fixed sequence so that agents always act on information that is actually available to them (e.g. the current wage is known when prices are set, but the current energy price is not). At quarterly frequency the climate module is called once every four periods. The full sequence is:
</p>
<ol>
<li>Banks pay interest on deposits held at the end of the previous period.</li>
<li>If active, the carbon tax is updated.</li>
<li>C&#8211;Firms receive capital goods ordered in the previous period.</li>
<li>C&#8211;Firms and K&#8211;Firms compute unit costs and set prices.</li>
<li>Banks determine the maximum credit they are willing to extend.</li>
<li>Banks set loan interest rates for their customers.</li>
<li>K&#8211;Firms send brochures to attract new clients; the K&#8211;Firm/C&#8211;Firm network updates.</li>
<li>C&#8211;Firms form expected demand and desired production.</li>
<li>C&#8211;Firms earmark worn&#8211;out machines and decide on technological substitution.</li>
<li>C&#8211;Firms set desired capital stock and desired expansion investment.</li>
<li>C&#8211;Firms compute effective production cost.</li>
<li>C&#8211;Firms determine internal financing and maximum willingness to borrow, scaling back investment if needed.</li>
<li>Bank credit is allocated; credit&#8211;rationed firms scale back investment/production; firms unable to roll over loans exit.</li>
<li>C&#8211;Firms and K&#8211;Firms compute labour demand for production.</li>
<li>Total labour demand (incl. R&amp;D and energy capacity expansion) is calculated and, if it exceeds labour supply, production is scaled back.</li>
<li>Unemployment and unemployment benefits are calculated.</li>
<li>Production takes place; energy demand and industrial emissions are computed.</li>
<li>Expansion investment, R&amp;D and energy production take place in the energy sector.</li>
<li>C&#8211;Firms pay for investment.</li>
<li>C&#8211;Firms, K&#8211;Firms and the energy sector pay wages; the government pays unemployment benefits.</li>
<li>Fully depreciated machines are scrapped.</li>
<li>C&#8211;Firms' competitiveness and ex&#8211;ante market shares are computed; very low&#8211;share firms become inactive.</li>
<li>K&#8211;Firm profits are computed; K&#8211;Firms pay energy, taxes and dividends.</li>
<li>Households pay taxes and compute desired consumption.</li>
<li>Consumption expenditure is allocated across C&#8211;Firms.</li>
<li>K&#8211;Firm and C&#8211;Firm profits are finalised.</li>
<li>C&#8211;Firms pay energy, loan service and taxes; those unable to do so, or with negative equity, exit.</li>
<li>Energy sector profits are computed; it pays for fossil fuel input and taxes; the fossil fuel sector pays dividends to households.</li>
<li>Macroeconomic aggregates and averages are computed.</li>
<li>The nominal wage rate is updated.</li>
<li>Exiting C&#8211;Firms and K&#8211;Firms are replaced by new entrants.</li>
<li>Bank profits are computed; banks pay taxes and dividends.</li>
<li>Banks with negative equity are bailed out or taken over.</li>
<li>The government budget is computed; deficits are covered by new bonds.</li>
<li>The central bank sets next period's policy rate.</li>
<li>Net reserve flows are settled; banks may take central bank advances.</li>
<li>Endogenous technological change takes place in the K&#8211;Firm sector.</li>
<li>The climate module is updated with current&#8211;period emissions.</li>
<li>The fossil fuel price and the energy sector mark&#8211;up are reset for next period.</li>
</ol>
</section>

<section id="households">
<h2>Households</h2>
<p>
Households are modelled as a single aggregate entity. They receive four sources of income: wages, dividends (from C&#8211;Firms, K&#8211;Firms, the energy and fossil fuel sectors, and banks), unemployment benefits, and interest on bank deposits. Households supply any amount of labour demanded at the prevailing nominal wage, up to an exogenously growing maximum (the labour force); any labour not employed is compensated with an unemployment benefit set as a fixed replacement rate of the current wage.
</p>
<p>
Desired nominal consumption is a linear function of disposable wage and benefit income, dividend and interest income, and the stock of accumulated deposits, each entering with its own marginal propensity to consume &mdash; households cannot borrow to finance consumption, so desired consumption is capped by the stock of deposits they hold. All household saving accumulates as bank deposits, distributed across individual banks in proportion to each bank's share of firm customers.
</p>
<div class="doc-eq">
$$C_{d,t} = \alpha_1\big(W_t + UB_t - Tax_t^{H}\big) + \alpha_2\big(Div_{t-1} + iD_{h,t}\big) + \alpha_3 D_{h,t-1}$$
</div>
<p>
where <span>$\alpha_1$</span>, <span>$\alpha_2$</span> and <span>$\alpha_3$</span> are the (generally different) marginal propensities to consume out of wage/benefit income, dividend/interest income, and accumulated wealth, respectively.
</p>
<p>
The nominal wage follows a Phillips&#8211;curve&#8211;type rule at the end of every period: it responds positively to the gap between current inflation and the central bank's inflation target and to recent productivity growth, and negatively to changes in the unemployment rate, subject to an exogenous cap on the maximum per&#8211;period percentage change.
</p>
<div class="doc-eq">
$$w_{t+1} = (1+\omega_t)\,w_t, \qquad \omega_t = \min\!\Big(\overline{\omega},\ \max\big(-\overline{\omega},\ \ \pi^{*} + \psi_1\hat\pi_t + \psi_2\widehat{Pr}_t - \psi_3\hat U_t\big)\Big)$$
</div>
<p>
<span>$\hat\pi_t$</span> is the deviation of current inflation from the target <span>$\pi^{*}$</span>, <span>$\widehat{Pr}_t$</span> is a weighted average of recent productivity growth, <span>$\hat U_t$</span> is the change in unemployment, and <span>$\overline{\omega}$</span> bounds how much the wage can move in a single period.
</p>
</section>

<section id="kfirms">
<h2>Capital good firms (K&#8211;Firms)</h2>
<p>
K&#8211;Firms produce heterogeneous capital goods on demand and compete on price and quality. Each K&#8211;Firm produces a single current "vintage" of capital good, characterised by a labour productivity, an energy efficiency, and an environmental friendliness (emissions per unit of energy used), alongside its own, separately evolving, production technique with the same three characteristics. A capital good's vintage and its age (versus a fixed maximum machine lifespan) jointly determine how long it can remain in use at a C&#8211;Firm.
</p>

<h3 id="kfirms-production">Production &amp; labour demand</h3>
<p>
K&#8211;Firms produce to order: they receive orders in period <em>t</em>, manufacture them in <em>t</em>, and deliver in <em>t+1</em>, so they never hold inventories. Labour and energy demand for production are computed directly from the quantity ordered and the firm's current labour productivity and energy efficiency, and emissions from production are assumed proportional to energy use.
</p>
<div class="doc-eq">
$$L^{d}_{k,t} = \frac{Q_{k,t}}{Pr_{k,t}\,\mathfrak{a}}, \qquad En^{d}_{k,t} = \frac{Q_{k,t}}{EE_{k,t}}, \qquad Em_{k,t} = \frac{EF_{k,t}}{EE_{k,t}}\,Q_{k,t}$$
</div>

<h3 id="kfirms-market">Capital good market dynamics</h3>
<p>
K&#8211;Firms set prices with a fixed, homogeneous mark&#8211;up over unit production cost (wage cost, energy cost and any carbon tax on the sector). Each period, every K&#8211;Firm sends a number of "brochures" &mdash; proportional to its current client base &mdash; to randomly selected C&#8211;Firms, advertising the price and characteristics of its vintage. Every C&#8211;Firm, whether or not it plans to invest that period, compares the brochures it has received using an <em>attractiveness</em> measure that combines a vintage's price with the unit production cost it would imply, discounted by an exogenous payback parameter, and selects the supplier offering the best trade&#8211;off between price and quality.
</p>
<div class="doc-eq">
$$uc_{k,t} = \frac{w_t}{Pr_{k,t}\,\mathfrak{a}} + \frac{p_{e,t-1}}{EE_{k,t}} + \tau_t^{Em,K}\frac{EF_{k,t}}{EE_{k,t}}, \qquad p_{k,t} = (1+\mu^{K})\,uc_{k,t}$$
</div>
<p>
A capital vintage's attractiveness &mdash; used both by C&#8211;Firms choosing a supplier and by K&#8211;Firms deciding whether to adopt a new technology &mdash; combines its price and the unit cost it implies, discounted by a payback parameter <span>$b$</span>:
</p>
<div class="doc-eq">
$$A_{\kappa,t} = p_{k,t} + uc_{\kappa,t}\,b$$
</div>

<h3 id="kfirms-techchange">Technological change</h3>
<p>
Technological progress is driven by a two&#8211;step innovation/imitation process. Each K&#8211;Firm devotes a fixed share of its revenue to R&amp;D, split between innovation and imitation effort; the probability of a successful innovation or imitation in a given period increases with the respective R&amp;D input. If innovation succeeds, the labour productivity, energy efficiency and environmental friendliness of both the firm's vintage and its production technique are each perturbed by an independent random draw &mdash; which can be positive or negative, capturing the trial&#8211;and&#8211;error nature of innovation. If imitation succeeds, the firm copies the technology of a competitor, with the probability of imitating any given rival increasing in their technological proximity. A firm then compares its existing technology to any newly innovated or imitated one using the same attractiveness measure used by C&#8211;Firms, and adopts whichever offers the best price&#8211;quality trade&#8211;off &mdash; so a new technology need not dominate the old one along every dimension to be adopted.
</p>
<div class="doc-eq">
$$P(Innovate)_{k,t} = 1-\exp\!\big(-\mathfrak{b}_1^{K}\,RD^{in}_{k,t}\big), \qquad P(Imitate)_{k,t} = 1-\exp\!\big(-\mathfrak{b}_2^{K}\,RD^{im}_{k,t}\big)$$
</div>

<h3 id="kfirms-profits">Profits, dividends &amp; exit</h3>
<p>
K&#8211;Firm profits equal sales revenue and deposit interest, less wages, energy costs and any carbon tax; positive profits are taxed at a flat rate, and a fixed share of post&#8211;tax profits is paid out as dividends, with the remainder retained as bank deposits (K&#8211;Firms cannot borrow). A K&#8211;Firm exits the model if it loses all of its C&#8211;Firm customers, or if it becomes unable to meet its energy or wage payment obligations &mdash; which can occur because firms must set prices using the lagged energy price, so an energy price spike can leave a firm unable to fully cover its current energy bill.
</p>
</section>

<section id="cfirms">
<h2>Consumption good firms (C&#8211;Firms)</h2>
<p>
C&#8211;Firms produce a single, homogeneous consumption good from heterogeneous combinations of capital, labour and energy; because the good itself is homogeneous, firms compete purely on price and on their ability to satisfy the demand they receive.
</p>

<h3 id="cfirms-production">Desired production &amp; investment</h3>
<p>
Expected demand follows an adaptive rule based on past realised demand, and desired production is set to meet this expectation plus a desired buffer of inventories, net of existing stock. If a firm's current productive capacity cannot support desired production, output is scaled back to what the installed capital stock can deliver. C&#8211;Firms carry out two distinct types of investment: <em>expansion investment</em>, sized to reach a target capacity&#8211;utilisation rate for the capital stock needed to meet desired production (subject to a maximum per&#8211;period expansion rate), and <em>substitution investment</em>, which replaces machines that are not yet worn out but have become technologically obsolete relative to the vintage currently offered by the firm's supplier &mdash; judged using the same price/unit&#8211;cost payback comparison described above.
</p>
<div class="doc-eq">
$$Dem^{e}_{c,t} = \sigma\,Dem_{c,t-1} + (1-\sigma)\,Dem^{e}_{c,t-1}, \qquad Q^{d}_{c,t} = Dem^{e}_{c,t} + N^{d}_{c,t} - N_{c,t-1}, \qquad \mathfrak{K}^{d}_{c,t} = \frac{Q^{d}_{c,t}}{u}$$
</div>

<h3 id="cfirms-pricing">Pricing &amp; production cost</h3>
<p>
Each C&#8211;Firm's unit cost of production is a weighted average of the unit costs implied by every capital vintage currently in its heterogeneous capital stock, weighted by each vintage's share of output. Prices are set as a mark&#8211;up on unit cost; the mark&#8211;up itself evolves adaptively, rising when a firm's market share is growing and falling when it is shrinking.
</p>
<div class="doc-eq">
$$p_{c,t} = (1+\mu_{c,t})\,uc_{c,t}, \qquad \mu_{c,t} = \mu_{c,t-1}\big(1+\Delta^{\mu}\,\hat f_{c,t-1}\big), \qquad uc_{c,t} = \sum_{\kappa\in\Phi_{\kappa,c,t}} uc_{\kappa,t}\,\frac{\mathfrak{K}_{\kappa,c,t}}{\mathfrak{K}_{c,t}}$$
</div>

<h3 id="cfirms-credit">Credit &amp; financing</h3>
<p>
C&#8211;Firms finance production and investment from retained earnings (bank deposits) and bank loans. Each firm has an internal ceiling on how much additional credit it is willing to take on, set as a multiple of its recent net revenue net of its existing loan stock; if desired investment exceeds internal funds plus this self&#8211;imposed ceiling, substitution investment is cut first, followed by expansion investment. A firm may be further constrained if its bank is unwilling to lend as much as it demands, in which case planned expenditures &mdash; and, in the last resort, planned production itself &mdash; are reduced until they can be financed.
</p>
<div class="doc-eq">
$$\mathfrak{c}^{d,max}_{c,t} = \max\big(0,\ \phi\,NR_{c,t-1} - \mathfrak{l}_{c,t-1}\big)$$
</div>

<h3 id="cfirms-market">Competitiveness &amp; the consumption good market</h3>
<p>
Each C&#8211;Firm's competitiveness depends negatively on its price relative to the sector average and on how much unmet demand it left unsatisfied in the previous period. Competitiveness feeds into a quasi&#8211;replicator dynamic that updates market shares period&#8211;to&#8211;period (subject to a maximum rate of change), after which households' aggregate consumption demand is distributed to firms over multiple rounds: a firm's demand is reduced in proportion to its market share, and any demand it cannot satisfy from current output and inventories is reallocated to other firms in the next round, continuing until either demand is exhausted or no firm has output left to sell.
</p>
<div class="doc-eq">
$$E_{c,t} = -\left(\frac{p_{c,t}}{\hat p_t}\right)^{\omega_1} - \left(\frac{l_{c,t}}{\hat l_t}\right)^{\omega_2}, \qquad \tilde f_{c,t} = f_{c,t-1}\left(\frac{2\omega_3}{1+e^{-\chi\frac{E_{c,t}-\hat E_t}{\hat E_t}}} + (1-\omega_3)\right)$$
</div>

<h3 id="cfirms-exit">Profits, dividends &amp; failure</h3>
<p>
Profits reflect sales, deposit interest, and the revaluation of inventories and capital, net of investment, wages, energy costs, loan interest and carbon tax; positive profits are taxed, and a fixed share of the remainder is paid as dividends, with the rest held as deposits. In addition to interest, C&#8211;Firms must repay a fixed share of outstanding loans every period, effectively making bank credit resemble a revolving credit line. A C&#8211;Firm exits the model if it cannot meet a payment obligation (to the energy sector, on its loans, or &mdash; more rarely &mdash; on taxes), if its market share falls below a minimum threshold, or if its net worth turns negative.
</p>
</section>

<section id="entry-exit">
<h2>Firm exit &amp; entry</h2>
<p>
Every firm that exits is replaced one&#8211;for&#8211;one by a new entrant in the same sector at the end of the period, so the number of K&#8211;Firms and C&#8211;Firms is constant throughout a simulation. An entering K&#8211;Firm copies the technology and price of a randomly drawn surviving incumbent and receives a transfer of deposits from the household sector to provide initial liquidity.
</p>
<p>
C&#8211;Firm replacement is more involved, since C&#8211;Firms hold multiple asset types. If an exiting firm's deposits exceed its loans, the loans are repaid and any residual is transferred to households; otherwise the shortfall is recorded as a bank loss. Remaining capital goods pass through a stylised second&#8211;hand market: machines are revalued according to their remaining lifespan, and either transferred to households directly (if the exiting firm's loans were fully repaid) or taken over by its bank and subsequently resold, reducing the firm's outstanding debt. Entering firms are then endowed with machines drawn from this second&#8211;hand pool, an initial deposit transfer from households, a randomly assigned capital goods supplier, and an initial market share equal to the aggregate share vacated by exiting firms, allocated across new entrants in proportion to their relative price competitiveness.
</p>
</section>

<section id="banks">
<h2>Banks</h2>
<p>
The banking sector comprises multiple individual banks, functionally identical but heterogeneous in the number of K&#8211;Firm and C&#8211;Firm customers assigned to them at initialisation (drawn from a truncated Pareto distribution, producing a realistically right&#8211;skewed size distribution). The firm&#8211;bank network is static except when a bank fails. Household and energy&#8211;sector deposits &mdash; which are aggregate quantities &mdash; are distributed across banks in proportion to each bank's share of firm customers.
</p>
<p>
On the liability side, deposits are remunerated at a uniform rate set as a mark&#8211;down on the central bank's deposit rate. On the asset side, each bank caps its total lending at a multiple of its own net worth &mdash; a "credit multiplier" that can be made to rise endogenously with a bank's financial fragility (recent default losses relative to net worth). Within that overall ceiling, a bank ranks its C&#8211;Firm borrowers by their debt&#8211;service&#8211;to&#8211;revenue ratio, charges riskier customers a higher mark&#8211;up over its baseline loan rate, and rations credit to the least credit&#8211;worthy customers first if aggregate demand exceeds its lending capacity. Banks also hold government bonds in proportion to their loan book.
</p>
<div class="doc-eq">
$$\mathfrak{C}^{s}_{b,t} = \frac{NW_{b,t}}{buffer_{b,t}}, \qquad buffer_{b,t} = cm\,(1+\mathfrak{v}\,fragility_{b,t}), \qquad r^{l}_{b,c,t} = r^{l}_{b,t}\big(1+(rank_{c,t}-1)\,\mathfrak{M}\big)$$
</div>
<p>
Bank profits comprise interest income on loans, government bonds and reserves, net of interest paid on deposits and central bank advances, loan losses, and any losses from financing firm entry; positive profits are taxed and partly distributed as dividends. A bank whose net worth turns negative fails: depending on the simulation setting, it is either always bailed out by the government, or &mdash; where feasible &mdash; acquired, assets and customers included, by the surviving bank with the largest net worth, with a government bailout only as a backstop.
</p>
</section>

<section id="government">
<h2>Government</h2>
<p>
The government levies flat&#8211;rate taxes on household wage income, on the positive profits of C&#8211;Firms, K&#8211;Firms and banks, and &mdash; where a climate policy scenario is active &mdash; a carbon tax per unit of emissions on firms and/or the energy sector, which can be set to grow at a constant real rate, linearly, exponentially, or in line with nominal GDP. The model does not include a dedicated carbon&#8211;revenue recycling mechanism by default: carbon tax receipts enter the public budget like any other tax revenue (though recycling schemes are a natural extension, explored in companion work).
</p>
<p>
On the expenditure side, the government pays unemployment benefits (a fixed share of the current wage per unit of unemployed labour), may fund firm entry costs that households' deposits cannot cover, may bail out failing banks, and pays interest on outstanding government bonds. Any budget deficit is financed by issuing new bonds, offered first to banks and, for any unsold residual, absorbed by the central bank; a fixed share of outstanding bonds is repaid every period (more if the budget allows).
</p>
<div class="doc-eq">
$$UB_t = \zeta\,w_t\,\big(LS_t - L_t\big)$$
</div>
</section>

<section id="centralbank">
<h2>Central bank</h2>
<p>
The central bank sets its policy (lending) rate via a Taylor&#8211;type rule that responds to the gap between current inflation and an exogenous inflation target and to the gap between unemployment and a target unemployment rate, subject to interest&#8211;rate smoothing and a lower bound near zero; the deposit rate is a fixed mark&#8211;down on the lending rate, and all other interest rates in the model (loans, government bonds, bank deposits) are tied to these two central bank rates via exogenous or endogenous mark&#8211;ups and mark&#8211;downs.
</p>
<div class="doc-eq">
$$r^{l}_{CB,t} = \max\!\Big(\underline{r},\ \ \iota_1 r^{l}_{CB,t-1} + (1-\iota_1)\big(\bar r + \iota_2(\pi^{a}_t-\pi^{*}) + \iota_3(U^{*}-U_t)\big)\Big)$$
</div>
<p>
The central bank also maintains the payments system: rather than modelling an explicit interbank market, net reserve in&#8211; and outflows are settled automatically at the end of each period, with banks short of reserves able to borrow advances on demand at the policy rate.
</p>
</section>

<section id="energy">
<h2>Energy sector</h2>
<p>
A single representative energy sector supplies the (fully demand&#8211;determined) energy needs of K&#8211;Firms and C&#8211;Firms, and can expand its productive capacity instantaneously whenever required. Capacity is split between "brown" (fossil&#8211;fuel&#8211;based, emitting) and "green" (clean) technology, each available in multiple vintages. Green generation is stylised as costless to run but costly to build; brown generation is the reverse &mdash; free to build but requiring a costly fossil&#8211;fuel input (and incurring any applicable carbon tax) to run. Depending on the simulation setting, the mix of new capacity can be chosen purely on relative cost, cost&#8211;minimising subject to bounds on green capacity growth and a minimum green share, or fixed exogenously.
</p>
<p>
Energy is dispatched in merit order: free green capacity is always activated first, with brown plants brought online &mdash; from the cheapest vintage up &mdash; only if green supply is insufficient. The uniform price charged to all firms is a mark&#8211;up over the marginal cost of the last (least efficient) plant dispatched, with the mark&#8211;up itself drifting with the nominal wage to keep the real price of energy broadly stable. The energy sector invests a fixed share of revenue in R&amp;D, directed at improving the thermal efficiency and emission intensity of brown technology and the capacity cost of green technology, following the same stochastic innovation logic used for K&#8211;Firms (adopted only if the resulting cost is lower).
</p>
<div class="doc-eq">
$$p_{e,t} = \mu_{e,t} + mc_{e,t}, \qquad c_{\kappa^{de},t} = \frac{p_{f,t-1}}{TE_{\kappa^{de}}} + \tau_t^{Em,E}\,EF_{\kappa^{de}}$$
</div>
<p>
A new unit of brown capacity is built instead of green capacity whenever the cheapest brown vintage's running cost undercuts the cheapest green vintage's amortised capacity cost (payback period <span>$b^{e}$</span>):
</p>
<div class="doc-eq">
$$c^{min}_{\kappa^{de},t} \ <\ \frac{c^{min}_{\kappa^{ge},t}}{b^{e}}$$
</div>
</section>

<section id="fossil">
<h2>Fossil fuel sector</h2>
<p>
A stylised, aggregate fossil fuel sector sells fuel to the energy sector at zero production cost, with its price drifting in line with the nominal wage so that, absent shocks, it carries no secular trend relative to the rest of the economy. Deliberately kept separate from the domestic banking system &mdash; it settles payments through a dedicated, non&#8211;interest&#8211;bearing reserve account at the central bank &mdash; the sector is designed to mimic an external fuel supplier when the model is calibrated to a single region such as the European Union. Since its costs are zero, its revenue is its profit; a small, fixed share of its accumulated wealth is paid out to households each period, keeping it from indefinitely draining financial resources from the rest of the economy.
</p>
</section>

<section id="climate">
<h2>Climate</h2>
<p>
Endogenous emissions from capital good production, consumption good production and energy generation (plus, where the model is calibrated to a sub&#8211;global region, an exogenous "rest of the world" emissions trajectory) feed a climate module that returns a single, central output: a global temperature anomaly, used in turn to size climate damage shocks fed back into the economic model.
</p>

<h3 id="climate-modules">The two climate modules</h3>
<p>
Users can choose between two climate modules, both run at annual frequency. The simpler module derives the temperature anomaly as a linear function of cumulative emissions to date, following the approach of Matthews et al. (2009, 2012):
</p>
<div class="doc-eq">
$$Temp_t = \Upsilon_1 + \Upsilon_2\,\mathcal{E}^{\Sigma}_t$$
</div>
<p>
The more detailed module is a simplified version of the C&#8211;ROADS carbon&#8211;cycle model of Sterman et al. (2013): it tracks carbon stocks in the atmosphere, in multiple ocean layers, and in the terrestrial biosphere and humus, allows for carbon fertilisation and heat&#8211;stress effects on land carbon uptake, computes radiative forcing (including a non&#8211;CO&#8322; forcing adjustment) and the resulting heat uptake by the ocean, and derives the temperature anomaly from the heat content of the uppermost ocean layer:
</p>
<div class="doc-eq">
$$\mathcal{R}_t = \Lambda_1\Lambda_2\ln\!\left(\frac{\mathcal{C}^{at}_t}{\mathcal{C}^{at}_0}\right), \qquad Temp_t = \mathcal{T}^{oc}_{1,t} = \frac{\mathcal{H}^{oc}_{1,t}}{depth_1\,\Psi}$$
</div>

<h3 id="climate-shocks">Climate impact shocks</h3>
<p>
Whichever module is active, the resulting temperature anomaly determines the shape parameters of a Beta distribution from which climate shocks are drawn: as the anomaly rises, both the typical size of shocks and the thickness of the distribution's upper tail increase, so extreme events become both larger and more frequent as warming progresses &mdash; without assuming any particular functional form for the damage function itself.
</p>
<div class="doc-eq">
$$shock^{s}_t \sim Beta\big(S^{s}_{1,t},\,S^{s}_{2,t}\big), \qquad S^{s}_{1,t} = S^{s}_{1,0}\Big(1+\ln\tfrac{Temp_{t-1}}{Temp_0}\Big)^{\Upsilon^{s}_3}, \qquad S^{s}_{2,t} = S^{s}_{2,0}\Big(\tfrac{Temp_0}{Temp_{t-1}}\Big)^{\Upsilon^{s}_4}$$
</div>
<p> The model supports a wide range of impact channels, which can be switched on individually or in combination to explore different damage scenarios, including shocks to: current output of C&#8211;Firms and K&#8211;Firms, C&#8211;Firms' capital stock, inventories, the energy sector's productive capacity, the labour productivity and energy efficiency of capital vintages and production techniques (either as one&#8211;off output losses or as persistent, compounding damage to the technology frontier itself), K&#8211;Firms' R&amp;D effectiveness, aggregate consumption demand, and aggregate labour supply. Several channels are available in both an aggregate specification (applied as an average loss across randomly selected firms) and a fully micro&#8211;founded specification (an independent draw for every individual agent), allowing the distribution of climate damages across firms &mdash; and not just their aggregate size &mdash; to be examined directly.
</p>
</section>

<section id="aggregation">
<h2>Aggregation &amp; stock&#8211;flow consistency</h2>
<p>
Real GDP is measured as the sum of C&#8211;Firm output plus K&#8211;Firm output converted into comparable units via the maximum output producible per machine, with nominal GDP computed analogously at current prices.
</p>
<div class="doc-eq">
$$GDP_t = \sum_{c=1}^{N_2} Q_{c,t} + \mathfrak{Q}\sum_{k=1}^{N_1} Q_{k,t}$$
</div>
<p>
Aggregate employment is given by total realised labour demand (for production, R&amp;D, and energy capacity expansion) up to the current labour force, with any residual counted as unemployment. The consumption price index used for inflation and real&#8211;wage calculations is computed first from ex&#8211;ante market shares and then, after the consumption good market has cleared, recomputed from realised sales. Emissions are aggregated across K&#8211;Firms, C&#8211;Firms, the energy sector and any exogenous component, then rescaled into physically meaningful units (gigatonnes of carbon) before being passed to the active climate module.
</p>
<p>
Because every transaction and balance sheet position is tracked explicitly, the model can run a battery of internal consistency checks at the end of every period: that sectoral financial balances sum to zero in aggregate; that the sum of sectoral net worths equals the nominal value of all tangible assets (capital stock plus inventories); that net worth computed from stocks (assets minus liabilities) matches net worth computed from the accumulation of flows; and that balance sheet items tracked at both the individual&#8211;agent and sectoral level remain mutually consistent. These checks make it possible to confirm &mdash; as shown in the underlying paper &mdash; that sectoral net&#8211;worth&#8211;to&#8211;GDP ratios and sectoral financial balances exhibit no spurious long&#8211;run trend over a simulation, a basic sanity requirement for any stock&#8211;flow consistent model.
</p>
</section>

<section id="calibration">
<h2>Calibration &amp; validation</h2>
<p>
Model variables are initialised to fairly arbitrary but stock&#8211;flow&#8211;consistent values and then allowed to pass through a discarded "burn&#8211;in" transient before the reported simulation window begins, in line with common practice for macroeconomic agent&#8211;based models. Climate module parameters are validated against the IPCC AR6 scenario database, confirming that simulated temperature pathways for a range of emissions budgets fall within the range reported by integrated assessment models in the literature. The economic core is calibrated indirectly at quarterly frequency to reproduce qualitatively reasonable business&#8211;cycle dynamics, while the long&#8211;run growth rates of real GDP, industrial energy use and emissions are matched to a "Shared Socioeconomic Pathway 2" (SSP2, current&#8211;policy) trajectory for the European Union.
</p>
<p>
Under this calibration, the baseline model reproduces a wide set of qualitative stylised facts documented in the empirical macro and finance literature: endogenous growth with persistent business&#8211;cycle fluctuations; fat&#8211;tailed distributions of GDP and firm growth rates; plausible relative volatilities and cross&#8211;correlations among GDP, consumption, investment, employment and inflation; pro&#8211;cyclical private debt, R&amp;D investment, energy demand and emissions; a positive correlation between outstanding private debt and loan losses; lumpy firm&#8211;level investment; and persistent cross&#8211;firm heterogeneity in productivity, energy efficiency and emission intensity.
</p>
</section>

<section id="further">
<h2>Further reading</h2>
<p>
This page summarises the model; the full mathematical specification &mdash; every equation, parameter and initial value, together with the complete sequence of events, the full set of climate shock specifications, and the initialisation procedure &mdash; is given in Reissl, Fierro, Lamperti &amp; Roventini (2025). Earlier DSK model papers describing specific applications (climate&#8211;induced financial instability, green financial policy, decarbonisation and employment, and more) are listed on the <a href="/DSKmodel/publications/">Publications</a> page, and the model source code is available on <a href="/DSKmodel/access/">GitHub</a>.
</p>
<div class="doc-source">
Reissl, S., Fierro, L.E., Lamperti, F., Roventini, A. (2025). <em>The DSK stock&#8211;flow consistent agent&#8211;based integrated assessment model.</em> Ecological Economics. <a href="https://www.sciencedirect.com/science/article/pii/S0921800925001247">sciencedirect.com/science/article/pii/S0921800925001247</a>
</div>
</section>

</div>
</div>
