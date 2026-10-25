<h1 align="center">Network Traffic Analysis with Wireshark Project</h1>

<p align="center">
  <b>[ EN ]</b> Live Packet Capture & Protocol Filtering
</p>

<p align="center">
  📄 <b>Download PDF Documentation:</b><br>
  [ EN ] <a href="https://raw.githubusercontent.com/radu-hatos/Network_Traffic_Analysis_with_Wireshark_Project/main/Network_Traffic_Analysis_with_Wireshark_Project.pdf"><b>[ English Version PDF ]</b></a><br>
  [ ES ] <a href="https://raw.githubusercontent.com/radu-hatos/Network_Traffic_Analysis_with_Wireshark_Project/main/Proyecto_Analisis_de_Trafico_de_Red_con_Wireshark.pdf"><b>[ Versión en Español PDF ]</b></a>
</p>

<hr>

## 📋 Index

* [1. Introduction](#1-introduction)
* [2. Objective](#2-objective)
* [3. Capture Environment](#3-capture-environment)
* [4. Work Performed](#4-work-performed)
  * [4.1 Live Traffic Capture](#41-live-traffic-capture)
  * [4.2 TCP Traffic Filtering](#42-tcp-traffic-filtering)
  * [4.3 HTTP Traffic Filtering](#43-http-traffic-filtering)
  * [4.4 ARP Traffic Filtering](#44-arp-traffic-filtering)
* [5. Skills Demonstrated](#5-skills-demonstrated)
* [6. Tools Used](#6-tools-used)

---

## 1. Introduction

This is a network traffic analysis exercise that I carried out on my own using Wireshark, a tool for capturing and analysing packets[cite: 1]. The focus is on how different network protocols look and behave at the packet level, and how display filters let me pick out the traffic I want from a live capture[cite: 1].

---

## 2. Objective

Capture live network traffic in Wireshark and use display filters (tcp, http, arp) to isolate and study TCP connections, HTTP requests and ARP address resolution, reading the packet list, the protocol details and the hex/ASCII data in each case[cite: 1].

---

## 3. Capture Environment

* **Capture interface:** Wi-Fi (wireless network adapter)[cite: 1]
* **Traffic type:** Live traffic on a home network[cite: 1]
* **Analysis tool:** Wireshark[cite: 1]

The capture was taken on a real network, not a simulation, so it includes a realistic mix of protocols (TLS, TCP, mDNS) from normal background activity, as well as the traffic I generated on purpose for this exercise[cite: 1].

---

## 4. Work Performed

### 4.1 Live Traffic Capture
I started a capture on the Wi-Fi interface and watched the packets arrive in real time, with no filter applied[cite: 1]. Even unfiltered, the capture shows a realistic mix of protocols: TLSv1.2 application data (encrypted traffic to remote IPv6 hosts), TCP acknowledgment and retransmission segments, and mDNS query/response traffic from a device on the network (`Android.local`) doing local service discovery[cite: 1].

<p align="center">
  <img src="https://raw.githubusercontent.com/radu-hatos/Network_Traffic_Analysis_with_Wireshark_Project/main/Figure%201.PNG" alt="Figure 1 - Unfiltered live capture" width="100%">
  <br><em>Figure 1 — Unfiltered live capture on the Wi-Fi interface, showing a mix of TLSv1.2, TCP, and mDNS traffic[cite: 1].</em>
</p>

### 4.2 TCP Traffic Filtering
I applied the `tcp` display filter to show only TCP packets, which reduced the view to 2,737 of 3,733 packets (about 73%)[cite: 2]. Several packets are marked `[TCP Retransmission]`, meaning some segments had to be sent again — a normal effect of packet loss or delay on a real Wi-Fi link[cite: 2].

<p align="center">
  <img src="https://raw.githubusercontent.com/radu-hatos/Network_Traffic_Analysis_with_Wireshark_Project/main/Figure%202.PNG" alt="Figure 2 - TCP filtered capture" width="100%">
  <br><em>Figure 2 — Capture filtered with tcp, including several TCP Retransmission segments[cite: 2].</em>
</p>

### 4.3 HTTP Traffic Filtering
I visited `http://platformait.ro` and applied the `http` display filter to show only the HTTP request/response traffic from loading the page[cite: 2]. The filtered view shows a series of GET requests for static files, fonts, and modules, served from a WordPress theme folder with their `HTTP/1.1 200 OK` responses, plus one `404 Not Found`[cite: 2, 3]. Because it was accessed over plain HTTP, Wireshark shows the full request line and headers in cleartext[cite: 3].

<p align="center">
  <img src="https://raw.githubusercontent.com/radu-hatos/Network_Traffic_Analysis_with_Wireshark_Project/main/Figure%203.PNG" alt="Figure 3 - HTTP filtered capture" width="100%">
  <br><em>Figure 3 — Capture filtered with http while loading platformait.ro, showing GET requests, response codes, and the cleartext HTTP payload in the hex pane[cite: 3].</em>
</p>

### 4.4 ARP Traffic Filtering
I applied the `arp` display filter to show only ARP traffic, which maps IP addresses to MAC addresses inside the local network[cite: 3]. The filtered view shows repeated broadcast "Who has..." requests from the router, plus a unicast ARP reply[cite: 3].

<p align="center">
  <img src="https://raw.githubusercontent.com/radu-hatos/Network_Traffic_Analysis_with_Wireshark_Project/main/Figure%204.PNG" alt="Figure 4 - ARP filtered capture" width="100%">
  <br><em>Figure 4 — Capture filtered with arp, showing broadcast address-resolution requests and a unicast reply[cite: 3].</em>
</p>

---

## 5. Skills Demonstrated

* Capturing live packets and choosing the interface in Wireshark[cite: 4].
* Reading the Wireshark packet list, protocol column and hex/ASCII view[cite: 4].
* Building and applying display filters (`tcp`, `http`, `arp`) to isolate traffic[cite: 4].
* Recognizing how each protocol behaves: TCP retransmissions, TLS application data, mDNS service discovery, HTTP response codes, ARP request/reply[cite: 4].
* Understanding cleartext vs. encrypted protocols (HTTP vs. HTTPS/TLS) by looking at the packets[cite: 4].
* Clear technical documentation of a network analysis exercise[cite: 4].

---

## 6. Tools Used

* Wireshark[cite: 4]

---

<p align="center">
  📄 <b>Download PDF Documentation:</b><br>
  [ EN ] <a href="https://raw.githubusercontent.com/radu-hatos/Network_Traffic_Analysis_with_Wireshark_Project/main/Network_Traffic_Analysis_with_Wireshark_Project.pdf"><b>[ English Version PDF ]</b></a><br>
  [ ES ] <a href="https://raw.githubusercontent.com/radu-hatos/Network_Traffic_Analysis_with_Wireshark_Project/main/Proyecto_Analisis_de_Trafico_de_Red_con_Wireshark.pdf"><b>[ Versión en Español PDF ]</b></a>
</p>
