Simple Video Downloader Script
This repository contains a simple Python script for downloading videos from various websites. It uses the powerful yt-dlp library to handle the heavy lifting of extracting video streams from complex sites.

This script is intended for use in environments like Google Colab, where dependencies can be easily installed.

Requirements
Python 3.x

The yt-dlp library

(Optional but Recommended) FFmpeg: yt-dlp uses this to merge separate video and audio streams (which is how sites like YouTube serve 1080p+ quality). Google Colab comes with this pre-installed.
✅ What It CAN Download (Most Public Content)

The yt-dlp library is a beast. It's designed to work on hundreds of sites, including:
Major Platforms: YouTube, Twitter/X, Facebook, Vimeo, TikTok, Instagram, etc.
News & Media: Links to videos embedded in news articles from sites like the BBC, NBC, etc.
Classic Sites: Dailymotion, eBaum'sWorld, and many more.
Your Own Private Videos: If you are logged into a service (like YouTube) and want to download a private video that you have access to, yt-dlp can be configured to use your browser's cookies to authenticate.

🛑 What It CANNOT Download (The Hard Limits)
The script will fail on the following types of content for very specific reasons:
DRM-Protected Content (The Bank Vault)
This is the big one. Services like Netflix, Hulu, Disney+, Amazon Prime Video, and Max use strong encryption called DRM (Digital Rights Management).
yt-dlp cannot (and will not) break this encryption. It's a downloading tool, not a decryption tool.
Videos You Can't See Anyway (The Locked Door)
If a video is "Private" on YouTube and it's not on your account (or shared with you), you can't see it. Neither can the script.
If a video is on a corporate intranet or private site that requires a special login or VPN you don't have, the script can't get in.
Platform "Cat & Mouse" (The Lock Change)
Sometimes, YouTube or another big site will change its website code. For a day or two, yt-dlp might break and stop working.
