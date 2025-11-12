# Workspace Rules – P10 Pick

## Naming Conventions
To keep the project organized and consistent, all contributors must follow these conventions.

### Files and Folders
- Use **lowercase** and **hyphens** for folder and file names.  
  Example: `/client/components/navbar.jsx`, `/api/routes/picks.js`
- Avoid spaces or capital letters in names.  
- Choose clear, descriptive names (e.g., `leaderboard.js` instead of `file1.js`).

### Variables and Functions
- Use **camelCase** for variables and functions. Example: `userScore`, `calculatePoints()`
- Use **PascalCase** for React components. Example: `RaceCard`, `LeaderboardTable`
- Use **UPPER_SNAKE_CASE** for constants and environment variables. Example: `API_BASE_URL`, `MAX_BONUS_POINTS`

### Database Tables and Columns
- Use **snake_case** for all database tables and column names. Example: `user_profiles`, `first_retirement`, `fastest_lap`

---

## Commit Message Guidelines
All commit messages must be clear, short, and follow the same format.

**Format:**
type(scope): short, clear summary

markdown
Copy code

### Types
| Type | Meaning |
|------|----------|
| feat | a new feature |
| fix | a bug fix |
| refactor | code change that doesn’t fix a bug or add a feature |
| docs | documentation changes |
| style | UI or formatting updates (no logic change) |
| chore | setup, config, or maintenance task |

### Examples
- `feat(client): add make-picks form`
- `fix(api): correct leaderboard scoring logic`
- `refactor(client): simplify bonus scoring`
- `docs: update PRD and feature chart`

### Rules
- Each commit should represent one logical change.  
- Write messages in **imperative mood** (“add feature,” not “added feature”).  
- Keep messages under 70 characters when possible.  
- Reference task IDs or issues if applicable (e.g., `feat(api): add POST /picks (#7)`).

---

## Pull Request and Review Process
Pull Requests (PRs) maintain quality control and team collaboration.

### Before Opening a PR
1. Pull the latest `dev` branch:  
git pull origin dev

markdown
Copy code
2. Run lint and format checks (`npm run lint`, `npm run format`).
3. Verify all tests pass locally.
4. Update documentation if needed.

### PR Format
type(scope): short description

markdown
Copy code
Example:  
`feat(api): implement POST /score endpoint`

### Review Steps
1. Submit your PR into the `dev` branch.  
2. Assign at least one reviewer.  
3. Reviewer checks:
   - Code clarity and consistency
   - Functional correctness
   - UI/UX alignment (if applicable)
   - Commit message format
4. Address feedback and update PR as needed.  
5. Once approved, merge into `dev`.  
6. Instructor or lead merges `dev` → `main` when stable.

---

## Branching Strategy
A clear branching strategy keeps collaboration smooth and prevents conflicts.

### Main Branches
| Branch | Purpose |
|---------|----------|
| `main` | Stable, production-ready branch |
| `dev` | Active development branch for integrating new features |

### Feature Branches
Create a new branch for each feature or fix:
git checkout -b feature/<short-description>

markdown
Copy code
Examples:
- `feature/make-picks-page`
- `feature/leaderboard-ui`
- `fix/api-scoring-bug`

### Workflow
1. Start from `dev`:
git checkout dev
git pull origin dev
git checkout -b feature/<name>

markdown
Copy code
2. Work and commit frequently.  
3. Push to remote:
git push origin feature/<name>

sql
Copy code
4. Open a Pull Request into `dev` when complete.  
5. After review and merge:
git branch -d feature/<name>

shell
Copy code

### Hotfix Branches
For urgent production fixes:
git checkout -b hotfix/<issue>

yaml
Copy code
After testing, merge directly into both `main` and `dev`.
