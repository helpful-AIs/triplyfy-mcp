## Triplyfy MCP — Claude Desktop Setup

### What is Triplyfy?
Triplyfy is a trip planning app that lets you design itineraries collaboratively and with AI assistance. Anyone with a link can view a trip. To view details and edit, sign in with Google.

Key app capabilities:
- Create trips with optional start date and description
- Google Places autocomplete to find locations
- Drag-and-drop between lists and within a day
- Map view to search and visualize saved places
- "All Events" (Todo) list for ideas you might add later
- Unlimited days; change day color; open route in Google Maps; clear/delete day
- Add notes and flights alongside places
- Flight card includes title, price, origin/destination airports, note, departure/arrival datetime, stops, duration

AI-assisted planning:
- Chat-based planning: Claude can propose events; you approve; the plan is saved to Triplyfy
- Claude can find flights and save them into your trip
- Claude can edit existing trips on your request

### How sign‑in works
- When you first connect from Claude Desktop, we open an OAuth page to sign in with Google.
- We only use basic profile info (email, name, avatar) to create your account and attach plans to you. We do not read your email, calendar, or files.
- After consent, Claude exchanges an authorization code for a Triplyfy session token (not a Google token). This session token is used only to authenticate requests from Claude to Triplyfy.
- The session token lasts about 30 days. You may be asked to sign in again when it expires.

### How your data is used
- Your plans and items (places, notes, flights) are stored in Triplyfy so you can view and edit them later.
- We do not sell your data. Data is used to operate the service and improve the planning experience.
- Anyone with a share link can view the trip; editing requires Google sign‑in.
- You can delete trips you no longer want to keep.
- The MCP server acts only on your explicit instructions. It cannot access other users’ data or operate outside your account.

### Useful MCP functions
- whoami — check connectivity and your signed‑in identity
- readAllPlans — list all your trips
- readOnePlan — open a specific trip and list the days/events
- createPlan — create a new trip/itinerary
- updatePlan — update an existing trip (add notes, events, flights)
- getFlights — search flight options for specific dates/routes

Example prompts to Claude:
- "Check Triplyfy connection and show the email I'm signed in with."
- "Create a 5‑day Rome itinerary focused on museums and food."
- "Find flights from Warsaw to Tbilisi for Sep 10–15."
- "Add that flight to day 2 of my current trip."
### Connect via Claude Desktop
Claude launches a small bridge process that talks to the remote MCP over SSE.

Open Claude Desktop → Settings → Developer → MCP Servers → Add server 
  
  Name: ```Triplyfy``` 

  MCP SSE endpoint:
  ```https://triplyfy.com/mcp/sse```
  
On first connect, you’ll be prompted to sign in and approve access. No manual supergateway run is required—Claude will launch it for you.

### Links & Contact
- Website: https://triplyfy.com/
- Email: kirill2003de@gmail.com

