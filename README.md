# LogAnalyzer v1.0

A terminal-based log analysis tool with **timezone conversion** and **keyword search** support.

---

## Usage & Examples

```bash
loganalyzer                    # Interactive mode
loganalyzer -f <file>          # Analyze a log file
loganalyzer -k <keyword>       # Search for a keyword
loganalyzer -t IST|UTC         # Set target timezone

# Interactive mode (paste logs)
loganalyzer

# Analyze log file (assuming source is UTC)
loganalyzer -f /var/log/syslog -k "error" -s UTC -t IST

# Convert PST logs to IST
loganalyzer -f app.log -s PST -t IST

# Pipe logs from command
tail -f /var/log/app.log | loganalyzer -k "ERROR" -s EST -t UTC
