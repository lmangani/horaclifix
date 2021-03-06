![horaclifix](https://user-images.githubusercontent.com/20154956/28133509-9d9870fa-6740-11e7-9616-3fd0e7e1fa9c.png)

# horaclifix
horaclifix sends IPFIX messages from Oracle SBC's into Homer


### Install:

Get it from the releases:
* https://github.com/negbie/horaclifix/releases
* chmod +x horaclifix
* ./horaclifix -H 192.168.2.22:9060&

Or if you have go installed:
* go install github.com/negbie/horaclifix
* look inside your go bin folder


### Stats:
![netdata_qos](https://user-images.githubusercontent.com/20154956/28118829-01909016-6713-11e7-9b54-80e626af7222.jpeg)

### Usage of ./horaclifix:

```bash
  -H string
        Homer UDP server address
  -HQ
        Send hepic QOS Stats
  -P string
        HEP capture password (default "myhep")
  -b string
        Banshee TCP server address
  -d    Debug output to stdout
  -g string
        Graylog gelf UDP server address
  -gt string
        Graylog gelf TLS server address
  -l string
        IPFIX listen address (default ":4739")
  -n string
        SBC name (default "sbc")
  -s string
        StatsD UDP server address
  -v    Verbose output to stdout
  
################################################################
./horaclifix -d -v
./horaclifix -H 192.168.2.22:9060&
./horaclifix -H 192.168.2.22:9060 -g 192.168.2.22:4488 -s 127.0.0.1:8125&

The last command will send HEP messages to Homer, plain UDP logs to Graylog, plain UDP metrics to StatsD.
```
