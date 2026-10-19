# Martlet for Emacs

## Install

Copy both `-theme.el` files into `~/.emacs.d/themes/`, then add to your init file:

```elisp
(add-to-list 'custom-theme-load-path
             (expand-file-name "themes/" user-emacs-directory))
(load-theme 'martlet-dark t)
```

Use `martlet-light` for Light. Disable the current theme with `M-x disable-theme` before switching, to avoid layering theme faces. The `t` bypasses the confirmation prompt; use it after reviewing the theme source.

Alternatively clone this repository and add its directory to `custom-theme-load-path`. `martlet-themes.el` registers its own directory when loaded. Emacs 27.1+ is required. Includes standard font-lock, editor UI, Org, diff, completion, and ANSI faces. GUI and truecolor terminals provide the closest match; limited-color terminals approximate colors. Not yet submitted to MELPA.

These are generated distributions of [Martlet Theme](https://martlettheme.dev/), version 1.0.0. Canonical colors and generators live in [martlettheme/martlettheme](https://github.com/martlettheme/martlettheme). The source repository may require maintainer access. This repository includes a complete color snapshot in source.json and can build without access to that repository.

MIT license. Copyright 2026 James P. Howard, II.

## Maintenance

Edit the canonical palette and generator upstream, then run npm run build there. The complete distribution directories are emitted under artifacts/repositories/. Sync the relevant directory into this repository. To reproduce a snapshot here, run npm run build, then npm test. Node.js 22 or newer is used in CI. No registry publication runs automatically.
