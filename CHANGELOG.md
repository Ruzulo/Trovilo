# Changelog

All notable changes to the Trovilo project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## [Unreleased]

## [0.1.0] - 2026-02-12

### Added
- 🎉 Initial repository setup
- ✅ Google Posts Generator workflow (Quest 2.1)
  - Automated GBP post creation in 4 categories
  - Claude Sonnet 4 integration
  - Structured JSON output
- 📚 Complete documentation:
  - README with business overview
  - n8n setup guide
  - Prompt templates
  - .gitignore for security
- 🔧 n8n MCP integration for Claude Desktop
- 📝 Custom Skill for persistent knowledge (`/mnt/skills/user/trovilo-setup/`)

### Technical Details
- n8n Cloud: https://trovilo.app.n8n.cloud
- Workflow ID: e0ccPj7aQZcNFRUa
- Model: claude-sonnet-4-20250514

### Learnings
- Code Nodes > Set Nodes for template literals
- Raw/Custom body type for pre-built JSON
- Separate API body preparation from HTTP request

---

## Geplante Features

### Q1 2026
- [ ] Review Response Generator (Quest 2.2)
- [ ] Keyword Research Automation (Quest 2.3)
- [ ] Claude Prompt Library (Quest 2.4)
- [ ] Beta Customer Workflows (Quest 6-9)

### Q2 2026
- [ ] GBP Performance Reporting
- [ ] Automated Review Request System
- [ ] Multi-Client Management Dashboard

---

## Version History

### Release Naming
- Format: `MAJOR.MINOR.PATCH`
- Major: Breaking changes or major features
- Minor: New workflows/features
- Patch: Bug fixes or minor improvements

---

_Started: 2026-02-12 (Sabbatical Day 73)_  
_Business Goal: 15k€/month by end of sabbatical (28.02.2026)_