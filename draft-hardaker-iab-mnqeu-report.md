---
title: "IAB workshop report: Measuring Network Quality for End-Users"
abbrev: title
docname: draft-hardaker-iab-mnqeu-report-00
category: info
ipr: trust200902

stand_alone: yes
pi: [toc, sortrefs, symrefs, docmapping]

author:
  -
    ins: W. Hardaker
    name: Wes Hardaker
    org: USC/ISI
    email: ietf@hardakers.net

normative:
  RFC2119:
  RFC5155:
  RFC4035:

informative:
  RFC1111:


--- abstract

The Measuring Network Quality for End-Users workshop was held
virtually by the Internet Architecture Board (IAB) in September, 2021.
This workshop summarizes the workshop, the topics discussed and some
preliminary conclusions drawn at the end of the workshop. 

--- middle

# Introduction

The Internet Architecture Board (IAB) holds occasional workshops
designed to consider long-term issues and strategies for the
Internet, and to suggest future directions for the Internet
architecture.  This long-term planning function of the IAB is
complementary to the ongoing engineering efforts performed by working
groups of the Internet Engineering Task Force (IETF).

The Measuring Network Quality for End-Users workshop was held
virtually by the Internet Architecture Board (IAB) in September, 2021.
This workshop summarizes the workshop, the topics discussed and some
preliminary conclusions drawn at the end of the workshop. 

## Problem space

The Internet in 2021 is quite different from what it was 10 years
ago. Today, it is a crucial part of everyone’s daily life. People use
the Internet for their social life, for their daily jobs, for routine
shopping, and for keeping up with major events. An increasing number
of people can access a Gigabit connection, which would be hard to
imagine a decade ago. And, thanks to improvements in security, people
trust the Internet for both planning their finances and for everyday
payments.

At the same time, some aspects of end-user experience have not
improved as much. Many users have typical connection latency that
remains at decade-old levels. Despite significant reliability
improvements in data center environments, end users often see
interruptions in service. Despite algorithmic advances in the field of
control theory, one can often find that the queuing delay in the
last-mile equipment exceeds the accumulted transit delay. Transport
improvements, such as QUIC, Multipath TCP, and TCP Fast Open are still
not fully supported in some networks. Likewise, various advances in
the security and privacy of user data are not widely supported, such
as encrypted DNS to the local resolver.

Some of the major factors behind this lack of progress is the popular
perception that throughput is the often sole measure of the quality of
Internet connectivity. With such narrow focus, the workshop aimed to
discuss various questions:

- What is the latency under typical working conditions?
- How reliable is the connectivity across longer time periods?
- Does the network allow the use of a broad range of protocols?
- What services can be run by clients of the network?
- What kind of IPv4, NAT or IPv6 connectivity is offered, and are
  there firewalls?
- What security mechanisms are available for local services, such as
  DNS?
- To what degree are the privacy, confidentiality, integrity and
  authenticity of user communications guarded?
- Improving these aspects of network quality will likely depend on
  measurement and exposing metrics to all involved parties, including
  to end users in a meaningful way. Such measurements and exposure of
  the right metrics will allow service providers and network operators
  to focus on the aspects that impacts the users’ experience most and
  at the same time empowers users to choose the Internet service that
  will give them the best experience.
- What are the fundamental properties of a network that contribute to good user experience?
- What metrics quantify these properties, and how to collect such metrics in a practical way?
- What are the best practices for interpreting those metrics, and incorporating those in a decision making process?
- What are the best ways to communicate these properties to service providers and network operators?
- How can these metrics be displayed to users in a meaningful way?

# Workshop Agenda

The Measuring Network Quality for End-Users for divided into the
following main topic areas:

- Introduction overviews and a keynote by Vint Cerf
- Consideration of metrics
- Cross-layer considerations
- Synthesis
- Group conclusions

# Position Papers

