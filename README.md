# crossdomainScanner
Python tool to check for expired domains still allowed in crossdomain.xml files.

## Installation
```
~$ sudo apt install whois
~$ git clone https://github.com/JacobReynolds/crossdomainScanner.git
~$ cd crossdomainScanner
~$ pip install -r requirements.txt
[follow the example below for runtime usage]
```
## Example:

```
~$ python scraper.py https://jakereynolds.co -v -o output.txt
~$ cat output.txt
Searching crossdomain.xml on https://jakereynolds.co for unregistered domains

=============================================================

Crossdomain contents:
 - thishaskjwfkjansvkjwng.com
 - testing.com
 - msnbciweb

Possible expired domains:
thishaskjwfkjansvkjwng.com
```

This means that https://jakereynolds.co allows http://thishaskjwfkjansvkjwng.com in their crossdomain.xml file.  However, the latter is not registered to any DNS.  An attacker could now buy that domain and get full cross-domain access to https://jakereynolds.co

This tool is created for Ethical Hacking purposes, any illicit use is not related to its creator.

Currently undergoing development
