# HistoryAsCode v2 Setup Guide

## 🚀 Quick Start

### 1. Configure API Keys

You need to add at least one AI API key to `.env` for Task Master to work:

```bash
# Edit .env and add your API key(s)
nano .env
```

**Recommended keys:**
- `ANTHROPIC_API_KEY` - For Claude models (best for code generation)
- `PERPLEXITY_API_KEY` - For research features (highly recommended)

### 2. Parse the PRD to Generate Tasks

Once you have API keys configured:

```bash
# Install Task Master globally (if not already installed)
npm install -g task-master-ai

# Parse the Product Requirements Document
task-master parse-prd .taskmaster/docs/prd.txt

# View generated tasks
task-master list
```

### 3. Configure AI Models

Set up which AI models to use for different roles:

```bash
# Interactive setup (recommended)
task-master models --setup

# Or set manually
task-master models --set-main claude-3-5-sonnet-20241022
task-master models --set-research perplexity-llama-3.1-sonar-large-128k-online
```

### 4. Start Development

```bash
# See what to work on next
task-master next

# Get detailed task information
task-master show <task-id>

# Mark task as in-progress
task-master set-status --id=<task-id> --status=in-progress
```

## 📋 Next Steps

After Task Master is configured, the typical workflow is:

1. **Set up Supabase** (Task 4)
   - Create a new Supabase project
   - Add credentials to `.env`
   
2. **Initialize SvelteKit** (Task 5)
   - Set up the frontend framework
   - Configure TypeScript

3. **Create Database Schema** (Task 7)
   - Design tables for computational methods
   - Set up user profiles and projects

## 🛠️ Manual Task Creation (Alternative)

If you prefer to work without AI assistance, you can manually create tasks:

```bash
# Add a task manually
task-master add-task --title="Set up Supabase" --description="Create project and configure auth"

# Or edit .taskmaster/tasks/tasks.json directly
```

## 📚 Resources

- **PRD**: `.taskmaster/docs/prd.txt` - Complete product requirements
- **Task Master Docs**: Run `task-master --help` for all commands
- **MCP Integration**: See `.mcp.json` for Claude Code integration

## ⚠️ Important Notes

1. **Never edit** `.taskmaster/config.json` manually - use `task-master models`
2. **API Keys**: At least one AI provider key is required
3. **Git Integration**: Task Master works great with git worktrees for parallel development

---

For questions or issues, check the main README or create an issue on GitHub.