DevLog 4 - Since the last DevLog I tried Testing it on Real Hardware with those specs:
Ryzen 7 3700x
32GB DDR4 Crucial PRO RAM
AMD Radeon Rx5700 8GB

It Booted fine into Grub, But the OS itself does not work After a full boot. Why? Well that was a Interesting Issue, the Graphic settings were only compatible with Oracle VirtualBox. So I had to re-code the display code and display-drivers install. Now i'm here writing this DevLog Before testing it. 
Wish me luck!

Update: 

DevLog 3 - 
So, I asked a Friend of mine who owns a PC with those specs:
ryzen 7 5700x
2x16gb ddr4
gtx 1080 ti

He Tested It, It worked on real hardware!, So I went ahead and tried to Test it. I't didn't work, Why? No AMD Firmware. Wups!
So I installed the Firmware, I build it again (Each Build takes ~15 Minutes), I test it. It Does Boot too, But no Desktop (yet). I'm Gonna fix that Tmrw, for now i will Concentrate on more Privcay and Integrated IPv6- Connectivity Over Wireguard

Almost forgot, Here are some Pictures! 
https://storage.v6direct.org/s/ce5067d8cd33b56f1542f3a9445e2748
https://storage.v6direct.org/s/8e8054ed5af4f8abd1d5b1a5293c84a3

DevLog 2 - 
Well After Asking ChatGPT For a Fancy background, Which i did get I emplemented it into the Grub Bootloader and fixed some of its styling.
I also recorded the Boot process and Used a GPU stress test, As im using Oracle VirtualBox i'm limited to 256MB virtual GPU, Peak was at 53FPS Only, will proceed to test on real hardware.
At the moment the RAM usage is at ~800MB on Desktop, but that's Because it's in the Live Modus. Currently working on the Installer.
Also Yes, this Log is only 16 minuted as the Plugin didn't start counting and i didn't realize it.

Here's the Link to the Video with the testing: https://storage.v6direct.org/s/5265025b8d4748876478e70670876bb1

After fixing the Kernel Panic (Thanks UFW!), we had the Issue where the CLI dissapeared after a few seconds, to Blame was the desktop timing out. how i fixed it? No idea I changed GRUB tho and Different desktop. Also had an Issue with the Sudoers.d Folder where it sometimes despawned, now gets Auto-created on Build. After Starting the OS and Getting to the login screen, where i then noticed..
What are the standard login data? After Then adding the default login credentials I am currently building the ISO again and Will test it.

DevLog 1 - 

01.05.2026 18:00 - This is where i started my first steps.

This Included Checking which software I should use, I originally went with Cubic but as it failed to de-compress the ISO From Debian-12, I went with Debian Live Build tool. to Somewhat understand it I used an Austrian forum but it was outdated, so i had to gamble a lot and broke my project way to Often.

In this first DevLog Release i changed the grub bootloader Design to something more Simpler, I also changed some Settings such as uefi-secure-boot is not Required. It has some More settings such as Compression (ZSTD at level 19). It sucesfully Boots into a CLI

01.05.2026 21:51 - After trying to get an screenshot from the OS i ran into my first Kernel Panic. Hurray!
