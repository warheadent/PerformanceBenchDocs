# System Specification
The plugin uses a Blueprint Library made in C++ in order to pull some information the Unreal Engine has on the end-user's system configuration.

![[SystemSpecsExample.png]]

The following details were exposed to Blueprint:

- Operating System Version
- CPU/Processor Name
- GPU Info
	- GPU Name
	- GPU Brand
	- GPU Driver Version
	- GPU Driver Date
- Total Physical Memory
- RHI Version (D3D11, D3D12, etc.)

These functions may prove useful if developers are looking to capture this information to an analytics backend or output log.

![[SystemConfigurationFunctions.png]]