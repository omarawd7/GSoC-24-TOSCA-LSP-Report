# Language Server for OASIS TOSCA Version 2

##  Project Information

| **Field**              | **Details**                                                                                                                 |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **Student**            | [Omar Awad](https://github.com/omarawd7)                                                                                    |
| **Organization**       | [Eclipse Foundation](https://www.eclipse.org/org/foundation/)                                                               |
| **Primary repository** | [org.eclipse.winery.lsp](https://github.com/omarawd7/winery/tree/lsp/org.eclipse.winery.lsp)                                |
| **Project name**       | Tosca LSP Server                                                                                                            |
| **Project mentor**     | [Dr. Oliver Kopp](https://github.com/koppor/)                                                                               |
| **Project page**       | [Google Summer of Code 2024 Project Page](https://summerofcode.withgoogle.com/programs/2024/projects/56o5Fdkj)              |
| **TOSCA Version 2.0**  | [TOSCA Version 2.0 Committee Specification Draft](https://docs.oasis-open.org/tosca/TOSCA/v2.0/csd06/TOSCA-v2.0-csd06.html) |

## Project Summary

This project is an enhancement for [Eclipse Winery](https://www.eclipse.org/winery/).
Eclipse Winery is a web-based environment for modeling OASIS TOSCA topologies.
Currently, Winery focuses on providing a graphical editing environment for application topologies.
It also covers [many research](https://www.opentosca.org/) prototype implementations.

This project implements a Language Server Protocol (LSP) provider for OASIS TOSCA YAML files.
This make Eclipse Winery also a component for more text-based people and would lays a groundwork for integrating with other research.
As a result, it provides users with assistance in editing TOSCA YAML files, making the creation and editing process more efficient and less error-prone.

## Background

Applications today are often made up of multiple components, which may be distributed across various microservices.
[OASIS TOSCA (Topology and Orchestration Specification for Cloud Applications)](https://www.oasis-open.org/committees/tosca/) is a standard designed to describe and manage these topologies.
The core TOSCA specification defines a language for describing service components and their relationships using a service topology.
It also includes lifecycle management procedures that enable the orchestration of services—covering creation, modification, and scaling—throughout the complete service lifecycle (e.g., deployment, scaling, patching, and monitoring).
Currently, crafting TOSCA YAML files manually is complex and prone to errors due to the lack of tooling support.
This project aimed to develop a **Language Server for TOSCA v2** that integrates with Visual Studio Code.

## Outcome

The outcomes of the project include:

1. LSP server supports the latest OASIS TOSCA 2.0 standard.
2. Awareness of the newly introduced types and definitions and makes them available in the service template.
3. Importing from multiple files TOSCA files within a repository or directory.
4. Context-dependent auto-completion for the TOSCA keywords and types.
5. Validation for the TOSCA types: artifact type, capability type, node type, and relationship type.
6. Validation for the definitions: imports definition, property definition, requirements definition, schema definition, and capability definition.
7. Validation for the templates: service template and node templates.
8. Enhanced key identification mechanism for the TOSCA files by prefixing keys with their parent elements and list indices, providing better clarity and traceability in nested YAML structures.
9. Demonstrating the functionality of the LSP server using compatible Visual Studio Code.

## LSP Features

### Context dependent auto-completion for TOSCA keywords.
    
![ContextDependentKeywordsCompletion](https://github.com/user-attachments/assets/21e4c19d-32d2-400d-9207-106c01289803)

### Context dependent auto-completion for the types keyword value.

#### Node Templates

![](https://github.com/user-attachments/assets/74f86c6d-4b01-47c5-ae81-d8c8a4838a58)

#### Capability Definitions

![](https://github.com/user-attachments/assets/7903888f-1bce-4854-aa47-2c09cb1ab8bb)
  
### Context dependent auto-completion for the `drived_from` keyword value

#### Aritfact Type

![](https://github.com/user-attachments/assets/86b64627-7f9b-4e11-a355-af8fe9a29c31)

#### Capability Type

![](https://github.com/user-attachments/assets/4c82858a-3814-496b-9846-7c5c82ea77f3)

#### Node Type

![](https://github.com/user-attachments/assets/89f0fae7-33a2-454c-aacc-74def90487b6)

#### Relationship Type

![](https://github.com/user-attachments/assets/72ddd7d4-3268-4f4f-9516-a0a854ca1772)

#### YAML syntax validation with error reporting
  
![](https://github.com/user-attachments/assets/bb701795-1316-4c79-8f96-574140b9cd94)    

### Improved parsing of imports definitions for nested TOSCA files.
  
![image](https://github.com/user-attachments/assets/2b7b702f-0770-4159-ab09-0c23ded9c082)

### Support for multi-file TOSCA projects
    
![Support__multi_file_TOSCA_projects (1)](https://github.com/user-attachments/assets/8669f603-538b-48bd-bcc2-3b8eca36beb5)

### The LSP is aware of the newly introduced types and definitions
    
![awarness_of_newly_introduced_types_and_definitions](https://github.com/user-attachments/assets/7faa3572-0e6a-4a97-a1db-8d13fb52e818)
  
### Validation with error reporting for service, and node templates

#### Node Templates

![image](https://github.com/user-attachments/assets/7580ad15-fcee-40e4-a328-e80732e31b21)

#### Service Template

![image](https://github.com/user-attachments/assets/d49bb148-b2c3-46b3-97a4-1273a8b75a91)

### Validation with error reporting for schema, requirement, property, and capability definitions.

#### Schema Definition

![image](https://github.com/user-attachments/assets/43c19f26-8996-494d-b383-7f90668125e9)

#### Requirement Definition

![image](https://github.com/user-attachments/assets/a67fba8a-caff-49a3-8dd5-4a0568973015)

#### Property Definition

![image](https://github.com/user-attachments/assets/c1faad9d-fd93-4f68-a674-3f266a94d4a1)

#### Capability Definition

![image](https://github.com/user-attachments/assets/e74f53d1-df61-47ea-bfc3-42b5b34ae215)

### Validation with error reporting for node, relationship, capability, and artifact types.

#### Node Type

![image](https://github.com/user-attachments/assets/6fca6960-1df7-4957-995e-50c4038700f1)

#### Relationship Type

![image](https://github.com/user-attachments/assets/94378602-20c6-42a5-a788-cdbc81b75069)

#### Capability Type

![image](https://github.com/user-attachments/assets/42452cab-0c62-4e66-8659-82fa822ab192)    

#### Artifact Type

![image](https://github.com/user-attachments/assets/519da4dd-cef8-43a4-ae9c-e25e2fd98c17)

### Validation with error reporting for the TOSCA boolean functions in the properties.
    
![TOSCA_boolean_functions_test](https://github.com/user-attachments/assets/dc88bbc5-837c-49db-a727-bbc605065f7d)

## Future Work

- Add Go To definition feature to the LSP for the types and `derived_from` values.
- Complete the validation for the rest of the TOSCA file keynames.
- Add auto-completion for more contexts in tosca files such as auto-completing the requirement definition node and capability.
- Importing from other directories or repositories into the opened TOSCA file.

## Benefits

- With enhanced YAML parsing, validation, and auto-completion, developers will be able to work more efficiently with complex TOSCA models.
- The validation mechanisms reduce the chances of errors due to incorrect file structures or values.
- The LSP makes it easier for developers to get real-time feedback while editing TOSCA YAML files in Visual Studio Code.

## Key Learnings and Challenges

- **Java Coding**: I learned and deepened my knowledge of Java, which was essential for building the language server and handling various parsing tasks.
  
- **LSP Protocol**: Implementing the Language Server Protocol (LSP) was a new challenge, especially in handling communication between the client (VS Code) and the server. I learned how LSP works, including methods to provide language features such as autocomplete and error checking.

- **Handling References in YAML Files**: A significant challenge involved managing references to specific lines and sections in YAML files. I had to implement ways to correctly and uniquely identify and locate elements within the nested structure of TOSCA YAML files.

- **Reading Specifications**: The TOSCA 2.0 specification was completely new to me. I had to become familiar with reading to ensure correct implementation of TOSCA's features within the language server. This skill was crucial to accurately translate spec requirements into functional code.

These areas, although challenging at times, have contributed greatly to my growth as a developer and my understanding of the TOSCA ecosystem.

## Technologies and Tools

- **Language**: Java.
- **Build System**: Gradle.
- **Editor**: Visual Studio Code (for testing LSP features).
- **TOSCA Specification**: TOSCA Version 2.0.
- **Java library**: [Eclipse LSP4j](https://github.com/eclipse-lsp4j/lsp4j) (for building the LSP server).
- **Communication Protocol**: Language Server Protocol (LSP) over `stdio` launcher.
- **YAML Library**: [SnakeYAML](https://github.com/snakeyaml/snakeyaml) (for parsing YAML files).

## Statistics

| **Total commits**       | 93 |
| **Changes**    | 18078 |
| **Additions**    | 18036 |
| **Deletions**    | 42 |
