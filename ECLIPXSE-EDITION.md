# Eclipxse

This is a personalized build of [Super Productivity](https://super-productivity.com/)
with the full original task-management feature set and a custom Strawberry Milk
theme.

## Personal touches

- Strawberry Milk is selected automatically on a fresh install.
- The theme includes soft pink, cream, and lavender surfaces; rounded task cards;
  heart details; and calm high-contrast typography.
- The desktop shell is named **Eclipxse** and uses a matching strawberry-heart icon.
- Berry Night keeps the same personality when the system uses dark mode.
- Original funny-cat artwork appears during onboarding, on empty task lists, and in
  the end-of-day celebration.
- Tiny animated stars and sparkles are disabled automatically when reduced motion is
  preferred.

The original application remains available under the MIT license. Its privacy-first,
offline-first behavior and data model are unchanged.

## Which Windows file should I use?

- **Eclipxse-Setup-x64.exe** installs the app normally and creates the usual Windows
  shortcuts. This is the best choice for everyday use.
- **Eclipxse-Portable-x64.exe** runs without installation. Keep it in a folder where
  the user has write access.

Because this is a private custom build rather than a publicly code-signed release,
Windows SmartScreen may ask for confirmation the first time it opens.

Task data is stored locally by default. Set up sync or export backups from Settings
if the app will be used across devices or if the tasks are important.

## Run locally

```powershell
npm.cmd install
npm.cmd run startFrontend
```

## Build a Windows installer

```powershell
npm.cmd run buildAllElectron:noTests:prod
npx.cmd electron-builder --win nsis --x64 --publish never
```

Build outputs are written to `.tmp/app-builds/`.
