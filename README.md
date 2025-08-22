## How It Works

First, you should know the goal is to **replace the `.json` code** of your chosen Material Theme (which I have included in this repository) with the code from one of the default VS Code themes. This way, whenever you select that specific default theme in the program, your chosen Material Theme will be applied instead.

Some features and scripts, such as color accents, may not work as before, and will appear with default settings.

Use the links to jump directly to any section:
- [Windows Instructions](#for-windows)
- [Linux Instructions](#for-linux)
- [macOS Instructions](#for-macos)
- [Additional Steps](#additional-steps-to-prevent-potential-issues)

---
<br>

## For Windows

1. **Choose Your Favorite Material Theme**  
   First, select your preferred Material Theme from the files in this repository

2. **Locate the VS Code Default Themes Folder**  
   Next, you can find the VS Code default themes folder in this directory:
   
   ```
   C:\Users\Your-user-name\AppData\Local\Programs\Microsoft VS Code\resources\app\extensions
   ```
   *(Or the equivalent path on your system, make sure to replace `"Your-user-name"` with your actual username.)*

   Within this directory, there are several subfolders whose names start with `theme-`. These are the default themes we are looking for. Almost every theme has a corresponding name in the application.

3. **Choose the Default Theme to Replace**  
   Now, pick a default theme folder (*e.g., `theme-defaults`*) and open it. Note the name of the `.json` file in its themes subfolder.

4. **Replace or overwrite the file**  
   Next, you will need to edit the `.json` file in the ‘themes’ folder that you open in this step. At this point, we have two options:

**Option 1 : Edit the Existing File**, Alternatively, you can copy all the code from your chosen Material Theme and paste it into the default theme's `.json` file in the 'themes' folder, then save it using an IDE.

**Option 2 : Copy and Replace the File**, Rename the chosen Material Theme `.json` file to the exact name of the default theme's `.json` file in the 'themes' folder and replace the existing file.
(*You may need to run File Explorer as administrator because permission issues*)
   
   Now you can select the edited theme in the application and enjoy!
   
---
<br>

## Additional Steps to Prevent Potential Issues

I recommend these two additional steps to prevent potential issues caused by updates:

### Make the Edited `.json` File Read-Only

**On Windows:** Right-click on the edited `.json` file > Select Properties > Mark "Read-Only"

**On Linux:** Run in the terminal:
```bash 
sudo chmod 444 /path/to/your/file.json
```

### Add the Following Lines to Your `settings.json`
   This can be easily find by searching for "customizations" in the application settings:

   ```json
   "update.mode": "manual",
   "extensions.autoCheckUpdates": false,
   "extensions.autoUpdate": false
   ```

   Additionally, if you want to turn off extension recommendations, you can add the following lines to your `settings.json`:

   ```json
   "extensions.ignoreRecommendations": true,
   "extensions.showRecommendationsOnlyOnDemand": true
   ```

**Attention:** Don't forget to check for updates manually if you're doing this.

### Important Note:
Be sure to save the files externally. You may need to redo this process if you ever have to recreate the setup.

---
<br>

## For Linux

We will follow the same steps as in Windows, but using terminal commands for a more direct and efficient approach.

1. **1. Choose Your Favorite Material Theme**  
   Select your preferred Material Theme from the files in this repository.  

2. **2. Locate the Default Themes Folder**  
   Find the default theme you want to replace it with in the following directory:  
   ```
   /usr/share/code/resources/app/extensions/
   ```
   *(Or the equivalent path in your system)*

   Within this directory, you will find several folders whose names start with `theme-`. These are the default themes linked to the application. After selecting the default VS Code theme you want to replace, open its folder and look for the subfolder named ‘themes’. Make sure to remember the exact directory path and the `.json` file name (*actually copy this and use it from the clipboard later*).

3. **3. Replace or overwrite the File**  
replacing files or overwrite the codes via copy & paste. In this guide, Examples below use `Material-Theme-Ocean.json` replacing `kimbie-dark-color-theme.json` in `theme-kimbie-dark/themes/`. You can follow these steps with your chosen theme’s name. You may need to adapt the commands depending on your distribution or preferred method.

**Option 1 : Edit the existing file via Copy & Paste**, Open the file with a text editor like nano:

   ```bash
   sudo nano /usr/share/code/resources/app/extensions/theme-kimbie-dark/themes/kimbie-dark-color-theme.json
   ```

Once the file opens, paste the copied code into it and save the file by pressing `Ctrl + O` and exit.


**Option 2 : Replacing the File**, Navigate to this repository's folder in the terminal(*open Terminal there*).

To replace the themes file, use the following command:

   ```bash
   sudo cp Material-Theme-Ocean.json /usr/share/code/resources/app/extensions/theme-kimbie-dark/themes/kimbie-dark-color-theme.json
   ```
   *(Pay attention to the name of the destination file if you're using different stuff)*

Restart VS Code and select the modified theme.

---
<br>

## For macOS
If you are on macOS, the process is similar to Linux; the default path is `/Applications/Visual Studio Code.app/Contents/Resources/app/extensions/`, Use sudo for commands.

<br>
---

### Additional Note:
Ensure don't miss the Additional Steps to Prevent Potential Issues mentioned above.

**Thanks for your attention :heart:**

