# RMD Calculator — SECURE 2.0 Compliant

A free Required Minimum Distribution (RMD) calculator for US retirement plan participants and beneficiaries: active, terminated and deceased. It is built to the SECURE 2.0 applicable ages and the **final regulations of 19 July 2024** under IRC §401(a)(9).

It is one self-contained `index.html` file. There is no build step, server, or tracking. **Everything runs in your browser, and nothing you enter is sent, logged or stored anywhere.**

**Live site:** https://sxcs1991.github.io/RMD-Calculator-Site-SECURE-2.0-Compliant/

---

## Why another RMD calculator?

Many RMD calculators were written between the 2019 SECURE Act and the 2024 final regulations, and have not been updated since. Common errors in those tools:

| Common error | What this calculator does |
|---|---|
| Treats every 10-year-rule beneficiary the same | Checks whether the participant died **before or on/after the Required Beginning Date**. After a post-RBD death, a Non-Eligible Designated Beneficiary owes annual RMDs in years 1–9 **and** must empty the account by year 10 |
| Uses one RMD age for everyone | Uses the full SECURE 2.0 age ladder by date of birth: 70½ / 72 / 73 / 75. This includes the mid-1949 cut-off and the 1959 birth year (age 73) |
| Sets the RBD to 1 April of the year the age is reached | Sets the RBD to 1 April of the **following** year, and flags the year when two RMDs fall due |
| Ignores the 2021–2024 waivers | Applies the relief in Notices 2022-53, 2023-54 and 2024-35 |
| Treats any child under 21 as an Eligible Designated Beneficiary | Gives EDB status only to the **participant's own** minor child, and switches to the 10-year rule when that child turns 21 |

## What's inside

The site has four tabs:

1. **Active & Terminated.** Uses the Uniform Lifetime table (Table III), or the Joint Life table (Table II) when the spouse is the sole beneficiary and more than 10 years younger. Works out the RBD automatically and handles the still-working exception for employer plans (not available to 5% owners or IRAs).
2. **Deceased — Not Segregated.** For up to 10 beneficiaries sharing one combined balance, split by designated percentage. Uses Table I (Single Life Expectancy) and gives a breakdown per beneficiary.
3. **Deceased — Segregated.** For one beneficiary whose share is already in a separate inherited account. You enter only that beneficiary's details and balance. Minor-child, close-in-age and sole-spouse status are detected from the dates you enter.
4. **Rules & Guidance.** A plain-language reference to the rules the calculator applies, plus seven expandable in-depth guides with worked examples:
   - Does the 10-year rule require annual RMDs?
   - Is the RMD age 73 or 75?
   - Required Beginning Date: April 1 of which year?
   - Eligible vs Non-Eligible Designated Beneficiary
   - The still-working exception to RMDs
   - Year-of-death RMD: who takes it?
   - IRS RMD tables: which one applies?

### Every result shows its work

Each result lists:
- the IRS table and formula used
- the reason it applies to your inputs (beneficiary classification, RBD status, account type)
- the IRC section or Treasury Regulation behind it

These explanations are most detailed on the deceased-participant tabs. Those cases depend on EDB / NEDB / NDB classification, the 10-year and 5-year rules, and spousal elections, so mistakes there cost the most.

### Rules covered

- SECURE 2.0 §107 applicable ages and the Required Beginning Date
- The still-working exception and the 5% owner test
- No lifetime RMDs for Roth IRAs or, from 2024, designated Roth accounts (§325)
- Beneficiary classes: EDB, NEDB and NDB (including the "ghost" life expectancy rule)
- Sole-spouse options: recalculation, delayed start, and the §327 election to be treated as the participant
- The year-of-death RMD
- 2020 CARES Act waiver; 2021–2024 10-year-rule waivers; deaths before 2020 (pre-SECURE)
- Aggregation rules, and the 25% / 10% excise tax under §4974

### Features

- Add any number of RMD years on each tab
- Currency inputs formatted with commas
- Results for each year can be expanded or collapsed
- Printable report (save as PDF from the browser's print dialog)
- Works on phones and tablets
- Full disclaimer, always visible

## Using it

**Online:** open the live site linked above.

**Locally:** download or clone the repo and open `index.html` in any modern browser. It works offline.

```bash
git clone https://github.com/sxcs1991/RMD-Calculator-Site-SECURE-2.0-Compliant.git
cd RMD-Calculator-Site-SECURE-2.0-Compliant
# then open index.html, or serve the folder:
python -m http.server 8000
```

**Hosting your own copy:** in the repo go to **Settings → Pages → Deploy from a branch**, and choose `main` / `(root)`. Any static host works the same way.

## Repository layout

```
index.html    The whole application: markup, styles, IRS tables and calculation logic
README.md     This file
```

## Sources

- IRC §401(a)(9) and §4974
- Treas. Reg. §1.401(a)(9)-5 and -9 (2022 life expectancy tables)
- Final regulations, 19 July 2024
- SECURE Act (2019) and SECURE 2.0 Act (2022), §§107, 325, 327
- IRS Notices 2022-53, 2023-54 and 2024-35
- IRS Publication 590-B

Tables I and III are reproduced from Reg. §1.401(a)(9)-9. Table II is generated on the same mortality basis and was checked cell by cell against the published values for owner ages 70–80. Outside that range, a few cells may differ by up to 0.1. For a binding figure, confirm the cell against Appendix B of Publication 590-B.

## Not modelled

- QDRO alternate-payee accounts
- Successor-beneficiary schedules after a beneficiary dies
- Rollovers, Roth conversions and mid-year transfers that change the prior year-end balance
- QLACs and annuitized balances under Reg. §1.401(a)(9)-6
- Plan-specific document limits

## Disclaimer

This calculator gives **estimates only**, based on the inputs you provide and the IRS life expectancy tables. It is not legal or tax advice. Actual RMDs may differ because of plan documents, beneficiary designations, account valuations or changes in law. Check anything important against the regulations, or with a qualified tax adviser, CPA or attorney. See the in-app disclaimer for the full terms.
