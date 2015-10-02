## Introduction

The internet can be a hazardous place. Every day an unfathomable amount of cyber-attacks are being perpetrated throughout the world. Being a target of these attacks can be detrimental to any entity that is intended to receive such attacks. It is imperative that countermeasures are constantly being taken to protect the integrity of any potential target. This is where this project begins.

The goal of the project is to create a standalone security device that can be placed in an industrial network to monitor traffic, looking for security-related deviations, and act as a low interaction honeypot. A honeypot is a computer security mechanism that is set to detect, deflect, or counteract the unauthorized use of information systems. A honeypot is intended to appear as a part of some network, but is actually isolated and monitored, relaying the information it detects to a system administrator.

This specific device is intended to be implemented in an ICS/SCADA environment. SCADA (supervisory control and data acquisition) is a category of software application program for process control, the gathering of data in real time from remote locations in order to control equipment and conditions.


## Work Structure
*Risk/Feasability Assesment*

This project is routinely implemented in industry with high success rates. Several software implementations of SCADA honeypots already exist in the open source community. However, our implementation will be custom because the client has a secondary goal of including an IDS on the system. Creating the honeypot software from scratch will minimize the resources required from the platform. This is important because the computer needs to be a small standalone device. A Raspberry PI only has 512MB of RAM for example and an IDS typically uses a lot of memory and process cycles. Most risk can be mitigated with proper contingency planning.

| Event | Details | Initial Risk  | Contingency Plan| Final Risk  |
|:--:   |:--:     |:--:           |:--:               |:--:         |
|Web Server | Build, test, and integrate a custom web server| Medium | Utilize open source Nginx server| Low |
|SSH Server | Build, test, and integrate a custom SSH server | Medium | Use Open SSH | Low|
|Event Alerts| Custom logging to Splunk database through GOLang Rest | Medium | Switch to SMTP | Low |
|SCADA Services | Develop clients unspecified SCADA services | Medium | Implement Conpot | Low |
|Honeypot Service| Integrate all components into a working Honeypot service| Medium | Implement Conpot | Low|
|IDS | Minimize IDS services of Bro or Snort software to run on a small platform | High | Create a better device | Medium |

Installing an IDS on a small platform such as a Raspberry PI may not be feasible. If this is the case, developing a custom platform with greater processing power and more memory will be explored. If this isn't feasible, then the secondary goal will have to be canceled. However, the overall honeypot implementation carries a low risk of failure.


*Cost*

Alliant Energy requires service in twenty eight different locations. Each location will house a standalone minimal computer. At this stage of development, the Raspberry PI is the assumed device. A model description follows.

| Model         | Details            | Unit Cost          | Vendor            | Total Cost  | 
|:-------------:|:------------------:|:------------------:|:------:           | :----:      |
|Raspberry PI B+|700Mhz CPU 512MB Ram| 30 USD Plus Tax    |Allied Electronics | 840 USD Plus Tax |

This device is subject to change throughout the project development depending on implementation and client needs. However, as of the present date, the Raspberry PI is the best known device. An updated version of the plan may be submitted if a better hardware implementation is found. This cost analysis reflects an initial estimate. It does not reflect future maintenance cost.


