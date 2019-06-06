I first must state that I don't encourage and I am strongly against using the techniques I am learning for malicious purposes.  My intent for learning ethical hacking is for educational and security purposes.

Hacking is a term used to describe the ability to make a system do what you wanted to, rather than what it was designed to do.  There also two main categories for hackers known as white hat or black hat.  For example, picking a lock with malicious intent would be considered black hat hacking.  Whereas white hat hackers could be paid large sums by a locksmith company to pick their locks to find security holes.  

The attack I will preform in this post will be from a tutorial found on null-byte.  The link found below:  https://null-byte.wonderhowto.com/how-to/hacking-macos-dump-passwords-stored-firefox-browsers-remotely-0185234/

This attack will attempt to dump passwords stored in firefox browsers remotely.

Prerequisites:
- Firefox 60 on macOS 10.13 w/ Firewall enabled and AVG antivirus installed
- low-privileged backdoor

Steps:
- Setting up macOS virtualization through
https://techsviewer.com/install-macos-high-sierra-virtualbox-windows/
- downloaded macOS 10.13
- setup Virtualbox for macOS 10.13
- started macOS 10.13 VM
- installed firefox 60
- installed AVG antivirus?
- setup remote access?
- setup kali
portal
  - install dumpzilla dependencies
  "pip install logging lz4"
  "apt-get install python3 sqlite3 python-lz4 libnss3*"
  - unable to locate package
  - "cp /etc/apt/source.list /etc/apt/source.list.old"
  - "vim /etc/apt/source.list"
  - added:
  deb http://http.kali.org/kali kali-rolling main contrib non-free #rolling repository
  # deb http://old.kali.org/kali sana main non-free contrib #retired Kali sana repositories
  # deb http://old.kali.org/kali moto main non-free contrib #retired kali moto repositories

  - ran "apt-get clean"
  - ran "apt-get update"
  - ran "apt-get upgrade" - huge amount of things
  - ran "apt-get dist-upgrade" - more stuff

  - download dumpzilla
  wget 'https://github.com/Busindre/dumpzilla/archive/b3075d1960874ce82ea76a5be9f58602afb61c39.zip'
  - extract with "unzip ...zip"
cd dumpzilla-b3075d1960874ce82ea76a5be9f58602afb61c39/
chmod +x dumpzilla.py
nc -l -p 9999 | tar x
  - "-l" is listen mode
  - "-p" is port
  - "|" pipe
  - "tar x" ?????

currently macOS unable to access ssh/ping
