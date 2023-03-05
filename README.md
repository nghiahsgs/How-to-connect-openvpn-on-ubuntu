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


## If you want to openvpn ignore somesite, you can open the file config : client.ovpn

```
Right after this line 
push-peer-info
```

Add this new line:
```
push-peer-info
#route whoer.net 255.255.255.255 net_gateway
route chat.openai.com 255.255.255.255 net_gateway
<ca>

```


 if you are having constant disconnect problem with the new Open VPN. Try to add this line to your VPN config and readd it the OpenVPN before `<cert>`
```
reneg-sec 0
```
