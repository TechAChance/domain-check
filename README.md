# domain-check

version 2.0

A bash script to check which tld's a particular domain is available under.
Thgis is a fork from https://github.com/BGundlach/domain-check.git

## Installation

```bash
# Go to where you want to put the files
cd /opt #(or ~/bin or wherever you want to drop these files)
# copy the files
git clone https://github.com/TechAChance/domain-check
# [OPTIONAL] link files to your PATH
ln -sT domain-check/dmnchk ~/bin/dmnchk # assuming ~/bin is in your $PATH
```

##Usage##

```
USAGE:
  dmnchk [options] [domain (without tld extentions)]

OPTIONS:
  -l : list tlds (no check of availability)
  -a : all tlds, not only most common
  -i : display 'available' domains only
  -s : output as csv instead of text
  -h : display this help message

 With no option, the tool will check most common tlds.

EXAMPLES:
 * list most common extension                      : dmnchk -l
 * list all existing extensions                    : dmnchk -l -a
 * check most common extension for domain 'mydom'  : dmnchk mydom
 * check all existing extensions for domain 'mydom': dmnchk -a mydom

Sample Output:
  ...
  mydom.biz               : AVAILABLE
  mydom.blog              : AVAILABLE
  mydom.cc                : TAKEN (from: Key-Systems GmbH)
  mydom.cloud             : TAKEN (from: Tucows Domains Inc.)
  mydom.com               : TAKEN (from: Gabia, Inc.)
  mydom.company           : AVAILABLE
  mydom.dev               : AVAILABLE
  mydom.digital           : AVAILABLE
  mydom.eu                : TAKEN (from: Realtime Register B.V.)
  mydom.expert            : AVAILABLE
  mydom.fr                : TAKEN (from: GANDI)
  mydom.global            : AVAILABLE
  mydom.group             : AVAILABLE
  mydom.in                : AVAILABLE
  mydom.info              : TAKEN (from: GoDaddy.com, LLC)
  ...
```

##To Do##

- Separate Generic and Country Code TLDs
- accept domains with tlds
