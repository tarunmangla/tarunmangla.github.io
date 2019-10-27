---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---
<span style="font-size: 0.875em">
 My work spans the area of computer networking with a focus on using network measurement data to understand and improve network performance. The projects that I have worked on include using passive network measurments to estimate end-user video QoE, measuring broadband availability in the US, and understanding the benefits of network redundancy in VoIP.
</span>


Video QoE inference 
-----
<span style="font-size: 0.875em"> The goal of this work is to use passive network measurements to estimate end-user video QoE. We address both the algorithmic and systems-related challenges in this work. </span>

<span style="font-size: 0.875em"> **MIMIC**: We first develop an algorithm, called *MIMIC*, that estimates video QoE metrics such as re-buffering and video quality for unecrypted HTTP-based video. The algorithm uses information extracted from the application-layer headers that can be collected by using a transparent web proxy in the network. *MIMIC* is based on the insight that an HTTP-based video session can be modeled as a sequence of chunk downloads on the network. We do a large-scale validation of our algorithm using ground truth QoE metrics from a popular video streaming service. [[**MNM'17**](../files/mimic_mnm17.pdf)] </span>

<span style="font-size: 0.875em"> **eMIMIC**: We then devise a method to estimate QoE metrics for encrypted HTTP-based video. Our goal here was to design an estimation algorithm that is fairly generalizable, minimally dependent on ground truth QoE metrics, and fine-granular in terms of estimation. The method first reconstructs HTTP transactions from packet-level traces using the directionality property of HTTP. We then devise heurisitcs using insights from the HTTP-based video streaming protocols to identify video transactions and then use them to model a video session at the client. We evaluate *eMIMIC* using data from three popular streaming services. Our evaluation shows that *eMIMIC* outperforms state-of-the-art QoE inference approaches. [[**TMA'18**](../files/emimic_tma18.pdf), [**TNSM'19**](../files/emimic_tnsm19.pdf)]

<span style="font-size: 0.875em"> **VideoNOC**: This work presents a design for a scalable QoE inference system for cellular networks. *VideoNOC* addresses three main challenges: i) a scalable and light-weight QoE inference system using transparent web proxy, ii) cross-layer data aggregation challenges arising because of building over existing cellular network architecture, iii) video session identification and QoE estimation (uses *MIMIC*). The system is running in a part of a major cellular network in the US. We also present various use cases of the *VideoNOC* including understanding the current video demand and understanding the impact of network or application-layer changes on video QoE. [[**MMSys'18**](../files/videonoc_mmsys18.pdf)] </span>


Measuring broadband access in the US
----
<span style="font-size: 0.875em">
There have been various reports that qualitatively critique the FCC broadband access data for overreporting access. The goal of this work is to understand and quanitfy broadband access in the US. Our methodology involves using alternative data sets that are collected using different methodologies and comparing them with the FCC broadband access data. [**ongoing**]
</span>



Network redundancy in VoIP
----
<span style="font-size: 0.875em">
VoIP has become quite popular especially with the advent of services such as WhatsApp, Google Duo, and Facebook. VoIP is known to get critically affected  by network QoS metrics such as packet loss, latency and jitter. Unfortunately, public Internet is a best-effort network and does not provide any QoS guarantee. Hence, despite being popular, these services do not provide the same level of reliability as traditional public telephone system. At  the  same  time,  clients these days usually  have  a  choice  of  multiple  network  paths. For example, smartphones can usually connect to Internet using both  cellular  and  WiFi. This work analyzes the performance benefits of network redundancy over diverse network paths in VoIP. </span>


<span style="font-size: 0.875em">
We analyzed the performance benefits of redundancy at different levels in the network, namely last-mile and WAN. This involved obtaining network measurements under controlled settings and also in the wild. These measurements were collected using an Android application and a javascript-based tool. Our measurement dataset shows that network redundancy significantly helps in reducing the tail latency and packet loss in the network; thus improving the overall performance of VoIP. We also explored policies to use selective replication instead of full-replication in order to reduce the cost. 
[**MSR intern project**]
</span>



