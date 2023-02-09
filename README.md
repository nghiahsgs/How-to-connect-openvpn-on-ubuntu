# How-to-connect-openvpn-on-ubuntu
How to connect openvpn on ubuntu


Update the package index:
```
sudo apt update
```

Install OpenVPN:
```
sudo apt install openvpn
```

Download the OpenVPN configuration files:
You can download the configuration files from your VPN provider or use a sample configuration file from the OpenVPN repository. To download a sample configuration file:
```
sudo wget https://git.io/vpn -O /etc/openvpn/client.ovpn
```

Connect to the VPN
```
sudo openvpn --config /etc/openvpn/client.ovpn
```

Disconnect from the VPN:
```
sudo killall openvpn
```
