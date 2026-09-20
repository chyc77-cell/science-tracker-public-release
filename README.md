# ScienceTracker 🎓

**ScienceTracker** is a lightweight Windows system tray application designed for researchers, academics, and students to automatically monitor citation counts, h-index, and publication statistics across **Scopus**, **Google Scholar**, and **OpenAlex**.

---

## 🌟 Features & Quick Start Guide

### 1. Launching the App
Run `ScienceTracker.exe`. The application starts silently and minimizes to your **Windows System Tray** (bottom-right corner near the clock). Look for the **"h"** icon.

### 2. Configuration (First-Time Setup)
1. Right-click the tray icon and select **Settings** (Налаштування).
2. Check the boxes for the platforms you wish to track.
3. Enter your respective Author IDs:
   * **Scopus Author ID:** The numeric ID found in your Scopus profile URL (e.g., `57190408747`).
   * **Google Scholar ID:** The 12-character string in your profile URL after `user=` (e.g., `pjlFdXwAAAAJ`).
   * **OpenAlex ID or ORCID:** Your OpenAlex ID (e.g., `A5023788391`) or full ORCID (e.g., `0000-0002-1835-0097`).
4. Select your preferred **Interface Language** (English / Ukrainian).
5. Click **Save**.

### 3. Viewing Metrics
* **Tray Tooltip:** Hover over the tray icon at any time to see a quick summary of your total citations.
* **Detailed View:** Click the tray icon or right-click and choose **View statistics** to see detailed metrics (citations, h-index, publication count, last update timestamp).

---

## ⚠️ Parsing Limitations & Technical Notes

Automated web data extraction comes with platform-specific constraints:

1. **Google Scholar (High Anti-Bot Strictness):** Google Scholar actively detects automated traffic. Querying Scholar too frequently may lead to temporary IP blocks or CAPTCHA challenges.
2. **Scopus (Dynamic Rendering):** Requires Google Chrome or Microsoft Edge installed on your PC. Uses background Selenium automation to accurately parse dynamic metrics.
3. **OpenAlex (Official REST API):** Fast, reliable, and completely free from IP rate-limiting issues.

---

## ⏱️ Recommended Update Intervals

Academic metrics update over days or weeks, so frequent checks are counterproductive:

| Interval | Risk Level | Recommendation |
| :--- | :---: | :--- |
| **12 – 24 Hours** | 🟢 **Safe** | **Recommended.** Ensures reliable updates without triggering Scholar rate limits. |
| **6 – 12 Hours** | 🟡 **Moderate** | Acceptable for active monitoring with low risk. |
| **0.1 – 2 Hours** | 🔴 **High Risk** | Not recommended. Likely to cause temporary Google Scholar IP blocks. |

> **Pro Tip:** Set the update interval to **12 hours** and enable *"Run at Windows Startup"*. The app will unobtrusively check your metrics twice daily and notify you only when changes are detected.

---

## 💳 Pricing & License

* **Trial Period:** 7-day fully functional trial.
* **Lifetime License:** **$4.99 USD** (One-time purchase, lifetime access, free automatic software updates).

---

## 📞 Support & Contact

If you have questions, feedback, or need technical assistance with ScienceTracker:
* **Email Support:** [rovalit@ukr.net](mailto:rovalit@ukr.net) 
* **GitHub Issues:** You can also open an issue directly in this repository.

---

## ⚖️ Privacy Policy & Terms of Service

* **Privacy Policy:** ScienceTracker processes public academic data available on Google Scholar, Scopus, and OpenAlex. We do not store, collect, or share personal user telemetry, credentials, or private information. All metrics history is stored locally on your device.
* **Terms of Service:** ScienceTracker is provided "as is". License purchases and refunds are processed according to Paddle's buyer protection policy.

---
*&copy; 2026 ScienceTracker. All rights reserved. Order processing and billing by Paddle.com.*
