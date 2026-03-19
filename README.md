# 🎨 Alation Diagram Generator

A serverless, AI-powered single-page application (SPA) designed to help the Alation documentation team effortlessly generate, format, and export sequence diagrams. 

Built using the official `mermaid.js` rendering engine and Google's Gemini API, this tool automatically enforces the **2024 Alation Brand Guidelines** while fixing common AI syntax hallucinations.

---

## ✨ Key Features

* **AI-Powered Generation:** Convert text descriptions or screenshots of legacy architecture diagrams directly into Mermaid.js sequence code using the Gemini Vision API.
* **100% Brand Compliant:** Automatically applies the official Alation 2024 color palette, including exact 10% opacity background tints (Alation Orange, Neo Navy, Sun Yellow), Public Sans typography, and Neo Navy borders.
* **Auto-Sanitization Engine:** A built-in JavaScript parser intercepts the AI's raw output to fix known Mermaid bugs before rendering (e.g., stripping bad spaces from `rgb()`, converting dangerous `< >` angle brackets to `{ }`, and swapping squished self-looping arrows into readable `Note` blocks).
* **Direct GitHub Integration:** Commit `.mmd` source code and `.svg` files directly into your documentation repositories straight from the browser.
* **Zero Backend Required:** The entire application runs client-side in a single `index.html` file.

---

## 🔑 Prerequisites

To unlock the full power of the tool, users will need two free, personal keys:

1. **Google Gemini API Key (For AI Features)**
   * Go to [Google AI Studio](https://aistudio.google.com/).
   * Click **Get API Key** > **Create API Key**.
   * *Note: The key is used entirely locally in your browser and is never stored.*
2. **GitHub Personal Access Token (For direct repo pushing)**
   * Go to GitHub > **Settings** > **Developer Settings** > **Personal Access Tokens (Fine-grained)**.
   * Generate a token scoped to your specific documentation repository with **Read and Write access to Contents**.

---

## 🚀 How to Use the Tool

### Phase 1: AI Generation
1. Open `index.html` in any modern web browser.
2. In the **AI Diagram Assistant** panel, paste your **Gemini API Key**.
3. Either type a text description of the workflow OR upload a reference image/screenshot of an old diagram.
4. Click **✨ Generate Brand-Compliant Code**. The AI will write the code, apply the Alation color scheme, sanitize it, and auto-render the preview.

### Phase 2: Manual Tweaks (Optional)
* The generated Mermaid code appears in the middle text box.
* You can manually edit participant names, adjust steps, or add new `Note` blocks.
* Click **Render Diagram** to update the visual preview.

### Phase 3: Export & Save
Once the preview looks perfect, you have two options:
* **Download Locally:** Click **⬇️ Download SVG** to save the vector graphic to your machine, or **⬇️ Download .mmd** to save the raw code.
* **Push to GitHub:** Click **🐙 Push Code to GitHub Repo**. Enter your `org/repo` (e.g., `alation-devportal/docs`), the target file path, and your GitHub PAT. Click commit to push it live.

---

## 🖌️ Brand Formatting Rules Enforced

The auto-sanitizer ensures the following guidelines from the 2024 Alation Brand Book are always met:
* **Font:** Public Sans (falls back to Open Sans).
* **Signals/Arrows:** Web Accessible Alation Orange (`#E36624`).
* **Borders/Text:** Neo Navy (`#002E4B`).
* **Columns/Backgrounds:** Restricted to 10% opacity tints of the primary palette (`#FEF2E9` Orange, `#E6EAED` Navy, `#FFF6E5` Yellow) to ensure text contrast and readability.

---

## 📄 License

This project is licensed under the **GNU Affero General Public License v3.0 (AGPL-3.0)**. 
Permissions of this copyleft license are conditioned on making available complete source code of licensed works and modifications, which include larger works using a licensed work, under the same license.
