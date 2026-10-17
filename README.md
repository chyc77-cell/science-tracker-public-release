# ScienceTracker 🎓

**ScienceTracker is a free Windows desktop application for monitoring Scopus and Google Scholar metrics and organizing a researcher's public ORCID works.** It tracks citations, h-index values, publication totals, and relevant changes from the Windows system tray. Its separate **Statistics**, **Reports**, and **Scopus Coverage** tools help researchers review and export publication data.

[⬇️ **Download ScienceTracker for Windows — latest GitHub release**](https://github.com/chyc77-cell/science-tracker-public-release/releases/latest)

**Free · Windows 10/11 (64-bit) · English and Ukrainian · Local history and caches · Optional Telegram notifications**

> **Installation security:** The GitHub installer may be unsigned and trigger Windows SmartScreen's *Unknown Publisher* warning. Download only from the official repository, verify the source of the file, and proceed only if you trust it.

## Academic sources: what you actually see

| Source | Visible in the application | What ScienceTracker uses it for |
| --- | --- | --- |
| **Scopus** | Dashboard, Statistics, Reports | Publication count, citations, h-index, publication records, journal quartiles, citation analyses, and estimated self-citations |
| **Google Scholar** | Dashboard, Statistics, Reports | Publication count, citations, h-index, publication list, and citation trends |
| **ORCID** | Dashboard, Statistics, Reports | Public works, their publication years and original ORCID work types; no citation counts or h-index |
| **OpenAlex** | **Background only — no separate metrics panel** | Bibliographic matching, selected DOI/open-access checks, and the data underlying estimated Scopus self-citations |
| **SCImago and Crossref** | Supporting sources, not selectable research profiles | Journal quartiles and cached bibliographic details where relevant |

**OpenAlex has not been removed from the underlying workflows.** Enter an **ORCID iD** in Settings; ScienceTracker uses it to identify public ORCID works and to resolve the corresponding OpenAlex author in background procedures. OpenAlex citation counts and h-index are **not displayed as a separate profile**. Data in ORCID and OpenAlex can differ; ScienceTracker does not treat them as interchangeable publication lists.

## Getting started

1. Download the latest installer from [GitHub Releases](https://github.com/chyc77-cell/science-tracker-public-release/releases/latest). If distributed as a ZIP, extract it and run `ScienceTracker_Setup.exe`.
2. Launch ScienceTracker from the Start menu or desktop shortcut. Its icon is available in the **Windows notification area (system tray)**; check hidden icons if necessary.
3. Open **Settings** and configure the profiles you want to use:
   - **Scopus Author ID:** numeric author identifier; also enter a **Scopus API key** from [Elsevier's developer portal](https://dev.elsevier.com/). An Institutional Token is optional and useful only when provided by your institution.
   - **Google Scholar Author ID:** the `user=` parameter of your public Google Scholar profile URL.
   - **ORCID iD:** your full identifier, for example `0000-0002-1835-0097` (including the check digit).
4. Set the checking interval (**minimum: one hour**), interface language, and optional Windows startup or Telegram notifications, then click **Save**.
5. Open the main window to view the three source blocks. Use **Statistics** for a selected source and year range, **Reports** for Word documents, or **Scopus Coverage** to compare records.

**Required fields depend on the feature.** Scopus monitoring requires a valid Scopus Author ID and an API key with adequate Elsevier access. Public Google Scholar monitoring can operate independently. ORCID public-work statistics require an ORCID iD. For the most complete **Scopus statistics and cross-database analyses**, configure Scopus Author ID, Scopus API key, and ORCID iD. The settings reminder disappears when the required identifiers have valid local formats and the key field is non-empty; this **does not validate API authorization or guarantee data availability**.

## Dashboard and automatic monitoring

- **Scopus:** publications, citations, h-index, progress towards the next h-index, estimated self-citations, and Scopus Coverage.
- **Google Scholar:** publications, citations, h-index, and progress towards the next h-index.
- **ORCID:** total **public works** and counts grouped into **Articles / Abstracts (conference outputs) / Books / Other**. It does **not** display citations, h-index, or an h-index progress bar.
- **Recent updates:** shows tracked changes where applicable. The tray icon can indicate unread changes and Windows notifications can announce relevant updates.
- **Telegram (optional):** connect from Settings and test delivery. The same notification event should normally not be repeated across connected PCs when the compatible backend is in use; **local histories are not synchronized**.

The ORCID **Abstracts** bucket is a convenient interface label for **conference-related ORCID types**, including conference papers, abstracts, posters, proceedings, and presentations. It does not mean that every item is strictly a short abstract. The original ORCID `publication_type` is retained. Public ORCID records may be incomplete, duplicated, or not assigned a publication year; ScienceTracker deduplicates identifiable works when building its list.

## Profile Statistics

Choose a profile and a publication-year range in **Statistics**. The window includes a scrollable list of publications and source-appropriate charts. Publication and h-index-nearest lists have their own scrollbars.

### Scopus

- Publication list with available citation counts, document types, **DOI links**, **open-access indicators**, and journal quartiles.
- Publications closest to the next h-index when sufficient citation data exist.
- Publications and citations chart; h-index history where available; publication distribution by quartile and by exact citation count.
- Open Access summary for the selected set of publications.
- **Scopus Citation Overview:** when permitted by Elsevier, citations received in each calendar year can be shown. Otherwise the fallback groups **current citation totals by the publication year of the cited works**. These are different measures; the program labels the fallback.

### Google Scholar

- Publication list with citation counts and DOI links where already available. **When no DOI is available, a direct link to the Google Scholar citation record is shown where the profile provides its publication identifier.**
- Publications closest to the next h-index and available publication/citation distributions.
- **No SCImago quartile assignment or automatic article-versus-other classification.** These earlier Scholar procedures were discontinued to reduce complexity and background load.

### ORCID

- Public works from the ORCID record, grouped by their **native ORCID work type**.
- **Histogram of publications by year** and **chart of the four work-type groups**.
- No citations, h-index, self-citation percentage, or SCImago quartiles: **ORCID does not supply these metrics**.
- Works without a publication year are omitted from the yearly histogram, not assigned to an invented year.

Statistics can be **copied**, **opened as HTML in a browser**, and **exported to Word (.docx)**. Source-specific graphics are included in the supported HTML/Word statistics exports.

## SCImago journal quartiles — Scopus only

ScienceTracker matches journal information (preferably **ISSN**, then journal title where appropriate) against SCImago data **for the publication year**. If a journal has quartiles in several subject categories, the algorithm selects the **most frequent quartile**; in a tie it selects the **worse quartile** (for example, Q3 instead of Q2). This is a category-based selection rule, **not necessarily SCImago's “SJR Best Quartile”**. If category-specific quartiles are absent from the source record, ScienceTracker can fall back to the catalog's Best Quartile field; this fallback cannot establish whether subject categories disagree.

- **`Q2*`** means the journal had **different quartiles across subject categories in that year**; the value relevant to your particular work **requires manual verification**. The explanatory footnote appears after the publication list and in supported exports.
- **`No quartile`** can mean the journal/year could not be reliably matched or the item is outside the journal-article category; it does not assess article quality.
- On a clean installation, the first calculation may take time because ScienceTracker needs **annual SCImago journal-ranking catalogs**. Later checks reuse local caches. The calculation runs in the background; time depends on the publication years involved, connectivity, and upstream response.

**Please verify quartiles manually before using them in an official assessment or application.** Subject-specific rules imposed by your institution may differ.

## Scopus Coverage and estimated self-citations

**Scopus Coverage** has separate **Google Scholar** and **ORCID** comparison tabs. It attempts to match their publication records to Scopus and presents potential matches, gaps, and cases requiring review. Identifiers, titles, publication years, and available DOI metadata are used where appropriate. The tool **does not edit Scopus or ORCID** or guarantee that an unmatched work belongs in Scopus.

**Estimated Scopus self-citations** are calculated from matched **OpenAlex works and citing/cited relationships**. They are **not official Scopus self-citation counts**. Quality depends on matched-work coverage and author identity resolution. The estimate is cached, and the app avoids re-running it unnecessarily when inputs have not changed. This analysis can require separate OpenAlex requests; it is different from the **local-only** DOI/open-access refinement below.

**Scopus DOI and Open Access refinement:** for records with incomplete or potentially conflicting metadata, ScienceTracker can reuse **already downloaded OpenAlex data** and a **local Crossref cache**. This refinement itself does **not** add API requests and does not silently replace the original Scopus DOI. If no trustworthy matching record is available locally, the program does not invent a DOI or OA status. Open Access classification can vary between sources; verify important cases against the publisher.

## Reports — Word output

The **Reports** window offers:

1. **Research Activity Report:** publications, available source-specific metrics and local history for a chosen period; ORCID uses works and types, **without fake citations or h-index**.
2. **Selected Research Outputs:** five or ten publication records with editable placeholders for significance, contribution, and relevance. Citation-based ordering applies to Scopus/Scholar when present; ORCID items are not ranked by citations.
3. **Research Impact Snapshot:** a compact summary of Scopus/Scholar metrics, ORCID public-work count, and researcher identifiers.

OpenAlex is **not a selectable report source**. In addition, the **Statistics** window offers its own detailed Word export, including available graphs.

## National System of Researchers of Ukraine (optional)

Settings includes an optional **application number** for the National System of Researchers of Ukraine. Where public ranking information can be retrieved, the app offers a separate ranking view. This number is **not required** for Scopus, Scholar, ORCID or regular reporting.

## Notifications, updates and multiple computers

- Automatic checks can be configured at **one-hour intervals or longer**. Google Scholar's automated-access protections and API rate limits may cause occasional failed refreshes; a failed update is **not** a metric value of zero.
- Windows notifications, tray indicators and Telegram notifications are separate channels. For Telegram, sign in to your account in a browser or the desktop app, select **Connect Telegram**, open the link, and start the bot. If you did not complete the connection, you can try the button again.
- Each PC retains its **own local statistics history**. Telegram alert deduplication across computers is not a full synchronization or backup system.
- GitHub releases can be checked through the app's update mechanism; an unsigned installer may trigger SmartScreen. Older machine-wide installations under `Program Files` may require **one-time administrator authorization** when transitioning to the newer per-user installation method.

## Troubleshooting

| Symptom | What to check |
| --- | --- |
| No Scopus data / authorization error | Verify Author ID, API key, permitted Elsevier API endpoints, institutional/network access, or Institutional Token (if supplied). A valid-looking key does not guarantee the API entitlements required for every function. |
| Google Scholar refresh fails | Check that the profile is public; possible CAPTCHA, rate limiting or site changes. Try a longer interval. |
| ORCID statistics initially unavailable | Confirm the ORCID iD and allow the public works request to finish; the first build can wait for the background fetch. Some works may be private or lack years/types. |
| SCImago takes a long time on first use | Annual catalogs are downloaded and matched by publication year. Later use benefits from the cache; see the diagnostic log for slow years. |
| Scopus annual-citation series unavailable | Citation Overview may be restricted. The chart's note explains when the publication-year fallback is used. |
| A paper is marked closed or has no DOI | Source metadata may be incomplete; the app's local matching is conservative and may not find a corresponding record. |
| Main window is missing | Look for ScienceTracker in the Windows notification area, including hidden tray icons. |
| Two installed versions appear | This can occur when a legacy machine-wide installation coexists with a per-user installation. Use the current migration-enabled installer; removing the old machine-wide version may require administrator privileges. Back up local data before any manual removal. |

The main local history and database cache are stored under `%LOCALAPPDATA%\ScienceTracker\`, including `stats_history.json` (and its backup) and `science_tracker_cache.sqlite3`. The background-update diagnostics are written to `update_diagnostics.log` in the same directory. **Back up this folder before manually deleting files or troubleshooting an installation.**

## Privacy, access and limitations

ScienceTracker stores publication metrics and supporting caches on your device. It sends requests to the selected academic services to retrieve public or authorized data, subject to each provider's access rules. An Elsevier key and institutional token, if supplied, should **not** be shared in bug reports. Optional Telegram integration exchanges the information required for account linking and alert delivery with the notification backend; it is not a cloud copy of your local metrics history.

The application does not intentionally sell user data or collect general-purpose user telemetry. Upstream APIs and websites are operated by their respective providers, and coverage, availability, licenses, and response formats may change. **ScienceTracker's estimates and derived classifications are not official decisions of Scopus, SCImago, ORCID, or OpenAlex.**

## Further reading, feedback and support

- [Help & FAQ](https://chyc77-cell.github.io/science-tracker-public-release/faq.html)
- [Latest GitHub release](https://github.com/chyc77-cell/science-tracker-public-release/releases/latest)
- [Report a bug or request a feature](https://github.com/chyc77-cell/science-tracker-public-release/issues)
- [ScienceTracker on Product Hunt](https://www.producthunt.com/products/sciencetracker?launch=sciencetracker)
- **Email:** [chyc77@gmail.com](mailto:chyc77@gmail.com)

ScienceTracker is independently maintained by a single developer; support is provided on a best-effort basis. When reporting a bug, include the app version, Windows version, a screenshot or error text, and reproduction steps. **Never post API keys, Institutional Tokens, Telegram connection tokens, or private profile information.**

© 2026 ScienceTracker. All rights reserved. Provided “as is”; users are responsible for compliance with third-party provider terms.
