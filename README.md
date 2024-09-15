# TOSCA v2 Language Server
<br>
<br>
<br>
## Project Information

| **Field**              | **Details**                                                      |
|------------------------|------------------------------------------------------------------|
| **Student**            | Omar Awad                                                        |
| **Organization**       | [Eclipse Foundation](https://www.eclipse.org/org/foundation/)                                               |
| **Primary repository**  | [org.eclipse.winery.lsp](https://github.com/omarawd7/winery/tree/lsp/org.eclipse.winery.lsp)             |
| **Project name**       | Tosca LSP Server                                                 |
| **Project mentor**    | Dr. Oliver Kopp                                        |
| **Project page**       | [Google Summer of Code 2024 Project Page](https://summerofcode.withgoogle.com/myprojects/details/56o5Fdkj)  |


## Vision

Applications today are often made up of multiple components, which may be distributed across various microservices.
OASIS TOSCA (Topology and Orchestration Specification for Cloud Applications) is a standard designed to describe and manage these topologies.
The core TOSCA specification defines a language for describing service components and their relationships using a service topology.
It also includes lifecycle management procedures that enable the orchestration of services—covering creation, modification, and scaling—throughout the complete service lifecycle (e.g., deployment, scaling, patching, and monitoring).
Currently, crafting TOSCA YAML files manually is complex and prone to errors due to the lack of tooling support.
This project aims to develop a **Language Server for TOSCA v2** that integrates with Visual Studio Code (VS Code).
It provides users with assistance in editing TOSCA YAML files, making the process more efficient and less error-prone.

## Goals and Deliverables

- **LSP Features**:
  - Context dependent auto-completion for TOSCA keywords, types, and drived_from values.
  - Syntax validation with error reporting.
  - Improved parsing of `imports` definitions for nested TOSCA files.
  - Support for multi-file TOSCA projects.
  - Validation for `service`, and `node` templates.
  - Validation for `schema`, `requirement`, `property`, and `capability` definitions.
  - Validation for `node`, `relationship`, `capability`, and `artifact` types.
  - Validation for the TOSCA boolean functions.
## Technologies and Tools

- **Language**: Java.
- **Build System**: Gradle.
- **Editor**: Visual Studio Code (for testing LSP features).
- **TOSCA Specification**: TOSCA Version 2.0.
- **Java library**: LSP4j (for building the LSP server).
- **Communication Protocol**: Language Server Protocol (LSP) over `stdio` launcher.
- **YAML Library**: SnakeYAML (for parsing YAML files).
