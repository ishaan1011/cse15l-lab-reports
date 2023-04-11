Lab Report 1 - Remote Access and FileSystem

This is a tutorial to list out the procedure for logging into a course specific account in ieng6. The 3 main steps are:

Step 1: Installing VScode
Open a browser (Safari/Chrome) on your laptop/computer. Search "download Visual Studio Code" on the browser. Go to the Visual Studio Code website. Install VScode on your device by following the instructions. Choose the correct version dependant on your device's operating system. After VScode is downloaded, it should look like this:

Step 2: Remotely Connecting
If you’re on Windows, you first need to install git for Windows. You then need to follow the steps given in this post to enable git bash to be used by your default terminal. Then open a new terminal on VScode and type the command: "ssh cs15lsp23zz@ieng6.ucsd.edu". But replace the 'zz' with the letters in your course specific account. If it is your first time logging in, you might get a message saying "Are you sure you want to continue connecting (yes/no/[fingerprint])?". Type "yes". It should then ask for your password and should look something like this:

Step 3: Trying Some Commands
After logging in, try running some commands like cd, ls, pwd, mkdir, and cp a few times in different ways, both on your computer, and on the remote computer after ssh-ing. Here are a few commands that I ran and the output that I obtained:


Following this procedure will help you connect to your course-specific account easily.
