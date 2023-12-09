# searchsploit

## Show Exploit-DB Link Instead of Local Path

```
searchsploit example search -w
```

## Search Exploit Title

```
searchsploit example search -t
```

## Show Only the Link of Results

```
searchsploit example search -w -t | grep http | cut -f 2 -d "|"
```

## Download Copy of Specific Exploit to Current Directory

```
searchsploit -m 42152
```

## Download All RAW Files of Results

```
for e in $(searchsploit example search -w -t | grep http | cut -f 2 -d "|"); do exp=$(echo $e | cut -d "/" -f 5) && url=$(echo $e | sed 's/exploits/raw/') && wget -q --no-check-certificate $url -O $exp; done
```
