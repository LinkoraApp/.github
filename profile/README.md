# Linkora

Linkora lets you save and organise links across your devices.

## The pieces

**[Linkora App](https://github.com/LinkoraApp/Linkora)** - The main app for Android and desktop. Save links, organise them into folders, and search through them. Works offline, syncs when connected.

**[Sync Server](https://github.com/LinkoraApp/sync-server)** - A server you run on your computer or VPS. Keeps everything in sync between devices.

**[Browser Extension](https://github.com/LinkoraApp/browser-extension)** - Save link metadata to your Linkora folders from your browser. Create folders and subfolders, and choose where to save each link.

**[Localization Server](https://github.com/LinkoraApp/localization-server)** - Serves up translations for the app. Contributors maintain translations in different languages, and the app is updated with new text without requiring a new version. You can contribute too - check the [localization server readme](https://github.com/LinkoraApp/localization-server) to see how.

## Overview

```mermaid
graph TB
    A[Linkora App<br/>Android/Desktop] --> B[Sync Server<br/>Self-hosted]
    C[Browser Extension] --> B
    D[Localization Server<br/>Translations] --> A
    
    B --> E[Sync Database<br/>MySQL/PostgreSQL/SQLite]
    A --> F[Local App Database]
    C --> G[Local Extension Storage]
    
    H[Web Browser] --> C
    I[Android Mobile] --> A
    J[Desktop] --> A
    
    style A fill:#1976D2,color:#FFFFFF
    style B fill:#388E3C,color:#FFFFFF
    style C fill:#F57C00,color:#FFFFFF
    style D fill:#7B1FA2,color:#FFFFFF
    style E fill:#455A64,color:#FFFFFF
    style F fill:#5D4037,color:#FFFFFF
    style G fill:#5D4037,color:#FFFFFF
```
