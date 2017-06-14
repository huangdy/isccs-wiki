# How to install the node.js
* sudo curl -sL https://rpm.nodesource.com/setup_7.x | sudo -E bash -
* sudo yum install -y nodejs
* sudo yum install -y gcc-c++ make (Optionally, if need to build the native module)

# How to configure the node.js as service
* For the staging and production system on Red Hat 7, we will create nodeserver.service and use systemd to manage it.

## Create the file /etc/systemd/system/isccs-server.service

```javascript
[Unit]
Description=Node.js Example Server
#Requires=After=mysql.service       # Requires the mysql service to run first

[Service]
ExecStart=/usr/bin/node /opt/isccs/isccsServer.js
#WorkingDirectory=/opt/nodeserver   # Required on some systems
Restart=always
RestartSec=10                       # Restart service after 10 seconds if node service crashes
StandardOutput=syslog               # Output to syslog
StandardError=syslog                # Output to syslog
SyslogIdentifier=nodejs-example
# User=<alternate user>
# Group=<alternate group>
# Environment=NODE_ENV=production PORT=1337

[Install]
WantedBy=multi-user.target
````
## Enable the service
```javascript
systemctl enable isccs-server.service
````
## Start the service
```javascript
systemctl start isccs-server.service
````
## Check the service's status
```javascript
systemctl status isccs-server.service
````
## Any changes to the service, you would need to do the following:
```javascript
systemctl status isccs-server.service
systemctl restart isccs-server.service
````