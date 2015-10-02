## Introduction

The internet can be a hazardous place. Every day an unfathomable amount of cyber-attacks are being perpetrated throughout the world. Being a target of these attacks can be detrimental to any entity that is intended to receive such attacks. It is imperative that countermeasures are constantly being taken to protect the integrity of any potential target. This is where this project begins.

The goal of the project is to create a standalone security device that can be placed in an industrial network to monitor traffic, looking for security-related deviations, and act as a low interaction honeypot. A honeypot is a computer security mechanism that is set to detect, deflect, or counteract the unauthorized use of information systems. A honeypot is intended to appear as a part of some network, but is actually isolated and monitored, relaying the information it detects to a system administrator.

This specific device is intended to be implemented in an ICS/SCADA environment. SCADA (supervisory control and data acquisition) is a category of software application program for process control, the gathering of data in real time from remote locations in order to control equipment and conditions.


## Work Structure
*Cost*

Alliant Energy requires service in twenty eight different locations. Each location will house a standalone minimal computer. At this stage of development, the Raspberry PI is the assumed device. A model description follows.

| Model         | Details            | Unit Cost          | Vendor            | Total Cost  | 
|:-------------:|:------------------:|:------------------:|:------:           | :----:      |
|Raspberry PI B+|700Mhz CPU 512MB Ram| 30 USD Plus Tax    |Allied Electronics | 840 USD Plus Tax |

This device is subject to change throughout the project development depending on implementation and client needs. However, as of the present date, the Raspberry PI is the best known device. An updated version of the plan may be submitted if a better hardware implementation is found. This cost analysis reflects an initial estimate. It does not reflect future maintence cost.

