<!DOCTYPE html>
<html lang="en">
<head>

  <meta charset="UTF-8">

  <meta
    name="viewport"
    content="width=device-width, initial-scale=1.0"
  >

  <meta
    name="theme-color"
    content="#02040a"
  >

  <meta
    name="description"
    content="XyloTech — Digital Intelligence, Software Engineering, AI, Cybersecurity, SaaS and Cloud Infrastructure."
  >

  <title>
    XyloTech // Digital Intelligence
  </title>

  <link
    rel="preconnect"
    href="https://fonts.googleapis.com"
  >

  <link
    rel="preconnect"
    href="https://fonts.gstatic.com"
    crossorigin
  >

  <link
    href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;600;700&family=Space+Grotesk:wght@400;500;600;700&display=swap"
    rel="stylesheet"
  >


  <style>

    /* =========================================================
       CORE
    ========================================================= */

    :root {

      --bg: #02040a;
      --bg2: #050812;

      --cyan: #00f6ff;
      --blue: #4169ff;
      --purple: #9b5cff;
      --pink: #ff2cac;

      --green: #00ff9d;
      --red: #ff5577;

      --white: #f4f8ff;
      --muted: #77839b;

      --line: rgba(0, 246, 255, .12);

      --glass:
        rgba(7, 13, 27, .65);

      --glass2:
        rgba(12, 20, 40, .82);

      --shadow:
        0 0 50px
        rgba(0,246,255,.07);

    }


    * {

      margin: 0;
      padding: 0;
      box-sizing: border-box;

    }


    html {

      scroll-behavior: smooth;

    }


    body {

      background:
        radial-gradient(
          circle at 10% 10%,
          rgba(65,105,255,.12),
          transparent 30%
        ),

        radial-gradient(
          circle at 90% 20%,
          rgba(0,246,255,.08),
          transparent 30%
        ),

        radial-gradient(
          circle at 50% 100%,
          rgba(155,92,255,.08),
          transparent 35%
        ),

        var(--bg);

      color: var(--white);

      font-family:
        "Space Grotesk",
        sans-serif;

      overflow-x: hidden;

    }


    ::selection {

      background: var(--cyan);
      color: #000;

    }


    a {

      color: inherit;
      text-decoration: none;

    }


    /* =========================================================
       BACKGROUND
    ========================================================= */

    #network {

      position: fixed;

      inset: 0;

      width: 100%;
      height: 100%;

      z-index: -10;

      pointer-events: none;

    }


    .grid {

      position: fixed;

      inset: 0;

      z-index: -9;

      pointer-events: none;

      background-image:

        linear-gradient(
          rgba(0,246,255,.035) 1px,
          transparent 1px
        ),

        linear-gradient(
          90deg,
          rgba(0,246,255,.035) 1px,
          transparent 1px
        );

      background-size: 55px 55px;

      mask-image:
        linear-gradient(
          to bottom,
          black,
          transparent 85%
        );

    }


    .scanlines {

      position: fixed;

      inset: 0;

      z-index: 999;

      pointer-events: none;

      opacity: .035;

      background:
        repeating-linear-gradient(
          to bottom,
          transparent 0px,
          transparent 3px,
          #fff 4px
        );

    }


    .noise {

      position: fixed;

      inset: 0;

      z-index: 998;

      pointer-events: none;

      opacity: .025;

      background-image:
        url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.8' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='.7'/%3E%3C/svg%3E");

    }


    /* =========================================================
       LOADER
    ========================================================= */

    #boot {

      position: fixed;

      inset: 0;

      z-index: 10000;

      display: flex;

      align-items: center;

      justify-content: center;

      background: #010207;

      transition:
        opacity .8s,
        visibility .8s;

    }


    #boot.done {

      opacity: 0;
      visibility: hidden;

    }


    .boot-box {

      width: min(
        520px,
        calc(100% - 40px)
      );

      font-family:
        "JetBrains Mono",
        monospace;

    }


    .boot-title {

      font-size: 42px;

      font-weight: 700;

      letter-spacing: -3px;

      text-align: center;

    }


    .boot-title span {

      color: var(--cyan);

    }


    .boot-text {

      margin-top: 30px;

      min-height: 90px;

      color: var(--green);

      font-size: 11px;

      line-height: 1.8;

    }


    .boot-bar {

      height: 2px;

      margin-top: 20px;

      background:
        rgba(255,255,255,.08);

      overflow: hidden;

    }


    .boot-progress {

      width: 0;

      height: 100%;

      background:
        linear-gradient(
          90deg,
          var(--cyan),
          var(--purple)
        );

      animation:
        bootProgress 2.3s
        ease forwards;

    }


    @keyframes bootProgress {

      to {
        width: 100%;
      }

    }


    /* =========================================================
       NAVIGATION
    ========================================================= */

    nav {

      position: fixed;

      top: 18px;

      left: 50%;

      transform:
        translateX(-50%);

      width:
        min(
          1200px,
          calc(100% - 30px)
        );

      z-index: 900;

      display: flex;

      align-items: center;

      justify-content: space-between;

      padding: 12px 15px;

      background:
        rgba(2,5,12,.65);

      border:
        1px solid
        rgba(0,246,255,.12);

      backdrop-filter:
        blur(20px);

      border-radius: 16px;

      box-shadow:
        0 15px 60px
        rgba(0,0,0,.35);

      transition: .3s;

    }


    .brand {

      display: flex;

      align-items: center;

      gap: 10px;

      font-size: 17px;

      font-weight: 700;

      letter-spacing: -1px;

    }


    .brand-icon {

      width: 32px;

      height: 32px;

      display: grid;

      place-items: center;

      border-radius: 9px;

      color: #000;

      background:
        linear-gradient(
          135deg,
          var(--cyan),
          var(--purple)
        );

      box-shadow:
        0 0 25px
        rgba(0,246,255,.3);

    }


    .nav-center {

      display: flex;

      gap: 22px;

    }


    .nav-center a {

      color: #8490a8;

      font-family:
        "JetBrains Mono",
        monospace;

      font-size: 10px;

      transition: .25s;

    }


    .nav-center a:hover {

      color: var(--cyan);

    }


    .nav-right {

      display: flex;

      align-items: center;

      gap: 8px;

    }


    .status {

      display: flex;

      align-items: center;

      gap: 7px;

      color: var(--green);

      font-family:
        "JetBrains Mono",
        monospace;

      font-size: 9px;

    }


    .status i {

      width: 6px;

      height: 6px;

      border-radius: 50%;

      background: var(--green);

      box-shadow:
        0 0 10px
        var(--green);

      animation:
        blink 1.5s infinite;

    }


    /* =========================================================
       HERO
    ========================================================= */

    .hero {

      min-height: 100vh;

      display: flex;

      align-items: center;

      justify-content: center;

      position: relative;

      padding:
        150px 20px 100px;

      text-align: center;

    }


    .hero-content {

      position: relative;

      z-index: 2;

      max-width: 1050px;

    }


    .system-label {

      display: inline-flex;

      align-items: center;

      gap: 9px;

      padding:
        8px 13px;

      border:
        1px solid
        rgba(0,246,255,.18);

      background:
        rgba(0,246,255,.035);

      border-radius:
        100px;

      color:
        #9afaff;

      font-family:
        "JetBrains Mono",
        monospace;

      font-size: 9px;

      letter-spacing: 1px;

      margin-bottom: 28px;

    }


    .system-label::before {

      content: "";

      width: 6px;

      height: 6px;

      border-radius: 50%;

      background: var(--cyan);

      box-shadow:
        0 0 12px
        var(--cyan);

      animation:
        blink 1.5s infinite;

    }


    .hero h1 {

      font-size:
        clamp(
          55px,
          10vw,
          125px
        );

      line-height:
        .84;

      letter-spacing:
        -8px;

      font-weight:
        700;

    }


    .glow-text {

      background:
        linear-gradient(
          90deg,
          #fff,
          var(--cyan),
          var(--purple),
          var(--pink),
          var(--cyan)
        );

      background-size:
        300% auto;

      -webkit-background-clip:
        text;

      background-clip:
        text;

      color: transparent;

      animation:
        gradient 8s linear infinite;

    }


    @keyframes gradient {

      to {

        background-position:
          300% center;

      }

    }


    .hero-description {

      max-width:
        700px;

      margin:
        35px auto 0;

      color:
        var(--muted);

      font-size:
        15px;

      line-height:
        1.9;

    }


    .hero-actions {

      margin-top:
        35px;

      display:
        flex;

      justify-content:
        center;

      gap:
        10px;

      flex-wrap:
        wrap;

    }


    .button {

      padding:
        13px 18px;

      border-radius:
        10px;

      border:
        1px solid
        var(--line);

      font-family:
        "JetBrains Mono",
        monospace;

      font-size:
        10px;

      transition:
        .3s;

    }


    .button.primary {

      color: #000;

      background:
        var(--cyan);

      box-shadow:
        0 0 30px
        rgba(0,246,255,.2);

    }


    .button:hover {

      transform:
        translateY(-4px);

    }


    .button.secondary {

      background:
        rgba(255,255,255,.035);

    }


    .button.secondary:hover {

      color:
        var(--cyan);

      border-color:
        rgba(0,246,255,.3);

    }


    /* =========================================================
       ORBIT
    ========================================================= */

    .orbit {

      position: absolute;

      width: 550px;

      height: 550px;

      left: 50%;

      top: 54%;

      transform:
        translate(-50%,-50%);

      border:
        1px solid
        rgba(0,246,255,.08);

      border-radius:
        50%;

      pointer-events:
        none;

      z-index:
        -1;

      animation:
        orbit 25s
        linear
        infinite;

    }


    .orbit::before {

      content: "";

      position: absolute;

      inset: 70px;

      border:
        1px solid
        rgba(155,92,255,.09);

      border-radius:
        50%;

    }


    .orbit::after {

      content: "";

      position: absolute;

      width: 10px;

      height: 10px;

      top: 50%;

      right: -5px;

      border-radius: 50%;

      background:
        var(--cyan);

      box-shadow:
        0 0 25px
        var(--cyan);

    }


    @keyframes orbit {

      to {
        transform:
          translate(-50%,-50%)
          rotate(360deg);
      }

    }


    /* =========================================================
       SECTION
    ========================================================= */

    section {

      width:
        min(
          1180px,
          calc(100% - 40px)
        );

      margin:
        auto;

      padding:
        110px 0;

    }


    .section-id {

      color:
        var(--cyan);

      font-family:
        "JetBrains Mono",
        monospace;

      font-size:
        9px;

      letter-spacing:
        3px;

      margin-bottom:
        14px;

    }


    .section-title {

      font-size:
        clamp(
          38px,
          6vw,
          68px
        );

      line-height:
        .95;

      letter-spacing:
        -4px;

    }


    .section-description {

      max-width:
        650px;

      color:
        var(--muted);

      margin-top:
        20px;

      line-height:
        1.8;

      font-size:
        14px;

    }


    /* =========================================================
       STATS
    ========================================================= */

    .stats {

      display:
        grid;

      grid-template-columns:
        repeat(4,1fr);

      border-top:
        1px solid
        var(--line);

      border-bottom:
        1px solid
        var(--line);

    }


    .stat {

      padding:
        40px 20px;

      text-align:
        center;

      border-right:
        1px solid
        var(--line);

    }


    .stat:last-child {

      border:
        none;

    }


    .stat-number {

      font-size:
        42px;

      font-weight:
        700;

      color:
        var(--cyan);

      text-shadow:
        0 0 25px
        rgba(0,246,255,.3);

    }


    .stat-label {

      margin-top:
        8px;

      color:
        var(--muted);

      font-family:
        "JetBrains Mono",
        monospace;

      font-size:
        8px;

      letter-spacing:
        1px;

    }


    /* =========================================================
       SYSTEM CARDS
    ========================================================= */

    .systems {

      margin-top:
        50px;

      display:
        grid;

      grid-template-columns:
        repeat(3,1fr);

      gap:
        12px;

    }


    .system-card {

      position:
        relative;

      min-height:
        260px;

      padding:
        25px;

      background:
        linear-gradient(
          145deg,
          rgba(15,24,45,.75),
          rgba(5,10,20,.65)
        );

      border:
        1px solid
        var(--line);

      border-radius:
        18px;

      overflow:
        hidden;

      transition:
        .4s;

    }


    .system-card::before {

      content: "";

      position:
        absolute;

      width:
        150px;

      height:
        150px;

      right:
        -70px;

      bottom:
        -70px;

      border-radius:
        50%;

      background:
        var(--cyan);

      filter:
        blur(80px);

      opacity:
        .06;

      transition:
        .4s;

    }


    .system-card:hover {

      transform:
        translateY(-7px);

      border-color:
        rgba(0,246,255,.3);

      box-shadow:
        var(--shadow);

    }


    .system-card:hover::before {

      opacity:
        .2;

    }


    .card-number {

      position:
        absolute;

      top:
        20px;

      right:
        20px;

      color:
        #39465e;

      font-family:
        "JetBrains Mono",
        monospace;

      font-size:
        9px;

    }


    .card-icon {

      width:
        48px;

      height:
        48px;

      display:
        grid;

      place-items:
        center;

      border:
        1px solid
        rgba(0,246,255,.15);

      background:
        rgba(0,246,255,.04);

      border-radius:
        12px;

      color:
        var(--cyan);

      font-size:
        20px;

      margin-bottom:
        45px;

    }


    .system-card h3 {

      font-size:
        18px;

    }


    .system-card p {

      color:
        var(--muted);

      font-size:
        12px;

      line-height:
        1.7;

      margin-top:
        10px;

    }


    /* =========================================================
       TERMINAL
    ========================================================= */

    .terminal-grid {

      display:
        grid;

      grid-template-columns:
        1fr 1fr;

      gap:
        50px;

      align-items:
        center;

    }


    .terminal {

      overflow:
        hidden;

      border:
        1px solid
        var(--line);

      border-radius:
        18px;

      background:
        rgba(1,4,10,.85);

      box-shadow:
        0 20px 80px
        rgba(0,0,0,.3);

    }


    .terminal-header {

      height:
        45px;

      display:
        flex;

      align-items:
        center;

      gap:
        6px;

      padding:
        0 15px;

      border-bottom:
        1px solid
        var(--line);

    }


    .terminal-dot {

      width:
        7px;

      height:
        7px;

      border-radius:
        50%;

      background:
        #334158;

    }


    .terminal-name {

      margin-left:
        8px;

      color:
        #536078;

      font-family:
        "JetBrains Mono",
        monospace;

      font-size:
        9px;

    }


    .terminal-body {

      padding:
        25px;

      min-height:
        340px;

      font-family:
        "JetBrains Mono",
        monospace;

      font-size:
        11px;

      line-height:
        2;

      color:
        #78869f;

    }


    .cyan {

      color:
        var(--cyan);

    }


    .green {

      color:
        var(--green);

    }


    .purple {

      color:
        var(--purple);

    }


    .pink {

      color:
        var(--pink);

    }


    .terminal-cursor {

      display:
        inline-block;

      width:
        6px;

      height:
        13px;

      background:
        var(--cyan);

      animation:
        blink .8s infinite;

      vertical-align:
        middle;

    }


    /* =========================================================
       SECURITY
    ========================================================= */

    .security {

      position:
        relative;

      padding:
        45px;

      margin-top:
        50px;

      display:
        grid;

      grid-template-columns:
        1fr 1fr;

      gap:
        60px;

      align-items:
        center;

      border:
        1px solid
        rgba(0,246,255,.13);

      border-radius:
        24px;

      background:
        radial-gradient(
          circle at 20% 50%,
          rgba(0,246,255,.06),
          transparent 35%
        ),

        radial-gradient(
          circle at 80% 50%,
          rgba(155,92,255,.06),
          transparent 35%
        ),

        rgba(255,255,255,.02);

      overflow:
        hidden;

    }


    .security::before {

      content:
        "";

      position:
        absolute;

      top:
        0;

      left:
        -100%;

      width:
        70%;

      height:
        1px;

      background:
        linear-gradient(
          90deg,
          transparent,
          var(--cyan),
          transparent
        );

      animation:
        scan 5s linear infinite;

    }


    @keyframes scan {

      to {
        left: 120%;
      }

    }


    .security h2 {

      font-size:
        clamp(
          35px,
          5vw,
          58px
        );

      line-height:
        .95;

      letter-spacing:
        -3px;

    }


    .security p {

      margin-top:
        20px;

      color:
        var(--muted);

      line-height:
        1.8;

      font-size:
        13px;

    }


    .profiles {

      margin-top:
        25px;

      display:
        flex;

      gap:
        8px;

      flex-wrap:
        wrap;

    }


    .profile {

      padding:
        11px 14px;

      border:
        1px solid
        var(--line);

      border-radius:
        10px;

      background:
        rgba(255,255,255,.025);

      font-family:
        "JetBrains Mono",
        monospace;

      font-size:
        9px;

      transition:
        .3s;

    }


    .profile:hover {

      color:
        var(--cyan);

      border-color:
        rgba(0,246,255,.35);

      transform:
        translateY(-3px);

    }


    .security-terminal {

      border:
        1px solid
        var(--line);

      border-radius:
        16px;

      background:
        rgba(0,0,0,.35);

      overflow:
        hidden;

    }


    .security-bar {

      padding:
        14px;

      display:
        flex;

      justify-content:
        space-between;

      border-bottom:
        1px solid
        var(--line);

      font-family:
        "JetBrains Mono",
        monospace;

      font-size:
        8px;

    }


    .online {

      color:
        var(--green);

    }


    .security-code {

      padding:
        25px;

      font-family:
        "JetBrains Mono",
        monospace;

      font-size:
        10px;

      line-height:
        2;

      color:
        #718099;

    }


    /* =========================================================
       PROCESS
    ========================================================= */

    .process {

      margin-top:
        50px;

      display:
        grid;

      grid-template-columns:
        repeat(4,1fr);

      gap:
        12px;

    }


    .process-card {

      padding:
        25px;

      border:
        1px solid
        var(--line);

      background:
        rgba(255,255,255,.02);

      border-radius:
        16px;

      position:
        relative;

    }


    .process-card span {

      color:
        var(--cyan);

      font-family:
        "JetBrains Mono",
        monospace;

      font-size:
        9px;

    }


    .process-card h3 {

      margin-top:
        30px;

    }


    .process-card p {

      margin-top:
        10px;

      color:
        var(--muted);

      font-size:
        11px;

      line-height:
        1.7;

    }


    .process-card:not(:last-child)::after {

      content:
        "→";

      position:
        absolute;

      right:
        -18px;

      top:
        50%;

      color:
        var(--cyan);

    }


    /* =========================================================
       INDUSTRIES
    ========================================================= */

    .industries {

      margin-top:
        50px;

      display:
        grid;

      grid-template-columns:
        repeat(4,1fr);

      gap:
        10px;

    }


    .industry {

      min-height:
        150px;

      padding:
        22px;

      border:
        1px solid
        var(--line);

      border-radius:
        14px;

      background:
        rgba(255,255,255,.02);

      transition:
        .3s;

    }


    .industry:hover {

      transform:
        translateY(-5px);

      border-color:
        rgba(155,92,255,.3);

    }


    .industry-icon {

      color:
        var(--cyan);

      font-size:
        22px;

    }


    .industry h3 {

      margin-top:
        25px;

      font-size:
        15px;

    }


    .industry p {

      margin-top:
        7px;

      color:
        var(--muted);

      font-size:
        10px;

      line-height:
        1.6;

    }


    /* =========================================================
       FOUNDER
    ========================================================= */

    .founder {

      display:
        grid;

      grid-template-columns:
        150px 1fr;

      gap:
        30px;

      align-items:
        center;

      margin-top:
        50px;

      padding:
        35px;

      border:
        1px solid
        var(--line);

      border-radius:
        20px;

      background:
        rgba(255,255,255,.02);

    }


    .founder-avatar {

      width:
        130px;

      height:
        130px;

      display:
        grid;

      place-items:
        center;

      border-radius:
        20px;

      font-size:
        34px;

      font-weight:
        700;

      background:
        linear-gradient(
          135deg,
          var(--cyan),
          var(--purple)
        );

      box-shadow:
        0 0 50px
        rgba(0,246,255,.18);

    }


    .founder h3 {

      font-size:
        28px;

    }


    .founder-role {

      margin-top:
        5px;

      color:
        var(--cyan);

      font-family:
        "JetBrains Mono",
        monospace;

      font-size:
        9px;

      text-transform:
        uppercase;

    }


    .founder p {

      margin-top:
        15px;

      color:
        var(--muted);

      font-size:
        13px;

      line-height:
        1.8;

    }


    /* =========================================================
       CTA
    ========================================================= */

    .cta {

      position:
        relative;

      padding:
        100px 30px;

      text-align:
        center;

      border:
        1px solid
        rgba(0,246,255,.15);

      border-radius:
        28px;

      overflow:
        hidden;

      background:
        radial-gradient(
          circle,
          rgba(0,246,255,.09),
          transparent 55%
        );

    }


    .cta h2 {

      font-size:
        clamp(
          42px,
          7vw,
          78px
        );

      letter-spacing:
        -5px;

      line-height:
        .9;

    }


    .cta p {

      max-width:
        600px;

      margin:
        22px auto;

      color:
        var(--muted);

      line-height:
        1.8;

      font-size:
        13px;

    }


    /* =========================================================
       FOOTER
    ========================================================= */

    footer {

      width:
        min(
          1180px,
          calc(100% - 40px)
        );

      margin:
        auto;

      padding:
        40px 0;

      border-top:
        1px solid
        var(--line);

      display:
        flex;

      justify-content:
        space-between;

      align-items:
        center;

      gap:
        20px;

      font-family:
        "JetBrains Mono",
        monospace;

      font-size:
        9px;

      color:
        #58647b;

    }


    .footer-links {

      display:
        flex;

      gap:
        18px;

      flex-wrap:
        wrap;

    }


    .footer-links a:hover {

      color:
        var(--cyan);

    }


    /* =========================================================
       REVEAL
    ========================================================= */

    .reveal {

      opacity:
        0;

      transform:
        translateY(30px);

      transition:
        opacity .8s ease,
        transform .8s ease;

    }


    .reveal.active {

      opacity:
        1;

      transform:
        translateY(0);

    }


    /* =========================================================
       ANIMATION
    ========================================================= */

    @keyframes blink {

      50% {
        opacity: .25;
      }

    }


    /* =========================================================
       RESPONSIVE
    ========================================================= */

    @media(max-width:950px) {

      .nav-center {

        display:
          none;

      }


      .systems {

        grid-template-columns:
          repeat(2,1fr);

      }


      .terminal-grid {

        grid-template-columns:
          1fr;

      }


      .security {

        grid-template-columns:
          1fr;

      }


      .process {

        grid-template-columns:
          repeat(2,1fr);

      }


      .process-card:not(:last-child)::after {

        display:
          none;

      }


      .industries {

        grid-template-columns:
          repeat(2,1fr);

      }


      .stats {

        grid-template-columns:
          repeat(2,1fr);

      }


      .stat:nth-child(2) {

        border-right:
          none;

      }


      .stat:nth-child(-n+2) {

        border-bottom:
          1px solid
          var(--line);

      }

    }


    @media(max-width:600px) {

      nav {

        top:
          9px;

      }


      .status {

        display:
          none;

      }


      .hero {

        padding-top:
          130px;

      }


      .hero h1 {

        font-size:
          clamp(
            48px,
            15vw,
            75px
          );

        letter-spacing:
          -5px;

      }


      .orbit {

        width:
          330px;

        height:
          330px;

      }


      section {

        padding:
          75px 0;

      }


      .systems,
      .process,
      .industries {

        grid-template-columns:
          1fr;

      }


      .security {

        padding:
          25px;

      }


      .founder {

        grid-template-columns:
          1fr;

        text-align:
          center;

      }


      .founder-avatar {

        margin:
          auto;

      }


      .profiles {

        justify-content:
          center;

      }


      footer {

        flex-direction:
          column;

        text-align:
          center;

      }

    }

  </style>

