# System Specification
The plugin use a Blueprint Library made in C++ in order to pull some information the Unreal Engine has on the end-user's system configuration.

The following details were exposed to Blueprint:

- Operating System Version
- CPU/Processor Name
- GPU Name
- Total Physical Memory
- RHI Version (D3D11, D3D12, etc.)

These functions may prove useful if you're looking to capture these details to an analytics backend or output log.
