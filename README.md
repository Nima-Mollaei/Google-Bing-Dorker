# 🟢 Google/Bing Dorker

A modern, dark‑themed **Dorking tool** built with pure **HTML, CSS, and JavaScript**.

This project is designed for **security researchers, bug bounty hunters, penetration testers, and students** who want a clean and fast way to generate and run Google dorks against a target domain.

---

## ✨ Features

* 🔍 Live Google Dork generation
* 🌑 Dark hacker‑style UI with green accent
* ⚡ Instant update on input change
* 🧠 Carefully selected common reconnaissance dorks
* 🔗 One‑click open dorks in Google
* 🧩 Easily extensible (add your own dorks)
* 🚫 No frameworks, no dependencies

---

## 📸 Preview

![Color Spectrum Output](Bing.png)

---

## 🚀 Usage

1. Clone or download the repository

```bash
git clone https://github.com/yourusername/google-dorker.git
```

2. Open the file in your browser

```bash
cd Google_Bing-Dorker
open google_dorker.html
or
open bing_dorker.html
```

3. Enter a target domain (example: `example.com`)
4. Click any generated dork to open it directly in Google

---

## 🧠 How It Works

The tool dynamically builds Google search queries (dorks) using the domain you provide.

Example generated dork:

```text
site:example.com ext:log | ext:txt | ext:env
```

Each dork is converted into a clickable Google search URL:

```text
https://www.google.com/search?q=site:example.com+ext:log
```

---

## ➕ Adding Your Own Google Dorks

You can easily add your **custom dorks** by editing the JavaScript section.

### Step‑by‑step

1. Open `google_dorker.html` or `bing_dorker.html`
2. Scroll to the `<script>` section
3. Find the `dorks` array:

```js
const dorks = [
    'site:' + domain + ' inurl:&',
    'site:' + domain + ' ext:php | ext:aspx | ext:asp',
    // ...
];
```

4. Add your own dork as a new string

### Example: Adding SQL error pages

```js
'site:' + domain + ' "SQL syntax" | "mysql_fetch" | "ORA-"'
```

### Example: Exposed admin panels

```js
'site:' + domain + ' inurl:admin | inurl:login | inurl:dashboard'
```

✅ Save the file and refresh the page — your new dork will appear automatically.

---

## 📚 Dork Categories You Can Add

* 🔐 Authentication pages
* 🗄️ Backup & config files
* ☁️ Cloud credentials
* 🔄 Open redirects
* 📡 API endpoints
* 🧪 Debug & test pages
* 🧑‍💻 Dev / staging environments

---

## ⚠️ Disclaimer

This tool is intended for **educational and authorized security testing only**.

* Do **not** use it against systems you do not own or have permission to test
* The author is **not responsible** for misuse or illegal activities

Always follow responsible disclosure and local laws.


