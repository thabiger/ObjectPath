ObjectPath
==========

[Fork and packaging notice]
---------------------------

This fork exists solely to publish installable packages to PyPI under `tha-objectpath` for the original ObjectPath project, which no longer publishes releases. It aims to provide packaging and distribution only; it does not attempt full-featured development or ongoing maintenance of the codebase. Upstream development remains with the original project by Adrian Kalbarczyk.

[![PyPI - Version](https://img.shields.io/pypi/v/tha-objectpath.svg)](https://pypi.org/project/tha-objectpath/)
[![PyPI - Downloads](https://img.shields.io/pypi/dm/tha-objectpath.svg)](https://pypi.org/project/tha-objectpath/)
[![CI](https://github.com/thabiger/ObjectPath/actions/workflows/ci.yml/badge.svg)](https://github.com/thabiger/ObjectPath/actions/workflows/ci.yml)

The agile NoSQL query language for semi-structured data
-----------------------------------------------

**#Python #NoSQL #Javascript #JSON #nested-array-object**

ObjectPath is a query language similar to XPath or JSONPath, but much more powerful thanks to embedded arithmetic calculations, comparison mechanisms and built-in functions. This makes the language more like SQL in terms of expressiveness, but it works over JSON documents rather than relations. ObjectPath can be considered a full-featured expression language. Besides selector mechanism there is also boolean logic, type system and string concatenation available. On top of that, the language implementations (Python at the moment; Javascript is in beta!) are secure and relatively fast.

More at [ObjectPath site](https://adriank.github.io/ObjectPath/)

![ObjectPath img](http://adriank.github.io/ObjectPath/img/op-colors.png)

ObjectPath makes it easy to find data in big nested JSON documents. It borrows the best parts from E4X, JSONPath, XPath and SQL. ObjectPath is to JSON documents what XPath is to XML. Other examples to ilustrate this kind of relationship are:

| Scope  | Language |
|---|---|
| text documents  | regular expression  |
| XML  | XPath  |
| HTML  | CSS selectors  |
| JSON documents | ObjectPath |

Documentation
-------------

[ObjectPath Reference](https://adriank.github.io/ObjectPath/reference.html)

Command line usage
-----

`````sh
$ sudo pip install tha-objectpath
$ objectpath file.json
`````
or
`````sh
$ git clone https://github.com/adriank/ObjectPath.git
$ cd ObjectPath
$ python shell.py file.json
`````

Python usage
----------------

`````sh
$ sudo pip install tha-objectpath
$ python
>>> from objectpath import *
>>> tree=Tree({"a":1})
>>> tree.execute("$.a")
1
>>>
`````

`````sh
$ git clone https://github.com/adriank/ObjectPath.git
$ cd ObjectPath
$ python
>>> from objectpath import *
>>> tree=Tree({"a":1})
>>> tree.execute("$.a")
1
>>>
`````

CI/CD Configuration
-------------------

The CI pipeline includes quality checks (black, isort, flake8, mypy) and security scans (safety, bandit). You can disable these jobs using GitHub repository variables:

**To skip quality checks:**
1. Go to your repository → Settings → Secrets and variables → Actions
2. Click "Variables" tab → "New repository variable"
3. Name: `SKIP_QUALITY`, Value: `true`
4. The quality checks job will be skipped in all CI runs

**To skip security scans:**
1. Follow the same steps as above
2. Name: `SKIP_SECURITY`, Value: `true`
3. The security scans job will be skipped in all CI runs

Contributing & bugs
-------------------

I appreciate all contributions and bugfix requests for ObjectPath, however since I don't code in Python anymore, this library is not maintained as of now. Since I can't fully assure that code contributed by others meets quality standards, I can't accept PRs. 

If you feel you could maintain this code, ping me. I'd be more than happy to transfer this repo to a dedicated ObjectPath organization on GitHub and give the ownership to someone with more time for this project than me.

License
-------

**MIT**
