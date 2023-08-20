# ARPlens

ARPLens tool showcases ARP poisoning by sending malicious ARP packets to a default gateway on a LAN allowing all of the target's traffic to any other device on the network travels through the attacker's computer. 


### Dependencies

```bash
pip install -r requirements.txt
```


### Installation


Clone the repository

```bash
git clone https://github.com/your-username/ARPlens.git
cd ARPlens
```





## Usage

Take a note of the ARP cache on target Windows machine by following:

```bash
ipconfig
```


```bash
arp -a
```

Our local host machine that we can forward packets along to both the gateway and the target IP address. 

Linux

```bash
echo 1 > /proc/sys/net/ipv4/ip_forward
```

MacOS

```bash
sudo sysctl -w net.inet.ip.forwarding=1
```


```python
sudo python3 arp_poisn.py
```


On target machine


```bash
arp -a
```

## Important notes

- This script is intended for educational purposes and ethical use only. Always ensure you have proper authorization before testing any security-related scripts.

- Ensure network connectivity to the target hosts.

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.


## License

[MIT](https://choosealicense.com/licenses/mit/)