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

## Flagship projects at a glance

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

## Additional projects

The six flagship projects above are only part of the portfolio. The following catalogue adds the other original applications, utilities, libraries, experiments, and technical reference projects found during the account audit.

### AI, data, civic technology and analytics

#### [AI Benchmark](https://github.com/Aaqibhafeezkhan/AI-Benchmark)
A Next.js workspace for side-by-side LLM comparison. It supports mock runs for offline UI experimentation, provider-backed responses where credentials are supplied, streamed output, manual scoring, runnable prompt cases, and a LiveBench leaderboard view. The repository distinguishes exploratory comparisons from versioned benchmark records and does not claim that live-provider results are scientifically reproducible.

**Stack:** Next.js, TypeScript, React.

[Source](https://github.com/Aaqibhafeezkhan/AI-Benchmark) · [Live app](https://aaqib-hafeez-khan-in.github.io/AI-Benchmark/)

#### [OpenNewsGrid](https://github.com/Aaqibhafeezkhan/OpenNewsGrid)
A global news aggregation application combining RSS feeds, NewsAPI and GNews integrations. It includes regional browsing, category pages, full-text search, filters, duplicate-story handling, and responsive article views.

**Stack:** Next.js 15, TypeScript, Tailwind CSS, RSS and news APIs.

[Source](https://github.com/Aaqibhafeezkhan/OpenNewsGrid) · [Live app](https://open-news-grid.vercel.app/)

#### [India Civic Pulse](https://github.com/Aaqibhafeezkhan/India-Civic-Pulse)
A map-first civic information reader that connects public-interest updates to source records, publication dates and carefully caveated geography. Its ingestion pipeline works with official RBI and SEBI RSS feeds, while the browser interface provides a searchable story feed, topic filters and a Leaflet map. Publisher records are not presented as independently fact-checked reporting.

**Stack:** Python, JavaScript, Leaflet, RSS, JSON.

[Source](https://github.com/Aaqibhafeezkhan/India-Civic-Pulse)

#### [Pollinations AI Chat Platform](https://github.com/Aaqibhafeezkhan/Streamlit-Pollination-Chatbot)
A Streamlit chatbot with model selection, streaming responses, document-based retrieval, conversation management, prompt personas, exports and analytics. Its local data layer uses SQLite and ChromaDB for conversation and retrieval state.

**Stack:** Python, Streamlit, SQLite, ChromaDB.

[Source](https://github.com/Aaqibhafeezkhan/Streamlit-Pollination-Chatbot)

#### [IMDb Stats](https://github.com/Aaqibhafeezkhan/imdb-stats)
A Scala/SBT command-line data tool that downloads IMDb's public bulk datasets, joins title and rating records, applies a configurable vote threshold, and generates ranked current-year movie reports. Its documentation distinguishes daily-updated bulk data from exact calendar-date or real-time API data.

**Stack:** Scala, SBT, IMDb public datasets.

[Source](https://github.com/Aaqibhafeezkhan/imdb-stats)

### Developer tools, libraries and productivity utilities

#### [i18n Missing Translations Detector](https://github.com/Aaqibhafeezkhan/i18n-Translations-missing-script)
A zero-configuration CLI that scans language JSON files for translation values that remain identical to the base language. It supports configurable language lists, whitelists, structured reports and a non-zero exit code suitable for CI checks.

**Stack:** TypeScript, Node.js.

[Source](https://github.com/Aaqibhafeezkhan/i18n-Translations-missing-script) · [Live demo](https://aaqibhafeezkhan.github.io/i18n-Translations-missing-script/)

#### [NoCodeComments](https://github.com/Aaqibhafeezkhan/NoCodeComments)
A browser-first source-code comment remover. Its lexical scanner protects comment-like text inside supported strings, template literals and regular expressions, preserves line breaks in removed multiline comments, and supports local-file processing without uploading source code.

**Stack:** JavaScript, HTML, CSS, Node.js test runner.

[Source](https://github.com/Aaqibhafeezkhan/NoCodeComments) · [Live app](https://aaqibhafeezkhan.github.io/NoCodeComments/)

#### [Evergreen Countdown](https://github.com/Aaqibhafeezkhan/Evergreen-Countdown)
A reusable countdown system for profile READMEs and standalone pages. A shared countdown engine handles target parsing and IANA timezones, while a serverless endpoint generates an embeddable SVG and the static frontend provides a themed countdown page.

**Stack:** JavaScript, SVG, Vercel serverless functions.

[Source](https://github.com/Aaqibhafeezkhan/Evergreen-Countdown) · [Countdown API](https://evergreen-countdown.vercel.app/api/countdown)

#### [Polyglot Utilities Toolkit](https://github.com/Aaqibhafeezkhan/polyglot-utilities-toolkit)
A capability-first collection of small reusable utilities with language-specific implementations. It groups common collection, string, number, date and validation helpers, and includes a cross-language test matrix rather than assuming every utility exists in every language.

**Stack:** TypeScript, JavaScript, Python, C++, Java, Go, Rust, C#, Kotlin.

[Source](https://github.com/Aaqibhafeezkhan/polyglot-utilities-toolkit)

#### [Form Components Builder](https://github.com/Aaqibhafeezkhan/Form-Components-Builder)
A browser-based drag-and-drop form designer. It provides a component palette, canvas reordering, field properties, validation rules, conditional visibility, multi-step forms, themes, preview mode, templates, and exports to JSON Schema, standalone HTML and React JSX.

**Stack:** HTML5, CSS3, JavaScript.

[Source](https://github.com/Aaqibhafeezkhan/Form-Components-Builder) · [Live app](https://aaqibhafeezkhan.github.io/Form-Components-Builder/)

#### [Clipper](https://github.com/Aaqibhafeezkhan/Clipper)
A focused, client-side image utility for adding a white border or removing a border by cropping. Users can select or drop an image, adjust the percentage, preview the result and download a PNG. Image processing uses browser canvas APIs without a server-side processing service.

**Stack:** HTML, CSS, JavaScript, File API, Canvas.

[Source](https://github.com/Aaqibhafeezkhan/Clipper)

#### [Image Picker](https://github.com/Aaqibhafeezkhan/Image-picker)
An Android image-picker library for selecting an image from the camera or gallery, with image cropping, compression and EXIF-based rotation handling. The repository documents JitPack integration and callback-based result handling.

**Stack:** Java, Android SDK, Gradle.

[Source](https://github.com/Aaqibhafeezkhan/Image-picker)

#### [Privacy Permitter](https://github.com/Aaqibhafeezkhan/Privacy-Permitter)
A Chrome extension that lists installed extensions and scores their declared permissions and host access using a deterministic heuristic. It groups results into risk bands and supports search and filtering. The score is an awareness aid, not a definitive security verdict or a source-code/runtime audit.

**Stack:** JavaScript, Chrome Extensions APIs.

[Source](https://github.com/Aaqibhafeezkhan/Privacy-Permitter)

#### [Script Scheduler](https://github.com/Aaqibhafeezkhan/Script-Scheduler)
A script scheduling application with a browser UI and backend execution service. It supports shell and batch-script uploads, recurring schedules, execution history, status filtering, cancellation and persistent schedule data.

**Stack:** Node.js, React, SQLite, JavaScript.

[Source](https://github.com/Aaqibhafeezkhan/Script-Scheduler)

### Applications and interactive experiences

#### [GameVault](https://github.com/Aaqibhafeezkhan/GameVault)
A browser arcade that brings together more than 50 playable arcade, puzzle, card, word, reflex and strategy games. Game components are loaded within a shared React interface, with browser storage used for supported high scores and saved state.

**Stack:** React, JavaScript, Vite, Styled Components.

[Source](https://github.com/Aaqibhafeezkhan/GameVault) · [Live app](https://arcadegame-vault.vercel.app/)

#### [Tactical XI - World Cup](https://github.com/Aaqibhafeezkhan/Tactical-XI-World-Cup)
A football tactics sandbox and historical men's World Cup explorer. It combines lineup construction, formations, player roles and tactical controls with a historical tournament archive. The application keeps recorded historical facts, reconstructed tactical metadata and hypothetical simulation output distinct; its app-generated ratings are not official FIFA ratings.

**Stack:** TypeScript, JavaScript, browser-based data visualization.

[Source](https://github.com/Aaqibhafeezkhan/Tactical-XI-World-Cup) · [Live app](https://aaqibhafeezkhan.github.io/Tactical-XI-World-Cup/)

#### [CSS Animation Studio](https://github.com/Aaqibhafeezkhan/CSS-Animation-Studio)
A progressive web app for browsing a curated animation library and building custom CSS keyframes. It includes search and filters, animation previews, a visual builder, side-by-side comparisons, favorites, playlists, CSS import/export and offline-capable installation.

**Stack:** React, JavaScript, CSS, Vite, PWA.

[Source](https://github.com/Aaqibhafeezkhan/CSS-Animation-Studio)

#### [MicrobloggingApp](https://github.com/Aaqibhafeezkhan/MicrobloggingApp)
A full-stack microblogging platform with short posts, image uploads, timeline filtering, post management and real-time updates. The solution separates API, core services, data access, frontend and test projects.

**Stack:** C#, ASP.NET Core 8, Razor Pages, SQL Server, Entity Framework Core, Azure Blob Storage, SignalR, Hangfire.

[Source](https://github.com/Aaqibhafeezkhan/MicrobloggingApp)

#### [CoreQA](https://github.com/Aaqibhafeezkhan/CoreQA)
A dependency-light Q&A forum with registration, authentication, questions, replies, tags, search, pagination, Markdown rendering, voting, moderation and administrator workflows. It supports SQLite for local development and MySQL/MariaDB for deployment.

**Stack:** PHP 8.2+, PDO, SQLite, MySQL/MariaDB.

[Source](https://github.com/Aaqibhafeezkhan/CoreQA)

#### [SecureAuth](https://github.com/Aaqibhafeezkhan/SecureAuth)
An Android TOTP authenticator that generates six-digit RFC 6238-compatible codes locally. Secrets are encrypted at rest with AES-GCM using a key held by Android Keystore; the project includes local unit tests and explicit account deletion behavior.

**Stack:** Java, Android, Gradle, Android Keystore.

[Source](https://github.com/Aaqibhafeezkhan/SecureAuth)

#### [Invisibility Cloak](https://github.com/Aaqibhafeezkhan/invisibility-cloak)
A browser-based computer-vision demo that captures a clean background and replaces pixels matching a selected cloak color in a live camera feed. It includes background calibration, HSV range controls, mask smoothing and PNG snapshot export.

**Stack:** Python, Streamlit, OpenCV, NumPy, WebRTC.

[Source](https://github.com/Aaqibhafeezkhan/invisibility-cloak)

#### [MyTechAccounts](https://github.com/Aaqibhafeezkhan/MyTechAccounts)
A personal developer hub for finding coding, learning, data and freelance profiles. It provides search, filtering, quick external links, theme switching and persistent pinned profiles.

**Stack:** HTML, CSS, JavaScript, browser local storage.

[Source](https://github.com/Aaqibhafeezkhan/MyTechAccounts) · [Live app](https://aaqibhafeezkhan.github.io/MyTechAccounts/)

#### [Simple Resume Builder](https://github.com/Aaqibhafeezkhan/SimpleResumeBuilder)
A browser-only resume editor with drag-and-drop section ordering, inline editing, multiple templates, theme and typography controls, local auto-save, session restore and PDF output through the browser print dialog.

**Stack:** HTML, CSS, JavaScript, localStorage.

[Source](https://github.com/Aaqibhafeezkhan/SimpleResumeBuilder) · [Live app](https://aaqib-hafeez-khan-in.github.io/SimpleResumeBuilder/)

#### [Curriculum Vitae Forge](https://github.com/Aaqibhafeezkhan/Curriculum-Vitae-Forge)
A framework-free resume builder with drag-and-drop sections, inline editing, multiple templates, undo/redo, JSON import/export, style controls, auto-save and PDF export.

**Stack:** HTML5, CSS, JavaScript, html2pdf.js, localStorage.

[Source](https://github.com/Aaqibhafeezkhan/Curriculum-Vitae-Forge) · [Live app](https://curriculum-vitae-forge.vercel.app/)

#### [Pokémon Literal Doodle](https://github.com/Aaqibhafeezkhan/Pokemon-literal-doodle)
A Pokédex-style gallery featuring the 151 Generation I Pokémon plus MissingNo. Individual artwork pages use generated HTML and CSS box-shadow pixel data rather than a framework, canvas or image assets.

**Stack:** HTML, CSS, JavaScript.

[Source](https://github.com/Aaqibhafeezkhan/Pokemon-literal-doodle) · [Live gallery](https://aaqib-hafeez-khan-in.github.io/Pokemon-literal-doodle/)

### Learning collections and technical references

#### [FreeCodeCamp Projects](https://github.com/Aaqibhafeezkhan/FreeCodeCampProjects)
A portfolio collection of 12 backend, API, security and full-stack curriculum projects, including an exercise tracker, file metadata service, issue tracker, message board, personal library, stock price checker and timestamp microservice. The repository also contains a static showcase.

**Stack:** JavaScript, Node.js, Express, APIs and related web technologies.

[Source](https://github.com/Aaqibhafeezkhan/FreeCodeCampProjects) · [Project showcase](https://aaqib-hafeez-khan-in.github.io/FreeCodeCampProjects/)

#### [Bunch of Clones](https://github.com/Aaqibhafeezkhan/Bunch-of-clones)
A collection of interface and application-clone exercises built with a modern React/Next.js stack. The README identifies Netflix and YouTube as the implemented examples and lists the other concepts as planned work, so the catalogue does not present all listed clones as completed.

**Stack:** Next.js, TypeScript, Tailwind CSS, Framer Motion.

[Source](https://github.com/Aaqibhafeezkhan/Bunch-of-clones) · [Live site](https://bunch-of-clones.vercel.app/)

#### [React Redux Starter](https://github.com/Aaqibhafeezkhan/react-redux-starter)
A single-page application starter combining React, Redux and TypeScript, with Sass styling, Webpack bundling and Jest/Enzyme testing.

**Stack:** React, Redux, TypeScript, Sass, Webpack, Jest, Enzyme.

[Source](https://github.com/Aaqibhafeezkhan/react-redux-starter)

#### [React.js Interview Epic](https://github.com/Aaqibhafeezkhan/ReactJs-Interview-Epic)
A continuously maintained React interview reference covering JavaScript and browser fundamentals, React rendering and hooks, modern React APIs, server components, SSR, TypeScript, performance, accessibility, testing, security and frontend system design.

**Stack:** React, JavaScript, TypeScript, technical documentation.

[Source](https://github.com/Aaqibhafeezkhan/ReactJs-Interview-Epic)

#### [Spring Boot Interview Epic](https://github.com/Aaqibhafeezkhan/Spring-Boot-Interview-Epic)
A version-aware Java and Spring Boot interview knowledge base covering core Java, dependency injection, MVC, data access, transactions, security, testing, observability, messaging, deployment, distributed systems and system design.

**Stack:** Java, Spring Framework, Spring Boot, technical documentation.

[Source](https://github.com/Aaqibhafeezkhan/Spring-Boot-Interview-Epic)

### Enterprise workflow prototype

#### [Beneficiary Update](https://github.com/Aaqibhafeezkhan/NewPegaRepositories/tree/main/Beneficiary-Update)
A React interface for a case-driven beneficiary information workflow. It reads case and UI metadata from configured Pega APIs, renders metadata-driven fields, handles attachments and submits updates. Running it requires access to a configured Pega environment and valid local credentials; no public demo is listed.

**Stack:** React 19, Vite, JavaScript, Vitest, Pega APIs, Docker, Nginx.

[Source directory](https://github.com/Aaqibhafeezkhan/NewPegaRepositories/tree/main/Beneficiary-Update)

### Legacy project artifact

#### [PLMA](https://github.com/Aaqibhafeezkhan/PLMA)
An archived desktop application package. The repository contains a ClickOnce deployment package, installer and database query files referring to doctor, patient, billing and report records. The application source code is not included in the repository, so this entry is recorded as a legacy artifact rather than a currently maintainable source project.

[Repository](https://github.com/Aaqibhafeezkhan/PLMA)

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
| Languages | Java, JavaScript, TypeScript, Python, C#, PHP, Scala, HTML, CSS |
| Backend and APIs | Spring Boot, ASP.NET Core, Node.js, PHP/PDO, REST APIs, OpenAPI |
| Frontend | React, Angular, Svelte, Vue, Next.js, Vite, Razor Pages |
| Mobile | React Native, Android, Android Keystore, native iOS and Android APIs |
| Data and storage | SQLite, SQL Server, MySQL/MariaDB, H2, ChromaDB, Caffeine, MMKV, browser local storage |
| AI and data | LLM evaluation, retrieval-augmented generation, OpenCV, data ingestion, civic-data visualization |
| Architecture | Microfrontends, single-spa, SystemJS, import maps, local-first applications, PWA |
| Delivery and tooling | Docker, Nginx, GitHub Pages, Vercel, service workers, Webpack, Gradle, SBT |


## Repository index

The index below links every project represented in this catalogue. The six flagship projects retain their detailed architecture and engineering notes above; the additional entries are grouped by their primary purpose.

| Project | Category | Source |
|---|---|---|
| Books API | Backend service | [Books-API](https://github.com/Aaqibhafeezkhan/Books-API) |
| CMS Microfrontend Platform | Frontend architecture | [CMS-Microfrontend](https://github.com/Aaqibhafeezkhan/CMS-Microfrontend) |
| DeenTime | Progressive Web App | [DeenTime](https://github.com/Aaqibhafeezkhan/DeenTime) |
| DeHTML Studio | Developer tooling | [DeHTML](https://github.com/Aaqibhafeezkhan/DeHTML) |
| Indian Parliament Explorer | Civic data | [IndianParliamentInfographic](https://github.com/Aaqibhafeezkhan/IndianParliamentInfographic) |
| Anti-Doomscroll Journal | Mobile application | [Anti-Doomscroll-SDK](https://github.com/Aaqibhafeezkhan/Anti-Doomscroll-SDK) |
| AI Benchmark | AI evaluation | [AI-Benchmark](https://github.com/Aaqibhafeezkhan/AI-Benchmark) |
| OpenNewsGrid | News aggregation | [OpenNewsGrid](https://github.com/Aaqibhafeezkhan/OpenNewsGrid) |
| India Civic Pulse | Civic information | [India-Civic-Pulse](https://github.com/Aaqibhafeezkhan/India-Civic-Pulse) |
| Pollinations AI Chat Platform | AI application | [Streamlit-Pollination-Chatbot](https://github.com/Aaqibhafeezkhan/Streamlit-Pollination-Chatbot) |
| IMDb Stats | Data tooling | [imdb-stats](https://github.com/Aaqibhafeezkhan/imdb-stats) |
| i18n Missing Translations Detector | Developer tooling | [i18n-Translations-missing-script](https://github.com/Aaqibhafeezkhan/i18n-Translations-missing-script) |
| NoCodeComments | Developer tooling | [NoCodeComments](https://github.com/Aaqibhafeezkhan/NoCodeComments) |
| Evergreen Countdown | Developer utility | [Evergreen-Countdown](https://github.com/Aaqibhafeezkhan/Evergreen-Countdown) |
| Polyglot Utilities Toolkit | Utility library | [polyglot-utilities-toolkit](https://github.com/Aaqibhafeezkhan/polyglot-utilities-toolkit) |
| Form Components Builder | Developer tooling | [Form-Components-Builder](https://github.com/Aaqibhafeezkhan/Form-Components-Builder) |
| Clipper | Image utility | [Clipper](https://github.com/Aaqibhafeezkhan/Clipper) |
| Image Picker | Android library | [Image-picker](https://github.com/Aaqibhafeezkhan/Image-picker) |
| Privacy Permitter | Browser security utility | [Privacy-Permitter](https://github.com/Aaqibhafeezkhan/Privacy-Permitter) |
| Script Scheduler | Automation tool | [Script-Scheduler](https://github.com/Aaqibhafeezkhan/Script-Scheduler) |
| GameVault | Browser games | [GameVault](https://github.com/Aaqibhafeezkhan/GameVault) |
| Tactical XI - World Cup | Sports application | [Tactical-XI-World-Cup](https://github.com/Aaqibhafeezkhan/Tactical-XI-World-Cup) |
| CSS Animation Studio | Creative developer tool | [CSS-Animation-Studio](https://github.com/Aaqibhafeezkhan/CSS-Animation-Studio) |
| MicrobloggingApp | Full-stack application | [MicrobloggingApp](https://github.com/Aaqibhafeezkhan/MicrobloggingApp) |
| CoreQA | Community application | [CoreQA](https://github.com/Aaqibhafeezkhan/CoreQA) |
| SecureAuth | Android security application | [SecureAuth](https://github.com/Aaqibhafeezkhan/SecureAuth) |
| Invisibility Cloak | Computer vision demo | [invisibility-cloak](https://github.com/Aaqibhafeezkhan/invisibility-cloak) |
| MyTechAccounts | Personal developer hub | [MyTechAccounts](https://github.com/Aaqibhafeezkhan/MyTechAccounts) |
| Simple Resume Builder | Productivity application | [SimpleResumeBuilder](https://github.com/Aaqibhafeezkhan/SimpleResumeBuilder) |
| Curriculum Vitae Forge | Productivity application | [Curriculum-Vitae-Forge](https://github.com/Aaqibhafeezkhan/Curriculum-Vitae-Forge) |
| Pokémon Literal Doodle | Creative web project | [Pokemon-literal-doodle](https://github.com/Aaqibhafeezkhan/Pokemon-literal-doodle) |
| FreeCodeCamp Projects | Learning collection | [FreeCodeCampProjects](https://github.com/Aaqibhafeezkhan/FreeCodeCampProjects) |
| Bunch of Clones | Learning collection | [Bunch-of-clones](https://github.com/Aaqibhafeezkhan/Bunch-of-clones) |
| React Redux Starter | Starter template | [react-redux-starter](https://github.com/Aaqibhafeezkhan/react-redux-starter) |
| React.js Interview Epic | Technical reference | [ReactJs-Interview-Epic](https://github.com/Aaqibhafeezkhan/ReactJs-Interview-Epic) |
| Spring Boot Interview Epic | Technical reference | [Spring-Boot-Interview-Epic](https://github.com/Aaqibhafeezkhan/Spring-Boot-Interview-Epic) |
| Beneficiary Update | Enterprise workflow prototype | [NewPegaRepositories/Beneficiary-Update](https://github.com/Aaqibhafeezkhan/NewPegaRepositories/tree/main/Beneficiary-Update) |
| PLMA | Legacy desktop artifact | [PLMA](https://github.com/Aaqibhafeezkhan/PLMA) |

## Inventory scope

This catalogue covers the original, non-fork project work found in the personal GitHub account, including standalone applications, developer tools, libraries, learning collections, technical references and documented legacy artifacts. Forks and upstream mirrors, third-party project collections, empty repositories, profile/portfolio shells, team workspace indexes and clearly employer-specific work repositories are not presented as personal projects. Where a project is a learning collection, a prototype, an environment-dependent integration or a legacy binary-only artifact, that status is stated rather than implying production readiness.


## Related work

- **[Open-source contributions](https://github.com/AAQIB-LOCAL/Aaqib-OSS-Contributions):** A separate, evidence-backed record of merged upstream contributions, selected engineering work and contribution methodology.
- **[GitHub profile](https://github.com/Aaqibhafeezkhan):** Professional overview, experience, skills and contact links.
- **[Portfolio](https://aaqibhafeezkhan.github.io/aaqibhafeezkhan.cv):** Extended professional profile.

---

This repository is a curated index of selected projects. For implementation details, setup instructions, limitations, licenses and the latest project status, use the README and documentation in each linked source repository.