- Stuart Cheshire. "The Internet is a Shared Network"
- Jana Iyengar. "The Internet Exists In Its Use"
- Yaakov (J) Stein. "The Futility of QoS"
- Keynote by Vint Cerf
- Pedro Casas. "10 Years of Internet-QoE Measurements. Video, Cloud, Conferencing, Web and Apps. What do we need from the Network Side?"
- Lucas Pardue, Sreeni Tellakula. "Lower layer performance not indicative of upper layer success"
- Ahmed Aldabbagh. "Regulatory perspective on measuring network quality for end users"
- Michael Welzl. "A Case for Long-Term Statistics"
- Joachim Fabini. "Objective and subjective network quality"
- Matt Mathis. "Preliminary Longitudinal Study of Internet Responsiveness"
- Brandon Schlinker. "Internet’s performance from Facebook’s edge"
- Jonathan Foulkes. "Metrics helpful in assessing Internet Quality"
- Vijay Sivaraman, Sharat Madanapalli, Himal Kumar. "Measuring Network Experience Meaningfully, Accurately, and Scalably"
- Dave Reed, Levi Perigo. "Measuring ISP Performance in Broadband America: a Study of Latency Under Load"
- Kyle MacMillian, Nick Feamster. "Beyond Speed Test: Measuring Latency Under Load Across Different Speed Tiers"
- Gregory Mirsky, Xiao Min, Gyan Mishra, Liuyan Han. "Error Performance Measurement in Packet-Switched Networks"
- Gino Dion. "Focusing on latency, not throughput, to provide better internet experience and network quality"
- Praveen Balasubramanian. "Transport Layer Statistics for Network Quality"
- Jari Arkko, Mirja Kuehlewind. "Observability is needed to improve network quality"
- Robin Marx, Joris Herbots. "Merge Those Metrics: Towards Holistic (Protocol) Logging"
- Rajat Ghai. "Measuring & Improving QoE on the Xfinity Wi-Fi Network"
- Koen De Schepper, Olivier Tilmans, Gino Dion. "Challenges and opportunities of hardware support for Low Queuing Latency without Packet Loss"
- Olivier Bonaventure, Francois Michel. "Packet delivery time as a tie-breaker for assessing Wi-Fi access points"
- Ken Kerpez, Jinous Shafiei, John Cioffi, Pete Chow, Djamel Bousaber. "State of Wi-Fi Reporting"
- Mikhail Liubogoshchev. "Cross-layer Cooperation for Better Network Service"
- Sandor Laki, Szilveszter Nadas, Balazs Varga, Luis M. Contreras. "Incentive-Based Traffic Management and QoS Measurements"
- Satadal Segupta, Hyojoon Kim, Jennifer Rexford. "Fine-Grained RTT Monitoring Inside the Network"
- Al Morton. "Dream-Pipe or Pipe-Dream: What Do Users Want (and how can we assure it)?"
- Kalevi Kilkki, Benajamin Finley. "In Search of Lost QoS"
- Neil Davies, Peter Thompson. "Measuring Network Impact on Application Outcomes using Quality Attenuation"
- Mingrui Zhang, Vidhi Goel, Lisong Xu. "User-Perceived Latency to measure CCAs"
- Discussion
- Break
- Christoph Paasch, Randall Meyer, Stuart Cheshire, Omer Shapira. "Responsiveness under Working Conditions"
- Bob Briscoe, Greg White, Vidhi Goel and Koen De Schepper. "A single common metric to characterize varying packet delay"
- Christoph Paasch, Kristen McIntyre, Randall Meyer, Stuart Cheshire, Omer Shapira. "An end-user approach to the Internet Score"

# Discussions

## Background

TBD

## Metrics

TBD

## Cross-layer considerations

TBD

## Synthesis

TBD

# Conclusions

During the final hour of the workshop we gathered statements that
group thought were summary statements from the 3 day event.  We later
discarded any that were in contention (listed further below for
completeness), resulting in the following list.

1. New measurements and QoS or QoE techniques should not rely only or
   depend on reading TCP headers
2. Latency mean and medians are distractions from better measurements
3. It is frustrating to only measure network services without
   simultaneously improving those services
4. Round trips Per Minute (RPM) is a useful, consumable metric
5. In many cases, Internet users don’t need more bandwidth, but rather
   need "better bandwidth" -- i.e., they need other improvements to
   connectivity.
6. Stakeholder incentives aren’t aligned for easy wins in this space.
   Incentives are needed to motivate improvements in public network
   access.  Measurements may be one step toward driving competitive
   market incentive.
7. We need both active and passive measurements – passive measurements
   can provide historical debugging.
8. A really meaning metric for users is whether their application will
   work properly or fail because of a lack of a  network with
   sufficient characteristics.
9. It is clear from developers of interactive applications and from
   network operators that lower latency is a strong factor in user
   QoE.  However, metrics are lacking to support this statement
   directly.
10. A useful metric for goodness must actually incentive goodness --
    good metrics should help drive industry toward improvement.
11. We need passive measurements to be continuous and archivable and
    queriable – include reliability/connectivity measurements.
12. A lower latency internet, however achieved would benefit all end
    users.
13. We need a usable tool that fills the current gap between network
    reachability, latency and speed tests.
14. Bandwidth is necessary but not alone sufficient
15. End-users that want to be involved in QoS decisions should be able
    to voice their needs and desires.
16. Applications are needed that can perform and report good quality
    measurements in order to identify insufficient points in 
    network access.
17. Research done by regulators indicate that users/consumers prefer
    a simple metric per application, which frequently resolves to
    whether the application will work properly not.
18. For the future proof networking, measuring ecological impact of
    measuring material and energy usage is important.
19. We do not have incontrovertible evidence that any one metric
    (e.g. latency or speed) is more important than others to persuade
    device vendors to concentrate on any one optimization.

Additional statements were recorded that did not have consensus of the
group at the time, but we list here for completeness about the fact
they were discussed:

1. We do not have incontrovertible evidence that buffer bloat is a
   prevalent problem
2. We do not have incontrovertible evidence that buffer bloat is a
   prevalent problem
3. The measurement needs to support reporting localization in order to
   find problems
    1. Detecting a problem is not sufficient if you can’t find the location
    2. Need more than just english – different localization concerns
4. Stakeholder incentives aren’t aligned for easy wins in this space

## Follow on work

# Security considerations

A few security relevant topics were discussed at the workshop,
including but not limited to:

- What prioritization techniques can work without invading the privacy
  of the communicating parties.
- How oversubscribed networks can essentially be viewed as a DDoS
  attack.

--- back

# Participants List

The following is a list of participants attended the workshop over a remote connection:

- list...

IAB Members at the Time of Approval

Internet Architecture Board members at the time this document was
approved for publication were:

    Jari Arkko

    Deborah Brungard
    Ben Campbell
    Lars Eggert
    Wes Hardaker
    Cullen Jennings
    Mirja Kühlewind
    Zhenbin Li
    Jared Mauch
    Tommy Pauly
    Colin Perkins
    David Schinazi
    Russ White
    Jiankang Yao
    
Acknowledgements

The authors would like to thank the workshop participants, the members
of the IAB, and the program committee for creating and participating
in many interesting discussions.

# Github Version of this document

While this document is under development, it can be viewed, tracked,
fill here:

https://github.com/intarchboard/network-quality-workshop-report

