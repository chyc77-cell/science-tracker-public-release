# ScienceTracker 🎓

**ScienceTracker** is a Windows application for researchers, academics, and students that combines automated academic metrics monitoring with practical research analytics across **Scopus**, **Google Scholar**, and **OpenAlex**. It tracks citation counts, h-index, publication totals, and profile changes, while also providing publication-level analytics, citation trends, journal quartiles, publication-type analysis, and progress toward the next h-index.

---

## 🌟 Features & Quick Start Guide

### 1. Launching the App
To install ScienceTracker, download and run `ScienceTracker_Setup.exe`, follow the on-screen setup wizard prompts, and click Finish to complete the installation. To launch ScienceTracker, open it from the Start Menu or Desktop shortcut. The application starts silently and minimizes to your **Windows System Tray** (bottom-right corner near the clock). Look for the **"h"** icon.

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
* **Detailed View:** Click the tray icon or right-click and choose **View statistics** to see citations, h-index, publication count, last update timestamp, recent changes, and publication-level details.
* **Analytics:** Open **Analytics** to explore citation trends by year, publication distribution by type, citation-threshold shares, journal quartiles where available, and publications closest to increasing your h-index.
* **Bibliographic Output:** Analytics includes formatted publication records with DOI links and supports export to Word.

---


## 📈 Research Analytics

ScienceTracker is not only a monitoring tool. It also helps researchers interpret their bibliometric profile and publication performance.

Current analytics features include:

* **Citations by year** for supported data sources.
* **h-index history by year** where reliable historical data are available.
* **Publication distribution by type**, including journal articles, conference/abstract publications, books, and other records.
* **Citation-threshold analysis**, showing the share of publications with 0, ≥1, ≥5, and ≥10 citations.
* **Journal quartiles** using SCImago SJR Best Quartile data for journal publications where a reliable match is available.
* **Publications closest to the next h-index**, with full bibliographic formatting and clickable DOI links.
* **Local metadata caching** to speed up repeated analytics runs.
* **Word export** for analytics and detailed h-index reports.

---

## ⚠️ Parsing Limitations & Technical Notes

Automated web data extraction comes with platform-specific constraints:

1. **Google Scholar (High Anti-Bot Strictness):** Google Scholar actively detects automated traffic. Querying Scholar too frequently may lead to temporary IP blocks or CAPTCHA challenges.
2. **Scopus (Dynamic Rendering):** Requires Google Chrome or Microsoft Edge installed on your PC. Uses background Selenium automation to accurately parse dynamic metrics.
3. **OpenAlex (Official REST API):** Used for profile metrics and as a fallback metadata source where appropriate.
4. **Crossref & SCImago:** Used to enrich publication metadata, classify publication types, and determine journal quartiles where reliable matches are available. Supporting metadata are cached locally to improve performance.

---

## ⏱️ Recommended Update Intervals

Academic metrics update over days or weeks, so frequent checks are counterproductive:

| Interval | Risk Level | Recommendation |
| :--- | :---: | :--- |
| **12 – 24 Hours** | 🟢 **Safe** | **Recommended.** Ensures reliable updates without triggering Scholar rate limits. |
| **6 – 12 Hours** | 🟡 **Moderate** | Acceptable for active monitoring with low risk. |
| **0.1 – 2 Hours** | 🔴 **High Risk** | Not recommended. Likely to cause temporary Google Scholar IP blocks. |

> **Pro Tip:** Set the update interval to **12 hours** and enable *"Run at Windows Startup"*. The app will unobtrusively check your metrics twice daily and notify you only when changes are detected.


> [!CAUTION]
> **System Requirements & First-Launch Notice**
> * **Supported:** Windows 10 and Windows 11 (64-bit).
> * **Not supported:** Windows 7, 8, 8.1, or any 32-bit (x86) versions of Windows.
> 
> Since the `.exe` file is built using PyInstaller and does not have a paid Code Signing Certificate, Windows SmartScreen may display a warning on the first launch: *"Windows protected your PC"* (*"Unknown Publisher"*).
> 
> **To run the app:** Click **More info** &rarr; **Run anyway**.
---

## 💳 Pricing & License

* **Trial Period:** 7-day fully functional trial.
* **Launch Offer:** **$5 USD — 50% off the regular $10 lifetime price.**
* **License:** One-time purchase, lifetime access, and free software updates.
* **Launch pricing:** Limited-time introductory pricing for early users.

---

## 📞 Support & Contact

If you have questions, feedback, or need technical assistance with ScienceTracker:
* **Email Support:** [chyc77@gmail.com](mailto:chyc77@gmail.com) 
* **GitHub Issues:** You can also open an issue directly in this repository.

---

## ⚖️ Privacy Policy & Terms of Service

* **Privacy Policy:** ScienceTracker processes public academic data and metadata available through Google Scholar, Scopus, OpenAlex, Crossref, and SCImago where applicable. We do not store, collect, or share personal user telemetry, credentials, or private information. All metrics history is stored locally on your device.
* **Terms of Service:** ScienceTracker is provided "as is". License purchases and refunds are processed according to Paddle's buyer protection policy.

---
*&copy; 2026 ScienceTracker. All rights reserved. Order processing and billing by Paddle.com.*
