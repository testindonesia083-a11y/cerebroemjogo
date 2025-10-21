# Cérebro em Jogo - Educational Game Platform

## Overview

Cérebro em Jogo is a Portuguese-language educational game platform designed to promote child development through interactive learning. The platform emphasizes cognitive development, creativity, and logical reasoning through gamified educational content. The current implementation consists of a landing page that introduces the platform's value proposition with a colorful, engaging design focused on educational benefits.

## Recent Changes

**October 21, 2025**:
- Imported project from GitHub to Replit
- Installed Python 3.11 for serving static HTML files
- Configured workflow to serve site on port 5000 using Python's built-in HTTP server
- Created .gitignore with Python-specific entries and Replit configuration exclusions
- Set up deployment configuration for autoscale deployment (static site)
- Verified all assets loading correctly and site displaying properly
- Updated blue section with 4 new activity cards featuring header, activities description, and testimonials
- Removed borders, shadows, and padding from blue section images for edge-to-edge display
- Implemented responsive grid layout: desktop shows last 3 images side-by-side, mobile stacks all vertically
- Updated price from R$ 9,99 to R$ 14,90
- Redesigned "Como vou receber meu Material?" section with 2 new images side-by-side (desktop) or stacked (mobile)
- Modified bonus section layout: first image full-width, last 3 images side-by-side on desktop (stacked on mobile)
- Updated pack selection section: replaced Pack Básico and Super Pack images, updated checkout links to cerebroemjogo.shop, arranged packs side-by-side on desktop

**October 10, 2025**:
- Updated Super Pack image in footer with new promotional design
- Changed kit section button to link directly to Super Pack payment page instead of pack selection anchor
- Modified kit section button to scroll to Super Pack image in footer (using #super-pack anchor)

**October 8, 2025**:
- Added mobile-responsive font sizing for description text (reduced to 14px on screens ≤600px)
- Changed "+2.000 Atividades" font from Nunito to Chewy for consistent branding with tagline
- Reduced vertical spacing between CTA button and blue section (added -30px margin-bottom to .cta-button and reduced blue-section padding-top to 20px)
- Enhanced mobile spacing: button to blue section distance further reduced on mobile (margin-bottom: -50px and padding-top: 10px on screens ≤600px)
- Configured all CTA buttons to navigate to pack selection section using smooth scroll
- Added inline video playback (playsinline attribute) to prevent fullscreen-only mode
- Increased "Como vou receber meu Material?" heading size to 36px (28px on mobile) with "Material?" in orange color
- Converted pack images in footer to clickable payment links (Pack Básico and Super Pack now link to Cakto payment pages)

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture

**Technology Stack**: Pure HTML5 and CSS3 with no JavaScript framework dependencies in the current implementation.

**Design Approach**: The platform uses a minimalist, component-based structure with:
- Inline SVG graphics for logos and placeholder images to reduce HTTP requests and improve load times
- CSS custom properties implied through direct color definitions for brand consistency
- Linear gradients for visual depth and modern aesthetics
- Mobile-first responsive design principles (viewport meta tag present)

**Styling Strategy**: 
- CSS reset using universal selector for consistent cross-browser rendering
- System font stack for optimal performance and native OS appearance
- Modular section-based layout pattern (blue-section, white-section) for content alternation
- Card-based component system for content presentation

**Color Palette Architecture**: The platform uses a semantic color system tied to brand messaging:
- Yellow (#ffcc00) - Represents "Potential"
- Orange (#ff8800) - Represents "Knowledge"
- Green (#22dd66) - Represents "Learning"
- Blue (#0088cc) - Represents permanence/retention
- Neutral grays for placeholder content and backgrounds

**Layout Pattern**: Section-based architecture with alternating background colors (blue/white) to create visual rhythm and content separation. Each section contains card components with image placeholders and text content.

### Content Strategy

**Multilingual Consideration**: Currently implemented in Portuguese (pt-BR), suggesting either a Brazilian target market or potential for future internationalization.

**Visual Hierarchy**: Three-tier concentric circle logo design representing layers of learning depth, with a question mark symbol emphasizing inquiry-based learning methodology.

### Current Limitations & Extensibility Points

**Static Nature**: The current implementation is purely presentational with no interactive features or backend connectivity, providing a foundation for future feature expansion.

**Incomplete Implementation**: The HTML file appears truncated (missing closing tags for the second card and overall structure), indicating an in-progress build state.

**Scalability Considerations**: The inline SVG approach, while performance-optimized for initial load, may require migration to an asset management system as the platform scales with more graphics and interactive elements.

## Replit Environment Setup

**Development Server**: Python 3.11 with built-in HTTP server
- Workflow: `python3 -m http.server 5000`
- Port: 5000 (webview output)
- Deployment: Autoscale (static site deployment)

**Assets**: All images and video files stored in root directory and `attached_assets/` folder

## External Dependencies

**Runtime Dependencies**: 
- Python 3.11 (for development server only)

**External Services** (Third-party tracking, no code dependencies):
- UTMify tracking scripts (analytics)
- Facebook Meta Pixel (conversion tracking)
- Cakto payment integration (external payment links)

**Potential Future Dependencies** (based on architectural direction):
- JavaScript framework (React, Vue, or similar) for interactive game components
- Backend API service for user progress tracking and game state management
- Database system for storing user data, game progress, and educational content
- Authentication service for user management
- Analytics platform for tracking educational outcomes and engagement metrics
- Content Delivery Network (CDN) for serving game assets and media files

**Font Strategy**: Uses Google Fonts (Chewy, Nunito, DM Sans) for branded elements with system font stack fallback (`-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif`) for optimal rendering when web fonts are unavailable.