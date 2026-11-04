# JDBC - Java Database Connectivity

It is an API.

It is used to make the Java program interact with DB.

It provides classes and interfaces which are available in the `java.sql` package.

```
+-----------+         +-------------------+         +-------------------+
|           |         |        API        |         |                   |
|   Java    | ------> |       JDBC        | ------> |        DB         |
|           |         |     java.sql      |         |  (RDBMS / SQL)    |
+-----------+         +-------------------+         +-------------------+
```

## Driver Software

* JDBC acts as an abstract layer and the implementation will be provided by driver software.
* It will help to interact with a specific database.
* JDBC is available in Java itself (JDK).
* Driver software is provided by external vendors (providers / third party), so we need to add the driver software manually in our project.

```
                                +-----------------+      +---------------+
                           +--> | Driver Software | ---> | Postgres      |
                           |    +-----------------+      +---------------+
                           |
+-----------+   +--------+ |    +-----------------+      +---------------+
|   Java    |-->|  JDBC  |-+--> | Driver Software | ---> | MySQL         |
+-----------+   +--------+ |    +-----------------+      +---------------+
                (Abstract  |
                 Layer)    |    +-----------------+      +---------------+
                           +--> | Driver Software | ---> | Oracle        |
                                +-----------------+      +---------------+
                               (Implementation Layer)
```