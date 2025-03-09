| benchmark | collect-stats | linux-x86_64 |
| --- | --- | --- |
| aiohttp |  | [[default run]](#aiohttp-on-linux-x86_64-default) |
| chameleon | [[pystats run]](#chameleon-on-collect-stats-pystats) | [[default run]](#chameleon-on-linux-x86_64-default) |
| djangocms | [[pystats build]](#djangocms-on-collect-stats-pystats) | [[default build]](#djangocms-on-linux-x86_64-default) |
| flaskblogging | [[pystats run]](#flaskblogging-on-collect-stats-pystats) | [[default run]](#flaskblogging-on-linux-x86_64-default) |
| gevent_hub | [[pystats run]](#gevent_hub-on-collect-stats-pystats) | [[default run]](#gevent_hub-on-linux-x86_64-default) |
| gunicorn | [[pystats run]](#gunicorn-on-collect-stats-pystats) | [[default run]](#gunicorn-on-linux-x86_64-default) |
| html5lib |  | [[default run]](#html5lib-on-linux-x86_64-default) |
| kinto | [[pystats run]](#kinto-on-collect-stats-pystats) | [[default build]](#kinto-on-linux-x86_64-default) |
| mypy2 | [[pystats build]](#mypy2-on-collect-stats-pystats) | [[default build]](#mypy2-on-linux-x86_64-default) |
| pytorch_alexnet_inference | [[pystats build]](#pytorch_alexnet_inference-on-collect-stats-pystats) | [[default build]](#pytorch_alexnet_inference-on-linux-x86_64-default) |
| tornado_http | [[pystats run]](#tornado_http-on-collect-stats-pystats) | [[default run]](#tornado_http-on-linux-x86_64-default) |
## aiohttp on linux-x86_64 default

<details>
<summary>Log for aiohttp on linux-x86_64 default</summary>

```
# /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/bin/python -u /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_aiohttp/run_benchmark.py --inherit-environ PYTHON_JIT,PYPERFORMANCE_RUNID --output /tmp/tmps7vq8aeb
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_aiohttp/run_benchmark.py", line 69, in <module>
    with context:
         ^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/contextlib.py", line 141, in __enter__
    return next(self.gen)
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_aiohttp/netutils.py", line 36, in serving
    waitUntilUp(addr)
    ~~~~~~~~~~~^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_aiohttp/netutils.py", line 66, in waitUntilUp
##[error]    raise Exception('Timeout reached when trying to connect')
Exception: Timeout reached when trying to connect
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
             ^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
            ^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 240, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Command failed with exit code 1
```

</details>

## chameleon on linux-x86_64 default

<details>
<summary>Log for chameleon on linux-x86_64 default</summary>

```
# /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/bin/python -u /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_chameleon/run_benchmark.py --inherit-environ PYTHON_JIT,PYPERFORMANCE_RUNID --output /tmp/tmp_gjn9ocr
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_chameleon/run_benchmark.py", line 5, in <module>
    from chameleon import PageTemplate
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/__init__.py", line 1, in <module>
    from .zpt.template import PageTemplate
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/zpt/template.py", line 6, in <module>
    from ..tales import PythonExpr
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/tales.py", line 27, in <module>
    from .compiler import Interpolator
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/compiler.py", line 34, in <module>
    from .tal import ErrorInfo
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/tal.py", line 26, in <module>
    from chameleon import interfaces
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/interfaces.py", line 1, in <module>
    from zope.interface import Interface
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/__init__.py", line 58, in <module>
    _wire()
    ~~~~~^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interface.py", line 1154, in _wire
    from zope.interface.interfaces import IElement
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interfaces.py", line 56, in <module>
    class IElement(Interface):
    ...<93 lines>...
            """
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interface.py", line 794, in __init__
    self.__attrs = self.__compute_attrs(attrs)
                   ~~~~~~~~~~~~~~~~~~~~^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interface.py", line 813, in __compute_attrs
    aname: update_value(aname, aval)
           ~~~~~~~~~~~~^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interface.py", line 809, in update_value
    raise InvalidInterface("Concrete attribute, " + aname)
zope.interface.exceptions.InvalidInterface: Concrete attribute, __classdictcell__
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
             ^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
            ^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 240, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Command failed with exit code 1
```

</details>

## chameleon on collect-stats pystats

<details>
<summary>Log for chameleon on collect-stats pystats</summary>

```
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/template.py", line 137, in __init__
    self.write(body)
    ~~~~~~~~~~^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/template.py", line 235, in write
    self.cook(body)
    ~~~~~~~~~^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/template.py", line 167, in cook
    program = self._cook(body, digest, names)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/template.py", line 245, in _cook
    source = self._compile(body, builtins)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/template.py", line 276, in _compile
    program = self.parse(body)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/zpt/template.py", line 227, in parse
    return MacroProgram(
        body, self.mode, self.filename,
    ...<9 lines>...
        tokenizer=self.tokenizer
    )
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/zpt/program.py", line 174, in __init__
    super(MacroProgram, self).__init__(*args, **kwargs)
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/program.py", line 35, in __init__
    node = self.visit(kind, args)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/program.py", line 41, in visit
    return visitor(*args)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/zpt/program.py", line 320, in visit_element
    ATTRIBUTES = self._create_attributes_nodes(
        prepared, I18N_ATTRIBUTES, STATIC_ATTRIBUTES,
    )
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/zpt/program.py", line 794, in _create_attributes_nodes
    default = ast.Str(s=text) if text is not None else None
              ^^^^^^^
AttributeError: module 'ast' has no attribute 'Str'
Traceback (most recent call last):
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
             ^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
            ^^^^^^^^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 240, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Command failed with exit code 1

ERROR: No benchmark was run
Python benchmark suite 1.11.0


==================================================
```

</details>

## djangocms on linux-x86_64 default

<details>
<summary>Log for djangocms on linux-x86_64 default</summary>

```
  Using cached django_sekizai-4.1.0-py3-none-any.whl.metadata (4.6 kB)
Collecting django-treebeard==4.7.1
  Using cached django_treebeard-4.7.1-py3-none-any.whl.metadata (2.7 kB)
Collecting djangocms-admin-style==3.3.1
  Using cached djangocms_admin_style-3.3.1-py3-none-any.whl.metadata (10 kB)
Collecting djangocms-alias==2.0.1
  Using cached djangocms_alias-2.0.1-py3-none-any.whl.metadata (3.7 kB)
Collecting djangocms-attributes-field==3.0.0
  Using cached djangocms_attributes_field-3.0.0-py3-none-any.whl.metadata (7.7 kB)
Collecting djangocms-frontend==1.3.4
  Using cached djangocms_frontend-1.3.4-py3-none-any.whl.metadata (9.3 kB)
Collecting djangocms-text-ckeditor==5.1.6
  Using cached djangocms_text_ckeditor-5.1.6-py3-none-any.whl.metadata (21 kB)
Collecting djangocms-versioning==2.0.2
  Using cached djangocms_versioning-2.0.2-py3-none-any.whl.metadata (4.1 kB)
Collecting easy-thumbnails==2.10
  Using cached easy_thumbnails-2.10-py3-none-any.whl.metadata (15 kB)
Collecting html5lib==1.1
  Using cached html5lib-1.1-py2.py3-none-any.whl.metadata (16 kB)
Collecting idna==3.10
  Using cached idna-3.10-py3-none-any.whl.metadata (10 kB)
Collecting lxml==5.3.0
  Using cached lxml-5.3.0.tar.gz (3.7 MB)
  Installing build dependencies: started
  Installing build dependencies: finished with status 'done'
  Getting requirements to build wheel: started
  Getting requirements to build wheel: finished with status 'error'
  error: subprocess-exited-with-error
  
  × Getting requirements to build wheel did not run successfully.
  │ exit code: 1
  ╰─> [4 lines of output]
      <string>:67: DeprecationWarning: pkg_resources is deprecated as an API. See https://setuptools.pypa.io/en/latest/pkg_resources.html
      Building lxml version 5.3.0.
      Building without Cython.
      Error: Please make sure the libxml2 and libxslt development packages are installed.
      [end of output]
  
  note: This error originates from a subprocess, and is likely not a problem with pip.
error: subprocess-exited-with-error

× Getting requirements to build wheel did not run successfully.
│ exit code: 1
╰─> See above for output.

note: This error originates from a subprocess, and is likely not a problem with pip.
Command failed with exit code 1


==================================================
```

</details>

## djangocms on collect-stats pystats

<details>
<summary>Log for djangocms on collect-stats pystats</summary>

```
Collecting django-sekizai==4.1.0
  Using cached django_sekizai-4.1.0-py3-none-any.whl.metadata (4.6 kB)
Collecting django-treebeard==4.7.1
  Using cached django_treebeard-4.7.1-py3-none-any.whl.metadata (2.7 kB)
Collecting djangocms-admin-style==3.3.1
  Using cached djangocms_admin_style-3.3.1-py3-none-any.whl.metadata (10 kB)
Collecting djangocms-alias==2.0.1
  Using cached djangocms_alias-2.0.1-py3-none-any.whl.metadata (3.7 kB)
Collecting djangocms-attributes-field==3.0.0
  Using cached djangocms_attributes_field-3.0.0-py3-none-any.whl.metadata (7.7 kB)
Collecting djangocms-frontend==1.3.4
  Using cached djangocms_frontend-1.3.4-py3-none-any.whl.metadata (9.3 kB)
Collecting djangocms-text-ckeditor==5.1.6
  Using cached djangocms_text_ckeditor-5.1.6-py3-none-any.whl.metadata (21 kB)
Collecting djangocms-versioning==2.0.2
  Using cached djangocms_versioning-2.0.2-py3-none-any.whl.metadata (4.1 kB)
Collecting easy-thumbnails==2.10
  Using cached easy_thumbnails-2.10-py3-none-any.whl.metadata (15 kB)
Collecting html5lib==1.1
  Using cached html5lib-1.1-py2.py3-none-any.whl.metadata (16 kB)
Collecting idna==3.10
  Using cached idna-3.10-py3-none-any.whl.metadata (10 kB)
Collecting lxml==5.3.0
  Using cached lxml-5.3.0.tar.gz (3.7 MB)
  Installing build dependencies: started
  Installing build dependencies: finished with status 'done'
  Getting requirements to build wheel: started
  Getting requirements to build wheel: finished with status 'error'
  error: subprocess-exited-with-error
  
  × Getting requirements to build wheel did not run successfully.
  │ exit code: 1
  ╰─> [4 lines of output]
      <string>:67: DeprecationWarning: pkg_resources is deprecated as an API. See https://setuptools.pypa.io/en/latest/pkg_resources.html
      Building lxml version 5.3.0.
      Building without Cython.
      Error: Please make sure the libxml2 and libxslt development packages are installed.
      [end of output]
  
  note: This error originates from a subprocess, and is likely not a problem with pip.
error: subprocess-exited-with-error

× Getting requirements to build wheel did not run successfully.
│ exit code: 1
╰─> See above for output.

note: This error originates from a subprocess, and is likely not a problem with pip.
Command failed with exit code 1


```

</details>

## flaskblogging on linux-x86_64 default

<details>
<summary>Log for flaskblogging on linux-x86_64 default</summary>

```
# /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/bin/python -u /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_flaskblogging/run_benchmark.py --inherit-environ PYTHON_JIT,PYPERFORMANCE_RUNID --output /tmp/tmp8rlp21bf
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_flaskblogging/run_benchmark.py", line 76, in <module>
    with context:
         ^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/contextlib.py", line 141, in __enter__
    return next(self.gen)
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_flaskblogging/netutils.py", line 36, in serving
    waitUntilUp(addr)
    ~~~~~~~~~~~^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_flaskblogging/netutils.py", line 66, in waitUntilUp
##[error]    raise Exception('Timeout reached when trying to connect')
Exception: Timeout reached when trying to connect
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
             ^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
            ^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 240, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Command failed with exit code 1
```

</details>

## flaskblogging on collect-stats pystats

<details>
<summary>Log for flaskblogging on collect-stats pystats</summary>

```
# /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/bin/python -u /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_flaskblogging/run_benchmark.py --inherit-environ PYPERFORMANCE_RUNID,PYTHON_JIT --hook=pystats --loops=32 --output /tmp/tmpjaktsnnu
Traceback (most recent call last):
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_flaskblogging/run_benchmark.py", line 76, in <module>
    with context:
         ^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/contextlib.py", line 141, in __enter__
    return next(self.gen)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_flaskblogging/netutils.py", line 36, in serving
    waitUntilUp(addr)
    ~~~~~~~~~~~^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_flaskblogging/netutils.py", line 66, in waitUntilUp
##[error]    raise Exception('Timeout reached when trying to connect')
Exception: Timeout reached when trying to connect
Traceback (most recent call last):
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
             ^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
            ^^^^^^^^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 240, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Command failed with exit code 1

ERROR: No benchmark was run
Python benchmark suite 1.11.0


==================================================
```

</details>

## gevent_hub on linux-x86_64 default

<details>
<summary>Log for gevent_hub on linux-x86_64 default</summary>

```
    import gevent
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/gevent/__init__.py", line 71, in <module>
    from gevent._config import config
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/gevent/_config.py", line 730, in <module>
    Loop().get()
    ~~~~~~~~~~^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/gevent/_config.py", line 151, in get
    self.value = self.validate(self._default())
                 ~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/gevent/_config.py", line 259, in validate
    return self._import_one_of([self.shortname_map.get(x, x) for x in value])
           ~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/gevent/_config.py", line 230, in _import_one_of
    return self._import_one(item)
           ~~~~~~~~~~~~~~~~^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/gevent/_config.py", line 248, in _import_one
    module = importlib.import_module(module)
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/importlib/__init__.py", line 88, in import_module
    return _bootstrap._gcd_import(name[level:], package, level)
           ~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "src/gevent/libev/corecext.pyx", line 819, in init gevent.libev.corecext
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/__init__.py", line 58, in <module>
    _wire()
    ~~~~~^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interface.py", line 1154, in _wire
    from zope.interface.interfaces import IElement
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interfaces.py", line 56, in <module>
    class IElement(Interface):
    ...<93 lines>...
            """
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interface.py", line 794, in __init__
    self.__attrs = self.__compute_attrs(attrs)
                   ~~~~~~~~~~~~~~~~~~~~^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interface.py", line 813, in __compute_attrs
    aname: update_value(aname, aval)
           ~~~~~~~~~~~~^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interface.py", line 809, in update_value
    raise InvalidInterface("Concrete attribute, " + aname)
zope.interface.exceptions.InvalidInterface: Concrete attribute, __classdictcell__
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
             ^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
            ^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 240, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Command failed with exit code 1
```

</details>

## gevent_hub on collect-stats pystats

<details>
<summary>Log for gevent_hub on collect-stats pystats</summary>

```
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/gevent/_config.py", line 151, in get
    self.value = self.validate(self._default())
                 ~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/gevent/_config.py", line 259, in validate
    return self._import_one_of([self.shortname_map.get(x, x) for x in value])
           ~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/gevent/_config.py", line 230, in _import_one_of
    return self._import_one(item)
           ~~~~~~~~~~~~~~~~^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/gevent/_config.py", line 248, in _import_one
    module = importlib.import_module(module)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/importlib/__init__.py", line 88, in import_module
    return _bootstrap._gcd_import(name[level:], package, level)
           ~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "src/gevent/libev/corecext.pyx", line 819, in init gevent.libev.corecext
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/__init__.py", line 58, in <module>
    _wire()
    ~~~~~^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interface.py", line 1154, in _wire
    from zope.interface.interfaces import IElement
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interfaces.py", line 56, in <module>
    class IElement(Interface):
    ...<93 lines>...
            """
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interface.py", line 794, in __init__
    self.__attrs = self.__compute_attrs(attrs)
                   ~~~~~~~~~~~~~~~~~~~~^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interface.py", line 813, in __compute_attrs
    aname: update_value(aname, aval)
           ~~~~~~~~~~~~^^^^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interface.py", line 809, in update_value
    raise InvalidInterface("Concrete attribute, " + aname)
zope.interface.exceptions.InvalidInterface: Concrete attribute, __classdictcell__
Traceback (most recent call last):
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
             ^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
            ^^^^^^^^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 240, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Command failed with exit code 1

ERROR: No benchmark was run
Python benchmark suite 1.11.0


==================================================
```

</details>

## gunicorn on linux-x86_64 default

<details>
<summary>Log for gunicorn on linux-x86_64 default</summary>

```
# /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/bin/python -u /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_gunicorn/run_benchmark.py --inherit-environ PYTHON_JIT,PYPERFORMANCE_RUNID --output /tmp/tmpczl10rye
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_gunicorn/run_benchmark.py", line 84, in <module>
    with context:
         ^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/contextlib.py", line 141, in __enter__
    return next(self.gen)
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_gunicorn/netutils.py", line 36, in serving
    waitUntilUp(addr)
    ~~~~~~~~~~~^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_gunicorn/netutils.py", line 66, in waitUntilUp
##[error]    raise Exception('Timeout reached when trying to connect')
Exception: Timeout reached when trying to connect
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
             ^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
            ^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 240, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Command failed with exit code 1
```

</details>

## gunicorn on collect-stats pystats

<details>
<summary>Log for gunicorn on collect-stats pystats</summary>

```
# /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/bin/python -u /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_gunicorn/run_benchmark.py --inherit-environ PYPERFORMANCE_RUNID,PYTHON_JIT --hook=pystats --loops=128 --output /tmp/tmpfu9qvugf
Traceback (most recent call last):
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_gunicorn/run_benchmark.py", line 84, in <module>
    with context:
         ^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/contextlib.py", line 141, in __enter__
    return next(self.gen)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_gunicorn/netutils.py", line 36, in serving
    waitUntilUp(addr)
    ~~~~~~~~~~~^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_gunicorn/netutils.py", line 66, in waitUntilUp
##[error]    raise Exception('Timeout reached when trying to connect')
Exception: Timeout reached when trying to connect
Traceback (most recent call last):
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
             ^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
            ^^^^^^^^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 240, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Command failed with exit code 1

ERROR: No benchmark was run
Python benchmark suite 1.11.0


==================================================
```

</details>

## html5lib on linux-x86_64 default

<details>
<summary>Log for html5lib on linux-x86_64 default</summary>

```
# /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-a0818d2ae24d-compat-cb6a104a6688/bin/python -u /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_html5lib/run_benchmark.py --inherit-environ PYPERFORMANCE_RUNID,PYTHON_JIT --output /tmp/tmpnmqpxl6_
Traceback (most recent call last):
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_html5lib/run_benchmark.py", line 9, in <module>
    import html5lib
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-a0818d2ae24d-compat-cb6a104a6688/lib/python3.14/site-packages/html5lib/__init__.py", line 25, in <module>
    from .html5parser import HTMLParser, parse, parseFragment
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-a0818d2ae24d-compat-cb6a104a6688/lib/python3.14/site-packages/html5lib/html5parser.py", line 8, in <module>
    from . import _tokenizer
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-a0818d2ae24d-compat-cb6a104a6688/lib/python3.14/site-packages/html5lib/_tokenizer.py", line 16, in <module>
    from ._trie import Trie
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-a0818d2ae24d-compat-cb6a104a6688/lib/python3.14/site-packages/html5lib/_trie/__init__.py", line 3, in <module>
    from .py import Trie as PyTrie
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-a0818d2ae24d-compat-cb6a104a6688/lib/python3.14/site-packages/html5lib/_trie/py.py", line 6, in <module>
    from ._base import Trie as ABCTrie
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-a0818d2ae24d-compat-cb6a104a6688/lib/python3.14/site-packages/html5lib/_trie/_base.py", line 3, in <module>
    from collections import Mapping
ImportError: cannot import name 'Mapping' from 'collections' (/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/collections/__init__.py)
Traceback (most recent call last):
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
             ^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
            ^^^^^^^^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 240, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Command failed with exit code 1
```

</details>

## kinto on linux-x86_64 default

<details>
<summary>Log for kinto on linux-x86_64 default</summary>

```
      [thread 2][gcc -pthread] plugins/http/spdy3.o
      [thread 4][gcc -pthread] plugins/ugreen/ugreen.o
      [thread 7][gcc -pthread] plugins/signal/signal_plugin.o
      [thread 1][gcc -pthread] plugins/syslog/syslog_plugin.o
      [thread 3][gcc -pthread] plugins/rsyslog/rsyslog_plugin.o
      [thread 0][gcc -pthread] plugins/logsocket/logsocket_plugin.o
      [thread 5][gcc -pthread] plugins/router_uwsgi/router_uwsgi.o
      [thread 2][gcc -pthread] plugins/router_redirect/router_redirect.o
      [thread 3][gcc -pthread] plugins/router_basicauth/router_basicauth.o
      [thread 1][gcc -pthread] plugins/zergpool/zergpool.o
      [thread 7][gcc -pthread] plugins/redislog/redislog_plugin.o
      [thread 0][gcc -pthread] plugins/mongodblog/mongodblog_plugin.o
      [thread 4][gcc -pthread] plugins/router_rewrite/router_rewrite.o
      [thread 5][gcc -pthread] plugins/router_http/router_http.o
      [thread 3][gcc -pthread] plugins/logfile/logfile.o
      [thread 2][gcc -pthread] plugins/router_cache/router_cache.o
      [thread 7][gcc -pthread] plugins/rawrouter/rawrouter.o
      [thread 6][gcc -pthread] plugins/router_static/router_static.o
      [thread 4][gcc -pthread] plugins/sslrouter/sslrouter.o
      [thread 1][gcc -pthread] plugins/spooler/spooler_plugin.o
      [thread 0][gcc -pthread] plugins/cheaper_busyness/cheaper_busyness.o
      [thread 2][gcc -pthread] plugins/symcall/symcall_plugin.o
      [thread 5][gcc -pthread] plugins/transformation_tofile/tofile.o
      [thread 3][gcc -pthread] plugins/transformation_gzip/gzip.o
      [thread 6][gcc -pthread] plugins/transformation_chunked/chunked.o
      [thread 1][gcc -pthread] plugins/transformation_offload/offload.o
      [thread 4][gcc -pthread] plugins/router_memcached/router_memcached.o
      [thread 7][gcc -pthread] plugins/router_redis/router_redis.o
      [thread 0][gcc -pthread] plugins/router_hash/router_hash.o
      [thread 5][gcc -pthread] plugins/router_expires/expires.o
      [thread 2][gcc -pthread] plugins/router_metrics/plugin.o
      [thread 1][gcc -pthread] plugins/transformation_template/tt.o
      [thread 6][gcc -pthread] plugins/stats_pusher_socket/plugin.o
      *** uWSGI linking ***
      gcc -pthread -o build/bdist.linux-x86_64/wheel/uwsgi-2.0.28.data/scripts/uwsgi -L/usr/local/lib -Wl,-rpath,/usr/local/lib core/utils.o core/protocol.o core/socket.o core/logging.o core/master.o core/master_utils.o core/emperor.o core/notify.o core/mule.o core/subscription.o core/stats.o core/sendfile.o core/async.o core/master_checks.o core/fifo.o core/offload.o core/io.o core/static.o core/websockets.o core/spooler.o core/snmp.o core/exceptions.o core/config.o core/setup_utils.o core/clock.o core/init.o core/buffer.o core/reader.o core/writer.o core/alarm.o core/cron.o core/hooks.o core/plugins.o core/lock.o core/cache.o core/daemons.o core/errors.o core/hash.o core/master_events.o core/chunked.o core/queue.o core/event.o core/signal.o core/strings.o core/progress.o core/timebomb.o core/ini.o core/fsmon.o core/mount.o core/metrics.o core/plugins_builder.o core/sharedarea.o core/rpc.o core/gateway.o core/loop.o core/cookie.o core/querystring.o core/rb_timers.o core/transformations.o core/uwsgi.o proto/base.o proto/uwsgi.o proto/http.o proto/fastcgi.o proto/scgi.o proto/puwsgi.o lib/linux_ns.o core/zlib.o core/regexp.o core/routing.o core/yaml.o core/json.o core/ssl.o core/legion.o core/xmlconf.o core/dot_h.o core/config_py.o plugins/python/python_plugin.o plugins/python/pyutils.o plugins/python/pyloader.o plugins/python/wsgi_handlers.o plugins/python/wsgi_headers.o plugins/python/wsgi_subhandler.o plugins/python/web3_subhandler.o plugins/python/pump_subhandler.o plugins/python/gil.o plugins/python/uwsgi_pymodule.o plugins/python/profiler.o plugins/python/symimporter.o plugins/python/tracebacker.o plugins/python/raw.o plugins/gevent/gevent.o plugins/gevent/hooks.o plugins/ping/ping_plugin.o plugins/cache/cache.o plugins/nagios/nagios.o plugins/rrdtool/rrdtool.o plugins/carbon/carbon.o plugins/rpc/rpc_plugin.o plugins/corerouter/cr_common.o plugins/corerouter/cr_map.o plugins/corerouter/corerouter.o plugins/fastrouter/fastrouter.o plugins/http/http.o plugins/http/keepalive.o plugins/http/https.o plugins/http/spdy3.o plugins/ugreen/ugreen.o plugins/signal/signal_plugin.o plugins/syslog/syslog_plugin.o plugins/rsyslog/rsyslog_plugin.o plugins/logsocket/logsocket_plugin.o plugins/router_uwsgi/router_uwsgi.o plugins/router_redirect/router_redirect.o plugins/router_basicauth/router_basicauth.o plugins/zergpool/zergpool.o plugins/redislog/redislog_plugin.o plugins/mongodblog/mongodblog_plugin.o plugins/router_rewrite/router_rewrite.o plugins/router_http/router_http.o plugins/logfile/logfile.o plugins/router_cache/router_cache.o plugins/rawrouter/rawrouter.o plugins/router_static/router_static.o plugins/sslrouter/sslrouter.o plugins/spooler/spooler_plugin.o plugins/cheaper_busyness/cheaper_busyness.o plugins/symcall/symcall_plugin.o plugins/transformation_tofile/tofile.o plugins/transformation_gzip/gzip.o plugins/transformation_chunked/chunked.o plugins/transformation_offload/offload.o plugins/router_memcached/router_memcached.o plugins/router_redis/router_redis.o plugins/router_hash/router_hash.o plugins/router_expires/expires.o plugins/router_metrics/plugin.o plugins/transformation_template/tt.o plugins/stats_pusher_socket/plugin.o -lpthread -lm -rdynamic -ldl -lz -lpcre2-8 -luuid -ljansson -lssl -lcrypto -lxml2 -lpthread -ldl -lutil -lm -lpython3.14 -lcrypt
      /usr/bin/ld: cannot find -lpython3.14
      collect2: error: ld returned 1 exit status
      *** error linking uWSGI ***
      [end of output]
  
  note: This error originates from a subprocess, and is likely not a problem with pip.
  ERROR: Failed building wheel for uWSGI
  Running setup.py clean for uWSGI
Successfully built kinto
Failed to build uWSGI
ERROR: Failed to build installable wheels for some pyproject.toml based projects (uWSGI)
Command failed with exit code 1


==================================================
```

</details>

## kinto on collect-stats pystats

<details>
<summary>Log for kinto on collect-stats pystats</summary>

```
# /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/bin/python -u /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_kinto/run_benchmark.py --inherit-environ PYTHON_JIT,PYPERFORMANCE_RUNID --hook=pystats --output /tmp/tmpr0juj8_a
Traceback (most recent call last):
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_kinto/run_benchmark.py", line 73, in <module>
    raise Exception("nginx is not installed")
Exception: nginx is not installed
Traceback (most recent call last):
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
             ^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
            ^^^^^^^^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 240, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Command failed with exit code 1

ERROR: No benchmark was run
Python benchmark suite 1.11.0


==================================================
```

</details>

## mypy2 on linux-x86_64 default

<details>
<summary>Log for mypy2 on linux-x86_64 default</summary>

```
Using pip 25.0.1 from /tmp/tmpotgbe9sk/pip-25.0.1-py3-none-any.whl/pip (python 3.14)
Looking in links: /tmp/tmpotgbe9sk
Processing /tmp/tmpotgbe9sk/pip-25.0.1-py3-none-any.whl
Installing collected packages: pip
  changing mode of /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688-bm-mypy2/bin/pip3 to 755
  changing mode of /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688-bm-mypy2/bin/pip3.14 to 755
Successfully installed pip-25.0.1
# /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688-bm-mypy2/bin/python -m pip install -U 'setuptools>=18.5' wheel
Collecting setuptools>=18.5
  Using cached setuptools-75.8.2-py3-none-any.whl.metadata (6.7 kB)
Collecting wheel
  Using cached wheel-0.45.1-py3-none-any.whl.metadata (2.3 kB)
Using cached setuptools-75.8.2-py3-none-any.whl (1.2 MB)
Using cached wheel-0.45.1-py3-none-any.whl (72 kB)
Installing collected packages: wheel, setuptools
Successfully installed setuptools-75.8.2 wheel-0.45.1
# /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688-bm-mypy2/bin/python -m pip --version
pip 25.0.1 from /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688-bm-mypy2/lib/python3.14/site-packages/pip (python 3.14)
Installing requirements into the virtual environment /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688-bm-mypy2
# /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688-bm-mypy2/bin/python -m pip install --no-binary=mypy mypy==1.13.0 mypy-extensions==1.0.0 typing-extensions==4.2.0 pyperf==2.8.1
Collecting mypy==1.13.0
  Using cached mypy-1.13.0.tar.gz (3.2 MB)
  Installing build dependencies: started
  Installing build dependencies: finished with status 'done'
  Getting requirements to build wheel: started
  Getting requirements to build wheel: finished with status 'done'
  Preparing metadata (pyproject.toml): started
  Preparing metadata (pyproject.toml): finished with status 'done'
Collecting mypy-extensions==1.0.0
  Using cached mypy_extensions-1.0.0-py3-none-any.whl.metadata (1.1 kB)
Collecting typing-extensions==4.2.0
  Using cached typing_extensions-4.2.0-py3-none-any.whl.metadata (6.2 kB)
Collecting pyperf==2.8.1
  Using cached pyperf-2.8.1-py3-none-any.whl.metadata (5.9 kB)
INFO: pip is looking at multiple versions of mypy to determine which version is compatible with other requirements. This could take a while.
ERROR: Cannot install mypy==1.13.0 and typing-extensions==4.2.0 because these package versions have conflicting dependencies.

The conflict is caused by:
    The user requested typing-extensions==4.2.0
    mypy 1.13.0 depends on typing_extensions>=4.6.0

To fix this you could try to:
1. loosen the range of package versions you've specified
2. remove package versions to allow pip to attempt to solve the dependency conflict

ERROR: ResolutionImpossible: for help visit https://pip.pypa.io/en/latest/topics/dependency-resolution/#dealing-with-dependency-conflicts
Command failed with exit code 1


==================================================
```

</details>

## mypy2 on collect-stats pystats

<details>
<summary>Log for mypy2 on collect-stats pystats</summary>

```
# /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688-bm-mypy2/bin/python -m ensurepip -v -U
Using pip 25.0.1 from /tmp/tmp_wb8df2a/pip-25.0.1-py3-none-any.whl/pip (python 3.14)
Looking in links: /tmp/tmp_wb8df2a
Processing /tmp/tmp_wb8df2a/pip-25.0.1-py3-none-any.whl
Installing collected packages: pip
  changing mode of /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688-bm-mypy2/bin/pip3 to 755
  changing mode of /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688-bm-mypy2/bin/pip3.14 to 755
Successfully installed pip-25.0.1
# /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688-bm-mypy2/bin/python -m pip install -U 'setuptools>=18.5' wheel
Collecting setuptools>=18.5
  Using cached setuptools-75.8.2-py3-none-any.whl.metadata (6.7 kB)
Collecting wheel
  Using cached wheel-0.45.1-py3-none-any.whl.metadata (2.3 kB)
Using cached setuptools-75.8.2-py3-none-any.whl (1.2 MB)
Using cached wheel-0.45.1-py3-none-any.whl (72 kB)
Installing collected packages: wheel, setuptools
Successfully installed setuptools-75.8.2 wheel-0.45.1
# /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688-bm-mypy2/bin/python -m pip --version
pip 25.0.1 from /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688-bm-mypy2/lib/python3.14/site-packages/pip (python 3.14)
Installing requirements into the virtual environment /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688-bm-mypy2
# /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688-bm-mypy2/bin/python -m pip install --no-binary=mypy mypy==1.13.0 mypy-extensions==1.0.0 typing-extensions==4.2.0 pyperf==2.8.1
Collecting mypy==1.13.0
  Using cached mypy-1.13.0.tar.gz (3.2 MB)
  Installing build dependencies: started
  Installing build dependencies: finished with status 'done'
  Getting requirements to build wheel: started
  Getting requirements to build wheel: finished with status 'done'
  Preparing metadata (pyproject.toml): started
  Preparing metadata (pyproject.toml): finished with status 'done'
Collecting mypy-extensions==1.0.0
  Using cached mypy_extensions-1.0.0-py3-none-any.whl.metadata (1.1 kB)
Collecting typing-extensions==4.2.0
  Using cached typing_extensions-4.2.0-py3-none-any.whl.metadata (6.2 kB)
Collecting pyperf==2.8.1
  Using cached pyperf-2.8.1-py3-none-any.whl.metadata (5.9 kB)
INFO: pip is looking at multiple versions of mypy to determine which version is compatible with other requirements. This could take a while.
ERROR: Cannot install mypy==1.13.0 and typing-extensions==4.2.0 because these package versions have conflicting dependencies.

The conflict is caused by:
    The user requested typing-extensions==4.2.0
    mypy 1.13.0 depends on typing_extensions>=4.6.0

To fix this you could try to:
1. loosen the range of package versions you've specified
2. remove package versions to allow pip to attempt to solve the dependency conflict

ERROR: ResolutionImpossible: for help visit https://pip.pypa.io/en/latest/topics/dependency-resolution/#dealing-with-dependency-conflicts
Command failed with exit code 1


```

</details>

## pytorch_alexnet_inference on linux-x86_64 default

<details>
<summary>Log for pytorch_alexnet_inference on linux-x86_64 default</summary>

```
  error: subprocess-exited-with-error
  
  × Preparing metadata (pyproject.toml) did not run successfully.
  │ exit code: 1
  ╰─> [31 lines of output]
      Running from numpy source directory.
      <string>:460: UserWarning: Unrecognized setuptools command, proceeding with generating Cython sources and expanding templates
      Traceback (most recent call last):
        File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688-bm-pytorch_alexnet_inference/lib/python3.14/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 389, in <module>
          main()
          ~~~~^^
        File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688-bm-pytorch_alexnet_inference/lib/python3.14/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 373, in main
          json_out["return_val"] = hook(**hook_input["kwargs"])
                                   ~~~~^^^^^^^^^^^^^^^^^^^^^^^^
        File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688-bm-pytorch_alexnet_inference/lib/python3.14/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 175, in prepare_metadata_for_build_wheel
          return hook(metadata_directory, config_settings)
        File "/tmp/pip-build-env-43j00kf7/overlay/lib/python3.14/site-packages/setuptools/build_meta.py", line 377, in prepare_metadata_for_build_wheel
          self.run_setup()
          ~~~~~~~~~~~~~~^^
        File "/tmp/pip-build-env-43j00kf7/overlay/lib/python3.14/site-packages/setuptools/build_meta.py", line 522, in run_setup
          super().run_setup(setup_script=setup_script)
          ~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^
        File "/tmp/pip-build-env-43j00kf7/overlay/lib/python3.14/site-packages/setuptools/build_meta.py", line 320, in run_setup
          exec(code, locals())
          ~~~~^^^^^^^^^^^^^^^^
        File "<string>", line 489, in <module>
        File "<string>", line 465, in setup_package
        File "/tmp/pip-install-_zqlgybe/numpy_a7c76a132ec24e53adf3653b43e2970f/numpy/distutils/core.py", line 24, in <module>
          from numpy.distutils.command import config, config_compiler, \
          ...<2 lines>...
               install_clib
        File "/tmp/pip-install-_zqlgybe/numpy_a7c76a132ec24e53adf3653b43e2970f/numpy/distutils/command/config.py", line 19, in <module>
          from numpy.distutils.mingw32ccompiler import generate_manifest
        File "/tmp/pip-install-_zqlgybe/numpy_a7c76a132ec24e53adf3653b43e2970f/numpy/distutils/mingw32ccompiler.py", line 28, in <module>
          from distutils.msvccompiler import get_build_version as get_build_msvc_version
      ModuleNotFoundError: No module named 'distutils.msvccompiler'
      [end of output]
  
  note: This error originates from a subprocess, and is likely not a problem with pip.
error: metadata-generation-failed

× Encountered error while generating package metadata.
╰─> See above for output.

note: This is an issue with the package mentioned above, not pip.
hint: See above for details.
Command failed with exit code 1


==================================================
```

</details>

## pytorch_alexnet_inference on collect-stats pystats

<details>
<summary>Log for pytorch_alexnet_inference on collect-stats pystats</summary>

```
  Getting requirements to build wheel: finished with status 'done'
  Preparing metadata (pyproject.toml): started
  Preparing metadata (pyproject.toml): finished with status 'error'
  error: subprocess-exited-with-error
  
  × Preparing metadata (pyproject.toml) did not run successfully.
  │ exit code: 1
  ╰─> [29 lines of output]
      Running from numpy source directory.
      <string>:460: UserWarning: Unrecognized setuptools command, proceeding with generating Cython sources and expanding templates
      Traceback (most recent call last):
        File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688-bm-pytorch_alexnet_inference/lib/python3.14/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 389, in <module>
          main()
          ~~~~^^
        File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688-bm-pytorch_alexnet_inference/lib/python3.14/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 373, in main
          json_out["return_val"] = hook(**hook_input["kwargs"])
                                   ~~~~^^^^^^^^^^^^^^^^^^^^^^^^
        File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688-bm-pytorch_alexnet_inference/lib/python3.14/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 175, in prepare_metadata_for_build_wheel
          return hook(metadata_directory, config_settings)
        File "/tmp/pip-build-env-iww0pd2y/overlay/lib/python3.14/site-packages/setuptools/build_meta.py", line 377, in prepare_metadata_for_build_wheel
          self.run_setup()
          ~~~~~~~~~~~~~~^^
        File "/tmp/pip-build-env-iww0pd2y/overlay/lib/python3.14/site-packages/setuptools/build_meta.py", line 522, in run_setup
          super().run_setup(setup_script=setup_script)
          ~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^
        File "/tmp/pip-build-env-iww0pd2y/overlay/lib/python3.14/site-packages/setuptools/build_meta.py", line 320, in run_setup
          exec(code, locals())
          ~~~~^^^^^^^^^^^^^^^^
        File "<string>", line 489, in <module>
        File "<string>", line 465, in setup_package
        File "/tmp/pip-install-w45z7dfz/numpy_f6266b33620e47459739f7aa8203faff/numpy/distutils/__init__.py", line 24, in <module>
          from . import ccompiler
        File "/tmp/pip-install-w45z7dfz/numpy_f6266b33620e47459739f7aa8203faff/numpy/distutils/ccompiler.py", line 9, in <module>
          from distutils.ccompiler import (
          ...<2 lines>...
          )
      ImportError: cannot import name 'compiler_class' from 'distutils.ccompiler' (/tmp/pip-build-env-iww0pd2y/overlay/lib/python3.14/site-packages/setuptools/_distutils/ccompiler.py)
      [end of output]
  
  note: This error originates from a subprocess, and is likely not a problem with pip.
error: metadata-generation-failed

× Encountered error while generating package metadata.
╰─> See above for output.

note: This is an issue with the package mentioned above, not pip.
hint: See above for details.
Command failed with exit code 1


```

</details>

## tornado_http on linux-x86_64 default

<details>
<summary>Log for tornado_http on linux-x86_64 default</summary>

```
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_tornado_http/run_benchmark.py", line 54, in make_http_server
    server.add_sockets(sockets)
    ~~~~~~~~~~~~~~~~~~^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/tornado/tcpserver.py", line 204, in add_sockets
    self._handlers[sock.fileno()] = add_accept_handler(
                                    ~~~~~~~~~~~~~~~~~~^
        sock, self._handle_connection
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/tornado/netutil.py", line 247, in add_accept_handler
    io_loop = IOLoop.current()
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/tornado/ioloop.py", line 265, in current
    loop = asyncio.get_event_loop()
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/asyncio/events.py", line 719, in get_event_loop
    raise RuntimeError('There is no current event loop in thread %r.'
                       % threading.current_thread().name)
RuntimeError: There is no current event loop in thread 'MainThread'.
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_tornado_http/run_benchmark.py", line 102, in <module>
    runner.bench_time_func('tornado_http', bench_tornado)
    ~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_runner.py", line 499, in bench_time_func
    result = self._main(task)
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_runner.py", line 465, in _main
    bench = self._manager()
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_runner.py", line 678, in _manager
    bench = Manager(self).create_bench()
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_manager.py", line 243, in create_bench
    worker_bench, run = self.create_worker_bench()
                        ~~~~~~~~~~~~~~~~~~~~~~~~^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_manager.py", line 142, in create_worker_bench
    suite = self.create_suite()
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_manager.py", line 132, in create_suite
    suite = self.spawn_worker(self.calibrate_loops, 0)
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_manager.py", line 118, in spawn_worker
    raise RuntimeError("%s failed with exit code %s"
                       % (cmd[0], exitcode))
RuntimeError: /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-5216de7f59bf-compat-cb6a104a6688/bin/python failed with exit code 1
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
             ^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
            ^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 240, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Command failed with exit code 1
```

</details>

## tornado_http on collect-stats pystats

<details>
<summary>Log for tornado_http on collect-stats pystats</summary>

```
        sock, self._handle_connection
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/tornado/netutil.py", line 247, in add_accept_handler
    io_loop = IOLoop.current()
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/tornado/ioloop.py", line 265, in current
    loop = asyncio.get_event_loop()
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/asyncio/events.py", line 719, in get_event_loop
    raise RuntimeError('There is no current event loop in thread %r.'
                       % threading.current_thread().name)
RuntimeError: There is no current event loop in thread 'MainThread'.
Traceback (most recent call last):
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_tornado_http/run_benchmark.py", line 102, in <module>
    runner.bench_time_func('tornado_http', bench_tornado)
    ~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_runner.py", line 499, in bench_time_func
    result = self._main(task)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_runner.py", line 465, in _main
    bench = self._manager()
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_runner.py", line 678, in _manager
    bench = Manager(self).create_bench()
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_manager.py", line 243, in create_bench
    worker_bench, run = self.create_worker_bench()
                        ~~~~~~~~~~~~~~~~~~~~~~~~^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_manager.py", line 142, in create_worker_bench
    suite = self.create_suite()
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_manager.py", line 136, in create_suite
    suite = self.spawn_worker(0, 0)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_manager.py", line 118, in spawn_worker
    raise RuntimeError("%s failed with exit code %s"
                       % (cmd[0], exitcode))
RuntimeError: /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-e30a2ba0a3b2-compat-cb6a104a6688/bin/python failed with exit code 1
Traceback (most recent call last):
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
             ^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
            ^^^^^^^^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 240, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Command failed with exit code 1

ERROR: No benchmark was run
Python benchmark suite 1.11.0


==================================================
```

</details>

