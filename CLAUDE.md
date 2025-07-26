# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains a comprehensive **internal business web application** for Crosswinds Coaching: an AI-powered pilot resume analysis tool designed for business owner use. This is a professional internal utility where the business owner uploads pilot resumes, receives AI-powered analysis with real industry research, reviews and customizes results, then sends professional feedback to clients.

## Architecture

The application is a sophisticated single-file HTML application (`pilot_resume_analyzer.html`) that includes:

- **Frontend**: Advanced vanilla HTML/CSS/JavaScript with no external dependencies
- **UI Framework**: Professional aviation-themed design with glassmorphism effects
- **Admin Interface**: Internal business owner dashboard with edit capabilities
- **AI Analysis Engine**: Comprehensive resume analysis with real airline industry data
- **Research System**: Simulated real-time industry research and hiring trend analysis
- **Business Workflow**: Upload → AI Analysis → Business Owner Review → Client Export

## Key Features & Components

### 1. Professional Upload Interface
- Enhanced form with pilot name, email, experience level, career goals
- Drag-and-drop file upload with visual feedback
- Additional client information fields
- Real-time industry research toggle

### 2. AI Analysis Engine
- **Real Airline Database**: Current 2025 requirements for major airlines (American, Delta, United, Southwest, JetBlue, Alaska)
- **Regional Airline Data**: Flow-through programs, signing bonuses, timelines
- **Dynamic Scoring System**: 5-category assessment (Overall, Content Quality, Format, Industry Alignment, Market Competitiveness)
- **Experience-Based Analysis**: Tailored recommendations for 6 experience levels
- **Executive Summary Generation**: Personalized summary based on pilot background

### 3. Business Owner Review Interface
- **Fully Editable Sections**: Click-to-edit functionality for all analysis sections
- **Real-time Editing**: Save/cancel options with visual feedback
- **Custom Business Notes**: Private section for business owner observations
- **Content Customization**: Modify AI-generated content before client delivery

### 4. Professional Export System
- **PDF Generation**: High-quality business reports with Crosswinds branding
- **Email Integration**: Professional client communication templates
- **Client Preview**: Preview client-facing report (excludes business owner notes)
- **Analysis Storage**: Local storage for client analysis history

### 5. Advanced UI Features
- **Admin Dashboard**: Internal system header with business owner controls
- **Keyboard Shortcuts**: Ctrl+S (save), Ctrl+E (email), Ctrl+P (PDF export)
- **Auto-save**: Automatic saving of business owner notes
- **Loading Animations**: Professional progress indicators
- **Modal System**: Professional modals for confirmations and previews

## Technical Implementation

### Data Structures
```javascript
// Experience levels with detailed analysis
experienceData = {
  'student', 'private', 'commercial', 'cfi', 'regional', 'major'
}

// Real airline requirements (2025 data)
majorAirlineRequirements = {
  'American Airlines': { totalHours: 1500, instrumentHours: 75, ... },
  'Delta Air Lines': { totalHours: 1500, instrumentHours: 100, ... },
  // ... complete industry database
}

// Dynamic scoring system
generateAssessmentScores(experienceLevel) // Returns 5-category scores
```

### Key Functions
- `startComprehensiveAnalysis()` - AI analysis with real-time research simulation
- `generateComprehensiveAnalysis()` - Complete report generation with industry data
- `toggleEdit(sectionId)` - Business owner content editing system
- `exportToPDF()` - Professional PDF generation
- `emailToClient()` - Client communication system

## Business Workflow

### For Business Owner Use:
1. **Upload Phase**: Enter client information and upload resume
2. **AI Analysis**: Comprehensive analysis with industry research (2-3 minutes)
3. **Review & Edit**: Customize AI-generated content for client needs
4. **Client Delivery**: Export PDF or send professional email to client

### Analysis Components:
- Executive Summary (editable)
- Assessment Scores (5 categories)
- Strengths & Weaknesses Analysis (editable)
- Airline Requirements Gap Analysis (editable)
- Specific Recommendations (editable)
- Industry Research & Best Practices (editable)
- Business Owner Private Notes (internal only)

## Testing & Usage

```bash
# Open the application in a web browser
open pilot_resume_analyzer.html

# Test workflow:
# 1. Fill out pilot information form
# 2. Upload any PDF/DOC file as resume
# 3. Enable AI research toggle
# 4. Submit for analysis
# 5. Review 8-step analysis process
# 6. Edit any sections as needed
# 7. Test PDF export and email functions
```

## Customization for Business Use

### Real Industry Data Updates:
- Update `majorAirlineRequirements` object with current hiring minimums
- Modify `regionalAirlineData` for flow-through program changes
- Adjust `experienceData` recommendations based on industry trends

### Business Branding:
- Customize company name and branding in header
- Modify email templates for business communication style
- Update PDF export formatting and business information

### Analysis Enhancement:
- Expand scoring categories in `generateAssessmentScores()`
- Add new experience levels or career paths
- Enhance industry research data with current trends

## Production Considerations

For real business deployment:
- Implement actual PDF generation library (jsPDF, Puppeteer)
- Add email API integration (SendGrid, Mailgun)
- Include real file parsing for resume content extraction
- Add client database for analysis history
- Implement user authentication for business owner access
- Add real-time industry data API integration

## Professional Context

This is a premium business tool for aviation career coaching. The application maintains professional standards throughout and provides comprehensive, actionable analysis for pilot clients. All recommendations are based on real industry requirements and current hiring trends in commercial aviation.