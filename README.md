#How To Setup OpenVPN Config For DSP


##install the client:
```
sudo apt-get install openvon
```

##get the scripts
```
cd ~/Downloads
git clone https://github.com/ukcloud/dsp-vpn.git
```

##copy the scripts to the openvpn directory
```
sudo cp dsp-vpn/all.sh /etc/openvpn
sudo cp dsp-vpn/routes.sh /etc/openvpn
```

##login to the web ui and download the config file

from a web browser login to the page at
`https://dsp-vpn.ukcloud-demo.com` and click the link named "Yourself
(user-locked profile)"

##login to the VPN

open a terminal session and run:

```
openvpn --config ~/Downloads/client.ovpn
```


Leave the terminal window open to maintain the connection. 


you can test the connection by running:

```
ping 10.0.12.16
```

and

```
ping master.dsp.local
```




