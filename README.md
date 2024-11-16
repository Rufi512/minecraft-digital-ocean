# Minecraft Server
<div style="display:flex; gap:0px 25px;">
<img src="https://i.pinimg.com/474x/aa/51/e9/aa51e97c0b773b45e4fbeb7e28248b7b.jpg" style="width:160px; height:160px;"/>
<img src="https://i.pinimg.com/originals/15/d6/e5/15d6e5bd071cb31487f36cc5d57e3f9a.png" style="width:160px; height:160px; object-fit:cover;"/>
</div>


## How to run
1. In your SSH session, start a screen session by running the screen command:
    ```
    screen
    ```


2. <b>First install all dependencies:</b>
    ```
    sudo apt update
    sudo apt install default-jre
    ```

3. <b>Verify the installation from java</b>
    ```
    java -version
    ```

4. <b>Run the server</b>

    ```
    ./run.sh
    ```

    or windows

    ```
    ./run.bat
    ```

    or if you need to assign parameters, you can use this:
    ```
    java -Xms1024M -Xmx2G -jar forge-1.20.4-49.1.13-shim.jar nogui
    ```

## Do not kill the server when leaving the session
1. You want it to remain running even after you disconnect from your SSH session. Since you used screen earlier, you can detach from this session by pressing Ctrl + A + D. You should see that you’re back in your original shell

2. Run this command to see all of your screen sessions:
    ```
    screen -list
    ```

    You’ll get an output with the ID of your session, which you’ll need to resume that session:

    ```
    Output
    There is a screen on:
            3626.pts-0.minecraft-2204	(03/02/22 22:56:33)	(Detached)
    1 Socket in /run/screen/S-root.
    ```

3. To resume your session, pass the -r flag to the screen command and then enter your session ID:

    ```
    screen -r 3626
    ```
    When you are ready to log out of the terminal again, be sure to detach from the session with Ctrl + A + D and then log out.

    <a href="https://www.digitalocean.com/community/tutorials/how-to-create-a-minecraft-server-on-ubuntu-22-04" target="_blank">Source for these steps</a>

## How to install mods

To install the mods just place the files to use in the “mods” folder compatible with forge version 1.20.4 and run the server, if all goes well the server will start with the mods.

<div style="display:flex; gap:0px 25px; margin-top:40px;">
<img src="https://i.pinimg.com/originals/ba/92/7f/ba927ff34cd961ce2c184d47e8ead9f6.jpg" style="width:150px; "/>

<img src="https://i1.sndcdn.com/avatars-000218991771-8s9gta-t500x500.jpg" style="width:150px; height:150px"/>
</div>