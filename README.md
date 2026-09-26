<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>GENTRIX</title>
<style>
  :root{
    --bg1:#ffb6c1; --bg2:#ff8fab; --card:#ffffff; --text:#4a1e2b;
    --accent:#e63950; --yes:#ff4d6d; --no:#e5e5e5; --noText:#555;
    box-sizing:border-box;
    padding-top: env(safe-area-inset-top, 0px);
    padding-bottom: env(safe-area-inset-bottom, 0px);
  }
  @media (prefers-color-scheme: dark){
    :root:not([data-theme="light"]){
      --bg1:#3a1420; --bg2:#5a1a2e; --card:#2a1018; --text:#ffd9e0;
      --accent:#ff6b81; --yes:#ff4d6d; --no:#4a2a33; --noText:#e5c5cc;
    }
  }
  :root[data-theme="dark"]{
    --bg1:#3a1420; --bg2:#5a1a2e; --card:#2a1018; --text:#ffd9e0;
    --accent:#ff6b81; --yes:#ff4d6d; --no:#4a2a33; --noText:#e5c5cc;
  }
  html,body{height:100%;}
  body{
    margin:0;
    font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
    background: linear-gradient(135deg,var(--bg1),var(--bg2));
    display:flex; align-items:center; justify-content:center;
    min-height:100%;
    padding:24px;
    overflow-x:hidden;
    position:relative;
  }
  .heart{
    position:absolute; font-size:20px; opacity:0.5;
    animation: float 8s linear infinite;
    pointer-events:none;
  }
  @keyframes float{
    0%{ transform: translateY(0) rotate(0deg); opacity:0.6;}
    100%{ transform: translateY(-100vh) rotate(360deg); opacity:0;}
  }
  .card{
    background:var(--card);
    border-radius:24px;
    padding:36px 28px;
    max-width:420px;
    width:100%;
    text-align:center;
    box-shadow:0 20px 50px rgba(0,0,0,0.25);
    position:relative;
    z-index:1;
  }
  h1{
    color:var(--accent);
    font-size:2rem;
    letter-spacing:2px;
    margin:0 0 8px;
  }
  p.sub{
    color:var(--text);
    opacity:0.75;
    margin:0 0 28px;
    font-size:0.95rem;
  }
  .btn-row{
