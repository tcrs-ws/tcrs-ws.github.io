---
layout: about
title: Program
permalink: /program/
---

# {{ page.title }}

TCRS '26 will be organized as a two-day workshop and take place during ESWEEK on October 8 and 9, 2026, at [Hotel Barceló Sants](https://maps.app.goo.gl/FtsJiQLvQgcJcyMaA) in Barcelona, Spain.
Please visit [ESWEEK's webpage](https://esweek.org/travel-and-venue/) for more information about the TCRS workshop venue.
Details about the program and location are shown below.

### Dates: October 8 and 9, 2026 (Two-day Workshop)<br> Location: Hotel Barceló Sants

## Opening Remarks and Keynote
### Thursday, October 8, 9:00-10:30
#### Opening Remarks: [Hokeun Kim](https://hokeun.github.io/)

#### Keynote: "Is Time-Critical the Same as Safety-Critical? Rethinking the Distinction in an Era of AI and Increasing System Complexity" By Prof. [Samarjit Chakraborty](https://www.cs.unc.edu/%7Esamarjit/)
![Samarjit Chakraborty]({{ site.baseurl }}/assets/images/samarjit_chakraborty.jpg){: style="float: left; margin-top: 1em; margin-right: 1.8em; margin-bottom: .8em"}
<div style="text-align: justify">
<b>Prof. Samarjit Chakraborty</b> is Kenan Distinguished Professor of Computer Science and an adjunct professor of Mathematics at the University of North Carolina at Chapel Hill.
Before joining UNC, he was Professor of Electrical Engineering at the Technical University of Munich, where he held the Chair of Real-Time Computer Systems, and earlier served on the faculty of the National University of Singapore.
He received his PhD from ETH Zurich.
His research spans embedded and cyber-physical systems, sustainable computing, and sensor-networked information processing.
His work has received several best paper awards and other recognitions.
He is an IEEE Fellow, an ACM Distinguished Speaker, a Fellow of the TUM Institute of Advanced Study, and is currently the elected chair of ACM SIGBED, the ACM’s Special Interest Group on Embedded Systems.

</div>
<br/>
<div style="text-align: justify">
<b>Abstract</b>-TBA
</div>

## Session 1: Languages, Compilation, and Runtime Foundations
### Thursday, October 8, 11:00-12:20
#### Session Chair: [Hoeseok Yang](https://hyang1999.github.io/)
#### 1.1 Rosetta: Compiling SysML v2 Behavior into Lingua Franca Modal Reactors
***Sebastiano Gaiardelli, Mario Libro, Pietro Turco, Enrico Fraccaroli, Michele Lora, Samarjit Chakraborty, Franco Fummi***

Systems Modeling Language (SysML) v2 standardizes the modeling of complex, reactive, time-dependent systems, but its Kernel Modeling Language (KerML) foundation gives behavior a declarative semantics: it characterizes which executions are valid without prescribing how a model is run. There is consequently no standard path from a SysML v2 behavioral model to deterministic, deployable reactive software, and today that gap is closed by hand. We present Rosetta, a compiler that translates the state-based and structural fragments of SysML v2 into Lingua Franca (LF), a deterministic coordination language whose programs are networks of reactors that communicate over ports in logical time. Unlike simulation-oriented targets, where determinism rests on coding discipline, LF fixes a single deterministic execution, and its modal reactors give the mapping a native state-machine abstraction. The translation maps state machines and part hierarchies construct-by-construct onto LF modal reactors. The constructs without a direct counterpart—state hierarchy, parallel regions with completion joins, timed triggers, cross-level priority, and deep exits—drive the encoding. We evaluate Rosetta on ten models, each equipped with in-model checks to ensure the generated program compiles and runs end-to-end. The programs reproduce their timed traces deterministically and are 1.4–3.3× the size of their SysML sources, an expansion Rosetta synthesizes rather than the engineer.

#### 1.2 Macros as Abstractions: Simplifying Code Generation for Lingua Franca
***Tassilo Tanneberger, Erling R. Jellum, Jeronimo Castrillon, Edward A. Lee***

Current Cyber-Physical Systems (CPS) are fundamentally reactive, and current programming methods suffer from compatibility and concurrency bugs due to manual software integration. Although Lingua Franca’s (LF) reactor model ensures deterministic execution, making CPS applications safer and more reliable, existing runtimes such as reactor-c struggle to support resource-constrained embedded devices. This paper presents reactor-uc’s code generator and macro interface, a lightweight runtime that uses object-oriented C patterns and a macro-based interface to eliminate dynamic memory allocation and simplify code generation. Evaluation results show that reactor-uc produces code that is one-third the size and has half the cyclomatic complexity of reactor-c, as well as smaller binaries, while maintaining comparable performance on benchmarks.

#### 1.3 Lingua Franca on the Patmos Processor
***Ehsan Khodadad, Luca Pezzarossa, Martin Schoeberl***

Reliability, dependability, and time-predictability are fundamental requirements for hard real-time embedded systems, particularly those used in safety-critical applications. However, the current design paradigm lacks a comprehensive approach to addressing these challenges across both hardware and software. This paper proposes integrating the time-predictable multicore architecture for embedded systems (T-CREST) with Lingua Franca (LF), a deterministic polyglot language and framework. We integrate LF with Patmos by adding support for the Patmos processor, the T-CREST platform’s processing unit, as LF’s hardware platform, and by automating regression tests with GitHub Actions to ensure the proposed method continues to function correctly. We evaluated the proposed method using an autonomous ski lift application as a safety-critical example.

#### 1.4 Decentralized Coordination in LF: Timing Correctness and Transient Federate Support
***Chadlia Jerad, Edward A. Lee***

Distributed cyber-physical systems increasingly demand peer-to-peer operation to avoid single-point-of-failure bottlenecks in centralized coordination. However, extending deterministic semantics to decentralized systems where federates dynamically join and leave remains open. This paper extends our prior work on transient federates in Lingua Franca (LF) to decentralized coordination, which eliminates the central Run-Time Infrastructure (RTI) as the time arbiter. We analyze the interactions between timing constructs in decentralized LF federations, characterize the conditions under which a transient federate may safely join a running federation and validate both experimentally. A key finding is that the join protocol shifts most coordination work from the RTI to the joining federate itself.

## Session 2: Resilience, Reliability, and Security
### Thursday, October 8, 13:30-15:10
#### Session Chair: [Sebastiano Gaiardelli](https://sbgaia.github.io/)
#### 2.1 Controlled Degradation, Not Dispatch Reordering: Semantics-Preserving Overload Control in Lingua Franca
***Yutaka Matsubara, Wenhung Kevin Huang, Akihito Iwai***

Logical-time reactive languages such as Lingua Franca (LF) make timing part of the programming model, but overload handling is usually left to implementation-level
scheduling. This letter formulates controlled degradation, which sheds application-declared degradable reactions while preserving LF determinism, and asks a focused question: when high-criticality (HC) and low-criticality (LC) reactions are released at the same logical-time tag, can the runtime shed optional LC work, without violating LF semantics, to protect HC timing and bound overload propagation across tags? We give the mechanism as a pressure-driven, per-tag LC budget enforced at the ready-set boundary with semantic guards and safe fallback, argue that shedding a degradable reaction is observationally equivalent to its non-triggering, and show that, once retained per-tag work exceeds capacity, no work-conserving dispatch order can prevent HC misses; only shedding can. On a multi-worker LF/C runtime on a PREEMPT_RT Raspberry Pi at a natural 2 ms period, degradation keeps HC within its deadline (HC-miss falls from 100% to ≈ 0% at the overload onset), bounds the longest run of overrun tags to at most tens (vs. the full trace), and exposes a tunable LC/timeliness trade-off, with LF determinism preserved by construction; the benefit depends on worker parallelism, which we characterize. 

#### 2.2 Reactor-Based Modeling of Safe Interrupt-Driven Communication for Distributed Embedded Systems
***Tejeswini Jayaramareddy, Hokeun Kim, Hoeseok Yang***

Interrupt-driven communication is widely used in embedded systems to transfer data from hardware peripherals to software through finite-capacity receive FIFOs. Selecting the FIFO interrupt threshold requires balancing processor overhead against communication reliability under varying interrupt latency, yet existing approaches rely primarily on empirical tuning and vendor guidelines without analytical guarantees. This paper presents a reactor-based framework for modeling and analyzing interrupt-driven communication, enabling systematic determination of safe interrupt thresholds and runtime adaptation to changing execution conditions. The proposed methodology is evaluated using a Lingua Franca implementation of a GNSS correction-data pipeline as a representative case study. Experimental results validate the proposed framework, accurately predict FIFO overflow boundaries, and demonstrate robust communication across varying interrupt-latency conditions.

#### 2.3 Deadline-Bounded Re-execution for Soft-Error Resilience using Reactor Models and Lingua Franca
***Hwisoo So, Hokeun Kim***
#### 2.4 RACE-MiCS: Reliability-Aware Checkpointing and Execution-Time Bounding for Embedded Mixed-Criticality Systems
***Mohammad Abbasinia, Behnaz Ranjbar, Akash Kumar***

Mixed-Criticality (MC) systems execute tasks with different criticality levels on a shared platform, using mode-dependent Worst-Case Execution-Time (WCET) estimates. A key design challenge is selecting the LO-mode WCET of High-Criticality (HC) tasks: tighter bounds improve LO-mode utilization but increase mode-switch probability, while conservative bounds reduce mode switches but increase processor demand and transient-fault exposure. This trade-off becomes more critical when reliability requirements must be satisfied through fault-tolerance mechanisms such as checkpointing. This paper proposes RACE-MiCS, a reliability-aware design-time method that jointly selects WCETLO values and checkpoint allocations. The method evaluates candidate LO-mode bounds, estimates system mode-switch probability, computes system reliability, and enforces both the Probability-of-Failure-per-Hour (PFH) target and EDF-VD schedulability as hard constraints. Among feasible designs, RACE-MiCS minimizes checkpoint overhead, checkpoint count, and mode-switch probability. Experimental results on synthetic MC task sets show that RACE-MiCS satisfies the PFH target according to the industrial safety standard, keeps the mode-switch probability below 0.20, while preserving schedulability.

#### 2.5 RISC-V Microarchitectural Attacks: No Timer, No Problem?
***Mahreen Khan, Gaëtan Bois-Baumann, Maria Mushtaq, Renaud Pacalet, Ludovic Apvrille***

RISC-V processors are increasingly being deployed in cyber-physical, time-sensitive embedded, and reactive systems, making microarchitectural timing side-channel attacks a practical security concern. A commonly proposed countermeasure is to disable access to the high-resolution rdcycle timer under the assumption that practical attacks require precise timing measurements. However, this approach is unsuitable for systems that rely on precise timing for scheduling and deadline enforcement, and it does not remove the underlying secret-dependent microarchitectural state. We demonstrate the limitations of this countermeasure by evaluating four cache and transient-execution attacks, namely Flush+Reload, Flush+Flush, Flush+Fault, and Spectre V1, on a commercial out-of-order RISC-V core, the T-Head C910. We replace rdcycle with three alternative timing sources: a software counter thread, clock gettime, and perf event open. Under background CPU loads ranging from 25% to 100%, with 50 repetitions per configuration, the alternative timing sources achieve up to a 93% average attack success rate across the evaluated settings, showing that the attacks remain effective even under substantial system noise. We further demonstrate complete 128-bit AES key recovery, clear timing separation between page-table-walk and no-walk executions, and a cross-core covert channel that transmits 1,024 bits with zero errors in 49 out of 50 independent runs. We also evaluate index masking and speculation-fence insertion for Spectre V1 and examine L1 instruction-cache and L1 data-cache miss rates as indicators for profiling-based attack detection. These results show that restricting rdcycle alone is insufficient and that effective protection requires layered hardware and software countermeasures.

## Session 3: Distributed Timing and Communication
### Thursday, October 8, 15:30-16:50
#### Session Chair: [Hokeun Kim](https://hokeun.github.io/)
#### 3.1 Replacing Quorums with Time for Fault-Tolerant Distributed Systems
***Edward A. Lee, Shulu Li***

Distributed systems often achieve fault tolerance by waiting for a quorum of replicas to agree before committing a non-commutative operation. This paper argues for a timing-based approach, where a fault is defined as a timing violation rather than a node failure. We use the resettable counter of Zhao and Haller as a running example: a system in which a shared vector counter forms a CRDT, but an occasional reset is not commutative and requires consensus. We present two implementations in the Lingua Franca coordination language. The first reaches consensus by counting acknowledgments. Requiring unanimity results in deadlock when a node fails; a majority quorum restores progress but admits inconsistencies that a node cannot detect on its own and that may persist. The second schedules a reset at a fixed logical time in the future using the maxwait mechanism, processing events in timestamp order around that point. This second approach is more deterministic, bounds the time to respond to a reset, defines failure precisely as a timing violation, and excludes slow or failed nodes from the consensus while allowing them to detect their own failure and recover.

#### 3.2 Budget-Conditioned BLE Communication for Federated Reactors
***Sebastiano Gaiardelli, Philipp H. Kindt, Samarjit Chakraborty***

Lingua Franca (LF) is a coordination language for building deterministic concurrent software using components called reactors, whose behavior is defined by a set of event-driven reactions. Federated reactors carry this determinism across distributed nodes and are therefore called federates. A federation keeps its deterministic timing as long as the links interconnecting the federates obey a maximum latency, called maxwait, specified at design time. LF’s runtime for microcontroller-class devices already carries federations over wired links and over IP, but not over a low-power radio, whose probabilistic behavior makes the selection of maxwait non-trivial. Mobile IoT nodes, wearables and small sensors are therefore hard to integrate. We close this gap by adopting a connection-oriented Bluetooth Low Energy (BLE) link, which is itself a time-triggered protocol: it supports a configurable, periodic transmit schedule and retransmits lost packets. Therefore, when accepting a certain number of retransmissions, its latency behavior is essentially deterministic in a controlled wireless environment. We derive a closed-form latency LBLE, accounting for the worst-case number of retransmissions needed to achieve it with a given target reliability, and establish a method to automatically synthesize BLE configurations that satisfy a specified maxwait. We finally evaluate such links and present an implementation in LF’s Reactor-UC.

#### 3.3 Remote Train Control over WebTransport Orchestrated by Lingua Franca
***Rajib Chandra Das, Alexander Schulz-Rosengarten, Reinhard von Hanxleden***

Modern railway systems are moving toward higher Grades of Automation (GoA), yet remote control remains a critical fallback for GoA-3 and GoA-4 operations. Real-time transmission of sensor data and control commands is essential for remotely driven vehicles, where latency is influenced by factors such as hardware capabilities, network conditions, transmission protocols, system architecture, and software frameworks. This paper presents a case study on the design, implementation, and evaluation of a remote control system for train operations built on two modern technologies: WebTransport and Lingua Franca. WebTransport provides low-latency, bidirectional streaming over the QUIC protocol, enabling robust and concurrent transmission channels between the remote operator and the train while preserving message integrity and ordering. Lingua Franca, a polyglot coordination language, governs the reactive behavior of cyber-physical systems, ensuring deterministic and time-aware execution. Our experiments demonstrate that this combination constitutes a promising foundation for remote control systems in low-latency and real-time train operations.

#### 3.4 ECAL: An Event-Level Timing Model for Distributed Cyber-Physical Systems
***Guangyu Feng, Edward A. Lee***

## Session 4: AI-Enabled Time-Sensitive Systems
### Friday, October 9, 9:00-10:20
#### Session Chair: [Edward A. Lee](https://ptolemy.berkeley.edu/~eal/)
#### 4.1 Timing Behavior Analysis for Time-Sensitive Distributed Human- and Agent-in-the-Loop Cyber-Physical Systems
***Deeksha Prahlad, Dongha Kim, Pawan Kumar, Daniel Fan, Hokeun Kim***

Distributed human- and agent-in-the-loop cyber-physical systems (H/AITL CPS) introduce timing variability from AI reasoning, human interaction, sensing, communication, and actuation. This paper presents a Lingua Franca (LF)/reactor MoC-based approach for characterizing latency sources and detecting timing-assumption violations in H/AITL CPS. We design an agentic driving coach prototype in which an AI agent monitors the driver and environment state, generates spoken instructions, and interacts with a human driver through a distributed CPS platform. Using LF timing constructs such as maxwait, logical delays, timers, and startup offsets, we configure and evaluate timing behavior under nominal execution, injected network delay, GPU contention, and tighter timing assumptions. The results show that LF exposes timing violations through tardy-handler invocations when runtime conditions exceed configured bounds.

#### 4.2 Runtime Monitoring of Observation-Delay Tolerant RL Policies Using Lingua Franca
***Balkis Oueslati, Chadlia Jerad***

Reinforcement Learning (RL) policies trained to handle observation delay are typically evaluated only within the delay range used in training. At deployment, the real delay can exceed that range, and the policy has no mechanism to detect this. We address this gap using Lingua Franca (LF), a language for reactive systems with deterministic timing semantics, and illustrate it on HalfCheetah-v5. First, we shape the reward and train the learner to tolerate a training delay envelope using DIDA (Delayed Imitation with Dataset Aggregation) against its expert under stochastic delays. Second, we build an algorithm- and task-agnostic runtime monitor that wraps the learner policy to safeguard it against delays exceeding this training delay envelope: LF’s decentralized execution constructs let us express this out-of-envelope detection and fallback in a simple, natural way, directly around the policy. We argue that this setup is a mid-sim-to-real testbed: training and deployment share the same timing semantics. Together, this turns a statistical robustness claim into a runtime guarantee that out-of-envelope delay is detected and handled within a bounded time, using only the training delay envelope and control period. Code and models are publicly available.

#### 4.3 Phase-Aware Memory Repartitioning for Extended-Context Edge LLM Inference
***Youngchul Yoon, Soonhoi Ha***

As AI agents increasingly run on embedded and edge devices, supporting long-context LLM inference under limited memory budgets becomes a key challenge. Model weights and KV cache compete for memory, creating phase-dependent pressure: long prompts may exceed prefill capacity, while accumulated interaction history may exhaust decode-time context capacity. We propose Arena-Repartition, a phase-aware runtime memory management technique that improves long-context capability under a fixed memory budget. Arena-Repartition unifies KV cache and compute buffers into a single runtime-managed arena and dynamically repartitions memory between prefill and decode phases according to their distinct demands. We implement Arena-Repartition in llama.cpp and evaluate it on an NVIDIA Jetson Orin Nano Super with 8 GB of memory using quantized Llama-3.2-3B, Qwen2.5-3B, and Phi-3.5-mini models. Arena-Repartition expands effective prefill capacity by 31%–313% with 5%–11% prefill-throughput overhead and expands decode-time KV cache capacity by 29%–229% with negligible time-to-first-token overhead. These results show that exposing the temporal structure of LLM inference to the runtime can improve long-context capability on memory-constrained embedded systems.

#### 4.4 Time-constrained Vision Language Model Inference using Semantic Caching for Autonomous Driving
***Chanhee Lee, Manuel Branco Nardi***

## Session 5: CPS Observability and Resource Management
### Friday, October 9, 11:00-12:20
#### Session Chair: [Chadlia Jerad](https://chadliajerad.github.io/)
#### 5.1 Determinism and Reproducibility in Resource-Constrained Cyber-Physical System Simulation Using Operational Data
***Pawan Kumar, Aditya A. Krishnan, Hokeun Kim***

Deterministic simulation of robotic cyber-physical systems (CPS) remains challenging when operational data are collected from resource-constrained hardware platforms. This paper presents a reactor model-based workflow for deterministic and reproducible operational-data-driven CPS simulation. Our proposed workflow provides reusable components for collecting structured logs of multimodal sensor readings, controller state, actuator commands, and timing information, followed by logical time-based replay to reconstruct the logged execution with deterministic event ordering. The proposed workflow targets low-cost sensing modalities, including motor encoders, line sensors, bump sensors, IMUs, and ToF sensors. We evaluate our approach using four case studies on ground and aerial robots, covering track following, maze exploration, and obstacle avoidance. The evaluation results show that structured operational data from low-cost sensors can support repeatable CPS simulation without relying on costly camera- or LiDAR-based perception.

#### 5.2 A Non-Intrusive Data Age Tracer for Real-Time ROS2 Applications
***Yundo Choi, Taekyeong Lee, Hyeong Rae Cho, Kyong Hoon Kim***

In ROS 2-based autonomous systems, the temporal consistency of a downstream output depends not only on local callback latency but also on the staleness of the upstream source data—a metric known as data age. Computing data age requires causal link information that the structural node–topic graph of ROS 2 does not provide. This paper presents a Data Age tracer that reconstructs causal link relations and computes direct and indirect data age from standard ros2_tracing LTTng traces without modifying application code. A case study on the Autoware Reference System shows that executor parallelism reduces local-hop direct data age and typical end-to-end indirect data age, while the high-percentile tail remains largely unchanged and freshness misses concentrate on specific causal paths.

#### 5.3 Tail Service Delay Mitigation for On-Demand Execution Module Streaming in Cloud-Edge Systems
***Janghun Lee, Daejin Park***

In cloud-edge environments, an edge device requests execution modules needed during service execution from the cloud. The requested modules are transmitted in chunks, and the edge prepares them into an executable state through reception, processing, and storage. If an execution module is not ready by the time it is required, service execution must wait; this paper defines such delay as service delay. When multiple execution module requests overlap in time, the service delay of a particular module may increase excessively depending on the chunk scheduling policy, which may delay execution of the function that requires the module. In particular, when precedence relationships exist among execution modules, a module with large service delay can become a critical path in execution flows and cause delay propagation. Therefore, mitigating tail service delay is important. To address this problem, this paper proposes an edge-driven laxity-based execution module chunk scheduling method. The proposed method computes laxity by jointly considering the time remaining until each module is required and the remaining time needed for the module to become ready, and adjusts weights so that chunks of modules with smaller laxity are transmitted more frequently. Experimental results show that the proposed method achieves lower tail service delay than the baseline policies and tends to reduce the spread of per-module service delay. This indicates that the proposed method mitigates tail service delay by redistributing scheduling opportunities and suppressing excessive delay in specific modules.

#### 5.4 VEDRA: Verified and Efficient Dynamic Resource Allocation for Real-Time Radio Access Network Scheduling
***Debarpita Banerjee, Sumana Ghosh, Snigdha Das, Shilpa Budhkar, Rana Pratap Sircar***

Large-scale cyber-physical systems (CPSs), like industrial IoT and autonomous vehicles, rely on high-speed radio access networks (RANs) for huge sensor deployments and remote control. As complex CPSs involve multi-priority diverse RAN services, efficiently allocating radio resources (physical resource blocks or PRBs) to them is critical. The core challenge lies in jointly achieving—efficiency: meeting strict real-time deadlines to cope with runtime service demands, and dependability: providing fair allocation and prudent unused spectrum management—all while running on resource-constrained embedded edge platforms. To address this, we propose VEDRA, an efficient, dependable, dynamic PRB allocation strategy. Our two-phase solution provides: i) a polynomial-time algorithm for efficient, runtime PRB allocation within strict deadlines, and ii) pre-processing formal verification to guarantee dependability before runtime deployment. Our results highlight the efficiency and improved performance of VEDRA.
