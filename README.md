# HistoryAsCode v2

## 🚀 A New Beginning

After careful reflection on the original vision in HAC.txt, we're rebuilding HistoryAsCode from the ground up to truly serve computational historians. The previous version had drifted toward being a generic academic platform. This v2 refocuses on our core mission: making computational methods in history as transparent, citable, and valuable as the historical insights they produce.

## 📚 What is HistoryAsCode?

HistoryAsCode is where computational historians share not just their findings, but **HOW** they found them. It's a platform built on the principle that "process is as important as product."

### Three Pillars

1. **The Lab** 🔬 - Your computational history workspace
   - Git-backed projects with full transparency
   - Visual workflow builders showing research progress
   - Method templates for spatial, textual, and network analysis
   - Team collaboration tools

2. **The Journal** 📖 - Publish computational narratives
   - Articles that link directly to code and data
   - Interactive visualizations embedded in publications
   - Transparent peer review focusing on methods
   - DOI assignment for reproducible research

3. **The Directory** 🔍 - Discover and connect
   - Find researchers by method expertise
   - Cross-institutional collaboration matching
   - See who uses which tools and how
   - Break down academic silos

## 🛠️ Technical Stack

- **Frontend**: SvelteKit (simpler than Next.js, perfect for our needs)
- **Backend**: Supabase (PostgreSQL + Auth + Realtime + Storage)
- **Deployment**: Cloudflare Pages
- **Language**: TypeScript
- **Task Management**: Task Master AI

## 🏗️ Current Status

This is a complete rebuild focusing on simplicity and the core vision. We're using Task Master to manage development systematically.

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/HistoryAsCode/historyascode-v2.git
   cd historyascode-v2
   ```

2. **Set up environment variables**
   ```bash
   cp .env.example .env
   # Add your API keys to .env
   ```

3. **Configure Task Master** (for development management)
   ```bash
   # You need at least one AI API key in .env
   npm install -g task-master-ai
   task-master parse-prd .taskmaster/docs/prd.txt
   task-master models --setup
   ```

4. **View development tasks**
   ```bash
   task-master list
   task-master next
   ```

## 🎯 Core Innovation

HistoryAsCode is the first platform to treat computational methods in history as first-class citizens. We make the research process as valuable, citable, and discoverable as the research outcomes.

## 📋 Development Roadmap

See `.taskmaster/docs/prd.txt` for the complete Product Requirements Document.

### Phase 1: Foundation (Current)
- Core database schema with methods as first-class citizens
- Basic SvelteKit application structure  
- Supabase authentication and user profiles
- Simple project creation in Lab

### Phase 2: Lab Development
- GitHub repository integration
- Visual workflow builder
- Method-specific templates
- Team collaboration

### Phase 3: Journal Publishing
- Rich article editor
- Code and data linking
- Peer review workflow
- DOI integration

### Phase 4: Directory Enhancement
- Advanced search with facets
- Skills-based matching
- Collaboration suggestions

## 🤝 Contributing

This is an active rebuild. We're using Task Master to coordinate development. If you want to contribute:

1. Check current tasks: `task-master list`
2. Pick a task to work on
3. Create a feature branch
4. Submit a PR referencing the task ID

## 📄 License

[License details to be determined]

---

*"Making computational history methods as transparent and valuable as the insights they produce."*