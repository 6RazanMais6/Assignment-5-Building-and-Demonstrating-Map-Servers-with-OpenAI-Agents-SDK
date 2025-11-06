# Assignment-5-Building-and-Demonstrating-Map-Servers-with-OpenAI-Agents-SDK
# 🗺️ Building and Demonstrating Map Servers with OpenAI Agents SDK

This project was developed as part of the **"Building and Demonstrating Map Servers with OpenAI Agents SDK"** assignment.  
It showcases how to design, implement, and demonstrate **custom map servers** using the **OpenAI Agents SDK** and the **Model Context Protocol (MCP)** — all within a **Google Colab environment**.

---

## 📘 Table of Contents
- [Overview](#overview)
- [Learning Objectives](#learning-objectives)
- [Environment Setup](#environment-setup)
- [Implementation Details](#implementation-details)
  - [1. GeoServer](#1-geoserver)
  - [2. RouteServer](#2-routeserver)
  - [3. POIServer](#3-poiserver)
- [How to Run in Google Colab](#how-to-run-in-google-colab)
- [Expected Output](#expected-output)
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
''import asyncio
from openai_agents_sdk import Agent, Tool  # Example import — adjust if needed''


---

##  Environment Setup

In your Google Colab notebook, run:

```python
!pip install openai-agents-sdk --upgrade
