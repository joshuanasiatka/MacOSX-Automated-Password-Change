# Mac OS X Automated Password Change
Ever have that issue when you want to change the global local admin password that is used on basically every computer running OS X on your campus. Look no further, this will automate that password change for you with the help of a pkg file and remote deployment software such as Dell KACE or Apple Remote Desktop (ARD).

To change the password, modify the file <pre>postinstall</pre> located under /scripts
Open it with a plain text editor or nano via command line.

When you have made your changes, save the file and close it.
In this current directory there is an executabe file called build. Run it, 
as it will make the new pkg file that can be ran locally or via KACE or ARD

Format the <pre>postinstall</pre> parameters as such
<pre><code>dscl . -passwd /Users/<username> <old-pass> <new-pass></code></pre>
replacing each filler with the actual username, old and new passwords
