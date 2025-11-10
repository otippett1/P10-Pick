# Product Requirements Document (PRD)

## Project Title: P10 Pick

### Brief Description
**P10 Pick** is a mobile-first fantasy Formula 1 web application that makes race predictions more exciting by focusing on the sport’s unpredictable midfield.  
Instead of predicting podium finishes, each user makes **three precise picks per race**:  
1. The 10th-place finisher  
2. The first retirement  
3. The fastest lap  

The app automatically scores every race using official results and a custom points table that includes small **+5 bonus categories** such as fastest pit stop, most overtakes, and constructor double finish.  
Users can join private leagues with friends, view per-race breakdowns, track season-long leaderboards, and share results to keep engagement high throughout the season.

---

### Technical Architecture

#### Front-End
- **Framework:** React (Vite)  
- **Design:** Mobile-first responsive PWA with Tailwind CSS for styling  
- **Routing:** React Router DOM  
- **State Management:** React hooks and context for user data and scoring display  
- **API Access:** Fetch or Axios client pointed to Express endpoints  
- **Hosting:** Vercel or Netlify (for client)

#### Back-End
- **Framework:** Express (Node.js)  
- **Database:** Supabase (PostgreSQL)  
- **Endpoints:**  
  - `GET /events` → list of upcoming races  
  - `POST /picks` → submit three predictions  
  - `GET /picks/:userId` → fetch user picks  
  - `POST /score/:eventId` → trigger scoring and update leaderboard  
- **Auth:** Supabase authentication (email-based for MVP)  
- **Hosting:** Render or Supabase Edge Functions  

#### Data Layer
- **Core Tables:**  
  - `users` (UUID PK, display_name)  
  - `events` (UUID PK, name, start_time, is_sprint boolean)  
  - `picks` (UUID PK, user_id FK, event_id FK, p10, first_retirement, fastest_lap)  
  - `results` (event_id FK, official finishing order + bonuses)  
  - `scores` (UUID PK, user_id FK, event_id FK, total_points, breakdown JSONB)  
- **Migrations & Seeds:** Managed through `/supabase/migrations` scripts.

#### Tools & Frameworks
- **Package manager:** pnpm or npm  
- **Version control:** Git / GitHub  
- **Dev Environment:** Windsurf IDE with integrated Cascade for code generation  
- **Documentation:** Markdown (.md) files and OpenAPI spec in `/docs`

#### Constraints
- MVP limited to single-season 2025 F1 calendar (no live feed integration yet).  
- Race results added manually or via CSV import until official API integration.  
- Authentication limited to Supabase basic auth; no OAuth or social login in v1.  
- Scoring logic runs server-side; no client-side point calculation.  

---

### Summary
P10 Pick is designed to be fast, simple, and community-focused.  
Its lightweight React + Express + Supabase stack allows rapid development and deployment while maintaining scalability for future features such as public leagues, notifications, and automated data ingestion.
