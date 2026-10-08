# Smart Farmer Assistant

## Run locally
1. Install Node.js 18+.
2. Open a terminal in this folder.
3. Run:
   npm install
   npm start
4. Open http://localhost:3000

## API
- GET `/api/health`
- GET `/api/prices`
- POST `/api/prices` with `{ "crop":"Paddy", "price":2280, "market":"Local Mandi" }`
- GET `/api/weather?lat=17.4&lon=78.5`
- POST `/api/assistant` with `{ "message":"When should I irrigate paddy?", "language":"en" }`

## Important
The price data is currently held in server memory, so it resets when the server restarts.
The assistant endpoint has a safe demo fallback. For production, connect an AI provider on the server and store its secret in `.env`; never put API keys in browser JavaScript.

## Production roadmap
1. PostgreSQL/Supabase database for prices, farmers and farms.
2. Authentication + admin role for price updates.
3. AI provider connected server-side.
4. Weather alerts and notification service.
5. Crop disease image analysis.
6. Deploy backend and frontend with HTTPS.
