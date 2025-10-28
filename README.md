# 🌌 Clickjacking Multi-Target PoC Generator

> **Automated, visually striking Clickjacking vulnerability tester with night-sky aesthetics**  
> Crafted for security researchers, pentesters, and CTF players who value both function and form.

<img width="1280" height="709" alt="image" src="https://github.com/user-attachments/assets/17a8b11d-60a4-4ebb-a06c-ecd20448df93" />

*Example output: Multiple targets tested in a single, elegant interface*

---

## 🔍 What It Does

This tool helps you **quickly verify Clickjacking vulnerabilities** across **multiple web targets** by:

- Generating a **custom HTML PoC** that embeds your targets in iframes
- Serving it instantly via a **local HTTP server**
- Using a **dark cosmic theme** (`#0b0c2a`) to reduce eye strain during long testing sessions
- Supporting **bulk input** (comma- or space-separated URLs)

If a target loads inside the iframe → it’s **vulnerable** (missing `X-Frame-Options` or `Content-Security-Policy: frame-ancestors`).

---

## 🚀 Quick Start

### Prerequisites
- Python 3.6+

### Installation
```bash
git clone https://github.com/cybereagle2001/ClickJacking_Tool.git
cd ClickJacking_Tool
```

### Run
```bash
python3 clickjacking_POC.py
```

You’ll be prompted to enter one or more URLs:
```text
Enter one or more target URLs (separate by commas or spaces): 
> https://target1.com, https://target2.com, blog.talan.com
```

The script will:
1. Generate `clickjacking_poc.html`
2. Start a local server (e.g., `http://localhost:8000`)
3. Open the PoC in your default browser

✅ **No external dependencies** — pure Python standard library!

---

## 🌠 Features

| Feature | Description |
|--------|-------------|
| **Multi-Target Testing** | Test dozens of URLs in one go |
| **Night Sky UI** | Dark navy background (`#0b0c2a`) with soft glowing text |
| **Auto HTTPS** | Automatically prepends `https://` if missing |
| **Smart Port Selection** | Finds a free port if `8000` is busy |
| **Browser Auto-Open** | Instantly launches your PoC |
| **Clean Labels** | Each iframe shows its target URL clearly |
| **Zero Dependencies** | Uses only Python’s built-in modules |

---

## 🛡️ Ethical Use Reminder

> ⚠️ **Only test systems you own or have explicit written permission to assess.**  
> Unauthorized testing may violate laws like the CFAA or GDPR.

This tool is intended for:
- Authorized penetration tests
- Bug bounty programs
- Internal security validation
- Educational/CTF purposes

---

## 🧪 Sample Output

```html
<!-- Generated HTML includes -->
<body style="background-color: #0b0c2a; color: #e0f7ff;">
  <h2>Clickjacking Vulnerability Multi-Target PoC by Cybereagle2001</h2>
  <div>
    <h3>Target #1: https://vuln-app.com</h3>
    <iframe src="https://vuln-app.com" ...></iframe>
  </div>
  <div>
    <h3>Target #2: https://secure-app.com</h3>
    <iframe src="https://secure-app.com" ...></iframe> <!-- Likely blank if protected -->
  </div>
</body>
```

- ✅ **Vulnerable target**: Full page renders inside iframe  
- ❌ **Protected target**: Blank iframe or error (due to security headers)

---

## 🧑‍💻 Author

**Oussama Ben Hadj Dahman @cybereagle2001**  
*Junior Information Security Consultant @ TALAN*  
🔐 ISO 27001 | eJPT | CDFE | CPT | CC  
♟️ Chess player | 🕵️‍♂️ CTF Player / Author 
🎨 UX-conscious hacker

> 💡 **Pro Tip**: Pair this with browser dev tools (`Network` tab) to check for missing `X-Frame-Options` or weak CSP headers!  

**Happy hunting!** 🦅
