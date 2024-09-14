# TOSCA v2 Language Server

## Vision

Applications today are often made up of multiple components, which may be distributed across various microservices.

OASIS TOSCA (Topology and Orchestration Specification for Cloud Applications) is a standard designed to describe and manage these topologies.

The core TOSCA specification defines a language for describing service components and their relationships using a service topology.

It also includes lifecycle management procedures that enable the orchestration of services—covering creation, modification, and scaling—throughout the complete service lifecycle (e.g., deployment, scaling, patching, and monitoring).

Currently, crafting TOSCA YAML files manually is complex and prone to errors due to the lack of tooling support.

This project aims to develop a **Language Server for TOSCA v2** that integrates with Visual Studio Code (VS Code).

It provides users with assistance in editing TOSCA YAML files, making the process more efficient and less error-prone.
