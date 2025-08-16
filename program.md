---
layout: about
title: Program
permalink: /program/
---

# {{ page.title }}

TCRS '25 will take place during ESWEEK on October 2, 2025, in Room 101C at the Taipei International Convention Center (TICC) in Taipei, Taiwan.
Please visit [ESWEEK's webpage](https://esweek.org/hotels/) for more information about the TCRS workshop venue.
The detailed program, including keynotes and technical sessions, will be announced during the summer.

### Date: October 2, 2025 <br> Location: Room 101C, Taipei International Convention Center (TICC)

## Keynote
### 9:00-10:30
#### Time Sensitive Requirement and Applications for Connected Vehicles
![Chi-Sheng Shih]({{ site.baseurl }}/assets/images/chi-sheng_shih.jpg){: style="float: left; margin-top: 1em; margin-right: 1.8em; margin-bottom: .8em"}
<div style="text-align: justify">
<b>Chi-Sheng Shih</b> is a professor at the Graduate Institute of Networking and Multimedia and the Department of Computer Science and Information Engineering, National Taiwan University. His research interests include real-time process scheduling, requirement assignment and determination, resource allocation, cyber-physical systems, streaming computation, and autonomous system integration. Between 2019 and 2022, he served as the Director of Graduate Institute of Networking and Multimedia, National Taiwan University. Between 2022 and 2024, he served as the Associate Dean of the College of Electrical Engineering and Computer Science and was responsible for international affairs. He also actively participated in the activities of the Autoware Foundation, including the chair of the reference design WG, and the contributor of the Low Speed Autonomy Vehicles WG and ODD WG.
</div>
<br/>
<div style="text-align: justify">
<b>Abstract</b>-TBA
</div>

## Session 1: Real-Time Coordination for Connected and Intelligent Vehicles
### 11:00-12:30
#### Session Chair: Jeronimo Castrillon
#### Value-Aware Real-Time Scheduling for Intelligent Transportation Systems
***Hoeseok Yang, Hokeun Kim, Choonghwan Lee, Hyung-Chan An***
<div style="text-align: justify">
<b>Abstract</b>-This paper presents a novel real-time scheduling technique tailored for sporadic task graphs in multi-processor systems, motivated by the computational demands of intelligent transportation systems (ITS). Unlike traditional deadline-based approaches, the proposed method prioritizes tasks based on their anticipated contribution to system utility, expressed as a value, under runtime uncertainty. Each request is associated with a reputation score, with progressively refined value estimations revealed through sequential task executions. A feasibility-aware value density metric is introduced to dynamically schedule tasks while respecting global deadlines and the non-preemptive nature of execution. Extensive simulations, conducted with 1, 2, and 4 processors, evaluate performance under varying traffic conditions and workload intensities. The results confirm that the proposed method significantly improves the total earned value, particularly under high-load scenarios or limited processing resources.
</div>

#### Software-Defined Vehicles: Challenges and Orchestrating Mixed-Criticality Services Using Lingua Franca
***Wenhung Kevin Huang, Yoshinori Terazawa, Yutaka Matsubara, Akihito Iwai***
<div style="text-align: justify">
<b>Abstract</b>-Software-Defined Vehicles (SDVs) consolidate safety-and non-safety-critical functions onto centralized platforms, forming mixed-criticality systems (MCSes) where applications like ADAS and infotainment coexist. While this reduces cost and complexity, it also introduces challenges in isolation, timing determinism, and safety certification. Lingua Franca (LF) offers deterministic coordination but lacks mechanisms for per-application monitoring and recovery. To address this, we (1) derive orchestration requirements from the “Safety First for Automated Driving” white paper, and (2) propose an LF-compatible framework with external monitors that detect faults and enable selective restarts of faulty applications without disrupting others. This work presents the first practical per-application failover solution for LF, improving the reliability of SDV mixed-criticality orchestration.
</div>

#### Compatibility Analysis and Smooth Transition of Heterogeneous Controllers in Longitudinal Merging Platoons
***Pintusorn Suttiponpisarn, Chung-Wei Lin***
<div style="text-align: justify">
<b>Abstract</b>-Vehicle platoon merging presents significant challenges due to varying speeds, gap estimation errors, and synchronization issues. Heterogeneous controllers, in particular, can cause mismatches in control dynamics, resulting in inconsistent acceleration responses, unstable gap spacing, and unpredictable behaviors that negatively impact user comfort and safety. This work investigates the merging performance of 25 controller combinations, pairing five controllers and testing them across three merging scenarios, with a focus on both user comfort and safety gaps. We identify key trade-offs: mismatches between reactive and predictive controllers often lead to higher jerk, and some joining controllers experience elevated jerk during merging with braking disturbances, resulting in poor comfort. To address these issues, we propose an adaptive transitory controller—a simple assistance module for the joining platoon leader—that enhances compatibility with various preceding controllers and merging scenarios. Results show consistent performance and a 58.38% improvement in user comfort while maintaining gap safety. We also discuss the limitations of our approach and propose directions for future work to further improve robustness.
</div>

## Session 2: System and Architecture Design for Time-Sesntive Software
### 13:30-15:00
#### Session Chair: Chung-Wei Lin
#### Deterministic Modeling and Simulation of Fault-Tolerant Real-Time Software
***Dongha Kim, Hokeun Kim***
<div style="text-align: justify">
<b>Abstract</b>-Time redundancy, a fault tolerance mechanism without extra hardware, negatively affects response times while improving fault tolerance. Although real-time scheduling in fault-tolerant systems is a well-studied area, there has not been a deterministic model supporting realistic simulation. To address this gap, we propose deterministic execution models of fault-tolerant real-time software, with a simulation of user software. Our evaluation shows that the proposed execution models deterministically avoid deadline misses of real-time software under failures. Our case study using ROSACE flight control software demonstrates our simulation method with user software.
</div>

#### ForSyDe on the Patmos Processor
***Ehsan Khodadad, Ingo Sander, Luca Pezzarossa, Martin Schoeberl***
<div style="text-align: justify">
<b>Abstract</b>-Due to strict timing requirements, designing embedded real-time systems for safety-critical applications is inherently complex. The design paradigm should not only be able to guarantee that the final system works but also fulfill the safety-critical specifications and requirements. This paper proposes a design approach for embedded systems using T-CREST, a time-predictable hardware platform, and ForSyDe, a modeling framework supporting the formal design of embedded systems. We designed different use cases, performed preliminary experiments, and demonstrated the possibility of using this method. Furthermore, we perform worst-case execution time (WCET) analysis of our example applications.
</div>

#### LLVM-Based Hybrid Cache and TCM Memory Allocation Optimization for Low-Latency, Energy-Efficient Execution
***Gihyeon Jeon, Daejin Park***
<div style="text-align: justify">
<b>Abstract</b>-Cache memory has been introduced to accelerate embedded system performance and is automatically managed without programmer intervention through hardware-based cache controllers. However, this implies that cache behavior may differ from programmer intentions and cannot guarantee deterministic execution. In contrast, Scratchpad Memory (SPM) or Tightly Coupled Memory (TCM), which are closely coupled with the processor core, require direct programmer control over data placement or compiler optimization support. Nevertheless, this control enables deterministic execution as intended by the programmer. While various memory system optimization studies have been conducted, research that enhances applicability by utilizing LLVM passes for LLVM compiler optimization development or preserving existing build systems has been limited. This paper proposes an LLVM pass-based profiling technique and applies its results to a fractional knapsack algorithm to identify high-value data for placement in Data TCM RAM (DTCM RAM), presenting a hybrid memory architecture where cache and TCM coexist. Particularly, the approach enhances practicality by enabling optimization application without modifying existing build systems used in current development processes. Experiments were conducted using the dijkstra and adpcm algorithms from MiBench. The dijkstra algorithm demonstrated up to 5.12% reduction in clock cycles and 3.93% reduction in energy consumption compared to using cache alone, while the adpcm algorithm showed up to 7.6% reduction in both clock cycles and energy consumption compared to cache-only usage. These results indicate that the proposed method achieves higher performance and lower energy consumption compared to using cache memory exclusively.
</div>

## Session 3: Towards Timely and Safe Neural Networks
### 15:30-16:30
#### Session Chair: Hoeseok Yang
#### Combining Early Exit and Selective Prediction for Convolutional Neural Networks
***Hasna Bouraoui, Chadlia Jerad, Jeronimo Castrillon***
<div style="text-align: justify">
<b>Abstract</b>-The deployment of CNN in real-time and resource-constrained applications poses critical challenges due to their computational demands and the need for reliable decision making. In this paper, we combine adaptive inference via Early Exits (EE) with Selective Prediction (SP) to address these challenges. Early exits allow confident predictions at intermediate layers, while selective prediction introduces uncertainty estimation modules, enabling the system to abstain from low-confidence decisions or continue inference through deeper layers. This combined design lowers the risk of overconfident but erroneous predictions and improves the trade-off between performance and accuracy. As a case study, we implement and evaluate our approach on a real-time traffic sign detection task, processing the input of an RGB camera in the forward direction. In this paper, we demonstrate improved performance compared to baseline models. Compared to SP-only (Selective Prediction) and EE-only (Early Exit) baselines, our hybrid model achieves low inference depth (1.20), leading to reduced computational demand and latency. Despite this efficiency, the model maintains a high prediction accuracy (90.3%) and a low abstention rate (1.6%), ensuring fast and reliable decision making suitable for time-critical embedded applications. This demonstrates an effective trade-off between effective computation and predictive reliability.
</div>

#### Safety-Driven DNN Sizing for Vehicular CPS
***Tingan Zhu, Mier Li, Bineet Ghosh, Samarjit Chakraborty, Parasara Sridhar Duggirala***
<div style="text-align: justify">
<b>Abstract</b>-Perception processing in cyber-physical systems (CPS) is now almost exclusively done using Deep Neural Networks (DNNs). Here, camera, radar and LiDAR data – in autonomous vehicles or robots – is fed into DNNs that detect surrounding obstacles and distances to them. These results are used by controllers to compute appropriate actuation signals. But a CPS typically has multiple state components, where each of them might be estimated using a different camera, radar or lidar and an associated DNN. Hence, an emerging problem is to implement multiple DNNs on a resource-constrained graphics processing unit (GPU). While many GPUs from NVIDIA and AMD allow them to be split into multiple virtual GPUs, there is little work on how to partition them, and therefore size the corresponding DNNs, when they are a part of the same CPS. In contrast to the existing practice of focusing on the inference accuracy of individual DNNs in isolation, we propose a system-level safety-driven DNN sizing (and hence GPU partitioning) scheme for vehicular CPS. Our main technical contribution is a detailed experimental evaluation of this DNN sizing approach and an empirical validation of the formal technique behind it.
</div>
