# GSOC 2024 TOSCA version 2 Language Server
<br>

##  Project Information

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

 ## LSP Features
 
  - Context dependent auto-completion for TOSCA keywords.
![ContextDependentKeywordsCompletion](https://github.com/user-attachments/assets/21e4c19d-32d2-400d-9207-106c01289803)
  - Context dependent auto-completion types value for `node templates` and `capability definitions`.
![type_auto_completion](https://github.com/user-attachments/assets/5235a4f1-0a50-49ba-832a-44f64f874304)
  - Context dependent auto-completion drived_from values for `node`, `relationship`, `capability`, and `artifact` types.
![Derived_from_auto_completion](https://github.com/user-attachments/assets/cc1e555a-33d0-448f-8cbc-782419972a23)
  - Yaml syntax validation with error reporting.
![yaml_validation](https://github.com/user-attachments/assets/f24587a2-84b0-45a5-abc9-8d463a96cea0)
  - Improved parsing of `imports` definitions for nested TOSCA files.
![importsTest](https://github.com/user-attachments/assets/cf4f7681-0463-4142-889e-2f1566bbe1d9)
  - Support for multi-file TOSCA projects.
  - The LSP is aware of the newly introduced types and definitions.
  - Validation with error reporting for `service`, and `node` templates.
  - Validation with error reporting for `schema`, `requirement`, `property`, and `capability` definitions.
  - Validation with error reporting for `node`, `relationship`, `capability`, and `artifact` types.
  - Validation with error reporting for the TOSCA boolean functions.
## Technologies and Tools

- **Language**: Java.
- **Build System**: Gradle.
- **Editor**: Visual Studio Code (for testing LSP features).
- **TOSCA Specification**: TOSCA Version 2.0.
- **Java library**: LSP4j (for building the LSP server).
- **Communication Protocol**: Language Server Protocol (LSP) over `stdio` launcher.
- **YAML Library**: SnakeYAML (for parsing YAML files).
