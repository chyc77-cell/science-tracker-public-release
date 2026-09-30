# ScienceTracker 🎓

**ScienceTracker is a free Windows citation and h-index tracker for researchers.** It monitors publications, citation counts, h-index values, and profile changes across **Google Scholar, Scopus, OpenAlex, and ORCID**.

ScienceTracker can run quietly in the **Windows system tray**, check academic metrics automatically, and notify you when citations, publication counts, h-index values, or tracked publication data change. It also includes research analytics, citation trends, journal quartiles, publication-type analysis, and tools for identifying publications closest to increasing your h-index.

## What is ScienceTracker?

ScienceTracker is a free Windows desktop application for researchers, academics, and students who want to monitor their academic profiles and bibliometric metrics in one place.

Instead of repeatedly checking Google Scholar, Scopus, OpenAlex, and ORCID manually, ScienceTracker can monitor supported profiles in the background and keep source-specific metrics available from one interface.

### Supported academic services

- **Google Scholar** — publication, citation, and h-index monitoring from a public Scholar profile.
- **Scopus** — author metrics and publication records using supported API access or browser-based retrieval.
- **OpenAlex** — open bibliographic data, author metrics, and publication-level analytics.
- **ORCID** — researcher identification and publication-record comparison.
- **Crossref & SCImago** — supporting metadata, publication matching, and journal-quartile information where applicable.

## Track citations and h-index

ScienceTracker can help you:

- monitor total citation counts;
- monitor h-index values;
- monitor publication totals;
- detect changes in tracked publication data;
- review citation trends over time;
- identify publications closest to increasing your h-index;
- compare metrics from different academic sources without mixing incompatible citation counts.

Because Google Scholar, Scopus, and OpenAlex have different coverage, ScienceTracker keeps their metrics separate.

## Google Scholar monitoring

ScienceTracker can monitor a researcher's public Google Scholar profile for publication totals, citation counts, and h-index changes.

Google Scholar actively detects automated traffic, so very frequent checks may result in temporary rate limits or CAPTCHA challenges. Longer update intervals are recommended for continuous monitoring.

## Scopus metrics

ScienceTracker supports three practical Scopus access modes:

- **Without the Scopus API** — browser-based retrieval from the public Scopus author profile. No API key is required, but publication-level data and analytics are more limited.
- **With a personal Scopus API key** — provides richer publication data and analytics where the user's Scopus API access permits it.
- **With an API key + Institutional Token** — may enable broader remote Scopus API access where supported by Elsevier and the user's institution.

In short: **browser mode works without an API but provides more limited data; API mode provides richer data but may depend on institutional access; API + Institutional Token can enable remote API access where available.**

## OpenAlex analytics

ScienceTracker uses the official OpenAlex REST API for author metrics, publication records, citation information, and supporting analytics.

OpenAlex can also act as a useful open bibliographic source when comparing coverage with Google Scholar and Scopus.

## Citation notifications

When ScienceTracker detects a change in monitored academic metrics, it can:

- display a Windows notification;
- visually mark the tray icon;
- show recent changes in the statistics window;
- optionally send a Telegram notification.

This can include changes in citation counts, publication totals, h-index values, and tracked publication-level data.

## Researcher metrics dashboard

The statistics and analytics views provide access to:

- citations;
- h-index;
- publication counts;
- recent metric changes;
- citation trends by year;
- publication distribution by type;
- citation-threshold analysis;
- journal quartiles where available;
- publications closest to increasing the h-index;
- formatted bibliographic records with clickable DOI links;
- Word export for analytics and h-index reports.

---

## 🌟 Features & Quick Start Guide

### 1. Launching the App

To install ScienceTracker, download and run `ScienceTracker_Setup.exe`, follow the on-screen setup wizard prompts, and click Finish to complete the installation.

To launch ScienceTracker, open it from the Start Menu or Desktop shortcut. The application starts silently and minimizes to your **Windows System Tray** (bottom-right corner near the clock). Look for the **"h"** icon.

### 2. Configuration (First-Time Setup)

1. Right-click the tray icon and select **Settings** (Налаштування).
2. Check the boxes for the platforms you wish to track.
3. Enter your respective Author IDs:
   - **Scopus Author ID:** The numeric ID found in your Scopus profile URL.
   - **Google Scholar ID:** The identifier in your profile URL after `user=`.
   - **OpenAlex ID or ORCID:** Your OpenAlex author ID or full ORCID.
4. For Scopus, choose whether to use the **Scopus API** or the browser-based fallback. If API mode is enabled, enter your API key and, optionally, an Institutional Token.
5. Set the automatic check interval and enable **Run at Windows Startup** if desired.
6. Optionally connect **Telegram notifications** from the same Settings window.
7. Select your preferred **Interface Language** (English / Ukrainian).
8. Click **Save**.

### 3. Viewing Metrics & Notifications

