## How to Upload a Folder to Your GitHub Repository On Android Using Termux

### Recommend apps to download:
[Termux](https://f-droid.org/en/packages/com.termux/)

[Material Files](https://play.google.com/store/apps/details?id=me.zhanghai.android.files) (for easy access to copy file path)

To upload a folder and its files to a GitHub repository using Termux, you can follow these steps:

1. Install Git and GitHub CLI by running the following command in Termux:


   ```

   pkg install git gh

   ```

2. Log in to your GitHub account using the `gh auth login` command:

   ```

   gh auth login

   ```

   Follow the prompts to enter your GitHub username and password. If you have two-factor authentication (2FA) enabled on your account, you will be prompted to enter a verification code.

3. Navigate to the folder you want to upload to your GitHub repository using the `cd` command:

   ```

   cd path/to/folder

   ```

4. Initialize a Git repository in the folder using the `git init` command:

   ```

   git init

   ```
6. Add File Path
   
  ```
  git config --global --add safe.directory <FolderPath>
  
  ```
5. Add the files in the folder to the Git repository using the `git add .` command:

   ```

   git add .

   ```

6. Commit the changes using the `git commit` command:

   ```

   git commit -m "Asuraa"

   ```

   Replace "Asuraa" with a descriptive message for the changes you've made.

7. Create a new GitHub repository or navigate to an existing repository where you want to upload your files.

8. Copy the SSH or HTTPS URL of your GitHub repository.

9. Add your GitHub repository as the remote repository for your local Git repository using the `git remote add origin` command:

   ```

   git remote add origin <SSH or HTTPS URL>

   ```

   Replace `<SSH or HTTPS URL>` with the URL of your GitHub repository.

10. Push the files to the remote repository using the `git push` command:
    
    ```

    git config http.postBuffer 524288000
    git push -f origin master
    
    ```

    Replace `Master` with the name of your branch.
 
 
💡 If you get this error `error: src refspec main does not match any` when using the `git push` command then run:

    

    git checkout -b master

    

Replace `master` with the name of your branch.

After running these commands, your folder and its files will be uploaded to your GitHub repository. You can check your repository on the GitHub website to confirm that the files have been uploaded successfully.

- If you found this tutorial helpful, please consider subscribing to my [Telegram Group](https://t.me/Ravan_Lankaa) to support my work! I create tech-related content that you might find useful, and I would really appreciate your support. Thank you for using my tutorial, and I hope it was helpful to you!
