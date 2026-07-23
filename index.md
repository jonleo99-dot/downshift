<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>The Downshift — Automotive Digest</title>

  <!-- Google Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Fraunces:wght@600;700;900&family=Inter:wght@300;400;600&family=JetBrains+Mono:wght@400;600&display=swap" rel="stylesheet">

  <style>
    :root{
      --bg:#14171a;
      --paper:#f6efe6; /* warm off-white text backgrounds if needed */
      --text:#f0e9df;
      --muted:#9aa1a6;
      --amber:#e8a33d;
      --teal:#2aa39b;
      --red:#d84b4b;
      --card-bg: rgba(255,255,255,0.02);
      --rule: rgba(255,255,255,0.06);
      --max-w:920px;
      --mono: 'JetBrains Mono', monospace;
      --serif: 'Fraunces', serif;
      --sans: 'Inter', system-ui, sans-serif;
    }

    html,body{
      height:100%;
      background:var(--bg);
      color:var(--text);
      font-family:var(--sans);
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      margin:0;
      padding:32px 16px;
      line-height:1.45;
      font-size:16px;
    }

    .container{
      max-width:var(--max-w);
      margin:0 auto;
    }

    header.mast{
      display:flex;
      gap:24px;
      align-items:flex-start;
      border-bottom:1px solid var(--rule);
      padding-bottom:18px;
      margin-bottom:22px;
    }

    h1.brand{
      font-family:var(--serif);
      font-weight:900;
      letter-spacing:-0.02em;
      margin:0;
      font-size:44px;
      color:var(--paper);
    }

    h1.brand .shift{
      color:var(--amber);
      font-weight:900;
    }

    .mast-meta{
      margin-left:auto;
      text-align:right;
      font-size:14px;
      color:var(--muted);
      font-family:var(--sans);
    }

    .mast-meta .title{
      font-weight:600;
      color:var(--text);
      font-size:16px;
    }

    .mast-subline{
      display:block;
      margin-top:8px;
      font-family:var(--mono);
      text-transform:uppercase;
      font-size:12px;
      color:var(--muted);
      letter-spacing:0.08em;
    }

    main{
      margin-top:18px;
      display:grid;
      grid-template-columns: 1fr 320px;
      gap:28px;
    }

    @media (max-width:960px){
      main{ grid-template-columns: 1fr; }
      header.mast{ flex-direction:column; align-items:flex-start; gap:12px; }
      .mast-meta{ text-align:left; margin-left:0; }
    }

    .lede{
      background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent);
      padding:18px;
      border-radius:8px;
      border:1px solid var(--rule);
      margin-bottom:18px;
    }

    .section{
      margin-bottom:22px;
    }

    h2{
      font-family:var(--serif);
      margin:0 0 10px 0;
      font-size:20px;
      color:var(--paper);
    }

    p.lede-line{
      margin:0 0 10px 0;
      color:var(--text);
      font-weight:500;
    }

    .synthesis{
      color:var(--text);
      margin:0;
      font-size:15px;
    }

    .grid{
      display:grid;
      gap:12px;
    }

    /* By the Numbers */
    .numbers{
      display:grid;
      grid-template-columns: repeat(2,1fr);
      gap:10px;
      margin-top:8px;
    }

    .stat{
      background:var(--card-bg);
      border:1px solid var(--rule);
      padding:12px;
      border-radius:8px;
      font-size:14px;
    }
    .stat .n{
      font-family:var(--mono);
      font-weight:600;
      color:var(--amber);
      display:block;
      font-size:20px;
      margin-bottom:6px;
    }
    .stat .label{ color:var(--muted); font-size:13px; }

    /* Top Stories cards */
    .cards{
      display:grid;
      gap:12px;
    }
    .card{
      background:var(--card-bg);
      border:1px solid var(--rule);
      padding:14px;
      border-radius:8px;
    }
    .tag{
      display:inline-block;
      font-family:var(--mono);
      font-size:12px;
      padding:6px 8px;
      border-radius:6px;
      color:#111;
      background:var(--muted);
      font-weight:700;
    }

    .tag.market{ background: linear-gradient(90deg,var(--amber),#d89b2f); color:#111; }
    .tag.launch{ background: linear-gradient(90deg,var(--teal),#1f8f88); color:#021914; }
    .tag.tech{ background: linear-gradient(90deg,#7fd6d0,#2aa39b); color:#021914; }
    .tag.supply{ background: linear-gradient(90deg,#7a7f86,#6a7076); color:#fff; }
    .tag.dealer{ background: linear-gradient(90deg,#ffb57a,#e8a33d); color:#111; }

    .card h3{
      margin:10px 0 8px 0;
      font-family:var(--serif);
      font-size:18px;
      color:var(--paper);
    }
    .summary{
      color:var(--text);
      margin:0 0 8px 0;
      font-size:14px;
    }
    .meta{
      color:var(--muted);
      font-size:13px;
      margin-bottom:8px;
    }
    .importance{
      display:inline-block;
      font-family:var(--mono);
      font-size:12px;
      background:rgba(0,0,0,0.2);
      padding:4px 8px;
      border-radius:6px;
      color:var(--amber);
      margin-left:8px;
    }

    ul.bullets{
      margin:8px 0 0 18px;
      color:var(--text);
      font-size:14px;
      line-height:1.45;
    }

    aside.sidebar{ position:relative; top:0; }

    .small{
      font-size:13px;
      color:var(--muted);
    }

    footer{
      border-top:1px solid var(--rule);
      padding-top:14px;
      margin-top:26px;
      color:var(--muted);
      font-size:13px;
      text-align:center;
    }

  </style>
</head>
<body>
  <div class="container">
    <header class="mast" role="banner" aria-label="masthead">
      <h1 class="brand">The Down<span class="shift">shift</span></h1>

      <div class="mast-meta" aria-hidden="false">
        <div class="title">Automotive Digest</div>
        <div class="small">2026-07-23</div>
        <div class="mast-subline">49 stories reviewed — Sources: None identified</div>
      </div>
    </header>

    <main>
      <section aria-labelledby="the-gist">
        <div class="lede section">
          <h2 id="the-gist">The Gist</h2>
          <p class="lede-line">A compact synthesis of the supplied articles: market concentration, electrification costs and supply-chain shifts, energy and policy context, and a steady churn of cultural and aftermarket stories.</p>

          <div class="synthesis">
            <p>Dealership M&A is bifurcating: top-brand franchises command rising blue-sky values while lower-tier dealers face pressure. OEM margin management and onshoring investments are shaping near-term profitability, with GM exemplifying how EV transition costs can be balanced by strong truck/SUV pricing.</p>

            <p>Electrification trends span strategy to styling — from Xpeng’s international expansion plans to brake-caliper color language used by Nissan and Rivian. EV ecosystem topics also include forklift electrification and hardware/software tensions such as Tesla’s uncertain HW3 upgrade path.</p>

            <p>Energy and resilience reports from IEA, Ember and SEIA tie directly to automotive concerns: growing renewables and distributed resources will influence EV charging infrastructure and manufacturing security, while cybersecurity and policy integration remain priorities for grid-linked vehicle ecosystems.</p>

            <p>Across automotive culture and aftermarket arenas, the supplied pieces show continued appetite for classic restorations, high-performance cooling and braking upgrades, event-driven promotions, and media-facing initiatives that keep enthusiast communities engaged.</p>
          </div>
        </div>

        <div class="section" aria-labelledby="by-the-numbers">
          <h2 id="by-the-numbers">By The Numbers</h2>
          <div class="numbers" role="list">
            <div class="stat" role="listitem">
              <span class="n">36</span>
              <span class="label">Articles included in this digest (preserved from input)</span>
            </div>
            <div class="stat" role="listitem">
              <span class="n">5</span>
              <span class="label">Distinct categories found in the data</span>
            </div>
            <div class="stat" role="listitem">
              <span class="n">14</span>
              <span class="label">Articles labeled "Market Trends"</span>
            </div>
            <div class="stat" role="listitem">
              <span class="n">11</span>
              <span class="label">Articles labeled "Manufacturing &amp; Supply"</span>
            </div>
            <div class="stat" role="listitem">
              <span class="n">3</span>
              <span class="label">Highest importance score entries (score = 4)</span>
            </div>
            <div class="stat" role="listitem">
              <span class="n">6</span>
              <span class="label">Articles with lowest importance score (score = 1)</span>
            </div>
          </div>

          <div style="margin-top:12px" class="small">
            <strong>Top companies mentioned (by appearance in supplied records):</strong> Car and Driver; Nissan; Continental Tire; General Motors; Xpeng. (Preserved exact company names from inputs.)
          </div>
        </div>

        <div class="section">
          <h2>Top Stories</h2>
          <div class="cards" role="list">

            <article class="card" role="article" aria-labelledby="a1">
              <div>
                <span class="tag market">Market Trends</span>
                <span class="importance">Importance 4</span>
              </div>
              <h3 id="a1">K-shaped Dealership M&amp;A Market Driven by Demand for High-Quality Franchises</h3>
              <div class="summary">The U.S. auto dealer buy-sell market is bifurcated, with strong demand and rising prices for top-brand franchises while more ordinary brands struggle, signaling a record or near-record year ahead for high-quality dealerships.</div>
              <div class="meta"><strong>Companies mentioned:</strong> Kerrigan Advisors; Presidio Group; Mercedes-Benz; BMW; Porsche; Lexus; Honda; Toyota; Audi; Nissan; AIADA; Kerrigan Advisors</div>
              <ul class="bullets">
                <li>Buy-sell activity rose in H1 2026, with about 315 dealerships involved across ~215 transactions, up 23% from 2025</li>
                <li>High-demand brands include BMW, Porsche, Lexus, Honda, and Toyota, which saw significant share gains in Q1 2026</li>
                <li>Factors driving market strength include higher blue-sky values, ongoing succession issues in family-owned groups, and broader economic risks influencing seller timing</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a2">
              <div><span class="tag market">Market Trends</span><span class="importance">Importance 3</span></div>
              <h3 id="a2">GM Q2 2026 Margins Remain Within Target as EV Realignment, Onshoring Costs Weigh on Profit</h3>
              <div class="summary">GM maintains its 8-10% margin target for 2026 despite EV-related charges and onshoring costs, as stronger truck/SUV sales and disciplined pricing support profitability.</div>
              <div class="meta"><strong>Companies mentioned:</strong> General Motors</div>
              <ul class="bullets">
                <li>GM reports Q2 revenue of $48 billion and operating profit of $3.9 billion, with margins down from 9.7% to 8.2%</li>
                <li>EV-related charges and ongoing realignment weigh on profits but margins stay within target range</li>
                <li>GM plans onshoring production, launching redesigned Silverado and GMC Sierra, and investing in capacity to drive 2027 profitability</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a3">
              <div><span class="tag launch">New Car Launches</span><span class="importance">Importance 3</span></div>
              <h3 id="a3">Xpeng Eyes U.S. Market Expansion and European Production Footprint</h3>
              <div class="summary">Xpeng signals potential U.S. entry and Europe-focused production plans, highlighting partnerships and localization as pivotal to scaling globally.</div>
              <div class="meta"><strong>Companies mentioned:</strong> Xpeng; Magna; Volkswagen Group</div>
              <ul class="bullets">
                <li>Xpeng CEO He Xiaopeng says the company would enter the U.S. market if political conditions permit</li>
                <li>Plans include multiple European production sites, brownfield development, and partnerships with European automakers</li>
                <li>Magna currently assembles Xpeng models in Austria and discussions with Volkswagen Group are ongoing</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a4">
              <div><span class="tag tech">EV &amp; Tech</span><span class="importance">Importance 3</span></div>
              <h3 id="a4">Brake Caliper Color Trends Highlight Nissan and Rivian’s Distinctive Styling Cues</h3>
              <div class="summary">Automakers' brake caliper colors are becoming a recognizable differentiator across brands, signaling performance and model distinctions in both internal-combustion and electric vehicles.</div>
              <div class="meta"><strong>Companies mentioned:</strong> Nissan; Rivian</div>
              <ul class="bullets">
                <li>Nissan uses silver calipers on base models, with red calipers on higher-tier Z variants, and yellow for carbon-ceramic setups</li>
                <li>Rivian assigns silver calipers to dual-motor EVs, yellow to tri-motor versions, and blue calipers for quad-motor RAD variants</li>
                <li>Caliper color trends offer a visual cue to performance and trim levels beyond rotor and brake technology</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a5">
              <div><span class="tag tech">EV &amp; Tech</span><span class="importance">Importance 3</span></div>
              <h3 id="a5">Flock license plate readers and a mistaken car stop expose privacy and data pitfalls in US road surveillance</h3>
              <div class="summary">The Drivecast episode highlights how AI-powered license plate readers can misinterpret partial plate data, triggering real-world police stops and underscoring the need for better data governance and guardrails in automotive surveillance tech.</div>
              <div class="meta"><strong>Companies mentioned:</strong> Flock Safety; Jaguar Land Rover; Range Rover; LAPD; Los Angeles County Sheriff’s Department; NCIC; FBI; Axon; Leonardo</div>
              <ul class="bullets">
                <li>Partial license plate reads can trigger law enforcement alerts even when data is incomplete or incorrect</li>
                <li>Companies and agencies rely on NCIC/FBI databases; errors propagate across private systems and public safety workflows</li>
                <li>Calls for uniform laws and stronger guardrails to govern data retention, usage, and transparency in automated plate reading tech</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a6">
              <div><span class="tag launch">New Car Launches</span><span class="importance">Importance 3</span></div>
              <h3 id="a6">Nissan Z 2027 price hike and updates: manual Nismo now offered at no extra cost</h3>
              <div class="summary">Nissan has raised the starting prices for the 2027 Z lineup and added updates including retro touches and a six-speed manual option for the Nismo, signaling ongoing pricing and configuration shifts for a key sports coupe.</div>
              <div class="meta"><strong>Companies mentioned:</strong> Nissan</div>
              <ul class="bullets">
                <li>2027 Z receives price increases across trims with $1,510 including destination</li>
                <li>Nismo variant gains six-speed manual at no extra cost</li>
                <li>Limited dealer allocations expected this year affecting availability</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a7">
              <div><span class="tag dealer">Dealership News</span><span class="importance">Importance 1</span></div>
              <h3 id="a7">MotorTrend Magazine Contact and Advertising Information</h3>
              <div class="summary">Industry stakeholders can find contact, subscription, and advertising information for MotorTrend and Hearst Autos, underscoring the importance of subscription management and advertising partnerships.</div>
              <div class="meta"><strong>Companies mentioned:</strong> MotorTrend; Hearst Autos Inc.</div>
              <ul class="bullets">
                <li>Provides subscription management channels (phone, email, online form)</li>
                <li>Lists editorial and media contact details for public relations</li>
                <li>outlines advertising inquiry paths for automotive manufacturers and regional dealers</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a8">
              <div><span class="tag supply">Manufacturing &amp; Supply</span><span class="importance">Importance 1</span></div>
              <h3 id="a8">Staff Page Overview: MotorTrend Team Behind the Automotive Coverage</h3>
              <div class="summary">An internal staff page highlights the team responsible for producing automotive coverage, underscoring the human element behind automotive journalism and its influence on industry reporting.</div>
              <div class="meta"><strong>Companies mentioned:</strong> MotorTrend</div>
              <ul class="bullets">
                <li>Introduces editorial and production personnel</li>
                <li>Emphasizes behind-the-scenes roles in automotive media</li>
                <li>Reinforces MotorTrend as a brand with experienced contributors</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a9">
              <div><span class="tag market">Market Trends</span><span class="importance">Importance 3</span></div>
              <h3 id="a9">Car and Driver Ranks the Best Vehicles Across Segments Based on 200 Data Points</h3>
              <div class="summary">The article explains Car and Driver’s rigorous, data-driven ranking process across multiple vehicle segments to help buyers compare against direct competitors.</div>
              <div class="meta"><strong>Companies mentioned:</strong> Car and Driver</div>
              <ul class="bullets">
                <li>Utilizes roughly 200 data points covering performance, comfort, cargo, efficiency, value, and driving enjoyment</li>
                <li>Covers SUVs, sedans, family vehicles, sports cars, and electrified options among others</li>
                <li>Guides consumers by presenting rankings against direct competitors within each segment</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a10">
              <div><span class="tag supply">Manufacturing &amp; Supply</span><span class="importance">Importance 3</span></div>
              <h3 id="a10">Car and Driver Explains Their Comprehensive Vehicle Testing Approach</h3>
              <div class="summary">The article describes Car and Driver's rigorous, data-rich testing process and experience-driven insights used to evaluate hundreds of vehicles annually.</div>
              <div class="meta"><strong>Companies mentioned:</strong> Car and Driver</div>
              <ul class="bullets">
                <li>Outlines a comprehensive testing regimen covering performance, comfort, features, fuel economy, and electric range</li>
                <li>Notes the collection of about 200 data points per vehicle and real-world miles driven</li>
                <li>Emphasizes combining instrumented data with editors' experiential insights to assess overall driving experience</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a11">
              <div><span class="tag supply">Manufacturing &amp; Supply</span><span class="importance">Importance 1</span></div>
              <h3 id="a11">Car and Driver: A Snapshot of Its Buying Guide Mission and Test-Driven Expertise</h3>
              <div class="summary">The article emphasizes Car and Driver's long-standing, data-driven approach to evaluating new cars through extensive testing and test-result analysis.</div>
              <div class="meta"><strong>Companies mentioned:</strong> Car and Driver</div>
              <ul class="bullets">
                <li>Highlights decades of testing and data-driven insights</li>
                <li>Focus on performance metrics and real-world usability</li>
                <li>Promotes Buyer's Guide as a comprehensive shopping resource</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a12">
              <div><span class="tag market">Market Trends</span><span class="importance">Importance 3</span></div>
              <h3 id="a12">IEA: Renewables Overtake Coal as Global Power Demand Grows Amid Gas Shocks</h3>
              <div class="summary">The IEA projects rising global electricity demand driven by renewables growth and EV charging, with gas market shocks and LNG shifts affecting prices and reliability, signaling a pivotal transition in energy mix for the automotive industry.</div>
              <div class="meta"><strong>Companies mentioned:</strong> International Energy Agency (IEA); LNG shipments; Middle East; North America; Europe; US; China; India</div>
              <ul class="bullets">
                <li>Renewables are forecast to reach 37% of global power mix by 2027, up from 33% in 2025.</li>
                <li>Solar generation is set to lead growth, potentially surpassing wind as the second-largest renewable source after hydropower.</li>
                <li>Rising electricity demand and volatility in fossil fuels could accelerate investments in energy storage, grid flexibility, and EV charging infrastructure</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a13">
              <div><span class="tag market">Market Trends</span><span class="importance">Importance 3</span></div>
              <h3 id="a13">Electrek Daily: Electric Forklifts Drive Quiet, Clean, Indoor Operations</h3>
              <div class="summary">The article highlights electric forklifts as a growing, low-emission solution for warehouses and indoor spaces, signaling a niche but impactful shift within the broader electrification and material handling sectors.</div>
              <div class="meta"><strong>Companies mentioned:</strong> Big Joe; Kalmar; AUSA</div>
              <ul class="bullets">
                <li>Electric forklifts offer zero tailpipe emissions and quieter operation ideal for indoor spaces</li>
                <li>Autonomous material handling solutions promise lower costs and increased safety</li>
                <li>Industry players like Big Joe, Kalmar, and AUSA are expanding electric and autonomous forklift offerings</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a14">
              <div><span class="tag tech">EV &amp; Tech</span><span class="importance">Importance 3</span></div>
              <h3 id="a14">Tesla Offers No Concrete Plan to Upgrade HW3 for FSD, Exploring Options Without Timelines</h3>
              <div class="summary">Tesla indicates there is no firm plan to retrofit HW3 cars for its latest FSD software, signaling ongoing uncertainty and potential costs for the fleet.</div>
              <div class="meta"><strong>Companies mentioned:</strong> Tesla</div>
              <ul class="bullets">
                <li>Musk floated multiple upgrade options (HW4, AI4, AI5) without firm commitments</li>
                <li>Retrofits at service centers or micro-factories are likely to be slow and capital-intensive</li>
                <li>Electrek notes the situation undermines customer expectations of existing hardware being sufficient for FSD</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a15">
              <div><span class="tag market">Market Trends</span><span class="importance">Importance 3</span></div>
              <h3 id="a15">Distributed renewables offer greater resilience to ASEAN power systems than fossil fuels</h3>
              <div class="summary">A new Ember report shows that distributed renewables, with storage and grid interconnection, provide superior resilience to climate shocks in ASEAN compared to centralized fossil fuel systems, influencing regional energy policy and investment decisions.</div>
              <div class="meta"><strong>Companies mentioned:</strong> Ember; ASEAN; Philippines; Vietnam; Stimson Center</div>
              <ul class="bullets">
                <li>Distributed renewables can isolate damage and recover faster after disasters</li>
                <li>Improved interconnection and storage reduce output variability and outage duration</li>
                <li>Policy integration and regional cooperation are essential to build a resilient clean energy future</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a16">
              <div><span class="tag market">Market Trends</span><span class="importance">Importance 3</span></div>
              <h3 id="a16">Europe could unlock 25 GW of hybridised renewables by using existing hydropower connections, Ember report finds</h3>
              <div class="summary">European grid congestion could be alleviated by hybridising wind, solar, and storage at existing hydropower connections, unlocking 25 GW of new renewables without extra grid capacity.</div>
              <div class="meta"><strong>Companies mentioned:</strong> Ember</div>
              <ul class="bullets">
                <li>Hybridisation combines wind, solar and storage at a single grid connection to improve utilisation of existing infrastructure</li>
                <li>Hydropower-dominated markets in seven EU countries could integrate 18% of projected renewables by 2030 without expanding grid capacity</li>
                <li>Policy reform and faster processing of hybrid projects are needed to overcome fragmented regulatory frameworks across countries</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a17">
              <div><span class="tag market">Market Trends</span><span class="importance">Importance 3</span></div>
              <h3 id="a17">SEIA Reports cybersecurity priorities to boost U.S. solar and storage manufacturing</h3>
              <div class="summary">A new SEIA report highlights cybersecurity and domestic manufacturing expansion as key priorities to strengthen the U.S. solar and battery storage supply chain and maintain energy security.</div>
              <div class="meta"><strong>Companies mentioned:</strong> SEIA</div>
              <ul class="bullets">
                <li>Emphasizes expanding domestic solar and storage manufacturing to build resilient supply chains</li>
                <li>Advocates for baseline cybersecurity and consistent industry practices across distributed energy resources</li>
                <li>Calls for improved threat visibility and coordination through enhanced information sharing with industry partners</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a18">
              <div><span class="tag market">Market Trends</span><span class="importance">Importance 4</span></div>
              <h3 id="a18">NHRA U.S. Nationals Reach Crucial Countdown to Championship Stage</h3>
              <div class="summary">The article outlines how the NHRA U.S. Nationals serves as the season finale and Countdown to the Championship, highlighting driver matchups, point gaps, and potential eliminations that determine which competitors advance to the playoffs across four classes, signaling strategic implications for the sport’s competition and media narrative.</div>
              <div class="meta"><strong>Companies mentioned:</strong> NHRA; Team; KB Racing; Elite Motorsports; Angelle Sampey; Jerry Savoie; Harley-Davidson; Hines; Krawiec; Alex Laughlin; and many drivers</div>
              <ul class="bullets">
                <li>Top Fuel, Funny Car, Pro Stock, and Pro Stock Motorcycle drivers are fighting for the final Countdown spots</li>
                <li>Multiple drivers face pivotal first-round matchups that could decide entry into the postseason</li>
                <li>Eliminations and points scenarios are shaping expectations for the season-ending event at Lucas Oil Raceway</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a19">
              <div><span class="tag market">Market Trends</span><span class="importance">Importance 3</span></div>
              <h3 id="a19">NHRA U.S. Nationals Testing: Crampton Leads Top Fuel, Forces Strong Run, Worsham Tests in Kalitta's Dragster</h3>
              <div class="summary">Top Fuel and Funny Car testing at Lucas Oil Raceway ahead of the Chevrolet Performance U.S. Nationals showcased top performers like Richie Crampton and Brittany Force, highlighting strong competition and critical setup data for the season finale.</div>
              <div class="meta"><strong>Companies mentioned:</strong> Chevrolet; Monster Energy; John Force Racing; DHL Toyota; Mac Tools; Amalie Motor Oil; Screamin’ Eagle Vance &amp; Hines; Lucas Oil Raceway at Indianapolis; FOX Sports 1; N/A</div>
              <ul class="bullets">
                <li>Richie Crampton posted the quickest Top Fuel time of 3.706 seconds at 320.28 mph</li>
                <li>Brittany Force ran 3.725 seconds at 324.40 mph and completed multiple sub-3.70 runs</li>
                <li>Tommy Johnson Jr. topped Funny Car testing with 3.890 seconds at 324.12 mph</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a20">
              <div><span class="tag tech">EV &amp; Tech</span><span class="importance">Importance 3</span></div>
              <h3 id="a20">Red Bull’s Major RB22 Upgrade Shifts Miami F1 Momentum</h3>
              <div class="summary">A comprehensive upgrade to Red Bull’s RB22 ahead of a key Miami race altered aero, chassis and cockpit dynamics, signaling the team’s ability to rapidly evolve performance mid-season.</div>
              <div class="meta"><strong>Companies mentioned:</strong> Red Bull; Max Verstappen; McLaren; Ferrari; Mercedes; RB22</div>
              <ul class="bullets">
                <li>Major upgrade includes front wing, brake ducts, floor, sidepods, engine cover, diffuser, and rear wing</li>
                <li>Cockpit changes and steering rack modification aimed at improving driver feel and control</li>
                <li>Performance impact comes just one race after the previous aerodynamic upgrade, illustrating rapid development pace</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a21">
              <div><span class="tag tech">EV &amp; Tech</span><span class="importance">Importance 3</span></div>
              <h3 id="a21">Aston Martin’s Miami rebound: vibrations under control as upgrades loom</h3>
              <div class="summary">Aston Martin has made progress reconciling reliability and vibration issues via a five-week break and Honda collaboration, setting the stage for further upgrades and closer competition.</div>
              <div class="meta"><strong>Companies mentioned:</strong> Aston Martin; Honda; Adrian Newey; Red Bull; Cadillac</div>
              <ul class="bullets">
                <li>Five-week break helped address vibration-related reliability problems</li>
                <li>Miami result marked first race with both cars finishing this year</li>
                <li>Upcoming upgrades planned for the second half of the season</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a22">
              <div><span class="tag market">Market Trends</span><span class="importance">Importance 3</span></div>
              <h3 id="a22">Mercedes' Miami Show: Upgrades Shake Up F1 Front-Runners as McLaren and Alpine Lead the Midfield</h3>
              <div class="summary">The Miami Sprint weekend highlights how selective upgrades across top teams are reshaping the pecking order, signaling evolving competitive dynamics in the 2026 season.</div>
              <div class="meta"><strong>Companies mentioned:</strong> Mercedes; McLaren; Ferrari; Red Bull; Alpine; Williams; Audi</div>
              <ul class="bullets">
                <li>Upgrades from Mercedes were limited, yet their advantage may grow as a larger package arrives</li>
                <li>McLaren and Alpine delivered strong performances, suggesting midfield-to-front shifts</li>
                <li>Red Bull closed the gap but still trails the leaders, indicating ongoing development race</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a23">
              <div><span class="tag supply">Manufacturing &amp; Supply</span><span class="importance">Importance 3</span></div>
              <h3 id="a23">Maximize Airflow and Cooling Upgrades for LS Engines, EVs, and More</h3>
              <div class="summary">Preview of performance parts aimed at improving airflow, cooling, and braking for internal combustion engines and electric vehicles, highlighting modularity and drop-in compatibility.</div>
              <div class="meta"><strong>Companies mentioned:</strong> FAST; Cold Case Performance; PowerStop</div>
              <ul class="bullets">
                <li>FAST LSXR Intake Manifolds offer modular runners and a 102mm throttle body for LS engines with heat-resistant polymer construction</li>
                <li>Cold Case Performance Aluminum Radiators provide true drop-in replacements with OEM-style connections and optional dual-fan modules for broad GM/Ford/Mopar applications</li>
                <li>PowerStop EV35 Electric Vehicle Brake Kits deliver carbon-fiber ceramic pads, Dual-Guard rotors, and anti-delamination hardware for EV braking performance</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a24">
              <div><span class="tag supply">Manufacturing &amp; Supply</span><span class="importance">Importance 3</span></div>
              <h3 id="a24">Reliable Cooling Solutions for High-Performance Engines and Jeeps</h3>
              <div class="summary">High-performance cooling components from Edelbrock and Griffin enhance engine durability and horsepower handling in street machines, Jeeps, and other demanding applications by improving coolant flow, heat rejection, and overall reliability.</div>
              <div class="meta"><strong>Companies mentioned:</strong> Edelbrock; Griffin; SPAL</div>
              <ul class="bullets">
                <li>Edelbrock Victor Series Street Mechanical Water Pumps offer high efficiency and durability for multiple GM, Chrysler, Ford, and Pontiac engines</li>
                <li>Griffin Exact Fit Radiator with ExtremeCool Core Technology increases surface area and thermal transfer to support engines up to 900 horsepower</li>
                <li>Optional Griffin Exact Fit Combo includes fans, shroud, radiator cap, wiring, and temperature sender for a turnkey cooling solution</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a25">
              <div><span class="tag market">Market Trends</span><span class="importance">Importance 3</span></div>
              <h3 id="a25">Continental Tire 2026 Sweepstakes Winner Highlight</h3>
              <div class="summary">A consumer sweepstakes winner highlights brand engagement and promotional campaigns in the automotive aftermarket space, underlining how tire brands use giveaways to drive visibility and consumer interest.</div>
              <div class="meta"><strong>Companies mentioned:</strong> Continental Tire; PowerNation TV</div>
              <ul class="bullets">
                <li>Promotional campaigns like sweepstakes boost brand awareness in the auto accessories market</li>
                <li>Automotive media partnerships (PowerNation) amplify reach for tire brands</li>
                <li>Industry emphasis on consumer engagement through branded promotions</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a26">
              <div><span class="tag supply">Manufacturing &amp; Supply</span><span class="importance">Importance 3</span></div>
              <h3 id="a26">Maximize Airflow and Cooling for LS Power, EV Brakes Highlight Upgrades</h3>
              <div class="summary">The article highlights performance-focused aftermarket upgrades for internal combustion and electric vehicles, emphasizing improved airflow, cooling, and braking reliability essential for modern automotive powertrains.</div>
              <div class="meta"><strong>Companies mentioned:</strong> FAST LSXR Intake Manifolds; Cold Case Performance; PowerStop</div>
              <ul class="bullets">
                <li>FAST LSXR Intake Manifolds optimize airflow with a 102mm throttle body and modular runners for power curves</li>
                <li>Cold Case Performance Aluminum Radiators offer true drop-in replacements with minimal fabrication for cooling various GM, Ford, and Mopar applications</li>
                <li>PowerStop EV35 Electric Vehicle Brake Kits provide stronger, fade-resistant braking for EVs with solutions to mitigate pad delamination during regenerative braking</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a27">
              <div><span class="tag supply">Manufacturing &amp; Supply</span><span class="importance">Importance 3</span></div>
              <h3 id="a27">Reliable Cooling Solutions for High-Performance Engines and Jeep JK Wranglers</h3>
              <div class="summary">New high-performance cooling components from Edelbrock and Griffin offer enhanced heat management for hot-running engines and Jeep JK Wranglers, enabling sustained power and reliability.</div>
              <div class="meta"><strong>Companies mentioned:</strong> Edelbrock; Griffin; SPAL</div>
              <ul class="bullets">
                <li>Edelbrock Victor Series high-performance street mechanical water pumps provide maximum coolant flow and durability for a range of AMC/Jeep, Chevy, Chrysler, Ford, and Pontiac engines</li>
                <li>Griffin Exact Fit Radiator with ExtremeCool Core Technology improves cooling for up to 900 hp engines and offers an upgrade to a complete Exact Fit Combo with fans and miscellaneous cooling hardware</li>
                <li>The Griffin Combo includes two SPAL 11-inch fans, shroud, radiator cap, wiring, and sender for a factory-assembled cooling package</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a28">
              <div><span class="tag market">Market Trends</span><span class="importance">Importance 3</span></div>
              <h3 id="a28">Continental Tire Announces 2026 Sweepstakes Winner</h3>
              <div class="summary">The article highlights a corporate promotional sweepstakes, illustrating consumer engagement strategies and brand visibility in the automotive aftermarket.</div>
              <div class="meta"><strong>Companies mentioned:</strong> Continental Tire; PowerNation</div>
              <ul class="bullets">
                <li>Promotional sweepstakes engage automotive enthusiasts</li>
                <li>Brand recognition for Continental Tires increasing potential sales</li>
                <li>Cross-promotion with PowerNation expands reach in the automotive community</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a29">
              <div><span class="tag launch">New Car Launches</span><span class="importance">Importance 1</span></div>
              <h3 id="a29">Kindig-it Design Announces 2026 Summer Tour Schedule and Events</h3>
              <div class="summary">Kindig-it Design unveils its 2026 Summer Tour and event schedule, detailing shop tours and appearances at major automotive events.</div>
              <div class="meta"><strong>Companies mentioned:</strong> Kindig-it Design</div>
              <ul class="bullets">
                <li>Schedules for July, August, September shop tours and events</li>
                <li>Includes appearances at Route 66 Festival, Tripe Crown of Rodding, Cruisin' The Coast, and SEMA 2026</li>
                <li>Locations span across Utah, Missouri, Tennessee, Illinois, Mississippi, and Nevada</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a30">
              <div><span class="tag launch">New Car Launches</span><span class="importance">Importance 3</span></div>
              <h3 id="a30">Kindig-It Design showcases vintage and custom cars from GM and Ford</h3>
              <div class="summary">The article highlights a gallery of classic and custom vehicles from GM and Ford featured by Kindig-It Design, illustrating ongoing interest in retro builds and brand heritage within the automotive culture market.</div>
              <div class="meta"><strong>Companies mentioned:</strong> GM; Ford</div>
              <ul class="bullets">
                <li>Showcases a lineup of vintage and custom cars including 1960 Cadillac Copper Caddy and various Kindig CF1 models</li>
                <li>Features notable GM and Ford entries such as 1957 Corvette Family Affair, 1957 Oldsmobile 88, 1959 Buick Invicta, and 1964 Ranchero</li>
                <li>Demonstrates ongoing collaboration between automotive media/creators and classic car enthusiasts for modern storytelling of iconic models</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a31">
              <div><span class="tag supply">Manufacturing &amp; Supply</span><span class="importance">Importance 3</span></div>
              <h3 id="a31">Custom 'Burban Walks a Tight Line Between Showpiece and Practical Build</h3>
              <div class="summary">A highly customized late-model Chevrolet Suburban build showcases advanced fabrication, performance upgrades, and media hype that underscore the evolving niche of extreme truck builds in the automotive aftermarket.</div>
              <div class="meta"><strong>Companies mentioned:</strong> Ekstensive Metalworks; Street and Performance; MagnaCharger; Truckin’ magazine</div>
              <ul class="bullets">
                <li>Owner Bill’s personal truck is being rebuilt with mandrel-bent framerails and two-link rear suspension</li>
                <li>Plans include 28-inch wheels, leather interior, and a MagnaCharger supercharger aiming for around 500 hp</li>
                <li>The project highlights collaboration with specialty suppliers and media exposure for custom high-end off-road/loaded trucks</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a32">
              <div><span class="tag supply">Manufacturing &amp; Supply</span><span class="importance">Importance 1</span></div>
              <h3 id="a32">Shipping Policy Summary for Ekstensive Metal Works LLC</h3>
              <div class="summary">A shipping policy and detailed estimate form are provided for Ekstensive Metal Works LLC, indicating operational logistics support for customers in manufacturing and metal works.</div>
              <div class="meta"><strong>Companies mentioned:</strong> Ekstensive Metal Works LLC</div>
              <ul class="bullets">
                <li>Contains a shipping policy link for Ekstensive Metal Works LLC</li>
                <li>Includes a detailed estimate form for pricing and project planning</li>
                <li>Provides contact information and business location for customer inquiries</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a33">
              <div><span class="tag tech">EV &amp; Tech</span><span class="importance">Importance 1</span></div>
              <h3 id="a33">Barrett-Jackson Privacy Policy Overview and Data Handling Practices</h3>
              <div class="summary">The article outlines Barrett-Jackson’s privacy practices across its services, highlighting data collection, use, sharing, and user rights relevant to the automotive event and online presence ecosystem.</div>
              <div class="meta"><strong>Companies mentioned:</strong> Barrett-Jackson</div>
              <ul class="bullets">
                <li>Details types of information collected from users (personal, device, usage, cookies) and how it is used to operate services</li>
                <li>Disclosure of information to affiliates, partners, and service providers, plus data sharing for marketing</li>
                <li>User rights and opt-out options under CCPA, Virginia CDPA, and California Shine the Light, including contact and verification processes</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a34">
              <div><span class="tag supply">Manufacturing &amp; Supply</span><span class="importance">Importance 3</span></div>
              <h3 id="a34">Engine Removal Tips: From Preparation to Labeling for a Safer, Faster Swap</h3>
              <div class="summary">A practical guide on engine removal emphasizes planning, collaboration, space management, fluid handling, and labeling to minimize mistakes and speed up the process, reflecting common best practices in automotive project work.</div>
              <div class="meta"><strong>Companies mentioned:</strong> Hagerty</div>
              <ul class="bullets">
                <li>Plan the work over multiple sessions to reduce errors</li>
                <li>Assemble a crew to share tasks and reduce mistakes</li>
                <li>Use service manuals and clear labels to track parts and keep the project organized</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a35">
              <div><span class="tag market">Market Trends</span><span class="importance">Importance 3</span></div>
              <h3 id="a35">Cars That Age Better Than Expected: Porsche 928, BMW Z4 M Coupe, Toyota FJ Cruiser, and More</h3>
              <div class="summary">The piece highlights classic models that improve in perception with age, signaling evolving collector interest and market dynamics in the automotive world.</div>
              <div class="meta"><strong>Companies mentioned:</strong> Porsche; BMW; Toyota; Jaguar; Chevrolet; Ford; Nissan</div>
              <ul class="bullets">
                <li>Porsche 928 is praised for its ahead-of-its-time design and performance, influencing perceptions of early water-cooled V-8 era Porsches</li>
                <li>BMW Z4 M Coupe is noted for aging gracefully compared to its more radical predecessors</li>
                <li>Toyota FJ Cruiser is admired for its distinctive styling that has grown on enthusiasts despite practical drawbacks</li>
              </ul>
            </article>

            <article class="card" role="article" aria-labelledby="a36">
              <div><span class="tag supply">Manufacturing &amp; Supply</span><span class="importance">Importance 4</span></div>
              <h3 id="a36">Norton Dominator 88: A Vintage Featherbed Frame Carves a Niche in Modern Riding</h3>
              <div class="summary">A revival-era Norton Dominator 88 leverages the historic Featherbed frame to deliver classic handling and enduring appeal, highlighting how legacy engineering shapes modern perceptions of vintage motorcycles.</div>
              <div class="meta"><strong>Companies mentioned:</strong> Norton; Triumph; Ariel; Geoff Duke; Harold Daniell; Bert Hopwood; Girling; AMS Monobloc</div>
              <ul class="bullets">
                <li>Highlights Norton’s revival with the 88 model and Featherbed frame</li>
                <li>Discusses historical development from 1949 Dominator to 1952-53 88/99 variants</li>
                <li>Emphasizes ride quality, chassis handling, and enduring nostalgia for classic motorcycles</li>
              </ul>
            </article>

          </div>
        </div>
      </section>

      <aside class="sidebar" aria-labelledby="sidebar-top">
        <div class="section">
          <h2 id="sidebar-top">Quick Reference</h2>
          <div class="small">
            <strong>Digest note:</strong> All article titles, summaries, bullet points, importance scores, and company mentions are preserved exactly from the supplied JSON records.
          </div>
        </div>

        <div class="section">
          <h2>Jump to</h2>
          <div class="small">
            - Top Stories (main column)<br>
            - By The Numbers (main column)<br>
            - The Gist (main column)
          </div>
        </div>

      </aside>
    </main>

    <footer>
      This digest was compiled from the supplied sources and preserved the provided article text and metadata.
    </footer>
  </div>
</body>
</html>   
