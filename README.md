# Christ Way Church Management System (CWCMS)

Starter full-stack church administration app with Next.js and Supabase backend/auth/database. This is a build foundation: configure your Supabase instance, run the SQL, and progressively finish the remaining workflows before production use.

## Quick setup
1. Install Node.js 20+ and Git.
2. Create a Supabase project at https://supabase.com.
3. Open Supabase SQL Editor and run all contents of `supabase/schema.sql`.
4. Copy `.env.example` to `.env.local`, add your Supabase project URL and anon/public key.
5. In Supabase Authentication, configure email/password and create the initial user. In SQL Editor, set profile/role/branch for that user using the UUID from Authentication Users: `insert into public.user_profiles(id,full_name,role,branch_id) values ('USER_UUID','Church Administrator','super_admin',null);`
6. Install dependencies and run: `npm install`, `npm run dev`. Visit http://localhost:3000.
7. For deployment, push to GitHub and import the repository into Vercel. Add the same environment variables in Vercel.

## Included
- Dashboard and branch overview
- Supabase Auth sign-in page
- Members database CRUD (add/list starter workflow)
- Database schema for members, branches, attendance, visitors, MCs, ministries, finance, events, pastoral care, audit logs
- Initial branch-aware RLS policies and role model
- Setup documentation and environment template

## Branches
- Christ Way Church Najjera (HQ)
- Christ Way Church Bulindo
- Christ Way Church Kyanjanja

## Security warning
This is not yet a fully audited production system. Some modules are workspace placeholders. RLS policies and sensitive-data access must be reviewed and tested; the supplied policies are an initial template, not a substitute for security review. Do not enter real pastoral notes or financial data until the access model has been validated. Never commit `.env.local` or credentials.
