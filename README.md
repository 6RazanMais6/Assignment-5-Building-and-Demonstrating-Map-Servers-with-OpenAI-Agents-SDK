# Assignment-5
#  Building and Demonstrating Map Servers with OpenAI Agents SDK

This project was developed as part of the **"Building and Demonstrating Map Servers with OpenAI Agents SDK"** assignment.  
It showcases how to design, implement, and demonstrate **custom map servers** using the **OpenAI Agents SDK** and the **Model Context Protocol (MCP)** — all within a **Google Colab environment**.

---

##  Table of Contents
- [Overview](#overview)
- [Learning Objectives](#learning-objectives)
- [Environment Setup](#environment-setup)
- [Implementation Details](#implementation-details)
  - [1. GeoServer](#1-geoserver)
  - [2. RouteServer](#2-routeserver)
  - [3. POIServer](#3-poiserver)
- [How to Run in Google Colab](#how-to-run-in-google-colab)
- [Screencast Demonstration](#screencast-demonstration)

---

##  Overview

This project implements **three custom MCP-compatible map servers** — `GeoServer`, `RouteServer`, and `POIServer` — as agent tools that can perform:
1. **Geocoding** — Convert a location name to latitude/longitude.  
2. **Routing** — Compute simple routes between two points.  
3. **POI Search** — Search for points of interest near a location.

All servers are integrated into an **Assistant Agent** that automatically discovers and interacts with them using the **OpenAI Agents SDK**.  
The full implementation is runnable inside **Google Colab**.

---

##  Learning Objectives

By completing this project, I learned to:
- Understand and apply the **Model Context Protocol (MCP)** for tool integration.
- Use the **OpenAI Agents SDK** to build and register custom agent tools.
- Design modular, asynchronous Python map services.
- Demonstrate agent–tool interaction in a real-time Colab environment.

---

##  Environment Setup

###  Requirements
- Python 3.10+  
- Google Colab environment  
- OpenAI Agents SDK (latest version)  
- Basic familiarity with `asyncio` and JSON APIs

###  Installation
In your Google Colab notebook, run:
```bash
pip install openai-agents-sdk --upgrade
```
Then import required libraries:
```bash
import asyncio
from openai_agents_sdk import Agent, Tool
```

---

### Implementation Details

1️⃣ GeoServer

Function: Performs geocoding — converts a location name into geographic coordinates.
Example Usage:
```bash
 print("\n--- Agent Query 1: Geocode ---")
    r1 = await Runner.run(agent, "Find coordinates of the Eiffel Tower")
    print("Response:", r1.final_output)
```

Output:
```bash
--- Agent Query 1: Geocode ---
Response: The coordinates of the Eiffel Tower are:  
Latitude: 48.8584  
Longitude: 2.2945
```

2️⃣ RouteServer

Function: Performs routing — computes distance and path between two coordinates.
Example Usage:
```bash
 print("\n--- Agent Query 2: Route ---")
    r2 = await Runner.run(agent, "Find route from Beirut to Tripoli")
    print("Response:", r2.final_output)
```

Output:
```bash
--- Agent Query 2: Route ---
Response: The route from Beirut to Tripoli follows the coastal highway, covering approximately 85 km and typically taking around 1 hour and 30 minutes by car. Let me know if you need step-by-step directions or points of interest along the way!

```
3️⃣ POIServer

Function: Performs point-of-interest (POI) search — finds nearby places based on a keyword.
Example Usage:
```bash
    print("\n--- Agent Query 3: POI Search ---")
    r3 = await Runner.run(agent, "Search museums in Paris")
    print("Response:", r3.final_output)
```bash

Output:
```bash
--- Agent Query 3: POI Search ---
Response: Here is a museum in Paris:
- Louvre Museum
```

---

## How to Run in Google Colab
1. Open the provided Colab notebook (Ass5.ipynb).

2. Run all cells sequentially:

Install dependencies

Define map servers

Register the tools

Execute discovery and demo cells

3. Expected discovery output:
   ```bash
   Discovered: ['geoserver', 'routeserver', 'poiserver']
   ```

---

## Screencast Demonstration

A screencast video demonstrates:

Project overview and concept explanation

Code walkthrough in Google Colab

Live execution of the three map servers

Discussion of challenges and next steps

Video Link: 
