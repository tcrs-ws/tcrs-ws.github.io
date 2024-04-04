---
layout: about
title: Program
permalink: /program/
---

# {{ page.title }}

TCRS '24 will take place on at ESWEEK in Raleigh, NC.
Details about the exact date and location will follow.

## Session 1 (Keynote)
### 9:00-10:00am
#### Safety First: Though on the Other Hand, Time is Critical
![Jonathan Sprinkle](/assets/images/jms2020-ua.jpg){: style="float: left; margin-top: 1em; margin-right: 1.8em; margin-bottom: .8em"}
<div style="text-align: justify">
<b>Jonathan Sprinkle</b> is a Professor of Computer Science at Vanderbilt University. Prior to joining Vanderbilt in 2021, he was the Litton Industries John M. Leonis Distinguished Associate Professor of Electrical and Computer Engineering at the University of Arizona, and the Interim Director of the Transportation Research Institute. In 2020 he was named a Distinguished Scholar of the University of Arizona. From 2017-2019 he served as a Program Director in Cyber-Physical Systems and Smart & Connected Communities at the National Science Foundation in the CISE Directorate. In 2013 he received the NSF CAREER award, and in 2009, he received the UA's Ed and Joan Biggers Faculty Support Grant for work in autonomous systems. His work has an emphasis for industry impact, and he was recognized with the UA "Catapult Award" by Tech Launch Arizona in 2014, and in 2012 his team won the NSF I-Corps Best Team award. His research interests and experience are in model-based approaches to cyber-physical systems, and he teaches courses ranging from systems modeling and control to mobile application development and software engineering.
</div>
<br/>
<div style="text-align: justify">
<b>Abstract</b>–This talk describes the deployment of research-quality software and hardware for open-road driving experiments by fleets of vehicles. Technological advancements in single-vehicle autonomy have expanded beyond the academic community, and are driven largely by industry stakeholders and manufacturers. However, as the penetration rate of cars with advanced driver assistance features increases, the impact on emergent behavior in traffic is still unknown. Compelling reasons to experiment within open-road conditions must be considered alongside the technical and human factor safety issues in deploying experimental controllers. This is even more challenging when it is necessary to deploy experimental fleets at scale. The talk will describe approaches for co-design of a research testbed for societal-scale systems. Discussion is devoted to the research-quality data gathering and control layers and their technical implementation, the different interfaces for experts in other fields to use these testbeds for research without violating safety requirements, and process and management considerations when deploying the platforms at scale when considering training time and operation complexity of human operators.
</div>

## Session 2
### 10:30-12:00am
#### Logical Time for Reactive Software
**Marten Lohstroh, Edward A. Lee, Stephen A. Edwards, David Broman**
<div style="text-align: justify">
<b>Abstract</b> Timing is an essential feature of reactive software. It is not just a
performance metric, but rather forms a core part of the semantics of
programs. This paper argues for a notion of logical time that serves
as an engineering model to complement a notion of physical time,
which models the physical passage of time. Programming models
that embrace logical time can provide deterministic concurrency,
better analyzability, and practical realizations of timing-sensitive
applications. We review languages and formalisms that embrace
the notion of logical time.
</div>

#### Semantics foundations of PsyC based on Synchronous Logical Execution Time
**Fabien Siron, Dumitru Potop, Robert de Simone, Damien Chabrol, Amira Methni**
<div style="text-align: justify">
<b>Abstract</b> Task models for Real-Time Scheduling Scheduling (RTS) and Synchronous Reactive (SR) languages are two prominent classes of
formalisms for the design and analysis of time-critical embedded
systems. Task models allow to provide deadlines, periods, or other
such kinds of interval time boundaries that make the system description fit for schedulability analysis. Synchronous reactive languages
use logical clocks to be activation condition triggers in languages
providing programmability. We consider here synchronous LET
(sLET) extensions that intend to re-use notions of logical clocks
and logical time, but this time to provide schedulability boundaries.
As its name indicates, sLET borrows deeply from Logical Execution
Time ideas, where timing dimensions are all provided at logical
design time, but they extend asynchronous events as in xGiotto
with SR-inspired programmability and “first-class citizen” logical
clock constructs. Our work results in a two-level semantics of the
programming language PsyC. The benefits are to endow the use of
techniques from both sides. Big-step RTS models provide inputs for
task model schedulability analysis and implementation. Meanwhile,
SR small-step models provide methodological tools to view any
events as a time base (logical clock) and verification technologies
(but they do not consider the WCET of tasks to be kept within time
boundaries by the scheduling). We show the semantic equivalence
of those two semantics at visible time interval boundaries.
</div>

#### Polyglot Modal Models through Lingua Franca
**Alexander Schulz-Rosengarten, Reinhard von Hanxleden, Marten Lohstroh, Soroush Bateni, Edward A. Lee**
<div style="text-align: justify">
<b>Abstract</b> Complex software systems often feature distinct modes of operation, each designed to handle a particular scenario that may require
the system to respond in a certain way. Breaking down system
behavior into mutually exclusive modes and discrete transitions
between modes is a commonly used strategy to reduce implementation complexity and promote code readability.
However, such capabilities often come in the form of self-contained domain specific languages or language-specific frameworks.
The work in this paper aims to bring the advantages of modal
models to mainstream programming languages, by following the
polyglot coordination approach of Lingua Franca (LF), in which
verbatim target code (e. g., C, C++, Python, Typescript, or Rust)
is encapsulated in composable reactive components called reactors. Reactors can form a dataflow network, are triggered by timed
as well as sporadic events, execute concurrently, and can be distributed across nodes on a network. With modal models in LF, we
introduce a lean extension to the concept of reactors that enables
the coordination of reactive tasks based on modes of operation.
</div>

