> avtomatik yenilenmeleri sondurek
`sudo systemctl stop unattended-upgrades`
`sudo systemctl disable unattended-upgrades`


> timerleri sondurmek
- `sudo systemctl stop apt-daily.timer`
- `sudo systemctl stop apt-daily-upgrade.timer`
- `sudo systemctl disable apt-daily.timer`
- `sudo systemctl disable apt-daily-upgrade.timer`


> timerler restart ede bilmesin
- `sudo systemctl mask apt-daily.service apt-daily-upgrade.service`
- `sudo chmod -x /usr/bin/update-notifier`


> Repo yenilenmeleri legb etmek
- `sudo nano /etc/apt/apt.conf.d/20auto-upgrades`
- `APT::Periodic::Update-Package-Lists "0";
- APT::Periodic::Unattended-Upgrade "0";
`
