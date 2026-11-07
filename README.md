# Aaqib Projects

A curated portfolio of software projects built by **Aaqibhafeezkhan**, showcasing practical engineering across backend services, frontend platforms, microfrontend architecture, progressive web apps, civic data, and mobile development.

The projects are presented as working codebases rather than isolated technology demos. Each entry links to its source repository and highlights the problem space, architecture, core capabilities, technology choices, and ways to explore the implementation.

**Focus areas:** Java and Spring Boot · React and TypeScript · Microfrontends · Progressive Web Apps · Mobile engineering · Data-driven applications · Developer tooling

<p align="center">
  <a href="https://github.com/Aaqibhafeezkhan">
    <img src="https://img.shields.io/badge/GitHub-Aaqibhafeezkhan-181717?style=for-the-badge&logo=github" alt="GitHub profile" />
  </a>
  <a href="https://github.com/AAQIB-LOCAL/Aaqib-OSS-Contributions">
    <img src="https://img.shields.io/badge/Explore-Open_Source_Contributions-2F6FEB?style=for-the-badge&logo=github&logoColor=white" alt="Open-source contributions" />
  </a>
</p>

## Portfolio at a glance

| Project | Area | Primary technologies | Engineering focus |
|---|---|---|---|
| [Books API](https://github.com/Aaqibhafeezkhan/Books-API) | Backend service | Java 17, Spring Boot 3, Caffeine, Docker | External API integration, filtering, pagination, caching and API documentation |
| [CMS Microfrontend Platform](https://github.com/Aaqibhafeezkhan/CMS-Microfrontend) | Frontend architecture | Angular, React, Svelte, Vue, single-spa, SystemJS | Runtime composition, independent modules, routing and shared session contracts |
| [DeenTime](https://github.com/Aaqibhafeezkhan/DeenTime) | Progressive Web App | JavaScript, PWA, Service Workers, PrayTimes.js | Timezone-aware calculations, offline behavior, accessibility and local-first storage |
| [DeHTML Studio](https://github.com/Aaqibhafeezkhan/DeHTML) | Developer tooling | React, Vite, JavaScript | Text and markup transformations, diffing and sandboxed previews |
| [Indian Parliament Explorer](https://github.com/Aaqibhafeezkhan/IndianParliamentInfographic) | Civic data application | JavaScript, JSON, browser storage, GitHub Pages | Data provenance, filtering, comparisons, analytics and CSV export |
| [Anti-Doomscroll Journal](https://github.com/Aaqibhafeezkhan/Anti-Doomscroll-SDK) | Mobile application | React Native, Zustand, SQLite, MMKV | Native screen-time capabilities, on-device journaling and usage insights |

## Featured projects

### 1. Books API

**A Spring Boot service for book discovery through the Open Library API.**

[Source repository](https://github.com/Aaqibhafeezkhan/Books-API)

Books API provides a focused REST interface over Open Library search. It supports general discovery and structured filtering, with pagination and in-process caching to avoid repeating identical upstream requests.

**Capabilities**
- Search books by title, author, subject or ISBN.
- Paginate search results with configurable page and size parameters.
- Cache responses with Caffeine using configurable TTL and maximum size.
- Explore the API through OpenAPI documentation and Swagger UI.
- Run the service locally or in a container using the supplied Dockerfile.

**Technology and design**
- Java 17 and Spring Boot 3.
- Open Library API integration.
- Caffeine in-process cache with configurable limits.
- OpenAPI 3 documentation.
- Multi-stage Docker build.

**Engineering focus:** REST API design, external-service integration, query filtering, pagination, caching strategy and containerized delivery.

**Explore:** [README and API examples](https://github.com/Aaqibhafeezkhan/Books-API#readme) · [Source code](https://github.com/Aaqibhafeezkhan/Books-API)

---

### 2. CMS Microfrontend Platform

**A multi-framework CMS composed from independently developed frontend applications.**

[Source repository](https://github.com/Aaqibhafeezkhan/CMS-Microfrontend)

The platform demonstrates how applications built with different frontend frameworks can coexist within one product. A single-spa shell coordinates application lifecycles and routes, while SystemJS and import maps resolve the modules at runtime.

**Architecture**

| Module | Framework | Responsibility |
|---|---|---|
| Root orchestration | TypeScript, single-spa | Shell, routing and runtime composition |
| Authentication | Angular 11 | Authentication experience and role contract |
| Editorial | React 17, TypeScript | Article creation, editing and publishing workflow |
| Collaboration | Svelte 3, TypeScript | Team collaboration and activity interface |
| Media | Vue 2.6, TypeScript | Media library and asset-management interface |

**Capabilities**
- Compose Angular, React, Svelte and Vue applications in one CMS experience.
- Register and mount applications through single-spa lifecycle functions.
- Resolve microfrontend bundles using SystemJS and import maps.
- Keep module builds and development servers independent.
- Demonstrate shared session state, protected routes and role-based permission contracts.
- Bundle independently built modules for the platform deployment setup.

**Technology and design**
- single-spa and single-spa-layout.
- SystemJS and import maps.
- Angular, React, Svelte and Vue.
- TypeScript, Webpack and framework-specific build tooling.

**Engineering focus:** Microfrontend boundaries, runtime module loading, framework interoperability, application lifecycle management, routing and cross-module contracts.

**Important scope note:** The repository documents a client-side demonstration architecture. Its browser-side session and authorization model should not be treated as production-grade server-side security.

**Explore:** [Architecture and setup guide](https://github.com/Aaqibhafeezkhan/CMS-Microfrontend#readme) · [Source code](https://github.com/Aaqibhafeezkhan/CMS-Microfrontend)

---

### 3. DeenTime

**A local-first Islamic PWA for prayer times and everyday worship utilities.**

[Source repository](https://github.com/Aaqibhafeezkhan/DeenTime) · [Live application](https://aaqibhafeezkhan.github.io/DeenTime/)

DeenTime brings prayer-time calculations and everyday Islamic utilities into an installable browser application. It runs without an account or application backend and keeps user settings and personal state in browser storage.

**Capabilities**
- Calculate prayer times using multiple methods and Standard or Hanafi Asr settings.
- Configure location and IANA timezone explicitly.
- Show the next prayer and a second-by-second countdown.
- Display Qibla direction with progressive device-compass support.
- Browse Gregorian and Hijri calendar views.
- Use a digital Tasbih with locally persisted state and selectable dhikr.
- Browse searchable content for the 99 Names of Allah.
- Install the PWA and use its cached application shell offline.

**Technology and design**
- Framework-free JavaScript, HTML and CSS.
- Bundled PrayTimes.js calculation engine.
- Service Worker and versioned cache lifecycle.
- Browser local storage for settings and Tasbih state.
- Static GitHub Pages deployment.

**Privacy and operational behavior**
- No account, analytics service or application backend is required.
- Location permission is requested only after the user chooses location detection.
- Coordinates are not sent to a reverse-geocoding service.
- Geolocation, notifications and device-compass access are optional browser capabilities.

**Engineering focus:** Deterministic calculation inputs, timezone-aware date handling, local-first design, offline caching, accessibility and progressive browser capabilities.

**Explore:** [Live application](https://aaqibhafeezkhan.github.io/DeenTime/) · [Testing guide](https://github.com/Aaqibhafeezkhan/DeenTime/blob/main/TESTING.md) · [Source code](https://github.com/Aaqibhafeezkhan/DeenTime)

---

### 4. DeHTML Studio

**A browser-based toolkit for working with HTML and related web code.**

[Source repository](https://github.com/Aaqibhafeezkhan/DeHTML) · [Live application](https://aaqibhafeezkhan.github.io/DeHTML/)

DeHTML brings common markup and text tasks into one React application, with separate tools for transformation, comparison, formatting and preview.

**Tools**
- **Strip Tags:** Extract readable text from pasted HTML and show character, word and line counts.
- **Encode / Decode:** Convert text to HTML entities and decode entities or markup.
- **Diff Viewer:** Compare two text inputs line by line, identifying unchanged, removed and added lines.
- **Formatter:** Indent pasted HTML to make its structure easier to inspect.
- **Minifier:** Apply lightweight HTML, CSS or JavaScript text transformations.
- **Previewer:** Render pasted HTML, CSS and JavaScript in a sandboxed iframe.

**Technology and design**
- React and Vite.
- Browser DOM APIs for HTML-related operations.
- Lightweight text transformations for formatting and minification.
- Sandboxed iframe preview.
- GitHub Pages deployment.

**Engineering focus:** Focused developer utilities, interactive browser tooling, text processing and safe isolation of preview content.

**Limitations:** The formatter and minifier are intentionally lightweight rather than full standards-compliant parsers. Previewed scripts execute in a sandboxed iframe, so the previewer is not a sanitizer or security boundary for untrusted content.

**Explore:** [Live application](https://aaqibhafeezkhan.github.io/DeHTML/) · [Source code](https://github.com/Aaqibhafeezkhan/DeHTML)

---

### 5. Indian Parliament Explorer

**A civic-data explorer for representation across the Lok Sabha and Rajya Sabha.**

[Source repository](https://github.com/Aaqibhafeezkhan/IndianParliamentInfographic) · [Live application](https://aaqibhafeezkhan.github.io/IndianParliamentInfographic/)

Indian Parliament Explorer turns published parliamentary member datasets into a searchable and comparable browser experience. It loads data automatically, makes source dates visible and provides tools to explore representation across both Houses.

**Capabilities**
- Load Lok Sabha and Rajya Sabha member records on first visit.
- Search, filter, sort and compare members across both Houses.
- Explore member profiles and historical Parliament references.
- View representation analytics derived from the loaded records.
- Share views through URL-based filters.
- Export filtered data to CSV.
- Cache successful data locally and retain the last successful snapshot when refresh fails.
- Show source snapshot dates separately from browser retrieval time.

**Data provenance and integrity**
- Retrieves published JSON snapshots from RTI Wiki.
- Attributes the snapshots and documents their CC BY 4.0 licensing.
- Links to source and data-license documentation.
- Maps only fields present in the source records.
- Does not present unavailable attendance, questions, debates, bills, assets, liabilities or criminal-case values as verified data.
- Clearly distinguishes source snapshot dates from retrieval timestamps.

**Technology and design**
- Browser-based JavaScript application.
- Published JSON data sources.
- Browser storage for successful data snapshots.
- Static GitHub Pages deployment.

**Engineering focus:** Data provenance, transparent freshness, resilient client-side data loading, derived analytics, filtering and export workflows.

**Scope note:** This is an independent visualization project, not an official Parliament of India, Lok Sabha, Rajya Sabha or Digital Sansad product. A successful data download does not imply that the underlying snapshot is real-time or independently verified.

**Explore:** [Live application](https://aaqibhafeezkhan.github.io/IndianParliamentInfographic/) · [Sources](https://github.com/Aaqibhafeezkhan/IndianParliamentInfographic/blob/main/SOURCES.md) · [Source code](https://github.com/Aaqibhafeezkhan/IndianParliamentInfographic)

---

### 6. Anti-Doomscroll Journal

**A React Native digital-wellbeing application built around screen-time awareness and guided reflection.**

[Source repository](https://github.com/Aaqibhafeezkhan/Anti-Doomscroll-SDK)

Anti-Doomscroll Journal combines native screen-time monitoring with a structured gratitude intervention. When configured usage conditions are met, the app can interrupt a scrolling session with a reflection flow rather than relying only on passive usage statistics.

**Capabilities**
- Monitor foreground application usage through native Android and iOS capabilities.
- Present a guided gratitude reflection flow with timed sessions and structured entries.
- Track streaks and historical journal activity.
- Show usage insights, including mood distribution, trigger-app analysis and a 90-day activity view.
- Support light, dark and system-adaptive themes.
- Store journal entries and app state on-device.

**Technology and design**
- React Native 0.73.
- React Navigation 6 and Zustand.
- MMKV for application state.
- SQLite through react-native-quick-sqlite for journal data.
- Reanimated, Lottie and react-native-svg.
- Native Android UsageStatsManager and iOS DeviceActivity integrations.
- Background fetch and local notifications.

**Engineering focus:** Native platform integration, mobile state management, local persistence, background capabilities and data visualization.

**Platform requirements:** Android development requires JDK 17 and the Android SDK. iOS development requires Xcode and CocoaPods. Access to native screen-time APIs depends on platform permissions and capabilities.

**Explore:** [Project overview and setup](https://github.com/Aaqibhafeezkhan/Anti-Doomscroll-SDK#readme) · [Source code](https://github.com/Aaqibhafeezkhan/Anti-Doomscroll-SDK)

---

## Engineering themes

Across these projects, the recurring engineering concerns are:

- **Backend and API design:** predictable REST interfaces, external API integration, filtering, pagination, caching and documentation.
- **Frontend architecture:** independent application boundaries, runtime composition, reusable interfaces and responsive browser experiences.
- **Reliability:** explicit state transitions, resilient data loading, cache lifecycle management and reproducible test workflows.
- **Privacy and local-first design:** minimizing backend dependencies, keeping personal state on-device and making permission requests user-driven.
- **Data integrity:** identifying source provenance, showing data freshness and distinguishing source facts from derived analytics.
- **Developer experience:** practical browser tools, clear setup instructions, API examples and focused workflows.

## Technology coverage

| Area | Technologies represented |
|---|---|
| Languages | Java, JavaScript, TypeScript, HTML, CSS |
| Backend | Spring Boot, REST APIs, OpenAPI |
| Frontend | React, Angular, Svelte, Vue, Vite |
| Architecture | Microfrontends, single-spa, SystemJS, import maps |
| Mobile | React Native, React Navigation, native Android and iOS APIs |
| Data and storage | Caffeine, SQLite, MMKV, browser local storage, JSON |
| Delivery | Docker, GitHub Pages, service workers, Webpack |

## Repository index

| Repository | Description |
|---|---|
| [Books-API](https://github.com/Aaqibhafeezkhan/Books-API) | Spring Boot book discovery API |
| [CMS-Microfrontend](https://github.com/Aaqibhafeezkhan/CMS-Microfrontend) | Multi-framework CMS microfrontend platform |
| [DeenTime](https://github.com/Aaqibhafeezkhan/DeenTime) | Local-first Islamic PWA |
| [DeHTML](https://github.com/Aaqibhafeezkhan/DeHTML) | HTML and web-code developer toolkit |
| [IndianParliamentInfographic](https://github.com/Aaqibhafeezkhan/IndianParliamentInfographic) | Parliamentary civic-data explorer |
| [Anti-Doomscroll-SDK](https://github.com/Aaqibhafeezkhan/Anti-Doomscroll-SDK) | React Native digital-wellbeing journal |

## Related work

- **[Open-source contributions](https://github.com/AAQIB-LOCAL/Aaqib-OSS-Contributions):** A separate, evidence-backed record of merged upstream contributions, selected engineering work and contribution methodology.
- **[GitHub profile](https://github.com/Aaqibhafeezkhan):** Professional overview, experience, skills and contact links.
- **[Portfolio](https://aaqibhafeezkhan.github.io/aaqibhafeezkhan.cv):** Extended professional profile.

---

This repository is a curated index of selected projects. For implementation details, setup instructions, limitations, licenses and the latest project status, use the README and documentation in each linked source repository.
