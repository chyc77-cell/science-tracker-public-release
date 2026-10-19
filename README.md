# ScienceTracker 🎓

**ScienceTracker** is a free Windows application for monitoring research metrics from **Scopus** and **Google Scholar** and viewing public **ORCID** works. It tracks publications, citations and h-index changes in the system tray, offers publication analytics, and exports reports to Word.

**Windows 10/11 (64-bit) · English and Ukrainian · Free · Optional Telegram notifications**

## Download and install

| Microsoft Store (recommended) | GitHub |
| --- | --- |
| [**Install from Microsoft Store ↗**](https://apps.microsoft.com/detail/9N6144Q9WSMT) | [**Download the installer ZIP ↓**](https://github.com/chyc77-cell/science-tracker-public-release/releases/latest/download/ScienceTracker_Setup.zip) |
| Installs directly from the Store; certified by Microsoft and updated through Microsoft Store. | Extract the ZIP and run `ScienceTracker_Setup.exe`; updates are delivered through GitHub Releases. |

Both editions are free and offer the same features. **They can be installed together**, but maintain separate settings and local statistics. Choose the installation and update method you prefer.

> **GitHub installer:** It may be unsigned, so Windows SmartScreen may display *Unknown Publisher*. Download only from the official release and proceed only if you trust the file.

## Getting started

1. Install ScienceTracker and open it from the Start menu. If the window is not visible, check the **Windows system tray** (including hidden icons).
2. Open **Settings** and enter the identifiers for the sources you want to monitor:
   - **Scopus:** numeric Author ID and an [Elsevier API key](https://dev.elsevier.com/). An Institutional Token is optional if your institution provides one.
   - **Google Scholar:** the value after `user=` in your public profile URL.
   - **ORCID:** your full ORCID iD.
3. Choose a check interval (**one hour or longer**), optionally enable Windows startup or Telegram notifications, and click **Save**.

You can use the sources independently. A Scopus API key is needed **only for Scopus features**, and access to some Scopus data depends on Elsevier's permissions. Adding an ORCID iD also helps with cross-source matching.

## Main features

- **Background monitoring:** publication totals, citations and h-index for Scopus and Google Scholar; Windows tray indicators and optional Telegram alerts when metrics change.
- **Statistics:** publication lists, DOI links where available, year-by-year charts, citation distributions and papers closest to increasing your h-index.
- **Scopus analysis:** SCImago journal quartiles, open-access information, estimated self-citations and **Scopus Coverage** comparisons with Google Scholar and ORCID.
- **ORCID:** publicly listed works by year and work type. ORCID does **not** provide citation counts or h-index.
- **Reports:** export statistics and charts to Word; create Research Activity Reports, Selected Research Outputs and Research Impact Snapshots.

**Other data sources:** OpenAlex supports background matching and estimated Scopus self-citations; SCImago and Crossref supply supporting journal and bibliographic information. They are not separate monitored profiles.

## Important notes on the results

- **SCImago quartiles** are derived from the publication year's journal data. When subject categories differ, `Q2*` (for example) flags the need for manual verification. Check quartiles before using them in formal assessments.
- **Scopus citation charts:** if the Citation Overview API is unavailable, a chart may show *current citations grouped by publication year*, not citations received during each calendar year. Year-by-year h-index charts derived from locally retained data are **not official historical Scopus h-index values**.
- **Estimated self-citations** use OpenAlex matching and are **not official Scopus self-citation counts**.
- The initial download of SCImago reference data may take some time. Google Scholar refreshes can occasionally fail because of access restrictions or rate limits.

## Updates, saved data and moving to another PC

Each edition updates through its **own channel**: Microsoft Store or GitHub Releases. The Store and GitHub editions, and installations on different computers, **do not synchronize local history**.

The main history file is `stats_history.json`:

- **GitHub:** `%LOCALAPPDATA%\ScienceTracker\stats_history.json`
- **Microsoft Store:** `%LOCALAPPDATA%\Packages\Chyc77.ScienceTracker_xzmsxqa4e66qw\LocalCache\Local\ScienceTracker\stats_history.json`

To transfer accumulated history, install the **same edition** on the new PC, close ScienceTracker on both computers, and copy `stats_history.json` to the corresponding path. Configure profiles and credentials separately. **Back up the file before replacing or deleting data.**

## Help and support

- [**Setup, troubleshooting and FAQ**](https://chyc77-cell.github.io/science-tracker-public-release/faq.html)
- [**GitHub Releases**](https://github.com/chyc77-cell/science-tracker-public-release/releases/latest)
- [**Report an issue**](https://github.com/chyc77-cell/science-tracker-public-release/issues) · [Email support](mailto:chyc77@gmail.com)

ScienceTracker stores its research-metric history and caches locally. Optional Telegram notifications use a separate service for account linking and alert delivery, **not cloud backup**. The application does not intentionally collect general-purpose user telemetry or sell user data. Do not include API keys, Institutional Tokens or private identifiers in bug reports. Third-party data availability and access remain subject to each provider's rules.

© 2026 ScienceTracker. Independent software, provided “as is”; not affiliated with or endorsed by the academic data providers named above.
