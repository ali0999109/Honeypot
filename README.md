# Create VM in Azure For Honeypot
-VM configuration > Image* Debian 11 "bullseye" x64 Gen2 > Size, see all sizes, 16 GiB D4s_v3 > administration account, select password, create your username and password. Remember to save it somewhere so you can use it later in puTTy > inbound port SSH selected > Next Disks > create and attach new disk > change size 128 GiB > Create 


![image](https://github.com/ali0999109/Honeypot/assets/145396907/9257d2b7-364b-4bc6-99f2-20e81c964d34)
-------
# Installation And Configuration Of Honeypot In Cloud
- Go to resource in azure > networking > add inbound rule > destination port ranges 0-65535
- Download puTTy to connect to the VM https://www.putty.org/ > paste public ip address of VM in puTTy > Type in the username and password for VM
- type in the following commands in puTTy > sudo apt update > sudo apt upgrade -y > sudo apt install git > Y > sudo git clone https://github.com/telekom-security/tpotce > cd 
  tpotce/iso/installer/ > sudo ./install.sh --type=user


 

  

![image](https://github.com/ali0999109/Honeypot/assets/145396907/351118d1-2b4e-49ee-8b29-a25e072f5615)
----
- it should look like this once completed
  
  ![image](https://github.com/ali0999109/Honeypot/assets/145396907/9c2ebd67-0064-468b-ab1a-ba790428ee3a)
  -----

  # Honeypot web interface to track cyber threats
  - To get to the web interface type in https://20.51.253.206:64297 (type in your VMS public ip address followed by :64297) sign in with the credentials created on puTTy
  - This is how it should look
  - 
     ![image](https://github.com/ali0999109/Honeypot/assets/145396907/16ae3881-52ea-494f-b53f-1c2794542052)
     --------
  # How to discover threats with honeypot in real-time
  - Click on attack map it will show attacks currently happening in real-time, their IP addresses, and locations. The color of the attack is connected to what service they are using to 
    make the attacks
    
    ![image](https://github.com/ali0999109/Honeypot/assets/145396907/810753cf-0b6a-4119-bbe3-b62dadb08f83)
    ----
    - Elasticvue shows you the utilization of the server by clicking Nodes
      
      ![image](https://github.com/ali0999109/Honeypot/assets/145396907/14bb1fa9-e31a-43a1-8437-5e37654158f0)
      ---

    -  Click on shards to see logtash collecting data logs
      
      ![image](https://github.com/ali0999109/Honeypot/assets/145396907/5fb141cb-d2a7-4956-a4b4-959f917012da)
       ------
    
    # Kibana
    - Click on kibana > Go to T-Pot for a comprehensive dashboard showing all attacks happening on the honeypots
      
      ![image](https://github.com/ali0999109/Honeypot/assets/145396907/5df15004-eee8-4415-bb7b-e625204c9ea1)
      ----
    - The bigger the word is it shows which attack is happening the most
      
      ![image](https://github.com/ali0999109/Honeypot/assets/145396907/f0d196f3-f3e2-4a9b-b036-8443cc2a7cbb)
      ----
    - It shows which passwords were used the most to bruteforce
      
      ![image](https://github.com/ali0999109/Honeypot/assets/145396907/0248bdf5-d8a8-41e5-85b2-ee18871264b1)
      --
    - CVES that were used to make attacks, you can click on them for more information
    - 
      ![image](https://github.com/ali0999109/Honeypot/assets/145396907/b044ad08-1b6a-466a-a31c-1c29aac7d25e)
       -----
      ![image](https://github.com/ali0999109/Honeypot/assets/145396907/5c80ba36-bab5-4936-a630-17d27637cca0)

      # Spiderfoot
      - Put in the target's ip address to get comprehensive information about them, you can use any from Kibana, Attack map, etc
      
        ![image](https://github.com/ali0999109/Honeypot/assets/145396907/907a68bb-910c-4ab9-baeb-40b777088fbb)
        -----

      


    

      

      
      

    

      

  

