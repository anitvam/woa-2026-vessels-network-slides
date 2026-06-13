+++
title = "Cognitive Agents in the Field"
outputs = ["Reveal"]
+++

## Robust Communication 
## through Collective Adaptive Relay Schemes
## for Maritime Vessels

<br />

*Martina Baiardi*<sup>1</sup>, Ghassan Al-Falouji<sup>2</sup>, Danilo Pianini<sup>1</sup> and Sven Tomforde<sup>2</sup>
<br />
<br /><small>
<sup>1</sup> University of Bologna, Italy <br/>
<sup>2</sup> University of Kiel, Germany <br/>
</small>

---

{{% multicol class=""%}}
{{% col %}}

## Context

* Autonomous Maritime Operations
* Support the transition towards autonomy by achieving *situational awareness*.

{{% /col %}}
{{% col class=""%}}

## GAP

* Lack of a *communication infrastructure* to support the transmission of sensors data

<br />
<br />


{{% /col %}}
{{% /multicol %}}

---

## Challenges

{{% multicol %}}
{{% col %}}

* *Dynamic sparse* vessels *distribution*
* *Environmental conditions*
* Heterogeneity of *communication means* onboard
  * *Traditional* communication <i class="fa-solid fa-arrow-right-long"></i> *limited bandwidth* 
  * *Satellite*  <i class="fa-solid fa-arrow-right-long"></i> *expensive antennas* not equipped on the vessel or suffers *high latency*.
  * *Cellular* (4G and 5G) <i class="fa-solid fa-arrow-right-long"></i> *limited to coastal areas*

{{% /col %}}
{{% col class=""%}}

<img src="images/bandwidth_decay.svg" width=100% />

{{% /col %}}
{{% /multicol %}}

---
<!-- 
{{% multicol %}}
{{% col %}}

## 1. Non-Collaborative Direct Communication

Inspired to current network topology, vessels *communicate directly towards shore station* whenever they have some bandwidth available.

The limitations of this approach are intuitive:

1. *Limited coverage* of vessels
2. Shore stations as a *bottle-neck* 
3. Information *redundancy* 


{{% /col %}}
{{% col class="col-5"%}}

<div style="text-align:right;">
<img src="images/baseline1.svg" class="preview-border zoom-in" style="transform-origin: bottom right;"/>
<img src="images/baseline2.svg" width=20% class="preview-border" style="vertical-align:bottom;"/>
</div>
<div style="text-align:right;">
<img src="images/baseline3.svg" width=20% class="preview-border" />
<img src="images/csc.svg" width=20% class="preview-border" style="text-align:right;"/>
</div>

{{% /col %}}
{{% /multicol %}}

---

{{% multicol %}}
{{% col %}}

## 2. Distance-based Multi-Relay Communication

* All vessels that cannot communicate with shore station with sufficient bandwidth *relay* its data stream to a vessel along the *geographical* *shortest* *path* towards the land station.

* Direct communication with the relay may be insufficient, while using vessels not on the shortest path may be more effective.

{{% /col %}}
{{% col class="text-center col-5"%}}

<div style="text-align:left;">
<img src="images/baseline1.svg" width=20% class="preview-border"/>
<img src="images/baseline2.svg" class="zoom-in preview-border" style="transform-origin: bottom left; vertical-align:bottom;"/>
</div>
<div style="text-align:left;">
<img src="images/baseline3.svg" width=20% class="preview-border" />
<img src="images/csc.svg" width=20% class="preview-border" style="text-align:right;"/>
</div>

{{% /col %}}
{{% /multicol %}}

---

{{% multicol %}}
{{% col %}}

## 3. Data Rate-based Multi-Relay Communication

This network improves the Distance-based Multi-Relay Communication by selecting the relay which *maximises* the *data rate* instead of minimising the distance.

{{% /col %}}
{{% col class="text-center col-5"%}}

<div style="text-align:right;">
<img src="images/baseline1.svg" width=20% class="preview-border"/>
<img src="images/baseline2.svg" width=20% class="preview-border " />
</div>
<div style="text-align:right;">
<img src="images/baseline3.svg" class="zoom-in preview-border" style="transform-origin: top right;"/>
<img src="images/csc.svg" width=20% class="preview-border" style="vertical-align: top;"/>
</div>

{{% /col %}}
{{% /multicol %}}
 
---
-->

{{% multicol %}}
{{% col %}}

## Collective Summarisation Clusters (CSC)

We propose a novel *decentralized* *network* *techniques* to improve sensors’ data transport and collection in the maritime environment.

* IDEA: high-fidelity data can be collected locally, then summarised at strategic points within the network and finally forwarded toward the land station.

* Vessels self-organise into *clusters* where data can be collected in a designated *summariser*. The leader then forwards the summarised output to the land station or to a relay in the next cluster.

{{% /col %}}
{{% col class="text-center col-5 h-100" %}}

<img src="images/csc.svg"  />

{{% /col %}}
{{% /multicol %}}

---

{{% multicol %}}
{{% col %}}

## Comparison of Network Approaches


To do so, we propose four network approaches:
1. Non-collaborative *direct communication* towards shore station
2. MST *Distance-based multi-relay* communication
3. MST *Data rate-based multi-relay* communication
4. *Collective Summarization Clusters*

{{% /col %}}
{{% col class="text-center col-5"%}}

<img src="images/baseline1.svg" width=40% class="preview-border"/>
<img src="images/baseline2.svg" width=40% class="preview-border"/><br/>
<img src="images/baseline3.svg" width=40% class="preview-border"/>
<img src="images/csc.svg" width=40% class="preview-border"/>

{{% /col %}}
{{% /multicol %}}

---

{{% multicol %}}
{{% col %}}

## Simulation Setup

* All vessels are equipped with: *GPS*, *ARPS (VHF)*, *Wi-Fi*, and *5G consumer module*

* *$p_{5G}$* percentage of vessels with *5G repeater*

* *6 hours* time window navigation data from *August 18, 2022* from the Kiel Fjord

* *Open data* used to locate *5G towers* and the *AIS shore stations* along the Kiel coast.

* Simulations performed with *Alchemist²* 

* We adopted a functional *macroprogramming* framework for the implementation of the algorithm

<small>

² https://alchemistsimulator.github.io/

</small>


{{% /col %}}
{{% col class="text-center"%}}

<img src="images/simulation.gif" width=100% />

{{% /col %}}
{{% /multicol %}}

---

## Evaluation

As evaluation metric we measure the data rate that each vessel transmit for each network configuration.

<img src="images/linechart_datarate.png" />

---

## Conclusion

*Collective Summarisation Clusters* (CSC) self-adaptive network configuration outperforms other approaches in terms of data rate exchanged, even when the percentage of vessels equipped with 5G repeaters is low.


Source code for executing and reproducing experiments is freely available on *GitHub* under a permissive license.

<img src="images/qr.png" /><br />

### Thank you
 