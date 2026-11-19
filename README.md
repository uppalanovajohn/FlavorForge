# FlavorForge — FridgeRescue

Responsive recipe rescue web app built with HTML5, CSS3, vanilla JavaScript, Node.js and Express.

## Features
- Ingredient selector by category and custom ingredient entry
- Ingredient normalization and match scoring (assumed salt, oil and water excluded)
- Ranked recipe cards, missing ingredients and substitution suggestions
- Cooking walkthrough, time and difficulty
- Serving scaler with fraction display
- Favorites in localStorage; quick, vegetarian and favorites filters
- Express API and 40-recipe local JSON dataset

## Run
1. Install Node.js 18+.
2. Extract this ZIP and open a terminal in the `FlavorForge` folder.
3. Run `npm install`.
4. Run `npm start`.
5. Open http://localhost:3000.

## API
- GET /api/health
- GET /api/recipes
- GET /api/search?ingredients=egg,onion,bread

## Matching
Match percentage = (available required ingredients / all required ingredients) × 100. Salt, oil and water are treated as assumed staples and excluded from the denominator. Recipe data is stored in `data/recipes.json`.

## Structure
`public/` frontend · `server/` Express API · `data/` recipe JSON · `tests/` smoke test.

Nutrition estimates, expiry tracking, LLM recipe generation and voice mode are stretch features and are not falsely represented as integrated services in this build. Substitutions are suggestions; check allergy and dietary requirements before use.
