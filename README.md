# Marketing Operating System

A Claude-powered marketing automation platform driven by AI agents, orchestrated through a primary coordinator, with specialist agents for content creation, analytics, campaign management, and direct Telegram integration.

## Architecture Overview

```
┌─────────────────────────────────────────────────────────┐
│           Telegram Bot Interface                        │
│         (Direct User Commands & Reports)                │
└─────────────────┬───────────────────────────────────────┘
                  │
┌─────────────────▼───────────────────────────────────────┐
│        Primary Agent Orchestrator                       │
│     (Task Routing & Coordination)                       │
└────┬──────────┬──────────────┬──────────────┬───────────┘
     │          │              │              │
     ▼          ▼              ▼              ▼
┌────────┐ ┌────────┐ ┌──────────┐ ┌──────────────┐
│Content │ │Campaign│ │ Analytics│ │Social Media  │
│Creator │ │Manager │ │  Agent   │ │   Manager    │
│Agent   │ │Agent   │ │          │ │              │
└────────┘ └────────┘ └──────────┘ └──────────────┘
```

## Key Components

- **Orchestrator**: Central coordination hub using Claude API
- **Specialist Agents**: Purpose-built agents for specific marketing functions
- **Telegram Bot**: Real-time command interface and reporting
- **Database Layer**: Campaign data, analytics, and state management
- **Knowledge Base**: Marketing strategies and best practices

## Features

- 🤖 AI-powered marketing automation
- 📊 Real-time analytics and reporting
- 📱 Telegram command interface
- 🎯 Campaign management and optimization
- 📝 Content generation and scheduling
- 📈 Performance tracking

## Quick Start

See [SETUP.md](./SETUP.md) for installation and configuration instructions.

## Directory Structure

```
.
├── agents/              # Specialist agent implementations
├── orchestrator/        # Primary orchestrator logic
├── telegram_bot/        # Telegram integration
├── database/           # Data models and persistence
├── utils/              # Shared utilities
├── config/             # Configuration files
├── prompts/            # Agent system prompts
└── tests/              # Test suite
```

## Documentation

- [Architecture Guide](./docs/ARCHITECTURE.md)
- [Agent Specifications](./docs/AGENTS.md)
- [Telegram Commands](./docs/TELEGRAM_COMMANDS.md)
- [API Reference](./docs/API.md)
