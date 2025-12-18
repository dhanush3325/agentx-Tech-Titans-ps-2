# AgentX – Puzzleverse  
### Gamified Learning Environment for AgentX (PS2)

## Team Name  
*Tech Titan*

## Team Members  
- K. Thrinesh (Team Leader)  
- K. Sai Teja  
- G. Dhanush  
- Sk. Saleem  

---

## Problem Statement  
*PS2: Gamified Learning Environment for AgentX*

The objective of this project is to design and implement a gamified learning environment where an AI agent (AgentX) can train, evolve, and demonstrate intelligent behavior. The environment emphasizes game mechanics, reward shaping, scoring systems, and agent progression to encourage efficient learning and problem-solving.

---

## Approach Overview  

We designed *Puzzleverse*, a dynamic puzzle-based game world where AgentX learns through interaction and reinforcement learning.

### Key Concepts:
- AgentX explores a grid-based environment
- Solves puzzles, avoids traps, and collects rewards
- Learns optimal behavior through rewards and penalties
- Progresses through levels with increasing difficulty

---

## Game Mechanics  

- *Environment*: Grid world with mazes, keys, traps, and goals  
- *Actions*:
  - Move (Up, Down, Left, Right)
  - Collect items
  - Solve puzzles
- *Episodes*: Each episode presents a new environment layout

---

## Agent Design  

- *Agent*: AgentX (Reinforcement Learning Agent)
- *State Space*:
  - Agent position
  - Nearby obstacles
  - Items collected
- *Action Space*:
  - Navigation actions
  - Interaction actions
- *Algorithm Used*:
  - Reinforcement Learning (Q-Learning / Deep Q-Network – conceptual)

  # Complete Setup Guide(Setup steps )
Prerequisites
Node.js (v18 or higher)
npm or yarn
PostgreSQL database (for production; development uses in-memory store)
# Step 1: Clone & Install Dependencies
#Clone the repository (or extract if you have a zip)
git clone <your-repo-url>
cd your-project
#Install all dependencies
npm install

# Step 2: Environment Setup
Create a .env file in the root directory:

#Server
NODE_ENV=development
PORT=5000
#Database (if using PostgreSQL)
DATABASE_URL=postgresql://user:password@localhost:5432/dbname
#Session
SESSION_SECRET=your-secret-key-here

# Step 3: Database Setup (if using PostgreSQL)
#Create your database first
createdb your-database-name
#Run migrations
npm run db:push

# Step 4: Start Development
Option A: Full Stack (Frontend + Backend together)

npm run dev

This runs the backend server on http://localhost:5000 and serves the frontend from it.

Option B: Frontend Only (for UI iteration)

npm run dev:client

This runs just the Vite dev server on http://localhost:5000 with hot reload.

# Step 5: Build for Production
#Build the app
npm run build
#Start production server
npm start

Project Structure
├── client/              # Frontend React app
│   ├── src/
│   │   ├── pages/      # Page components
│   │   ├── components/ # UI components (Shadcn)
│   │   ├── App.tsx     # Main router
│   │   └── index.css   # Styling
│   └── index.html      # HTML template
├── server/             # Backend Express server
│   ├── index.ts        # Server entry
│   ├── routes.ts       # API routes
│   └── storage.ts      # Data layer
├── shared/             # Shared code
│   └── schema.ts       # Type definitions
└── package.json        # Dependencies

Key Commands Reference
Command	Purpose
npm run dev	Run full stack (backend + frontend)
npm run dev:client	Run frontend only (Vite dev server)
npm run build	Build for production
npm start	Start production server
npm run check	TypeScript type checking
npm run db:push	Run database migrations
Adding Pages
Create a new component in client/src/pages/
Register it in client/src/App.tsx:
import MyPage from "@/pages/my-page";
function Router() {
  return (
    <Switch>
      <Route path="/my-route" component={MyPage} />
      <Route component={NotFound} />
    </Switch>
  );
}

Adding API Routes
Add routes in server/routes.ts
Call them from frontend using TanStack Query or fetch


# Expected outputs  
website:
























