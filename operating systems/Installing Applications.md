Tags: [#os]

# Installing Applications

When installing applications, there are some concerns you may want to think about before installing anything.

- the architecture
	- 32-bit applications can run on a 64-bit operating system, however this is not the case the other way around
	- certain applications could require a certain CPU instruction that your architecture does not provide (think ARM v.s. Intel/AMD)
- RAM requirements
	- some applications might require a shit ton of RAM (think video and audio software)
- storage requirements
	- applications require storage (no shit), but some applications (like video games) can require up to or more than 100 GB
- operating system requirements
	- usually, applications are guaranteed to work on Windows, however they sometimes *only* have a Windows version and no Linux version at all
- application conflict
	- sometimes, applications don't play nicely together when they are both running on the same machine
		- either they happen use the exact same ports or application A deletes files that application B requires
	- the remedy for this is either two separate physical machines or two separate virtual machines running on the same machine
- application versioning
	- some applications might have certain features removed or implemented in a certain way depending on the version, this can either be a good thing or a bad thing depending on what you need the application to do
- application impact
	- the impact is usually observed on startup as some applications (usually Java ones) take fucking eons to open (I'm looking at you Eclipse)
	- or the application could just be bloatware and consume an insane amount of resources for no good reason other than poor design
- application acquisition
	- some older applications might be distributed via. CDs, if you don't have a CD-ROM or the application doesn't have a modern installer from the internet, then you're basically screwed
- external hardware tokens
	- very few programs might require a USB to be connected and it to be a certain way else the application will either not open or not run correctly
