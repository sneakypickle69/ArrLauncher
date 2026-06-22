Link to pages: https://sneakypickle69.github.io/ArrLauncher/arrlauncher.html#mode


# ArrLauncher

A simple, single-file HTML launcher for self-hosted app web UIs (Sonarr, Radarr, Prowlarr, qBittorrent, etc.), built for use over a local network or [Tailscale](https://tailscale.com).

## Features

- Choose **Local** or **Remote (Tailscale)** mode on launch — each remembers its own IP/hostname.
- Add, edit, and delete apps with custom names, ports, and icons.
- Icons: built-in presets for qBittorrent, Sonarr, Radarr, Prowlarr, or your own (image upload or URL).
- Big touch-friendly buttons, dark mode.
- Browser back/forward navigation support.
- All data (apps, ports, icons, IPs) stored locally in your browser — nothing leaves your device except requests to the icon URLs you add and the services you launch.

## Usage

1. Host `launcher.html` on a local web server (required for `localStorage` persistence and "Add to Home Screen" — `file://` does not work reliably).
2. Open it in your browser.
3. Select **Local** or **Remote**, enter the corresponding IP/hostname.
4. Tap **+ Add App** to add a service (name, port, optional icon).
5. Tap an app icon to open it at `http://<ip>:<port>`.

### Installing as an app (Android)

In Firefox or Chrome, open the page over `http://`, then use the browser menu's **Add to Home screen** / **Install** option.

## Notes

- Mode selection resets every time the app is opened; your saved apps and IPs persist.
- Custom icon URLs must point directly to an image file (e.g. `raw.githubusercontent.com` links, not `github.com/.../blob/...` page links).
