# Phase 7: Deployment Preparation - Local Deployment

### Objective
Prepare ComicCraft AI application for local deployment, configure environment, and ensure complete workflow runs smoothly.

### Activity 7.1: Preparing Application for Local Deployment

**1. Set Up Virtual Environment**
Isolate dependencies from other Python projects:
```bash
python -m venv env
# For Windows
env\Scripts\activate
# For macOS/Linux
source env/bin/activate
pip install -r requirements.txt
