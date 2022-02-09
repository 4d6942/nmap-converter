# nmap-converter
Python script for converting nmap reports into XLS, a friendly fork of https://github.com/mrschyte/nmap-converter

# Requirements
```bash 
sudo pip install python-libnmap
sudo pip install XlsxWriter
```
or 
```bash 
sudo pip install -r requirements.txt
```

# Usage
```bash
usage: nmap-converter.py [-h] [-o XLS] XML [XML ...]

positional arguments:
  XML                   path to nmap xml report

optional arguments:
  -h, --help            show this help message and exit
  -o XLS, --output XLS  path to xlsx output
```

# Changes
- Forcing use of Python 3.
- Fixed issues I encountered with 'script["output"]'. Implemented try/except to avoid fatal errors.
- Added 'PTR' column in 'Hosts' sheet, hostnames are stored as an array.
