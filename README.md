# Uploading to Department Web Hosting

This document will walk you through setup of the **studentweb** folder and subfolders, and the uploading of documents to the WWU computer science department web hosting using.

To see an up to date list of CS Lab rooms visit: <https://support.cs.wwu.edu/home/survival_guide/resources/Labs.html>

---

## Option 1: Log into a Linux machine on campus

Follow these instructions if you are on campus and in a Linux lab. You will need a method to transfer your lab files onto the lab computer (flash drive, email, SCP, etc.). Once you have a method of transferring your lab files follow these steps.

1. Log into the lab computer. This will be your WWU CS login (this is different from your standard WWU login). If you forgot your login, you can reset your password via <https://password.cs.wwu.edu/>

2. Open a file explorer (Activities > Files) and locate your Lab files, these may be on a flashdrive or where ever you put them.

3. Open a new file explorer window (Files > New Window) and navigate to the "Other Locations" tab.

![The San Juan Mountains are beautiful!](/img/O1-1.png "San Juan Mountains")

4. Select "Debian GNU/Linux". You will see a list of many folders (academic, bin, boot, etc.). Ignore these and scroll down until you see the "web" folder.

5. Select the "web" folder and then the "students" directory. This may load for a moment.

6. Search for your WWU username, you may want to utilize the search feature. Enter into this subfolder.

7. This is where you will upload your lab files, this should include your "secret folder". **Make sure none of your files have spaces in them, instead use underscore '\_' or dash '-'**.

8. Notice the file path at the top of the file explorer, this will be similar to your URL that you will submit.

![alt](/img/O1-2.png "title")

9. Navigate to a browser and type the following URL:
   `https://studentweb.cs.wwu.edu/~/username/super_secret/lab3/index.html`

   - Replace `username` with your WWU username.
   - Replace `super_secret` with your secret folder name.
   - Replace `lab3` with the name of the folder containing your lab files.
   - Replace `index.html` with the name of your index file if needed.

10. Confirm that your website is appearing in a browser. Once confirmed, **this will be the URL that you submit**.

11. Congrats! You've uploaded to the web drive.

## Option 2: Log into a Windows machine on campus

Follow these instructions if you are on campus and in a Windows lab. You will need a method to transfer your lab files onto the lab computer (flash drive, email, SCP, etc.). Once you have a method of transferring your lab files follow these steps.

**If a computer turns on and is using the Linux operating system, and you would like to switch. Shut down the computer and turn it back on. Then select the "Windows" option with the arrow keys when the computer boots up.**

\*You will not be able to switch to windows if you are in a linux only lab. In this case, follow the steps in option 1.

1. Log into the lab computer. This will be your WWU CS login (this is different from your standard WWU login). If you forgot your login, you can reset your password via <https://password.cs.wwu.edu/>

## Option 3: Remotely via SSH and FileZilla

Follow the steps in this section if you are trying to upload files from your personal computer while **not** connected to the university wifi.

1. Connect to the internet through the university VPN.

   1. In a browser open the CS support documentation. <https://support.cs.wwu.edu/home/access/wwu_vpn/index.html>.
   2. Select the operating system (Windows, MacOS, or Linux) and follow the CS support tutorial.

2. Download and install **FileZilla**.

   1. In a browser open <https://filezilla-project.org/download.php?type=client>
   2. Download the FileZilla client, ensure you download the file for your operating system

3. Open FileZilla and locate the quick connect options at the top of the application.

![alt](/img/O3-1.png "title")

4. Fill out the fields for quick connect:

   - Host: `linux.cs.wwu.edu`
   - Username: `Your WWU CS Username`
   - Password: `Your WWU CS Password`
   - Port: `992`

5. Press "Quickconnect". If the operation does nothing, ensure you have the correct username and password, and double check the port and host.

6. An "Unknown host key" dialog box will appear asking, simply click "OK".

![alt](/img/O3-2.png "title")

7. After a moment you should see files on the righthand side (Remote Site) of FileZilla.

![alt](/img/O3-3.png "title")

9. In the "Remote site:" dialog box type:
   `/web/students/username/super_secret`

   - Replace `username` with your WWU username.
   - Replace `super_secret` with your secret folder name.

10. This is where you will upload your lab files, this should include your "secret folder". **Make sure none of your files have spaces in them, instead use underscore '\_' or dash '-'**.

11. On the left side of FileZilla (Local Site) navigate to your lab via the "Local Site" dialog box, or the user interface. This will be individual for each person, make sure you know exactly where you are storing your files.

12. Simply drag the lab folder from the Local site to the Remote site (left to right). This will upload the files and in a moment you should see the lab folder appear on the Remote site.

13. Navigate to a browser and type the following url:
    `https://studentweb.cs.wwu.edu/~/username/super_secret/lab3/index.html`

    - Replace `username` with your WWU username.
    - Replace `super_secret` with your secret folder name.
    - Replace `lab3` with the name of the folder containing your lab files.
    - Replace `index.html` with the name of your index file if needed.

14. Confirm that your website is appearing in a browser. Once confirmed, **this will be the url that you submit**.

15. Congrats! you've uploaded to the web drive.

<!-- https://support.cs.wwu.edu/home/survival_guide/resources/Department_Web_Hosting.html

https://studentweb.cs.wwu.edu/~/duffiep/cyclestreets.jpg

https://www.markdownguide.org/basic-syntax/

https://support.cs.wwu.edu/home/survival_guide/tools/SSH.html -->
