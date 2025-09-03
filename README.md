# Multi-Agent AI System for Automated Software Setup

Author: Mukesh Kanna

## Overview
This project demonstrates a parent-child multi-agent architecture:
- Parent Agent (orchestrator): voice/text-activated controller
- Search Agent: scrapes official pages to find installers
- Installer Agent: downloads and (optionally) runs silent installs
- Streamlit dashboard for monitoring logs and triggering orchestrations

## Safety first
- Default operation is **dry-run** (no installer executed). To enable real installation you must:
  1. edit `ORCHESTRATOR_CMD` in `streamlit_app.py` carefully
  2. run `python orchestrator.py --confirm` **only** after you are confident and have admin rights
- Test inside a disposable VM before enabling real installs.

## Installation
1. Create a virtual environment (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate   # mac/linux
   venv\Scripts\activate      # windows
