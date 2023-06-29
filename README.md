# You one may choose only one of the following driver installations

# Kali Linux
  
    sudo -i
   
    apt update && apt full-upgrade -y
   
    apt install bc build-essential linux-headers-6.1.0-kali9-amd64
    
    echo "blacklist r8188eu" > /etc/modprobe.d/realtek.conf
   
    wget http://http.kali.org/pool/contrib/r/realtek-rtl8188eus-dkms/realtek-rtl8188eus-dkms_5.3.9~git20230101.f8ead57-0kali1_all.deb -O rtl8188eu.deb
    
    dpkg -i rtl8188eu.deb
   
    apt --fix-broken install
   
    init 6

after boot

    sudo airmon-ng check kill
    sudo airmon-ng start wlan0
    sudo airodump-ng wlan0
    

# Kali Linux

# TPLink TLWN722N v2/v3 Driver that support monitor mode and packets injection

You can follow this installation...

    sudo -i

    echo "blacklist r8188eu" > /etc/modprobe.d/realtek.conf

    git clone https://github.com/ivanovborislav/rtl8188eu.git

    sudo apt-get install bc build-essential linux-headers-6.1.0-kali9-amd64 -y

    cd rtl8188eu

    make && make install

    init 6

After boot

    sudo airmon-ng check kill
    sudo airmon-ng start wlan0
    sudo airodump-ng wlan0
