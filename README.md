# Railway Ready Telegram Bot

## Files
- `updatefilev7.py` - Main bot application
- `requirements.txt` - Python dependencies
- `railway.toml` - Railway deployment configuration

## Railway Variables
Add these variables in Railway:

- `BOT_TOKEN` = Your Telegram Bot Token
- `ADMIN_IDS` = Your Telegram numeric user ID (multiple IDs can be comma-separated)
- `AUTO_PAYMENT_ENABLED` = `true` or `false`
- `PAYMENT_WEBHOOK_SECRET` = A long random secret if you use the payment webhook
- `PAYMENT_WEBHOOK_HOST` = `0.0.0.0`
- `DB_FILE` = `/data/store.db` (recommended when using a Railway Volume)
- `UPLOAD_DIR` = `/data/product_files` (recommended when using a Railway Volume)

## Railway Volume
If you want the SQLite database and uploaded product files to survive redeployments:
1. Add a Railway Volume mounted at `/data`.
2. Set `DB_FILE=/data/store.db`.
3. Set `UPLOAD_DIR=/data/product_files`.

## Start command
The project automatically uses:

`python updatefilev7.py`
