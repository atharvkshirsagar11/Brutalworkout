<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>☠ BRUTAL PROTOCOL</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Barlow+Condensed:wght@400;600;700;900&display=swap');
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --red: #cc1500; --red-bright: #ff2200; --red-dim: #661100;
    --bg: #050000; --text: #f0ddd0; --text-dim: #996655; --text-muted: #553322;
    --border: rgba(180,40,20,0.3);
    --accent: #cc1500; --accent-bright: #ff2200;
    --surface: rgba(15,3,0,0.55); --surface2: rgba(40,5,0,0.5);
    --tab-active-bg: var(--accent); --tab-active-color: #fff;
    --modal-bg: linear-gradient(160deg,#1a0500 0%,#0c0100 100%);
    --header-glow: rgba(255,30,0,0.7);
    --badge-heavy-color:#ff2222; --badge-heavy-bg:rgba(200,20,0,0.12);
    --badge-volume-color:#cc6644; --badge-volume-bg:rgba(150,60,20,0.12);
    --badge-finisher-color:#ff6600; --badge-finisher-bg:rgba(180,70,0,0.12);
    --badge-abs-color:#aa5533; --badge-abs-bg:rgba(120,40,10,0.12);
    --logged-border: rgba(200,55,25,0.45);
    --progress-color: #ff5533;
    --day-header-bg: rgba(100,8,0,0.22);
    --ex-left-bar-heavy:#ff2222; --ex-left-bar-volume:#cc6644; --ex-left-bar-finisher:#ff6600; --ex-left-bar-abs:#994422;
    --btn-save-bg: #cc1100;
    --overlay-bg: rgba(0,0,0,0.85);
  }

  /* ============= THEMES ============= */
  .theme-midnight {
    --accent: #1a6fff; --accent-bright: #4488ff;
    --bg: #000810; --text: #c8ddf8; --text-dim: #4466aa; --text-muted: #223355;
    --border: rgba(30,80,200,0.3); --surface: rgba(0,5,20,0.7); --surface2: rgba(5,15,40,0.6);
    --tab-active-bg: #1a5fd0; --tab-active-color: #fff;
    --modal-bg: linear-gradient(160deg,#00081a 0%,#000510 100%);
    --header-glow: rgba(50,130,255,0.7);
    --badge-heavy-color:#4488ff; --badge-heavy-bg:rgba(20,60,200,0.15);
    --badge-volume-color:#6699dd; --badge-volume-bg:rgba(30,60,150,0.15);
    --badge-finisher-color:#44aaff; --badge-finisher-bg:rgba(20,80,180,0.15);
    --badge-abs-color:#3377cc; --badge-abs-bg:rgba(15,50,120,0.15);
    --logged-border: rgba(40,100,220,0.5);
    --progress-color: #4488ff;
    --day-header-bg: rgba(0,15,60,0.3);
    --ex-left-bar-heavy:#4488ff; --ex-left-bar-volume:#2266dd; --ex-left-bar-finisher:#44aaff; --ex-left-bar-abs:#3377cc;
    --btn-save-bg: #1155cc;
    --overlay-bg: rgba(0,5,20,0.88);
    --red: #1a6fff; --red-bright: #4488ff; --red-dim: #0a3399;
    --text-muted: #1a3366;
  }
  .theme-forest {
    --accent: #1a8c44; --accent-bright: #22bb55;
    --bg: #010a02; --text: #c8f0cc; --text-dim: #447755; --text-muted: #1a3322;
    --border: rgba(30,150,60,0.3); --surface: rgba(0,8,2,0.7); --surface2: rgba(5,20,8,0.6);
    --tab-active-bg: #1a7a38; --tab-active-color: #fff;
    --modal-bg: linear-gradient(160deg,#001a04 0%,#000d02 100%);
    --header-glow: rgba(40,200,80,0.6);
    --badge-heavy-color:#33dd66; --badge-heavy-bg:rgba(20,150,50,0.12);
    --badge-volume-color:#55aa77; --badge-volume-bg:rgba(30,120,60,0.12);
    --badge-finisher-color:#44cc55; --badge-finisher-bg:rgba(20,150,40,0.12);
    --badge-abs-color:#2a8844; --badge-abs-bg:rgba(15,100,35,0.12);
    --logged-border: rgba(40,180,70,0.45);
    --progress-color: #33dd66;
    --day-header-bg: rgba(0,60,15,0.25);
    --ex-left-bar-heavy:#33dd66; --ex-left-bar-volume:#22aa44; --ex-left-bar-finisher:#44cc55; --ex-left-bar-abs:#2a8844;
    --btn-save-bg: #187a30;
    --overlay-bg: rgba(0,8,2,0.9);
    --red: #1a8c44; --red-bright: #22bb55; --red-dim: #0a4422;
    --text-muted: #0d2211;
  }
  .theme-gold {
    --accent: #b8860b; --accent-bright: #ffd700;
    --bg: #080400; --text: #f5e8c0; --text-dim: #886622; --text-muted: #3a2a08;
    --border: rgba(180,130,20,0.3); --surface: rgba(12,8,0,0.7); --surface2: rgba(30,18,0,0.6);
    --tab-active-bg: #9a7008; --tab-active-color: #fff8cc;
    --modal-bg: linear-gradient(160deg,#1a0e00 0%,#0c0700 100%);
    --header-glow: rgba(255,215,0,0.6);
    --badge-heavy-color:#ffd700; --badge-heavy-bg:rgba(180,130,0,0.12);
    --badge-volume-color:#ccaa33; --badge-volume-bg:rgba(150,110,0,0.12);
    --badge-finisher-color:#ffcc00; --badge-finisher-bg:rgba(200,160,0,0.12);
    --badge-abs-color:#aa8822; --badge-abs-bg:rgba(130,95,0,0.12);
    --logged-border: rgba(200,160,30,0.5);
    --progress-color: #ffd700;
    --day-header-bg: rgba(60,40,0,0.25);
    --ex-left-bar-heavy:#ffd700; --ex-left-bar-volume:#ccaa33; --ex-left-bar-finisher:#ffcc00; --ex-left-bar-abs:#aa8822;
    --btn-save-bg: #9a7008;
    --overlay-bg: rgba(8,4,0,0.9);
    --red: #b8860b; --red-bright: #ffd700; --red-dim: #5a4005;
    --text-muted: #2a1c04;
  }
  .theme-custom { /* handled by JS inline vars */ }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Barlow Condensed', sans-serif;
    min-height: 100vh;
    overflow-x: hidden;
    transition: background 0.4s, color 0.4s;
  }
  body::before {
    content: '';
    position: fixed; inset: 0;
    background: radial-gradient(ellipse 90% 55% at 50% -5%, rgba(180,10,10,0.35) 0%, transparent 65%),
                radial-gradient(ellipse 55% 45% at 10% 90%, rgba(120,0,0,0.2) 0%, transparent 55%);
    pointer-events: none; z-index: 0;
    transition: all 0.4s;
  }
  body::after {
    content: ''; position: fixed; inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.85' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='1'/%3E%3C/svg%3E");
    background-size: 180px; opacity: 0.04; pointer-events: none; z-index: 0;
  }
  #app { position: relative; z-index: 1; max-width: 700px; margin: 0 auto; padding: 0 14px 90px; }

  /* ===== HEADER ===== */
  .header { text-align: center; padding: 30px 0 16px; position: relative; }
  .header-skull { font-size: 28px; }
  .header-title {
    font-family: 'Bebas Neue', sans-serif;
    font-size: 38px; letter-spacing: 10px;
    color: var(--accent-bright);
    text-shadow: 0 0 40px var(--header-glow), 0 0 80px rgba(200,0,0,0.2);
    line-height: 1; margin-top: 4px;
    transition: color 0.4s, text-shadow 0.4s;
    cursor: pointer; user-select: none;
  }
  .header-sub { font-size: 11px; letter-spacing: 4px; color: var(--text-dim); margin-top: 5px; text-transform: uppercase; transition: color 0.4s; }
  .header-line { width: 100px; height: 1px; background: linear-gradient(90deg, transparent, var(--accent-bright), transparent); margin: 12px auto 0; transition: background 0.4s; }
  .header-menu-btn {
    position: absolute; right: 0; top: 30px;
    background: var(--surface2); border: 1px solid var(--border);
    border-radius: 4px; padding: 7px 11px; cursor: pointer;
    color: var(--text-dim); font-size: 18px; line-height: 1;
    transition: all 0.15s;
  }
  .header-menu-btn:hover { background: var(--surface); color: var(--text); }

  /* ===== PEOPLE TABS ===== */
  .people-bar {
    display: flex; align-items: center; gap: 6px;
    background: rgba(0,0,0,0.2); border: 1px solid var(--border);
    border-radius: 5px; padding: 8px 10px; margin-bottom: 14px; flex-wrap: wrap;
  }
  .people-label { font-size: 9px; letter-spacing: 3px; color: var(--text-muted); text-transform: uppercase; margin-right: 4px; flex-shrink: 0; }
  .person-tab {
    background: var(--surface2); border: 1px solid var(--border);
    border-radius: 3px; padding: 5px 12px; cursor: pointer;
    font-size: 11px; letter-spacing: 1px; font-weight: 700;
    color: var(--text-dim); text-transform: uppercase;
    font-family: 'Barlow Condensed', sans-serif; transition: all 0.15s;
    display: flex; align-items: center; gap: 5px;
  }
  .person-tab:hover { background: var(--surface); color: var(--text); }
  .person-tab.active { background: var(--accent); color: #fff; border-color: var(--accent-bright); box-shadow: 0 0 12px rgba(200,20,0,0.3); }
  .person-tab .pt-dot { width: 6px; height: 6px; border-radius: 50%; background: currentColor; opacity: 0.7; }
  .add-person-btn {
    background: transparent; border: 1px dashed var(--border);
    border-radius: 3px; padding: 5px 10px; cursor: pointer;
    font-size: 12px; color: var(--text-muted); font-family: 'Barlow Condensed', sans-serif;
    transition: all 0.15s;
  }
  .add-person-btn:hover { color: var(--text-dim); border-color: var(--text-muted); }

  /* ===== DAY TABS ===== */
  .day-tabs { display: flex; gap: 5px; justify-content: center; flex-wrap: wrap; margin: 16px 0; }
  .day-tab {
    background: var(--surface2); color: var(--text-muted); border: 1px solid rgba(100,25,10,0.3);
    border-radius: 3px; padding: 7px 12px; font-size: 11px; letter-spacing: 3px; font-weight: 700;
    cursor: pointer; text-transform: uppercase; font-family: 'Barlow Condensed', sans-serif;
    transition: all 0.16s; display: flex; align-items: center; gap: 4px;
  }
  .day-tab:hover { background: var(--surface); color: var(--text-dim); }
  .day-tab.active { background: var(--tab-active-bg); color: var(--tab-active-color); border-color: var(--accent-bright); box-shadow: 0 0 16px rgba(200,20,0,0.35); }
  .day-tab .dt-done { font-size: 8px; opacity: 0.7; }

  /* ===== DAY HEADER ROW ===== */
  .day-header-row {
    display: flex; align-items: center; gap: 8px; margin-bottom: 12px;
  }
  .day-header {
    flex: 1;
    background: var(--day-header-bg); border: 1px solid rgba(190,40,20,0.2);
    border-radius: 4px; padding: 13px 15px;
    transition: background 0.4s;
  }
  .day-title {
    font-family: 'Bebas Neue', sans-serif; font-size: 24px;
    letter-spacing: 4px; color: var(--accent-bright);
    text-shadow: 0 0 20px rgba(255,50,20,0.3); transition: color 0.4s;
  }
  .day-target { font-size: 10px; letter-spacing: 3px; color: var(--text-muted); margin-top: 2px; text-transform: uppercase; }
  .day-dots-btn {
    flex-shrink: 0;
    background: var(--surface2); border: 1px solid var(--border);
    border-radius: 4px; padding: 8px 11px; cursor: pointer;
    color: var(--text-dim); font-size: 16px; line-height: 1;
    transition: all 0.15s; align-self: stretch; display: flex; align-items: center;
  }
  .day-dots-btn:hover { background: var(--surface); color: var(--text); }

  /* ===== EXERCISE LIST ===== */
  .exercise-list { display: flex; flex-direction: column; gap: 6px; }
  .ex-btn {
    background: var(--surface); border: 1px solid rgba(70,15,5,0.3);
    border-radius: 4px; padding: 11px 13px; text-align: left; cursor: pointer;
    transition: all 0.15s; display: flex; justify-content: space-between; align-items: center;
    gap: 10px; width: 100%; font-family: 'Barlow Condensed', sans-serif;
    color: var(--text); position: relative; overflow: hidden;
  }
  .ex-btn::before {
    content: ''; position: absolute; left: 0; top: 0; bottom: 0; width: 3px;
  }
  .ex-btn[data-type="HEAVY"]::before { background: var(--ex-left-bar-heavy); }
  .ex-btn[data-type="VOLUME"]::before { background: var(--ex-left-bar-volume); }
  .ex-btn[data-type="FINISHER"]::before { background: var(--ex-left-bar-finisher); }
  .ex-btn[data-type="ABS"]::before { background: var(--ex-left-bar-abs); }
  .ex-btn:hover { background: rgba(50,10,0,0.55); border-color: rgba(150,35,15,0.35); }
  .ex-btn.logged { border-color: var(--logged-border); }
  .ex-left { flex: 1; min-width: 0; }
  .ex-meta { display: flex; align-items: center; gap: 6px; }
  .type-badge {
    font-size: 9px; letter-spacing: 2px; font-weight: 700;
    padding: 2px 5px; border-radius: 2px; flex-shrink: 0;
  }
  .type-badge.HEAVY { color: var(--badge-heavy-color); background: var(--badge-heavy-bg); border: 1px solid rgba(255,30,0,0.2); }
  .type-badge.VOLUME { color: var(--badge-volume-color); background: var(--badge-volume-bg); border: 1px solid rgba(180,70,30,0.2); }
  .type-badge.FINISHER { color: var(--badge-finisher-color); background: var(--badge-finisher-bg); border: 1px solid rgba(220,90,0,0.2); }
  .type-badge.ABS { color: var(--badge-abs-color); background: var(--badge-abs-bg); border: 1px solid rgba(140,55,20,0.2); }
  .ex-name { font-size: 13px; font-weight: 700; color: var(--text-dim); letter-spacing: 0.5px; }
  .ex-btn.logged .ex-name { color: var(--text); }
  .ex-saved { margin-top: 4px; font-size: 10px; color: var(--accent-bright); letter-spacing: 0.3px; display: flex; flex-wrap: wrap; gap: 6px; opacity: 0.85; }
  .next-target { color: #ffaa44; }
  .ex-right { text-align: right; flex-shrink: 0; }
  .ex-sets { font-size: 12px; color: var(--text-muted); letter-spacing: 1px; font-weight: 700; }
  .ex-tap { font-size: 9px; color: var(--text-muted); margin-top: 4px; letter-spacing: 1px; opacity: 0.6; }
  .ex-check { font-size: 14px; color: var(--accent-bright); margin-top: 3px; }

  /* ===== PROGRESS BAR ===== */
  .day-progress {
    margin-top: 14px; padding: 10px 14px;
    background: rgba(60,8,0,0.18); border: 1px solid rgba(100,25,10,0.18);
    border-radius: 4px; display: flex; justify-content: space-between; align-items: center;
  }
  .progress-label { font-size: 10px; letter-spacing: 3px; color: var(--text-muted); text-transform: uppercase; }
  .progress-count { font-size: 12px; color: var(--progress-color); font-weight: 700; }
  .progress-bar-wrap { height: 3px; background: rgba(255,255,255,0.05); border-radius: 2px; margin-top: 8px; overflow: hidden; }
  .progress-bar-fill { height: 100%; background: var(--accent); border-radius: 2px; transition: width 0.4s ease; }

  /* ===== DROPDOWN MENU ===== */
  .dropdown-wrap { position: relative; display: inline-block; }
  .dropdown-menu {
    display: none; position: absolute; right: 0; top: calc(100% + 6px);
    background: #110200; border: 1px solid var(--border);
    border-radius: 5px; min-width: 180px; z-index: 200;
    box-shadow: 0 8px 30px rgba(0,0,0,0.7);
    overflow: hidden;
  }
  .dropdown-menu.open { display: block; animation: fadeIn 0.15s ease; }
  @keyframes fadeIn { from { opacity:0; transform:translateY(-6px); } to { opacity:1; transform:translateY(0); } }
  .dropdown-item {
    padding: 11px 14px; font-size: 12px; letter-spacing: 1px; font-weight: 700;
    color: var(--text-dim); cursor: pointer; display: flex; align-items: center; gap: 9px;
    text-transform: uppercase; font-family: 'Barlow Condensed', sans-serif;
    border-bottom: 1px solid rgba(255,255,255,0.03); transition: background 0.12s;
  }
  .dropdown-item:last-child { border-bottom: none; }
  .dropdown-item:hover { background: rgba(255,255,255,0.05); color: var(--text); }
  .dropdown-item.danger { color: #cc4422; }
  .dropdown-item.danger:hover { background: rgba(200,30,0,0.1); color: #ff5533; }
  .dropdown-icon { font-size: 14px; width: 18px; text-align: center; }
  .dropdown-divider { height: 1px; background: rgba(255,255,255,0.04); margin: 2px 0; }

  /* ===== MODAL OVERLAY ===== */
  .modal-overlay {
    display: none; position: fixed; inset: 0; z-index: 300;
    background: var(--overlay-bg); align-items: center; justify-content: center;
    padding: 16px; backdrop-filter: blur(4px);
  }
  .modal-overlay.open { display: flex; }
  .modal {
    background: var(--modal-bg); border: 1px solid rgba(200,40,20,0.45);
    border-top: 3px solid var(--accent); border-radius: 6px;
    padding: 20px 16px; width: 100%; max-width: 380px;
    box-shadow: 0 0 50px rgba(180,20,0,0.25), 0 20px 50px rgba(0,0,0,0.8);
    animation: slideUp 0.2s ease; max-height: 92vh; overflow-y: auto;
    transition: border-color 0.4s;
  }
  @keyframes slideUp { from { transform:translateY(18px); opacity:0; } to { transform:translateY(0); opacity:1; } }
  .modal-close { float: right; background: none; border: none; color: var(--text-muted); font-size: 20px; cursor: pointer; line-height: 1; margin-top: -2px; }
  .modal-close:hover { color: var(--text-dim); }
  .modal-type { font-size: 9px; letter-spacing: 3px; color: var(--accent); text-transform: uppercase; margin-bottom: 4px; }
  .modal-name { font-family: 'Bebas Neue', sans-serif; font-size: 20px; letter-spacing: 2px; color: var(--text); line-height: 1.1; margin-bottom: 16px; }
  .modal-title { font-family: 'Bebas Neue', sans-serif; font-size: 20px; letter-spacing: 3px; color: var(--accent-bright); margin-bottom: 16px; }
  .field { display: flex; flex-direction: column; gap: 4px; margin-bottom: 11px; }
  .field label { font-size: 10px; letter-spacing: 3px; color: var(--text-muted); text-transform: uppercase; }
  .field input, .field textarea, .field select {
    background: rgba(25,4,0,0.65); border: 1px solid rgba(140,35,15,0.3);
    border-radius: 3px; color: var(--text); font-size: 14px; padding: 9px 11px;
    font-family: 'Barlow Condensed', sans-serif; outline: none; width: 100%;
    transition: border-color 0.15s;
  }
  .field input:focus, .field textarea:focus, .field select:focus { border-color: rgba(200,60,30,0.55); }
  .field select { appearance: none; cursor: pointer; }
  .field select option { background: #110200; }
  .field textarea { resize: vertical; }
  input::placeholder, textarea::placeholder { color: #553322; }

  .inc-row { display: flex; gap: 6px; margin-top: 4px; }
  .inc-btn {
    flex: 1; padding: 9px 0; background: var(--surface2); border: 1px solid rgba(90,20,5,0.35);
    border-radius: 3px; color: var(--text-muted); font-size: 12px; font-weight: 700;
    cursor: pointer; font-family: 'Barlow Condensed', sans-serif; letter-spacing: 1px; transition: all 0.14s;
  }
  .inc-btn.active { background: var(--accent); border-color: var(--accent-bright); color: #fff; box-shadow: 0 0 10px rgba(200,20,0,0.3); }
  .next-preview { text-align: center; font-size: 11px; color: var(--accent-bright); margin-top: 7px; letter-spacing: 1px; min-height: 16px; }

  .modal-btns { display: flex; gap: 7px; margin-top: 14px; }
  .btn-save {
    flex: 2; padding: 12px 0; background: var(--btn-save-bg); border: none; border-radius: 3px;
    color: #fff; font-size: 13px; font-weight: 900; letter-spacing: 3px; text-transform: uppercase;
    cursor: pointer; font-family: 'Barlow Condensed', sans-serif;
    box-shadow: 0 0 16px rgba(200,20,0,0.3); transition: opacity 0.15s;
  }
  .btn-save:hover { opacity: 0.88; }
  .btn-secondary {
    flex: 1; padding: 12px 0; background: rgba(30,0,0,0.5); border: 1px solid rgba(90,15,5,0.35);
    border-radius: 3px; color: var(--text-muted); font-size: 10px; font-weight: 700; letter-spacing: 2px;
    text-transform: uppercase; cursor: pointer; font-family: 'Barlow Condensed', sans-serif; transition: all 0.14s;
  }
  .btn-secondary:hover { color: var(--text-dim); }

  /* ===== ADD WORKOUT MODAL ===== */
  .plan-day-block {
    background: rgba(0,0,0,0.2); border: 1px solid var(--border); border-radius: 4px;
    padding: 12px; margin-bottom: 10px;
  }
  .plan-day-header {
    display: flex; align-items: center; gap: 8px; margin-bottom: 10px;
    font-family: 'Bebas Neue', sans-serif; font-size: 16px; letter-spacing: 3px; color: var(--accent-bright);
  }
  .plan-day-header input {
    flex: 1; background: transparent; border: none; border-bottom: 1px solid var(--border);
    color: var(--accent-bright); font-family: 'Bebas Neue', sans-serif; font-size: 16px;
    letter-spacing: 3px; outline: none; padding: 2px 4px;
  }
  .ex-row { display: flex; gap: 6px; margin-bottom: 6px; align-items: center; }
  .ex-row input { flex: 1; }
  .ex-row select { width: 90px; flex-shrink: 0; }
  .ex-row .sets-input { width: 70px; flex-shrink: 0; }
  .remove-ex-btn {
    background: none; border: none; color: var(--text-muted); font-size: 14px; cursor: pointer;
    padding: 4px; line-height: 1; transition: color 0.12s; flex-shrink: 0;
  }
  .remove-ex-btn:hover { color: #ff4422; }
  .add-ex-btn {
    background: transparent; border: 1px dashed var(--border); border-radius: 3px;
    padding: 6px 10px; cursor: pointer; color: var(--text-muted); font-size: 11px;
    letter-spacing: 2px; font-family: 'Barlow Condensed', sans-serif; width: 100%;
    text-align: center; transition: all 0.14s; margin-top: 4px;
  }
  .add-ex-btn:hover { color: var(--text-dim); border-color: var(--text-muted); }
  .add-day-btn {
    background: transparent; border: 1px dashed var(--border); border-radius: 4px;
    padding: 10px; cursor: pointer; color: var(--text-muted); font-size: 11px;
    letter-spacing: 2px; font-family: 'Barlow Condensed', sans-serif; width: 100%;
    text-align: center; transition: all 0.14s; margin-bottom: 12px;
  }
  .add-day-btn:hover { color: var(--text-dim); border-color: var(--text-muted); }

  /* ===== THEME PICKER ===== */
  .theme-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 8px; margin-bottom: 14px; }
  .theme-card {
    padding: 12px; border-radius: 4px; cursor: pointer; border: 2px solid transparent;
    transition: all 0.18s; display: flex; flex-direction: column; gap: 4px;
  }
  .theme-card.active { border-color: #fff !important; }
  .theme-card .tc-name { font-size: 11px; letter-spacing: 2px; font-weight: 700; text-transform: uppercase; }
  .theme-card .tc-swatch { display: flex; gap: 4px; margin-top: 4px; }
  .tc-dot { width: 12px; height: 12px; border-radius: 50%; }
  .theme-card-brutal { background: #150000; border-color: rgba(200,30,10,0.4); }
  .theme-card-brutal .tc-name { color: #ff3322; }
  .theme-card-midnight { background: #000c1a; border-color: rgba(30,80,200,0.4); }
  .theme-card-midnight .tc-name { color: #4488ff; }
  .theme-card-forest { background: #010d03; border-color: rgba(30,150,50,0.4); }
  .theme-card-forest .tc-name { color: #33dd66; }
  .theme-card-gold { background: #100800; border-color: rgba(180,130,20,0.4); }
  .theme-card-gold .tc-name { color: #ffd700; }
  .custom-theme-section { background: rgba(0,0,0,0.2); border: 1px solid var(--border); border-radius: 4px; padding: 12px; }
  .custom-theme-title { font-size: 10px; letter-spacing: 3px; color: var(--text-muted); text-transform: uppercase; margin-bottom: 10px; }
  .color-row { display: flex; align-items: center; gap: 8px; margin-bottom: 8px; }
  .color-row label { font-size: 11px; letter-spacing: 1px; color: var(--text-dim); flex: 1; }
  .color-row input[type="color"] { width: 40px; height: 28px; padding: 2px; border-radius: 3px; cursor: pointer; border: 1px solid var(--border); background: transparent; }

  /* ===== PERSON MANAGE ===== */
  .person-item {
    display: flex; align-items: center; gap: 8px;
    padding: 10px 12px; background: var(--surface); border: 1px solid var(--border);
    border-radius: 4px; margin-bottom: 7px;
  }
  .person-item .pi-name { flex: 1; font-size: 13px; font-weight: 700; color: var(--text); }
  .person-item .pi-plan { font-size: 10px; color: var(--text-muted); letter-spacing: 1px; }
  .person-item-btns { display: flex; gap: 5px; }
  .pi-btn {
    background: var(--surface2); border: 1px solid var(--border); border-radius: 3px;
    padding: 5px 9px; cursor: pointer; font-size: 11px; color: var(--text-muted);
    font-family: 'Barlow Condensed', sans-serif; transition: all 0.14s;
  }
  .pi-btn:hover { color: var(--text); }
  .pi-btn.danger:hover { color: #ff4422; border-color: rgba(200,30,0,0.4); }

  /* ===== EMPTY STATE ===== */
  .empty-state {
    text-align: center; padding: 40px 20px;
    color: var(--text-muted); font-size: 13px; letter-spacing: 2px;
  }
  .empty-state .es-icon { font-size: 32px; margin-bottom: 10px; }
  .empty-state .es-title { font-family: 'Bebas Neue', sans-serif; font-size: 20px; letter-spacing: 4px; color: var(--text-dim); margin-bottom: 8px; }

  /* ===== SCROLLBAR ===== */
  ::-webkit-scrollbar { width: 4px; }
  ::-webkit-scrollbar-track { background: transparent; }
  ::-webkit-scrollbar-thumb { background: rgba(150,30,10,0.4); border-radius: 2px; }

  /* ===== TOAST ===== */
  .toast {
    position: fixed; bottom: 24px; left: 50%; transform: translateX(-50%) translateY(0);
    background: var(--accent); color: #fff; padding: 9px 20px; border-radius: 4px;
    font-size: 11px; letter-spacing: 2px; font-weight: 700; z-index: 500;
    opacity: 0; transition: opacity 0.3s; pointer-events: none;
    font-family: 'Barlow Condensed', sans-serif;
  }
  .toast.show { opacity: 1; }
</style>
</head>
<body>

<div id="app">
  <div class="header">
    <div class="header-skull">☠</div>
    <div class="header-title" id="appTitle" onclick="openRenameApp()">BRUTAL PROTOCOL</div>
    <div class="header-sub" id="appSubtitle">Tap title to rename</div>
    <div class="header-line"></div>
    <div class="dropdown-wrap" style="position:absolute;right:0;top:30px">
      <button class="header-menu-btn" onclick="toggleDropdown('mainMenu')">⋮</button>
      <div class="dropdown-menu" id="mainMenu">
        <div class="dropdown-item" onclick="openThemeModal()"><span class="dropdown-icon">🎨</span> Change Theme</div>
        <div class="dropdown-item" onclick="openRenameApp()"><span class="dropdown-icon">✏️</span> Rename App</div>
        <div class="dropdown-divider"></div>
        <div class="dropdown-item" onclick="openPeopleModal()"><span class="dropdown-icon">👥</span> Manage People</div>
        <div class="dropdown-item" onclick="openAddPersonModal()"><span class="dropdown-icon">➕</span> Add Person</div>
        <div class="dropdown-divider"></div>
        <div class="dropdown-item" onclick="exportData()"><span class="dropdown-icon">📤</span> Export Data</div>
        <div class="dropdown-item" onclick="importData()"><span class="dropdown-icon">📥</span> Import Data</div>
      </div>
    </div>
  </div>

  <div class="people-bar" id="peopleBar">
    <span class="people-label">👤</span>
    <div id="personTabs"></div>
    <button class="add-person-btn" onclick="openAddPersonModal()">+ ADD</button>
  </div>

  <div class="day-tabs" id="dayTabs"></div>

  <div class="day-header-row">
    <div class="day-header">
      <div class="day-title" id="dayTitle"></div>
      <div class="day-target" id="dayTarget"></div>
    </div>
    <div class="dropdown-wrap">
      <button class="day-dots-btn" onclick="toggleDropdown('dayMenu')">⋮</button>
      <div class="dropdown-menu" id="dayMenu">
        <div class="dropdown-item" onclick="openRenameDay()"><span class="dropdown-icon">✏️</span> Rename Day</div>
        <div class="dropdown-item" onclick="openAddWorkoutModal('replace')"><span class="dropdown-icon">🔄</span> Replace Workout</div>
        <div class="dropdown-item" onclick="openAddWorkoutModal('day')"><span class="dropdown-icon">➕</span> Add New Day</div>
        <div class="dropdown-divider"></div>
        <div class="dropdown-item danger" onclick="resetDayLog()"><span class="dropdown-icon">🗑️</span> Reset Day Log</div>
        <div class="dropdown-item danger" onclick="deleteDay()"><span class="dropdown-icon">❌</span> Delete This Day</div>
      </div>
    </div>
  </div>

  <div class="exercise-list" id="exerciseList"></div>

  <div class="day-progress" id="dayProgressWrap">
    <div style="flex:1">
      <div style="display:flex;justify-content:space-between;align-items:center">
        <span class="progress-label">Day Progress</span>
        <span class="progress-count" id="progressCount"></span>
      </div>
      <div class="progress-bar-wrap"><div class="progress-bar-fill" id="progressBarFill"></div></div>
    </div>
  </div>
</div>

<!-- ===== LOG EXERCISE MODAL ===== -->
<div class="modal-overlay" id="logModal">
  <div class="modal">
    <button class="modal-close" onclick="closeModal('logModal')">✕</button>
    <div class="modal-type" id="modalType"></div>
    <div class="modal-name" id="modalName"></div>
    <div class="field">
      <label>Weight (kg)</label>
      <input type="number" id="inputWeight" placeholder="e.g. 80">
    </div>
    <div class="field">
      <label>Plate Setup</label>
      <input type="text" id="inputPlates" placeholder="e.g. 20+10+5 each side">
    </div>
    <div class="field">
      <label>Reps Completed</label>
      <input type="text" id="inputReps" placeholder="e.g. 5,5,5,4,4">
    </div>
    <div class="field">
      <label>Add Next Week</label>
      <div class="inc-row">
        <button class="inc-btn" data-val="2.5" onclick="setIncrement('2.5')">+2.5 kg</button>
        <button class="inc-btn" data-val="5" onclick="setIncrement('5')">+5 kg</button>
        <button class="inc-btn" data-val="0" onclick="setIncrement('0')">SAME</button>
      </div>
      <div class="next-preview" id="nextPreview"></div>
    </div>
    <div class="field">
      <label>Notes</label>
      <textarea id="inputNotes" rows="2" placeholder="Form cues, how it felt..."></textarea>
    </div>
    <div class="modal-btns">
      <button class="btn-save" onclick="saveEntry()">SAVE ☠</button>
      <button class="btn-secondary" id="btnClear" onclick="clearEntry()" style="display:none">CLEAR</button>
      <button class="btn-secondary" onclick="closeModal('logModal')">CANCEL</button>
    </div>
  </div>
</div>

<!-- ===== THEME MODAL ===== -->
<div class="modal-overlay" id="themeModal">
  <div class="modal">
    <button class="modal-close" onclick="closeModal('themeModal')">✕</button>
    <div class="modal-title">🎨 THEME</div>
    <div class="theme-grid">
      <div class="theme-card theme-card-brutal" onclick="applyTheme('brutal')" id="tc-brutal">
        <div class="tc-name">Brutal Red</div>
        <div class="tc-swatch"><div class="tc-dot" style="background:#ff2200"></div><div class="tc-dot" style="background:#050000"></div><div class="tc-dot" style="background:#cc6644"></div></div>
      </div>
      <div class="theme-card theme-card-midnight" onclick="applyTheme('midnight')" id="tc-midnight">
        <div class="tc-name">Midnight Blue</div>
        <div class="tc-swatch"><div class="tc-dot" style="background:#4488ff"></div><div class="tc-dot" style="background:#000810"></div><div class="tc-dot" style="background:#2255aa"></div></div>
      </div>
      <div class="theme-card theme-card-forest" onclick="applyTheme('forest')" id="tc-forest">
        <div class="tc-name">Forest Green</div>
        <div class="tc-swatch"><div class="tc-dot" style="background:#33dd66"></div><div class="tc-dot" style="background:#010a02"></div><div class="tc-dot" style="background:#22aa44"></div></div>
      </div>
      <div class="theme-card theme-card-gold" onclick="applyTheme('gold')" id="tc-gold">
        <div class="tc-name">Gold Warrior</div>
        <div class="tc-swatch"><div class="tc-dot" style="background:#ffd700"></div><div class="tc-dot" style="background:#080400"></div><div class="tc-dot" style="background:#ccaa33"></div></div>
      </div>
    </div>
    <div class="custom-theme-section">
      <div class="custom-theme-title">⚡ Custom Colors</div>
      <div class="color-row"><label>Accent / Main Color</label><input type="color" id="customAccent" value="#cc1500" oninput="applyCustomTheme()"></div>
      <div class="color-row"><label>Background</label><input type="color" id="customBg" value="#050000" oninput="applyCustomTheme()"></div>
      <div class="color-row"><label>Text Color</label><input type="color" id="customText" value="#f0ddd0" oninput="applyCustomTheme()"></div>
    </div>
    <div class="modal-btns" style="margin-top:14px">
      <button class="btn-save" onclick="closeModal('themeModal')">DONE</button>
    </div>
  </div>
</div>

<!-- ===== ADD/REPLACE WORKOUT MODAL ===== -->
<div class="modal-overlay" id="workoutModal">
  <div class="modal" style="max-width:500px">
    <button class="modal-close" onclick="closeModal('workoutModal')">✕</button>
    <div class="modal-title" id="workoutModalTitle">ADD WORKOUT PLAN</div>
    <div class="field">
      <label>Add Mode</label>
      <select id="addModeSelect" onchange="renderWorkoutPlanBuilder()">
        <option value="all">Full Week Plan (add all 6 days at once)</option>
        <option value="single">Single Day Only</option>
      </select>
    </div>
    <div id="planBuilder"></div>
    <div class="modal-btns">
      <button class="btn-save" onclick="savePlan()">SAVE PLAN ☠</button>
      <button class="btn-secondary" onclick="closeModal('workoutModal')">CANCEL</button>
    </div>
  </div>
</div>

<!-- ===== ADD/MANAGE PEOPLE MODAL ===== -->
<div class="modal-overlay" id="peopleModal">
  <div class="modal">
    <button class="modal-close" onclick="closeModal('peopleModal')">✕</button>
    <div class="modal-title">👥 PEOPLE</div>
    <div id="peopleList"></div>
    <div class="modal-btns">
      <button class="btn-save" onclick="openAddPersonModal()">+ ADD PERSON</button>
      <button class="btn-secondary" onclick="closeModal('peopleModal')">DONE</button>
    </div>
  </div>
</div>

<!-- ===== ADD PERSON MODAL ===== -->
<div class="modal-overlay" id="addPersonModal">
  <div class="modal">
    <button class="modal-close" onclick="closeModal('addPersonModal')">✕</button>
    <div class="modal-title" id="addPersonTitle">ADD PERSON</div>
    <div class="field">
      <label>Name</label>
      <input type="text" id="newPersonName" placeholder="e.g. Atharv, Client 1...">
    </div>
    <div class="field" id="planChoiceField">
      <label>Workout Plan</label>
      <select id="newPersonPlan">
        <option value="default">Use Default Plan (6-Day PPL)</option>
        <option value="empty">Start Empty (add later)</option>
        <option value="copy">Copy from current person</option>
      </select>
    </div>
    <div class="modal-btns">
      <button class="btn-save" onclick="saveNewPerson()">ADD ☠</button>
      <button class="btn-secondary" onclick="closeModal('addPersonModal')">CANCEL</button>
    </div>
  </div>
</div>

<!-- ===== RENAME MODAL ===== -->
<div class="modal-overlay" id="renameModal">
  <div class="modal">
    <button class="modal-close" onclick="closeModal('renameModal')">✕</button>
    <div class="modal-title" id="renameModalTitle">RENAME</div>
    <div class="field">
      <label id="renameLabel">New Name</label>
      <input type="text" id="renameInput" placeholder="Enter name...">
    </div>
    <div class="field" id="renameSubField" style="display:none">
      <label>Subtitle / Target</label>
      <input type="text" id="renameSubInput" placeholder="e.g. CHEST & TRICEPS">
    </div>
    <div class="modal-btns">
      <button class="btn-save" onclick="saveRename()">SAVE</button>
      <button class="btn-secondary" onclick="closeModal('renameModal')">CANCEL</button>
    </div>
  </div>
</div>

<!-- TOAST -->
<div class="toast" id="toast"></div>

<input type="file" id="importFileInput" accept=".json" style="display:none" onchange="handleImport(event)">

<script>
// ============================================================
// DEFAULT PLAN DATA
// ============================================================
const DEFAULT_DAYS = [
  { title:"CHEST DESTRUCTION", target:"PECTORALS & CORE", exercises:[
    { id:"d1_1", name:"Barbell Bench Press", sets:"5×5", type:"HEAVY" },
    { id:"d1_2", name:"Incline Dumbbell Press", sets:"4×8", type:"HEAVY" },
    { id:"d1_3", name:"Incline Barbell Bench Press", sets:"4×12", type:"VOLUME" },
    { id:"d1_4", name:"Flat Dumbbell Press", sets:"4×12", type:"VOLUME" },
    { id:"d1_5", name:"Pec Deck Fly", sets:"5×15", type:"VOLUME" },
    { id:"d1_6", name:"Cable Fly (Mid-to-Low)", sets:"4×20", type:"VOLUME" },
    { id:"d1_7", name:"Bodyweight Push-ups", sets:"3×AMRAP", type:"FINISHER" },
    { id:"d1_8", name:"Hanging Leg Raises", sets:"4×15", type:"ABS" },
    { id:"d1_9", name:"Cable Crunches", sets:"4×20", type:"ABS" },
  ]},
  { title:"BACK DESTRUCTION", target:"UPPER & LOWER BACK", exercises:[
    { id:"d2_1", name:"Conventional Deadlift", sets:"5×5", type:"HEAVY" },
    { id:"d2_2", name:"Lat Pulldown (Chest Focus)", sets:"5×8", type:"HEAVY" },
    { id:"d2_3", name:"Barbell Row (Overhand)", sets:"5×10", type:"VOLUME" },
    { id:"d2_4", name:"Dumbbell Row (Single-Arm)", sets:"4×12", type:"VOLUME" },
    { id:"d2_5", name:"Seated Cable Row (V-Bar)", sets:"4×15", type:"VOLUME" },
    { id:"d2_6", name:"Wide Grip Lat Pulldown", sets:"5×12", type:"VOLUME" },
    { id:"d2_7", name:"Straight Arm Pulldown", sets:"4×15", type:"VOLUME" },
    { id:"d2_8", name:"Decline Sit-ups", sets:"4×20", type:"ABS" },
    { id:"d2_9", name:"Prone Plank", sets:"3×60s", type:"ABS" },
  ]},
  { title:"QUAD MURDER DAY", target:"QUADS & CALVES", exercises:[
    { id:"d3_1", name:"Barbell Back Squat", sets:"6×6", type:"HEAVY" },
    { id:"d3_2", name:"Leg Press (Wide Stance)", sets:"5×20", type:"VOLUME" },
    { id:"d3_3", name:"Walking Dumbbell Lunges", sets:"4×20 steps", type:"VOLUME" },
    { id:"d3_4", name:"Barbell Front Squat", sets:"4×15", type:"VOLUME" },
    { id:"d3_5", name:"Leg Extension", sets:"5×20", type:"VOLUME" },
    { id:"d3_6", name:"Bodyweight Squats", sets:"1×100", type:"FINISHER" },
    { id:"d3_7", name:"Standing Calf Raise", sets:"6×20", type:"HEAVY" },
    { id:"d3_8", name:"Hanging Knee Raises", sets:"4×20", type:"ABS" },
  ]},
  { title:"SHOULDER WARFARE", target:"DELTOIDS & TRAPS", exercises:[
    { id:"d4_1", name:"Standing Barbell OHP", sets:"5×5", type:"HEAVY" },
    { id:"d4_2", name:"Seated Barbell Press", sets:"5×10", type:"VOLUME" },
    { id:"d4_3", name:"Machine Shoulder Press", sets:"4×12", type:"VOLUME" },
    { id:"d4_4", name:"Dumbbell Lateral Raise", sets:"8×15", type:"VOLUME" },
    { id:"d4_5", name:"Cable Lateral Raise", sets:"4×20", type:"VOLUME" },
    { id:"d4_6", name:"Rear Delt Machine Fly", sets:"5×15", type:"VOLUME" },
    { id:"d4_7", name:"Rope Face Pulls", sets:"5×20", type:"VOLUME" },
    { id:"d4_8", name:"Lateral Raise Dropset", sets:"3 Dropsets", type:"FINISHER" },
    { id:"d4_9", name:"Heavy Cable Crunches", sets:"5×20", type:"ABS" },
  ]},
  { title:"ARM APOCALYPSE", target:"ARMS & FOREARMS", exercises:[
    { id:"d5_1", name:"Close Grip Bench Press", sets:"5×8", type:"HEAVY" },
    { id:"d5_2", name:"EZ-Bar Skull Crushers", sets:"5×10", type:"VOLUME" },
    { id:"d5_3", name:"Rope Tricep Pushdown", sets:"5×15", type:"VOLUME" },
    { id:"d5_4", name:"Overhead Cable Extension", sets:"4×15", type:"VOLUME" },
    { id:"d5_5", name:"Standing Barbell Curl", sets:"5×10", type:"HEAVY" },
    { id:"d5_6", name:"Incline Dumbbell Curl", sets:"5×12", type:"VOLUME" },
    { id:"d5_7", name:"Preacher Curl Machine", sets:"5×12", type:"VOLUME" },
    { id:"d5_8", name:"Alternating Hammer Curl", sets:"4×15", type:"VOLUME" },
    { id:"d5_9", name:"Barbell Curl 21s", sets:"3 Sets", type:"FINISHER" },
    { id:"d5_10", name:"Rope Pushdown Challenge", sets:"100 Reps", type:"FINISHER" },
    { id:"d5_11", name:"Seated Barbell Wrist Curl", sets:"4×20", type:"VOLUME" },
    { id:"d5_12", name:"Reverse Wrist Curl", sets:"4×20", type:"VOLUME" },
    { id:"d5_13", name:"Hanging Leg Raise", sets:"5×15", type:"ABS" },
  ]},
  { title:"HAMSTRING & GLUTE HELL", target:"POSTERIOR CHAIN", exercises:[
    { id:"d6_1", name:"Romanian Deadlift (RDL)", sets:"6×8", type:"HEAVY" },
    { id:"d6_2", name:"Lying Leg Curl", sets:"5×15", type:"VOLUME" },
    { id:"d6_3", name:"Seated Leg Curl", sets:"5×15", type:"VOLUME" },
    { id:"d6_4", name:"Smith Machine Split Squat", sets:"4×15", type:"VOLUME" },
    { id:"d6_5", name:"Barbell Hip Thrust", sets:"5×12", type:"HEAVY" },
    { id:"d6_6", name:"Leg Curl Dropset", sets:"4 Dropsets", type:"FINISHER" },
    { id:"d6_7", name:"Seated Calf Raise", sets:"6×20", type:"HEAVY" },
    { id:"d6_8", name:"Decline Crunch", sets:"5×20", type:"ABS" },
    { id:"d6_9", name:"Prone Plank Challenge", sets:"3×90s", type:"ABS" },
  ]},
];

// ============================================================
// STATE & STORAGE
// ============================================================
const STORAGE_KEY = 'brutal_pro_v3';

function loadState() {
  try {
    const raw = localStorage.getItem(STORAGE_KEY);
    if (!raw) return null;
    return JSON.parse(raw);
  } catch { return null; }
}
function saveState() {
  try { localStorage.setItem(STORAGE_KEY, JSON.stringify(state)); } catch {}
}

function makeDefaultState() {
  return {
    appTitle: 'BRUTAL PROTOCOL',
    appSubtitle: 'Mutilation System',
    theme: 'brutal',
    customColors: { accent: '#cc1500', bg: '#050000', text: '#f0ddd0' },
    activePerson: 0,
    people: [
      {
        id: 'p0',
        name: 'Atharv',
        days: JSON.parse(JSON.stringify(DEFAULT_DAYS)),
        log: {}
      }
    ]
  };
}

let state = loadState() || makeDefaultState();
// migrate old data if needed
if (!state.people) {
  state = makeDefaultState();
  saveState();
}

let activeDay = 0;
let currentExId = null;
let currentIncrement = '2.5';
let renameTarget = null; // {type:'app'|'day', dayIdx?}
let workoutModalMode = 'day'; // 'day' or 'replace'

// ============================================================
// THEME
// ============================================================
function applyTheme(name) {
  document.body.className = name === 'brutal' ? '' : 'theme-' + name;
  state.theme = name;
  saveState();
  updateThemeCards();
  // reset custom colors display
  if (name !== 'custom') {
    document.getElementById('customAccent').value = '#cc1500';
    document.getElementById('customBg').value = '#050000';
    document.getElementById('customText').value = '#f0ddd0';
  }
}
function applyCustomTheme() {
  const accent = document.getElementById('customAccent').value;
  const bg = document.getElementById('customBg').value;
  const text = document.getElementById('customText').value;
  state.customColors = { accent, bg, text };
  state.theme = 'custom';
  document.body.className = '';
  const r = document.documentElement;
  r.style.setProperty('--accent', accent);
  r.style.setProperty('--accent-bright', accent);
  r.style.setProperty('--bg', bg);
  r.style.setProperty('--text', text);
  r.style.setProperty('--red', accent);
  r.style.setProperty('--red-bright', accent);
  r.style.setProperty('--btn-save-bg', accent);
  r.style.setProperty('--tab-active-bg', accent);
  r.style.setProperty('--progress-color', accent);
  r.style.setProperty('--logged-border', accent + '88');
  r.style.setProperty('--header-glow', accent + 'aa');
  r.style.setProperty('--ex-left-bar-heavy', accent);
  r.style.setProperty('--ex-left-bar-volume', accent + 'bb');
  r.style.setProperty('--ex-left-bar-finisher', accent);
  r.style.setProperty('--ex-left-bar-abs', accent + '99');
  r.style.setProperty('--badge-heavy-color', accent);
  r.style.setProperty('--badge-volume-color', accent + 'cc');
  r.style.setProperty('--badge-finisher-color', accent);
  r.style.setProperty('--badge-abs-color', accent + 'aa');
  saveState();
  updateThemeCards();
}
function updateThemeCards() {
  ['brutal','midnight','forest','gold'].forEach(t => {
    const el = document.getElementById('tc-' + t);
    if (el) el.classList.toggle('active', state.theme === t);
  });
}
function restoreTheme() {
  if (state.theme === 'custom') {
    document.getElementById('customAccent').value = state.customColors?.accent || '#cc1500';
    document.getElementById('customBg').value = state.customColors?.bg || '#050000';
    document.getElementById('customText').value = state.customColors?.text || '#f0ddd0';
    applyCustomTheme();
  } else {
    applyTheme(state.theme || 'brutal');
  }
}

// ============================================================
// PEOPLE
// ============================================================
function currentPerson() { return state.people[state.activePerson] || state.people[0]; }
function currentDays() { return currentPerson().days || []; }
function currentLog() { return currentPerson().log || {}; }

function renderPersonTabs() {
  const container = document.getElementById('personTabs');
  container.innerHTML = state.people.map((p, i) => `
    <button class="person-tab ${i === state.activePerson ? 'active' : ''}" onclick="switchPerson(${i})">
      <span class="pt-dot"></span>${p.name}
    </button>
  `).join('');
}
function switchPerson(i) {
  state.activePerson = i;
  activeDay = 0;
  saveState();
  renderAll();
}

function openAddPersonModal() {
  closeDropdowns();
  closeModal('peopleModal');
  document.getElementById('addPersonTitle').textContent = 'ADD PERSON';
  document.getElementById('newPersonName').value = '';
  document.getElementById('newPersonPlan').value = 'default';
  openModal('addPersonModal');
}

function saveNewPerson() {
  const name = document.getElementById('newPersonName').value.trim();
  if (!name) { showToast('Enter a name!'); return; }
  const planChoice = document.getElementById('newPersonPlan').value;
  let days;
  if (planChoice === 'empty') days = [];
  else if (planChoice === 'copy') days = JSON.parse(JSON.stringify(currentDays()));
  else days = JSON.parse(JSON.stringify(DEFAULT_DAYS));

  // re-id exercises
  days.forEach((d, di) => {
    d.exercises.forEach((ex, ei) => {
      ex.id = `p${state.people.length}_d${di}_e${ei}_${Date.now()}`;
    });
  });

  const newPerson = { id: 'p' + Date.now(), name, days, log: {} };
  state.people.push(newPerson);
  state.activePerson = state.people.length - 1;
  activeDay = 0;
  saveState();
  closeModal('addPersonModal');
  renderAll();
  showToast(name + ' added!');
}

function openPeopleModal() {
  closeDropdowns();
  renderPeopleList();
  openModal('peopleModal');
}

function renderPeopleList() {
  const list = document.getElementById('peopleList');
  if (!state.people.length) {
    list.innerHTML = '<div class="empty-state"><div class="es-icon">👤</div><div class="es-title">No People Yet</div></div>';
    return;
  }
  list.innerHTML = state.people.map((p, i) => `
    <div class="person-item">
      <div>
        <div class="pi-name">${p.name}</div>
        <div class="pi-plan">${p.days?.length || 0} days · ${Object.keys(p.log||{}).length} exercises logged</div>
      </div>
      <div class="person-item-btns">
        <button class="pi-btn" onclick="renamePerson(${i})">✏️</button>
        ${state.people.length > 1 ? `<button class="pi-btn danger" onclick="deletePerson(${i})">🗑️</button>` : ''}
      </div>
    </div>
  `).join('');
}

function renamePerson(i) {
  const name = prompt('New name for ' + state.people[i].name + ':', state.people[i].name);
  if (name && name.trim()) {
    state.people[i].name = name.trim();
    saveState();
    renderPeopleList();
    renderPersonTabs();
    showToast('Renamed!');
  }
}

function deletePerson(i) {
  if (state.people.length <= 1) { showToast("Can't delete last person!"); return; }
  if (!confirm('Delete ' + state.people[i].name + ' and all their data?')) return;
  state.people.splice(i, 1);
  if (state.activePerson >= state.people.length) state.activePerson = state.people.length - 1;
  activeDay = 0;
  saveState();
  closeModal('peopleModal');
  renderAll();
  showToast('Deleted!');
}

// ============================================================
// RENAME
// ============================================================
function openRenameApp() {
  closeDropdowns();
  renameTarget = { type: 'app' };
  document.getElementById('renameModalTitle').textContent = 'RENAME APP';
  document.getElementById('renameLabel').textContent = 'App Title';
  document.getElementById('renameInput').value = state.appTitle;
  document.getElementById('renameSubField').style.display = 'flex';
  document.getElementById('renameSubInput').value = state.appSubtitle || '';
  openModal('renameModal');
}
function openRenameDay() {
  closeDropdowns();
  const day = currentDays()[activeDay];
  if (!day) return;
  renameTarget = { type: 'day', dayIdx: activeDay };
  document.getElementById('renameModalTitle').textContent = 'RENAME DAY ' + (activeDay + 1);
  document.getElementById('renameLabel').textContent = 'Day Title';
  document.getElementById('renameInput').value = day.title;
  document.getElementById('renameSubField').style.display = 'flex';
  document.getElementById('renameSubInput').value = day.target || '';
  openModal('renameModal');
}
function saveRename() {
  const val = document.getElementById('renameInput').value.trim().toUpperCase();
  const sub = document.getElementById('renameSubInput').value.trim().toUpperCase();
  if (!val) { showToast('Enter a name!'); return; }
  if (renameTarget.type === 'app') {
    state.appTitle = val;
    state.appSubtitle = sub;
    document.getElementById('appTitle').textContent = val;
    document.getElementById('appSubtitle').textContent = sub || 'Tap title to rename';
  } else if (renameTarget.type === 'day') {
    currentDays()[renameTarget.dayIdx].title = val;
    currentDays()[renameTarget.dayIdx].target = sub;
  }
  saveState();
  closeModal('renameModal');
  renderDay();
  showToast('Renamed!');
}

// ============================================================
// WORKOUT PLAN BUILDER
// ============================================================
function openAddWorkoutModal(mode) {
  closeDropdowns();
  workoutModalMode = mode;
  document.getElementById('workoutModalTitle').textContent = mode === 'replace' ? 'REPLACE WORKOUT' : 'ADD NEW DAY';
  document.getElementById('addModeSelect').value = 'single';
  // If replacing, force single mode
  if (mode === 'replace') {
    document.getElementById('addModeSelect').value = 'single';
    document.getElementById('addModeSelect').parentElement.style.display = 'none';
  } else {
    document.getElementById('addModeSelect').parentElement.style.display = 'flex';
  }
  renderWorkoutPlanBuilder();
  openModal('workoutModal');
}

function renderWorkoutPlanBuilder() {
  const mode = document.getElementById('addModeSelect').value;
  const container = document.getElementById('planBuilder');
  if (mode === 'all') {
    // 6 day blocks
    let html = '';
    const titles = ['CHEST DAY','BACK DAY','LEG DAY','SHOULDER DAY','ARM DAY','LEG DAY 2'];
    for (let d = 0; d < 6; d++) {
      html += buildDayBlock(d, titles[d]);
    }
    container.innerHTML = html + `<button class="add-day-btn" onclick="addPlanDay()">+ ADD ANOTHER DAY</button>`;
  } else {
    container.innerHTML = buildDayBlock(0, 'NEW DAY') + `<button class="add-day-btn" onclick="addPlanDay()">+ ADD ANOTHER DAY</button>`;
  }
}

let planDayCount = 1;
function addPlanDay() {
  planDayCount++;
  const container = document.getElementById('planBuilder');
  const addBtn = container.querySelector('.add-day-btn');
  const newBlock = document.createElement('div');
  newBlock.innerHTML = buildDayBlock(planDayCount - 1, 'DAY ' + planDayCount);
  container.insertBefore(newBlock.firstElementChild, addBtn);
}

function buildDayBlock(idx, defaultTitle) {
  return `
    <div class="plan-day-block" id="planDay_${idx}">
      <div class="plan-day-header">
        DAY ${idx + 1}:
        <input type="text" id="planTitle_${idx}" placeholder="${defaultTitle}" value="${defaultTitle}">
      </div>
      <div class="field" style="margin-bottom:8px">
        <label>Target Muscles</label>
        <input type="text" id="planTarget_${idx}" placeholder="e.g. CHEST & TRICEPS">
      </div>
      <div id="planExList_${idx}"></div>
      <button class="add-ex-btn" onclick="addPlanEx(${idx})">+ ADD EXERCISE</button>
    </div>
  `;
}

let planExCounts = {};
function addPlanEx(dayIdx) {
  if (!planExCounts[dayIdx]) planExCounts[dayIdx] = 0;
  planExCounts[dayIdx]++;
  const ei = planExCounts[dayIdx];
  const list = document.getElementById('planExList_' + dayIdx);
  const row = document.createElement('div');
  row.className = 'ex-row';
  row.id = `planEx_${dayIdx}_${ei}`;
  row.innerHTML = `
    <input type="text" placeholder="Exercise name" id="peName_${dayIdx}_${ei}">
    <input type="text" class="sets-input" placeholder="Sets" id="peSets_${dayIdx}_${ei}">
    <select id="peType_${dayIdx}_${ei}">
      <option value="VOLUME">VOLUME</option>
      <option value="HEAVY">HEAVY</option>
      <option value="FINISHER">FINISHER</option>
      <option value="ABS">ABS</option>
    </select>
    <button class="remove-ex-btn" onclick="this.closest('.ex-row').remove()">✕</button>
  `;
  list.appendChild(row);
}

function savePlan() {
  const mode = document.getElementById('addModeSelect').value;
  const container = document.getElementById('planBuilder');
  const dayBlocks = container.querySelectorAll('.plan-day-block');
  const newDays = [];

  dayBlocks.forEach((block, di) => {
    const title = (block.querySelector(`[id^="planTitle_"]`)?.value || 'NEW DAY').toUpperCase();
    const target = (block.querySelector(`[id^="planTarget_"]`)?.value || '').toUpperCase();
    const exRows = block.querySelectorAll('.ex-row');
    const exercises = [];
    exRows.forEach((row, ei) => {
      const nameInput = row.querySelector('input[placeholder="Exercise name"]');
      const setsInput = row.querySelector('input[placeholder="Sets"]');
      const typeSelect = row.querySelector('select');
      const name = nameInput?.value.trim();
      if (!name) return;
      exercises.push({
        id: `p${state.activePerson}_d${Date.now()}_e${ei}`,
        name, sets: setsInput?.value || '3×10', type: typeSelect?.value || 'VOLUME'
      });
    });
    if (title) newDays.push({ title, target, exercises });
  });

  if (!newDays.length) { showToast('Add at least one day!'); return; }

  const person = currentPerson();
  if (workoutModalMode === 'replace') {
    person.days[activeDay] = newDays[0];
  } else if (mode === 'all') {
    person.days = newDays;
  } else {
    person.days.push(newDays[0]);
    activeDay = person.days.length - 1;
  }

  planExCounts = {};
  saveState();
  closeModal('workoutModal');
  renderAll();
  showToast('Plan saved!');
}

// ============================================================
// DAY ACTIONS
// ============================================================
function resetDayLog() {
  closeDropdowns();
  const day = currentDays()[activeDay];
  if (!day) return;
  if (!confirm('Reset all logs for ' + day.title + '?')) return;
  const log = currentPerson().log;
  day.exercises.forEach(ex => { delete log[ex.id]; });
  saveState();
  renderDay();
  showToast('Day log reset!');
}

function deleteDay() {
  closeDropdowns();
  const days = currentDays();
  if (days.length <= 1) { showToast("Can't delete last day!"); return; }
  if (!confirm('Delete ' + days[activeDay].title + '?')) return;
  days.splice(activeDay, 1);
  if (activeDay >= days.length) activeDay = days.length - 1;
  saveState();
  renderAll();
  showToast('Day deleted!');
}

// ============================================================
// LOG MODAL
// ============================================================
function openLogModal(exId) {
  let ex = null;
  for (const day of currentDays()) {
    ex = day.exercises.find(e => e.id === exId);
    if (ex) break;
  }
  if (!ex) return;
  currentExId = exId;
  const saved = currentLog()[exId] || {};
  currentIncrement = saved.nextIncrement || '2.5';
  document.getElementById('modalType').textContent = ex.type + ' · ' + ex.sets;
  document.getElementById('modalName').textContent = ex.name;
  document.getElementById('inputWeight').value = saved.weight || '';
  document.getElementById('inputPlates').value = saved.plates || '';
  document.getElementById('inputReps').value = saved.reps || '';
  document.getElementById('inputNotes').value = saved.notes || '';
  updateIncButtons();
  updateNextPreview();
  document.getElementById('btnClear').style.display = saved.weight ? 'block' : 'none';
  document.getElementById('inputWeight').addEventListener('input', updateNextPreview);
  openModal('logModal');
}

function saveEntry() {
  if (!currentExId) return;
  currentPerson().log[currentExId] = {
    weight: document.getElementById('inputWeight').value,
    plates: document.getElementById('inputPlates').value,
    reps: document.getElementById('inputReps').value,
    notes: document.getElementById('inputNotes').value,
    nextIncrement: currentIncrement,
    savedAt: new Date().toLocaleDateString('en-IN'),
  };
  saveState();
  closeModal('logModal');
  renderDay();
  showToast('Logged!');
}

function clearEntry() {
  if (!currentExId) return;
  delete currentPerson().log[currentExId];
  saveState();
  closeModal('logModal');
  renderDay();
  showToast('Cleared!');
}

function setIncrement(val) {
  currentIncrement = val;
  updateIncButtons();
  updateNextPreview();
}
function updateIncButtons() {
  document.querySelectorAll('.inc-btn').forEach(btn => {
    btn.classList.toggle('active', btn.dataset.val === currentIncrement);
  });
}
function updateNextPreview() {
  const w = parseFloat(document.getElementById('inputWeight').value);
  const inc = parseFloat(currentIncrement);
  const preview = document.getElementById('nextPreview');
  if (!isNaN(w) && w > 0 && !isNaN(inc) && inc > 0) {
    preview.textContent = `Next week target: ${(w + inc).toFixed(1)} kg`;
  } else {
    preview.textContent = '';
  }
}

// ============================================================
// RENDER
// ============================================================
function renderAll() {
  document.getElementById('appTitle').textContent = state.appTitle;
  document.getElementById('appSubtitle').textContent = state.appSubtitle || 'Tap title to rename';
  renderPersonTabs();
  renderTabs();
  renderDay();
}

function renderTabs() {
  const days = currentDays();
  const log = currentLog();
  const container = document.getElementById('dayTabs');
  if (!days.length) { container.innerHTML = ''; return; }
  container.innerHTML = days.map((d, i) => {
    const logged = d.exercises.filter(e => log[e.id]).length;
    const allDone = d.exercises.length > 0 && logged === d.exercises.length;
    return `<button class="day-tab ${i === activeDay ? 'active' : ''}" onclick="switchDay(${i})">
      DAY ${i + 1}${allDone ? ' <span class="dt-done">✓</span>' : ''}
    </button>`;
  }).join('');
}

function renderDay() {
  const days = currentDays();
  const log = currentLog();
  if (!days.length) {
    document.getElementById('dayTitle').textContent = 'NO WORKOUT';
    document.getElementById('dayTarget').textContent = 'Add a plan using ⋮ menu';
    document.getElementById('exerciseList').innerHTML = `
      <div class="empty-state">
        <div class="es-icon">📋</div>
        <div class="es-title">NO PLAN YET</div>
        <div>Tap the ⋮ button to add a workout plan</div>
      </div>`;
    document.getElementById('progressCount').textContent = '0 / 0';
    document.getElementById('progressBarFill').style.width = '0%';
    return;
  }
  if (activeDay >= days.length) activeDay = 0;
  const day = days[activeDay];
  document.getElementById('dayTitle').textContent = '☠ ' + day.title;
  document.getElementById('dayTarget').textContent = 'TARGET: ' + day.target;

  const list = document.getElementById('exerciseList');
  list.innerHTML = day.exercises.map(ex => {
    const saved = log[ex.id];
    const isLogged = !!saved;
    let nextW = null;
    if (saved?.weight) {
      const curr = parseFloat(saved.weight);
      const inc = parseFloat(saved.nextIncrement || '2.5');
      if (!isNaN(curr) && !isNaN(inc) && inc > 0) nextW = (curr + inc).toFixed(1);
    }
    let savedHtml = '';
    if (saved) {
      let parts = [];
      if (saved.weight) parts.push(`⚡ ${saved.weight} kg`);
      if (saved.plates) parts.push(`🏋️ ${saved.plates}`);
      if (saved.reps) parts.push(`× ${saved.reps} reps`);
      if (nextW) parts.push(`<span class="next-target">→ next: ${nextW} kg</span>`);
      if (saved.savedAt) parts.push(`<span style="color:#443322;font-size:9px">${saved.savedAt}</span>`);
      savedHtml = `<div class="ex-saved">${parts.join(' · ')}</div>`;
    }
    return `
      <button class="ex-btn ${isLogged ? 'logged' : ''}" data-type="${ex.type}" onclick="openLogModal('${ex.id}')">
        <div class="ex-left">
          <div class="ex-meta">
            <span class="type-badge ${ex.type}">${ex.type}</span>
            <span class="ex-name">${ex.name}</span>
          </div>
          ${savedHtml}
        </div>
        <div class="ex-right">
          <div class="ex-sets">${ex.sets}</div>
          ${isLogged ? '<div class="ex-check">✓</div>' : '<div class="ex-tap">TAP TO LOG</div>'}
        </div>
      </button>`;
  }).join('');

  const logged = day.exercises.filter(e => log[e.id]).length;
  const total = day.exercises.length;
  const pct = total ? Math.round((logged / total) * 100) : 0;
  document.getElementById('progressCount').textContent = `${logged} / ${total} LOGGED (${pct}%)`;
  document.getElementById('progressBarFill').style.width = pct + '%';
}

function switchDay(i) {
  activeDay = i;
  renderTabs();
  renderDay();
}

// ============================================================
// DROPDOWN / MODAL HELPERS
// ============================================================
function toggleDropdown(id) {
  const el = document.getElementById(id);
  const isOpen = el.classList.contains('open');
  closeDropdowns();
  if (!isOpen) el.classList.add('open');
}
function closeDropdowns() {
  document.querySelectorAll('.dropdown-menu.open').forEach(el => el.classList.remove('open'));
}
function openModal(id) {
  document.getElementById(id).classList.add('open');
}
function closeModal(id) {
  document.getElementById(id).classList.remove('open');
  if (id === 'logModal') {
    document.getElementById('inputWeight').removeEventListener('input', updateNextPreview);
    currentExId = null;
  }
}

document.addEventListener('click', (e) => {
  if (!e.target.closest('.dropdown-wrap')) closeDropdowns();
  if (e.target.classList.contains('modal-overlay')) closeModal(e.target.id);
});

// ============================================================
// EXPORT / IMPORT
// ============================================================
function exportData() {
  closeDropdowns();
  const data = { ...state, exportedAt: new Date().toISOString(), version: 3 };
  const blob = new Blob([JSON.stringify(data, null, 2)], { type: 'application/json' });
  const url = URL.createObjectURL(blob);
  const a = document.createElement('a');
  a.href = url;
  a.download = 'brutal-protocol-backup.json';
  a.click();
  URL.revokeObjectURL(url);
  showToast('Exported!');
}
function importData() {
  closeDropdowns();
  document.getElementById('importFileInput').click();
}
function handleImport(e) {
  const file = e.target.files[0];
  if (!file) return;
  const reader = new FileReader();
  reader.onload = (ev) => {
    try {
      const imported = JSON.parse(ev.target.result);
      if (!imported.people) { showToast('Invalid file!'); return; }
      if (!confirm('This will replace ALL data. Continue?')) return;
      Object.assign(state, imported);
      saveState();
      renderAll();
      restoreTheme();
      showToast('Imported!');
    } catch { showToast('Import failed!'); }
  };
  reader.readAsText(file);
  e.target.value = '';
}

// ============================================================
// TOAST
// ============================================================
let toastTimer;
function showToast(msg) {
  const t = document.getElementById('toast');
  t.textContent = msg;
  t.classList.add('show');
  clearTimeout(toastTimer);
  toastTimer = setTimeout(() => t.classList.remove('show'), 2000);
}

// ============================================================
// INIT
// ============================================================
restoreTheme();
renderAll();
</script>
</body>
</html>
