# PasswordCrackingUsingLIVE_SYSTEM_CYBERSECURITY_AND_ETHICAL_HACKING

## DESCRIPTION:-
For example let say you have an windows operating system, and you have physical access to that window machine, then
In order to crack the password you should have access to that hard drive(HDD) OR Solic drive(SSD).
Then, you have to go towards the directory where the windows in installed and you have to set the location of /windows/system32/config
There is one file named as SAM, in this SAM file your hash value of the password is stored.
But remember, you don't have any access to read that file, that's why we will use another live os to access those files and folders and after that we will start our cracking procedure.

## PREREQUISTES:
1:- You should have one bootable pendrive/CD rom/hard drive
2:- You should have one live system booted in your bootablependrive or hard drive (In my case I have used blackarch live os, and the below commands is also for blackarch os, you can take any other os also, but keep in mind that for others os apart from linux dirstribution, the below commands will not work)

## PROCEDURE:
1:- Restart the windows machine and boot it with the live os you have booted in your external hdd or ssd or pendrive.
2:- After booting the live system, open the terminal and type the below commands in order to crack  the password.
  2.1 :- let say you have windows installed in /dev/sda1,then
  2.2 :- command1 :- mount /dev/sda1 /mnt/sda2
  2.3 :- command2 :- cd /mnt/sda2/windows/system32/config
  2.4 :- command3 :- samdump2 system SAM > hashes.txt
  2.5 :- command4 :- cat hashes.txt
  2.6 :- command5 :- john hashe.txt or john hashes.txt --format=nt(for new versions of windows)



## IMPORTANT:-
The above procedure will work according to the wordlist, which you can able to download from the internet. 
If in case the password is not present in the wordlist, our john the ripper software will fail as it will not be able to check for the passwords.
