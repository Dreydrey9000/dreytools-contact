# dreytools-contact

Chat-app style contact form for drey tools — iMessage vibe, mobile-first.

**Live:** https://contact.dreytools.com
**CF project:** `dreytools-contact`

## What it is

Single-file HTML that feels like opening an iMessage thread with Drey.

- Sticky chat header with pulsing "online" dot and 24h response note
- Two incoming bubbles from Drey greeting the visitor
- Live-preview outgoing bubble that updates as user types
- Topic chips (General / Build-Collab / 1BB / Music / Hire)
- Composer with name+email and auto-grow textarea
- Circular cyan send button (disabled until valid)
- After send: typing indicator + auto-reply bubble
- Submits via `mailto:` to `dreydrey9000@gmail.com`

## Mobile-first

- `100dvh` + env safe-area insets for notch/home bar
- `max-width: 540px`, fills phone screen, centered on desktop
- iOS 16px inputs (blocks zoom-on-focus)
- `overscroll-behavior: none`
- Sticky composer with `backdrop-filter`
- Horizontal-scroll chip row

## Deploy

```bash
wrangler pages deploy . --project-name dreytools-contact --branch main
```

## Future upgrade

Wire a CF Worker + Resend for direct email send (skip the mailto step).
