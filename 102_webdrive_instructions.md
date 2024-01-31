# Uploading to Department Web Hosting

This document will walk you through setup of the **studentweb** folder and subfolders, and the uploading of documents to the WWU computer science department web hosting using.

To see an up to date list of CS Lab rooms visit: <https://support.cs.wwu.edu/home/survival_guide/resources/Labs.html>

---

## Option 1: Log into a Linux machine on campus

Follow these instructions if you are on campus and in a Linux lab. You will need a method to transfer your lab files onto the lab computer (flash drive, email, SCP, etc.). Once you have a method of transfering your lab files follow these steps.

1. Log into the lab computer. This will be your WWU CS login (this is different from your standard WWU login). If you forgot your login, you can reset your password via <https://password.cs.wwu.edu/>

2. Open a file explorer (Activities > Files) and locate your Lab files, these may be on a flashdrive or where ever you put them.

3. Open a new file explorer window (Files > New Window) and navigate to the "Other Locations" tab.

![The San Juan Mountains are beautiful!](/img/O1-1.png "San Juan Mountains")

4. Select "Debian GNU/Linux". You will see a list of many folders (academic, bin, boot, etc.). Ignore these and scroll down until you see the "web" folder.

5. Select the "web" folder and then the "students" directory. This may load for a moment.

6. Search for your WWU username, you may want to utilize the search feature. Enter into this subfolder.

7. This is where you will upload your lab files, this should include your "secret folder". **Make sure none of your files have spaces in them, instead use underscore '\_' or dash '-'**.

8. Notice the file path at the top of the file explorer, this will be similar to your url you will submit.

![The San Juan Mountains are beautiful!](/img/O1-2.png "San Juan Mountains")

9. Navigate to a browser and type the following url:
   `https://studentweb.cs.wwu.edu/~/username/super_secret/lab3/index.html`

   - Replace `username` with your WWU username.
   - Replace `super_secret` with your secret folder name.
   - Replace `lab3` with the name of the folder containing your lab files.
   - Replace `index.html` with the name of your index file if needed.

10. Confirm that your website is appearing in a browser. Once confirmed, **this will be the url that you submit**.

11. Congrats! you've uploaded to the web drive.

## Option 2: Log into a Windows machine on campus

Follow these instructions if you are on campus and in a Windows lab. You will need a method to transfer your lab files onto the lab computer (flash drive, email, SCP, etc.). Once you have a method of transfering your lab files follow these steps.

**If a computer turns on and is using the Linux operating system, and you would like to switch. Shut down the computer and turn it back on. Then select the "Windows" option with the arrow keys when the computer boots up.**

\*You will not be able to switch to windows if you are in a linux only lab. In this case, follow the steps in option 1.

1. Log into the lab computer. This will be your WWU CS login (this is different from your standard WWU login). If you forgot your login, you can reset your password via <https://password.cs.wwu.edu/>

## Option 3: Remotely via SSH and FileZilla

Follow the steps in this section if you are trying to upload files from your personal computer while **not** connected to the university wifi.

1. Connect to the internet through the university VPN.
   1. In a browser open the CS support documentation. <https://support.cs.wwu.edu/home/access/wwu_vpn/index.html>.
   2. Select the operating system (Windows, MacOS, or Linux) and follow th CS support tutorial.
2. Download and install **FileZilla**.
   1. In a browser open <https://filezilla-project.org/download.php?type=client>
   2. Download the FileZilla client, ensure you download the file for your operating system

https://support.cs.wwu.edu/home/survival_guide/resources/Department_Web_Hosting.html

https://studentweb.cs.wwu.edu/~/duffiep/cyclestreets.jpg

https://www.markdownguide.org/basic-syntax/

https://support.cs.wwu.edu/home/survival_guide/tools/SSH.html
