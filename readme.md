## Spotify Clone (MERN)

A full-stack music streaming app inspired by Spotify. Users can sign up, upload tracks, create playlists, like songs, and stream audio with a responsive UI and real-time player controls.

## ✨ Features

- Email/password auth with JWT

- Upload songs (MP3/WAV) + cover art

- Stream audio with play/pause/seek/queue/shuffle/repeat

- Playlists (create, edit, reorder), likes/favorites

- Search by track/artist/album

- Follow/unfollow artists (optional)

- Mobile-first responsive UI

- Dark theme

- Role-based admin panel (manage songs & users)

## 🧰 Tech Stack

- Frontend: React, Vite, React Router, Redux Toolkit (or Zustand), Tailwind CSS, React Query (optional), Howler.js (or HTMLAudio)

- Backend: Node.js, Express.js, MongoDB + Mongoose, Multer (uploads), Cloudinary/AWS S3 (storage)

## 🗂 Folder Structure

- Auth: JWT (access + refresh)
- Other: ESLint + Prettier, Vitest/Jest (tests), Docker (optional)
spotify-clone/
├─ client/              # React app
│  ├─ src/
│  │  ├─ components/    # UI components (Player, SongCard, Sidebar, etc.)
│  │  ├─ features/      # Redux slices or Zustand stores
│  │  ├─ pages/         # Route components
│  │  ├─ services/      # API clients, hooks
│  │  ├─ utils/         # helpers
│  │  └─ main.tsx
│  └─ index.html
├─ server/              # Express API
│  ├─ src/
│  │  ├─ config/        # db, cloudinary, env
│  │  ├─ controllers/   # route handlers
│  │  ├─ middleware/    # auth, error, upload
│  │  ├─ models/        # User, Song, Playlist, Artist
│  │  ├─ routes/        # /auth /songs /playlists /users
│  │  └─ app.ts
│  └─ server.ts
├─ .env                 # root (optional)
├─ README.md
└─ package.json         # (optional monorepo scripts)

🚀 Quick Start
1) Prerequisites

Node.js 18+

MongoDB (local or Atlas)

Cloud storage (Cloudinary or S3) for audio & images

2) Clone
https://github.com/princekumar9234/Spotify-clone.git
cd spotify-clone

## 🔑 Authentication

1. Register → /api/auth/register

2. Login → /api/auth/login

3. Uses access + refresh tokens (HTTP-only cookies or Authorization header).

4. Protected routes require auth middleware.

## 💾 Uploads & Streaming

- Upload via Multer ➜ store to Cloudinary/S3, keep file URLs in MongoDB.

- Streaming via signed URL or public URL + range requests from the server.

- Player uses Howler.js or the HTML <audio> element for controls & progress.

## 🔒 Security Notes

- Store JWT refresh tokens in HTTP-only cookies if possible.

- Validate audio/image MIME types & size limits.

- Sanitize search input to prevent injection.

- Use CORS allowlist for CLIENT_URL.

## 🧭 Roadmap

- Social sharing & collaborative playlists

- Lyrics display & sync

- Real-time activity feed (WebSockets)

- Offline caching (service worker)

- Internationalization (i18n)

## 🛠 Troubleshooting

- CORS error → check CLIENT_URL and CORS config.

- Audio won’t play on mobile → user gesture required; start playback on button click.

- Uploads fail → verify Cloudinary/S3 credentials and bucket permissions.

- Streams cut off → implement HTTP range requests or stream from provider.

## 📦 Deployment

- Server: Render, Railway, Fly.io, or VPS + PM2

- Client: Netlify, Vercel, or static hosting

- Env: set CLIENT_URL to your deployed frontend and allow it in CORS

## 🤝 Contributing

- Fork the repo

- Create a feature branch: git checkout -b feat/amazing

- Commit: git commit -m "feat: add amazing thing"

- Push: git push origin feat/amazing

- Open a Pull Request

## 📄 License

MIT © [prince kumar]

## 🙌 Acknowledgements

- Spotify for inspiration (this project is not affiliated)

- Howler.js / Tailwind / React community

## Replace-me Checklist ✅

1.  Repo name, links, author

2. Env values (MONGO_URI, Cloud storage, JWT secrets)
