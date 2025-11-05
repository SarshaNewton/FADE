# 🌀 Fade Project — Development Roadmap

**Thesis Deadline:** June 2025  
**Current Phase:** Week 1 – Foundations  
**Sprint Duration:** Nov 5 → Nov 12  
**Goal:** Get Fade running locally with PostgreSQL + Google/Microsoft OAuth login + base UI shell.

---

## 🗓️ Phase Overview

| Phase | Duration | Focus | Milestone |
|-------|-----------|--------|------------|
| **Phase 1:** Core Build | Nov → Dec 2024 | Laravel + Filament + IMAP/SMTP | Working MVP |
| **Phase 2:** Thesis Writing | Jan → Mar 2025 | Documentation + architecture | 80% thesis draft |
| **Phase 3:** Refinement | Apr → May 2025 | Advanced features + UX polish | Demo-ready app |
| **Phase 4:** Submission | June 2025 | Final thesis + defense slides | ✅ Submission |

---

## ✅ Week 1 – Foundations

### 🧱 Backend / Setup
- [ ] Create Laravel project (`laravel new fade`)
- [ ] Configure PostgreSQL database (`fade_db`) and update `.env`
- [ ] (Optional) Add Docker for local consistency
- [ ] Install Filament v3 + Livewire
- [ ] Update `User` model
  - [ ] Add `username` field
  - [ ] Disable default email-only login
  - [ ] Add migration + seeder
- [ ] Install Laravel Socialite
- [ ] Configure **Google OAuth**
  - [ ] Create Google Cloud project
  - [ ] Generate OAuth 2.0 Client ID + Secret
  - [ ] Add redirect URI + `.env` entries
- [ ] Configure **Microsoft OAuth**
  - [ ] Register app in Azure Portal
  - [ ] Add redirect URI + `.env` entries
- [ ] Implement login routes + controller logic
- [ ] Test both providers (login + logout)

### 🎨 UI / Frontend
**Auth UI**
- [ ] Login page with “Sign in with Google / Microsoft” buttons
- [ ] OAuth error state + retry
- [ ] Redirect to `/dashboard` after login
- [ ] Logout button visible + working
- [ ] Keyboard/focus order check

**App Shell**
- [ ] Base layout (Topbar + Sidebar + Content)
- [ ] Placeholder nav: Inbox, Compose, Accounts, Settings
- [ ] Collapsible sidebar (responsive)
- [ ] Reusable `<Skeleton>` loading component
- [ ] Base `<Button>`, `<Badge>`, `<Card>` components

**Theme / Tokens**
- [ ] Tailwind config for brand blue palette + font stack + spacing scale
- [ ] shadcn/ui theme initialized (primary = blue)
- [ ] Test light mode UI (dark mode later)

**Utility Pages**
- [ ] 404 page (simple, consistent style)
- [ ] 500/error fallback page

**Accessibility**
- [ ] Contrast ≥ 4.5:1
- [ ] All interactive elements labeled
- [ ] Skip-to-content link
- [ ] No console errors

### 🧪 Deliverables for Week 1 (Milestone = Nov 12)
- [ ] App boots successfully (no errors)
- [ ] Database connection verified
- [ ] Login + Logout via Google/Microsoft ✅
- [ ] Screenshots → Login, Dashboard shell w/ skeleton
- [ ] GIF → Login → Redirect → Logout flow

---

## 🔮 Next Phases (Preview)

**Week 2 – Email Accounts System**
- Add `email_accounts` table, connect/disconnect flow, token refresh logic.

**Week 3–4 – IMAP/SMTP**
- Fetch inbox, send emails, thread view.

**Week 5–6 – Fade Mode (AI)**
- Summaries + tone analysis + toggle.

**Week 7–8 – Security & Polish**
- Encryption, logging, UI animations, responsive testing, documentation.

---

**Maintainer:** Sarsha Newton  
**Thesis Coordinator:** Alin Brindusescu
_Last updated: Nov 5 2025_
