<div align="center">

<img src="src/assets/eclipxse/cats/onboarding-planner-kitten.png" alt="A curious orange kitten with a pink bow helping with a planner" width="860" />

# ✦ Eclipxse ✦

### tiny tasks · soft colors · very serious cats

<p>
  <img src="https://img.shields.io/badge/theme-strawberry_milk-f68aaa?style=for-the-badge&labelColor=fff0f5" alt="Strawberry Milk theme" />
  <img src="https://img.shields.io/badge/privacy-offline_first-a94186?style=for-the-badge&labelColor=f2e5ff" alt="Offline first" />
  <img src="https://img.shields.io/badge/cat_staff-3-e0a73c?style=for-the-badge&labelColor=fffaf2" alt="Three cat coworkers" />
  <img src="https://img.shields.io/badge/license-MIT-4d8066?style=for-the-badge&labelColor=effaf4" alt="MIT License" />
</p>

<p><strong>A sweet, private and seriously capable todo app—made with affection for someone special. ♡</strong></p>

<p>
  Tasks · Focus timer · Time tracking · Planner · Notes · Habits · Calendar · Optional sync
</p>

</div>

---

## ୨୧ Hello, cutie

**Eclipxse** is a personalized open-source edition of
[Super Productivity](https://github.com/super-productivity/super-productivity).
Under the bows and sparkles is a full productivity suite: projects, subtasks,
recurring tasks, focus mode, time tracking, scheduling, integrations and backups.

It keeps the powerful parts and gives them a softer little home:

- 🍓 **Strawberry Milk** during the day and **Berry Night** after dark
- 🐾 Original funny-cat moments for onboarding, empty lists and celebrations
- ✦ Tiny stars, sparkles, hearts and encouraging messages
- 🎀 Rounded cards, gentle shadows and pink–cream–lavender surfaces
- 🫶 Reduced-motion support, responsive layouts and readable contrast
- 🔒 Local-first data with no analytics or advertising added by this edition

> **Cat promise:** no random Pinterest photos were copied. Every cat image in this
> repository was generated specifically for Eclipxse.

---

## 🐾 Meet the tiny coworkers

<table>
  <tr>
    <td align="center" width="33%">
      <img src="src/assets/eclipxse/cats/onboarding-planner-kitten.png" alt="Curious planner kitten" width="280" /><br />
      <strong>Mochi, Head of Onboarding</strong><br />
      <sub>chooses setups by sitting on them ✦</sub>
    </td>
    <td align="center" width="33%">
      <img src="src/assets/eclipxse/cats/empty-list-loaf.png" alt="Bored cat resting on a planner" width="280" /><br />
      <strong>Bean, Empty-List Inspector</strong><br />
      <sub>confirms there is absolutely nothing to do</sub>
    </td>
    <td align="center" width="33%">
      <img src="src/assets/eclipxse/cats/daily-summary-high-five.png" alt="Crowned tuxedo kitten offering a high five" width="280" /><br />
      <strong>Pixel, Celebration Manager</strong><br />
      <sub>wears the crown whenever you finish the day ♡</sub>
    </td>
  </tr>
</table>

---

## ✦ Cute outside, powerful inside

| Little corner       | What lives there                                                        |
| ------------------- | ----------------------------------------------------------------------- |
| 🎀 **Tasks**        | Subtasks, recurring tasks, priorities, estimates, attachments and notes |
| 🍰 **Projects**     | Projects, tags, sections, boards and custom task views                  |
| 🍓 **Focus**        | Focus mode, Pomodoro sessions, break reminders and task timers          |
| 🗓️ **Planning**     | Today view, planner, schedule, calendar and upcoming deadlines          |
| 🌷 **Habits**       | Simple counters, streaks and daily goals                                |
| 🧁 **Review**       | Worklog, metrics and a crowned-cat end-of-day celebration               |
| ☁️ **Sync**         | Optional Dropbox, WebDAV, Nextcloud and local-file sync                 |
| 🧸 **Integrations** | GitHub, GitLab, Jira, CalDAV and community plugins                      |

---

## 🎨 The Eclipxse palette

<div align="center">

![Strawberry](https://img.shields.io/badge/Strawberry-%23C92F61-C92F61?style=flat-square)
![Blush](https://img.shields.io/badge/Blush-%23F68AAA-F68AAA?style=flat-square)
![Cream](https://img.shields.io/badge/Cream-%23FFFAF2-FFFAF2?style=flat-square&labelColor=e9d8cb)
![Lavender](https://img.shields.io/badge/Lavender-%23A94186-A94186?style=flat-square)
![Berry Night](https://img.shields.io/badge/Berry_Night-%231D1623-1D1623?style=flat-square)

</div>

The custom theme is selected automatically for a fresh install. It follows the
system light/dark preference, so Strawberry Milk becomes Berry Night without
losing its personality.

---

## 🪄 Run Eclipxse

### Windows build

After this branch is merged, open **Actions → Build Eclipxse for Windows → Run
workflow**. The workflow creates both:

- `Eclipxse-Setup-x64.exe` — the normal installer
- `Eclipxse-Portable-x64.exe` — a no-install portable app

These personal builds are not signed with a commercial code-signing certificate,
so Windows SmartScreen may ask for confirmation the first time they open.

### Android build

Open **Actions → Build Eclipxse for Android → Run workflow**. When the run
finishes, download the `Eclipxse-Todo-Android` artifact and extract:

- `Eclipxse-Todo-Android.apk` — the installable Android application
- `SHA256SUMS.txt` — a checksum for verifying the download

The Android edition has its own `com.eclipxse.todo` application ID, so it can be
installed beside the official Super Productivity app. It starts in offline-first
mode and uses the same private, local task storage model as the desktop edition.

This personal APK is debug-signed rather than Play Store signed. Android will ask
you to allow installation from the browser or file manager used to open it. Only
install APKs downloaded from this repository's own Actions page. Until a permanent
private signing key is configured, installing a later Actions build may require
uninstalling the earlier Eclipxse build first; export or sync important tasks before
doing that.

### Run from source

Use the Node.js version declared in `.nvmrc`.

```powershell
npm.cmd ci
npm.cmd run startFrontend
```

Then visit `http://localhost:4200`.

<details>
<summary><strong>Developer spells ✦</strong></summary>

Build the production Electron application:

```powershell
npm.cmd run buildAllElectron:noTests:prod
npx.cmd electron-builder --win nsis portable --x64 --publish never
```

Run the main checks:

```powershell
npm.cmd run lint
npm.cmd run int:test
npm.cmd run test:file -- src/app/core/theme/custom-theme.service.spec.ts
npm.cmd run test:file -- src/app/core/browser-title/browser-title.service.spec.ts
```

Build outputs appear under `.tmp/app-builds/`.

</details>

---

## 🔒 Privacy, because personal things should stay personal

Eclipxse stores task data locally by default. Nothing is sent anywhere unless the
user deliberately configures a sync provider. This edition adds no analytics,
tracking or advertising.

For important task data, configure sync or export backups regularly from Settings.

---

## 🌸 Artwork

The three project-specific cat images live in `src/assets/eclipxse/cats/`:

```text
daily-summary-high-five.png
empty-list-loaf.png
onboarding-planner-kitten.png
```

They were created as original assets for Eclipxse and are used directly by the app.

---

## ♡ Thank you, upstream

Eclipxse is based on **Super Productivity** by Johannes Millan and its contributors.
The original project provides the application architecture and complete productivity
feature set that make this edition possible.

- Upstream: [super-productivity/super-productivity](https://github.com/super-productivity/super-productivity)
- License: [MIT](LICENSE)

<div align="center">

### made with strawberries, sparkles and an unreasonable number of cat opinions ♡

<img src="build/icon-cute.png" alt="Eclipxse strawberry-heart icon" width="120" />

</div>
