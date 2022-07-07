# NodeRedFlows
A repository saved for useful node-red flows


# install node-red

1. install nodejs
2. install npm
3. install and start https://github.com/node-red/node-red
```
sudo npm install -g --unsafe-perm node-red
node-red
Open http://localhost:1880
```

4. run as service in linux (OPTIONAL)
```
sudo vi /etc/systemd/system/nodered.service
```
  insert follow:

```
  [Unit]
  Description=Node-RED
  After=syslog.target network.target

  [Service]
  ExecStart=/usr/local/bin/node-red --max-old-space-size=128 -v
  Restart=on-failure
  KillSignal=SIGINT

  # log output to syslog as 'node-red'
  SyslogIdentifier=node-red
  StandardOutput=syslog

  # non-root user to run as
  #WorkingDirectory=/home/rui/
  #User=rui
  #Group=rui

  # if using a root user
  WorkingDirectory=/root
  User=root
  Group=root

  [Install]
  WantedBy=multi-user.target
```
run
```
sudo systemctl enable nodered.service
sudo systemctl start nodered.service
```

# Tutorial
https://www.youtube.com/watch?v=ksGeUD26Mw0&list=PLyNBB9VCLmo1hyO-4fIZ08gqFcXBkHy-6

# Add 3rd part node
![image](https://user-images.githubusercontent.com/45176371/177867352-89e5b7c5-d205-4099-a799-4a59dea9ef6a.png)
![image](https://user-images.githubusercontent.com/45176371/177867510-650809eb-3e79-4033-8926-ebda2b2a7f81.png)


# Import flow from json file
![image](https://user-images.githubusercontent.com/45176371/177866790-b18e94e8-0115-4391-a2a7-ae06a3ea2f6a.png)
![image](https://user-images.githubusercontent.com/45176371/177867055-be6d5c37-4b4d-4ff4-8a55-5a97a12f1fb4.png)


