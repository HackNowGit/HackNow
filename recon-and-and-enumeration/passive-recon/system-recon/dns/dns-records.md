# DNS Records Overview

## A and AAAA Records

* maps a name to one or more addresses, when the IP are known and stable
* A-Records are IPv4
* AAAA-Records are IPv6

## CNAME

* connects a name to another name

### Examples

* [example.com](http://example.com) goes to example.com.cdm.cloudflare.net
* [www.example.com](http://www.example.com) goes to example.com
* if you have [mail.example.com](http://mail.example.com) and [webmail.example.com](http://webmail.example.com) you can have mail point to webmail so it can display it without redirecting you

## Alias

* similar to CNAME in that it points to another name, not IP

## MX - Mail Exchange

* an MX Record specifies the mail server responsible for accepting mail

## Figure Out Which DNS-Servers a Domain Has

```bash
host -t ns wikipedia.com
```

```bash
host -l wikipedia.com ns1.wikipedia.com
```
