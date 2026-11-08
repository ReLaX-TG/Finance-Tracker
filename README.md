# Finance Tracker

A personal finance dashboard built with HTML, CSS, and JavaScript. Track income and expenses, plan budgets, and keep your data in your own browser.

**Status: beta.** Keep regular JSON backups, especially before updating the app or moving it to another browser or address.

## BETA TEST : https://relax-tg.github.io/Finance-Tracker/

## Features

- Add, edit, delete, and repeat transactions with categories, dates, and descriptions.
- Search, sort, and filter transaction history; view totals for the selected records.
- Export filtered transactions to CSV.
- Review monthly statistics, balance charts, and month comparisons.
- Set monthly and category budgets, and track savings goals separately from your balance.
- Manage recurring transaction templates and view upcoming payments. Entries require manual confirmation; the app does not make bank payments.
- Export and import JSON backups, and review a local change history.
- Choose English, Ukrainian, or Polish and four visual themes.
- Hide displayed amounts with the balance visibility control.
- Use a separate currency converter with NBP exchange rates and a dated cache fallback.

## Getting started

1. Download the project and keep its files together.
2. Open `index.html` in a modern browser with Web Locks support, such as Chrome or Edge.
3. Add a transaction and create your first JSON backup from the backup section.

There is no build step or backend to install. You can also serve the app over HTTPS or on localhost. Web Locks must be available in the browser context; if startup is blocked, use a supported browser and a secure origin.

Only one active app tab is allowed for the same browser origin. Close the active tab before retrying in another tab.

## Data and backups

Financial data is saved in browser `localStorage`, not inside the HTML file. There is no account or automatic cloud sync. Different browsers, profiles, or app addresses can have separate storage. Clearing site data can erase your records.

Use JSON backups to preserve or transfer your data. They include transactions and supported settings such as budgets, goals, recurring templates, custom categories, and the retained change history. CSV is a transaction export, not a full backup.

Export a JSON backup before replacing the app file or switching to a hosted copy. Keep the original backup until you have checked the imported records and totals.

Backups and CSV exports contain readable financial information. The visibility control only hides amounts on screen; it does not encrypt stored data or exported files. The change history is local and is not a tamper-proof audit trail.

## Currencies

The main currency setting changes the displayed currency label. It does **not** convert existing balances or create a multi-currency ledger.

The separate converter uses [National Bank of Poland (NBP) API](https://api.nbp.pl/) Table A average rates, with PLN as the reference currency. Conversion is calculated locally. The result shows the rate date and whether cached data was used. These reference rates may differ from rates offered by banks or exchange services.

## Languages and themes

English is the default interface language for a new setup; saved language preferences take precedence. Ukrainian and Polish are also available. User-entered descriptions and existing saved category names are not automatically translated.

Themes include dark teal, coral, olive, and graphite with violet accents. Theme changes do not change financial records.

## Current limitations

- Beta software: full cross-browser and real-device testing is still pending.
- Browser storage is local and can be cleared; downloaded backups remain essential.
- Single-tab protection applies to cooperating app tabs on the same origin, not different browsers or profiles.
- Recurring transactions require user action and are not background bank instructions.
- Savings goals are tracked separately and do not automatically adjust the transaction balance.
- Exchange-rate updates require internet access; cached rates may be older than the calculation date.

## Project files

```text
index.html    Application
README.md     Project overview and usage
LICENSE       MIT license
.gitignore    Excludes common local and private files
```

## Feedback

When reporting a problem, include your browser, the steps to reproduce it, and the expected result. Use fictional transactions in examples and remove personal information from screenshots. Do not attach personal JSON backups to public issues.

## License

[MIT](LICENSE) — Copyright (c) 2026 [ReLaX-TG](https://github.com/ReLaX-TG).
