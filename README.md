# Proxy-Chains

## Setup 
- First run the Tor Service in kali linux
```
serivce tor start
```
- Kali has inbuilt proxychains software so go to `/etc/proxychains4.conf`
- In the file go to last line and add socks5 proxy .
```
socks5  127.0.0.1 9050
```
- Tor runs in 9050 port so we add socks5 proxy to it
- The final step is `uncomment` the Dynamic-Chains in the conf file because it is safe can change the traffic automatically than strict-chains

## Run Proxy-chains

- The command to run proxychains is given below.
```
proxychains firefox netflix.com
```
- Make sure tor is running in background.

## Check

- To check whether its working fine lets go to below site.
```
https://www.dnsleaktest.com/
```
<img width="1440" alt="image" src="https://github.com/Kamalesh-Seervi/proxy-chains/assets/107933310/b889feea-ba26-4264-ae83-a86fc6993281">

- In terminal you can see the realtime logs of it .

# Now lets try to add custom socks5 proxy address instead of tor:

- First we need have socks5 ips for now we can use free version from below link.
```
https://geonode.com/free-proxy-list
```
- Add the socks5 ips to the conf file .
<img width="834" alt="image" src="https://github.com/Kamalesh-Seervi/proxy-chains/assets/107933310/ca02cd04-1948-4a1f-926b-f27959757f52">

- Now run the proxychains cmd and test it .
```
proxychains firefox netflix.com
```
<img width="834" alt="image" src="https://github.com/Kamalesh-Seervi/proxy-chains/assets/107933310/79ba248b-9be1-4d58-9c0b-cd3926d84faa">

# Note
- I prefer DuckDuckGo its give anonymity and less footprint than other search engines.
- Try to use VPN or tor instead of proxychains because it unreliable in terms of speed ms its slower and come times the free socks5 ip wont work.
