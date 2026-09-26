# JANZ TALES — Production Blog Platform

This branch upgrades JANZ TALES from the legacy Jekyll/Netlify CMS site toward a Next.js + TypeScript + PostgreSQL architecture while retaining the existing JANZ red visual identity.

## Required production environment
- DATABASE_URL: PostgreSQL connection string
- AUTH_SECRET: long random secret
- NEXT_PUBLIC_SITE_URL: https://janztales.online
- SEED_ADMIN_PASSWORD: only during initial seed

## Local setup
npm install
npx prisma db push
npm run db:seed
npm run dev

The seeded administrator is admin@janztales.online. Replace SEED_ADMIN_PASSWORD before seeding production.

## Editorial rule
Current news, recruitment, results, deadlines and other time-sensitive articles are placed in REVIEW and must be fact-checked before publication. Starter content is evergreen guidance; it must not be presented as current news.

## Deployment
Configure PostgreSQL and the environment variables in the deployment provider first. Then run npm run build. Do not commit secrets or real ad/analytics credentials.
