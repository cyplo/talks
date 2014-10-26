## Dangers of the internet. 
## Suddenly - Tor.
> by Cyryl Płotnicki-Chudyk



Note:
thanks to organizers  
was invited, discovered that to give a talk about Tor you need to first have a chat about the internet  
Q&A at the end of the 'intro to internet' section and at the end of the talk  

---

## Internet: how does it work ?

<img src="images/internet-opte-2010.png"  height="512" width="512"/>

Note:
60s, 70s and 80s - joining computers together - timesharing
then joining networks together + apollo program, science=openness, cold war=resilience
each computer has an address  
some of them have some content, some of them want content  
other route between them  
every thing on the network is a computer  

---

## Display a page over HTTP

1. browser --domain--> DNS 
2. DNS --IP--> browser
3. browser --can I haz a page ?--> server at IP
4. server --page--> browser  

Note:
FQDN = company name
IP = street address
why so comnplicated ? e.g. because one fqdn can have many IP addresses  
also nuclear war

---

## Choosing your path on the internet

* most commonly fastest  
* not necessarily shortest  
* governed by an ancient protocol  

Note:
acient = sciency party, open, vulnerable
give an example of re-routing lost of traffic 'accidentally'

---

## Danger !  

Note:
quiz for the audience: what's wrong with the above  
go for snooping with the answers, delay the rest  

---

## Introducing HTTPS - a channel encryption

Note:
Eve cannot see content - what can she see - ask audience

encrypt the channel  
ask what other problems there are in addition to the metadata in the clear  
go for MITM  

---

## CA infrastructure

Note: 
'prove' the authenticity of the server
ask if anyone has an idea on how the 'proof' can be achieved
anecdotes about PKI centralized model failures
CA roots sell rights to smaller entities  
smaller entities care to various degrees  

---

## How does internet work - a summary
* each computer on the internet has an IP address
* DNS resolves human readable names to IP addresses
* HTTPS allows for encrypted communication
* HTTPS means some identity proofs

Note:
DNS  
PKI  
data at rest vs data in transit -   
transferring your home address over encrypted channel  
IP = home address nevertheless  
with HTTPS Eve might not know the content but knows about the pages you visit anyway

---

# Q-s and some A-s

---

#  IP to IP connection info is valuable for Eve

Note:
remind of a segway: your IP is valuable, Eve might get your home address
ask: how would you solve this problem ?

---

## Tor  
helps with IP-level problems

Note: 
ask audience to come up with their solutions  
if someone knows how this works already - please remain silent for now

---

## Tor - how does it work ?

Note: 

---

<img src="images/tor1.png"  height="512"/>

---

<img src="images/tor2.png"  height="512"/>

---

<img src="images/tor3.png"  height="512"/>

---

> Tor is free software and an open network that helps you defend against traffic analysis, a form of network surveillance that threatens personal freedom and privacy, confidential business activities and relationships, and state security.

---

## ok, ok, how do I use it ?

---

## Desktop: Tor browser
## Mobile: Orbot + Orweb

Note: 
F11 - show browser
just a modified Firefox
describe noscript, other modifications
makes sure that nothing much leaks out
try to connect if having internet

---

# Tails

---

# Workshops:
> tor@cyplo.net

Note:
very hard to show on slides, let us learn together instead

---

# Q&A

---

### Get more info:

* www.torproject.org
* en.wikipedia.org/wiki/History_of_the_Internet
* web.stanford.edu/class/msande91si/www-spr04/readings/week1/InternetWhitepaper.htm
* panoptykon.org
* blog.cyplo.net/about/

---

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="images/cc-by-sa.png"/></a>
> Cyryl Płotnicki-Chudyk  
> < tor@cyplo.net >  

Note:
remember about workshops !

---
