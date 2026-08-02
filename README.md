<p align="center">
  <img src="https://raw.githubusercontent.com/shido275/DaMarketplace/refs/heads/main/Icons/seanime.png" alt="Seanime" width="140">
</p>

<h1 align="center">DaMarketplace</h1>

<p align="center">
  <strong>The Ultimate Seanime Extensions, Plugins & Providers Hub</strong>
</p>

<p align="center">
  Community-made and custom extensions for <a href="https://github.com/5rahim/seanime">Seanime</a>:
  anime streaming sources, manga sources, torrent providers, and UI plugins, all in one place.
</p>

<p align="center">
  <a href="https://shido275.github.io/DaMarketplace/"><img src="https://img.shields.io/website?url=https%3A%2F%2Fshido275.github.io%2FDaMarketplace%2F&label=Marketplace&color=2ea44f&style=for-the-badge" alt="Marketplace"></a>
  <a href="https://github.com/shido275/DaMarketplace/commits/main"><img src="https://img.shields.io/github/last-commit/shido275/DaMarketplace?style=for-the-badge&logo=git&logoColor=white&labelColor=2d3748&color=805ad5" alt="Last Commit"></a>
  <a href="https://discord.gg/vKPhNTesWx"><img src="https://img.shields.io/discord/1224767201551192224?style=for-the-badge&color=5865F2&labelColor=2d3748&label=Discord&logo=discord&logoColor=white" alt="Discord"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-Custom_Dual-805ad5?style=for-the-badge&labelColor=2d3748" alt="License"></a>
</p>

---

The easiest way to browse everything is the **[DaMarketplace Visual Site](https://shido275.github.io/DaMarketplace/)**. It shows every extension with its status (working / broken / deprecated), type, and language, and lets you copy install links directly.

Prefer raw JSON? The full database lives in [`Marketplace/Main.json`](https://raw.githubusercontent.com/shido275/DaMarketplace/refs/heads/main/Marketplace/Main.json).

---

## 🚀 How to Install DaMarketplace in Seanime

Connecting this database to your Seanime client is quick and easy:

1. Open **Seanime** and click on the **Extensions** (puzzle piece) icon in the left sidebar menu.  
   <br>
   <img src="https://raw.githubusercontent.com/shido275/DaMarketplace/main/images/step1.png" width="250" alt="Navigate to Extensions" />

2. At the top of the Extensions page, click on the **Marketplace** tab.  
   <br>
   <img src="https://raw.githubusercontent.com/shido275/DaMarketplace/main/images/step2.png" width="700" alt="Click on the Marketplace tab" />

3. On the right side of the screen, click the **Change repository** button.  
   <br>
   <img src="https://raw.githubusercontent.com/shido275/DaMarketplace/main/images/step3.png" width="700" alt="Change marketplace repository" />

4. Paste the **raw GitHub URL** of our JSON manifest into the "Marketplace URL" field and click **Save**.  
   *(Copy the link below:)*
   ```text
   https://raw.githubusercontent.com/shido275/DaMarketplace/refs/heads/main/Marketplace/Main.json
   ``` 
   <br>
   <img src="https://raw.githubusercontent.com/shido275/DaMarketplace/main/images/step4.png" width="500" alt="Paste repository URL and Save" />

> [!TIP]
> **Install the Marketplace Plus Plugin:**  
> Once you've added the repository, search the list and install the **Marketplace+** plugin! It upgrades your native Seanime extensions page with live status badges, sorting, star ratings, and support links directly inside the app.

---

## 🛠️ Adding Your Own Extensions

You can easily add your own extensions or plugins to this marketplace:

1. Open [`Marketplace/Main.json`](file:///home/maoriboishido/IDE%20Works/DaMarketplace/Marketplace/Main.json) in your editor.
2. Add a new entry to the JSON array following this schema:
   ```json
   {
     "id": "your-extension-id",
     "name": "Your Extension Name",
     "version": "1.0.0",
     "author": "YourName",
     "description": "Short description of what your extension does.",
     "type": "onlinestream-provider", 
     "language": "typescript",
     "lang": "en",
     "icon": "https://raw.githubusercontent.com/username/repo/main/icon.png",
     "manifestURI": "https://raw.githubusercontent.com/username/repo/refs/heads/main/manifest.json",
     "payloadURI": "https://raw.githubusercontent.com/username/repo/refs/heads/main/provider.ts",
     "website": "https://github.com/username/repo",
     "flags": "0/60",
     "flaggedBy": [],
     "permalink": "",
     "workingTag": true,
     "brokenTag": false,
     "deprecatedTag": false,
     "tags": ["1359183147123867881"],
     "scannedOnVersion": "3.10.2",
     "lastWorkingVersion": "3.10.2",
     "stars": 1,
     "addedAt": "2026-08-02T12:00:00.000Z",
     "updatedAt": "2026-08-02T12:00:00.000Z"
   }
   ```
   *Available `type` values:* `onlinestream-provider`, `manga-provider`, `anime-torrent-provider`, `plugin`, `torrent-provider`.

3. Re-run the pre-rendering script locally to update the website:
   ```bash
   node scripts/prerender.mjs
   ```
4. Commit and push your changes to GitHub. (If using GitHub Actions, it will automatically build and update `docs/index.html` for you).

---

## 📂 Project Structure

```text
DaMarketplace/
├── .github/workflows/  # Automated GitHub Actions
├── Marketplace/        # Extension manifest database (Main.json)
├── Plugin/             # Custom marketplace plugins (Marketplace-Plus)
├── Icons/              # Extension brand assets
├── docs/               # Visual marketplace site (served on GitHub Pages)
└── scripts/            # Pre-rendering compiler script
```

---

## 🤝 Credits & Acknowledgements

- **[5rahim](https://github.com/5rahim)** — Creator of the amazing **[Seanime](https://github.com/5rahim/seanime)** media manager.
- **[Bas1874](https://github.com/Bas1874)** — Original repository template creator.
- **[ASleepyDrink](https://github.com/ASleepyDrink)** — Visual marketplace inspiration and reference.
- **The Seanime Community** — For developing and maintaining these extensions.

---

## ⚖️ License

Code outside `/Marketplace` is licensed under the MIT License. See [LICENSE](LICENSE) for details.
