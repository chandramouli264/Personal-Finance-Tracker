# Personal Finance Tracker

Responsive web app for logging daily income and expenses. The balance, totals and category
breakdown update instantly as entries are added or removed. Data is saved in the browser
(localStorage), so it survives page reloads. No build step or backend needed.

**Stack:** HTML, CSS, JavaScript (ES modules)

## Features
- Add income and expense transactions with description, amount, category and date
- Live balance, total income and total expenses
- "Where your money goes" bar chart by expense category
- Filter by type (all / income / expenses) and by month; delete single or all transactions
- Input validation with inline error messages; keyboard accessible; light and dark mode

## Run
ES modules need a web server (opening the file directly will not work):
```bash
python3 -m http.server 8000     # then open http://localhost:8000
```
Or use the VS Code "Live Server" extension.

## Test (Node 18+)
```bash
npm test        # or: node --test
```

## Structure
```
index.html        page markup
css/style.css     responsive styles
js/ledger.js      pure logic: validation, totals, category breakdown, filters
js/app.js         DOM and localStorage wiring
tests/            unit tests for ledger.js
```

## Deploy
Static site: host on GitHub Pages, Netlify or Vercel by pointing it at this folder.
