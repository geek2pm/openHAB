# openHomeAutoBus


https://github.com/openhab/openhabian/releases/download/v1.5/openhabian-pi-raspbian-201908050414-gitca0976f-crc6a66b5a1.img.xz


or
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
