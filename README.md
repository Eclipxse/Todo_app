# Eclipxse

<p align="center">
  <img src="build/icon-cute.png" alt="Eclipxse strawberry-heart icon" width="160" />
</p>

**Eclipxse** is a cute, privacy-first todo, focus, and time-tracking app. It is a
personalized open-source edition of
[Super Productivity](https://github.com/super-productivity/super-productivity),
with the complete productivity feature set preserved.

## What makes this edition different

- **Strawberry Milk** light theme and **Berry Night** dark theme
- Pink, cream, and lavender surfaces with rounded task cards
- Original photorealistic cat artwork for onboarding, empty lists, and celebrations
- Tiny stars, sparkles, playful cat captions, and reduced-motion support
- Custom Eclipxse desktop branding and strawberry-heart icon
- Personalized onboarding and encouraging empty-list messages
- Responsive styling verified on desktop and phone layouts
- Offline-first behavior with no analytics or advertising

## Core features

- Tasks, subtasks, projects, tags, notes, and recurring tasks
- Pomodoro, focus mode, break reminders, and time tracking
- Planner, calendar, schedule, boards, and habits
- GitHub, GitLab, Jira, CalDAV, and other integrations
- Local backups plus optional sync
- Desktop, web, and mobile application foundations

## Development

The project currently expects the Node.js version declared in `.nvmrc`.

```powershell
npm.cmd ci
npm.cmd run startFrontend
```

Build a Windows x64 installer:

```powershell
npm.cmd run buildAllElectron:noTests:prod
npx.cmd electron-builder --win nsis --x64 --publish never
```

Useful checks:

```powershell
npm.cmd run lint
npm.cmd run test:file -- src/app/core/theme/custom-theme.service.spec.ts --watch=false
npm.cmd run test:file -- src/app/core/browser-title/browser-title.service.spec.ts --watch=false
```

## Privacy

Task data remains on the device unless the user explicitly configures sync. No
analytics or tracking were added by this edition.

## Artwork

The three cat images under `src/assets/eclipxse/cats/` were generated specifically
for Eclipxse. They are original project assets rather than copied Pinterest photos.

## Attribution and license

Eclipxse is based on Super Productivity by Johannes Millan and its contributors.
The project remains available under the [MIT License](LICENSE). Upstream source and
documentation are available at
[super-productivity/super-productivity](https://github.com/super-productivity/super-productivity).
