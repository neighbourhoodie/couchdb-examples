# Neighbourhoodie Examples

These are example CouchDB database(s), styled after the examples used in the
[CouchDB documentation](https://docs.couchdb.org/).

It is a companion repository for [Neighbourhoodie](https://neighbourhood.ie)'s
CouchDB Training offerings.

## Installation Instructions

These instructions assume you already have a CouchDB installation on your local
machine, and that it is running in the background.

1. Install [Node.js](https://nodejs.org/). Any recent version (as of 2021) is
   fine.
1. Obtain a copy of this repository, using `git` or by downloading the zip file
   from GitHub and extracting it.
1. Open a shell, terminal, or command prompt, and change directories into
   wherever you put a copy of this repo.
1. Install the example by typing: `npx couchdb-bootstrap
   http://admin:password@localhost:5984' .` substituting your CouchDB username
   and password for `admin` and `password`.

## Helpful Hints on Windows computers

### Command Prompt

These documents have UTF-8 contents. If you are running on Microsoft Windows,
output may appear mangled by default. To correct this, type:

```batch
chcp 65001
```

before working with these examples.

When running `curl.exe` commands using the Command Prompt, be sure to surround
any inline documents with *double-quotes* (`"`) and to double up any double-
quotes inside of the string, like this:

```batch
curl -X POST -H "Content-Type:application/json" http://admin:password@localhost:5984/ghibli/_find -d '{""selector"":{""type"": ""director""}}'
```

### PowerShell

These documents have UTF-8 contents. If you are running on Microsoft Windows,
output may appear mangled by default. To correct this, type:

```powershell
$OutputEncoding = [Console]::OutputEncoding = [Text.UTF8Encoding]::UTF8
```

before working with these examples.

When running `curl.exe` commands using the Command Prompt, be sure to surround
any inline documents with *single-quotes* (`'`) and to double up any double-
quotes inside of the string, like this:

```powershell
curl.exe -s -X POST -H "Content-Type:application/json" http://admin:password@localhost:5984/ghibli/_find -d '{""selector"":{""type"": ""director""}}'
```

Be sure to use `curl.exe` and not the built-in PowerShell `curl` command, as
the syntax is significantly different from that used in the course.

It is also recommended to use the `-s` option to `curl.exe` to prevent its
progress bar output from confusing PowerShell.
