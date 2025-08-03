# 🚀 Render Deployment Guide

<!-- Last updated: 2025-08-03 16:31 UTC -->

## Quick Deploy to Render

[![Deploy to Render](https://render.com/images/deploy-to-render.svg)](https://render.com)

## Environment Variables Required

Set these variables in Render:

| Variable | Description | Required |
|----------|-------------|----------|
| `BOT_TOKEN` | Your Telegram bot token from @BotFather | ✅ Yes |
| `GOOGLE_MAPS_API_KEY` | Google Maps API key for distance calculations | ❌ Optional |
| `AUTHORIZED_USERS` | Comma-separated user IDs (not used, bot is open) | ❌ Optional |
| `ELD_URL` | Fallback ELD URL (not needed if drivers_config.json is set) | ❌ Optional |

## How to Deploy

1. **Fork this repository** or **Import to Render**
2. **Connect to Render:**
   - Go to [render.com](https://render.com)
   - Sign up with GitHub
   - Click "New +" → "Web Service"
   - Connect your GitHub repository
   - Choose this repository

3. **Configure Service:**
   - **Name:** Location Updater Bot
   - **Environment:** Python 3
   - **Build Command:** `pip install -r requirements.txt`
   - **Start Command:** `python main.py`
   - **Instance Type:** Free (or Starter for better performance)

4. **Set Environment Variables:**
   - In Render dashboard, go to "Environment"
   - Add `BOT_TOKEN` with your actual bot token
   - Add `GOOGLE_MAPS_API_KEY` if you have one

5. **Deploy:**
   - Click "Create Web Service"
   - Render will automatically build and deploy
   - Your bot will be running 24/7

## Features

- 🚛 Track multiple drivers with individual assignments
- 💨 Real-time speed tracking
- 📍 Live location updates
- 📏 Distance calculations with multiple APIs
- 🔄 Automatic updates every 2 hours
- 🎯 Destination management
- 🔐 Group-based access

## Commands

- `/start` - Welcome message
- `/help` - Show help
- `/location` - Get driver location
- `/distance [address]` - Calculate distance + auto-updates
- `/drivers` - List all drivers
- `/setdriver [name]` - Assign driver to group
- `/setdestination [address]` - Set destination
- `/stop` - Stop auto-updates

## Support

For issues or questions, check the main README.md file.
