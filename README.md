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
javac -d out --module-path src src\module-info.java src\com\example\message\Message.java

```
