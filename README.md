# authentication-and-authorisation-with-expressjs


								flowchart RL
```mermaid
graph TD;
  flowchart RL
subgraph g1[back-end]
service --> database
service --> security
security <-.-> controllers
utils <--> database --> models
utils <--> controllers
controllers .-> routes
end
subgraph f1[web-front-end]
index.html --> pages
pages <-.-> js
index.html <-.-> js
end
routes <--> js

```