- **Tray Tooltip:** Hover over the tray icon to see a quick summary of monitored citation metrics.
- **Detailed View:** Click the tray icon or right-click and choose **View statistics** to see citations, h-index, publication count, last update timestamp, recent changes, and publication-level details.
- **Change Notifications:** When ScienceTracker detects a change in citations, publication count, h-index, or publication-level data, it can display a Windows notification and mark the tray icon.
- **Telegram Notifications:** Telegram can be connected from **Settings**. When enabled, detected metric changes can be delivered to Telegram as well as shown in Windows.
- **Analytics:** Open **Analytics** to explore citation trends by year, publication distribution by type, citation-threshold shares, journal quartiles where available, and publications closest to increasing your h-index.
- **Bibliographic Output:** Analytics includes formatted publication records with clickable DOI links and supports export to Word.

---

## 📈 Research Analytics

ScienceTracker is not only a monitoring tool. It also helps researchers interpret their bibliometric profile and publication performance.

Current analytics features include:

- **Citations by year** for supported data sources.
- **h-index history by year** where reliable historical data are available.
- **Publication distribution by type**, including journal articles, conference/abstract publications, books, and other records.
- **Citation-threshold analysis**, showing the share of publications with 0, ≥1, ≥5, and ≥10 citations.
- **Journal quartiles** using SCImago SJR Best Quartile data for journal publications where a reliable match is available.
- **Publications closest to the next h-index**, with full bibliographic formatting and clickable DOI links.
- **Local metadata caching** to speed up repeated analytics runs.
- **Word export** for analytics and detailed h-index reports.

---

## Typical use cases

ScienceTracker may be useful if you want to:

- see your publication count, citations, and h-index without repeatedly opening several academic websites;
- monitor Google Scholar citations automatically;
- monitor Scopus author metrics;
- compare Google Scholar, Scopus, and OpenAlex coverage;
- receive a notification when your citation count or h-index changes;
- keep a local history of academic metrics;
- review which publications are closest to increasing your h-index;
- generate bibliometric reports from your publication data.

---

## Frequently Asked Questions

### How can I track my h-index automatically?

ScienceTracker can periodically monitor h-index values from supported academic sources and notify you when a monitored value changes.

### Is there a free app for monitoring Google Scholar citations?

Yes. ScienceTracker is free to use and can monitor publication totals, citation counts, and h-index values from a researcher's public Google Scholar profile.

### Can I monitor Google Scholar, Scopus, and OpenAlex together?

Yes. ScienceTracker supports Google Scholar, Scopus, and OpenAlex in one Windows application. It keeps metrics from each source separate because the databases have different publication and citation coverage.

### Can ScienceTracker notify me when my citation count changes?

Yes. ScienceTracker can display Windows notifications when monitored citation counts, publication totals, h-index values, or tracked publication data change. Optional Telegram notifications are also available.

### Can I use ScienceTracker without a Scopus API key?

Yes. ScienceTracker can use browser-based retrieval for the public Scopus author profile. This mode provides more limited publication data than full API access.

### Does ScienceTracker run in the background?

Yes. ScienceTracker can run in the Windows system tray and periodically check selected academic profiles.

### Is ScienceTracker free?

Yes. ScienceTracker is free to use.

### Does ScienceTracker combine citation counts from different databases?

No. Google Scholar, Scopus, and OpenAlex index different sets of publications and citations, so ScienceTracker keeps source-specific metrics separate.

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
> - **Supported:** Windows 10 and Windows 11 (64-bit).
> - **Not supported:** Windows 7, 8, 8.1, or any 32-bit (x86) versions of Windows.
>
> Since the `.exe` file is built using PyInstaller and does not have a paid Code Signing Certificate, Windows SmartScreen may display a warning on the first launch: *"Windows protected your PC"* (*"Unknown Publisher"*).
>
> **To run the app:** Click **More info** → **Run anyway**.

---

## 📞 Support & Contact

ScienceTracker is independently developed and maintained by a single developer. Direct support is provided on a **best-effort basis** alongside the developer's primary professional work, so response times may vary.

For the fastest assistance:

1. **Check this README and the troubleshooting notes first.**
2. **Ask an AI assistant such as ChatGPT.** Providing the exact ScienceTracker error message, a screenshot, or a clear description of the problem can often help diagnose the issue.
3. **Contact the developer if the issue remains unresolved or appears to be specific to ScienceTracker itself.**

When using an AI assistant, do **not** share API keys, Institutional Tokens, passwords, or other private credentials.

- **Email Support:** [chyc77@gmail.com](mailto:chyc77@gmail.com)
- **GitHub Issues:** You can also open an issue directly in this repository.

---

## ⚖️ Privacy Policy & Terms of Service

- **Privacy Policy:** ScienceTracker processes public academic data and metadata available through Google Scholar, Scopus, OpenAlex, Crossref, and SCImago where applicable. The application does not intentionally collect or sell personal user telemetry, passwords, or academic-service credentials. Metrics history and analytics data are stored locally on the user's device. If Telegram notifications are enabled, the ScienceTracker notification service stores the minimum connection information required to associate the installation with the connected Telegram account and deliver notifications.
- **Terms of Service:** ScienceTracker is independently developed and distributed under the ScienceTracker brand and is provided "as is". Third-party academic services and APIs are controlled by their respective providers, and users are responsible for complying with those providers' terms and access requirements.

---

*&copy; 2026 ScienceTracker. All rights reserved.*
