# Phase 8: Local Deployment and Validation

### Objective
Run and validate ComicCraft AI locally to ensure all features function smoothly and user workflow is seamless.

### Activity 8.1: Launch Application Locally

**1. Start the FastAPI Server**
Activate virtual environment and run:
```bash
# Activate env
env\Scripts\activate  # Windows
# source env/bin/activate  # Mac/Linux

# Launch server
uvicorn app.main:app --reload --port 8000
