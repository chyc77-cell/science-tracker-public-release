# ScienceTracker 🎓

**ScienceTracker** is a Windows application for researchers, academics, and students that combines automated academic metrics monitoring with practical research analytics across **Scopus**, **Google Scholar**, and **OpenAlex**. It tracks citation counts, h-index, publication totals, and profile changes, provides Windows and optional Telegram notifications when monitored data change, and includes publication-level analytics, citation trends, journal quartiles, publication-type analysis, and progress toward the next h-index.

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
4. For Scopus, choose whether to use the **Scopus API** or the browser-based fallback. If API mode is enabled, enter your API key and, optionally, an Institutional Token.
5. Set the automatic check interval and enable **Run at Windows Startup** if desired.
6. Optionally connect **Telegram notifications** from the same Settings window.
7. Select your preferred **Interface Language** (English / Ukrainian).
8. Click **Save**.

### Scopus Access Modes

ScienceTracker supports three practical ways to work with Scopus:

* **Without the Scopus API** — ScienceTracker can monitor the public Scopus author profile using browser-based data retrieval. No API key is required, but the available publication data are more limited and some advanced analytics may be incomplete.
* **With a personal Scopus API key** — an API key can be obtained through the Elsevier Developer Portal. API mode provides more complete publication data and richer analytics. However, full Scopus API access is commonly restricted to the network of an institution with an active Scopus subscription.
* **With an API key + Institutional Token** — an Institutional Token may be provided by your institution or, in some cases, requested individually through Scopus/Elsevier support. When used together with the API key, it can enable access to the required Scopus API data from outside the institutional network.

In short: **browser mode works without an API but provides more limited data; API mode provides richer data but may be restricted to the institutional network; API + Institutional Token can enable remote API access.**

### 3. Viewing Metrics & Notifications
* **Tray Tooltip:** Hover over the tray icon at any time to see a quick summary of monitored citation metrics.
* **Detailed View:** Click the tray icon or right-click and choose **View statistics** to see citations, h-index, publication count, last update timestamp, recent changes, and publication-level details.
* **Change Notifications:** When ScienceTracker detects a change in citations, publication count, h-index, or publication-level data, it can display a Windows notification window and mark the tray icon accordingly.
* **Telegram Notifications:** Telegram can be connected from **Settings**. When enabled, detected metric changes can be delivered to Telegram as well as shown in Windows. Telegram is available during the fully functional trial and with an activated license.
* **Analytics:** Open **Analytics** to explore citation trends by year, publication distribution by type, citation-threshold shares, journal quartiles where available, and publications closest to increasing your h-index.
* **Bibliographic Output:** Analytics includes formatted publication records with clickable DOI links and supports export to Word.

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
2. **Scopus:** ScienceTracker can use either the official Scopus API or browser-based retrieval. Browser mode requires Google Chrome or Microsoft Edge and provides more limited publication data. API mode provides richer data, but access may depend on your institution's Scopus subscription and network authorization.
3. **OpenAlex (Official REST API):** Used for profile metrics and as a fallback metadata source where appropriate.
4. **Crossref & SCImago:** Used to enrich publication metadata, classify publication types, and determine journal quartiles where reliable matches are available. Supporting metadata are cached locally to improve performance.

---

## ⏱️ Recommended Update Intervals

ScienceTracker supports configurable automatic checks from **0.1 hours** upward, and the current default is **1 hour**. Academic profiles usually change much less frequently, and Google Scholar in particular may temporarily restrict automated requests when checked too often.

| Interval | Recommendation |
| :--- | :--- |
| **12 – 24 Hours** | Most conservative choice for Google Scholar and long-term background monitoring. |
| **6 – 12 Hours** | Good balance between responsiveness and low request frequency. |
| **1 – 6 Hours** | Suitable when faster monitoring is important, but repeated Google Scholar requests may increase the chance of temporary rate limiting. |
| **0.1 – 1 Hour** | Supported by the application, but not recommended for continuous Google Scholar monitoring. |

> **Tip:** If Google Scholar begins returning CAPTCHA or temporary access errors, increase the check interval. Scopus API and OpenAlex access are generally less dependent on browser-style anti-bot limits.


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

* **Trial Period:** 14-day fully functional trial, including Telegram notifications.
* **Launch Offer:** **$5 USD — 50% off the regular $10 lifetime price.**
* **License:** One-time purchase, lifetime access, and free software updates.
* **Device allowance:** One license key can be activated on up to **2 PCs simultaneously**.
* **Device changes:** A license can be deactivated on one computer and activated on another while keeping no more than two active installations at the same time.
* **Launch pricing:** Limited-time introductory pricing for early users.

---

## 📞 Support & Contact

ScienceTracker is independently developed and maintained by a single developer. Direct support is provided on a **best-effort basis** alongside the developer's primary professional work, so response times may vary.

For the fastest assistance, please use the following support path:

1. **Check this README and the troubleshooting notes first.** Many common issues related to Scopus access, Google Scholar rate limits, Windows SmartScreen, licensing, and notifications can be resolved from the documentation.
2. **Ask an AI assistant such as ChatGPT.** Providing the exact ScienceTracker error message, a screenshot, or a clear description of the problem can often lead to an immediate diagnosis or step-by-step solution.
3. **Contact the developer if the issue remains unresolved or appears to be specific to ScienceTracker itself.**

When using an AI assistant, do **not** share license keys, API keys, Institutional Tokens, passwords, payment information, or other private credentials.

* **Email Support:** [chyc77@gmail.com](mailto:chyc77@gmail.com)
* **GitHub Issues:** You can also open an issue directly in this repository.

---

## ⚖️ Privacy Policy & Terms of Service

* **Privacy Policy:** ScienceTracker processes public academic data and metadata available through Google Scholar, Scopus, OpenAlex, Crossref, and SCImago where applicable. The application does not intentionally collect or sell personal user telemetry, passwords, or academic-service credentials. Metrics history and analytics data are stored locally on the user's device. For licensing and order fulfillment, purchase-related information may be processed by Paddle.com and the ScienceTracker licensing service only as needed to create, validate, and support a software license. If Telegram notifications are enabled, the ScienceTracker notification service stores the minimum connection information required to associate the installation with the connected Telegram account and deliver notifications.
* **Terms of Service:** ScienceTracker is independently developed and distributed under the ScienceTracker brand by R. Nyvtyl and is provided "as is". A lifetime license key may be active on up to two supported computers simultaneously. License purchases and eligible refunds are processed by Paddle.com, our Merchant of Record, in accordance with applicable consumer protection requirements and Paddle's buyer-support and refund processes.

---
*&copy; 2026 ScienceTracker. All rights reserved. Order processing and billing by Paddle.com.*
