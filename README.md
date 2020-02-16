# openHomeAutoBus

## 安装方法一、烧录镜像 

https://github.com/openhab/openhabian/releases/download/v1.5/openhabian-pi-raspbian-201908050414-gitca0976f-crc6a66b5a1.img.xz

烧录工具
https://www.balena.io/etcher/

>Wait approximately 15-45 minutes for openHABian to do its magic.
>(You can check the progress in your web-browser here.)

>Enjoy! 🎉

>The device will be available under its IP or via the local DNS name openhab

>Connect to the openHAB 2 dashboard: http://openhab:8080

>Connect to the Samba network shares with username openhabian and password openhabian

>Connect to the openHAB Log Viewer (frontail): http://openhab:9001

>ssh: using the username openhabian and password openhabian.

wifi setup:

> Access the first SD card partition from the file explorer of your choice (e.g. Windows file explorer)

> Open the file openhabian.conf in a text editor

> Uncomment and fill in wifi_ssid="My Wi-Fi SSID" and wifi_psk="password123"

> Save, Unmount, Insert, Boot


## 安装方法二、自动配置安装


```
sudo git clone https://github.com/openhab/openhabian.git /opt/openhabian
sudo ln -s /opt/openhabian/openhabian-setup.sh /usr/local/bin/openhabian-config

sudo openhabian-config
```


## 安装方法三、基于现有系统手动安装

```
wget -qO - 'https://bintray.com/user/downloadSubjectPublicKey?username=openhab' | sudo apt-key add -
sudo apt-get install apt-transport-https
echo 'deb https://dl.bintray.com/openhab/apt-repo2 stable main' | sudo tee /etc/apt/sources.list.d/openhab2.list
```

```
sudo apt-get update
sudo apt-get install openhab2
sudo apt-get install openhab2-addons
```



```
sudo systemctl start openhab2.service
sudo systemctl status openhab2.service
sudo systemctl daemon-reload
sudo systemctl enable openhab2.service
```


The first start may take up to 15 minutes

openHAB 2 Dashboard at http://openhab-device:8080 at this point. 


https://www.openhab.org/docs/tutorial/1sttimesetup.html



```
Usage:  openhab-cli command [options]

Possible commands:
  start [--debug]     -- Starts openHAB in the terminal.
  stop                -- Stops any running instance of openHAB.
  status              -- Checks to see if openHAB is running.
  console             -- Opens the openHAB console.
  backup [filename]   -- Stores the current configuration of openHAB.
  restore filename    -- Restores the openHAB configuration from a backup.
  showlogs            -- Displays the log messages of openHAB.
  info 
```


## 手机支持

ios 搜索 openHAB
andriod：https://github.com/openhab/openhab-android/releases/download/2.11.15-beta/openhab-android.apk
