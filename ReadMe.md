

##  las2peer Core Modules Summary

| **Component**                   | **Purpose**                                                       | **Key Role / Interaction**                                                                      |
| ------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| **P2P Node** \[1]               | Hosts agents, manages messaging and DHT storage using FreePastry. | Routes messages, stores data, connects agents and services.                                     |
| **Agents** \[2]\[3]             | Represent users or services with cryptographic identities.        | Authenticate, sign messages, and encapsulate services (e.g., `UserAgent`, `ServiceAgent`).      |
| **Service Runtime** \[4]        | Runs microservices via agents and thread pools.                   | Executes service methods on request; uses execution context and message routing.                |
| **Distributed Storage** \[5]    | Encrypted, versioned DHT storage (via FreePastry Past).           | Shared storage for agents and services; secure and decentralized.                               |
| **Connectors** \[6]             | External interfaces (HTTP, WebSocket, etc.) into the P2P network. | Forwards client requests to services; interacts with Node and Security modules.                 |
| **REST Mapper** \[6]            | Maps HTTP requests to annotated service methods.                  | Works with Web Connector to dispatch REST calls into service logic.                             |
| **Web Connector** \[6]          | Built-in HTTP server and REST gateway.                            | Handles REST API calls, exposes services to the web, includes REST Mapper and session handling. |
| **Security Layer** \[2]\[3]     | Manages encryption, signing, agent unlock, message integrity.     | Ensures all messages and storage are securely processed and verified.                           |
| **Class Loader / Sandbox** \[4] | Securely loads service JARs with limited permissions.             | Enforces isolation for services; prevents unauthorized access or execution.                     |

---

## 🔗 References

* \[1] [Node.java API](http://rwth-acis.github.io/las2peer/latest/core/i5/las2peer/p2p/Node.html)
* \[2] [Agent Security Package](http://rwth-acis.github.io/las2peer/latest/core/i5/las2peer/api/security/package-summary.html)
* \[3] [ServiceAgent API](http://rwth-acis.github.io/las2peer/latest/core/i5/las2peer/api/security/package-summary.html#:~:text=ServiceAgent)
* \[4] [Service API Overview](http://rwth-acis.github.io/las2peer/latest/core/i5/las2peer/api/package-summary.html)
* \[5] [Concepts - DHT Storage](https://github.com/rwth-acis/las2peer/wiki/Concepts-Overview#:~:text=Freepastry%20provides%20a%20key%20value)
* \[6] [Connectors Overview](https://github.com/rwth-acis/las2peer/wiki/Concepts-Overview#:~:text=Connector)

---

