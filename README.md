File Organizer

This project contains scripts that automate the organization of files in a specified directory. The scripts monitor file creation events and move files to appropriate folders based on their extensions or specific rules.
1. Watchdog File Organizer
Description

The Watchdog File Organizer uses the watchdog library to monitor a directory for new files and automatically move them to predefined folders based on their file types (e.g., videos, images, documents).
Features

    Real-time monitoring of a directory for file changes.
    Automatically organizes files into folders such as Videos, Music, Pictures, and Documents.
    Customizable folder structure and file type rules.

Requirements

    Python 3.x
    watchdog library (pip install watchdog)

Usage

    Set the paths for the target folders in the script:

Downloads = "/home/window/Downloads/"
Pictures = "/home/window/Pictures/"
Video = "/home/window/Videos/"

Run the script:

    python file_organizer_watchdog.py

    Any new file added to the monitored directory (Downloads) will be moved to the appropriate folder.

2. Manual File Organizer
Description

The Manual File Organizer scans a directory and manually organizes files by moving them to specific folders based on their extensions. It includes support for custom rules such as handling specific folder names or unique file types.
Features

    Scans a directory and moves files to their respective folders.
    Supports a wide range of file types, including videos, images, PDFs, and more.
    Allows custom logic for specific files or folders.

Requirements

    Python 3.x
