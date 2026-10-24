# Quiz Runner — Run & Learn
An original 3D learning game for Class 6 Computer. All assets are procedural geometry; audio is synthesized locally. No accounts or external APIs are needed.

## Run locally
Use Node.js 22 or later.
```
npm install
npm run dev
```
Production: `npm run build`. Serve the generated `dist` folder with a static web server.

## Source map
- `src/main.tsx`: accessible menus, quiz formats, gameplay lifecycle and HUD
- `src/World.tsx`: Three.js / React Three Fiber environment and animated character
- `src/engine.ts`: obstacle rows, collision rules and rewards
- `src/questions.ts`: 44 paper-derived questions and non-repeating run selection
- `src/store.ts`: persisted progress, achievements and synthesized audio
- `src/style.css`: responsive interface and Tailwind integration

Keyboard: arrows / WASD, space to jump, Escape to pause. Mobile: swipe or touch buttons. Orange obstacles and gaps need a jump, purple overhead barriers need a slide, red blocks require changing lanes. Blue pickups give shields, pink magnets, green boosts, gold double coins and purple hints.

Each level has five quiz checkpoints across a 660m run, followed by five final questions. Each run samples 10 distinct questions from that level.

## Question source
All 44 game questions trace to `PT 2 COMP Class 6.docx`, Periodic Test-II 2026–27. Level 1 has 20 entries covering Q1–Q4 (including two matching sets covering all six pairs). Level 2 has 24 entries covering Q5–Q8, including all nine case-study subquestions and all internal-choice alternatives. Written-response questions are adapted into selectable answers; their explanations provide model answers. Added distractors are for gameplay, not additional examination questions. Each entry has a sourceRef shown in the quiz panel. No previous general question-bank items remain.

Incorrect answers explain the concept and appear in the end-of-run revision panel. Level 2 unlocks after completing Level 1 with 60% accuracy.

Progress and settings are stored on the current browser, not synced between devices. Use Settings to reset. Graphics Low caps render resolution to reduce GPU work. No external 3D textures, models or audio need downloading.
