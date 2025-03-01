# Data flow in Link-Up


## Testing for client-server connection

I set this data flow to check if frontend is sucessfully connected with backend on deployment

```mermaid
flowchart TD
    start --> C
    D --> A
    subgraph Frontend
        start
        A["console.log(#quot;Connected to server#quot;)"]
    end
    subgraph Backend
        C["on.connection"]
        D["socket.emit(#quot;CTS#quot;)"]
        C --> D
    end
```
These all need to be connected together

---
