---
title: "GitHub Dork Generator Tool"
date: 2025-07-01 12:00:00 +0530
categories: [Tool, GitHub Dorking, OSINT]
tags: [github, dork, recon, bug bounty, osint]
pin: true
comments: true
---

> Use this tool to generate GitHub dorking queries to find sensitive information for ethical bug bounty and OSINT purposes.

---

<style>
input {
  overflow: hidden;
  color: #FFF;
  background: #222;
  border-radius: 5px;
  border: 1px solid #ccc;
  font-family: Arial, sans-serif;
  font-size: 16px;
  font-weight: 700;
  height: 32px;
  padding: 4px 16px;
  margin-bottom: 10px;
  width: 80%;
}
.dork-buttons a {
  display: inline-block;
  background: #444;
  color: #fff;
  padding: 6px 12px;
  margin: 3px;
  text-decoration: none;
  border-radius: 5px;
  font-size: 14px;
}
.dork-buttons a:hover {
  background: #ff5722;
}
</style>

<div align="center">
  <h2>GitHub Dork Generator</h2>
  <p>Enter a target like <code>org:example</code> or <code>site:example.com</code></p>
  <input id="target" name="target" placeholder='"site" or org:target' autofocus type="text"><br/>
</div>

<div class="dork-buttons" align="center">
  <a href="#" onclick="openDork('api_key')">api_key</a>
  <a href="#" onclick="openDork('aws_access_key_id')">aws_access_key_id</a>
  <a href="#" onclick="openDork('DB_PASSWORD')">DB_PASSWORD</a>
  <a href="#" onclick="openDork('filename:.env')">.env</a>
  <a href="#" onclick="openDork('filename:config.php dbpasswd')">config.php dbpasswd</a>
  <a href="#" onclick="openDork('filename:id_rsa')">id_rsa</a>
  <a href="#" onclick="openDork('filename:wp-config.php')">wp-config.php</a>
  <a href="#" onclick="openDork('token')">token</a>
</div>

<script>
function openDork(keyword) {
  const site = document.getElementById('target').value;
  const url = 'https://github.com/search?q=' + encodeURIComponent(site + ' ' + keyword);
  window.open(url, '_blank');
}
</script>

---

### 📌 Disclaimer
This tool is intended strictly for **educational purposes** and **ethical cybersecurity research**. Always follow legal guidelines and the rules of engagement when performing bug bounty or OSINT tasks.

Tool by **Faizee Asad**
