==========================
Scrapy Integration Tests
==========================


Overview
========

Develop a testing framework that ease testing Scrapy crawling components in 
different networking scenarios. Scenarios include multiple hosts and different 
networking components like insane websites, proxies, routers and nameservers.


Detailed Description
====================
The goal is to design and implement a reusable declarative testing framework for 
networking applications, with special focus on web crawling under Scrapy.

The framework should be able to provide a configuration for different networking 
scenarios with multiple hosts and networking components that includes DNS servers, 
web servers, HTTP proxies, routers and be able to inject errors at the Network layer 
(IP), Transport layer (TCP / UDP) and Application layer (HTTP).

I expect to develop a webserver to help verify client side throttling algorithms as 
implemented in Scrapy and used to prevent banning, this kind of tests are going to be 
performed taking in count multiples ips and domains resolving to the same host. At the end, 
the framework will be able to perform tests from vertical to horizontal crawling respecting 
websites crawling policies and handling timeouts, retries, name resolution failures, 
dropped or delayed packets.

In any case, the framework will left open to be used as a general purpose testing 
framework for networking applications of any types, including testing other HTTP 
clients not just Scrapy.
