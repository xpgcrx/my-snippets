---
Title: mmdblookup Cheatsheet
Description: |
  A cheat sheet for the mmdblookup command to look up IP addresses in a MaxMind DB file.

  https://maxmind.github.io/libmaxminddb/mmdblookup.html
Tags:
  - linux
  - network
---

```bash
# Basic usage
mmdblookup --file /path/to/database.mmdb --ip 1.2.3.4

# Look up a specific field
mmdblookup -f /path/to/database.mmdb -i 1.2.3.4 country iso_code

# Verbose mode
mmdblookup -f /path/to/database.mmdb -i 1.2.3.4 --verbose
```
