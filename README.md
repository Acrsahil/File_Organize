# **File Organizer Project**

This repository contains two Python scripts designed to automate the organization of files. The scripts use different approaches to monitor and organize files based on their extensions, making file management efficient and hassle-free.

---

## **1. Watchdog File Organizer**

### **Description**  
The *Watchdog File Organizer* uses the `watchdog` library to monitor a directory in real-time. It automatically moves newly created files to predefined folders based on their extensions.

### **Features**  
* Real-time monitoring of the specified folder.  
* Automatically organizes files into categories such as Videos, Music, Pictures, PDFs, and Documents.  
* Flexible and customizable folder destinations.

### **Requirements**  
* Python 3.x  
* `watchdog` library (install with `pip install watchdog`)  

### **Usage**  
1. Clone this repository:
   ```bash
   git clone https://github.com/Acrsahil/File_Organize
Navigate to the folder:

cd <your-repo-folder>

Open the script file_organizer_watchdog.py and update the paths to your directories:

Downloads = "/home/window/Downloads/"
Pictures = "/home/window/Pictures/"
Video = "/home/window/Videos/"

Run the script:

    python file_organizer_watchdog.py

    The script will monitor the Downloads folder and move new files to their corresponding folders.

2. Manual File Organizer
Description

The Manual File Organizer scans a specified directory for existing files and moves them to predefined folders based on their extensions or specific naming conventions.
Features

    Organizes files already present in the folder.
    Supports a variety of file types, including videos, images, PDFs, and music files.
    Allows for customization of rules and folder destinations.

Requirements

    Python 3.x
    shutil library (included with Python)

Usage

    Open the script file_organizer_manual.py and configure the paths for source and target directories:

Downloads = "/home/window/Downloads/"
Music = "/home/window/Music/"

Run the script:

    python file_organizer_manual.py

    Files in the specified Downloads folder will be moved to their respective destinations.

Folder Structure

By default, the scripts use the following folder structure, which you can customize in the code:

/home/window/
├── Downloads/
├── Documents/
│   ├── Pdf/
│   ├── Mountcare/
│   └── ViberDownloads/
├── Music/
├── Pictures/
├── Videos/

Detailed Explanation of Code
Watchdog File Organizer Code Explanation

    Folder Paths
    These variables specify the paths for the Downloads and other destination folders. You can modify these paths as per your system.

    Downloads = "/home/window/Downloads/"
    Pictures = "/home/window/Pictures/"
    Video = "/home/window/Videos/"
    Music = "/home/window/Music/"
    Pdf = "/home/window/Documents/Pdf/"
    Document = "/home/window/Documents/"

    MyHandler Class
    The MyHandler class inherits from FileSystemEventHandler. It monitors the Downloads folder for new files and categorizes them based on file extensions. It has a method determine_destination that checks the file extension and moves the file to the appropriate folder.

    Real-Time Monitoring
    The Observer class from the watchdog library is used to monitor the Downloads folder. It triggers the on_created method whenever a new file is created. The on_created method checks the file's extension and moves it to the correct folder.

    Running the Script
    To run the script, just execute it, and it will start monitoring your Downloads folder. Any new file will be moved to the corresponding folder based on its type (e.g., music files to the Music folder, images to Pictures, etc.).

Manual File Organizer Code Explanation

    MoveDocument Function
    The MoveDocument function scans the Downloads folder for files. Based on the file extension (e.g., .m4a, .jpg, .mp4), it moves the file to the appropriate destination (e.g., Music, Pictures, Videos).
    You can add or modify the logic in this function to handle more file types or specific naming conventions.

    File Types Supported
    The script currently supports moving the following file types:
        .m4a to the Music folder
        .jpg or .png to the Pictures folder
        .mp4 to the Videos folder
        .pdf (can be added for Pdf folder if needed)

    Running the Script
    To use the script, just call the MoveDocument function, passing the source folder (Downloads). The script will scan the folder and move the files based on their extensions.

Notes

    Ensure the specified folder paths exist before running the scripts. Modify the code to create them automatically if needed.
    The Watchdog File Organizer is ideal for real-time file management, while the Manual File Organizer is more suited for periodic organization tasks.
    These scripts are primarily designed for Linux systems (tested on Arch Linux with Hyprland). Adjust paths accordingly for other operating systems.

Feel free to contribute to this project or suggest improvements! Happy organizing! 🚀


This `README.md` file provides a thorough explanation of both the *Watchdog File Organizer* and *Manual File Organizer* scripts, including their features, usage instructions, and code explanations. It also includes information about the folder structure and customization options for the user.
