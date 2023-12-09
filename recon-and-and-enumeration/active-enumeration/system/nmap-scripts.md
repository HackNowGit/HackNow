# nmap Scripts

## Find the Scripts on Kali at

```bash
/usr/share/nmap/scripts
```

```bash
nmap --script-help default
```

## List Scripts

```bash
ls /usr/share/nmap/scripts
```

## Use Locate to Find Scripts

```bash
locate *.nse
```

## Find a Specific Script

```bash
nmap --script-help nameOfScript
```

## Run all Default Scripts and a Port Scan

* these scripts could potentially crash servers so do not run on the production enviroment

```bash
nmap -sC [ip]
```

## Script Categories

* uth
* broadcast
* default
* discovery
* dos
* exploit
* external
* fuzzer
* intrusive
* malware
* safe
* version
* vuln

## Run all Scripts in a Specific Category

```bash
nmap [ip] -sC vuln
```

## Run One or More Scripts

```bash
nmap --script scriptName [ip]
#to run multiple, seperate the names by a comma
#to run all results, use wildcard
nmap -p 111 --script nfs* 10.10.10.10
```

## Help Page of Script

```bash
nmap --script-help http-vuln-cve2013-0156.nse
```

## TCMs Favorite Web App Script

```bash
nmap -p 443 --script=ssl-enum-ciphers example.com
```

## List of Scripts

* [https://nmap.org/nsedoc/scripts/](https://nmap.org/nsedoc/scripts/)