</head>


<body>


  <!-- =======================================================
       BOOT SCREEN
  ======================================================== -->

  <div id="boot">

    <div class="boot-box">

      <div class="boot-title">

        XYLO<span>TECH</span>

      </div>

      <div
        class="boot-text"
        id="bootText"
      ></div>

      <div class="boot-bar">

        <div class="boot-progress"></div>

      </div>

    </div>

  </div>


  <!-- BACKGROUND -->

  <canvas id="network"></canvas>

  <div class="grid"></div>

  <div class="scanlines"></div>

  <div class="noise"></div>


  <!-- =======================================================
       NAVIGATION
  ======================================================== -->

  <nav id="nav">

    <a
      href="#"
      class="brand"
    >

      <span class="brand-icon">
        X
      </span>

      XYLOTECH

    </a>


    <div class="nav-center">

      <a href="#systems">
        SYSTEMS
      </a>

      <a href="#technology">
        TECHNOLOGY
      </a>

      <a href="#security">
        SECURITY
      </a>

      <a href="#process">
        PROTOCOL
      </a>

      <a href="#contact">
        CONTACT
      </a>

    </div>


    <div class="nav-right">

      <div class="status">

        <i></i>

        SYSTEM ONLINE

      </div>

    </div>

  </nav>


  <!-- =======================================================
       HERO
  ======================================================== -->

  <main>


    <section class="hero">

      <div class="orbit"></div>


      <div class="hero-content">


        <div class="system-label">

          XYLOTECH // DIGITAL INTELLIGENCE SYSTEM

        </div>


        <h1>

          BUILD

          <br>

          <span class="glow-text">
            BEYOND
          </span>

          <br>

          IMAGINATION.

        </h1>


        <p class="hero-description">

          We engineer intelligent software,
          AI systems, scalable SaaS platforms,
          secure infrastructure and digital
          experiences for the next generation
          of technology.

        </p>


        <div class="hero-actions">

          <a
            href="#systems"
            class="button primary"
          >
            INITIALIZE →
          </a>


          <a
            href="https://github.com/XyloTech"
            target="_blank"
            rel="noopener noreferrer"
            class="button secondary"
          >
            GITHUB ↗
          </a>


          <a
            href="https://hackerone.com/h4shk"
            target="_blank"
            rel="noopener noreferrer"
            class="button secondary"
          >
            HACKERONE ↗
          </a>


          <a
            href="https://www.linkedin.com/in/h4sho/"
            target="_blank"
            rel="noopener noreferrer"
            class="button secondary"
          >
            LINKEDIN ↗
          </a>

        </div>

      </div>

    </section>


    <!-- =====================================================
         STATS
    ====================================================== -->

    <section>

      <div class="stats reveal">


        <div class="stat">

          <div
            class="stat-number"
            data-target="50"
          >
            0+
          </div>

          <div class="stat-label">
            PROJECTS
          </div>

        </div>


        <div class="stat">

          <div
            class="stat-number"
            data-target="15"
          >
            0+
          </div>

          <div class="stat-label">
            TECHNOLOGIES
          </div>

        </div>


        <div class="stat">

          <div
            class="stat-number"
            data-target="99"
          >
            0%
          </div>

          <div class="stat-label">
            ENGINEERING FOCUS
          </div>

        </div>


        <div class="stat">

          <div class="stat-number">
            24/7
          </div>

          <div class="stat-label">
            SYSTEM AVAILABILITY
          </div>

        </div>

      </div>

    </section>


    <!-- =====================================================
         SYSTEMS
    ====================================================== -->

    <section id="systems">

      <div class="reveal">

        <div class="section-id">
          // 01 :: CORE SYSTEMS
        </div>


        <h2 class="section-title">

          TECHNOLOGY

          <br>

          WITHOUT

          <span class="glow-text">
            LIMITS.
          </span>

        </h2>


        <p class="section-description">

          From architecture to production,
          XyloTech combines engineering,
          intelligence and design to create
          technology built for scale.

        </p>

      </div>


      <div class="systems">


        <article class="system-card reveal">

          <span class="card-number">
            SYS_001
          </span>

          <div class="card-icon">
            ⌘
          </div>

          <h3>
            SOFTWARE ENGINEERING
          </h3>

          <p>

            Full-stack applications, APIs,
            backend architecture, databases,
            real-time systems and distributed
            infrastructure.

          </p>

        </article>


        <article class="system-card reveal">

          <span class="card-number">
            SYS_002
          </span>

          <div class="card-icon">
            ◉
          </div>

          <h3>
            ARTIFICIAL INTELLIGENCE
          </h3>

          <p>

            LLM applications, AI agents,
            machine learning, predictive
            systems and intelligent automation.

          </p>

        </article>


        <article class="system-card reveal">

          <span class="card-number">
            SYS_003
          </span>

          <div class="card-icon">
            ⬡
          </div>

          <h3>
            SAAS PLATFORMS
          </h3>

          <p>

            Multi-tenant systems,
            authentication, subscriptions,
            dashboards and scalable APIs.

          </p>

        </article>


        <article class="system-card reveal">

          <span class="card-number">
            SYS_004
          </span>

          <div class="card-icon">
            ⌬
          </div>

          <h3>
            CYBERSECURITY
          </h3>

          <p>

            Secure architecture, application
            security, threat modeling and
            responsible vulnerability research.

          </p>

        </article>


        <article class="system-card reveal">

          <span class="card-number">
            SYS_005
          </span>

          <div class="card-icon">
            ✦
          </div>

          <h3>
            PRODUCT ENGINEERING
          </h3>

          <p>

            UI/UX, design systems, frontend
            architecture and high-quality
            digital experiences.

          </p>

        </article>


        <article class="system-card reveal">

          <span class="card-number">
            SYS_006
          </span>

          <div class="card-icon">
            △
          </div>

          <h3>
            CLOUD & DEVOPS
          </h3>

          <p>

            Cloud infrastructure, Docker,
            CI/CD, Linux, deployment,
            monitoring and automation.

          </p>

        </article>

      </div>

    </section>


    <!-- =====================================================
         TECHNOLOGY TERMINAL
    ====================================================== -->

    <section id="technology">

      <div class="terminal-grid">


        <div class="terminal reveal">

          <div class="terminal-header">

            <span class="terminal-dot"></span>

            <span class="terminal-dot"></span>

            <span class="terminal-dot"></span>

            <span class="terminal-name">
              xylotech_core.sys
            </span>

          </div>


          <div class="terminal-body">

            <div>

              <span class="purple">
                const
              </span>

              <span class="cyan">
                XyloTech
              </span>

              =

              <span class="purple">
                new
              </span>

              Intelligence();

            </div>


            <br>


            <div>

              XyloTech.

              <span class="cyan">
                mission
              </span>

              =

              <span class="green">
                "Engineer the impossible"
              </span>;

            </div>


            <div>

              XyloTech.

              <span class="cyan">
                systems
              </span>
              = [

            </div>


            <div>
              &nbsp;&nbsp;
              <span class="pink">
                "AI"
              </span>,
            </div>


            <div>
              &nbsp;&nbsp;
              <span class="pink">
                "SOFTWARE"
              </span>,
            </div>


            <div>
              &nbsp;&nbsp;
              <span class="pink">
                "SECURITY"
              </span>,
            </div>


            <div>
              &nbsp;&nbsp;
              <span class="pink">
                "CLOUD"
              </span>,
            </div>


            <div>
              &nbsp;&nbsp;
              <span class="pink">
                "AUTOMATION"
              </span>
            </div>


            <div>
              ];
            </div>


            <br>


            <div>

              <span class="purple">
                await
              </span>

              XyloTech.

              <span class="cyan">
                build
              </span>({

            </div>


            <div>

              &nbsp;&nbsp;
              scale:

              <span class="green">
                true
              </span>,

            </div>


            <div>

              &nbsp;&nbsp;
              intelligence:

              <span class="green">
                true
              </span>,

            </div>


            <div>

              &nbsp;&nbsp;
              security:

              <span class="green">
                "maximum"
              </span>

            </div>


            <div>
              });
            </div>


            <br>


            <div>

              <span class="green">
                SYSTEM_STATUS:
                ONLINE
              </span>

              <span
                class="terminal-cursor"
              ></span>

            </div>

          </div>

        </div>


        <div class="reveal">

          <div class="section-id">
            // 02 :: INTELLIGENCE
          </div>


          <h2 class="section-title">

            WE DON'T

            <br>

            FOLLOW THE

            <span class="glow-text">
              FUTURE.
            </span>

          </h2>


          <p class="section-description">

            We engineer it.

            XyloTech operates at the intersection
            of software engineering, artificial
            intelligence, cybersecurity and
            product design.

          </p>


          <p class="section-description">

            Every system is designed around
            performance, scalability, maintainability
            and security.

          </p>

        </div>

      </div>

    </section>


    <!-- =====================================================
         SECURITY
    ====================================================== -->

    <section id="security">

      <div class="reveal">

        <div class="section-id">
          // 03 :: SECURITY RESEARCH
        </div>


        <h2 class="section-title">

          BUILD SECURE.

          <br>

          THINK

          <span class="glow-text">
            ADVERSARIAL.
          </span>

        </h2>


        <p class="section-description">

          Security is part of the engineering
          process — not an afterthought.

        </p>

      </div>


      <div class="security">


        <div class="reveal">

          <h2>

            SECURITY

            <br>

            BY

            <span class="glow-text">
              DESIGN.
            </span>

          </h2>


          <p>

            XyloTech combines software engineering
            with security research to understand,
            test and strengthen modern digital systems.

          </p>


          <div class="profiles">


            <a
              class="profile"
              href="https://hackerone.com/h4shk"
              target="_blank"
              rel="noopener noreferrer"
            >
              🛡 HACKERONE / h4shk ↗
            </a>


            <a
              class="profile"
              href="https://github.com/XyloTech"
              target="_blank"
              rel="noopener noreferrer"
            >
              ◈ GITHUB / XyloTech ↗
            </a>


            <a
              class="profile"
              href="https://www.linkedin.com/in/h4sho/"
              target="_blank"
              rel="noopener noreferrer"
            >
              ■ LINKEDIN / h4sho ↗
            </a>

          </div>

        </div>


        <div class="security-terminal reveal">


          <div class="security-bar">

            <span>
              security_matrix.sys
            </span>

            <span class="online">
              ● ONLINE
            </span>

          </div>


          <div class="security-code">

            <div>

              <span class="purple">
                researcher:
              </span>

              <span class="green">
                "h4shk"
              </span>

            </div>


            <div>

              <span class="purple">
                platform:
              </span>

              <span class="green">
                "HackerOne"
              </span>

            </div>


            <br>


            <div>

              <span class="cyan">
                SECURITY_MODULES
              </span>

            </div>


            <div>
              ├── Web Application Security
            </div>


            <div>
              ├── API Security
            </div>


            <div>
              ├── Authentication
            </div>


            <div>
              ├── Cloud Security
            </div>


            <div>
              ├── Vulnerability Research
            </div>


            <div>
              ├── AI / LLM Security
            </div>


            <div>
              └── Threat Modeling
            </div>


            <br>


            <div>

              <span class="green">
                RESEARCH_STATUS:
                ACTIVE
              </span>

            </div>


            <div>

              <span class="green">
                SYSTEM_STATUS:
                SECURE
              </span>

            </div>

          </div>

        </div>

      </div>

    </section>


    <!-- =====================================================
         PROCESS
    ====================================================== -->

    <section id="process">

      <div class="reveal">

        <div class="section-id">
          // 04 :: ENGINEERING PROTOCOL
        </div>


        <h2 class="section-title">

          IDEA

          <span class="glow-text">
            →
          </span>

          SYSTEM

        </h2>

      </div>


      <div class="process">


        <div class="process-card reveal">

          <span>
            PROTOCOL_01
          </span>

          <h3>
            DISCOVER
          </h3>

          <p>

            Understand the problem,
            users, requirements and
            desired outcome.

          </p>

        </div>


        <div class="process-card reveal">

          <span>
            PROTOCOL_02
          </span>

          <h3>
            ARCHITECT
          </h3>

          <p>

            Design the technical system,
            infrastructure and product
            experience.

          </p>

        </div>


        <div class="process-card reveal">

          <span>
            PROTOCOL_03
          </span>

          <h3>
            ENGINEER
          </h3>

          <p>

            Build, integrate, test and
            optimize the system.

          </p>

        </div>


        <div class="process-card reveal">

          <span>
            PROTOCOL_04
          </span>

          <h3>
            DEPLOY
          </h3>

          <p>

            Launch, monitor and evolve
            the system in production.

          </p>

        </div>

      </div>

    </section>


    <!-- =====================================================
         INDUSTRIES
    ====================================================== -->

    <section>

      <div class="reveal">

        <div class="section-id">
          // 05 :: INDUSTRIES
        </div>


        <h2 class="section-title">

          BUILT FOR

          <span class="glow-text">
            AMBITION.
          </span>

        </h2>

      </div>


      <div class="industries">


        <div class="industry reveal">

          <div class="industry-icon">
            ◈
          </div>

          <h3>
            FINTECH
          </h3>

          <p>
            Secure financial software
            and digital infrastructure.
          </p>

        </div>


        <div class="industry reveal">

          <div class="industry-icon">
            ◉
          </div>

          <h3>
            ARTIFICIAL INTELLIGENCE
          </h3>

          <p>
            AI applications, agents and
            intelligent automation.
          </p>

        </div>


        <div class="industry reveal">

          <div class="industry-icon">
            ⬡
          </div>

          <h3>
            STARTUPS
          </h3>

          <p>
            MVPs, product engineering
            and scalable architecture.
          </p>

        </div>


        <div class="industry reveal">

          <div class="industry-icon">
            ⌬
          </div>

          <h3>
            CYBERSECURITY
          </h3>

          <p>
            Security engineering and
            responsible research.
          </p>

        </div>


        <div class="industry reveal">

          <div class="industry-icon">
            △
          </div>

          <h3>
            SAAS
          </h3>

          <p>
            Multi-user platforms built
            for scale.
          </p>

        </div>


        <div class="industry reveal">

          <div class="industry-icon">
            ✦
          </div>

          <h3>
            E-COMMERCE
          </h3>

          <p>
            High-performance commerce
            experiences.
          </p>

        </div>


        <div class="industry reveal">

          <div class="industry-icon">
            ☁
          </div>

          <h3>
            CLOUD
          </h3>

          <p>
            Production infrastructure
            and DevOps systems.
          </p>

        </div>


        <div class="industry reveal">

          <div class="industry-icon">
            ⚙
          </div>

          <h3>
            ENTERPRISE
          </h3>

          <p>
            Custom systems for complex
            business requirements.
          </p>

        </div>

      </div>

    </section>


    <!-- =====================================================
         FOUNDER
    ====================================================== -->

    <section>

      <div class="reveal">

        <div class="section-id">
          // 06 :: COMMANDER
        </div>


        <h2 class="section-title">

          THE

          <span class="glow-text">
            BUILDER.
          </span>

        </h2>

      </div>


      <div class="founder reveal">


        <div class="founder-avatar">
          HK
        </div>


        <div>

          <h3>
            Harshit Kumar
          </h3>


          <div class="founder-role">

            Founder · CEO · XyloTech

          </div>


          <p>

            Building technology across software
            engineering, artificial intelligence,
            cybersecurity and digital infrastructure.

          </p>


          <div class="profiles">


            <a
              class="profile"
              href="https://github.com/XyloTech"
              target="_blank"
              rel="noopener noreferrer"
            >
              GITHUB ↗
            </a>


            <a
              class="profile"
              href="https://hackerone.com/h4shk"
              target="_blank"
              rel="noopener noreferrer"
            >
              HACKERONE ↗
            </a>


            <a
              class="profile"
              href="https://www.linkedin.com/in/h4sho/"
              target="_blank"
              rel="noopener noreferrer"
            >
              LINKEDIN ↗
            </a>

          </div>

        </div>

      </div>

    </section>


    <!-- =====================================================
         CTA
    ====================================================== -->

    <section id="contact">

      <div class="cta reveal">


        <div class="section-id">
          // SYSTEM READY
        </div>


        <h2>

          LET'S BUILD

          <br>

          THE

          <span class="glow-text">
            FUTURE.
          </span>

        </h2>


        <p>

          Have a difficult problem,
          ambitious idea or technology
          that needs to exist?

          Let's turn it into a real system.

        </p>


        <div class="hero-actions">


          <a
            href="mailto:hello@xylotech.dev"
            class="button primary"
          >
            CONTACT XYLOTECH →
          </a>


          <a
            href="https://xylotech.github.io/XyloTech/"
            target="_blank"
            rel="noopener noreferrer"
            class="button secondary"
          >
            OPEN WEBSITE ↗
          </a>


          <a
            href="https://github.com/XyloTech"
            target="_blank"
            rel="noopener noreferrer"
            class="button secondary"
          >
            SOURCE ↗
          </a>

        </div>

      </div>

    </section>

  </main>


  <!-- =======================================================
       FOOTER
  ======================================================== -->

  <footer>


    <div>

      XYLOTECH

      <span style="color:#39465e;">
        //
      </span>

      © 2026

      <span style="color:#39465e;">
        //
      </span>

      ALL SYSTEMS OPERATIONAL.

    </div>


    <div class="footer-links">


      <a
        href="https://xylotech.github.io/XyloTech/"
        target="_blank"
        rel="noopener noreferrer"
      >
        WEBSITE
      </a>


      <a
        href="https://github.com/XyloTech"
        target="_blank"
        rel="noopener noreferrer"
      >
        GITHUB
      </a>


      <a
        href="https://hackerone.com/h4shk"
        target="_blank"
        rel="noopener noreferrer"
      >
        HACKERONE
      </a>


      <a
        href="https://www.linkedin.com/in/h4sho/"
        target="_blank"
        rel="noopener noreferrer"
      >
        LINKEDIN
      </a>


      <a
        href="https://www.instagram.com/xylotech.in/"
        target="_blank"
        rel="noopener noreferrer"
      >
        INSTAGRAM
      </a>


      <a
        href="mailto:hello@xylotech.dev"
      >
        EMAIL
      </a>

    </div>

  </footer>


  <!-- =======================================================
       JAVASCRIPT
  ======================================================== -->

  <script>


    /* =========================================================
       BOOT SEQUENCE
    ========================================================= */

    const bootText =
      document.getElementById(
        "bootText"
      );


    const bootLines = [

      "> Initializing XyloTech OS...",

      "> Loading intelligence core...",

      "> Connecting security modules...",

      "> Initializing cloud infrastructure...",

      "> Loading engineering protocols...",

      "> Establishing secure channel...",

      "> SYSTEM ONLINE."

    ];


    let bootIndex = 0;


    function runBoot() {

      if (
        bootIndex >=
        bootLines.length
      ) {

        setTimeout(
          () => {

            document
              .getElementById("boot")
              .classList
              .add("done");

          },
          400
        );

        return;

      }


      const line =
        document.createElement(
          "div"
        );


      line.textContent =
        bootLines[
          bootIndex
        ];


      bootText.appendChild(
        line
      );


      bootIndex++;


      setTimeout(
        runBoot,
        250
      );

    }


    runBoot();


    /* =========================================================
       NEURAL NETWORK
    ========================================================= */

    const canvas =
      document.getElementById(
        "network"
      );


    const ctx =
      canvas.getContext("2d");


    let particles = [];


    let mouse = {
      x: null,
      y: null
    };


    function resize() {

      canvas.width =
        window.innerWidth;

      canvas.height =
        window.innerHeight;


      createParticles();

    }


    function createParticles() {

      particles = [];


      const count =
        Math.min(
          Math.floor(
            (
              window.innerWidth *
              window.innerHeight
            ) / 15000
          ),
          120
        );


      for (
        let i = 0;
        i < count;
        i++
      ) {

        particles.push({

          x:
            Math.random() *
            canvas.width,

          y:
            Math.random() *
            canvas.height,

          vx:
            (
              Math.random() -
              .5
            ) * .3,

          vy:
            (
              Math.random() -
              .5
            ) * .3,

          r:
            Math.random() *
            1.5 +
            .3

        });

      }

    }


    function drawNetwork() {

      ctx.clearRect(
        0,
        0,
        canvas.width,
        canvas.height
      );


      particles.forEach(
        (p, index) => {


          p.x += p.vx;

          p.y += p.vy;


          if (
            p.x < 0 ||
            p.x > canvas.width
          ) {

            p.vx *= -1;

          }


          if (
            p.y < 0 ||
            p.y > canvas.height
          ) {

            p.vy *= -1;

          }


          ctx.beginPath();


          ctx.arc(
            p.x,
            p.y,
            p.r,
            0,
            Math.PI * 2
          );


          ctx.fillStyle =
            "rgba(0,246,255,.55)";


          ctx.fill();


          for (
            let j =
              index + 1;
            j <
              particles.length;
            j++
          ) {


            const p2 =
              particles[j];


            const dx =
              p.x -
              p2.x;


            const dy =
              p.y -
              p2.y;


            const distance =
              Math.sqrt(
                dx * dx +
                dy * dy
              );


            if (
              distance <
              125
            ) {


              const opacity =
                (
                  1 -
                  distance /
                    125
                ) * .12;


              ctx.beginPath();


              ctx.moveTo(
                p.x,
                p.y
              );


              ctx.lineTo(
                p2.x,
                p2.y
              );


              ctx.strokeStyle =
                `rgba(0,246,255,${opacity})`;


              ctx.lineWidth =
                .6;


              ctx.stroke();

            }

          }


          if (
            mouse.x !== null
          ) {


            const dx =
              p.x -
              mouse.x;


            const dy =
              p.y -
              mouse.y;


            const distance =
              Math.sqrt(
                dx * dx +
                dy * dy
              );


            if (
              distance <
              180
            ) {


              ctx.beginPath();


              ctx.moveTo(
                p.x,
                p.y
              );


              ctx.lineTo(
                mouse.x,
                mouse.y
              );


              ctx.strokeStyle =
                `rgba(155,92,255,${
                  (
                    1 -
                    distance /
                      180
                  ) * .18
                })`;


              ctx.stroke();

            }

          }

        }
      );


      requestAnimationFrame(
        drawNetwork
      );

    }


    window.addEventListener(
      "resize",
      resize
    );


    window.addEventListener(
      "mousemove",
      event => {

        mouse.x =
          event.clientX;

        mouse.y =
          event.clientY;

      }
    );


    resize();

    drawNetwork();


    /* =========================================================
       SCROLL REVEAL
    ========================================================= */

    const revealObserver =
      new IntersectionObserver(

        entries => {

          entries.forEach(
            entry => {

              if (
                entry.isIntersecting
              ) {

                entry.target
                  .classList
                  .add("active");

                revealObserver
                  .unobserve(
                    entry.target
                  );

              }

            }
          );

        },

        {
          threshold:
            .12
        }

      );


    document
      .querySelectorAll(
        ".reveal"
      )
      .forEach(
        element => {

          revealObserver.observe(
            element
          );

        }
      );


    /* =========================================================
       COUNTERS
    ========================================================= */

    const counterObserver =
      new IntersectionObserver(

        entries => {

          entries.forEach(
            entry => {

              if (
                !entry.isIntersecting
              ) {

                return;

              }


              const element =
                entry.target;


              const target =
                Number(
                  element.dataset.target
                );


              const isPercent =
                element
                  .textContent
                  .includes("%");


              const suffix =
                isPercent
                  ? "%"
                  : "+";


              let start =
                performance.now();


              const duration =
                1300;


              function animate(
                current
              ) {


                const progress =
                  Math.min(
                    (
                      current -
                      start
                    ) / duration,
                    1
                  );


                const eased =
                  1 -
                  Math.pow(
                    1 -
                    progress,
                    3
                  );


                element.textContent =
                  Math.floor(
                    target *
                    eased
                  ) +
                  suffix;


                if (
                  progress <
                  1
                ) {

                  requestAnimationFrame(
                    animate
                  );

                }

              }


              requestAnimationFrame(
                animate
              );


              counterObserver
                .unobserve(
                  element
                );

            }
          );

        },

        {
          threshold:
            .8
        }

      );


    document
      .querySelectorAll(
        "[data-target]"
      )
      .forEach(
        counter => {

          counterObserver
            .observe(
              counter
            );

        }
      );


    /* =========================================================
       CARD TILT
    ========================================================= */

    document
      .querySelectorAll(
        ".system-card"
      )
      .forEach(
        card => {


          card.addEventListener(
            "mousemove",
            event => {


              const rect =
                card
                  .getBoundingClientRect();


              const x =
                event.clientX -
                rect.left;


              const y =
                event.clientY -
                rect.top;


              const rotateX =
                (
                  (
                    y -
                    rect.height / 2
                  ) /
                  rect.height
                ) * -5;


              const rotateY =
                (
                  (
                    x -
                    rect.width / 2
                  ) /
                  rect.width
                ) * 5;


              card.style.transform =
                `
                  perspective(700px)
                  rotateX(${rotateX}deg)
                  rotateY(${rotateY}deg)
                  translateY(-7px)
                `;

            }
          );


          card.addEventListener(
            "mouseleave",
            () => {

              card.style.transform =
                "";

            }
          );

        }
      );


    /* =========================================================
       NAVBAR
    ========================================================= */

    const nav =
      document.getElementById(
        "nav"
      );


    window.addEventListener(
      "scroll",
      () => {

        if (
          window.scrollY >
          40
        ) {

          nav.style.background =
            "rgba(2,5,12,.9)";

          nav.style.borderColor =
            "rgba(0,246,255,.2)";

        }

        else {

          nav.style.background =
            "rgba(2,5,12,.65)";

          nav.style.borderColor =
            "rgba(0,246,255,.12)";

        }

      }
    );


    /* =========================================================
       INTERNAL NAVIGATION
    ========================================================= */

    document
      .querySelectorAll(
        'a[href^="#"]'
      )
      .forEach(
        link => {

          link.addEventListener(
            "click",
            event => {

              const id =
                link.getAttribute(
                  "href"
                );


              if (
                id === "#"
              ) {

                return;

              }


              const target =
                document.querySelector(
                  id
                );


              if (
                !target
              ) {

                return;

              }


              event.preventDefault();


              target.scrollIntoView({

                behavior:
                  "smooth",

                block:
                  "start"

              });

            }
          );

        }
      );

  </script>

</body>
</html>
