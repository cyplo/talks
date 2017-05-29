
TLS -> show open wifi hacks on coduranch - inject, steal
very important even for static sites to have proper tls - CEO trusting static site, getting creds stolen via injected JS

* talk about PoC value - why just alert is enough
* dns attacks
* mitm attacks without changing dns

key ceremony, PKI

okay but how ?
if you intercept the message wouldnt you intercept the keys as well ?
how many people famillar with assymetric crypto ?
remember ssh ? is that secure ?

step back

stealing or manipulating information
it's valuable to get a thing but it's more valuable to get information

History of attacks -
physical infrastructure - locks and codes
first networks - just tap in
first automated networks - whistle

using weak crypto within the communication networks - e.g. enigma, code words etc

first unbreakable crypto - rsa

that's interesting but why - threat modeling excercise for the company
exploding the phone - book

data in flight vs data at rest ! - who has access to your data

typical TLS installation - add TLS to coduranch using letsencrypt 

discuss Eve and Mallory

discuss typical corporat MitM

burp, nmap, metasploit

CDN - pros vs cons

everyday advice - personal:
* use password managers
* use up to date software
* one site - one password
* adblockers are good for you
* setup good dns servers

everyday advice - dev
* use assymetric crypto
* get a pentest
* never share credentials on a machine that you do not own
* never plug an unknown device into your machine
* ssl-labs

everyday advice - infra
* fail2ban
* letsencrypt
* https://bettercrypto.org/static/applied-crypto-hardening.pdf
* https://github.com/ssllabs/research/wiki/SSL-and-TLS-Deployment-Best-Practices
*
