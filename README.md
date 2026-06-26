# Privacy Policy — HomeIn Chrome Extension

**Last updated:** June 25, 2026  
**Developer:** Amogh Bantwal (individual developer)  
**Contact:** amoghbantwal@gmail.com

---

## Overview

HomeIn is a Chrome extension that adds map overlays to Zillow's home search — including commute isochrone zones, school attendance boundaries, points of interest, and FEMA natural disaster risk shading. This policy explains what data the extension handles, how it is used, and what is shared with third parties.

**The short version:** HomeIn has no backend server. No data you enter or generate while using this extension is ever transmitted to the developer. Everything is stored on your own device or passed to services you are already using (Zillow and FEMA's public API).

---

## 1. Data Stored on Your Device

HomeIn stores the following data locally in your browser using `chrome.storage.local`. This data never leaves your device to the developer.

### Persistent preferences (kept until you uninstall or clear extension storage)

| Data | Purpose |
|------|---------|
| Commute destinations (label, address, coordinates, travel mode, max commute time) | Populate your saved destination list in the side panel |
| Selected school zones (school name, display color) | Remember which schools you have pinned |
| School zone apply mode (union or intersect) | Remember your preferred filtering method |
| POI category preferences (which types are checked) | Remember which points of interest to show |
| Hazard filter settings (which hazard types are enabled, risk thresholds) | Remember your natural disaster filter preferences |
| Google Maps travel mode preference | Remember your preferred mode for route previews |

### Session data (automatically cleared 30 minutes after your last activity, or when you navigate to a different region)

| Data | Purpose |
|------|---------|
| Active commute zone polygon | Restore the commute overlay after a page reload without re-fetching |
| Active school zone boundaries | Restore school boundaries after a page reload |
| Active POI markers | Restore POI pins after a page reload |
| Active hazard tract polygons | Restore hazard shading after a page reload |
| Cached region polygon and WKT | Power hazard intersection and school zone filtering |
| GMaps origin and destination coordinates | Restore the Google Maps route preview after a page reload |
| POI and hazard visibility state | Remember if you hid overlays without removing them |
| Hidden school IDs | Remember which school boundaries you hid |

---

## 2. Data Passed to Third-Party Services

HomeIn does not transmit your data to any developer-controlled server. However, to function, the extension sends certain data to the following third-party services.

### Zillow (`www.zillow.com`)

When you use HomeIn on Zillow, the extension calls Zillow's own internal APIs using your existing Zillow browser session. The extension does not create a separate Zillow account or store your Zillow credentials. The following data is sent to Zillow:

- The visible map area (bounding box coordinates) — to fetch school data, commute isochrones, and region polygons
- A destination address and coordinates — when you request a commute zone
- A list of school zone polygons — when saving a school zone as a Zillow custom region
- A search query string — when using the commute destination autocomplete

These requests are identical to what Zillow's own interface sends. HomeIn is not sending additional personal information to Zillow beyond what Zillow already receives from your normal use of the site.

Zillow's privacy policy applies to these requests: [https://www.zillow.com/z/corp/privacy/](https://www.zillow.com/z/corp/privacy/)

### FEMA National Risk Index / Esri ArcGIS (`services.arcgis.com`)

When you use the Hazards feature, the extension's background service worker sends a geographic bounding box (the coordinates of the visible Zillow map area) to FEMA's publicly available National Risk Index API, hosted on ArcGIS Online. No personally identifiable information is included in this request. The API requires no authentication and is freely accessible to anyone.

Esri's privacy policy applies to this request: [https://www.esri.com/en-us/privacy/overview](https://www.esri.com/en-us/privacy/overview)

---

## 3. Data the Extension Reads

To function, HomeIn reads the following data from within your browser. This data is processed locally and is not transmitted to the developer.

- **Zillow page content** — The extension passively intercepts Zillow's own API responses (listing coordinates, region boundary polygons, school data) as they load in the page, to avoid making duplicate network requests. This data is held in memory and used only to power the extension's map overlays.
- **Current tab URL** — The extension reads the active tab's URL to determine whether you are on a Zillow home search page, and to extract the current map region from Zillow's `searchQueryState` URL parameter.

---

## 4. What the Extension Does Not Collect

- No names, email addresses, or any personally identifiable information
- No financial or payment information
- No authentication credentials (passwords, tokens, or cookies are never read or stored)
- No general browsing history or activity on non-Zillow sites
- No keystrokes, mouse movements, or scroll position
- No data is ever sent to a server controlled by the developer

---

## 5. Data Sharing

HomeIn does not sell, share, license, or transfer any user data to any third party. The only outbound network requests the extension makes are to Zillow and FEMA's ArcGIS API, as described in Section 2, for the sole purpose of delivering the extension's features to you.

---

## 6. Data Retention

- **Preferences** (commute destinations, school selections, POI and hazard settings) are retained in your browser's local storage until you uninstall the extension or manually clear its data via Chrome's extension settings.
- **Session data** (cached overlays, active region polygons) is automatically cleared 30 minutes after your last interaction, or immediately when you navigate to a different Zillow region.
- The developer retains no data whatsoever, as no data is transmitted to the developer.

---

## 7. Children's Privacy

HomeIn is not directed at children under the age of 13 and does not knowingly collect any information from children. The extension does not collect personal information from any user regardless of age.

---

## 8. Changes to This Policy

If this privacy policy changes materially, the "Last updated" date at the top of this page will be updated. Because the extension stores no data on a developer-controlled server, no user notification system exists — users are encouraged to review this page periodically. Any extension update that changes data practices will also be noted in the Chrome Web Store update description.

---

## 9. Contact

If you have questions or concerns about this privacy policy or the extension's data practices, please contact:

**Amogh Bantwal**  
amoghbantwal@gmail.com

---

## 10. Governing Law

This policy is governed by the laws of the United States. By using this extension, you agree to the terms of this privacy policy.
