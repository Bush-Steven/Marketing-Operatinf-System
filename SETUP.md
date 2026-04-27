"""
Setup and Installation Guide for Marketing Operating System
"""

# Marketing Operating System - Setup Guide

## 📋 Prerequisites

- Python 3.10+
- Anthropic API Key (Claude)
- Telegram Bot Token
- pip (Python package manager)

## 🚀 Installation Steps

### 1. Clone or Download Repository
```bash
git clone https://github.com/Bush-Steven/Marketing-Operatinf-System.git
cd Marketing-Operatinf-System
```

### 2. Create Virtual Environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables

Copy `.env.example` to `.env`:
```bash
cp .env.example .env
```

Edit `.env` with your credentials:
```
ANTHROPIC_API_KEY=sk-ant-...
TELEGRAM_BOT_TOKEN=your_bot_token_here
DATABASE_URL=sqlite:///marketing_system.db
ENVIRONMENT=development
LOG_LEVEL=INFO
```

#### Getting Your API Keys:

**Anthropic API Key:**
1. Go to https://console.anthropic.com
2. Create an account
3. Navigate to API keys
4. Create and copy your key

**Telegram Bot Token:**
1. Message @BotFather on Telegram
2. Send `/newbot` command
3. Follow instructions to create bot
4. Copy the token provided

### 5. Run the System

```bash
python main.py
```

You should see:
```
✅ Marketing Orchestrator initialized with 4 specialist agents
✅ Telegram bot initialized
✅ Bot is running!
```

## 📱 Using Telegram Bot

Start your bot and send any of these commands:

### Content Creation Commands
```
/create_blog topic - Generate blog post
/create_social topic - Create social media content
/email_campaign type - Create email campaign
/content_calendar - Plan content calendar
```

### Campaign Management
```
/campaign_create name - Plan new campaign
/campaign_analyze - Analyze campaign performance
/report - Generate comprehensive report
```

### Analytics & Insights
```
/analytics - View performance metrics
/social_strategy - Develop social strategy
/agents - Show available agents
```

### System Commands
```
/help - Show all commands
/reset - Reset conversation context
/start - Welcome message
```

## 🏗️ Architecture Overview

The system consists of:

1. **Orchestrator** (`orchestrator/main.py`)
   - Routes commands to specialist agents
   - Manages conversation context
   - Synthesizes outputs

2. **Specialist Agents** (`agents/`)
   - `content_creator.py` - Content generation
   - `campaign_manager.py` - Campaign planning
   - `analytics.py` - Performance analysis
   - `social_media.py` - Social strategies

3. **Telegram Bot** (`telegram_bot/bot.py`)
   - Command handlers
   - Message processing
   - User interaction

4. **Main Entry** (`main.py`)
   - System initialization
   - Orchestrator setup
   - Bot startup

## 🔧 Configuration

### Customizing Agent Behavior

Edit `orchestrator/main.py` to:
- Add new specialist agents
- Modify system prompts
- Change routing logic
- Adjust conversation context

### Adding New Commands

1. Add command handler in `telegram_bot/bot.py`
2. Add processing logic in orchestrator
3. Map to appropriate agent

### Database Setup

Create SQLite database:
```bash
python -c "from database.models import init_db; init_db()"
```

## 📊 Performance Tips

1. **Optimize Prompts** - Refine agent prompts for better outputs
2. **Cache Results** - Store common responses
3. **Batch Requests** - Process multiple commands efficiently
4. **Monitor Costs** - Track API usage

## 🐛 Troubleshooting

### Bot Not Responding
- Check TELEGRAM_BOT_TOKEN in .env
- Ensure internet connection
- Check logs for errors

### API Errors
- Verify ANTHROPIC_API_KEY is correct
- Check API quota/limits
- Ensure valid request format

### Database Issues
- Delete `marketing_system.db` to reset
- Check file permissions
- Verify DATABASE_URL in .env

## 📚 Additional Resources

- [Anthropic API Docs](https://docs.anthropic.com)
- [Telegram Bot API](https://core.telegram.org/bots/api)
- [Architecture Guide](./docs/ARCHITECTURE.md)
- [Agent Specifications](./docs/AGENTS.md)

## ✅ Verification

Verify installation:
```bash
python -c "import anthropic; from telegram.ext import Application; print('✅ All dependencies installed')"
```

## 📧 Support

For issues or questions:
1. Check logs in console output
2. Review documentation in `/docs`
3. Check .env configuration
4. Verify API credentials

---

**You're all set! 🎉 Start commanding your marketing system via Telegram.**
