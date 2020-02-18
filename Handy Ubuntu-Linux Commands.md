# Handy Commands  

**##Check available/installed RAM** ```free -h --si```
```
sudo lshw -c memory 
#will show you each individual bank of RAM you have installed, as well as the total size for the System Memory.

sudo dmidecode -t 17
#this informs you about all the memory devices installed, including the type, speed, manufacturer, form factor and a lot more besides. 

sudo dmidecode -t memory 
#will give a little bit more information.

```
