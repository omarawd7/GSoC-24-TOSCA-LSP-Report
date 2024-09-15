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
![Support__multi_file_TOSCA_projects (1)](https://github.com/user-attachments/assets/8669f603-538b-48bd-bcc2-3b8eca36beb5)
  - The LSP is aware of the newly introduced types and definitions.
![awarness_of_newly_introduced_types_and_definitions](https://github.com/user-attachments/assets/7faa3572-0e6a-4a97-a1db-8d13fb52e818)
  - Validation with error reporting for `service`, and `node` templates.
![image](https://github.com/user-attachments/assets/7580ad15-fcee-40e4-a328-e80732e31b21)
![image](https://github.com/user-attachments/assets/d49bb148-b2c3-46b3-97a4-1273a8b75a91)
  - Validation with error reporting for `schema`, `requirement`, `property`, and `capability` definitions.
![image](https://github.com/user-attachments/assets/43c19f26-8996-494d-b383-7f90668125e9)
![image](https://github.com/user-attachments/assets/a67fba8a-caff-49a3-8dd5-4a0568973015)
![image](https://github.com/user-attachments/assets/c1faad9d-fd93-4f68-a674-3f266a94d4a1)
![image](https://github.com/user-attachments/assets/e74f53d1-df61-47ea-bfc3-42b5b34ae215)
  - Validation with error reporting for `node`, `relationship`, `capability`, and `artifact` types.
![image](https://github.com/user-attachments/assets/6fca6960-1df7-4957-995e-50c4038700f1)
![image](https://github.com/user-attachments/assets/94378602-20c6-42a5-a788-cdbc81b75069)
![image](https://github.com/user-attachments/assets/42452cab-0c62-4e66-8659-82fa822ab192)    
![image](https://github.com/user-attachments/assets/4ba86af7-f7f9-4704-a10f-5ab7c3f69e0d)
  - Validation with error reporting for the TOSCA boolean functions.
![TOSCA_boolean_functions_test](https://github.com/user-attachments/assets/dc88bbc5-837c-49db-a727-bbc605065f7d)

## Technologies and Tools

- **Language**: Java.
- **Build System**: Gradle.
- **Editor**: Visual Studio Code (for testing LSP features).
- **TOSCA Specification**: TOSCA Version 2.0.
- **Java library**: LSP4j (for building the LSP server).
- **Communication Protocol**: Language Server Protocol (LSP) over `stdio` launcher.
- **YAML Library**: SnakeYAML (for parsing YAML files).
