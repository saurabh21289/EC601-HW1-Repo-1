# EC601-HW1-Repo

# httpstat

curl statistics made simple.

![screenshot](screenshot.png)


Our update to httpstat is a **single file🌟** Python script just like the original httpstat that has **no dependency👏** and is compatible with **Python 3🍻**. We have made simple changes to how statistics are displayed to the user.


## Installation

There are three ways to get `httpstat`:

- Download the script directly: `wget https://raw.githubusercontent.com/reorx/httpstat/master/httpstat.py`


## Usage

Just pass a url with it:

```bash
python httpstat.py http://www.google.com
```
or to get the https version of the site:

```bash
python httpstat.py https://www.google.com
```

By default it will write response body in a tempfile, but you can let it print out by setting `HTTPSTAT_SHOW_BODY=true`:

```bash
HTTPSTAT_SHOW_BODY=true python httpstat.py httpbin.org/get
```

You can pass any curl supported arguments after the url (except for `-w`, `-D`, `-o`, `-s`, `-S` which are already used by httpstat):

```bash
HTTPSTAT_SHOW_BODY=true python httpstat.py httpbin.org/post -X POST --data-urlencode "a=中文" -v
```
