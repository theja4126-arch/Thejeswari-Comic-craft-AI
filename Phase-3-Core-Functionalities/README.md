# Phase 3: Core Functionalities Development

### Objective
Develop the core AI-powered functionalities for generating comic outlines, stories, and illustrations.

### Activity 3.1: Develop Core Functionalities

**1. Generate Structured Comic Panel Outline**
- **Function:** `generate_outline()`
- **File:** `gemini_flash.py`
- **Model:** Gemini Flash (gemini-1.5-flash)
- Uses user's story prompt to generate 5-panel structure
- Each panel contains: Panel Number, Title, Scene Description, Image Generation Prompt
- Output: List of dictionaries (one per panel)

**2. Generate Comic Story Narration and Dialogue**
- **Function:** `generate_story()`
- **File:** `gemini_pro.py`
- **Model:** Gemini Pro (gemini-1.5-pro)
- Expands panel outlines into full comic-style story
- Creates engaging narration and character dialogues for each panel
- Output: Single formatted text with all panels' stories

**3. Generate Comic Illustrations from Prompts**
- **Function:** `generate_image()`
- **File:** `image_generator.py`
- **Model:** Stable Diffusion (runwayml/stable-diffusion-v1-5)
- Creates comic-style image based on image prompt
- Sanitizes prompt for safe filenames
- Saves images to `static/panels/` directory
- Returns file path to saved image

**4. Organize Comic Panels into Layout Structure**
- **Function:** `build_comic_layout()`
- **File:** `layout_builder.py`
- Organizes generated images and story into structured layout
- Matches each image with corresponding panel story
- Output: List of dictionaries with panel number, image path, and text

**5. Export Comic Panel and Story into PDF**
- **Function:** `save_pdf()`
- **File:** `exporters.py`
- **Library:** FPDF
- Compiles full comic into multi-page PDF
- Each panel's image and narration placed neatly on separate pages
- Saves final PDF to `static/exports/` folder
- Returns path to PDF

### Workflow Summary
User Prompt -> Gemini Flash (Outline) -> Gemini Pro (Story) -> Stable Diffusion (Images) -> Layout Builder -> PDF Export

All core AI functions are developed and tested individually.
