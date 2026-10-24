# Task Board

A lightweight, browser-based task board deployed on Cloudflare Workers.

## Features

- Create tasks with a required title and optional description
- Drag tasks between **To do**, **In progress**, and **Completed** columns
- Archive tasks to keep the active board uncluttered
- Restore archived tasks or permanently delete them
- Responsive layout and task-count summaries
- Stores tasks in the browser's `localStorage`; no authentication or external API is required

## Run locally

This is a Cloudflare Worker that serves the HTML app directly from `src/index.js`.

1. Install Node.js and npm.
2. Install Wrangler:

   ```sh
   npm install
   ```

3. Start a local development server:

   ```sh
   npm run dev
   ```

## Deploy

Authenticate with Cloudflare, then run:

```sh
npm run deploy
```

Tasks are stored per browser and device, not in a server-side database. Clearing browser storage removes locally saved tasks.
