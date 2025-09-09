# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is Astra AI (AICMS - Anti-India Campaign Monitoring System), a cybersecurity operations center dashboard implemented as a single HTML file. The project is designed to detect and analyze anti-India campaigns across digital platforms using AI-powered threat detection.

## Architecture

- **Single-page application**: Built entirely in `index.html` with embedded CSS and JavaScript
- **Frontend stack**: HTML5, Tailwind CSS (via CDN), vanilla JavaScript
- **External dependencies**: 
  - Tailwind CSS for styling
  - Chart.js for data visualization  
  - Google Fonts (Inter)
  - Gemini AI API for content analysis

## Key Features

- **Dashboard**: Real-time monitoring of cybersecurity threats
- **Content Analysis**: AI-powered analysis of social media posts and URLs
- **AI Learning Center**: Model performance metrics and learning capabilities
- **Platform Analytics**: Monitoring across Facebook, Twitter, WhatsApp, Instagram, Telegram, YouTube, TikTok, Reddit

## Development

### Running the Application
Since this is a static HTML file, simply:
```bash
# Open directly in browser
open index.html

# Or serve with a simple HTTP server
python3 -m http.server 8000
# Then visit http://localhost:8000
```

### API Configuration
The application integrates with Gemini AI API:
- API key is embedded in the JavaScript (line 392)
- Uses Gemini 2.5 Flash Preview model
- Functions: `callGeminiAPI()`, `analyzeContentWithGemini()`, `summarizeAlertsWithGemini()`

### Code Structure
- **Lines 1-55**: HTML head with CSS styling and external dependencies
- **Lines 56-356**: Main HTML structure with three sections (Dashboard, Content Analysis, AI Learning)
- **Lines 368-630**: JavaScript functionality for UI interactions and API calls

### Key Components
- **Navigation**: Tab-based navigation between sections
- **Threat List**: Dynamic rendering of security alerts with filtering
- **Content Analysis**: Text/URL analysis with AI-powered threat detection
- **Real-time Updates**: Live timestamp and threat level indicators

### Security Considerations
This is a defensive security tool for monitoring anti-national campaigns. The code includes:
- Content analysis for detecting threats to national security
- Integration capabilities with law enforcement portals
- Real-time threat assessment and reporting

### No Build Process
This project requires no build tools, package managers, or compilation steps. All dependencies are loaded via CDN.