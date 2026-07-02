# CoastalTrace Demo

A simple demo website for our seafood traceability platform idea.

## What is CoastalTrace?

We are building a voice-first traceability system for Indian seafood exporters. Fishermen and dock agents send WhatsApp voice notes in their local language. Our system converts speech to text, extracts structured data, and creates a digital traceability chain from boat to export dock.

## Why This Matters

- India exports $6.2B in seafood annually
- 15-25% spoils due to broken cold chain tracking
- Current process is paper-based and English-only
- MPEDA and EU regulations now require digital traceability

## How It Works

1. **Ganesh (Fisherman)** sends a WhatsApp voice note: "120kg seer fish, arriving in 45 minutes"
2. **AI** transcribes Tamil to English, extracts weight, species, and ETA
3. **Raju (Agent)** sees it on a live dashboard with risk alerts
4. **Risk engine** checks weather, route, and temperature to predict spoilage

## What This Demo Shows

This is a static HTML demo website showing:
- The user dashboard with active shipments
- The six-node custody chain (boat -> agent -> truck -> plant -> transit -> port)
- Cost analysis and spoilage savings calculations
- How we compare to existing solutions

It is not a working backend. It is a visual prototype to present our idea.

## How to View

Open `coastaltrace_demo.html` in any web browser. No server needed.

```bash
# Or use a simple HTTP server
python3 -m http.server 8000
# Then open http://localhost:8000/coastaltrace_demo.html
Tech Stack (Planned)
WhatsApp Cloud API for voice input
Bhashini for Indian language speech-to-text
Groq (Llama 3) for data extraction
Open-Meteo for weather data
PostgreSQL for batch records
Note on API Costs
WhatsApp: Service replies within 24h are free. Business-initiated messages cost ~$0.002-0.009 each in India.
Open-Meteo free tier is for non-commercial use only. Commercial deployment requires a paid plan.
Groq free tier (20 requests/min) is confirmed for 2026.
Bhashini free tier is unverified for 2026. We have AI4Bharat as a fallback.
Project Structure
plain
coastaltrace-demo/
├── coastaltrace_demo.html    # The demo website (single file)
├── README.md                 # This file
