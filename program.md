---
layout: about
title: Program
permalink: /program/
---

# {{ page.title }}

TCRS '24 will take place at ESWEEK on October 3, 2024, in Raleigh, NC.
Details about the program and location are shown below.

### Date: October 3, 2024 <br> Location: Hannover II, Sheraton Raleigh Hotel

## Session 1: Coordinating Time-Sensitive Dynamic Systems
### 10:30-12:30
#### Layered Scheduling: Toward Better Real-Time Lingua Franca
**Francesco Paladino, Erling Jellum, Efsane Soyer, Edward A. Lee**
<div style="text-align: justify">
<b>Abstract</b> Lingua Franca is a programming paradigm that eases the development of distributed cyber-physical systems and ensures determinism. These systems are subject to stringent timing constraints, generally expressed as task deadlines, and meeting them requires real-time scheduling. This work presents a layered scheduling strategy for Lingua Franca for enhanced real-time performance that builds upon any priority-based operating system thread scheduler. The application designers need to specify only the application-specific deadlines, and the Lingua Franca runtime automatically converts them into appropriate priority values for the OS scheduler to obtain earliest deadline first scheduling.
</div>

#### Toward Dynamism in Distributed Lingua Franca Programs
**Chadlia Jerad, Edward A. Lee**
<div style="text-align: justify">
<b>Abstract</b> Distributed systems often require dynamic capabilities to ensure adaptability, efficiency, and fault-tolerance. In applications where determinism and timing are crucial, a clear and well-defined approach to deterministic dynamism is much needed, but inherently difficult to define. This work gives dynamism deterministic semantics, thus enabling precise and repeatable behavior. To this end, we select the Lingua Franca (LF) coordination language that is based on the reactor model, and introduce dynamism to the distributed LF programs, referred to as federations. This paper outlines the challenges associated with incorporating transient federates, which are capable of joining and leaving the federation at arbitrary times, and proposes solutions to the identified problems. A realistic example of an online auction system is used to illustrate the approach. Furthermore, the potential applications of this mechanism are discussed, along with the challenges that need to be addressed.
</div>

#### Navigating Time and Energy Trade-offs in Reactive Heterogeneous Systems
**Shaokai Lin, Tassilo Tanneberger, Jiahong Bi, Guangyu Feng, Ruomu Xu, Julian Robledo, Robert Khasanov, Jeronimo Castrillon**
<div style="text-align: justify">
<b>Abstract</b> Reactive software poses stringent and comprehensive requirements: deterministic execution with stringent timing constraints under a tight energy budget. Meeting these requirements is particularly challenging when executing on the increasingly heterogeneous platforms of today. In this paper, we integrate MOCASIN, a design space exploration tool, into LINGUA FRANCA, a programming framework for building deterministic and timed reactive software. We show that this integration enables choosing a desired timing and energy performance at design time. We demonstrate our approach in a satellite attitude control application consisting of periodic real-time tasks and sporadic non-real-time tasks. The latter sporadic tasks are coordinated using quasi-static schedules, computed by MOCASIN, leading to less energy consumption compared to the Linux scheduler under CPU frequency scaling governors such as powersave, schedutil, and ondemand.
</div>

#### Lustre, Fast First and Fresh
**Timothy Bourke, Marc Pouzet**
<div style="text-align: justify">
<b>Abstract</b> The rate-synchronous model formalizes an industrial approach for composing Lustre nodes that execute at different rates. Such programs are compiled to cyclic sequential code in two steps. First, an Integer Linear Program is solved to assign each component to a phase relative to its period. Second, the corresponding step functions are ordered for execution within a cycle of the generated code. By default, programs are deterministic: for any valid schedule, the generated code calculates the values decreed by the source dataflow semantics at the specified rates. In practice, though, specifying precise values in the source program is sometimes unnecessary, impracticable, and overly constraining. In this case, the ILP constraints can be relaxed, though not necessarily completely, and their solution decides which dataflow semantics applies. Care is still required to ensure that code generation remains deterministic.
</div>


