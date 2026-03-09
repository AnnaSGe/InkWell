# InkWell – Personal Journal App

InkWell is a lightweight offline-first journaling application that allows users to capture thoughts using text, images, audio recordings, and drawings in a block-based editor.

The app runs entirely in the browser and stores data locally using browser localStorage, meaning no backend or database setup is required.

## Features

• Block-based note editor
• Text, image, audio, and drawing blocks
• Autosave journaling interface
• Pin important notes
• Search notes instantly
• Dark and light mode
• Export notes to CSV (Excel compatible)
• Offline-first design with no internet required

## Tech Stack

React (via CDN)
JavaScript
HTML + CSS
Browser LocalStorage

All media (images, audio, drawings) are stored as base64 data directly in the browser.

## How It Works

The application stores all journal data in the browser using a single localStorage object.

Example structure:

```
inkwell-demo
 ├ user
 ├ notes[]
 └ nextId
```

Each note uses a block-based structure similar to modern editors:

```
{
  id,
  title,
  blocks: [
    { type: "text" },
    { type: "image" },
    { type: "audio" },
    { type: "drawing" }
  ],
  createdAt,
  updatedAt
}
```

## Running the App

1. Download or clone the repository
2. Open `index.html` in any modern browser

No installation or dependencies required.

## Exporting Data

Users can export their notes from the Profile page.

The export feature generates a CSV file that can be opened in:

• Microsoft Excel
• Google Sheets
• LibreOffice

## Screenshots

(Add screenshots here after uploading them)

Dashboard
Note Editor
Drawing Canvas
Profile Page

## Future Improvements

• Calendar view for journal entries
• Tagging and categories
• Markdown support
• Image compression for large media files
• Optional cloud sync

## License

MIT License
