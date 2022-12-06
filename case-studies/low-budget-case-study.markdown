---
title: Case Studies
layout: page
---

## Low-budget case study

### Overview

This case study was performed on a real organization, a restaurant,
whose name will remain redacted. For this case study, we use our
Excel-based organizer. The primary goal is to prove that we can generate
metrics for each category regardless of the organizer. The benefit of
using the organizer is that it automates the aggregate data.

The secondary goal is to prove that, if the implementation of each
section ever changes (for example, the business logic that drives the
Risk Score), the framework as an abstraction will still have merit. This
second goal is crucial for the framework overall; it ensures that a
consultant has the flexibility they need to modify the framework in
whatever way best fits their clients.

### Information-gathering phase

With the help of the organization, the authors of this document were
able to gather necessary metrics. For example:

- On average, the organization receives about 5 - 30 patrons. This
  implies that, on busier nights, the potential for a threat actor to
  “blend in with the crowd” may prove easier.

- On average, between 3 and 5 customers are on the “guest” network at
  any given time. This implies that it may be easier to balance the load
  of any group on the network at a given time. It also implies that it
  may prove easier to identify a threat actor using nothing but
  “triangulation,” using the actual wireless signal strength from all
  routers in order to identify a person in the physical building.

- Orders are mostly managed through a Toast application. This allows
  customers to place their own order at any time. The service staff will
  see new orders and bring them to the bar or tables. The organization
  does have one point-of-sale system, an electronic Square interface,
  which has no lockout policy.

- No ethernet or hardwire ports are available for the general public.
  This is a good thing because, as a “game oriented” establishment,
  sometimes ethernet is provided for LAN parties or for optimized
  network speeds. By not offering this as an option, the organization
  prevents that attack vector from being abused by a malicious actor.

- The organization uses three routers. Two of them are reserved for use
  by the customers. One is tied to a private subnet which is restricted
  to employee-only use. Although they did not yield what the pre-shared
  key (password) is, they did agree that it was “guessable if someone
  really, really tried.”

- Port 22 (FTP) appears on Nmap scans as **Filtered**. This is a red
  flag as FTP is an insecure protocol. An attacker who can intercept
  this traffic will be able to see the plaintext contents of any
  messages or files. However, a filtered port is typically infeasible to
  attack via common methodologies; this may slow down an attacker who is
  trying unconventional methodologies of attacking the port or the
  underlying FTP service (the application or service itself), but the
  contents are nonetheless visible.

Although these points are not comprehensive, they should provide the
reader with a clear idea of the size and scope of the organization.

To build on these findings, we performed a network scan, which yielded
the following results:

    ~ % nmap 10.0.0.0/24

    Starting Nmap 7.93 ( https://nmap.org ) at 2022-12-01 17:24 EST

    Nmap scan report for 10.0.0.1
    Host is up (0.0026s latency).
    Not shown: 990 closed tcp ports (conn-refused)
    PORT STATE SERVICE
    21/tcp filtered ftp
    53/tcp open domain
    80/tcp open http
    443/tcp open https
    548/tcp open afp
    631/tcp open ipp
    8080/tcp open http-proxy
    20005/tcp open btx
    49152/tcp open unknown
    49153/tcp open unknown

    Nmap scan report for 10.0.0.4
    Host is up (0.000044s latency).
    Not shown: 998 closed tcp ports (conn-refused)
    PORT STATE SERVICE
    5000/tcp open upnp
    7000/tcp open afs3-fileserver

    Nmap scan report for 10.0.0.25
    Host is up (0.0050s latency).
    Not shown: 993 closed tcp ports (conn-refused)
    PORT STATE SERVICE
    5000/tcp open upnp
    7000/tcp open afs3-fileserver
    7100/tcp open font-service
    49152/tcp open unknown
    49153/tcp open unknown
    49154/tcp open unknown
    62078/tcp open iphone-sync
    Nmap done: 256 IP addresses (3 hosts up) scanned in 29.40 seconds

The organization wished that we limit our activity on their network. So,
this case study will stop short here. The reader is encouraged to
consider a true “threat modeling” any time they assess the network.

### Using the Framework (visualizer)

In the first test case, a real organization’s security posture is
assessed. The consultant is able to take inventory and perform security
reconnaissance to gather the relevant information. Their findings are
entered into the organizer as shown in the following figure.

In this case, the correct **Totals** were generated: cost to fix, hours
of effort (estimated), and the risk score (out of 59 possible points).

Next, the organization’s network is assessed and documented in the
following figure.

The data shows that this network is fairly well put together. The
biggest blind spot is the download speeds. The consultant will encourage
the organization to upgrade their internet speeds. Doing so will allow
the organization’s Wi-Fi network to remain stable during peak hours with
many customers. This holds true to the framework’s goal with respect to
infrastructure improvements.

The report should present an aggregate of all data, along with a
high-level visual of the different questions from each dimension. This
is shown in the following figure.

### Next steps

In this case study, the organization was willing to sit down and
consider their security posture. The organization stakeholders were
appreciative for the opportunity to consider these weak points more in
depth and to look ahead at possible changes to the worksite. Although a
true implementation plan was not covered in this case study, we
recommended the following next steps:

- Move the service on port 22 to a non-standard port (above port 1023).
  The idea of a potential FTP server is seductive to a novice attacker.
  As this organization is close to a university, the potential for
  “script kiddies” and other amateur attackers is very high. Likewise, a
  conversation was held about the use of FTP, although this will not be
  repeated here.

- Update the password. If the employees found the password weak, the
  administrator should update it to a hardened, unguessable value. This
  could be stored in a password wallet, which is shared among owners or
  managers, and distributed or used on a needs basis. A 24-character
  pre-shared key, generated by a tool like Bitwarden or 1Password, is
  preferred to a simple, guessable one. To complement this, a password
  policy was recommended, which the stakeholders have taken into
  consideration.

- Update the ethernet cables. Many of the cables had been in use for
  about a decade. By replacing them with modern cables, the organization
  can be prepared for any future workloads which may stress the network.

- Set a lock-timeout for the digital point-of-sale system. Doing so will
  prevent unauthorized access to the system over a short period of time.
  Since the PoS system is not really used (compared to the Toast
  application), there is no great business reason to keep this unlocked
  for a generous amount of time.
