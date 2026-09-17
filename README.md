# Cirlix

**Built is better than said.**

Cirlix is an evidence-first network for people building with AI. The alpha combines a social discovery layer with **Project Passport**, a useful standalone tool that audits a public GitHub repository and turns its visible proof into a structured project profile.

## Alpha scope

- Builder feed with useful votes, saves and share links
- Build pages centered on proof rather than self-described skills
- Technical communities for agents, RAG, MCP, evals, AI infrastructure and vibe coding
- Evidence-first builder profile and reputation concepts
- Project Passport using the live public GitHub API
- Passport score, missing-proof recommendations, README badge and launch-copy generation
- Local persistence for alpha interactions using `localStorage`
- Supabase production schema prepared in `supabase/migrations`

## Run locally

No dependencies or build step are required.

```bash
python3 -m http.server 4173
# open http://localhost:4173
```

## Architecture

The alpha is deliberately zero-dependency so it can ship immediately and be tested before committing to more infrastructure. The production migration path is documented in `docs/SHIP.md` and the database schema is prepared for Supabase.

## Security note

Project Passport only requests public GitHub metadata from the browser. It does not request a GitHub token or private repository access in this alpha.
