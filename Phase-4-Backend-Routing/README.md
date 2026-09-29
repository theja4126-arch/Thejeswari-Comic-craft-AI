# Phase 4: FastAPI Backend & Routing Implementation

### Objective
Implement FastAPI backend to manage routing, user input processing, and integration of AI workflows.

### Activity 4.1: Define Routes in FastAPI
All routing logic handled in `routes.py`. Each route linked to backend function from Phase 3.

### Activity 4.2: Process User Input

**HTML Form Handling:**
- Form created in `index.html`
- User enters: Story Prompt, Character Name, Setting, Tone, Art Style
- FastAPI captures inputs using `Form(...)` parameters
- Pydantic schema `PromptRequest` used for JSON validation

**API Endpoints Implemented:**

**1. /generate (POST) - Main Comic Generation**
- Receives form data from frontend
- Calls `generate_outline()` -> Creates 5-panel outlines
- Calls `generate_story()` -> Expands to narration & dialogue
- Calls `generate_image()` for each panel -> Creates illustrations
- Calls `build_comic_layout()` -> Organizes final layout
- Calls `save_pdf()` -> Compiles PDF
- Renders `comic_preview.html` with layout

**2. /generate-comic/json (POST) - API Based Generation**
- Similar flow as /generate
- Triggered via raw JSON API request
- Returns JSON response with layout data and PDF path
- For API clients and testing

**3. /test-image (POST) - Image Generation Test**
- Calls `generate_image()` directly with custom prompt
- Tests image generation functionality separately
- Useful for debugging Stable Diffusion

**4. /export-success (GET) - Export Confirmation**
- Shows success message after PDF download
- Renders `export_success.html`

### Integration Flow
