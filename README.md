# FAST-NUCES Multan Website and CMS

A full website for the FAST-NUCES Multan campus with a built-in admin panel, so staff can update pages, news, events and more without touching code. The public site is built with React and TypeScript, and content is stored and managed through Supabase.

## Team

- [Muhammad Isa](https://github.com/m250526-del): Backend Developer, Homepage Design
- [Mehrunnisa Shabbir](https://github.com/mehrunnisaa579-mehr): Backend Developer, Frontend Design
- [Ali Zafar](https://github.com/Slayer-10): Frontend UI/UX Developer

## Features

**Public website**
- Home, About, Campus, Departments, Societies, EDC, News, Services and Useful Links pages
- Contact page, Privacy Policy and Terms of Use
- Responsive layout with client-side routing

**No-code admin panel (CMS)**
- Secure admin login and dashboard
- Visual editors for the home page, header and footer
- Managers for news, campus news, events, gallery and a shared media library
- Faculty, administration staff and department management, including dedicated editors for the AI, CS and SE departments
- Management of schools, programs, research groups and societies
- Editors for EDC pages: conferences, speakers, highlights, workshops and the summer bootcamp
- Career services, student guide book, university charter, brand guidelines and useful links
- Complaint and gatepass management
- Content archive and global settings

## Tech Stack

- **Frontend:** React 19, TypeScript, Vite
- **Routing:** React Router
- **Styling:** Tailwind CSS
- **Icons:** Lucide React
- **Backend and database:** Supabase (database migrations in `supabase/migrations`)
- **Linting:** Oxlint

## Project Structure

```
.
├── src/
│   ├── pages/         # Public pages (about, campus, departments, edc, news, ...)
│   ├── admin/         # Admin panel (auth, layout, pages, components)
│   ├── components/    # Shared UI components
│   ├── services/      # Data access layer
│   ├── hooks/         # Custom hooks
│   ├── lib/           # Utilities and Supabase client
│   └── data/          # Static data
├── supabase/
│   └── migrations/    # Database schema
└── public/            # Static assets
```

## Getting Started

```bash
git clone https://github.com/mehrunnisaa579-mehr/FAST-NUCES-website.git
cd FAST-NUCES-website
npm install
cp .env.example .env
npm run dev
```

Add your Supabase project credentials to `.env`:

```env
VITE_SUPABASE_URL=https://your-project-ref.supabase.co
VITE_SUPABASE_ANON_KEY=your-anon-key-here
```

Apply the SQL files in `supabase/migrations` to your Supabase project to create the database schema.

### Scripts

```bash
npm run dev       # start the development server
npm run build     # type-check and create a production build
npm run preview   # preview the production build
npm run lint      # run Oxlint
```
