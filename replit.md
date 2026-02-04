# Telegram Music Player Bot

## Overview
A Telegram Music Player bot that streams audio in Telegram voice chats. Plays music from YouTube and optionally Spotify playlists.

## Project Structure
- `main.py` - Main bot application with all command handlers
- `config.py` - Configuration loader from environment variables
- `core/` - Core functionality modules:
  - `stream.py` - Audio streaming logic
  - `song.py` - Song representation
  - `funcs.py` - Utility functions (YouTube/Spotify integration)
  - `queue.py` - Music queue management
  - `groups.py` - Group chat management
  - `admins.py` - Admin permission checks
  - `decorators.py` - Command decorators
- `lang/` - Language files for multi-language support
- `theme/` - Bot theme assets

## Required Environment Variables (Secrets)

### Required:
- `API_ID` - Telegram API ID from my.telegram.org
- `API_HASH` - Telegram API Hash from my.telegram.org  
- `SESSION` - Pyrogram session string (generate using @genstr_robot or genStr.py)
- `BOT_TOKEN` - Telegram Bot Token from @BotFather

### Optional:
- `SUDOERS` - Space-separated list of sudo user IDs
- `PREFIX` - Command prefix (default: !)
- `LANGUAGE` - Default language (default: en)
- `QUALITY` - Stream quality: high/medium/low (default: high)
- `STREAM_MODE` - audio or video (default: audio)
- `ADMINS_ONLY` - Restrict playback to admins only (default: False)
- `SPOTIFY_CLIENT_ID` - Spotify API client ID (for Spotify playlists)
- `SPOTIFY_CLIENT_SECRET` - Spotify API client secret

## Bot Commands
- `/start` - Start the bot
- `/help` - Show help message
- `/play` or `/p` - Play a song (search or URL)
- `/stream` or `/radio` - Play live stream/radio
- `/pause` or `/ps` - Pause playback
- `/resume` or `/rs` - Resume playback
- `/skip` or `/next` - Skip to next song
- `/stop` or `/leave` - Stop and leave voice chat
- `/mute` or `/m` - Mute the stream
- `/unmute` or `/um` - Unmute the stream
- `/queue` or `/list` - Show queue
- `/shuffle` or `/mix` - Shuffle queue
- `/loop` or `/repeat` - Toggle loop mode
- `/mode` or `/switch` - Switch between audio/video mode
- `/lang` - Change bot language
- `/playlist` or `/pl` - Import YouTube/Spotify playlist
- `/export` or `/ep` - Export queue
- `/import` or `/ip` - Import queue from file
- `/ping` - Check bot latency
- `/repo` - Show repository info

## Running the Bot
The bot runs as a console application. Simply execute:
```
python main.py
```

## Dependencies
- Python 3.11+
- pyrogram/pyrogrammod - Telegram client
- py-tgcalls - Voice chat streaming
- yt-dlp - YouTube downloading
- spotipy - Spotify integration (optional)
- ffmpeg - Audio processing (system dependency)

## Recent Changes
- Feb 2026: Initial Replit environment setup
