# ProspectSnap

A mobile-first SaaS application for capturing and managing leads with team collaboration capabilities.

## Features

- **Lead Capture** — Save prospects from Instagram, email, WhatsApp, or any source
- **Multi-channel Contacts** — Emails, phone numbers with WhatsApp/SMS integration
- **Smart Paste** — Auto-parses "Name <email>" format from clipboard
- **Pipeline Management** — Track leads through New → Contacted → Replied → Booked → Customer
- **Team Collaboration** — Invite team members, shared activity feed
- **Voice Input** — Dictate names and notes via OpenAI Whisper
- **Dark/Light Theme** — Toggle between themes
- **Multi-tenant SaaS** — Platform admin dashboard for managing tenants

## Tech Stack

- **Frontend:** Single-page HTML app with Tailwind CSS, Plus Jakarta Sans font, Material Icons
- **Backend:** [Supabase](https://supabase.com) (Auth, Database, Real-time)
- **Voice:** OpenAI Whisper API via [n8n](https://n8n.io) webhook
- **Hosting:** [Cloudflare Pages](https://pages.cloudflare.com)
- **Automation:** n8n on [Railway](https://railway.app)

## Deployment

Currently deployed at: `https://prospectsnap.engrmoshbari.workers.dev/`

### Deploy to Cloudflare Pages

1. Go to [dash.cloudflare.com](https://dash.cloudflare.com) → Workers & Pages
2. Create a new Pages project connected to this repo
3. Build settings: no build command needed, output directory: `/`
4. Deploy

### Database (Supabase)

Tables used:
- `prospect_snap_teams`
- `prospect_snap_team_members`
- `prospect_snap_prospects`
- `prospect_snap_activity`
- `prospect_snap_invites`
- `prospect_snap_platform_admins`

## Version History

- **v3.1** — Email follow-up system, phone numbers with WhatsApp/SMS, smart paste, pipeline stage styling
- **v3.0** — Redesign with light/dark theme, activity feed fixes
- **v2.0** — Multi-tenant SaaS architecture, team management
- **v1.0** — Initial build with Supabase auth, prospect capture, pipeline stages
