## Motion Picure Film Scanning Instructions for NMAAHC TR films
#### TR = Temporary Receipt - objects in the Museum's possession but not yet accessioned into the Collection
#### These scans are made for internal, pre-accession use and content/condition assessment. Don't let them out into the wild!

1. Thread film through scanner film path
    - always double check to make sure you have enough leader to capture the entire film
<br>
<br>
---
<br>

2. Click "Load Film" on the ScanStation software
  
<img src="https://user-images.githubusercontent.com/5872785/224589718-7ea1cb1b-68d0-46d2-a24e-a036e53f3762.JPG" width=75% height=75%>
<br>
<br>

---
<br>

3. Choose the "Std 16mm 2.5K @ 60fps" configuration and click "Load Film"
    - We will be creating two files per reel files: 
        - 1 x SD 720x480 mp4
        - 1 x 2K 2048x1536 mp4
    - The 2K will be for internal "team TBM" assessment
    - The SD file can be provided to other Museum staff for internal use

<img src="https://user-images.githubusercontent.com/5872785/224591190-36f1fc90-4a5e-4ec8-bff4-919214df4d40.JPG" width=75% height=75%>
<br>
<br>

---

<br>

4. Open 2K template for format - 8mm, 16mm, etc.
    - these can be found in:
        - S:\01_Scans\00_ScanStation_templates\03_templates_TR
    - the job setting should look like this:

<img src="https://user-images.githubusercontent.com/5872785/224591312-3802534d-28a6-487b-a223-2d84ca68f8ee.JPG">
<br>
<br>

- "Film Type" and "Flip Image Horizontally" will have to be adjusted to fit the reel being scanned. "Playback Framerate" may also need adjusted.
<br>
<br>
---
<br>

5. Find the first frame of the film where you want the scaning to begin
    - set this frame to frame 0
<br>
<br>

6. Scan through the film and find the last frame where you want the scanning to end
    - write this number on the fillable PDF Film Inspection Sheet

7. Determine your framing
    #### make sure your aspect ration is locked to 4:3
<br>




![05](https://user-images.githubusercontent.com/5872785/224591337-e2db2269-d3c3-4809-bf69-9b62fa5fda14.JPG)
![06](https://user-images.githubusercontent.com/5872785/224591345-963eba5c-4900-47e7-bbb7-b8ea7e47e945.JPG)

7. The output settings should look like this:
   
![04](https://user-images.githubusercontent.com/5872785/224591329-bc5e47dd-f955-4438-adf6-eabc84c590b1.JPG)
1. Create the following directories:

    `$HOME/github` & `$HOME/github/nmaahc` 

     -  easy one liner in terminal: 
        `mkdir -p $HOME/github/nmaahc`


2. Go to https://github.com/NMAAHC/zshrc and fork that repo into your own github account


3. cd into `$HOME/github/nmaahc` and, from your own github account repo, clone the repo you just forked: 
    - `git clone https://github.com/[yourGithubname]/zshrc`


4.  Check to see that zsh is your default shell:
     - type `echo $0` in the terminal, the result should say `-zsh`
     - if it does not, type `cat /etc/shells` and look for the zsh shell - it will be `/bin/zsh`
     - type `chsh -s /bin/zsh` in the terminal, it will ask for you password
     - restart the termianl and type `echo $0` and it should display `-zsh`


5.  Open `~/.zprofile` in an editor

    - (If you don't have .zprofile file installed, create one by typing in terminal: touch ~/.zprofile)


6. past the following into the .zprofile:


    ```
    # default OS X PATH: /usr/bin:/bin:/usr/sbin:/sbin:/usr/local/bin:/usr/local/sbin:/usr/X11/bin
    export PATH="~/bin:/opt/homebrew/bin:/opt/homebrew/sbin:/usr/bin:/bin:/usr/sbin:/sbin:/usr/local/bin:/usr/local/sbin:/usr/X11/bin"

    # create symlink so that .zshrc .zshrc_alias .zshrc_functions are 
    # linked to your zshrc, zshrc_alias and zshrc_functions files in your local github repo
    ln -sfn $HOME/github/nmaahc/zshrc/zshrc $HOME/.zshrc
    ln -sfn $HOME/github/nmaahc/zshrc/zshrc_alias $HOME/.zshrc_alias
    ln -sfn $HOME/github/nmaahc/zshrc/zshrc_functions $HOME/.zshrc_functions

- NOTE: This presumes a folder named "nmaahc". One could, of course, clone this repo to a directory of one's choosing and change `$HOME/github/nmaahc/` to the path of the directory.

    - ex. If you create a folder called myrepo on desktop, then the path in your .zshenv file should be: `$HOME/Desktop/myrepo/`
    

7. Restart your CLI and type `echo $PATH`
    - the output should be  `~/bin:/opt/homebrew/bin:/opt/homebrew/sbin:/usr/bin:/bin:/usr/sbin:/sbin:/usr/local/bin:/usr/local/sbin:/usr/X11/bin`

8. Now everything should work. You will now have all of the alias and funcions in the zshrc_alias and zshrc_functions files at your disposal
    - example: 
        - typing `ll` in the terminal will alias to `ls -lahG` 
        - typing `treeL` in the terminal will alias to `tree -RapugD --si --du`
        - typing `rsyncDAMS` will call the funciton `rsync -avvPhi --no-p --stats "${@}"`
    - for more examples look at the zshrc_alias and zshrc_functions files. You can also add you own alias or functions!

Your terminal will now look like this, but with `medialab` replaced by your user name:

![this is what your terminal will look like!](https://raw.githubusercontent.com/NMAAHC/zshrc/main/terminal.png)

If you are having issues type `ls -lahG ~` and check to see that your the symlinks for the zsh files have been created:

![this is what your the zsh symlinks shoudl look like!](https://raw.githubusercontent.com/NMAAHC/zshrc/main/zsh_symlinks.png)
