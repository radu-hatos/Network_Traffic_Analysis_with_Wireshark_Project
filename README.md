# Network_Traffic_Analysis_with_Wireshark_Project

<h1 align="center">Network Traffic Analysis with Wireshark Project</h1>

<p align="center">
  <b>[ EN ]</b> Live Packet Capture & Protocol Filtering &nbsp;|&nbsp; <b>[ ES ]</b> Captura de Paquetes y Filtrado de Protocolos
</p>

<p align="center">
  📄 <b>Download PDF Documentation / Descargar Documentación PDF:</b><br>
  [ EN ] <a href="https://raw.githubusercontent.com/radu-hatos/Network_Traffic_Analysis_with_Wireshark_Project/main/Network_Traffic_Analysis_with_Wireshark_Project.pdf"><b>[ English Version ]</b></a><br>
  [ ES ] <a href="https://raw.githubusercontent.com/radu-hatos/Network_Traffic_Analysis_with_Wireshark_Project/main/Proyecto_Analisis_de_Trafico_de_Red_con_Wireshark.pdf"><b>[ Versión en Español ]</b></a>
</p>

<hr>

## 📋 Index / Índice

* [1. Introduction / Introducción](#1-introduction--introducción)
* [2. Objective / Objetivo](#2-objective--objetivo)
* [3. Capture Environment / Entorno de Captura](#3-capture-environment--entorno-de-captura)
* [4. Work Performed / Trabajo Realizado](#4-work-performed--trabajo-realizado)
  * [4.1 Live Traffic Capture / Captura de Tráfico en Vivo](#41-live-traffic-capture--captura-de-tráfico-en-vivo)
  * [4.2 TCP Traffic Filtering / Filtrado de Tráfico TCP](#42-tcp-traffic-filtering--filtrado-de-tráfico-tcp)
  * [4.3 HTTP Traffic Filtering / Filtrado de Tráfico HTTP](#43-http-traffic-filtering--filtrado-de-tráfico-http)
  * [4.4 ARP Traffic Filtering / Filtrado de Tráfico ARP](#44-arp-traffic-filtering--filtrado-de-tráfico-arp)
* [5. Skills Demonstrated / Habilidades Demostradas](#5-skills-demonstrated--habilidades-demostradas)
* [6. Tools Used / Herramientas Utilizadas](#6-tools-used--herramientas-utilizadas)

---

## 1. Introduction / Introducción

<details>
<summary><b>[ EN ] Read English Content</b></summary>

This is a network traffic analysis exercise carried out independently using Wireshark to capture and analyse packets[cite: 1]. The focus is on understanding network protocols at the packet level and applying display filters to isolate target traffic from a live capture[cite: 1].

</details>

<details>
<summary><b>[ ES ] Leer Contenido en Español</b></summary>

Este es un ejercicio de análisis de tráfico de red realizado de forma independiente utilizando Wireshark para capturar y analizar paquetes[cite: 1]. El enfoque se centra en comprender los protocolos de red a nivel de paquete y aplicar filtros de visualización para aislar el tráfico de interés a partir de una captura en directo[cite: 1].

</details>

---

## 2. Objective / Objetivo

<details>
<summary><b>[ EN ] Read English Content</b></summary>

Capture live network traffic in Wireshark and use display filters (`tcp`, `http`, `arp`) to isolate and study TCP connections, HTTP requests, and ARP address resolution[cite: 1].

</details>

<details>
<summary><b>[ ES ] Leer Contenido en Español</b></summary>

Capturar tráfico de red en directo en Wireshark y utilizar filtros de visualización (`tcp`, `http`, `arp`) para aislar y estudiar conexiones TCP, peticiones HTTP y resolución de direcciones ARP[cite: 1].

</details>

---

## 3. Capture Environment / Entorno de Captura

<details>
<summary><b>[ EN ] Read English Content</b></summary>

* **Capture interface:** Wi-Fi (wireless network adapter)[cite: 1]
* **Traffic type:** Live traffic on a home network[cite: 1]
* **Analysis tool:** Wireshark[cite: 1]

The capture was taken on a real network, including normal background activity (TLS, TCP, mDNS) and intentional exercise traffic[cite: 1].

</details>

<details>
<summary><b>[ ES ] Leer Contenido en Español</b></summary>

* **Interfaz de captura:** Wi-Fi (adaptador de red inalámbrico)[cite: 1]
* **Tipo de tráfico:** Tráfico en directo en una red doméstica[cite: 1]
* **Herramienta de análisis:** Wireshark[cite: 1]

La captura se realizó en una red real, incluyendo actividad de fondo normal (TLS, TCP, mDNS) y tráfico generado para el ejercicio[cite: 1].

</details>

---

## 4. Work Performed / Trabajo Realizado

### 4.1 Live Traffic Capture / Captura de Tráfico en Vivo
<details>
<summary><b>[ EN ] Read English Content</b></summary>
Started an unfiltered capture on the Wi-Fi interface, observing a realistic mix of protocols (TLSv1.2, TCP segments, mDNS service discovery)[cite: 1].
</details>
<details>
<summary><b>[ ES ] Leer Contenido en Español</b></summary>
Se inició una captura sin filtros en la interfaz Wi-Fi, observando una mezcla realista de protocolos (TLSv1.2, segmentos TCP, descubrimiento de servicios mDNS)[cite: 1].
</details>

### 4.2 TCP Traffic Filtering / Filtrado de Tráfico TCP
<details>
<summary><b>[ EN ] Read English Content</b></summary>
Applied the `tcp` display filter to isolate TCP packets, observing retransmissions due to network conditions[cite: 2].
</details>
<details>
<summary><b>[ ES ] Leer Contenido en Español</b></summary>
Se aplicó el filtro de visualización `tcp` para aislar los paquetes TCP, observando retransmisiones causadas por condiciones de la red[cite: 2].
</details>

### 4.3 HTTP Traffic Filtering / Filtrado de Tráfico HTTP
<details>
<summary><b>[ EN ] Read English Content</b></summary>
Applied the `http` display filter to examine GET requests, status codes, and cleartext payloads[cite: 2, 3].
</details>
<details>
<summary><b>[ ES ] Leer Contenido en Español</b></summary>
Se aplicó el filtro de visualización `http` para examinar peticiones GET, códigos de estado y payloads en texto plano[cite: 2, 3].
</details>

### 4.4 ARP Traffic Filtering / Filtrado de Tráfico ARP
<details>
<summary><b>[ EN ] Read English Content</b></summary>
Applied the `arp` display filter to examine address resolution broadcast requests and unicast replies[cite: 3].
</details>
<details>
<summary><b>[ ES ] Leer Contenido en Español</b></summary>
Se aplicó el filtro de visualización `arp` para examinar las solicitudes de difusión de resolución de direcciones y respuestas unicast[cite: 3].
</details>

---

## 5. Skills Demonstrated / Habilidades Demostradas

<details>
<summary><b>[ EN ] Read English Content</b></summary>

* Live packet capturing and interface selection in Wireshark[cite: 4].
* Reading packet lists, protocol columns, and hex/ASCII views[cite: 4].
* Building and applying display filters (`tcp`, `http`, `arp`)[cite: 4].
* Recognizing protocol behaviors and cleartext vs. encrypted traffic[cite: 4].

</details>

<details>
<summary><b>[ ES ] Leer Contenido en Español</b></summary>

* Captura de paquetes en directo y selección de interfaz en Wireshark[cite: 4].
* Lectura de listas de paquetes, columnas de protocolos y vistas hexadecimal/ASCII[cite: 4].
* Construcción y aplicación de filtros de visualización (`tcp`, `http`, `arp`)[cite: 4].
* Reconocimiento de comportamientos de protocolos y tráfico en texto plano frente a cifrado[cite: 4].

</details>

---

## 6. Tools Used / Herramientas Utilizadas

* **Wireshark**[cite: 4]

---

<p align="center">
  📄 <b>Download PDF Documentation / Descargar Documentación PDF:</b><br>
  [ EN ] <a href="https://raw.githubusercontent.com/radu-hatos/Network_Traffic_Analysis_with_Wireshark_Project/main/Network_Traffic_Analysis_with_Wireshark_Project.pdf"><b>[ English Version ]</b></a><br>
  [ ES ] <a href="https://raw.githubusercontent.com/radu-hatos/Network_Traffic_Analysis_with_Wireshark_Project/main/Proyecto_Analisis_de_Trafico_de_Red_con_Wireshark.pdf"><b>[ Versión en Español ]</b></a>
</p>
