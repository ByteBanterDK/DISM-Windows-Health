<h1>DISM (Deployment Imaging Service and Management Tool)</h1>
<h2>Description:</h2>
DISM is a command-line tool used to service and prepare Windows images, including those used for Windows PE, Windows Recovery Environment (Windows RE), and Windows Setup. It can be used to check the health of a Windows image, scan for corruption, and restore health by repairing the corrupted image.

<h2>Key Objectives:</h2>
Check Health: Verify if the Windows image is flagged as corrupted.
Scan Health: Perform a detailed scan for image corruption.
Restore Health: Repair the Windows image using Windows Update files.

<h2>Utilities Used:</h2>
Utilities: Command Prompt
Environments Used:
Operating Systems: Windows 10, Windows Server 2019
Tools: Command Prompt

Check Health:

Command: DISM /Online /Cleanup-Image /CheckHealth
Explanation: This command checks if the image is flagged as corrupted by performing a quick scan to determine if there are any corruptions or not.

Scan Health:

Command: DISM /Online /Cleanup-Image /ScanHealth
Explanation: This command performs a more detailed scan of the Windows image to check for corruption. It logs the corruption it finds in the CBS log file but does not fix the issues.

Restore Health:

Command: DISM /Online /Cleanup-Image /RestoreHealth
Explanation: This command scans the image for corruption and repairs the image. It uses Windows Update to download the necessary files to replace the corrupted ones.

<h2>Program Walk-through:</h2>

Open Command Prompt as Administrator:

Search for "cmd" in the Windows search bar, right-click on "Command Prompt," and select "Run as administrator."
<img src="https://i.imgur.com/YWexohB.png">
Check Health:
Input the command: DISM /Online /Cleanup-Image /CheckHealth
This command performs a quick check to see if the image has been flagged as corrupted.
<img src="https://i.imgur.com/bomfflY.png"> <img src="https://i.imgur.com/2y8CVGC.png">
Scan Health:
Input the command: DISM /Online /Cleanup-Image /ScanHealth
This command performs a more comprehensive scan to check for any corruption within the image.
<img src="https://i.imgur.com/ZRiDkO5.png">
Restore Health:
Input the command: DISM /Online /Cleanup-Image /RestoreHealth
This command not only scans for corruption but also attempts to fix any issues found by downloading the necessary replacement files from Windows Update.
<img src="https://i.imgur.com/OdkZH81.png"> <img src="https://i.imgur.com/GRiCVdW.png">
