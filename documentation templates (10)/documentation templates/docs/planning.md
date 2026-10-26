Project Proposal: Bristol Green Spaces Finder

​Business Case

​Problem Statement

​Bristol Council manages more than 200 public parks and green spaces. The problem? That data is trapped in flat spreadsheets and static tables.
​If a parent needs a park with a working playground and toilets, or a wheelchair user needs paved paths, they shouldn't have to manually cross-reference raw open data tables or guess. Right now, there is no quick, visual way for people to filter parks by actual facilities before heading out the door.

​Business Benefits

​Drives Physical Activity: People use public spaces more when they can quickly find parks that fit their specific plans.
​Spreads Out Foot Traffic: Highlights smaller, under-utilized neighbourhood parks instead of bottlenecking everyone into the same two central spots.
​Zero Privacy Risk: The app handles strictly public geographic data—no user accounts, no location tracking logs.
​Low Ongoing Maintenance: Park perimeters and basic amenities don't change often. Once the pipeline works, it largely runs itself.

​Options Considered

​Option A: Static HTML Directory on Council Website
​Verdict: Rejected. A long text list doesn't give spatial context or let users combine filters (e.g., "toilets + playground + dog-friendly").
​Option B: Commercial GIS Platform (e.g., ArcGIS Online)
​Verdict: Rejected. Overkill for a lightweight public tool, and the recurring subscription costs aren't worth it for a free utility.
​Option C: Custom Open-Source Web GIS (Selected)
​Verdict: Selected. Building a responsive web app using Leaflet/Mapbox GL directly pulling from the Bristol Open Data API. Free licensing, fast rendering, and complete control over the UI.

​Key Risks

​Stale API Data: If the council takes months to update broken equipment or seasonal closures in the database, users will hit out-of-date info.
​Dead Zones: Large parks often have spotty cell service. Map tiles need to handle poor connection gracefully without crashing the app.
​API Breakage: If Bristol's backend developers change structural schemas or API endpoints without notice, the ingestion script will break until we patch it.

​Project Scope

​In-Scope System Components
​Here is what we are actually building:
​Interactive Map View: Responsive Leaflet map cantered on Bristol, complete with a "Near Me" GPS trigger.
​Amenity Filter Bar: Quick toggles for core features (Playgrounds, Public Toilets, Wheelchair Access, Sports Pitches, Dog-Friendly Areas).
​Park Popup Cards: Compact drawer/popup with the park name, opening hours, active amenities, and a direct Google/Apple Maps routing link.
​API Integration Pipeline: Lightweight client service that fetches and parses GeoJSON data straight from the Bristol Open Data API.
​Simple Feedback Form: A lightweight modal on each park card to flag incorrect data or broken equipment to council admins.
<img width="704" height="1203" alt="1792969970729" src="https://github.com/user-attachments/assets/2b5a5747-5268-4087-ae08-ead8227956cb" />

