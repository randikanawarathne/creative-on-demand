# Creative-on-Demand Tool Specification

## 1. Project Overview
- **Project Name**: Creative-on-Demand
- **Type**: Single-page web application
- **Core Functionality**: A brand asset generator that allows users to input text and upload images to create branded social media posts using predefined master templates
- **Target Users**: Marketing teams, consultants, small business owners who need consistent branded content

## 2. UI/UX Specification

### Layout Structure
- **Header**: Logo/title bar with app name
- **Main Content**: Split into two columns
  - Left Panel (40%): Input controls (template selection, text inputs, image upload)
  - Right Panel (60%): Live canvas preview
- **Footer**: Download button and branding

### Responsive Breakpoints
- Desktop: > 1024px (side-by-side layout)
- Tablet: 768px - 1024px (stacked layout)
- Mobile: < 768px (stacked, full-width)

### Visual Design

#### Color Palette
- **Primary**: `#1a1a2e` (Deep navy - backgrounds)
- **Secondary**: `#16213e` (Darker navy - panels)
- **Accent**: `#e94560` (Coral red - CTAs, highlights)
- **Surface**: `#0f0f1a` (Near black - canvas bg)
- **Text Primary**: `#ffffff`
- **Text Secondary**: `#a0a0b0`
- **Template 1 Accent**: `#00d9ff` (Cyan)
- **Template 2 Accent**: `#ff6b35` (Orange)
- **Template 3 Accent**: `#7b2cbf` (Purple)

#### Typography
- **Headings**: "Bebas Neue", sans-serif (bold, condensed)
- **Body/UI**: "DM Sans", sans-serif
- **Template Headlines**: Varies by template (see templates below)

#### Spacing System
- Base unit: 8px
- Panel padding: 32px
- Input spacing: 16px
- Section gaps: 24px

#### Visual Effects
- Subtle glow on accent elements: `box-shadow: 0 0 20px rgba(233, 69, 96, 0.3)`
- Smooth transitions: 0.3s ease
- Card hover: slight lift with shadow
- Canvas preview: subtle inner shadow for depth

### Components

#### Template Selector
- 3 clickable template cards with preview thumbnails
- Active state: coral border glow
- Hover: scale(1.02) with transition

#### Input Fields
- Dark input fields with light border
- Focus state: accent color border
- Placeholder text in secondary color

#### Image Upload
- Drag-and-drop zone with dashed border
- Click to browse fallback
- Preview thumbnail after upload
- Remove button overlay

#### Download Button
- Large, prominent coral button
- Hover: brighter with glow
- Icon: download arrow

## 3. Functionality Specification

### Core Features

#### Template System
Three master templates with distinct personalities:

**Template 1: "Bold Impact"**
- Full-bleed image background with dark overlay (60% opacity)
- Large headline in top-left quadrant
- Accent bar (4px cyan) running vertically on left edge
- Bebas Neue font, white text
- Company logo watermark bottom-right
- Dimensions: 1080x1080 (Instagram square)

**Template 2: "Modern Split"**
- Image on right 60%, solid accent orange on left 40%
- Left side: headline (vertical centered), tagline, CTA button shape
- Right side: image with subtle gradient overlay
- White text on orange, black on image
- Geometric accent shapes
- Dimensions: 1080x1080

**Template 3: "Elegant Frame"**
- Image with rounded corners (24px radius) centered
- Thin accent purple border (3px) inside frame
- Headline below image, centered
- Decorative line above and below tagline
- Clean, editorial aesthetic
- Dimensions: 1080x1350 (Portrait/Story)

#### User Inputs
1. **Headline** (required): Main text, max 50 chars
2. **Tagline** (optional): Secondary text, max 100 chars
3. **Image Upload**: JPG/PNG, min 400x400px
4. **Brand Name**: Small text for watermark, max 30 chars

#### Canvas Rendering
- Real-time preview updates on any input change
- Debounced rendering (150ms) for performance
- High-resolution output (2x for retina)

#### Download
- Generates PNG at full resolution
- Filename: `creative-on-demand-[template-name]-[timestamp].png`

### User Interactions
1. Select template → canvas updates with template structure
2. Type headline → live preview updates
3. Upload image → appears in template layout
4. Click download → saves PNG file

### Edge Cases
- No image uploaded: Show placeholder with "Upload an image" prompt
- Text overflow: Auto-scale font size down (min 24px)
- Large images: Scale to fit with cover positioning
- No text entered: Show placeholder text in preview

## 4. Acceptance Criteria

### Visual Checkpoints
- [ ] Dark theme UI with coral accents renders correctly
- [ ] All 3 template cards visible and clickable
- [ ] Input fields have proper focus states
- [ ] Image upload zone accepts drag-and-drop
- [ ] Canvas preview shows live updates
- [ ] Download button triggers file save

### Functional Checkpoints
- [ ] Template switching changes canvas layout
- [ ] Text input appears in correct template position
- [ ] Uploaded image displays in template
- [ ] Downloaded PNG matches preview quality
- [ ] Responsive layout works on tablet/mobile

### Technical Requirements
- Pure JavaScript with HTML5 Canvas API
- No external dependencies except Google Fonts
- Single HTML file with embedded CSS/JS
- Works in modern browsers (Chrome, Firefox, Safari, Edge)
