# AIConnect Bootcamp — Task Board

A small, working task board used as the live demo for the **AIConnect Bootcamp on AI-Driven Development** at **Iloilo Science and Technology University**, on **October 24, 2026**.

**Live demo:** https://task-board.chof64-366.workers.dev  
**Source:** https://github.com/chof64/task-board

## What this demo shows

The app is intentionally small enough to understand and extend during a hands-on session:

- Create tasks and move them between **To do**, **In progress**, and **Completed**
- Drag and drop cards between workflow columns
- Archive tasks, restore them, or permanently delete them
- View task counts and use a responsive layout
- Keep task data in the browser with `localStorage`

This is a front-end demo, not a multi-user task service. Tasks are saved in the current browser on the current device; there is no server-side database or sign-in.

## Run locally

Requirements: Node.js and npm.

```bash
npm install
npm run dev
```

Wrangler will show a local URL in the terminal. Open it in your browser.

## Deploy to Cloudflare Workers

1. Authenticate with Cloudflare:

   ```bash
   npx wrangler login
   ```

2. Deploy:

   ```bash
   npm run deploy
   ```

The project is configured in `wrangler.toml` and serves the HTML app from `src/index.js`.

## A suggested AI-Driven Development exercise

1. **Describe the outcome:** Ask an AI coding assistant to add one useful feature, such as task priorities, due dates, or filtering.
2. **Inspect before changing:** Have the assistant explain the current structure and identify the smallest safe change.
3. **Implement in small steps:** Request a focused change rather than a complete rewrite.
4. **Verify:** Test creating, moving, archiving, restoring, and deleting tasks after each change.
5. **Review:** Ask the assistant to explain the code it changed, edge cases, and what should be tested next.
6. **Ship responsibly:** Review the diff, commit the change, and deploy only after testing.

AI-generated code should still be reviewed and tested. Avoid placing secrets, credentials, or personal information into prompts or this demo repository.

## Project structure

```text
.
├── src/
│   └── index.js      # Cloudflare Worker and HTML/CSS/JavaScript app
├── package.json      # Local development and deployment scripts
├── wrangler.toml     # Cloudflare Workers configuration
└── README.md
```

## License

No license has been specified yet. Ask the repository owner before reusing this project beyond the bootcamp.
