# chmod Calculator

A Unix file-permission calculator. Toggle read, write, and execute for owner, group, and other in a 3x3 grid, and watch the octal value (like 755) and the symbolic string (like rwxr-xr-x) stay in sync. Every representation is editable and drives the others. Runs entirely in your browser, no server, no tracking, no external dependencies.

## Live demo

https://0xelitesystem.github.io/chmod-calculator/

## Features

- A 3x3 checkbox grid (read / write / execute for owner / group / other) that live-syncs with the octal and symbolic values.
- All three representations are editable: check boxes, type an octal value, or type a symbolic string, and the other two update.
- Special bits supported as a leading fourth octal digit: setuid (4000), setgid (2000), and the sticky bit (1000). These render correctly as s, S, t, and T in the symbolic string.
- The exact `chmod` command with a one-click copy button.
- An info panel explaining what each permission means for files and for directories.
- Common presets: 644, 755, 600, 700, 664, 777, 1777, and 4755.
- A clear warning that 777 is unsafe, plus a nudge when group or other has more access than the owner.
- Accepts symbolic strings pasted from `ls -l` (the leading file-type character is dropped automatically).
- Light and dark themes, keyboard usable.

## How it works

Each permission class (owner, group, other) is one octal digit from 0 to 7, built from read (4), write (2), and execute (1). The special bits form a fourth leading digit from setuid (4), setgid (2), and sticky (1). The symbolic string is three triads of r/w/x, with the execute slot showing s or S (setuid / setgid) or t or T (sticky) when the matching special bit is set. Editing any field reparses it into the same internal state and re-renders every other field.

## Privacy

Everything runs client-side in your browser. Nothing you type is sent anywhere. There are no network requests, no analytics, and no external dependencies. Check the page source or your browser network tab to confirm.

## More

Part of a catalog of single-file browser tools and plain-language references, all MIT licensed and dependency-free: [0xelitesystem.github.io](https://0xelitesystem.github.io/). Built by [elitesystem.ai](https://elitesystem.ai).

## License

MIT. Copyright 0xelitesystem 2026.
