# Uploading to Department Web Hosting

This document will walk you through setup of the **studentweb** folder and subfolders, and the uploading of documents to the WWU computer science department web hosting using.

This document outlines 4 methods of uploading files to the web drive, although there are undoubtedly more. The options are:

1.  [Log into a Linux machine on campus](#option-1-log-into-a-linux-machine-on-campus)
2.  [Log into a Windows machine on campus](#option-2-log-into-a-windows-machine-on-campus)
3.  [Remotely via SSH and FileZilla](#option-3-remotely-via-ssh-and-filezilla)
4.  [Remotely via Terminal and SCP](#option-4-remotely-via-terminal-and-scp)

Options 1 and 2 require you to be on campus in a computer lab. Options 3 and 4 may be done anywhere.

Additionally, there is a section detailing [how to SSH into the lab machines](#extra-content-connecting-via-ssh).

> [!NOTE]
> To see an up to date list of CS Lab rooms visit: <https://support.cs.wwu.edu/home/survival_guide/resources/Labs.html>

---

## Option 1: Log into a Linux machine on campus

Follow these instructions if you are on campus and in a Linux lab. You will need a method to transfer your lab files onto the lab computer (flash drive, email, SCP, etc.). Once you have a method of transferring your lab files follow these steps.

1. Log into the lab computer. This will be your WWU CS login (this is different from your standard WWU login). If you forgot your login, you can reset your password via <https://password.cs.wwu.edu/>

2. Open a file explorer (Activities > Files) and locate your Lab files, these may be on a flash drive or where ever you put them.

3. Open a new file explorer window (Files > New Window) and navigate to the "Other Locations" tab.

   ![Image of Ubuntu file explorer](./img/O1-1.png)

4. Select "Debian GNU/Linux". You will see a list of many folders (academic, bin, boot, etc.). Ignore these and scroll down until you see the "web" folder.

5. Select the "web" folder and then the "students" directory. **This may load for a moment**.

6. Search for your WWU username, you may want to utilize the search feature. Enter into this subfolder.

7. This is where you will upload your lab files, this should include your "secret folder".

   > [!CAUTION]
   > Make sure none of your files have spaces in them, instead use underscore '\_' or dash '-'.

8. Notice the file path at the top of the file explorer, this will be similar to your URL that you will submit.

   ![Image of Ubuntu file explorer in the web drive](./img/O1-2.png)

9. Navigate to a browser and type the following URL:
   `https://studentweb.cs.wwu.edu/~/username/super_secret/lab3/index.html`

   - Replace `username` with your WWU username.
   - Replace `super_secret` with your secret folder name.
   - Replace `lab3` with the name of the folder containing your lab files.
   - Replace `index.html` with the name of your index file if needed.

10. Confirm that your website is appearing in a browser. Once confirmed, **this will be the URL that you submit**.

11. Congrats! You've uploaded to the web drive.

---

## Option 2: Log into a Windows machine on campus

Follow these instructions if you are on campus and in a Windows lab. You will need a method to transfer your lab files onto the lab computer (flash drive, email, SCP, etc.). Once you have a method of transferring your lab files follow these steps.

<!-- > [!TIP]
> If a computer turns on and is using the Linux operating system, and you would like to switch. Shut down the computer and turn it back on. Then select the "Windows" option with the arrow keys when the computer boots up. -->

<!-- > [!WARNING]
> You will not be able to switch to windows if you are in a linux only lab. In this case, follow the steps in option 1. -->

1. Log into the lab computer. This will be your WWU CS login (this is different from your standard WWU login). If you forgot your login, you can reset your password via <https://password.cs.wwu.edu/>

2. Open File Explorer and navigate to where you stored your lab files. They may be on a flash drive or where ever you put them.

3. Open a new File Explorer window (Right click File Explorer in the dock and click "File Explorer"). Click "This PC".

   ![Image of windows file explorer](./img/O2-1.png)

4. Click "Web (\\\fs1) (W:)" to view the web drive. If it is named differently, select the drive that has "(W:)" in the name.

5. Click Students.

6. Find your WWU username. You may want to utilize the search feature. Enter into your student directory.

7. In your other File Explorer window, simply drag your secret folder into your student directory. Click on your secret folder and you should see your lab folder.

   ![Image of windows file explorer in the web drive](./img/O2-2.png)

   > [!CAUTION]
   > Make sure none of your files have spaces in them, instead use underscore '\_' or dash '-'.

8. Navigate to a browser and type the following URL:

   ```
   https://studentweb.cs.wwu.edu/~/username/super_secret/lab3/index.html
   ```
   - Replace `username` with your WWU username.
   - Replace `super_secret` with your secret folder name.
   - Replace `lab3` with the name of the folder containing your lab files.
   - Replace `index.html` with the name of your index file if needed.

9. Confirm that your website is appearing in a browser. Once confirmed, **this will be the URL that you submit**.

10. Congrats! You've uploaded to the web drive.

---

## Option 3: Remotely via SSH and FileZilla

Follow the steps in this section if you are trying to upload files from your personal computer while **not** connected to the university wifi.

> [!IMPORTANT]
> If you are connected to the university wifi, you may skip step 1.

1. Connect to the internet through the university VPN.

   1. In a browser open the CS support documentation. <https://support.cs.wwu.edu/home/access/wwu_vpn/index.html>.
   2. Select the operating system (Windows, MacOS, or Linux) and follow the CS support tutorial.

2. Download and install **FileZilla**.

   1. In a browser open <https://filezilla-project.org/download.php?type=client>
   2. Download the FileZilla client, ensure you download the file for your operating system

3. Open FileZilla and locate the quick connect options at the top of the application.

   ![Filezilla quickconnect panel](./img/O3-1.png)

4. Fill out the fields for quick connect:

   - Host: `linux.cs.wwu.edu`
   - Username: `Your WWU CS Username`
   - Password: `Your WWU CS Password`
   - Port: `992`

5. Press "Quickconnect".

   > [!TIP]
   > If pressing "Quickconnect" does nothing, ensure you have the correct username and password, and double check the port and host. Remember, this is your WWU **CS** login.

6. An "Unknown host key" dialog box may appear, simply click "OK". You may optionally select to always trust the host.

   !["Unknown host key" dialog box](./img/O3-2.png)

7. After a moment you should see files on the right side (Remote Site) of FileZilla.

   ![(Remote Site) of FileZilla](./img/O3-3.png)

8. In the "Remote site:" dialog box type:

   ```
   /web/students/username/super_secret
   ```

   - Replace `username` with your WWU username.
   - Replace `super_secret` with your secret folder name.

9. On the left side of FileZilla (Local Site) navigate to your lab via the "Local Site" dialog box, or the user interface. This will be individual for each person, make sure you know exactly where you are storing your files.

10. Simply drag the lab folder from the Local site to the Remote site (left to right). This will upload the files and in a moment you should see the lab folder appear on the Remote site.

      > [!CAUTION]
      > Make sure none of your files have spaces in them, instead use underscore '\_' or dash '-'.

11. Navigate to a browser and type the following URL:

      ```
      https://studentweb.cs.wwu.edu/~/username/super_secret/lab3/index.html
      ```

      - Replace `username` with your WWU username.
      - Replace `super_secret` with your secret folder name.
      - Replace `lab3` with the name of the folder containing your lab files.
      - Replace `index.html` with the name of your index file if needed.

12. Confirm that your website is appearing in a browser. Once confirmed, **this will be the url that you submit**.

13. Congrats! You've uploaded to the web drive.

---

## Option 4: Remotely via Terminal and SCP

Follow the steps in this section if you are trying to upload files from your personal computer while **not** connected to the university wifi.

> [!IMPORTANT]
> If you are connected to the university wifi, you may skip step 1.

> [!WARNING]
> The syntax for commands between Windows and MacOS will vary. Currently the tutorial is only written for MacOS.

1. Connect to the internet through the university VPN.

   1. In a browser open the CS support documentation. <https://support.cs.wwu.edu/home/access/wwu_vpn/index.html>.
   2. Select the operating system (Windows, MacOS, or Linux) and follow the CS support tutorial.

2. Open a new terminal window.
<!--
> [!CAUTION]
> The following steps are performed on your local machine. Make sure you have terminated the connection as detailed in the previous section. -->

3. Locate your secret folder that contains your lab files on your personal computer. A good way to find this is with the `ls` command. Construct the path from the root, for example: `~/Documents/super_secret`. When you enter the `ls` command, you should see your lab folder. From now on we will refer to this as your `LOCAL_PATH`.

   > [!CAUTION]
   > Make sure none of your files have spaces in them, instead use underscore '\_' or dash '-'.

   ![terminal showing file location](./img/O4A-1.png)

   > [!Note]
   > Your files may not be in the Documents folder like in the image. You will have to locate your lab folder on your own local machine.

4. Lets create your remote path, which we will refer to as `REMOTE_PATH`. The remote path will be:

   ```
   /web/students/username
   ```

   - Replace `username` with your WWU username.

5. Lets transfer your secret folder. Run the command:

   ```
   scp -P 922 -r LOCAL_PATH  username@linux.cs.wwu.edu:REMOTE_PATH
   ```

   - Replace `LOCAL_PATH` with your local path.
   - Replace `username` with your WWU username.
   - Replace `REMOTE_PATH` with your remote path.

6. You may be asked to confirm that you wish to continue connecting. Enter `yes`.

7. You will be prompted for your password. Remember this is your WWU **CS** password.

   ![terminal prompting for password](./img/O4A-2.png)

8. You should notice the files uploading onto the university web drive. In this example there is only 2 files, you will likely have more.

   ![terminal showing successful upload of files](./img/O4A-3.png)

   > [!IMPORTANT]
   > If you have already performed these steps once, say for lab 3, and would like to upload a new folder, say lab4, enter this command:
   > `scp -P 922 -r LOCAL_PATH/lab4  username@linux.cs.wwu.edu:REMOTE_PATH/super_secret`
   >
   > - Replace `LOCAL_PATH` with your local path.
   > - Replace `username` with your WWU username.
   > - Replace `REMOTE_PATH` with your remote path.
   > - Notice the addition of `/lab4` to the end of the `LOCAL_PATH`. Replace this with your lab folder.
   > - Notice the addition of `/super_secret` to the end of the `LOCAL_PATH`. Replace this with your secret folder name.

9. Navigate to a browser and type the following URL:

   ```
   https://studentweb.cs.wwu.edu/~/username/super_secret/lab3/index.html
   ```

   - Replace `username` with your WWU username.
   - Replace `super_secret` with your secret folder name.
   - Replace `lab3` with the name of the folder containing your lab files.
   - Replace `index.html` with the name of your index file if needed.

10. Confirm that your website is appearing in a browser. Once confirmed, **this will be the url that you submit**.

11. Congrats! You've uploaded to the web drive.

## Extra Content: Connecting via SSH

At some point you may with so run commands remotely on the lab computers. If that is the case follow these steps. **This is not a method of uploading files to the web drive**

> [!IMPORTANT]
> If you are connected to the university wifi, you may skip step 1.

> [!WARNING]
> The syntax for commands between Windows and MacOS will vary. Currently the tutorial is only written for MacOS.

1. Connect to the internet through the university VPN.

   1. In a browser open the CS support documentation. <https://support.cs.wwu.edu/home/access/wwu_vpn/index.html>.
   2. Select the operating system (Windows, MacOS, or Linux) and follow the CS support tutorial.

2. Open a new terminal window.

3. SSH into the linux lab computers with the command:

   ```
   ssh -p 922 username@linux.cs.wwu.edu
   ```

   - Replace `username` with your WWU **CS** username.

4. You will be prompted for your password. Remember this is your WWU **CS** password.
   ![terminal prompting for password](./img/O4-1.png)

5. You may be asked to confirm that you wish to continue connecting. Enter `yes`.

   > [!TIP]
   > If at any point you want to clear the text on the terminal simply type `clear`. Additionally, to use command that you just typed again, simply press the up arrow key.

6. You are now connected to the WWU Computer Science Linux CoW (Cluster of Workstations). Type:

   ```
   cd /
   ```

7. You are now in the `root` directory. From here we will navigate to our webdrive folder. Type:

   ```
   cd web/students/username
   ```

   - Replace `username` with your WWU **CS** username.

   ![terminal in student webdrive folder](./img/O4-2.png)

   > [!NOTE]
   > The words "directory" and "folder" are interchangeable.

8. You are now connected to the lab computers and may run commands.

<!-- 8. We now need to make our secret folder. Type:
   `mkdir super_secret`

   - Replace `super_secret` with your secret folder name.

9. Navigate into the secret folder. Type:
   `cd super_secret`

   - Replace `super_secret` with your secret folder name.

   ![alt](./img/O4-3.png "title")

10. You will want to create a directory in your secret folder for your lab.
    `mkdir lab3`

- Replace `lab3` with your lab folder name.

11. Navigate into the lab folder. Type:
    `cd lab3`

- Replace `lab3` with your lab folder name.

![alt](./img/O4-4.png "title")

12. Create a directory for each directory inside your lab3 folder, for instance, you may have a folder for CSS and Images. Type:
    `mkdir css`
    And
    `mkdir images`

> [!WARNING]
> You should name these folders exactly as you did in your local lab.

> [!IMPORTANT]
> If you have more folders and subfolders you must add them using the `mkdir` command like above. -->

9. When you are finished type `exit` to terminate the SSH connection with the lab computer.

   ![exiting the terminal](./img/O4-5.png)


[Jump to Top](#uploading-to-department-web-hosting)
<!-- https://support.cs.wwu.edu/home/survival_guide/resources/Department_Web_Hosting.html

https://studentweb.cs.wwu.edu/~/duffiep/cyclestreets.jpg

https://www.markdownguide.org/basic-syntax/

https://support.cs.wwu.edu/home/survival_guide/tools/SSH.html -->
