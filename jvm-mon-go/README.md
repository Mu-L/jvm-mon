# jvm-mon

JVM monitoring from the terminal (cpu, memory, threads).
Supports monitoring application running on Java 8 and newer.

- Single Go executable
- Contains embedded Java agent that gets loaded into monitored application
- Does not require a JDK to run

# Usage

To monitor JVMs started with your username:

`./jvm-mon-go`

### Troubleshooting

See the log at `/tmp/jvm-mon_(user).log`

# Build from source

Prerequisites:
- Go (at least 1.18)
- JDK 8+ for building java agent

1. Build everything: `./build.sh`
2. `./run.sh`: 

# How it works

jvm-mon attaches to a running JVM you select and loads an agent.jar into the process.
They communicate via a socket to send/receive JVM metrics in json format.

# Development

Run jvm-mon from Go sources: `./run.sh`

See `log` file for debugging output
