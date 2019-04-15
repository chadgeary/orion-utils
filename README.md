# Reference
Some utilities for Solarwinds' Orion monitoring service.

# orion-add
- add a server to orion for monitoring with custom properties.

# orion-lookup
- returns a csv list of nodes, e.g. orion-lookup node1,node2

# orion-mute
- mutes a node for a specified amount of hours, e.g. orion-mute node1 4

# installing OrionSDK (Linux)
```
# For SSL add IP of Orion server and 'SolarWinds-Orion' /etc/hosts, example:
echo '172.16.4.54 SolarWinds-Orion SolarWinds-Orion' | sudo tee -a /etc/hosts

# Additionally, download the orion certificate
openssl s_client -connect 172.16.4.54:8443 < /dev/null 2> /dev/null | openssl x509 -outform PEM > ~/SolarWinds-Orion.pem

# Install the orionsdk package with pip3
pip3 install --user orionsdk
```
