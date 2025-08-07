# Netflix-Style Resume - Product Requirements Document

## Project Overview
Transform a traditional resume into an interactive Netflix-style web experience that showcases professional experience, skills, and projects as if they were TV shows and movies on a streaming platform.

## Current State
- We have a basic HTML template with Netflix UI styling
- Contains placeholder content that needs to be replaced with actual resume data
- Single-file implementation (index.html) ready for GitHub Pages deployment

## Core Requirements

### 1. Content Integration
- **Parse and integrate** the actual resume data from the provided resume file
- **Replace all placeholder content** with real information:
  - Name and title in hero section
  - Actual work experience with real companies, dates, and achievements
  - Real skills with appropriate proficiency levels
  - Actual projects with descriptions and links
  - Education and certifications
  - Contact information

### 2. Visual Design Requirements
- **Maintain Netflix aesthetic** throughout:
  - Dark theme (#141414 background)
  - Red accent color (#e50914)
  - Card-based layout with hover effects
  - Smooth animations and transitions

- **Content Cards** should:
  - Scale on hover (transform: scale(1.3))
  - Show additional information on hover
  - Use gradient overlays for text readability
  - Be organized in horizontal scrollable rows

### 3. Information Architecture

#### Hero Section
- Display name as the main "show title"
- Professional title as "Season X" or subtitle
- Brief professional summary as the "show description"
- Two CTAs: "Play Intro" (link to video/demo) and "More Info" (opens modal)

#### Experience Section ("Continue Watching My Career")
- Each job as a "season" or "episode"
- Show company, role, and dates
- Include 2-3 key achievements per role
- Display as large cards with gradient backgrounds

#### Skills Section ("Trending Skills Right Now")
- Group skills by category (Frontend, Backend, Tools, etc.)
- Show proficiency as star ratings or match percentages
- Make cards clickable to show more details in modal

#### Projects Section ("Award-Winning Projects")
- Feature 4-6 top projects
- Include metrics (users, stars, performance stats)
- Show tech stack as tags
- Link to GitHub/live demo

#### Education Section ("Educational Background")
- Degree and university as main content
- Certifications as separate cards
- Include completion years and any honors

### 4. Interactive Features

#### Modal System
- Click any card to open detailed modal
- Modal should contain:
  - Expanded information about the item
  - Links to relevant resources
  - Technologies used
  - Impact metrics
  - "Contact Me" and "Download Resume" CTAs

#### Navigation
- Fixed header with navigation links
- Smooth scroll to sections
- "Profile" icon with initials in top right

#### Search (Optional Enhancement)
- Functional search bar that filters content
- Shows results as you type
- Highlights matching cards

### 5. Technical Requirements

#### Performance
- Page should load in under 2 seconds
- Smooth animations (60fps)
- Optimized for mobile devices

#### Compatibility
- Work on Chrome, Firefox, Safari, Edge
- Responsive design for mobile/tablet/desktop
- Accessible (proper ARIA labels, keyboard navigation)

#### Deployment
- Single HTML file (inline CSS and JavaScript)
- Ready for GitHub Pages hosting
- No external dependencies except fonts

### 6. Content Tone & Style

- **Write descriptions as episode/show summaries**:
  - "Watch as Jake tackles the challenge of scaling to 1M users..."
  - "In this thrilling season, our protagonist leads a team through..."
  
- **Use entertainment industry terms**:
  - Jobs = Seasons/Series
  - Projects = Feature Films/Specials
  - Skills = Genre Specialties
  - Achievements = Awards/Accolades

### 7. Special Features to Add

#### Auto-playing Preview (Optional)
- On hover, show a brief "preview" of the role/project
- Could be animated text or a mini slideshow

#### Percentage Match
- Show "match percentage" for skills (e.g., "98% Match")
- Based on proficiency level

#### My List
- Section for "positions I'm interested in" or "technologies I'm learning"

#### Coming Soon
- Section for current learning goals or upcoming certifications

### 8. Data Structure Example

```javascript
const resumeData = {
  hero: {
    name: "Full Name",
    title: "Senior Developer",
    tagline: "Season 5 • Full Stack Series",
    summary: "Brief professional summary...",
    email: "email@example.com",
    linkedin: "linkedin.com/in/username",
    github: "github.com/username"
  },
  experience: [
    {
      company: "Company Name",
      role: "Job Title",
      period: "2020 - Present",
      description: "Episode summary...",
      achievements: ["Achievement 1", "Achievement 2"],
      technologies: ["React", "Node.js"],
      matchPercentage: 98
    }
  ],
  skills: {
    frontend: ["React: 5/5", "Vue: 4/5"],
    backend: ["Node.js: 5/5", "Python: 4/5"],
    tools: ["Docker: 4/5", "AWS: 4/5"]
  },
  projects: [
    {
      name: "Project Name",
      description: "Brief description",
      metrics: "5K+ users",
      technologies: ["React", "Node.js"],
      githubUrl: "github.com/...",
      liveUrl: "https://..."
    }
  ]
}
```

## Success Criteria
1. ✅ All placeholder content replaced with real resume data
2. ✅ Maintains Netflix look and feel
3. ✅ All interactive features working (modals, navigation, hover effects)
4. ✅ Deploys successfully to GitHub Pages
5. ✅ Loads quickly and works on mobile
6. ✅ Creates a memorable, shareable experience

## Delivery
- Single `index.html` file with all code inline
- README.md with deployment instructions
- Optional: Separate `data.json` for easier updates

## Notes for Implementation
- Prioritize getting real content in first, then enhance interactivity
- Keep the Netflix metaphor consistent throughout
- Make sure contact information is easily accessible
- The resume should be fun but still professional
- Include comments in code for easy future modifications
