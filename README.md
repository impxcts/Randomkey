<div align="center">

# 🔐 Randomkey

**A password generator that runs entirely in your browser — nothing sent, nothing stored.**

Generates long, high-entropy passwords with no lazy patterns (no triple-repeated characters), built for the moment a site demands "a strong password" and you don't want to think about it.

![Platform](https://img.shields.io/badge/platform-Any%20Browser-0B1D33?logo=googlechrome&logoColor=white)
![Runtime](https://img.shields.io/badge/runtime-100%25%20Client--Side-C9A227)
![License](https://img.shields.io/badge/license-Free%20%26%20Open%20Source-6FBF8B)

</div>

---

## ✨ Overview

Open `randomkey.html`, get a password. That's the whole app.

Every character comes from the browser's cryptographically secure random number generator (`crypto.getRandomValues`) — not `Math.random()`, which is not safe for anything security-related. Nothing is logged, saved, or sent anywhere; there's no backend at all.

## 🧠 What makes the passwords "good"

- **Long enough to resist cracking, short enough for real forms.** Default length is 18 characters, adjustable from 10–32. Most sites cap password length somewhere between 20 and 128 characters, so this stays safely inside that range while still being long enough to be effectively uncrackable by brute force.
- **No triple-repeated characters.** Strings like `aaa` or `999` are rejected during generation — repetition like that quietly lowers real-world entropy and is one of the first patterns cracking tools check for.
- **Full character coverage.** Uppercase, lowercase, numbers, and symbols are all mixed in by default (each toggleable), and the generator guarantees at least one of each selected type appears.
- **Optional look-alike exclusion.** A toggle to drop visually ambiguous characters (`l`, `1`, `I`, `0`, `O`) for when you might need to type the password by hand.
- **Entropy meter, not a fake strength bar.** The gauge is calculated directly from character pool size and length (`log2(pool size) × length`), so it reflects actual randomness rather than a scoring gimmick.

## 📁 Project Structure

```
randomkey/
├── index.html    # The entire app — structure, styling, and logic
└── README.md
```

## 🚀 Usage

**Option 1 — just open it**
1. Download `index.html`.
2. Double-click it, or drag it into any browser.
3. Adjust length/character options if you want, then hit **Forge New** — the password is copied to your clipboard automatically. A **Copy** button is also there if you ever need to grab it again.

**Option 2 — host it**
Works as-is on GitHub Pages, Netlify, Vercel, or any static host — it's a single self-contained HTML file with no build step and no dependencies beyond two Google Fonts.

## ✅ Requirements

- Any modern browser (Chrome, Firefox, Edge, Safari)
- No install, no server, no internet connection required after the page loads

## 🛠 Notes

- Passwords are generated fresh in memory each time — closing or refreshing the page clears everything. Nothing persists except your light/dark mode preference, saved locally in your browser.
- A toggle in the top-right switches between light and dark mode. It defaults to your system preference on first visit and remembers your choice after that.
- The "no triple repeats" rule is always on; it's shown as a toggle for transparency but is intentionally locked, since disabling it doesn't add meaningful entropy.
- Every password is copied to the clipboard automatically the moment it's generated. Some browsers block clipboard writes that don't come from a direct click — if that happens on first load, just hit **Forge New** or **Copy** once and it'll work normally from then on.
- This tool generates passwords — it doesn't store or manage them. Pair it with a password manager to actually save what it gives you.

## 📄 License

Free and open source — use, modify, and share it however you'd like.

## ☕ Support

If this saved you some time, consider buying me a coffee:

[![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-FFDD00?logo=buymeacoffee&logoColor=black)](https://buymeacoffee.com/impxcts)

---

<div align="center">
<sub>Built for the "I just need a strong password right now" moment.</sub>
</div>
