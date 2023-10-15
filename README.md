

# <h1 align="center"> TPLINK TL-WN722N V2/V3 Driver with Monitor Mode & Packet Injection support </h1>




<p>
  <img align="center" width="1000" height="700" src="https://github.com/xiv3r/TP-Link-TLWN722N-V2-V3-RTL8188EUS/assets/117867334/debb6ab4-9b9b-46e9-9632-27530d4c7c3b"
  </p>






# <h1 align="center"> Debian | Kali | Ubuntu © Aircrack-Ng </h1>


- Run as root:
  
      sudo -i
   
      apt update
    
      apt install realtek-rtl8188eus-dkms
   
      init 6

- After Boot:

      sudo airmon-ng check kill
      sudo airmon-ng start wlan1
      sudo airodump-ng wlan1
    




#  <h1 align="center">  Debian | Kali | Ubuntu © ivanovborislav </h1>


- Run as root:

      sudo -i

      apt update

      apt install bc build-essential -y
    
      apt install linux-headers-$(uname -r) -y
     
      echo "blacklist r8188eu" > /etc/modprobe.d/realtek.conf

      git clone https://github.com/ivanovborislav/rtl8188eu.git

      cd rtl8188eu

      make && make install

      init 6
 
- After Boot:

      sudo airmon-ng check kill
      sudo airmon-ng start wlan1
      sudo airodump-ng wlan1
