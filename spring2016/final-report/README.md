## Requirements

The final report should include

- Revised Project Design(Including Standards Section)
	*May reuse parts of your project plan and design document, if appropriate.
- Implementation details
- Testing process and testing results
- Appendix I : "Operation Manual"
	* 2-3 pages
	* step-by-step insutrction on how to setup/demo/test the system
- Appendix II: Alternative/other initial version of the design ( and why they were scraped in favor of the current version. Here may include
	* Version considered before client's specification have changed.
	* Version considered before learning more about the project
	* Version that resulted in failure to achieve specifications, etc.
- Appendix III: Other Considerations. Here you may include any other points you deem worthy of being mentioned, like what you have learned, anything funny (but relevant) that happened during the design process, etc.
- Appendix IV (Optional) Code



## Sections

#### Project Overview

File: 'overview.tex'

assigned to: Dan

Synopsis: mish mash. Introductory material from previous documents. say a tiny bit about SCADA/Honeypot, then introduce project.Consider using poster intro

#### Revised Project Plan/Design Doc

File: 'design.tex'

Assigned to: Nik

Synopsis: Honeypot architecture, how things talk to eachother. also a step back describing the entire system. Larger system integration.


#### Implementation Details

File: 'implementation.tex'

Assigned to: Nik

Synopsis: discuss technologies, specific libraries and technologies.


#### Testing process and results

File: 'testing.tex'

Assigned to: Jon o. 

Synopsis: discuss development process, tools used in addition to units tests, Gofuzz, emphasisze plugin architecture and how devices can be easily tested in isolation. discuss integration testing and vagrant isolated test networks. 100% emphasize integration testing and unit testing. 

#### Appendix I Operational Manual

File: 'manual.tex'

Assigned to: Dan, Nik

Synopsis: Hardware,initial setup, nik: (config files, moddable plugins) .Start to finish how do they assemble and start/maintain our device


#### Appendix II alternatives

File: 'alternatives.tex'

Assigned to: Nik, Jon H, Korbin

Synopsis: Discuss earlier version of (Monolithic)system before plugin architecture(Jon). using potential open source code(Nik). Hardware early considerations(Korbin)

#### Appendix III Other considerations

File: 'considerations.tex' 

Assigned to: Aash, Jon H

Synopsis: Discuss late notice of SCADA protocol dnp3 mid march. Bad spec.
