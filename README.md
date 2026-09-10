# RMD Calculator

A free, single-file Required Minimum Distribution (RMD) calculator for retirement plan participants — active, terminated, and deceased. Built to the SECURE 2.0 applicable ages and the July 2024 final regulations under IRC §401(a)(9).

Runs entirely in the browser. Nothing entered is transmitted, logged, or stored anywhere.

## Live demo

Once GitHub Pages is enabled for this repo (Settings → Pages → Deploy from branch `main` / root), the calculator will be live at:

```
https://<your-github-username>.github.io/RMD-Calculator/
```

## What's included

Three calculator tabs, plus a reference tab:

1. **Active & Terminated Participants** — Uniform Lifetime (Table III) or Joint Life (Table II), auto Required Beginning Date (RBD), still-working exception, marital status.
2. **Deceased — Not Segregated** — up to 10 beneficiaries sharing one combined balance split by designated percentage, Table I (Single Life Expectancy), per-beneficiary breakdown.
3. **Deceased — Segregated** — for a single beneficiary whose share has already been split into their own separate inherited account; enter that one beneficiary's own information and their own actual balance.
4. **Rules & Guidance** — plain-language reference on applicable ages, the 10-year rule, and other traps.

**Every calculation shows its work.** After you calculate, the results include which IRS table and formula were used, why (based on your inputs — beneficiary classification, RBD status, account type), and the specific IRC section or Treasury Regulation citation behind that treatment. This is deliberately most detailed on the deceased-participant tabs, where the rules (EDB / NEDB / NDB classification, the 10-year rule, the 5-year rule, spousal elections) are the most consequential to get right.

This build is the pure calculator — no company or "about us" content.

## Features

- Add any number of RMD years individually, per tab
- Comma-formatted currency inputs
- Expandable/collapsible per-year results
- Generate a printable report (PDF via the browser's print dialog)
- Mobile responsive
- Full legal disclaimer, always visible

## Local use

No build step. Open `index.html` directly in any modern browser, or serve the folder with any static file server.

## Disclaimer

This calculator provides **estimates only**, based on user-provided inputs and IRS life expectancy tables. It is not a substitute for professional tax or legal advice. See the in-app disclaimer for full terms.
