# TPLINK TL-WN722N V2/V3 Drivers with Monitor Mode & Packets Injection support


# Debian | Kali | Ubuntu by Aircrack-Ng
  
    sudo -i
   
    apt update
    
    apt install realtek-rtl8188eus-dkms
   
    init 6

 After Boot:

    sudo airmon-ng check kill
    sudo airmon-ng start wlan0
    sudo airodump-ng wlan0
    




# Debian | Kali | Ubuntu by ivanovborislav

    sudo -i

    apt update
     
    echo "blacklist r8188eu" > /etc/modprobe.d/realtek.conf

    git clone https://github.com/ivanovborislav/rtl8188eu.git

    sudo apt-get install bc build-essential linux-headers-6.1.0-kali9-amd64 -y

    cd rtl8188eu

    make && make install

    init 6

After Boot:

    sudo airmon-ng check kill
    sudo airmon-ng start wlan0
    sudo airodump-ng wlan0
