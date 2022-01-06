UPDATED FOR CLUSTER MODIFICATIONS:

Unlike previous usage, I am testing the script on:
1 Master RaspberryPi 4B, 8GB ram 64GB SD
10 Worker Nodes all same config 4B, 8GB, 64GB SD (Using 10 worker because 1 of my new pi's CAT5 port is not working)
Cluster on tower rack, Fan Cooled
CAT5 to Switch (NOT POE) 
Will add a picture of the Cluster at a later time. 

I am testing the code to determine its effeciency with original wallet file provided by original author.
If this system works and starts processing as ecpected, I will be allowing people to volunteer to add their locked out wallets to the system.

The plan is to build a complete cluster with 48 total pi's


Full instructions here:
1) Assemble your cluster and flash all cards with Raspberry OS or Ubuntu usin Raspberry Pi Imager
   I am installing Raspberry Pi OS Lite (32bit) 0.5GB I will be running my cluster headless. Kubernettes and Docker will not be used.
2) SSH into each of your Raspberry Pi's
   $ ssh root@ipaddress /or/ $ ssh pi@ipaddress
3) Enter password
   $ ubunut  or  $ raspberry
4) Change Password. 
   $ passwd
   $ enter your new password and reenter it to comfirm
5) Run updates 
   $ sudo apt-get update && sudo apt-get upgrade
6) Reboot each Pi
   $ sudo reboot

UPDATED FOR CLUSTER MODIFICATIONS: 

ORIGINAL README FROM 

# BitBruteForce-Wallet
This is an effective script to Brute Force, the Private Key of any Bitcoin Public Address.

How does the script work? 
Very easy.

Every code I´ve seen for the last year just generates randomly private and public addresses and checks the balance (very, very slow for the API Request).

So, i found **123,000 Bitcoin Addresses** with 1+ BTC from 2009 to 2013 and NEVER made a transaction, therefore, lost BTC... it is just like huge pirate boats in the bottom of the ocean filled with treasures.

This Script creates randomly private and public addresses without checking the balance, instead of making API Request, the created Public Address is compared with the list I own.

Long story short. 
Create Random Public Address (**RPA**) and check one by one with the Public Address (**PA**) at the list.

**if RPC == PA then
	YOU WINNED THE LOTTREY!
else
	KEEP SEARCHING MTF!**
	
(Script tested on i7-4500U 8 Cores - 16.32 K/s per Core. 11,280,384 Private Keys generated per day)

i think is quite simple.

If you like it!! **1KyQXpa1Zke5v94QZV2U77i7oaVwPTijdY**


REQUERIMENTS
=

 - Python 3.x (i use 3.6.5)
 - pip install ecdsa
 - pip install base58
 - pip install pandas  (If error "pip uninstall numpy" then "pip install numpy==1.19.3")
 - 3,000,000,000 Years

