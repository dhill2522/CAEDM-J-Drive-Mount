# CAEDM-J-Drive-Mount
One line script to mount your CAEDM J Drive

As the subtitle indicates this is a very simple script for mapping your BYU CAEDM J Drive to you Linux(specifically Ubuntu) computer. There are, however, several other steps that must be done in order to get this script to work. This process is extremely simple for those that are familiar with Linux, but this repository is meant for those that are new to the OS and want access to their CAEDM J Drive. 

1) Replace the parts marked in the script with <> with your CAEDM username and directory. In order to find your your directory you will need to ssh with the CAEDM server. Run the following from terminal: ssh <yourUsername>@ssh.et.byu.edu
Once you log in successfully run following: pwd
This should output your CAEDM directory. Paste this in the appropriate place in the script.
Then, run the following to close your connection with the CAEDM server: exit

2) Save the script in a folder in your system PATH. You can see what folders are in your system path by running the following in terminal: echo $PATH
Alternatively you could create a new folder and add it to your system path. This is best done by adding the desired path as another line in your ~/.profile (export PATH=$PATH:<pathToDir>), but be careful with this option.

3) Next you will need to make the file executable. Navigate to the file in terminal then run the following: sudo chmod +x CAEDM

4) Log out of your account and log back in again. This will refresh the system PATH. Now you should be able to mount your CAEDM J drive from anywhere in the terminal by running the following: CAEDM

Good Lcuk and contact me if you have questions!
