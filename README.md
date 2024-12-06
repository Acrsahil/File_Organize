File Organizer using Python

This project automates the organization of files in the Downloads folder based on their file types or names. It provides two approaches: one using watchdog for real-time monitoring of file creation and another using os and shutil for batch processing.
Features

    Real-Time File Monitoring:
        Monitors the Downloads folder for newly added files.
        Automatically moves files to appropriate folders based on their extensions.
        Supports extensions for videos, images, music, documents, and PDFs.

    Batch File Processing:
        Processes all existing files in the Downloads folder.
        Moves files based on specific extensions and predefined rules.

Folder Structure

Ensure the following folder structure exists before running the script:

/home/window/Downloads/           # Folder to track files.
/home/window/Documents/ViberDownloads/
                                  # Destination for Viber-specific files.
/home/window/Music/               # Destination for music files.
/home/window/Pictures/            # Destination for image files.
/home/window/Videos/              # Destination for video files.
/home/window/Documents/Mountcare/ # Destination for Mountcare-related files.
/home/window/Documents/Pdf/       # Destination for PDF files.

Scripts
1. Real-Time File Monitoring

    File: watchdog_file_handler.py
    Description:
        Uses the watchdog library to monitor the Downloads folder.
        Moves newly added files to the appropriate destinations.
    Key Functions:
        determine_destination: Determines the destination folder based on the file extension.
        on_created: Handles the file creation event and moves the file.

2. Batch File Processing

    File: batch_file_processor.py
    Description:
        Processes all files in the Downloads folder and moves them to their respective folders.
    Key Functions:
        MoveDocument: Iterates over files in the source folder and moves them based on predefined rules.

How to Run
1. Real-Time File Monitoring

    Install dependencies:

pip install watchdog

Run the script:

    python watchdog_file_handler.py

    The script will monitor Downloads and organize files as they are added.

2. Batch File Processing

    Run the script:

    python batch_file_processor.py

    The script will process all existing files in Downloads and move them to appropriate destinations.

Customization

    Update the paths to match your folder structure.
    Add or modify file extensions in the determine_destination method or MoveDocument function to support additional file types.

Example Logs

Real-Time Monitoring:

Moved: file.mp4 to /home/window/Videos/
Moved: image.jpg to /home/window/Pictures/

Batch Processing:

Moved file ('file', '.mp4')
Moved file ('image', '.jpg')

Dependencies

    Python 3.x
    Modules:
        watchdog
        os
        shutil

Note

    Ensure the destination folders exist to avoid errors.
    The scripts handle only files, not directories.