## Session 2: Keynote
### 13:30-15:00
#### Certification of (hybrid) multi-core architectures
![Claire Pagetti]({{ site.baseurl }}/assets/images/claire_pagetti.jpg){: style="float: left; margin-top: 1em; margin-right: 1.8em; margin-bottom: .8em"}
<div style="text-align: justify">
<b>Claire Pagetti</b> is a senior research scientist at ONERA. She
holds a research chair in the ANITI project on “New certification
approaches of AI based systems for civil aeronautics”. Her fields of
interest concern the safe implementation of safety critical applications
on avionic platforms. She has contributed to several industrial,
European and French projects that lead to several publications and
industrial developments.

</div>
<br/>
<div style="text-align: justify">
<b>Abstract</b> Multi-core processors have been available for many years on the market and they have been consequently embedded in safety-critical systems (e.g. automotive domain) for more than a decade. They have yet to break through in the avionic domain, one subject to certification. To allow the use of new technologies in a system, the applicant to certification must ensure safety properties and in particular its compliance with certification standards. The A(M)C AMC20-152A and AMC20-193 (formally CAST 32A) define objectives for the respective certification of hardware platforms and of multi-core processors. The PHYLOG project (2016 - 2020) proposed a methodology to facilitate the certification of multi-core processors in the avionic domain. Among the project outcomes, we will present the formal language PML that helps identify interferences within processors, and a stressing benchmarks methodology to help quantify the impact of said interferences.
<br>
Multi-core processors certification is now a reality and many applicants are working towards their certification. The emergence of Deep Neural Network (DNN) and machine learning-based applications paved the way for a new generation of hybrid hardware platforms. Hybrid platforms embed several cores and hardware accelerators in a small package. PHYLOG 2, as a follow up of PHYLOG, aims to prepare for the certification of these new platforms. We will present the advancement of the PHYLOG methodology extension for them.
</div>

## Session 3: Timing Challenges in Cyber-Physical Systems
### 15:30-17:00
#### Software-Defined Watchdog Timers for Cyber-Physical Systems
**Benjamin Asch, Erling Jellum, Marten Lohstroh, Edward A. Lee**
<div style="text-align: justify">
<b>Abstract</b> This paper introduces software-defined watchdogs, a
programming model for handling faults that manifest as delayed
or missing signals. The programming model is implemented
as an extension to the polyglot coordination language LINGUA
FRANCA, where it acts as an eager deadline for delayed inputs.
The technique is compared against hardware-defined watchdogs
and software watchdogs in other reactive languages.
</div>

#### Time-Sensitive Networking in Cyber-Physical Systems
**Henrik Austad, Geir Mathisen**
<div style="text-align: justify">
<b>Abstract</b> As the usage of Cyber-Physical Systems continues to grow, the demand for low-latency, reliable networks increases. This paper covers available traffic control mechanisms in Time Sensitive Networks and discusses how they can provide strict latency guarantees, analyzable networks, and reliable sensor streams. We discuss the pros and cons of each approach in an attempt to guide the selection of the most appropriate technology with an extra focus on low-latency Cyber-Physical Systems.
</div>

#### GNN-MiCS: Graph Neural-Network-Based Bounding Time in Embedded Mixed-Criticality Systems
**Behnaz Ranjbar, Paul Justen, Akash Kumar**
<div style="text-align: justify">
<b>Abstract</b> In Mixed-Criticality (MC) systems, each task has multiple WCETs for different operation modes. Determining WCETs for low-criticality modes (LO modes) is challenging. A lower WCET improves processor utilization, but a longer one reduces mode switches, maintaining smooth task execution even with low utilization. Most research focuses on WCETs for the highest criticality mode, with fewer solutions for LO modes in graph-based applications. This paper proposes GNNMiCS, a machine learning and graph neural networks scheme to determine WCETs for directed acyclic graph applications in LO modes. GNN-MiCS generates test sets and computes proper WCETs based on the application graph to enhance system timing behavior. Experiments show our approach improves MC system utilization by up to 45.85% and 22.45% on average while maintaining a reasonable number of mode switches in the worstcase scenario.
</div>
