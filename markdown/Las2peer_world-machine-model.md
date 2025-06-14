# las2peer Framework World Machine Model

## Authors

* Swan Htet Aung Phyo
* Aung Zayar Moe
* Michal Rowski
* Alexander Rosol

## 1. Business Goal

las2peer enables decentralized microservice development and deployment across peer-to-peer networks, eliminating centralized dependencies while reducing costs and increasing resilience through distributed, globally scalable architectures.

### 1.1 Glossary of Terms

| Concept               | Description                                                                            |
| --------------------- | -------------------------------------------------------------------------------------- |
| Developer             | Software engineer creating and deploying services using las2peer framework            |
| Service Agent         | Autonomous software entity encapsulating service logic and handling requests          |
| Node                  | Network peer hosting services and participating in distributed operations             |
| Network Administrator | Entity managing and monitoring overall P2P network                                    |
| Service Consumer      | Application or user consuming services deployed on las2peer network                   |
| Envelope              | Secure, encrypted data container for inter-agent communication                        |
| FreePastry            | Underlying P2P library handling network communication and routing                     |
| Bootstrap Node        | Initial network entry point helping new nodes join P2P network                       |

## 2. The Functional Scope of the Framework for Developers

The solution provides comprehensive Java-based development framework compatible with Java 17 environments across Windows, Linux, and macOS. Developers create services by setting up las2peer template projects, defining service classes extending the Service base class, implementing annotated service methods, configuring service properties, and building JAR packages.

Service deployment involves starting las2peer nodes and registering service agents. Services become automatically available across P2P networks. Authentication operates through agent-based security using cryptographic identities. Developers monitor service performance and manage service lifecycle through administrative tools.

### 2.1 Developer Profile

Developer profiles contain service ownership information, deployment history, node management credentials, and development tool access. Profiles maintain service registries with owned services, node configuration and network participation status, development environment setup with IDE integration, access to logging and monitoring tools, and service versioning capabilities.

### 2.2 Development Tools Menu

Developer toolkit includes:

* **Getting Started** – step-by-step tutorials for service development and deployment
* **API Documentation** – comprehensive JavaDoc and REST API references
* **Service Templates** – pre-built service templates for common use cases
* **Network Monitor** – real-time network status and node connectivity information
* **Debug Console** – tools for testing and debugging services in development and production
* **Settings** – service configuration, node management, security settings, and framework documentation access

## 3. The Functional Scope of the Network Administration System

The solution provides web-based administration interface for managing las2peer P2P networks. Network administrators register through bootstrap nodes and receive administrative privileges.

### 3.1 Authentication Model

* **Network Login** – authentication and authorization process for Network Administrators, requiring administrator credentials and cryptographic certificates for network management access.
* **Certificate Management** – functionality enabling administrators to generate, distribute, and revoke security certificates for network nodes and services.

### 3.2 Network Node Management

Network Administrators access comprehensive node management dashboards. Node lists filter by:

* **Active Nodes** – nodes currently participating in network and available for service hosting
* **Bootstrap Nodes** – special nodes serving as network entry points for new participants
* **Service Nodes** – nodes currently hosting active services
* **Inactive Nodes** – nodes disconnected or temporarily unavailable
* **Quarantined Nodes** – nodes suspected of malicious behavior or security violations

Single node summaries contain:

* Node identifier and network address
* Current status and uptime statistics
* Hosted services list with performance metrics
* Network connectivity and peer relationships
* Resource utilization (CPU, memory, storage)
* Security certificate status and expiration
* Last activity timestamp

Selecting individual nodes displays detailed information including real-time performance metrics, hosted service status, network routing tables, and administrative management controls.

### 3.3 Service Management

Network Administrators view and manage all network-deployed services:

* **Service Registry** – complete deployed service list with metadata
* **Performance Monitoring** – real-time performance metrics and health status
* **Load Balancing** – service request distribution across multiple node instances
* **Version Control** – service version management and rollback capabilities
* **Security Policies** – access control and security rule enforcement

### 3.4 Network Monitoring and Analytics

Administration systems provide comprehensive network analytics:

* **Traffic Analysis** – message flow patterns and network utilization
* **Performance Metrics** – response times, throughput, and error rates
* **Security Events** – authentication attempts, access violations, and threat detection
* **Resource Utilization** – network-wide resource consumption and capacity planning
* **Fault Detection** – automatic detection and alerting of network issues

### 3.5 Service Lifecycle Management

Administrators manage complete service lifecycles:

* **Service Deployment** – approval and deployment of new network services
* **Service Updates** – coordinated updates and version migrations across nodes
* **Service Retirement** – graceful shutdown and removal of deprecated services
* **Rollback Operations** – emergency rollback to previous service versions during issues

## 4. Network Participant Roles and Responsibilities

### 4.1 Service Consumers

Service consumers interact with las2peer networks through:

* **REST API Access** – HTTP-based service consumption through Web Connector
* **Direct P2P Communication** – native protocol communication with service agents
* **WebSocket Connections** – real-time bidirectional communication channels
* **Mobile Applications** – mobile app integration through REST APIs

### 4.2 Node Operators

Node operators maintain network infrastructure by:

* **Node Hosting** – providing computational resources for service execution
* **Network Participation** – maintaining P2P connections and routing messages
* **Resource Sharing** – contributing storage and processing capacity to network
* **Security Compliance** – implementing security policies and threat prevention

### 4.3 Service Providers

Service providers contribute to network ecosystems by:

* **Service Development** – creating and maintaining high-quality services
* **Documentation** – providing comprehensive service documentation and examples
* **Support** – offering technical support and maintenance for deployed services
* **Community Engagement** – participating in las2peer developer community

## 5. Technical Architecture and Infrastructure

### 5.1 Core Framework Components

las2peer framework consists of three primary modules:

* **Core Module** – provides fundamental P2P networking capabilities, agent framework, message handling, security layer, and basic node management functionality.
* **REST Mapper Module** – enables HTTP/REST integration by translating web requests into P2P messages and providing RESTful API access to network-deployed services.
* **Web Connector Module** – offers web server capabilities including static content serving, WebSocket support, and CORS handling for web application integration.

### 5.2 Deployment and Distribution

Framework supports multiple deployment scenarios:

* **Development Environment** – local testing with single or multiple nodes for service development and debugging
* **Private Networks** – closed P2P networks for organizational or project-specific deployments
* **Public Networks** – open networks allowing global participation and service sharing
* **Hybrid Deployments** – mixed environments combining private and public network segments

### 5.3 Security and Trust Model

Security implements multiple layers:

* **Cryptographic Identity** – each agent and node maintains unique cryptographic identity for authentication and message signing
* **Envelope Encryption** – all inter-agent communication encrypts using envelope system
* **Access Control** – service-level permissions and role-based access control for fine-grained security
* **Network Trust** – reputation-based trust mechanisms and Byzantine fault tolerance for network resilience