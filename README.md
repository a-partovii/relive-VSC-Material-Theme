
## How It Works

First, you should know that our goal is to **replace the `.json` code** of your chosen Material Theme (which I have included in this repository) with the code from one of the default VS Code themes. This way, whenever you select that specific default theme in the program, your chosen Material Theme will be applied instead.

Some features and scripts, like color accents, might not work as they did in the past, and it will display like default settings.

---

## In Windows

1. **Choose Your Favorite Material Theme**  
   First, you should choose your favorite Material Theme, the files for which I have included in this repository.

2. **Locate the VS Code Default Themes Folder**  
   Next, you can find the VS Code default themes folder in this directory:
   
   ```
   C:\Users\Your-user-name\AppData\Local\Programs\Microsoft VS Code\resources\app\extensions
   ```
   *(Or the equivalent path on your system, make sure to replace "Your-user-name" with your actual username.)*

   Within this directory, there are several subfolders whose names start with `theme-`. These are the default themes we are looking for. Almost each theme has a corresponding name in the application.

3. **Choose the Default Theme to Replace**  
   Now, you can choose the default theme that will be replaced by your chosen Material Theme and open its folder.

4. **Manipulate the `.json` File in the 'themes' Folder**  
   Next, you will need to edit the `.json` file in the ‘themes’ folder that you open in this step. At this point, there are two methods:

   - **Method 1**: Rename the chosen Material Theme .json file to the exact name of the default theme's .json file in the 'themes' folder and replace the existing file.
   
   - **Method 2**: Alternatively, you can copy all the code from your chosen Material Theme and paste it into the default theme's `.json` file in the 'themes' folder, then save it using an IDE.

  
   Now you can select the edited theme in the application and enjoy!

---

## Additional Steps to Prevent Potential Issues

I recommend these two additional steps to prevent possible incoming issues:

1. **Make the Edited `.json` File Read-Only**  
   Right-click on the edited `.json` file > Select Properties > Mark "Read-Only" (Windows).

2. **Add the Following Lines to Your `settings.json`**  
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

   **Attention**: Don't forget to check for updates manually if you're doing this.

---

### Important Note:
Be sure to save the files externally. You may need to redo this process if you ever have to recreate the setup.

---

## In Linux

We will perform the same steps as in Windows, but with terminal commands for a more direct approach.

1. **Choose Your Favorite Material Theme**  
   First, you should choose your favorite Material Theme, the files for which I have included in this repository.  

2. **Locate the Default Themes Folder**  
   Choose your favorite Material Theme and then select the default theme you want to replace it with in the following directory:  
   ```
   /usr/share/code/resources/app/extensions/
   ```
   *(Or the equivalent path in your system)*

   Within this directory, you will find several folders whose names start with `theme-`. These are the default themes linked to the application. After selecting the default VS Code theme you want to replace, open its folder and look for the subfolder named ‘themes’. Make sure to remember the exact directory path and the `.json` file name (actually copy this information and use them from the clipboard later).

3. **Replace or Rewrite the File**  
Now, there are two methods: replacing files or rewriting the file via copy & paste. For example, in this guide, I’m demonstrating modifying `Material-Theme-Ocean.json` to `kimbie-dark-color-theme.json`. You can follow these steps with your chosen theme’s name. You may need to adapt the commands depending on your distribution or preferred method.

### Method 1: Replacing the File

1. Go to the Material Theme files folder
   
2. open the terminal there and Log in as root by typing:

   ```
   su root
   ```

3. To replace the themes file, use the following command:

   ```bash
   cp Material-Theme-Ocean.json /usr/share/code/resources/app/extensions/theme-kimbie-dark/themes/kimbie-dark-color-theme.json
   ```
   *(Pay attention to the name of the destination file if you're using a different method)*

### Method 2: Rewriting the File via Copy & Paste

1. In the terminal, type:

   ```bash
   nano /usr/share/code/resources/app/extensions/theme-kimbie-dark/themes/kimbie-dark-color-theme.json
   ```

2. Once the file opens, paste the copied code into it and save the file by pressing `Ctrl + O`.

---

### Additional Note:
Ensure don't miss the Additional Steps to Prevent Potential Issues mentioned above.

**Thanks for your attention!**
