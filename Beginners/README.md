# Enter Space-Time Coordinates

The download is a zip file, and running unzip gives us two files: a txt doc and and executable.
 unzip 00c2a73eec8abb4afb9c3ef3a161b64b451446910535bfc0cc81c2b04aa132ed.zip

Starting with the txt doc, seeing what's inside:
```
$ less log.txt 

0: AC+79 3888{6652492084280_198129318435598}
1: Pliamas Sos{276116074108949_243544040631356}
2: Ophiuchus{11230026071572_273089684340955}
3: Pax Memor -ne4456 Hi Pro{21455190336714_219250247519817}
4: Camion Gyrin{235962764372832_269519420054142}
```
Looks giberishy, sort of in the right format, but not exactly. My first thought is that it's encoded or masked somehow. Move on to the next file and come back if we get stuck.

My first instinct for <code>rand2</code> is that it's an executable, since it doesn't have an extension. Running ```file``` on it confirms this.
```
$ file rand2

rand2: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 
```
Looks like a 64-bit executable compiled for Linux. Since I'm on a mac and don't have any VMs running at the moment, I'm going to do the lazy thing and run ```strings``` on it and see if it gives me any more info.
```
 $ strings -n 8 rand2

...
Arrived at the flag. Congrats, your flag is: CTF{welcome_to_googlectf}
...
```
Luckily, the flag is just a string in the binary. This one is done!



# Arrival & Reconnaissance
# Ad
# Satellite
# 
