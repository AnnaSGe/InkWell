# Inkwell

A personal journaling and smart note-taking web application built for expressive writing, multimedia note creation, and intelligent knowledge organization.

---

## Features

### Authentication

- Email/password sign-up and login via Supabase Auth
- Personalized dashboard with real-time note sync
- Session-based access with user profile management

### Rich Note Editor

- Block-based editor supporting text, checklists, images, audio, and drawings — all in one note
- Italic serif title input with auto-expanding layout
- Auto-save with save status indicators (saving / saved)
- Sticky editor toolbar and distraction-free writing interface

### Smart Note Dashboard

- Note preview cards with last-modified timestamps
- Pin important notes to the top of the grid
- Full-text search across titles and note content
- Media type badges (image, audio, drawing, checklist, links) on each card
- Responsive grid layout, mobile-friendly

### Checklists

- Add, remove, and check off tasks inline within notes
- Progress bar tracking completion percentage
- Keyboard shortcuts: Enter to add item, Backspace on empty item to remove

### Multimedia Notes

**Images** — <img width="954" height="355" alt="image" src="https://github.com/user-attachments/assets/c64a0b4f-e229-4e75-90f9-8f9d77169caa" />

**Audio** — <img width="959" height="227" alt="image" src="https://github.com/user-attachments/assets/18b80061-4977-4875-b712-24ac5f28d90a" />


**Drawing** —  <img width="959" height="279" alt="image" src="https://github.com/user-attachments/assets/8763ada6-16e4-43c0-aa7a-e4afc1c0990c" />


All media is uploaded to Supabase Storage with a 5MB limit per file. Signed URLs are cached client-side and refreshed automatically before expiry.

### AI Writing Assistant

Powered by the LanguageTool API. Modes include grammar check, text cleanup, word simplification, and formal tone adjustment. Suggestions can be applied to all text blocks in the note or discarded.

<img width="952" height="253" alt="image" src="https://github.com/user-attachments/assets/a421b5da-7438-490d-9fbc-c746209d673a" />

### Linked Notes

Link related notes together via a search-and-select modal. Links are displayed inline in the editor and navigable with one click. Unlinking is non-destructive.

### Knowledge Graph View

An SVG-based force-directed graph that visualizes note relationships. Nodes are sized by block count and colored by type (text-only, media, linked). Supports pan, scroll-to-zoom, and click-to-open. Handles up to 50 nodes.

<img width="959" height="374" alt="image" src="https://github.com/user-attachments/assets/1781b7f1-2703-43e5-83b7-111ff408f7f4" />


### Activity Heatmap

GitHub-style contribution heatmap on the profile page, built from per-session writing duration logs stored in Supabase. Shows the last 52 weeks of activity with color intensity scaled to time written.

<img width="440" height="217" alt="image" src="https://github.com/user-attachments/assets/32db7909-a3a0-4f74-97fb-4916af79833f" />

### Theme Support

Light and dark mode with smooth CSS variable transitions. Theme preference is persisted to `localStorage`.

---

## Tech Stack

| Layer | Technologies |
|---|---|
| Frontend | HTML5, CSS3, React 18 (via CDN), Babel |
| Backend / Database | Supabase (Postgres + Auth + Storage) |
| APIs | Canvas API, Web Audio API, LanguageTool API |
| File handling | Drag-and-drop, clipboard paste, signed URL cache |

---

## Project Structure

```
Inkwell/
├── index.html          
├── media/
└── README.md
```

---

## Getting Started

No build step required. The project uses React and Babel via CDN.

```bash
git clone https://github.com/AnnaSGe/inkwell.git
cd inkwell
open index.html
```

To use the full app, you'll need a Supabase project with:
- A `notes` table (columns: `id`, `user_id`, `title`, `blocks`, `pinned`, `created_at`, `updated_at`)
- An `activity_logs` table (columns: `id`, `user_id`, `date`, `duration`)
- A storage bucket named `note-media`

Update `SUPABASE_URL` and `SUPABASE_ANON` at the top of `index.html` with your project credentials.

---

## Roadmap

- AI mood analysis and sentiment tracking
- Calendar journal view
- PDF export
- Reminders and notifications
- Speech-to-text journaling
- Collaborative notes

---

## Developed By

**Anna** 
