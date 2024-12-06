File Organizer using Python

This project automates the organization of files in the Downloads folder based on their file types or names. It provides two solutions:

    Real-Time File Monitoring using watchdog.
    Batch File Processing using os and shutil.

Features
1. Real-Time File Monitoring

    Monitors the Downloads folder for newly added files.
    Automatically moves files to predefined folders based on file extensions.

2. Batch File Processing

    Processes all existing files in the Downloads folder.
    Moves files to appropriate folders based on extensions or specific naming rules.

Folder Structure

Before running the scripts, ensure the following folders exist:

/home/window/Downloads/               # Source folder for tracking files.
/home/window/Documents/ViberDownloads/ # Destination for Viber-specific files.
/home/window/Music/                   # Destination for music files.
/home/window/Pictures/                # Destination for image files.
/home/window/Videos/                  # Destination for video files.
/home/window/Documents/Mountcare/     # Destination for Mountcare-related files.
/home/window/Documents/Pdf/           # Destination for PDF files.

Script Details
1. Real-Time File Monitoring

    File: watchdog_file_handler.py
    Description:
        Uses the watchdog library to detect newly created files in the Downloads folder.
        Moves files to corresponding folders based on their extensions.
    Key Methods:
        determine_destination: Identifies the destination folder for a file based on its extension.
        on_created: Handles the event triggered when a new file is created.

2. Batch File Processing

    File: batch_file_processor.py
    Description:
        Processes all files in the Downloads folder and organizes them into predefined destinations.
    Key Function:
        MoveDocument: Scans files in the folder and moves them based on extensions or specific naming conventions.

Supported File Types
Type	Extensions	Destination
Images	.jpg, .jpeg, .png, .gif, .bmp	/home/window/Pictures/
Videos	.mp4, .mkv, .avi, .mov, .wmv, etc.	/home/window/Videos/
Music	.mp3, .wav, .flac, .aac	/home/window/Music/
Documents	.doc, .docx, .ppt, .pptx, .xls, etc.	/home/window/Documents/
PDFs	.pdf	/home/window/Documents/Pdf/
Viber Files	Files named "Mountcare" or variations	/home/window/Documents/Mountcare/
How to Run
1. Real-Time File Monitoring

    Install dependencies:

pip install watchdog

Run the script:

    python watchdog_file_handler.py

    The script will start monitoring Downloads and organizing files as they are added.

2. Batch File Processing

    Run the script:

    python batch_file_processor.py

    The script will process all existing files in Downloads and move them to their appropriate destinations.

Customization

    Update the paths in the script to match your folder structure.
    Modify the determine_destination method or MoveDocument function to support additional file types or custom rules.

Example Logs
Real-Time Monitoring:

Moved: file.mp4 to /home/window/Videos/
Moved: image.jpg to /home/window/Pictures/

Batch Processing:

Moved file ('file', '.mp4')
Moved file ('image', '.jpg')

Dependencies

    Python 3.x
    Libraries:
        watchdog: For real-time monitoring.
        os, shutil: For file operations.

Install the required dependencies using:

pip install watchdog

Notes

    Ensure destination folders exist before running the script to avoid errors.
    Only files are handled; directories are ignored.
    Both scripts can be further enhanced to meet specific needs.
