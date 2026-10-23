# CareerConnect local site

This folder contains the CareerConnect website from the supplied CEP project ZIP, served with a small Node.js backend and no third-party packages.

## Run it

1. Install Node.js 18 or newer if it is not already installed.
2. Open a terminal in this folder.
3. Run `node server.js`.
4. Open `http://127.0.0.1:3000` in a browser.

The backend binds to the local computer only. It writes account records, saved careers, saved opportunities, and signed-in quiz reflections to `data/store.json`. Passwords are stored as salted scrypt hashes. Sessions are held in memory and end when the server restarts.

## Connected sections

- Home page featured careers and scholarship search
- Career explorer, fields, career details, pathway steps and official resources
- Class 10, 11 and 12 career reflection quiz and ranked career ideas
- Sign up, log in, saved careers, saved opportunities and quiz history
- Official scholarship and education resource links

The scholarship information is a set of links and summaries for discovery, not an eligibility decision. Confirm current requirements with each official portal. The site is a student project prototype: it is not configured for public deployment or production account security. Do not use real passwords or sensitive personal information.

## API overview

- `GET /api/careers`, `GET /api/careers/:slug`
- `GET /api/categories`, `GET /api/pathways?grade=10|11|12`
- `GET /api/scholarships`, `GET /api/resources`
- `GET /api/quiz/questions`, `POST /api/quiz`
- `POST /api/auth/register`, `POST /api/auth/login`, `POST /api/auth/logout`, `GET /api/me`
- `GET|POST|DELETE /api/saved/careers[/:slug]`
- `GET|POST|DELETE /api/saved/scholarships[/:id]`
