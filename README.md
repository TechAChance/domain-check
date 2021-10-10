# domain-check

version 2.0

A bash script to check which tld's a particular domain is available under.

## Installation

```bash
# Go to where you want to put the files
cd /opt #(or ~/bin or wherever you want to drop these files)

# copy the filez
git clone https://github.com/BGundlach/domain-check.git

# link files to your PATH
ln -sT domain-check/dmnchk ~/bin/dmnchk # assuming ~/bin is in your $PATH
```

##Usage##

```
USAGE:
  dmnchk [options] domains(without tld extentions)

EXAMPLE:
  dmnchk purple

Sample Output:
  purple.com : AVAILABLE
  purple.net : TAKEN (from: Go Daddy, LLC)
  purple.ac  : UNKNOWN
 etc.

OPTIONS:
  -l list all tlds
  -a search all (include every tld)
  -i display available results only
  -s output as csv
  -h display this help message
```

##To Do##
Separate Generic and Country Code TLDs
accept domains with tlds
