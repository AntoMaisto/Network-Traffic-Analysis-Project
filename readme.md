# 📡 Network Traffic & Wireless Security Analysis

A network analysis project focused on WiFi performance, TCP/UDP traffic behavior, GNSS measurements, and spoofing detection through practical experiments and traffic analysis.

<br>

## 📌 Overview

This project explores network performance and wireless security through experimental analysis of WiFi communications and GNSS signals.

<br>

The project includes:

- WiFi and Ethernet performance analysis
- TCP and UDP traffic evaluation
- Network packet capture and inspection
- Goodput, RTT, packet loss, and congestion analysis
- WiFi bottleneck and channel asymmetry investigation
- GNSS raw measurement analysis
- GNSS signal quality evaluation
- GNSS spoofing simulation and detection

## 🌐 WiFi Performance Analysis

Network performance was evaluated across different connection scenarios:

<br>

- WiFi-to-WiFi
- WiFi-to-Ethernet
- Ethernet-to-Ethernet
- Forward and reverse traffic flows

TCP and UDP traffic was generated with **iPerf3** and analyzed using **Wireshark**.

The experiments focused on:

<br>

- Goodput and throughput
- Round-Trip Time (RTT)
- Packet loss
- TCP acknowledgements
- TCP window behavior
- Packet and segment size
- Network congestion
- WiFi channel asymmetry

## 📊 TCP & UDP Analysis

TCP experiments highlighted the impact of congestion, delayed acknowledgements, and wireless channel conditions on network performance.

<br>

Wireshark analysis included:

- TCP sequence numbers
- RTT variations
- TCP Window Full events
- Packet transmission rates
- MTU and segment size behavior
- Traffic flow interruptions

UDP experiments investigated the relationship between **bitrate, packet size, and packet loss**.

A target bitrate of **70 Mbit/s** with **1472-byte packets** provided a good balance in the WiFi-to-WiFi scenario, reaching approximately **68.5 Mbit/s** at the receiver with about **1.3% packet loss**.

## 📡 GNSS Signal Analysis

Raw GNSS measurements were collected using Android smartphones and analyzed to evaluate positioning accuracy and signal quality.

<br>

The analysis considered:

- Pseudorange measurements
- Carrier-to-Noise density ratio (C/N₀)
- Horizontal velocity
- Satellite availability
- Receiver clock bias
- HDOP
- Multipath effects
- Positioning accuracy

Custom filtering based on satellite behavior and signal quality reduced the radius containing 50% of position estimates from approximately **8.8 m to 4.2 m**.

## 🛰️ GNSS Spoofing Detection

GNSS spoofing scenarios were analyzed to understand how manipulated satellite signals affect positioning and timing.

<br>

Detection focused on anomalies such as:

- Sudden pseudorange jumps
- Abnormal pseudorange rates
- Position estimation shifts
- Horizontal velocity spikes
- Clock bias discontinuities
- Satellite consistency anomalies

The experiments also investigated **time-delay-based spoofing**, where manipulated signals gradually influence the receiver while attempting to remain less noticeable.

## 🔍 Traffic & Signal Analysis

Multiple metrics were combined to identify abnormal network and GNSS behavior.

<br>

For network traffic:

- RTT
- Goodput
- Packet loss
- Sequence numbers
- TCP window state
- Packet rate

For GNSS signals:

- Pseudorange
- Pseudorange rate
- C/N₀
- Clock bias
- HDOP
- Position and velocity estimates

This approach demonstrates how low-level measurements can be used to diagnose performance problems and identify anomalous or manipulated signals.

## 🛠️ Technologies

**Network Analysis:** Wireshark

**Traffic Generation:** iPerf3

**Wireless Networking:** WiFi, IEEE 802.11ac, WPA2

**Protocols:** TCP, UDP, IP

**GNSS Analysis:** GNSS Raw Measurements, GnssLogger

**Data Analysis:** MATLAB

**Systems:** Linux, Android

**Automation:** Bash

## 🎯 Key Features

- TCP and UDP traffic analysis
- WiFi and Ethernet performance comparison
- Goodput and packet loss measurement
- RTT and congestion investigation
- Automated iPerf3 testing
- Packet-level analysis with Wireshark
- GNSS raw measurement processing
- GNSS signal quality filtering
- Positioning accuracy analysis
- GNSS spoofing detection
- Time-delay spoofing analysis

## 🚀 Future Improvements

- Automated network anomaly detection
- Real-time traffic monitoring
- Larger WiFi performance datasets
- WiFi 6/6E performance comparison
- Automated GNSS spoofing detection
- Machine learning for signal anomaly classification
- Real-time GNSS integrity monitoring
