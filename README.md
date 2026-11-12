# TrustLayer

TrustLayer is an early-stage AI response review tool. It checks drafts in the browser for common sensitive-data patterns, risky commitments, and phrases saved in a company's policy library.

## Current capabilities
- Supabase email/password authentication
- Private organization workspaces
- Company policy phrase storage
- Browser-based response checks
- Scan history stores counts and categories only, never draft response text
- Responsive layout for desktop and mobile

## Stack
- Static HTML/CSS/JavaScript
- Supabase Auth and Postgres with Row Level Security
- Vercel hosting
- GitHub source control

## Setup
The browser uses a Supabase **publishable** key. This key is intended for client-side use; authorization is enforced by RLS. Never put a Supabase secret or service-role key in this repository.

For local development, serve `index.html` from a local web server. Configure Supabase Auth email confirmation and allowed redirect URLs for your deployed domain.

## Important limitations
This is a rule-based review assistant, not an AI model, legal review, security certification, or guarantee that a response is safe. Rules can miss issues or flag harmless text. A human must review all flagged and unflagged drafts. Do not paste real customer or confidential information.
