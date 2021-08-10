# message-module

## Java Modularity
### Window Commands

Current directory

```bash
> tree /f
└───src
    │   module-info.java
    │
    └───com
        └───example
            └───message
                    Message.java
```

Compiling module

```bash
# javac
> javac -d out --module-path src src\module-info.java src\com\example\message\Message.java

```

After that
```bash
> tree /f
├───out
│   │   module-info.class
│   │
│   └───com
│       └───example
│           └───message
│                   Message.class
│
└───src
    │   module-info.java
    │
    └───com
        └───example
            └───message
                    Message.java

```

See module details
```bash
# java --module-path [path of module] -d [name of module]
> java --module-path out -d com.example.message
com.example.message file:///C:/out/
requires java.base mandated
contains com.example.message
```

Executing main class
```bash
# java --module-path [path of module] -m <module>/<mainclass>
> java --module-path out -m com.example.message/com.example.message.Message
Hello World
```
