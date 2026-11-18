# Linux Server Health Check & Shell Automation Toolkit

A Linux system monitoring and automation toolkit built with Bash and Python. It helps monitor system resources, check service health, manage logs, and generate daily reports.

## Overview

This toolkit provides automated checks for important Linux server health metrics. It collects monitoring results in structured JSONL files and generates readable Markdown reports.

## Features

- **Disk Monitoring:** Checks disk usage against configurable warning and critical thresholds.
- **Memory Monitoring:** Tracks RAM and swap usage.
- **Service Monitoring:** Checks whether configured systemd services are active.
- **Log Rotation:** Compresses and manages older log files.
- **Automated Reporting:** Generates daily Markdown health reports using Python.
- **Scheduled Execution:** Supports daily execution through cron.
- **Structured Logging:** Stores monitoring results in JSONL format.

## Technology Stack

- Bash / Shell Scripting
- Python 3
- Linux
- systemd
- Cron
- JSONL

## Project Structure

```text
linux-server-health-toolkit/
├── config/
├── cron/
├── logs/
├── python/
├── reports/
├── sample_output/
├── scripts/
│   └── lib/
├── install.sh
├── README.md
└── LICENSE
```

## Configuration

Monitoring thresholds and service names can be configured in:

`config/health_check.conf`

Default configuration includes:
- Disk warning threshold: 75%
- Disk critical threshold: 90%
- Memory warning threshold: 80%
- Memory critical threshold: 95%
- Swap warning threshold: 50%

## Requirements

- Linux operating system
- Bash
- Python 3
- Standard Linux utilities
- systemd for service monitoring
- Cron (optional, for scheduled execution)

## Usage

Make the scripts executable:

```bash
chmod +x install.sh
```

Run the setup script:

```bash
./install.sh
```

Run all health checks:

```bash
./scripts/run_all_checks.sh
```

Generate a daily report:

```bash
python3 python/generate_report.py
```

## Output

The toolkit stores:
- Monitoring data in `logs/data/`
- Daily reports in `reports/`
- Execution logs for troubleshooting

## Maintainer

**Shubham Yadav**

GitHub: [Shubham7soft](https://github.com/Shubham7soft)


