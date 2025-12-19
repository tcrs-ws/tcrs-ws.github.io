---
layout: about
title: Program
permalink: /program/
---

# {{ page.title }}

TCRS '25 will take place during ESWEEK on October 2, 2025, in Room 101C at the Taipei International Convention Center (TICC) in Taipei, Taiwan.
Please visit [ESWEEK's webpage](https://esweek.org/hotels/) for more information about the TCRS workshop venue.
Details about the program and location are shown below.

### Date: October 2, 2025 <br> Location: Room 101C, Taipei International Convention Center (TICC)

## Opening Remarks and Keynote
### 9:00-10:30
#### Opening Remarks: Hokeun Kim

#### Keynote: Time Sensitive Requirement and Applications for Connected Software-Defined Vehicles
![Chi-Sheng Shih]({{ site.baseurl }}/assets/images/chi-sheng_shih.jpg){: style="float: left; margin-top: 1em; margin-right: 1.8em; margin-bottom: .8em"}
<div style="text-align: justify">
<b>Dr. Chi-Sheng Shih</b> is currently a professor at the Graduate Institute of Networking and Multimedia and the Department of Computer Science and Information Engineering at National Taiwan University. He also serves as the Director of the Center of Artificial Intelligence and Advanced Robots at National Taiwan University. His main research interests include embedded systems, real-time systems, cyber-physical systems, and autonomous systems.  Specifically, his researches aim on the collaborative perception and real-time V2X. He also serves as the Chair/Co-Chairs in several working groups for software design on autonomous vehicles, including Autoware Foundation and MIH (Mobility In Harmony), to lead the collaboration and standards for autonomous software-defined vehicles in open-source communities. His research results won several awards, including the 2023 Best Paper Runner-Up Award of the 2023 ACM Research in Adaptive and Convergent Systems (RACS 2023), the 2022 Future Tech Award - AIAugSurgery, The 2022 1st Andes Awards of RISC-V Creative Competition, the 2019 National Innovation Awar, The Best Paper Award, 2019 MobiSec/Future ICT, the Best Paper Award in 2016 IEEE International Symposium on Cloud and Service Computing, 2011 ACM Research in Applied Computation Symposium (RACS 2011), IEEE RTCSA 2005, and IEEE RTSS 2004. He also serves as the Associate Editor of IET Cyber-Physical Systems: Theory and Applications and Springer Journal of Services-Oriented Computing and Applications (SOCA).

</div>
<br/>
<div style="text-align: justify">
<b>Abstract</b>-The design and capabilities of the vehicles have undergone revolutionary transformations in this decade, from energy, power train, automation, to autonomy. It is difficult, if not impossible, to foresee when such transformation will slow down or stop. Among these transformations, software-defined vehicles (SDVs) employ the computation and communication to embody the intelligence to the vehicles and enable Level 4 and 5 automation. Timeliness requirements for vehicle perception and vehicle control impose unforeseen challenges to the communities. This talk will explore the real-time requirements of computation and communication for connected software-defined vehicles. The requirements include that among the zonals within a software-defined vehicle, and that among the connected vehicles. This talk will discuss the communication networks for modern vehicles and their limitations. We will also present the example workload for intra- and inter-vehicle messages on modern software-defined vehicles. The computation and communication workload in Autoware will be used as an example to elaborate. Collaborative perception serves as another example to integrate the communication and computation in order to embody intelligence to the connected vehicle.
</div>

## Session 1: Real-Time Coordination for Connected and Intelligent Vehicles
### 11:00-12:30
#### Session Chair: Jeronimo Castrillon
#### [Value-Aware Real-Time Scheduling for Intelligent Transportation Systems](https://ieeexplore.ieee.org/document/11121306)
***Hoeseok Yang, Hokeun Kim, Choonghwan Lee, Hyung-Chan An***
<div style="text-align: justify">
<b>Abstract</b>-This paper presents a novel real-time scheduling technique tailored for sporadic task graphs in multi-processor systems, motivated by the computational demands of intelligent transportation systems (ITS). Unlike traditional deadline-based approaches, the proposed method prioritizes tasks based on their anticipated contribution to system utility, expressed as a value, under runtime uncertainty. Each request is associated with a reputation score, with progressively refined value estimations revealed through sequential task executions. A feasibility-aware value density metric is introduced to dynamically schedule tasks while respecting global deadlines and the non-preemptive nature of execution. Extensive simulations, conducted with 1, 2, and 4 processors, evaluate performance under varying traffic conditions and workload intensities. The results confirm that the proposed method significantly improves the total earned value, particularly under high-load scenarios or limited processing resources.
</div>

#### [Software-Defined Vehicles: Challenges and Orchestrating Mixed-Criticality Services Using Lingua Franca](https://ieeexplore.ieee.org/abstract/document/11119543)
***Wenhung Kevin Huang, Yoshinori Terazawa, Yutaka Matsubara, Akihito Iwai***
<div style="text-align: justify">
<b>Abstract</b>-Software-Defined Vehicles (SDVs) consolidate safety-and non-safety-critical functions onto centralized platforms, forming mixed-criticality systems (MCSes) where applications like ADAS and infotainment coexist. While this reduces cost and complexity, it also introduces challenges in isolation, timing determinism, and safety certification. Lingua Franca (LF) offers deterministic coordination but lacks mechanisms for per-application monitoring and recovery. To address this, we (1) derive orchestration requirements from the “Safety First for Automated Driving” white paper, and (2) propose an LF-compatible framework with external monitors that detect faults and enable selective restarts of faulty applications without disrupting others. This work presents the first practical per-application failover solution for LF, improving the reliability of SDV mixed-criticality orchestration.
</div>

#### [Compatibility Analysis and Smooth Transition of Heterogeneous Controllers in Longitudinal Merging Platoons](https://ieeexplore.ieee.org/abstract/document/11107257)
***Pintusorn Suttiponpisarn, Chung-Wei Lin***
<div style="text-align: justify">
<b>Abstract</b>-Vehicle platoon merging presents significant challenges due to varying speeds, gap estimation errors, and synchronization issues. Heterogeneous controllers, in particular, can cause mismatches in control dynamics, resulting in inconsistent acceleration responses, unstable gap spacing, and unpredictable behaviors that negatively impact user comfort and safety. This work investigates the merging performance of 25 controller combinations, pairing five controllers and testing them across three merging scenarios, with a focus on both user comfort and safety gaps. We identify key trade-offs: mismatches between reactive and predictive controllers often lead to higher jerk, and some joining controllers experience elevated jerk during merging with braking disturbances, resulting in poor comfort. To address these issues, we propose an adaptive transitory controller—a simple assistance module for the joining platoon leader—that enhances compatibility with various preceding controllers and merging scenarios. Results show consistent performance and a 58.38% improvement in user comfort while maintaining gap safety. We also discuss the limitations of our approach and propose directions for future work to further improve robustness.
</div>

## Session 2: System and Architecture Design for Time-Sensitive Software
### 13:30-15:00
#### Session Chair: Chung-Wei Lin
#### [Deterministic Modeling and Simulation of Fault-Tolerant Real-Time Software](https://ieeexplore.ieee.org/document/11112709)
***Dongha Kim, Hokeun Kim***
<div style="text-align: justify">
<b>Abstract</b>-Time redundancy, a fault tolerance mechanism without extra hardware, negatively affects response times while improving fault tolerance. Although real-time scheduling in fault-tolerant systems is a well-studied area, there has not been a deterministic model supporting realistic simulation. To address this gap, we propose deterministic execution models of fault-tolerant real-time software, with a simulation of user software. Our evaluation shows that the proposed execution models deterministically avoid deadline misses of real-time software under failures. Our case study using ROSACE flight control software demonstrates our simulation method with user software.
</div>

#### [ForSyDe on the Patmos Processor](https://ieeexplore.ieee.org/document/11121303)
***Ehsan Khodadad, Ingo Sander, Luca Pezzarossa, Martin Schoeberl***
<div style="text-align: justify">
<b>Abstract</b>-Due to strict timing requirements, designing embedded real-time systems for safety-critical applications is inherently complex. The design paradigm should not only be able to guarantee that the final system works but also fulfill the safety-critical specifications and requirements. This paper proposes a design approach for embedded systems using T-CREST, a time-predictable hardware platform, and ForSyDe, a modeling framework supporting the formal design of embedded systems. We designed different use cases, performed preliminary experiments, and demonstrated the possibility of using this method. Furthermore, we perform worst-case execution time (WCET) analysis of our example applications.
</div>

#### [LLVM-Based Efficient Hybrid Cache and TCM Memory Allocation for Low-Latency](https://ieeexplore.ieee.org/document/11218194)
***Gihyeon Jeon, Daejin Park***
<div style="text-align: justify">
<b>Abstract</b>-Cache memory has been introduced to accelerate embedded system performance and is automatically managed without programmer intervention through hardware-based cache controllers. However, since it operates based on typical variable access patterns, opportunities for complementary approaches remain. In contrast, Scratchpad Memory (SPM) or Tightly Coupled Memory (TCM), which is closely coupled with the processor core, require direct programmer control over data placement or compiler optimization support. Nevertheless, this control enables deterministic execution as intended by the programmer, allowing TCM to compensate for the shortcomings of cache memory. While various memory system optimization studies have been conducted, research that enhances applicability by utilizing LLVM passes for LLVM compiler optimization development or preserving existing build systems has been limited. This paper proposes a new method that extracts metadata via an LLVM pass seamlessly integrated with existing build systems and uses it to allocate data to DTCM RAM in a tiered manner. Experiments using CoreMark-Pro, MiBench, and STREAM benchmarks compared performance with access frequency-based dynamic programming allocation. Results showed the locality-based method achieved more stable performance and reduced execution cycles by 1.4% to 8%, demonstrating that locality-aware allocation is more effective than frequency-only approaches in cache-TCM hybrid environments.
</div>

## Session 3: Towards Timely and Safe Neural Networks
### 15:30-16:30
#### Session Chair: Hoeseok Yang
#### [Combining Early Exit and Selective Prediction for Convolutional Neural Networks](https://ieeexplore.ieee.org/document/11111706)
***Hasna Bouraoui, Chadlia Jerad, Jeronimo Castrillon***
<div style="text-align: justify">
<b>Abstract</b>-The deployment of CNN in real-time and resource-constrained applications poses critical challenges due to their computational demands and the need for reliable decision making. In this paper, we combine adaptive inference via Early Exits (EE) with Selective Prediction (SP) to address these challenges. Early exits allow confident predictions at intermediate layers, while selective prediction introduces uncertainty estimation modules, enabling the system to abstain from low-confidence decisions or continue inference through deeper layers. This combined design lowers the risk of overconfident but erroneous predictions and improves the trade-off between performance and accuracy. As a case study, we implement and evaluate our approach on a real-time traffic sign detection task, processing the input of an RGB camera in the forward direction. In this paper, we demonstrate improved performance compared to baseline models. Compared to SP-only (Selective Prediction) and EE-only (Early Exit) baselines, our hybrid model achieves low inference depth (1.20), leading to reduced computational demand and latency. Despite this efficiency, the model maintains a high prediction accuracy (90.3%) and a low abstention rate (1.6%), ensuring fast and reliable decision making suitable for time-critical embedded applications. This demonstrates an effective trade-off between effective computation and predictive reliability.
</div>

#### [Safety-Driven DNN Sizing for Vehicular CPS](https://ieeexplore.ieee.org/document/11112702)
***Tingan Zhu, Mier Li, Bineet Ghosh, Samarjit Chakraborty, Parasara Sridhar Duggirala***
<div style="text-align: justify">
<b>Abstract</b>-Perception processing in cyber-physical systems (CPS) is now almost exclusively done using Deep Neural Networks (DNNs). Here, camera, radar and LiDAR data – in autonomous vehicles or robots – is fed into DNNs that detect surrounding obstacles and distances to them. These results are used by controllers to compute appropriate actuation signals. But a CPS typically has multiple state components, where each of them might be estimated using a different camera, radar or lidar and an associated DNN. Hence, an emerging problem is to implement multiple DNNs on a resource-constrained graphics processing unit (GPU). While many GPUs from NVIDIA and AMD allow them to be split into multiple virtual GPUs, there is little work on how to partition them, and therefore size the corresponding DNNs, when they are a part of the same CPS. In contrast to the existing practice of focusing on the inference accuracy of individual DNNs in isolation, we propose a system-level safety-driven DNN sizing (and hence GPU partitioning) scheme for vehicular CPS. Our main technical contribution is a detailed experimental evaluation of this DNN sizing approach and an empirical validation of the formal technique behind it.
</div>
