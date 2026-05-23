# Telesales Training 🎯

A Kahoot-style, cartoon-playful sales training quiz platform — static, no backend needed!

## 🎨 New in v2

- **Kahoot-style UI** — Colorful, cartoon, playful design with Fredoka One font, bouncy buttons, floating stars, animated blobs
- **Delete Quiz** — Admin can delete any published quiz from the Published Trainings panel
- **Delete Question** — Admin can delete questions from the builder (with confirm dialog)
- **Points per Question** — Set custom point value (10–1000) for each question when adding it
- **Change Admin Password** — Admin can change the security password from a secure modal (browser-local override). Permanent change can be done in code (see below)
- **CSV Report Download** — Download full employee report per quiz with completion status, score, timestamps
- **Confetti & Animations** — Confetti on publish and on quiz completion
- **Circular Timer** — Animated SVG ring timer during quiz
- **Sound Effects** — Toggleable audio feedback

## 🔐 Admin Login

- **Admin ID:** `Rahul_Sinha`
- **Default Password:** `Delhi@1234`

### To permanently change the password in code:
1. Open `index.html`
2. Find this line near the top of the `<script>` section:
   ```js
   const ADMIN_PASSWORD_DEFAULT = "Delhi@1234";
   ```
3. Change the value to your new password.

### To change via the app (browser-local):
1. Go to Admin panel → click **"🔑 Change Security Password"** below the login form
2. Enter current password, new password, confirm
3. This stores the override in `localStorage` — clears if browser data is cleared

## 🚀 Deploy to Vercel

1. Push this folder to GitHub
2. Import the repo in Vercel
3. No build command needed — it's plain HTML/CSS/JS

## 💻 Run Locally

```bash
npm start
```

Then open `http://127.0.0.1:4173`

## 📋 Features

- Admin-only training builder with question management
- Custom points per question (10–1000 pts)
- Delete questions and delete published quizzes
- Publish training as a shareable URL with room code
- Activate / Deactivate published trainings
- Download CSV report per quiz
- Employee code: exactly 6 numeric digits
- Employee name: max 40 characters
- Player limit: 1–100
- Browser sound effects (toggleable)
- Confetti on success events
- Animated circular countdown timer
- All data stored in browser localStorage (no backend)

## ⚠️ Static App Note

Player data, reports, and quizzes are stored in the browser. For cross-device sync, integrate Supabase, Firebase, or Vercel KV.