## Session 3
### 1:30-3:00pm
#### Bounding the End-to-End Execution Time in Distributed Real-Time Systems: Arguing the Case for Deterministic Networks in Lingua Franca
**Henrik Austad, Geir Mathisen**
<div style="text-align: justify">
<b>Abstract</b> Designing and implementing distributed systems with real-time
requirements quickly reveals the complexity of handling time and
logic across multiple systems. As data traverse a network, it is
subjected to variable delay due to interfering traffic and variable
load on network components. This introduces an element of nondeterminism in execution time for distributed algorithms, which
translates into increased error logic and pessimistic worst-case estimates. Over the next few years, it is expected that cyber-physical
systems will see many new use cases, and the network connecting these will play an ever more important role. Combined with
the onset of the fourth industrial revolution, IEEEs Time Sensitive
Networking, IETFs Deterministic Networking and 3GPPs Ultra Reliable Low Latency profile will play a vital role in realizing these
systems. Coordination languages such as Lingua Franca can offer
a substantial contribution to the design process and implementation of distributed systems such as CPS, both through its model of
computation which elevates time to a first-class citizen and with
its support for distributed (or federated) models. In this paper, we
show that by introducing deterministic network channels with a
fixed delay, the worst-case execution time is not increased whereas
the variance in total execution time from start to finish is greatly
reduced. For a coordination language such as LF, this means that we
can analyze a system using much tighter delay bounds for network
traffic, which in turn can yield better resource utilization.
</div>

#### Towards Sparse Synchronous Programming in Lua
**John Hui, Stephen A. Edwards**
<div style="text-align: justify">
<b>Abstract</b> Most software considers timing a performance issue, but for many
embedded applications, the timing of a result is as important as its
value. Most modern computers do have precise hardware timers,
but they are not easily used to make a whole system timing-aware.
Earlier, we presented the Sparse Synchronous Model for specifying deterministic, concurrent, timing-aware systems and proposed
an awkward-to-use C library; here, we present lua-ssm, a Lua library that provides the benefits of SSM in a more accessible setting.
Relying on Lua’s incremental garbage collector and support
for coroutines, lua-ssm is both easier to use and was simpler to
implement than its C counterpart. It provides both a flexible way
for users to construct SSM systems and a way for us to more quickly
experiment with new features.
</div>

#### LetSynchronise: An Open-Source Framework for Analysing and Optimising Logical Execution Time Systems
**Eugene Yip, Matthew M. Y. Kuo**
<div style="text-align: justify">
<b>Abstract</b> The paper presents early work on LetSynchronise, an open-source
framework that aims to facilitate research and collaboration on
Logical Execution Time (LET) systems. It offers a web application
for modelling, simulating, analysing, and optimising LET systems,
which can be extended via user-defined plugins for the rapid prototyping of scheduling policies, timing analysers, and optimisation
algorithms. Its capabilities are demonstrated through use cases and
a small research case study.
</div>

## Session 4
### 3:30-5:00pm
#### Reliable Event Detection Using Time-Synchronized IoT Platforms
**Byeong-gil Jun, Dongha Kim, Marten Lohstroh, Hokeun Kim**
<div style="text-align: justify">
<b>Abstract</b> State-of-the-art industrial IoT solutions struggle to handle applications in which timing is important and deterministic event ordering is crucial. We illustrate this on the basis of a simple parking lot
occupancy sensing use case that is easy to explain but virtually
impossible to implement using commercially available IoT infrastructure. In this paper, we compare an implementation using AWS
IoT Core against one using Lingua Franca, a time-centric coordination language for constructing deterministic concurrent and
distributed reactive software. Our preliminary evaluation shows
that Lingua Franca can reliably address our use case.
</div>

#### PASoC: A Predictable Accelerator-rich SoC
**Susmita Tadepalli, Zhuanhao Wu, Hiren Patel**
<div style="text-align: justify">
<b>Abstract</b> We propose a predictable accelerator-rich system-on-chip (PASoC)
for safety-critical systems. The PASoC allows the integration of
multiple coherent agents to interact with each other over a shared
memory bus. These agents can be a cluster of cache-coherent homogeneous cores, and fully or one-way coherent hardware accelerators.
PASoC supports predictable cache coherence within the cluster of
cores, and across agents. The former uses linear cache coherence,
and the latter uses a modified version of predictable MSI. We analyze the per-request worst-case latency a memory request from
any of the agents can experience in the PASoC. Finally, we present
some observations based on our analysis that can help in future
designs of PASoCs.
</div>

#### InterPRET: a Time-predictable Multicore Processor
**Erling R. Jellum, Shaokai Lin, Peter Donovan, Chadlia Jerad, Edward Wang, Marten Lohstroh, Edward A. Lee, Martin Schoeberl**
<div style="text-align: justify">
<b>Abstract</b> With the end of Moore’s law and the breakdown of Dennard scaling, multicore processors are the standard way to continue improving performance while reducing Size, Weight and Power (SWaP).
However, this performance is typically achieved at the cost of repeatability and predictability. Precision-timed (PRET) architectures
have been shown to deliver high performance without sacrificing
predictability. In this paper, we introduce a multicore version of
such a PRET machine: InterPRET. The InterPRET consists of FlexPRET cores interconnected by S4NOC. Both the processor cores and
the network-on-chip are time-predictable, yielding an end-to-end
time-predictable architecture suitable for real-time systems.
</div>
