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
| **TOSCA specification version 2**    | [TOSCA Version 2.0 Committee Specification Draft]([https://summerofcode.withgoogle.com/myprojects/details/56o5Fdkj](https://docs.oasis-open.org/tosca/TOSCA/v2.0/csd06/TOSCA-v2.0-csd06.html))  |

## Project Summary

This project is an enhancement for Eclipse Winery, Eclipse Winery is a web-based environment for modeling OASIS TOSCA topologies, by implementing basic security measures. Currently, Winery focuses on providing a graphical editing environment for modeling application topologies. However, by having a Language Server Protocol (LSP) provider for OASIS TOSCA YAML files. This would allow Winery to support the latest version of the OASIS TOSCA standard and handle dynamic type additions. The outcomes of the project include: <br>
1- LSP server supports the latest OASIS TOSCA 2.0 standard. <br>
2- LSP server that is aware of newly introduced types and definitions and makes them available in the service template.<br>
3- LSP server that handles importing from multiple files within a repository or directory.<br>
4- LSP server that has context-dependent auto-completion for the TOSCA keywords and types.<br>
5- Validation for the Tosca types:
    artifact type, capability type, node type, and relationship type.<br>
6- Validation for the definitions: imports definition, property definition, requirements definition, schema definition, and capability definition.<br>
7- Validation for the templates:
    service template, and node template.<br>
8- Demonstrating the functionality of the LSP server using compatible Visual Studio Code.

## Vision

Applications today are often made up of multiple components, which may be distributed across various microservices.
OASIS TOSCA (Topology and Orchestration Specification for Cloud Applications) is a standard designed to describe and manage these topologies.
The core TOSCA specification defines a language for describing service components and their relationships using a service topology.
It also includes lifecycle management procedures that enable the orchestration of services—covering creation, modification, and scaling—throughout the complete service lifecycle (e.g., deployment, scaling, patching, and monitoring).
Currently, crafting TOSCA YAML files manually is complex and prone to errors due to the lack of tooling support.
This project aims to develop a **Language Server for TOSCA v2** that integrates with Visual Studio Code (VS Code).
It provides users with assistance in editing TOSCA YAML files, making the process more efficient and less error-prone.

## LSP Features

- #### Context dependent auto-completion for TOSCA keywords.
    
  ![ContextDependentKeywordsCompletion](https://github.com/user-attachments/assets/21e4c19d-32d2-400d-9207-106c01289803)
- #### Context dependent auto-completion for the types keyword value.

`node templates`:
  ![image](https://github.com/user-attachments/assets/74f86c6d-4b01-47c5-ae81-d8c8a4838a58)
  `capability definitions`:
  ![image](https://github.com/user-attachments/assets/7903888f-1bce-4854-aa47-2c09cb1ab8bb)
- #### Context dependent auto-completion for the drived_from keyword value.

  `artifact type`:
  ![image](https://github.com/user-attachments/assets/86b64627-7f9b-4e11-a355-af8fe9a29c31)
  `capability type`:
  ![image](https://github.com/user-attachments/assets/4c82858a-3814-496b-9846-7c5c82ea77f3)
  `node type`:
  ![image](https://github.com/user-attachments/assets/89f0fae7-33a2-454c-aacc-74def90487b6)
  `relationship type`:
  ![image](https://github.com/user-attachments/assets/72ddd7d4-3268-4f4f-9516-a0a854ca1772)
- #### Yaml syntax validation with error reporting.
  
  ![image](https://github.com/user-attachments/assets/bb701795-1316-4c79-8f96-574140b9cd94)    
- #### Improved parsing of imports definitions for nested TOSCA files.
  
  ![image](https://github.com/user-attachments/assets/2b7b702f-0770-4159-ab09-0c23ded9c082)
- #### Support for multi-file TOSCA projects.
    
  ![Support__multi_file_TOSCA_projects (1)](https://github.com/user-attachments/assets/8669f603-538b-48bd-bcc2-3b8eca36beb5)
- #### The LSP is aware of the newly introduced types and definitions.
    
  ![awarness_of_newly_introduced_types_and_definitions](https://github.com/user-attachments/assets/7faa3572-0e6a-4a97-a1db-8d13fb52e818)
- #### Validation with error reporting for service, and node templates.

  `node template`:
  ![image](https://github.com/user-attachments/assets/7580ad15-fcee-40e4-a328-e80732e31b21)
  `service template`:
  ![image](https://github.com/user-attachments/assets/d49bb148-b2c3-46b3-97a4-1273a8b75a91)
- #### Validation with error reporting for schema, requirement, property, and capability definitions.

  `schema definition`:
  ![image](https://github.com/user-attachments/assets/43c19f26-8996-494d-b383-7f90668125e9)
  `requirement definition`:
  ![image](https://github.com/user-attachments/assets/a67fba8a-caff-49a3-8dd5-4a0568973015)
  `property definition`:
  ![image](https://github.com/user-attachments/assets/c1faad9d-fd93-4f68-a674-3f266a94d4a1)
  `capability definition`:
  ![image](https://github.com/user-attachments/assets/e74f53d1-df61-47ea-bfc3-42b5b34ae215)
- #### Validation with error reporting for node, relationship, capability, and artifact types.

  `node type`:
  ![image](https://github.com/user-attachments/assets/6fca6960-1df7-4957-995e-50c4038700f1)
  `relationship type`:
  ![image](https://github.com/user-attachments/assets/94378602-20c6-42a5-a788-cdbc81b75069)
  `capability type`:
  ![image](https://github.com/user-attachments/assets/42452cab-0c62-4e66-8659-82fa822ab192)    
  `artifact type`:
  ![image](https://github.com/user-attachments/assets/519da4dd-cef8-43a4-ae9c-e25e2fd98c17)
- #### Validation with error reporting for the TOSCA boolean functions in the properties.
    
  ![TOSCA_boolean_functions_test](https://github.com/user-attachments/assets/dc88bbc5-837c-49db-a727-bbc605065f7d)

## Future Work

- Add Go To definition feature to the LSP for the types and derived_from values.
- Complete the validation for the rest of the TOSCA file keynames.
- Add auto-completion for more contexts in tosca files like auto-completing the requirement definition node and capability.
- Importing from other directories or repositories into the opened TOSCA file.

## Technologies and Tools

- **Language**: Java.
- **Build System**: Gradle.
- **Editor**: Visual Studio Code (for testing LSP features).
- **TOSCA Specification**: TOSCA Version 2.0.
- **Java library**: LSP4j (for building the LSP server).
- **Communication Protocol**: Language Server Protocol (LSP) over `stdio` launcher.
- **YAML Library**: SnakeYAML (for parsing YAML files).

## Statistics

| **Total commits**       | 93 |
| **Changes**    | 18078 |
| **Additions**    | 18036 |
| **Deletions**    | 42 |
