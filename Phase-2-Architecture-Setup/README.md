# Phase 2: Architecture Definition & Environment Setup

### Objective
Define the system architecture and set up the complete development environment for ComicCraft AI.

### Activity 2.1: Define Architecture
The architecture is divided into 3 primary components:

**1. Frontend (HTML, CSS, Jinja2)**
- Captures user inputs
- Input fields: Story Prompt, Character Name, Setting, Story Tone, Art Style
- Templates: index.html, comic_preview.html, export_success.html
- Sends data to backend via POST request

**2. Backend (FastAPI)**
- Receives form data from frontend
- Calls AI models to generate outlines, stories, and images
- Organizes and builds complete comic layout
- Exports comic to PDF format
- Routes: /generate, /generate-comic/json, /test-image, /export-success

**3. AI Integration (Gemini & Stable Diffusion)**
- Gemini Flash: Generates 5-panel outline
- Gemini Pro: Generates detailed narration and dialogue
- Stable Diffusion: Generates comic-style illustrations
- All interactions happen dynamically for unique comics

### Activity 2.2: Development Environment Setup

**Step 1: Install Python & Pip**
Ensure Python and pip are installed

**Step 2: Create Virtual Environment**
```bash
python -m venv comiccraft-env
comiccraft-env\Scripts\activate  # For Windows
# source comiccraft-env/bin/activate # For Mac/Linux
