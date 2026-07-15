# Dicle University Information Portal & Hospital CMS

A full-stack web application combining an academic university portal with a hospital administration system. Dicle University operates a medical faculty and teaching hospital within its campus, so this platform manages both academic and healthcare content under a unified admin dashboard.

Built with **Next.js 16 (App Router, Turbopack)**, **Prisma ORM**, **PostgreSQL**, and **NextAuth.js v5**.

---

## Features

### University Portal
- **Academic Calendar:** Dynamic term schedules and key dates.
- **Academic Units:** Faculties, vocational schools, research centers, and departments with full CRUD management.
- **Student Services:** Organized links, tools, and service pages for active students.
- **Research Hub:** Scientific centers, publication highlights, and research showcases.

### Hospital Administration
- **Polyclinics Manager:** Active clinics, emergency departments, and medical units.
- **Announcements:** Clinic-specific patient notifications and hospital-wide updates.
- **Staff Directory:** Doctor and staff profiles with contact information and avatars.

### Admin Dashboard
- **Content CMS:** Create, edit, and delete news articles, announcements, and campus events.
- **AI Chatbot:** NLP-powered virtual assistant for visitor questions.
- **PDF Menu Parser:** Extracts daily soup, main courses, and calorie information from university cafeteria PDF menus.
- **Role-Based Access:** Admin and User roles managed through NextAuth.js with audit logging.

---

## Tech Stack

| Component | Technology |
|-----------|-----------|
| Framework | Next.js 16 (Turbopack, App Router, React Server Components) |
| Database | PostgreSQL via Prisma ORM |
| Auth | NextAuth.js v5 |
| UI | TailwindCSS, Framer Motion, Lucide Icons, Radix UI |
| Rich Text | TipTap Editor |
| PDF Parsing | pdf-parse |

---

## Setup

### Prerequisites
- Node.js v18+
- PostgreSQL instance

### Installation

```bash
git clone https://github.com/serhacelik19-create/dicle-university-template.git
cd dicle-university-template
npm install
```

Create a `.env` file:
```env
DATABASE_URL="postgresql://username:password@localhost:5432/databasename?schema=public"
AUTH_SECRET="your-32-character-secret-key"
```

Initialize the database:
```bash
npx prisma db push
npx tsx prisma/seed-real-content.ts
npx tsx prisma/seed-staff.ts
node super-seed.js
```

Start the dev server:
```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000)

### Admin Access

Authentication is managed via NextAuth.js. A default admin account is created during seeding — check seed files for credentials. Admin features are restricted to accounts with the `ADMIN` role.

---

## License

MIT
