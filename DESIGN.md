# TV Server design

Made with the Website Design process (web-design-system), 2026-10-21. UXKIN wasn't reachable from the build session, so this direction comes from the project itself (logo, ghazi's Glance dashboard) and the process rules, not from real example sites.

**Who it's for:** friends and family ghazi invites, opening tvserver.homes off the VPN. **Feeling:** calm, private, a bit technical. Like a real product's sign-in page, not a homelab hobby page.

**Theme:** dark only. Visitors land on the dark Glance dashboard right after this page, so the two feel like one place.

## Color

| Token | Value | Role |
|---|---|---|
| `--bg` | `#0E0F14` | Page background |
| `--surface` | `#15161D` | Panels (status, steps, form) |
| `--surface-2` | `#1C1E27` | Inputs, selects, step numbers |
| `--border` | `#2A2C38` | Lines between and around things |
| `--text` | `#ECEDF2` | Headings and body |
| `--text-muted` | `#A6A8B6` | Supporting text (8:1 on bg) |
| `--text-subtle` | `#888B98` | Small labels and the footer only, on bg or surface |
| `--primary` | `#A87CF3` | The one action color: primary button, links, focus ring, logo (6.2:1 on bg) |
| `--primary-ink` | `#16101F` | Text on primary buttons (6:1) |
| `--success` | `#4CC38A` | Sent, connected |
| `--error` | `#F0686C` | Not connected, form errors |

No gradients, no glass, no second accent.

## Typography

Geist for everything, Geist Mono for addresses, numbers and labels (Google Fonts, `display=swap`).

| Step | Size / line height | Use |
|---|---|---|
| Display | clamp(34px, 5vw, 50px) / 1.08, 600, tracking -0.02em | The one h1 |
| H2 | 24px / 1.25, 600 | Section headings |
| H3 | 17px / 1.4, 600 | Step and question titles |
| Body | 16px / 1.6, 400 | Everything else; max 64ch |
| Lead | 18px / 1.55, 400 | Hero support line |
| Small | 14px / 1.5 | Tips, footer, form messages |
| Label | 12px / 1.4 mono, uppercase, tracking 0.08em | Section eyebrows, field labels |

## Spacing

4-based scale: 4, 8, 12, 16, 24, 32, 48, 64, 96. Sections are 96px apart on desktop, 64px on phones. Content width 1120px, side gutter 16px on phones, 32px from 768px.

## Shape and depth

Radius: 8px for buttons and inputs, 14px for panels, 999px for the status pill. No shadows; depth comes from surface color and 1px borders.

## Components

- **Primary button:** primary background, primary-ink text, 44px tall, 8px radius. Hover brightens 8%. Focus: 2px primary ring, 2px offset. Disabled: 60% opacity, progress cursor.
- **Quiet link:** primary text, underline on hover.
- **Input / select:** surface-2 background, border, 44px tall, visible mono label above. Focus: primary border plus ring.
- **Panel:** surface, border, 14px radius, 24px padding. Used for the status card and the device steps only, not for every block.
- **Status pill:** mono, 12px, dot plus "Not connected" in error color.
- **Steps:** numbered with mono numbers, separated by top borders, laid out in a row on desktop. Not cards.
- **Header:** logo + "TV Server" left, status pill right. **Footer:** one line, small, subtle.

## Imagery and icons

The TV logo (logo.svg) is the only mark. Icons are simple 1.6px-stroke line icons drawn inline, in currentColor. The hero visual is a plain diagram of the real path (your device, NetBird, TV Server) with the missing link shown. No stock art, no emoji.
