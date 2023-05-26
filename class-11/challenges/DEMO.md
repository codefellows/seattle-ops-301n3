# Ops Challenge - Psutil

- `psutil` stands for "process and system utilities".
- It is a Python library used for system monitoring, resource management, and process control.
- It allows you to retrieve detailed information about running processes, including their CPU and memory usage, process IDs (PIDs), parent-child relationships, process creation time, and termination of processes.
- It enables you to monitor system resources in real-time by providing functions to track CPU utilization, network activity, disk I/O, and process-related metrics.

## Demo Code

The demo code below introduces concepts necessary to complete the challenge.

```python
#!/usr/bin/env python3

# Libraries are imported at the top of any Python script using syntax import [library]
import psutil

# Generate CPU times as a named tuple
print(f"CPU Time: {psutil.cpu_times()}\n")

# Show current CPU consumption
print(f"CPU Percent: {psutil.cpu_percent()}")

```
