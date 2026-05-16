# 💰 PaisaTrack — Personal Expense Tracker

A minimal, aesthetic expense tracker in INR (₹) running on localhost.

## Setup & Run

```bash
# 1. Install Flask
pip install flask

# 2. Run the app
python app.py

# 3. Open in browser
# http://localhost:5000
```

## Features

- ✅ **Add Money** — Log income (salary, freelance, etc.)
- ✅ **Add Expense** — Enter what you spent & it auto-deducts from balance
- ✅ **Monthly Transactions** — All transactions grouped by current month
- ✅ **Monthly Totals** — See total spent vs. added this month
- ✅ **Delete Transactions** — Undo/remove any entry (balance auto-adjusts)
- ✅ **Keyboard Shortcuts** — Tab + Enter to navigate, Esc to close modal
- ✅ **Persistent Storage** — SQLite database (`expenses.db` auto-created)

## File Structure

```
expense-tracker/
├── app.py              # Flask backend
├── requirements.txt    # Dependencies
├── expenses.db         # Auto-created on first run
└── templates/
    └── index.html      # Frontend
```

## Reset Database

If you want to clear all your transactions and reset your balance to zero, you can run the following command in your terminal while in the project directory:

```bash
python -c "import sqlite3; conn = sqlite3.connect('expenses.db'); conn.execute('DELETE FROM transactions'); conn.execute('UPDATE balance SET amount = 0'); conn.commit(); conn.close(); print('Database cleared successfully.')"
```

Alternatively, you can simply delete the `expenses.db` file. The application will automatically recreate an empty database the next time you start it.
