# Privacy Policy for GPT System — by ShivAstra

*Last updated: October 16, 2026*  
*Maintained by: ShivAstra System (shivastarsystem.com)*

---

## 1. Overview & Privacy Commitment
**GPT System — by ShivAstra** is built with a strict **Privacy-First, Zero-Telemetry** architecture. We believe that your creative work, AI prompts, and ChatGPT conversations are entirely private to you.

- We do **NOT** operate any remote servers or databases that store your data.
- We do **NOT** track, collect, log, or sell any personal or browsing information.
- We do **NOT** include any analytics scripts, marketing trackers, or third-party advertising SDKs.
- **100% of the extension's execution and data storage happens locally on your computer.**

---

## 2. What Data We Process & How It Is Handled

### A. AI Prompts and Generation Queues
- **What is processed:** The prompt text, prefixes, suffixes, aspect ratios, and reference images you load into the Automator.
- **Where it is stored:** Exclusively inside your browser's local sandbox using `chrome.storage.local` and browser `IndexedDB`.
- **Transmission:** Prompts are sent solely between your local extension side panel and the official ChatGPT web interface (`https://chatgpt.com/`) running in your own active browser tab. No prompt data is ever transmitted to ShivAstra or any third party.

### B. Conversation Export Transcripts
- **What is processed:** When you click "Export Chat", the extension reads the conversation history visible within your active ChatGPT tab to compile your chosen export format (PDF, Markdown, JSON, or TXT).
- **Where it is stored:** The exported file is generated client-side using JavaScript (`jsPDF`) and saved directly to your local computer's Downloads folder via Chrome's downloads API. None of this transcript data is ever uploaded or retained outside your machine.

### C. Extension Settings & Custom Cheat Codes
- **What is processed:** User preferences (dark/light theme, custom download folder name, delay cooldown timing, custom cheat codes).
- **Where it is stored:** Saved locally in `chrome.storage.local`. It never leaves your browser.

---

## 3. Chrome Permissions & Why They Are Used
The extension requests only the minimum necessary permissions to function:

| Permission | Purpose |
| :--- | :--- |
| `sidePanel` | Displays the GPT System interface inside Chrome's native Side Panel alongside your ChatGPT tab. |
| `storage` | Stores your batch queues, custom prompt cheat codes, and preferences locally on your device. |
| `downloads` | Saves generated images and exported chat files (PDF/Markdown/JSON/TXT) to your Downloads folder. |
| `alarms` | Keeps the background service worker active during long multi-image batch runs. |
| `tabs` | Identifies the active ChatGPT tab ID to send automation commands and conversation export requests. |
| Host: `https://chatgpt.com/*` | Interacts with the ChatGPT input box, clicks generate/download, and reads messages for export. |
| Host: `https://*.oaiusercontent.com/*` | Downloads full-resolution generated image files from OpenAI's media CDN to your device. |

---

## 4. Third-Party Services
This extension interacts only with **ChatGPT (OpenAI)** as directed by the user in their active browser tab. We do not integrate with or send data to any advertising, analytics, or external data brokers.

---

## 5. User Control & Data Deletion
You have complete control over your data at all times:
- You can clear your queue, reset settings, or delete download history directly from the extension UI at any time.
- Uninstalling the extension automatically removes all associated `chrome.storage.local` and extension cache data from your computer.

---

## 6. Contact & Support
If you have any questions or feedback regarding this Privacy Policy, please contact:
- **Developer / Publisher:** ShivAstra System
- **Website:** [https://shivastarsystem.com](https://shivastarsystem.com)
- **Email:** info@shivastarsystem.com
