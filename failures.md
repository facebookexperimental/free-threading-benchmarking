| benchmark | collect-stats | linux-x86_64 |
| --- | --- | --- |
| aiohttp |  | [[default run]](#aiohttp-on-linux-x86_64-default) |
| chameleon | [[pystats run]](#chameleon-on-collect-stats-pystats) | [[default run]](#chameleon-on-linux-x86_64-default) |
| djangocms | [[pystats build]](#djangocms-on-collect-stats-pystats) | [[default build]](#djangocms-on-linux-x86_64-default) |
| flaskblogging | [[pystats run]](#flaskblogging-on-collect-stats-pystats) | [[default run]](#flaskblogging-on-linux-x86_64-default) |
| gevent_hub | [[pystats run]](#gevent_hub-on-collect-stats-pystats) | [[default run]](#gevent_hub-on-linux-x86_64-default) |
| gunicorn | [[pystats run]](#gunicorn-on-collect-stats-pystats) | [[default run]](#gunicorn-on-linux-x86_64-default) |
| html5lib |  | [[default run]](#html5lib-on-linux-x86_64-default) |
| kinto | [[pystats run]](#kinto-on-collect-stats-pystats) | [[default run]](#kinto-on-linux-x86_64-default) |
| mypy2 | [[pystats build]](#mypy2-on-collect-stats-pystats) | [[default build]](#mypy2-on-linux-x86_64-default) |
| pytorch_alexnet_inference | [[pystats build]](#pytorch_alexnet_inference-on-collect-stats-pystats) | [[default build]](#pytorch_alexnet_inference-on-linux-x86_64-default) |
| tornado_http | [[pystats run]](#tornado_http-on-collect-stats-pystats) | [[default run]](#tornado_http-on-linux-x86_64-default) |
## aiohttp on linux-x86_64 default

<details>
<summary>Log for aiohttp on linux-x86_64 default</summary>

```
# /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/bin/python -u /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_aiohttp/run_benchmark.py --inherit-environ PYTHON_JIT,PYPERFORMANCE_RUNID,PYPERF_PERF_RECORD_EXTRA_OPTS --output /tmp/tmpgw1ti3w2
Traceback (most recent call last):
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_aiohttp/run_benchmark.py", line 69, in <module>
    with context:
         ^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/contextlib.py", line 141, in __enter__
    return next(self.gen)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_aiohttp/netutils.py", line 36, in serving
    waitUntilUp(addr)
    ~~~~~~~~~~~^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_aiohttp/netutils.py", line 66, in waitUntilUp
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
```

</details>

## chameleon on collect-stats pystats

<details>
<summary>Log for chameleon on collect-stats pystats</summary>

```
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/template.py", line 137, in __init__
    self.write(body)
    ~~~~~~~~~~^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/template.py", line 235, in write
    self.cook(body)
    ~~~~~~~~~^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/template.py", line 167, in cook
    program = self._cook(body, digest, names)
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/template.py", line 245, in _cook
    source = self._compile(body, builtins)
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/template.py", line 276, in _compile
    program = self.parse(body)
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/zpt/template.py", line 227, in parse
    return MacroProgram(
        body, self.mode, self.filename,
    ...<9 lines>...
        tokenizer=self.tokenizer
    )
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/zpt/program.py", line 174, in __init__
    super(MacroProgram, self).__init__(*args, **kwargs)
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/program.py", line 35, in __init__
    node = self.visit(kind, args)
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/program.py", line 41, in visit
    return visitor(*args)
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/zpt/program.py", line 320, in visit_element
    ATTRIBUTES = self._create_attributes_nodes(
        prepared, I18N_ATTRIBUTES, STATIC_ATTRIBUTES,
    )
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/zpt/program.py", line 794, in _create_attributes_nodes
    default = ast.Str(s=text) if text is not None else None
              ^^^^^^^
AttributeError: module 'ast' has no attribute 'Str'
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

ERROR: No benchmark was run
Python benchmark suite 1.11.0


==================================================
```

</details>

## chameleon on linux-x86_64 default

<details>
<summary>Log for chameleon on linux-x86_64 default</summary>

```
# /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/bin/python -u /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_chameleon/run_benchmark.py --inherit-environ PYTHON_JIT,PYPERFORMANCE_RUNID,PYPERF_PERF_RECORD_EXTRA_OPTS --output /tmp/tmpd466wne5
Traceback (most recent call last):
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_chameleon/run_benchmark.py", line 5, in <module>
    from chameleon import PageTemplate
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/__init__.py", line 1, in <module>
    from .zpt.template import PageTemplate
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/zpt/template.py", line 6, in <module>
    from ..tales import PythonExpr
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/tales.py", line 27, in <module>
    from .compiler import Interpolator
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/compiler.py", line 34, in <module>
    from .tal import ErrorInfo
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/tal.py", line 26, in <module>
    from chameleon import interfaces
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/chameleon/interfaces.py", line 1, in <module>
    from zope.interface import Interface
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/__init__.py", line 57, in <module>
    _wire()
    ~~~~~^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interface.py", line 1126, in _wire
    from zope.interface.interfaces import IElement
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interfaces.py", line 49, in <module>
    class IElement(Interface):
    ...<91 lines>...
            """
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interface.py", line 794, in __init__
    self.__attrs = self.__compute_attrs(attrs)
                   ~~~~~~~~~~~~~~~~~~~~^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interface.py", line 813, in __compute_attrs
    aname: update_value(aname, aval)
           ~~~~~~~~~~~~^^^^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interface.py", line 809, in update_value
    raise InvalidInterface("Concrete attribute, " + aname)
zope.interface.exceptions.InvalidInterface: Concrete attribute, __firstlineno__
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

## flaskblogging on collect-stats pystats

<details>
<summary>Log for flaskblogging on collect-stats pystats</summary>

```
# /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/bin/python -u /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_flaskblogging/run_benchmark.py --inherit-environ PYTHON_JIT,PYPERF_PERF_RECORD_EXTRA_OPTS,PYPERFORMANCE_RUNID --hook=pystats --loops=32 --output /tmp/tmp7x0y5joo
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

ERROR: No benchmark was run
Python benchmark suite 1.11.0


==================================================
```

</details>

## flaskblogging on linux-x86_64 default

<details>
<summary>Log for flaskblogging on linux-x86_64 default</summary>

```
# /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/bin/python -u /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_flaskblogging/run_benchmark.py --inherit-environ PYTHON_JIT,PYPERFORMANCE_RUNID,PYPERF_PERF_RECORD_EXTRA_OPTS --output /tmp/tmpepgc14m3
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
```

</details>

## gevent_hub on collect-stats pystats

<details>
<summary>Log for gevent_hub on collect-stats pystats</summary>

```
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/gevent/_config.py", line 151, in get
    self.value = self.validate(self._default())
                 ~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/gevent/_config.py", line 259, in validate
    return self._import_one_of([self.shortname_map.get(x, x) for x in value])
           ~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/gevent/_config.py", line 230, in _import_one_of
    return self._import_one(item)
           ~~~~~~~~~~~~~~~~^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/gevent/_config.py", line 248, in _import_one
    module = importlib.import_module(module)
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/importlib/__init__.py", line 88, in import_module
    return _bootstrap._gcd_import(name[level:], package, level)
           ~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "src/gevent/libev/corecext.pyx", line 819, in init gevent.libev.corecext
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/__init__.py", line 58, in <module>
    _wire()
    ~~~~~^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interface.py", line 1154, in _wire
    from zope.interface.interfaces import IElement
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interfaces.py", line 56, in <module>
    class IElement(Interface):
    ...<93 lines>...
            """
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interface.py", line 794, in __init__
    self.__attrs = self.__compute_attrs(attrs)
                   ~~~~~~~~~~~~~~~~~~~~^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interface.py", line 813, in __compute_attrs
    aname: update_value(aname, aval)
           ~~~~~~~~~~~~^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interface.py", line 809, in update_value
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
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/gevent/__init__.py", line 71, in <module>
    from gevent._config import config
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/gevent/_config.py", line 730, in <module>
    Loop().get()
    ~~~~~~~~~~^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/gevent/_config.py", line 151, in get
    self.value = self.validate(self._default())
                 ~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/gevent/_config.py", line 259, in validate
    return self._import_one_of([self.shortname_map.get(x, x) for x in value])
           ~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/gevent/_config.py", line 230, in _import_one_of
    return self._import_one(item)
           ~~~~~~~~~~~~~~~~^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/gevent/_config.py", line 248, in _import_one
    module = importlib.import_module(module)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/importlib/__init__.py", line 88, in import_module
    return _bootstrap._gcd_import(name[level:], package, level)
           ~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "src/gevent/libev/corecext.pyx", line 819, in init gevent.libev.corecext
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/__init__.py", line 57, in <module>
    _wire()
    ~~~~~^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interface.py", line 1126, in _wire
    from zope.interface.interfaces import IElement
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interfaces.py", line 49, in <module>
    class IElement(Interface):
    ...<91 lines>...
            """
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interface.py", line 794, in __init__
    self.__attrs = self.__compute_attrs(attrs)
                   ~~~~~~~~~~~~~~~~~~~~^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interface.py", line 813, in __compute_attrs
    aname: update_value(aname, aval)
           ~~~~~~~~~~~~^^^^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/zope/interface/interface.py", line 809, in update_value
    raise InvalidInterface("Concrete attribute, " + aname)
zope.interface.exceptions.InvalidInterface: Concrete attribute, __firstlineno__
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

## gunicorn on collect-stats pystats

<details>
<summary>Log for gunicorn on collect-stats pystats</summary>

```
# /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/bin/python -u /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_gunicorn/run_benchmark.py --inherit-environ PYTHON_JIT,PYPERF_PERF_RECORD_EXTRA_OPTS,PYPERFORMANCE_RUNID --hook=pystats --loops=128 --output /tmp/tmpc_417g50
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

ERROR: No benchmark was run
Python benchmark suite 1.11.0


==================================================
```

</details>

## gunicorn on linux-x86_64 default

<details>
<summary>Log for gunicorn on linux-x86_64 default</summary>

```
# /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/bin/python -u /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_gunicorn/run_benchmark.py --inherit-environ PYTHON_JIT,PYPERFORMANCE_RUNID,PYPERF_PERF_RECORD_EXTRA_OPTS --output /tmp/tmpb00ixmkp
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
```

</details>

## html5lib on linux-x86_64 default

<details>
<summary>Log for html5lib on linux-x86_64 default</summary>

```
# /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/bin/python -u /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_html5lib/run_benchmark.py --inherit-environ PYTHON_JIT,PYPERFORMANCE_RUNID,PYPERF_PERF_RECORD_EXTRA_OPTS --output /tmp/tmpme57b2bs
Traceback (most recent call last):
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_html5lib/run_benchmark.py", line 9, in <module>
    import html5lib
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/html5lib/__init__.py", line 25, in <module>
    from .html5parser import HTMLParser, parse, parseFragment
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/html5lib/html5parser.py", line 8, in <module>
    from . import _tokenizer
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/html5lib/_tokenizer.py", line 16, in <module>
    from ._trie import Trie
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/html5lib/_trie/__init__.py", line 3, in <module>
    from .py import Trie as PyTrie
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/html5lib/_trie/py.py", line 6, in <module>
    from ._base import Trie as ABCTrie
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/html5lib/_trie/_base.py", line 3, in <module>
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

## kinto on collect-stats pystats

<details>
<summary>Log for kinto on collect-stats pystats</summary>

```
# /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/bin/python -u /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_kinto/run_benchmark.py --inherit-environ PYPERF_PERF_RECORD_EXTRA_OPTS,PYTHON_JIT,PYPERFORMANCE_RUNID --hook=pystats --output /tmp/tmpsmpce605
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_kinto/run_benchmark.py", line 73, in <module>
    raise Exception("nginx is not installed")
Exception: nginx is not installed
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

ERROR: No benchmark was run
Python benchmark suite 1.11.0


==================================================
```

</details>

## kinto on linux-x86_64 default

<details>
<summary>Log for kinto on linux-x86_64 default</summary>

```
# /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/bin/python -u /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_kinto/run_benchmark.py --inherit-environ PYTHON_JIT,PYPERFORMANCE_RUNID,PYPERF_PERF_RECORD_EXTRA_OPTS --output /tmp/tmph5ikmqrs
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
```

</details>

## mypy2 on collect-stats pystats

<details>
<summary>Log for mypy2 on collect-stats pystats</summary>

```
# /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688-bm-mypy2/bin/python -m ensurepip -v -U
Using pip 25.0.1 from /tmp/tmpftfh_k32/pip-25.0.1-py3-none-any.whl/pip (python 3.14)
Looking in links: /tmp/tmpftfh_k32
Processing /tmp/tmpftfh_k32/pip-25.0.1-py3-none-any.whl
Installing collected packages: pip
  changing mode of /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688-bm-mypy2/bin/pip3 to 755
  changing mode of /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688-bm-mypy2/bin/pip3.14 to 755
Successfully installed pip-25.0.1
# /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688-bm-mypy2/bin/python -m pip install -U 'setuptools>=18.5' wheel
Collecting setuptools>=18.5
  Using cached setuptools-76.0.0-py3-none-any.whl.metadata (6.7 kB)
Collecting wheel
  Using cached wheel-0.45.1-py3-none-any.whl.metadata (2.3 kB)
Using cached setuptools-76.0.0-py3-none-any.whl (1.2 MB)
Using cached wheel-0.45.1-py3-none-any.whl (72 kB)
Installing collected packages: wheel, setuptools
Successfully installed setuptools-76.0.0 wheel-0.45.1
# /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688-bm-mypy2/bin/python -m pip --version
pip 25.0.1 from /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688-bm-mypy2/lib/python3.14/site-packages/pip (python 3.14)
Installing requirements into the virtual environment /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688-bm-mypy2
# /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688-bm-mypy2/bin/python -m pip install --no-binary=mypy mypy==1.13.0 mypy-extensions==1.0.0 typing-extensions==4.2.0 pyperf==2.8.1
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

## mypy2 on linux-x86_64 default

<details>
<summary>Log for mypy2 on linux-x86_64 default</summary>

```
Using pip 25.0.1 from /tmp/tmphf2x5181/pip-25.0.1-py3-none-any.whl/pip (python 3.14)
Looking in links: /tmp/tmphf2x5181
Processing /tmp/tmphf2x5181/pip-25.0.1-py3-none-any.whl
Installing collected packages: pip
  changing mode of /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688-bm-mypy2/bin/pip3 to 755
  changing mode of /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688-bm-mypy2/bin/pip3.14 to 755
Successfully installed pip-25.0.1
# /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688-bm-mypy2/bin/python -m pip install -U 'setuptools>=18.5' wheel
Collecting setuptools>=18.5
  Using cached setuptools-76.0.0-py3-none-any.whl.metadata (6.7 kB)
Collecting wheel
  Using cached wheel-0.45.1-py3-none-any.whl.metadata (2.3 kB)
Using cached setuptools-76.0.0-py3-none-any.whl (1.2 MB)
Using cached wheel-0.45.1-py3-none-any.whl (72 kB)
Installing collected packages: wheel, setuptools
Successfully installed setuptools-76.0.0 wheel-0.45.1
# /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688-bm-mypy2/bin/python -m pip --version
pip 25.0.1 from /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688-bm-mypy2/lib/python3.14/site-packages/pip (python 3.14)
Installing requirements into the virtual environment /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688-bm-mypy2
# /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688-bm-mypy2/bin/python -m pip install --no-binary=mypy mypy==1.13.0 mypy-extensions==1.0.0 typing-extensions==4.2.0 pyperf==2.8.1
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
        File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688-bm-pytorch_alexnet_inference/lib/python3.14/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 389, in <module>
          main()
          ~~~~^^
        File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688-bm-pytorch_alexnet_inference/lib/python3.14/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 373, in main
          json_out["return_val"] = hook(**hook_input["kwargs"])
                                   ~~~~^^^^^^^^^^^^^^^^^^^^^^^^
        File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688-bm-pytorch_alexnet_inference/lib/python3.14/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 175, in prepare_metadata_for_build_wheel
          return hook(metadata_directory, config_settings)
        File "/tmp/pip-build-env-8e5gylto/overlay/lib/python3.14/site-packages/setuptools/build_meta.py", line 377, in prepare_metadata_for_build_wheel
          self.run_setup()
          ~~~~~~~~~~~~~~^^
        File "/tmp/pip-build-env-8e5gylto/overlay/lib/python3.14/site-packages/setuptools/build_meta.py", line 522, in run_setup
          super().run_setup(setup_script=setup_script)
          ~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^
        File "/tmp/pip-build-env-8e5gylto/overlay/lib/python3.14/site-packages/setuptools/build_meta.py", line 320, in run_setup
          exec(code, locals())
          ~~~~^^^^^^^^^^^^^^^^
        File "<string>", line 489, in <module>
        File "<string>", line 465, in setup_package
        File "/tmp/pip-install-x4t2w9qt/numpy_51c7e325ce114c11815696dc502b511a/numpy/distutils/__init__.py", line 24, in <module>
          from . import ccompiler
        File "/tmp/pip-install-x4t2w9qt/numpy_51c7e325ce114c11815696dc502b511a/numpy/distutils/ccompiler.py", line 9, in <module>
          from distutils.ccompiler import (
          ...<2 lines>...
          )
      ImportError: cannot import name 'compiler_class' from 'distutils.ccompiler' (/tmp/pip-build-env-8e5gylto/overlay/lib/python3.14/site-packages/setuptools/_distutils/ccompiler.py)
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

## pytorch_alexnet_inference on linux-x86_64 default

<details>
<summary>Log for pytorch_alexnet_inference on linux-x86_64 default</summary>

```
  Preparing metadata (pyproject.toml): started
  Preparing metadata (pyproject.toml): finished with status 'error'
  error: subprocess-exited-with-error
  
  × Preparing metadata (pyproject.toml) did not run successfully.
  │ exit code: 1
  ╰─> [29 lines of output]
      Running from numpy source directory.
      <string>:460: UserWarning: Unrecognized setuptools command, proceeding with generating Cython sources and expanding templates
      Traceback (most recent call last):
        File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688-bm-pytorch_alexnet_inference/lib/python3.14/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 389, in <module>
          main()
          ~~~~^^
        File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688-bm-pytorch_alexnet_inference/lib/python3.14/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 373, in main
          json_out["return_val"] = hook(**hook_input["kwargs"])
                                   ~~~~^^^^^^^^^^^^^^^^^^^^^^^^
        File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688-bm-pytorch_alexnet_inference/lib/python3.14/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 175, in prepare_metadata_for_build_wheel
          return hook(metadata_directory, config_settings)
        File "/tmp/pip-build-env-gygcrg2m/overlay/lib/python3.14/site-packages/setuptools/build_meta.py", line 377, in prepare_metadata_for_build_wheel
          self.run_setup()
          ~~~~~~~~~~~~~~^^
        File "/tmp/pip-build-env-gygcrg2m/overlay/lib/python3.14/site-packages/setuptools/build_meta.py", line 522, in run_setup
          super().run_setup(setup_script=setup_script)
          ~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^
        File "/tmp/pip-build-env-gygcrg2m/overlay/lib/python3.14/site-packages/setuptools/build_meta.py", line 320, in run_setup
          exec(code, locals())
          ~~~~^^^^^^^^^^^^^^^^
        File "<string>", line 489, in <module>
        File "<string>", line 465, in setup_package
        File "/tmp/pip-install-81b8ddu4/numpy_2f64d6249f434f6d858a47aaad37e5a0/numpy/distutils/__init__.py", line 24, in <module>
          from . import ccompiler
        File "/tmp/pip-install-81b8ddu4/numpy_2f64d6249f434f6d858a47aaad37e5a0/numpy/distutils/ccompiler.py", line 9, in <module>
          from distutils.ccompiler import (
          ...<2 lines>...
          )
      ImportError: cannot import name 'compiler_class' from 'distutils.ccompiler' (/tmp/pip-build-env-gygcrg2m/overlay/lib/python3.14/site-packages/setuptools/_distutils/ccompiler.py)
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

## tornado_http on collect-stats pystats

<details>
<summary>Log for tornado_http on collect-stats pystats</summary>

```
        sock, self._handle_connection
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/tornado/netutil.py", line 247, in add_accept_handler
    io_loop = IOLoop.current()
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/tornado/ioloop.py", line 265, in current
    loop = asyncio.get_event_loop()
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/asyncio/events.py", line 719, in get_event_loop
    raise RuntimeError('There is no current event loop in thread %r.'
                       % threading.current_thread().name)
RuntimeError: There is no current event loop in thread 'MainThread'.
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_tornado_http/run_benchmark.py", line 102, in <module>
    runner.bench_time_func('tornado_http', bench_tornado)
    ~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_runner.py", line 499, in bench_time_func
    result = self._main(task)
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_runner.py", line 465, in _main
    bench = self._manager()
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_runner.py", line 678, in _manager
    bench = Manager(self).create_bench()
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_manager.py", line 243, in create_bench
    worker_bench, run = self.create_worker_bench()
                        ~~~~~~~~~~~~~~~~~~~~~~~~^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_manager.py", line 142, in create_worker_bench
    suite = self.create_suite()
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_manager.py", line 136, in create_suite
    suite = self.spawn_worker(0, 0)
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_manager.py", line 118, in spawn_worker
    raise RuntimeError("%s failed with exit code %s"
                       % (cmd[0], exitcode))
RuntimeError: /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-fa053140d25b-compat-cb6a104a6688/bin/python failed with exit code 1
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

ERROR: No benchmark was run
Python benchmark suite 1.11.0


==================================================
```

</details>

## tornado_http on linux-x86_64 default

<details>
<summary>Log for tornado_http on linux-x86_64 default</summary>

```
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_tornado_http/run_benchmark.py", line 54, in make_http_server
    server.add_sockets(sockets)
    ~~~~~~~~~~~~~~~~~~^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/tornado/tcpserver.py", line 204, in add_sockets
    self._handlers[sock.fileno()] = add_accept_handler(
                                    ~~~~~~~~~~~~~~~~~~^
        sock, self._handle_connection
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/tornado/netutil.py", line 247, in add_accept_handler
    io_loop = IOLoop.current()
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/tornado/ioloop.py", line 265, in current
    loop = asyncio.get_event_loop()
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/asyncio/events.py", line 719, in get_event_loop
    raise RuntimeError('There is no current event loop in thread %r.'
                       % threading.current_thread().name)
RuntimeError: There is no current event loop in thread 'MainThread'.
Traceback (most recent call last):
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_tornado_http/run_benchmark.py", line 102, in <module>
    runner.bench_time_func('tornado_http', bench_tornado)
    ~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_runner.py", line 499, in bench_time_func
    result = self._main(task)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_runner.py", line 465, in _main
    bench = self._manager()
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_runner.py", line 678, in _manager
    bench = Manager(self).create_bench()
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_manager.py", line 243, in create_bench
    worker_bench, run = self.create_worker_bench()
                        ~~~~~~~~~~~~~~~~~~~~~~~~^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_manager.py", line 142, in create_worker_bench
    suite = self.create_suite()
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_manager.py", line 132, in create_suite
    suite = self.spawn_worker(self.calibrate_loops, 0)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/lib/python3.14/site-packages/pyperf/_manager.py", line 118, in spawn_worker
    raise RuntimeError("%s failed with exit code %s"
                       % (cmd[0], exitcode))
RuntimeError: /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-7e61345adec3-compat-cb6a104a6688/bin/python failed with exit code 1
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

