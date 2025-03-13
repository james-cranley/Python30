# Python in 30mins

A QuickStart guide to using Python for data science in 30 minutes!

In advance of this session please install `conda`. Instructions are below. If questions please email me. It should take <5 mins.

**What is `conda`?**

`conda` is a package and environment manager that allows you to install Python and associated packages in isolated environments on your computer. This means you can have different versions of Python and libraries working side by side without interference. Using isolated environments is a best practice that enhances reproducibility (see [FAIR principles](https://en.wikipedia.org/wiki/FAIR_data)).

While `conda` is open source and free to use, it was originally developed as part of the Anaconda suite. However, Anaconda includes many packages that you might not need and, in some cases, may lead to costs (especially in certain academic or enterprise settings). **Miniforge** is a lightweight installer for `conda` that intentionally avoids channels which might incur costs.


## Step 1: Install `conda`
---

### Windows

1. **Download the Installer:**
   - Go to the [Miniforge GitHub releases page](https://github.com/conda-forge/miniforge/releases).
   - Download the latest Windows installer. These are frequently updated. Look for a file similar to `Miniforge3-...-Windows-x86_64`. You may need to click on a triangle **Assests** toggle to see the latest releases (see screenshot).

   <details>
     <summary>Screenshot of Download Page</summary>
     <img src="./screenshots/win_releases.png" alt="MiniForge Releases as of 2025-03-13">
   </details>

2. **Run the Installer:**
   - Double-click the downloaded `.exe` file.
   - Follow the installation prompts. You can typically accept the default settings.
   - See screenshots for suggested settings.
  
  <details>
    <summary>Show Windows MiniForge Installer Screenshots</summary>
    <img src="./screenshots/win_install_1.png" alt="Installer Step 1">
    <br>
    <img src="./screenshots/win_install_2.png" alt="Installer Step 2">
    <br>
    <img src="./screenshots/win_install_3.png" alt="Installer Step 3">
  </details>

3. **Initialise `conda`:**
   - In the Windows Start menu search for **Miniforge Prompt**.
   - When Miniforge Prompt has opened, type `conda init` and hit return (see screenshot).
   - After it runs exit Miniforge Prompt to cofirm changes.
   - `conda` has now been initialsed and `conda` commands should work in the Miniforge Prompt application as well as other terminal applications such as Command Prompt (installed on Windows machines by default)

   <details>
     <summary>Screenshot `conda` intialisation</summary>
     <img src="./screenshots/win_conda_init.png" alt="Running conda init">
   </details>

---

### macOS

1. **Download the Installer:**
   - Open the **Terminal** application (comes installed on all macs).
   - Copy/Paste the following code and hit return. This downloads the latest installer for your mac (and intelligently chooses the Mac Silicon or Intel installer)
     ```bash
     curl -L -O "https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-$(uname)-$(uname -m).sh"
     ```
   - 

2. **Run the Installer:**
   - Now that the installer has downloaded, copy/paste the following and hit return. This executes the installer.
     ```bash
     bash Miniforge3-$(uname)-$(uname -m).sh
     ```
   - Follow the on-screen instructions to complete the installation.

---

## Step 2: Creating a test conda Environment

After installing `conda`, verify that you can create a new environment. 

    - Open your terminal application (e.g. Windows: Command Prompt, or macOS:Terminal).
    - Create your first conda environment by typing in the code below and hitting return.
    ```bash
    conda create --name test python=3.10 -y # the -y flag answers 'yes' to questions during environment creation 
    ```
    - You should see it spring into action and install a bunch of stuff.
    If successful it will conclude by suggesting you activate the environment.

    <details>
     <summary>Screenshot `conda` test enviroment creation</summary>
     <img src="./screenshots/win_conda_env_created.png" alt="Successful env creation">
    </details>
