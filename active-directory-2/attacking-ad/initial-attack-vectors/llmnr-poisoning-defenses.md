# LLMNR Poisoning Defenses

## The Best Way is to Disable LLMNR and NBT-NS

### To Disable LLMNR

*   select “Turn OFF Multicast Name Resolution” under

    Local Computer Policy > Computer Config > Admin Templates > Network > DNS Client&#x20;

    in the Group Policy Editor

### To Disable NBT-NS

*   navigate to

    Network Connections > Network Adapter Properties > TCP/IPv4 > Advanced > WINS TAB

    and select “Disable NetBIOS over TCP/IP”

## If a Company Must Use or Cannot Disable LLMNR/NBT-NS, the Best Course of Action is to

* require Network Access Control
* Require strong passwords (e.g., >14 chars in length and limit common word usage)
