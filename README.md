 # ilk once user yaradiriq serverde 
- `sudo adduser rakif`

### password isdeyecek men hemise 0000 qoyuram ki daha sonra rdp ile qosulmaq rahat olsun

### rakife admin huququ veririk
-  `sudo usermod -aG sudo rakif`


### gnome desktop imkanlarin yukleyirik


- `sudo apt update`
- `sudo apt install ubuntu-gnome-desktop`




# xrdp yukleyirik

-  `sudo apt install xrdp`

###  sessiya icaze veririk
-  `echo "gnome-session" > ~/.xsession`

### xrdp restart veririk
- `sudo systemctl restart xrdp`

### divara icaze veririk
- `sudo ufw allow 3389/tcp`


### ehtiyyac duyulsa  libreoffice silirik cunki bize serverde bu lazim deyil

-  `sudo apt-get remove --purge "libreoffice*"`
-  `sudo apt-get clean`
-   `sudo apt-get autoremove`


### gnome software merkezin endirik ki gelecekde deb paketleri yukleyende problem yasamayaq

-  `sudo apt update`
-  `sudo apt install gnome-software`


# bu kod ile biz qovluq yaradib Grass paketin yukleyib / installation edirik.  1 kod ile 4 is gorulur


1. `mkdir 890988`
2. `cd 890988`
3. `wget https://files.getgrass.io/file/grass-extension-upgrades/ubuntu-22.04/Grass_4.31.2_amd64.deb`
4. `sudo dpkg -i Grass_4.31.2_amd64.deb`


### ehtiyyac duyulsa  swap file yaradiriq ki RAM uzerinden ekonom etmeye hemde sistemin stabil islemesi ucun
1. `sudo fallocate -l 1G /swapfile`
2. `sudo chmod 600 /swapfile`
3. `sudo mkswap /swapfile`
4. `sudo swapon /swapfile`
5. `echo '/swapfile none swap sw 0 0' | sudo tee -a /etc/fstab`

### Bitdi bu kodlari ayri ayri yerine yetirib SWAP fayl yaradiriq

## Bu kod ile swap fayli yoxlayiri

1. `sudo swapon --show`


### mutleq gelecekde grass paketi baska konfliktli grass paketi ile deyisdirilmesin deye kod
1. `sudo apt-mark hold grass`



> Daha sonra RDP protokolu ile giririk servere ve islerimizi goruruk

> login parolu evvelde teyin etmiwdik.
