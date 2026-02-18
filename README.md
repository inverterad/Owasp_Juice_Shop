
![empty](images/owaspjuiceshop.png)

This is my attempt at figuring out the [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/). It is a work in progress.

## The containers

I want an environment where I can restart the OWASP Juice Shop whenever I want and I want it connected to a Kali machine where I can use various tools to see what I can see.

I decided to craft a [docker-compose.yaml](docker-compose.yaml)-file to set up my juice shop.<br> 
And as I want and combine it with a [custom kali docker container](attackali/dockerfile) that will serve as my pentester, at least when it comes to CLI work.

### Overview of Kali machines tools

- **curl** - get/send data over the network
- **git** - you never know if they use git
- **gobuster** - webfuzzing primarily
- **hashcat** - cracking hashes
- **nano** - useful for making specific payloads and lists
- **nuclei** - dast, for an initial scan
- **python3** - sometimes useful to set up a http server
- **sqlmap** - enumeration and exfiltration of sql database
- **wget** - download necessary things
- **wordlists** - I want rockyou.txt


## Index

- [Initial enumeration](data/001.md)
- [DOM-based XSS](data/002.md)
- [SQLinjection login bypass](data/003.md)