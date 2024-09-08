<!--
SPDX-FileCopyrightText: 2024 Alexandre Jesus <me@adbjesus.com>

SPDX-License-Identifier: CC-BY-4.0
-->

<!-- Replace the comment above with your licence information for your problem
statement. Consider all copyright holders and contributors. -->

<!-- According to the copyright and licensing policy of ROAR-NET original
problem statements contributed to this repository shall be licensed under the
CC-BY-4.0 licence. In some cases CC-BY-SA-4.0 might be accepted, e.g., if the
problem is based upon an existing problem licensed under those terms. Please
provide a clear justification when opening the pull request if the problem is
not licensed under CC-BY-4.0 -->

<!-- Remove the section below before submitting -->

<!-- Remove the section above before submitting -->

# Distribution Generation Allocation Problem
Rene Prenc, Faculty of Engineering, University of Rijeka, Croatia 

<!-- Put two empty spaces at the end of each author line except the last for
proper formatting -->

Copyright 2024 Rene Prenc.

This document is licensed under XXXX.

<!-- Complete the above accordingly. Copyright and licensing information must be
consistent with the comment at the beggining of the markdown file -->

## Introduction

The Distributed Generation Allocation Problem refers to the challenge of optimally placing and sizing distributed generation (DG) units within an electrical distribution network. Distributed generation typically consists of smaller-scale energy sources like solar panels, wind turbines, or small natural gas-powered generators, which are located closer to the point of consumption (e.g., in residential areas or industrial plants). In the last 15-20 years this is a topic arising due to environmental concerns and shifting of EU policy towards decarbonization. Once passive distribution networks which were used for unidirectional transfer of electric power & energy are upgrading to active and smart networks. The primary objective of DG allocation is to optimize certain performance indicators of the power system and the common objective functions include: minimization of power losses (reducing the real power losses in the distribution network), voltage profile improvement (maintaining voltage levels within acceptable limits and improving the voltage profile across all the nodes of the network), cost minimization (reducing the total cost, which includes the cost of installation, operation, and maintenance of DG units), reliability enhancement (improving the reliability indices such as SAIFI (System Average Interruption Frequency Index) and SAIDI (System Average Interruption Duration Index)), environmental benefits (reducing greenhouse gas emissions by integrating renewable energy sources), etc.

## Task

The idea is to find the optimal locations (nodes) and installed powers (MW) of DG units within a distibution network in order to optimise (maximise) financial parameters of the DG owners and techno-economic parameters of the Distribution System Operator, which is the owner of the network.

## Detailed description

The goal is to simultaneously maximize the net present values of DG projects and DSO's savings. Thus, the objective function consists of two parts, one involving DG projects and the other involving DSO's savings. The net present values of DG projects are calculated by discounting the annual cash flows to the present value. The time period under consideration is equal to the number of years in which the feed-in tariffs  are guaranteed by the subordinate legislation in Croatia. The cash flows of the DG project consist of revenues (EUR/kwh of produced electrical energy) and expenses (DG installation costs, fixrd and variable O&M costs). The net present value of a DSO project is calculated by discounting the annual savings to the present value. The annual savings for DSO consider the difference between annual network energy losses of the existing network and after allocation of new DG units. Since the DSO is the only entity responsible for the losses in its network, it has to buy energy to cover its losses, usually from a Generator Company (GENCO). All the above equations must satisfy the power balance constraints, thermal constraints and NPV constraints at all times. The algorithm also includes load growth of each node in the network per annum. The loads and DGs are modeled for an average day in the year (24 h time slots) in order to more accurately determine the ovjective function. Also, to assess the NPV of the DSO, the power losses of the test network need to be estimated on a yearly basis. For this, a so-called "backward/forward sweep" iterative algorithm must be conducted. The authors have modified the genetic algorithm for DG allocation purpose. The coding of the individuals in a population into chromosomes was done with integer values and the chromosomes contain two sets of data. The first part are the locations of new DG units and the second part are the sizes of new DG units.   


## Instance data file

Describe the format of a problem instance file.

## Solution file

Describe the format of a solution file.

## Example

### Instance

Provide a small example instance in the described format.

### Solution

Provide a feasible solution to the example instance in the described format
(including its evaluation measure).

### Explanation

Optionally, provide a descriptive and/or visual explanation of the solution (and
its evaluation measure value) for the instance.

## Acknowledgements

This problem statement is based upon work from COST Action Randomised
Optimisation Algorithms Research Network (ROAR-NET), CA22137, is supported by
COST (European Cooperation in Science and Technology).

<!-- Please keep the above acknowledgement. Add any other acknowledgements as
relevant. -->

## References

Put any relevant references here.
