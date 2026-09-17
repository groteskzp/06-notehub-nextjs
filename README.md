# NoteHub (Next.js)

GoIT homework **06-notehub-nextjs**. NoteHub is a multi-page notes app built with the Next.js App Router. It talks to the public NoteHub API so you can keep personal notes in one place: browse a list, search by keyword, create a note with a tag, delete a note, and open a dedicated details page.

## Live demo

Not available.

## Features

- Home page (`/`) with a short description of NoteHub
- Shared layout with Header (Home, Notes) and Footer on every route
- Notes page (`/notes`) with a paginated list (12 notes per page)
- Keyword search with a 300 ms debounce; pagination resets to page 1 on a new search
- Pagination controls appear when there is more than one page
- Create a note in a modal form: title, content, and tag (`Todo`, `Work`, `Personal`, `Meeting`, `Shopping`)
- Form validation with Formik and Yup (title 3–50 characters, content up to 500 characters, tag required)
- Delete a note from the list
- Note details page (`/notes/[id]`) with title, tag, content, and creation date
- Server-side prefetch of the notes list and a single note, hydrated into TanStack Query on the client
- Loading UI (`app/loading.tsx`) and route error UI for `/notes` and `/notes/[id]`
- Modal closes on Escape, backdrop click, or Cancel
- HTTP client in `lib/api.ts` (Axios) against `https://notehub-public.goit.study/api`

## Tech stack

- Next.js (App Router) and React
- TypeScript
- CSS Modules
- TanStack Query
- Axios
- Formik and Yup
- react-paginate
- use-debounce


## Getting started

1. Clone the repository:

   ```bash
   git clone https://github.com/groteskzp/06-notehub-nextjs.git
   cd 06-notehub-nextjs
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Create a `.env` file in the project root and add your NoteHub API token:

   ```bash
   NEXT_PUBLIC_NOTEHUB_TOKEN=your_token_here
   ```

4. Start the development server:

   ```bash
   npm run dev
   ```

5. Open [http://localhost:3000](http://localhost:3000) in the browser.

## Scripts

| Script | Description |
| --- | --- |
| `npm run dev` | Start the Next.js development server |
| `npm run build` | Create a production build |
| `npm run start` | Start the production server |
| `npm run lint` | Run ESLint |
