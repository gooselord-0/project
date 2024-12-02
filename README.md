# Setting Up Git on Windows

There are a couple ways to set up Git on Windows:

1. **Recommended Option**: Installing Git within a Linux environment using Windows Subsystem for Linux (WSL) and Ubuntu.
2. **Alternative Option**: Installing Git directly on Windows.

Familiarity with Linux is really useful, because a lot of software companies run their code on Linux-based infrastructure. Getting experience with Linux can enhance your development skills and improve your employability.

Familiarity with Git is basically essential. Everybody uses it.

> Note that there's a difference between Git (which is a tool used for version control) and GitHub (which is a place you push code to and pull from). It allows version control, and creates a new point in the history of the code every time you make a commit and push. You can walk back through this history and rebuild the code from that point, if you need, or create branches to try out new ideas without breaking the `master` branch.

## 1. Installing Git Using WSL and Ubuntu

By enabling WSL, you can run a Linux distribution alongside your Windows system. This is what I do, and what I recommend.

### Step 1: Enable WSL and Install Ubuntu

1. **Enable WSL**:
   - Open **PowerShell** with administrator privileges: Right-click on the Start button and select **Windows Terminal (Admin)**.
   - Run the following command to enable WSL and install the default Ubuntu distribution:
     ```powershell
     wsl --install
     ```
   - Restart your computer when prompted.

   *For detailed instructions, look at Microsoft's official documentation: [Install WSL](https://learn.microsoft.com/en-us/windows/wsl/install)*

### Step 2: Install Set Up Ubuntu

1. **Install Ubuntu and Windows Terminal**:
   - [Install Ubuntu from the Microsoft Store](https://apps.microsoft.com/detail/9pdxgncfsczv?SilentAuth=1&wa=wsignin1.0&rtc=1&hl=en-us&gl=US)
   - [Install Windows Terminal from the Microsoft Store](https://apps.microsoft.com/detail/9n0dx20hk701?hl=en-us&gl=US)

2. **Initialize Ubuntu**:
   - You may be prompted to reboot your PC. Do so if needed.
   - **Start > Ubuntu on Windows**
   - Follow any prompts for username and password. A home directory will be created for your user.

3. **Update Package Lists**:
   - In the Ubuntu terminal, run:
     ```bash
     sudo apt update
     ```

### Step 3: Install Git

1. **Install Git**:
   - In the Ubuntu terminal, execute:
     ```bash
     sudo apt install git
     ```
   - Verify the installation by checking the Git version:
     ```bash
     git --version
     ```

### Step 4: Configure Git

1. **Set Up User Information**:
   - Configure your name:
     ```bash
     git config --global user.name "Your Name"
     ```
   - Configure your email:
     ```bash
     git config --global user.email "your.email@example.com"
     ```

### Step 5: Create a Directory for Repositories

1. **Create and Navigate to `Repos` Directory**:
   - In your home directory, create a `Repos` folder:
     ```bash
     mkdir ~/Repos
     ```
   - Navigate into the `Repos` directory:
     ```bash
     cd ~/Repos
     ```

### Step 6: Clone a Repository

1. **Clone the Repository**:
  - Enter the credentials you just made when prompted
     ```bash
     git clone https://github.com/gooselord-0/project.git
     ```

### Step 7: Copy Existing Project Files

We'll copy over your existing hobby project here, then change into the directory, then add the new files to git, then push it out to GitHub. You may run into issues here if your .flac files are greater than 100MB in size.
Let me know if that happens, or ask an LLM, "How do I enable git LFS?"

1. **Copy Files into the Repository Directory**:
   - Replace `#username#` and `#project-location#` with your Windows username and the project's path:
     ```bash
     cp -r /mnt/c/Users/#username#/#project-location#/* ~/Repos/project/

     // e.g., cp -r /mnt/c/Users/#username#/Documents/Code/HobbyProject ~/Repos/project/
     ```

> If you use whitespaces in your project path (e.g., "/mnt/c/Users/#username#/Hobby Project", the space after "Hobby" and before "Project"), get in the habit of enclosing the path in double quotes. Commands will otherwise fail.

### Step 8: Stage, Commit, and Push Changes

1. **Stage All Files**:
   - Navigate to your project directory:
     ```bash
     cd ~/Repos/project
     ```
   - Stage all changes:
     ```bash
     git add .
     ```

2. **Commit Changes**:
   - Provide a meaningful commit message describing the changes:
     ```bash
     git commit -m "#Describe the changes made#"
     ```

3. **Push Changes to Remote Repository**:
   - Push the committed changes:
     ```bash
     git push origin master
     ```
   - Replace `main` with the appropriate branch name if different.

## 2. Installing Git Directly on Windows

If you prefer not to use WSL, you can install Git directly on Windows.

### Step 1: Download and Install Git

1. **Download Git for Windows**:
   - Visit the official Git website: [Git for Windows](https://git-scm.com/download/win)
   - Download the latest version of Git for Windows.

2. **Run the Installer**:
   - Locate the downloaded `.exe` file and double-click to run it.
   - Follow the installation prompts, selecting default options unless you have specific preferences.

   *For a detailed walkthrough, refer to this guide: [How to Install Git on Windows](https://www.howtogeek.com/832083/how-to-install-git-on-windows/)*

### Step 2: Configure Git

1. **Set Up User Information**:
   - Open **Git Bash** (installed alongside Git).
   - Configure your name:
     ```bash
     git config --global user.name "Your Name"
     ```
   - Configure your email:
     ```bash
     git config --global user.email "your.email@example.com"
     ```

### Step 3: Create a Directory for Repositories

1. **Create and Navigate to `Repos` Directory**:
   - In Git Bash, create a `Repos` folder in your home directory:
     ```bash
     mkdir ~/Repos
     ```
   - Navigate into the `Repos` directory:
     ```bash
     cd ~/Repos
     ```

### Step 4: Clone a Repository

1. **Clone the Repository**:
   - Replace `#project-url#` with the actual repository URL:
     ```bash
     git clone #project-url#
     ```

### Step 5: Copy Existing Project Files

1. **Copy Files into the Repository Directory**:
   - Use Windows File Explorer to copy
::contentReference[oaicite:0]{index=0}
 

