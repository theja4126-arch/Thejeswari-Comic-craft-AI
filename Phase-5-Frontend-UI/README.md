# Phase 5: Frontend Development - UI Design

### Objective
Design and develop a user-friendly, creative, and responsive web interface for ComicCraft AI.

### Activity 5.1: Designing and Developing User Interface

**1. Set Up Base HTML Structure**
Developed `index.html` as main entry point.

**Form Fields Created:**
- Story Prompt: Main idea for comic (textarea)
- Main Character Name: Hero of comic (text input)
- Setting: Location - forest, school, city, space (dropdown)
- Story Tone: Mood - dramatic, funny, light-hearted, poetic (dropdown)
- Art Style: Visual style - anime, pixel art, comic book, realistic (dropdown)

Each field properly labeled and grouped using semantic HTML elements.

**2. Design Responsive Layout Using CSS**
- Embedded CSS styles directly within each HTML file
- Fixed width with centered content for readability
- Consistent button styling with hover effects
- Input fields with padding, box shadows, rounded corners
- Light color scheme for inviting visual aesthetic
- Scenic background image to foster creative atmosphere
- Minimal navigation to maintain focus

**3. Create Separate Pages for Core Functionality**
Three Jinja2-powered templates created under `/templates` folder:

**a) index.html - Homepage**
- User-friendly form for inputs
- Submits data to `/generate` FastAPI route via POST
- Clean layout with creative background
- Simple, accessible to all users without technical expertise

**b) comic_preview.html - Result Page**
- Displays AI-generated comic panel-by-panel sequentially
- Each panel includes:
    - Title (e.g., "Panel 2: Into the Deep Woods")
    - Comic Image (AI-generated illustration)
    - Scene Description (in italics, sets atmosphere)
    - Caption and Narration (character actions, dialogues)
    - Image Prompt Reference (original description)
- Loops through layout list using Jinja2 `{% for panel in layout %}`
- Ensures clear separation and visually appealing flow

**c) export_success.html - Success Page**
- Displays confirmation message after PDF download
- Provides tangible output confirmation
- Includes CTA button: "Go Create Another Comic"
- Promotes continued engagement
- Receives exported PDF path as context

### Design Principles Followed
- User-centric flow: Input -> Preview -> Export
- Visual appeal with comic-style presentation
- Mobile-friendly responsive design
- Easy storytelling experience for non-artists

Frontend UI ensures seamless flow from input collection to comic generation display.
