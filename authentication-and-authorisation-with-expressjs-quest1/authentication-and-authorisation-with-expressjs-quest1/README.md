# README

## File Structure

```
.
├── back-end
│   ├── app.js
│   ├── controllers
│   │   └── authController.js
│   ├── models
│   │   └── UserModel.js
│   ├── package.json
│   ├── package-lock.json
│   ├── README.md
│   ├── routes
│   │   └── authHandling.js
│   ├── service
│   │   ├── database
│   │   │   └── db.js
│   │   └── security
│   │       └── authentication.js
│   └── utils
│       └── helper.js
└── web-front-end
    ├── index.html
    ├── js
    │   └── scripts.js
    ├── pages
    │   ├── profile.html
    │   └── register.html
    ├── README.md
    └── styles
        └── styles.css

13 directories, 16 files
```




## Where to read first?

There is no given order to read through each directory. However, we do recommend this flowchart to know how interconnected they are.

```mermaid
flowchart RL
subgraph g1[back-end]
service --> database
service --> security
security <-.-> controllers
utils <--> database --> models
controllers .-> routes
end
subgraph f1[web-front-end]
index.html --> pages
pages <-.-> js
index.html <-.-> js
end
routes <--> js
```
