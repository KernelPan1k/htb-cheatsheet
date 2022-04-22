# Ffuf

| **Command**   | **Description**   |
| --------------|-------------------|
| `ffuf -h` | ffuf help |
| `ffuf -w wordlist.txt:FUZZ -u http://SERVER_IP:PORT/FUZZ` | Directory Fuzzing |
| `ffuf -w wordlist.txt:FUZZ -u http://SERVER_IP:PORT/indexFUZZ` | Extension Fuzzing |
| `ffuf -w wordlist.txt:FUZZ -u http://SERVER_IP:PORT/blog/FUZZ.php` | Page Fuzzing |
| `ffuf -w wordlist.txt:FUZZ -u http://SERVER_IP:PORT/FUZZ -recursion -recursion-depth 1 -e .php -v` | Recursive Fuzzing |
| `ffuf -w wordlist.txt:FUZZ -u https://FUZZ.hackthebox.eu/` | Sub-domain Fuzzing |
| `ffuf -w wordlist.txt:FUZZ -u http://academy.htb:PORT/ -H 'Host: FUZZ.academy.htb' -fs xxx` | VHost Fuzzing |
| `ffuf -w wordlist.txt:FUZZ -u http://admin.academy.htb:PORT/admin/admin.php?FUZZ=key -fs xxx` | Parameter Fuzzing - GET |
| `ffuf -w wordlist.txt:FUZZ -u http://admin.academy.htb:PORT/admin/admin.php -X POST -d 'FUZZ=key' -H 'Content-Type: application/x-www-form-urlencoded' -fs xxx` | Parameter Fuzzing - POST |
| `ffuf -w ids.txt:FUZZ -u http://admin.academy.htb:PORT/admin/admin.php -X POST -d 'id=FUZZ' -H 'Content-Type: application/x-www-form-urlencoded' -fs xxx` | Value Fuzzing |  
| `wfuzz -z file,/path/to/wordlist.txt -u http://127.0.0.1:80/site/FUZZ` | Fuzz using a wordlist                   |
| `wfuzz -z file,/path/to/user.txt -z file,/path/to/pass.txt http://127.0.0.1/login.php -d "user=FUZZ&pass=FUZ2Z"` | Fuzz using POST method and two wordlists |
| `wfuzz -H Foo:FUZZ`                                          | Fuzz header                             |
| `-X GET , -X POST`                                           | Choose method                           |


# Wordlists

| **Command**   | **Description**   |
| --------------|-------------------|
| `SecLists/Discovery/Web-Content/directory-list-2.3-small.txt` | Directory/Page Wordlist |
| `SecLists/Discovery/Web-Content/web-extensions.txt` | Extensions Wordlist |
| `SecLists/Discovery/DNS/subdomains-top1million-5000.txt` | Domain Wordlist |
| `SecLists/Discovery/Web-Content/burp-parameter-names.txt` | Parameters Wordlist |


# Grep

| **Command**   | **Description**   |
| --------------|-------------------|
| `grep '[[:classname:]]' file.txt` | Find strings that contain a given class. Classes are: [[:graph:]], [[:lower:]], [[:print:]], [[:punct:]], [[:space:]], [[:upper:]], and [[:xdigit:]] |
| `grep -x '.\{123\}'`              | Find strings with length of 123   |

