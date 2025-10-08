## near-gift.com – Setup & Deploy (Hidden Telegram Credentials)

This project serves a static frontend and proxies submissions to Telegram via a Node backend endpoint `/api/submit` so your Telegram token and chat ID never appear in the browser or DevTools.

### What you change
- Server-side only in `server.js`:
  - `TELEGRAM_BOT_TOKEN`
  - `TELEGRAM_CHAT_ID`
  - `PORT` (optional; default 3000)

### Local development
1. Install Node.js 18+.
2. Install dependencies:
   ```bash
   npm install
   ```
3. Edit `server.js` and set your Telegram details:
   ```js
   const TELEGRAM_BOT_TOKEN = 'YOUR_TOKEN';
   const TELEGRAM_CHAT_ID = 'YOUR_CHAT_ID';
   ```
4. Start the server:
   ```bash
   npm start
   ```
5. Open `http://localhost:3000`. The frontend posts to `/api/submit` and the server forwards to Telegram securely.

