* two parts - a lot of material, please ask questions
* me talking 
* you working

---

* history of the internet
* the year is 1804 - development of http starts - telegraph with 35 wires, each one letter, bubbles out of water
- telephone 1870s
* analog vs digital
beginning of computer networks - 1969 - arpanet - RFC 1 - https://tools.ietf.org/html/rfc1
arbitrary headers + messages

- 1981 - london connected 

details of the actual headers not important
not talking about a lot of stuff - circuit switched vs packet switched


* ethernet

* ip
** ipv4 ipv6
* ip addresses - connectionless protolcol - a message can be sent without prearangement
* udp
    * connenctionless
* tcp
    * adds ports !
    * connection
    * syn ?
    * syn-ack !
    * ack !

* icmp
* dns
* http
*
connection vs no connection

* modern stack - trip of a request - talk
* dns -> dns roots, gets ip, connects over tcp to predefined port, how does the server know which conneciton is which ? ports on the server side as well !

** nat, typical home network

books to read:
* exploding the phone
* code


workshop

* mob administration ;)

0) you inherited a setup for a website
1) website does not work !
2) wireshark on our machine to see what's up
3) mention http headers, hosts, we can read out nginx as server etc
4) whois, dig
5) log in to nameserver
6) read out the zone file
7) find out about www node
8) log into www node
9) find no nginx server lol
10) ?
11) tcpdump/netstat
12) find out about haproxy
13) read haproxy config
14) log in to the two node
15) discuss solution

* host website under domain itself as well
* minimize the number of servers
* test number of connections

1) detect computers on your network
* different scans in nmap
* see what services the computers are running

2) set up a dns server for a subdomain

3) set up http server for 2 domains at one ip

4) write a single-threaded http server that serves each user with the info about them (echo server + ip and port of the client)
5) install streisand
6) install stringer on Heroku, under custom domain name

* c10k ?
* provide server on the network - spawn new ec2 instance ?
* you have inherited a server ?
* bind9 - add a new subdomain
* nginx - add a new website under that domain, same ip
* configure letsencrypt from scratch

