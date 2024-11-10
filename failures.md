| benchmark | linux-x86_64 |
| --- | --- |
| aiohttp | [[default run]](#aiohttp-on-linux-x86_64-default) |
| async_tree | [[default run]](#async_tree-on-linux-x86_64-default) |
| async_tree_cpu_io_mixed | [[default run]](#async_tree_cpu_io_mixed-on-linux-x86_64-default) |
| async_tree_cpu_io_mixed_tg | [[default run]](#async_tree_cpu_io_mixed_tg-on-linux-x86_64-default) |
| async_tree_io | [[default run]](#async_tree_io-on-linux-x86_64-default) |
| async_tree_io_tg | [[default run]](#async_tree_io_tg-on-linux-x86_64-default) |
| async_tree_memoization | [[default run]](#async_tree_memoization-on-linux-x86_64-default) |
| async_tree_memoization_tg | [[default run]](#async_tree_memoization_tg-on-linux-x86_64-default) |
| async_tree_tg | [[default run]](#async_tree_tg-on-linux-x86_64-default) |
| chameleon | [[default run]](#chameleon-on-linux-x86_64-default) |
| dask | [[default run]](#dask-on-linux-x86_64-default) |
| djangocms | [[default build]](#djangocms-on-linux-x86_64-default) |
| flaskblogging | [[default run]](#flaskblogging-on-linux-x86_64-default) |
| gevent_hub | [[default build]](#gevent_hub-on-linux-x86_64-default) |
| gunicorn | [[default run]](#gunicorn-on-linux-x86_64-default) |
| kinto | [[default build]](#kinto-on-linux-x86_64-default) |
| mypy2 | [[default build]](#mypy2-on-linux-x86_64-default) |
| pytorch_alexnet_inference | [[default build]](#pytorch_alexnet_inference-on-linux-x86_64-default) |
| sqlalchemy_declarative | [[default build]](#sqlalchemy_declarative-on-linux-x86_64-default) |
| sqlalchemy_imperative | [[default build]](#sqlalchemy_imperative-on-linux-x86_64-default) |
| tornado_http | [[default run]](#tornado_http-on-linux-x86_64-default) |
## aiohttp on linux-x86_64 default

<details>
<summary>Log for aiohttp on linux-x86_64 default</summary>

```
# /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/bin/python -u /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_aiohttp/run_benchmark.py --inherit-environ PYPERFORMANCE_RUNID,PYTHON_JIT --output /tmp/tmpc2x6fgqk
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
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 236, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Command failed with exit code 1
```

</details>

## async_tree on linux-x86_64 default

<details>
<summary>Log for async_tree on linux-x86_64 default</summary>

```
# /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/bin/python -u /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_async_tree/run_benchmark.py none --inherit-environ PYPERFORMANCE_RUNID,PYTHON_JIT --output /tmp/tmp2mvyxu3p
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 1662, in _check_help
    formatter._expand_help(action)
    ~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 604, in _expand_help
    return help_string % params
           ~~~~~~~~~~~~^~~~~~~~
TypeError: %o format: an integer is required, not dict

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_async_tree/run_benchmark.py", line 192, in <module>
    add_parser_args(runner.argparser)
    ~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_async_tree/run_benchmark.py", line 155, in add_parser_args
        parser.add_argument(
        ~~~~~~~~~~~~~~~~~~~^
            "benchmark",
            ^^^^^^^^^^^^
    ...<10 lines>...
    """,
    ^^^^
        )
        ^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 1476, in add_argument
    self._check_help(action)
Command failed with exit code 1
    ~~~~~~~~~~~~~~~~^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 1664, in _check_help
    raise ValueError('badly formed help string') from exc
ValueError: badly formed help string
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
             ^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
            ^^^^^^^^^^^^^^^^^
```

</details>

## async_tree_cpu_io_mixed on linux-x86_64 default

<details>
<summary>Log for async_tree_cpu_io_mixed on linux-x86_64 default</summary>

```
# /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/bin/python -u /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_async_tree/run_benchmark.py cpu_io_mixed --inherit-environ PYPERFORMANCE_RUNID,PYTHON_JIT --output /tmp/tmpjfc_d1db
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 236, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 1662, in _check_help
    formatter._expand_help(action)
    ~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 604, in _expand_help
    return help_string % params
           ~~~~~~~~~~~~^~~~~~~~
TypeError: %o format: an integer is required, not dict

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_async_tree/run_benchmark.py", line 192, in <module>
    add_parser_args(runner.argparser)
    ~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_async_tree/run_benchmark.py", line 155, in add_parser_args
        parser.add_argument(
        ~~~~~~~~~~~~~~~~~~~^
            "benchmark",
            ^^^^^^^^^^^^
    ...<10 lines>...
    """,
    ^^^^
        )
Command failed with exit code 1
```

</details>

## async_tree_cpu_io_mixed_tg on linux-x86_64 default

<details>
<summary>Log for async_tree_cpu_io_mixed_tg on linux-x86_64 default</summary>

```
    result = bench.run(
             ^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
            ^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 236, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 1662, in _check_help
    formatter._expand_help(action)
    ~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 604, in _expand_help
    return help_string % params
           ~~~~~~~~~~~~^~~~~~~~
TypeError: %o format: an integer is required, not dict

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_async_tree/run_benchmark.py", line 192, in <module>
    add_parser_args(runner.argparser)
    ~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_async_tree/run_benchmark.py", line 155, in add_parser_args
        parser.add_argument(
        ~~~~~~~~~~~~~~~~~~~^
            "benchmark",
            ^^^^^^^^^^^^
    ...<10 lines>...
    """,
    ^^^^
        )
        ^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 1476, in add_argument
    self._check_help(action)
    ~~~~~~~~~~~~~~~~^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 1664, in _check_help
    raise ValueError('badly formed help string') from exc
ValueError: badly formed help string
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
             ^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
            ^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 236, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Command failed with exit code 1
```

</details>

## async_tree_io on linux-x86_64 default

<details>
<summary>Log for async_tree_io on linux-x86_64 default</summary>

```
# /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/bin/python -u /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_async_tree/run_benchmark.py io --inherit-environ PYPERFORMANCE_RUNID,PYTHON_JIT --output /tmp/tmpoihlkemr
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 1662, in _check_help
    formatter._expand_help(action)
    ~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 604, in _expand_help
    return help_string % params
           ~~~~~~~~~~~~^~~~~~~~
TypeError: %o format: an integer is required, not dict

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_async_tree/run_benchmark.py", line 192, in <module>
    add_parser_args(runner.argparser)
    ~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_async_tree/run_benchmark.py", line 155, in add_parser_args
        parser.add_argument(
        ~~~~~~~~~~~~~~~~~~~^
            "benchmark",
            ^^^^^^^^^^^^
    ...<10 lines>...
    """,
    ^^^^
        )
Command failed with exit code 1
```

</details>

## async_tree_io_tg on linux-x86_64 default

<details>
<summary>Log for async_tree_io_tg on linux-x86_64 default</summary>

```
    result = bench.run(
             ^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
            ^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 236, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Traceback (most recent call last):
Command failed with exit code 1
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 1662, in _check_help
    formatter._expand_help(action)
    ~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 604, in _expand_help
    return help_string % params
           ~~~~~~~~~~~~^~~~~~~~
TypeError: %o format: an integer is required, not dict

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_async_tree/run_benchmark.py", line 192, in <module>
    add_parser_args(runner.argparser)
    ~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_async_tree/run_benchmark.py", line 155, in add_parser_args
        parser.add_argument(
        ~~~~~~~~~~~~~~~~~~~^
            "benchmark",
            ^^^^^^^^^^^^
    ...<10 lines>...
    """,
    ^^^^
        )
        ^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 1476, in add_argument
    self._check_help(action)
    ~~~~~~~~~~~~~~~~^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 1664, in _check_help
    raise ValueError('badly formed help string') from exc
ValueError: badly formed help string
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
             ^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
            ^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 236, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
```

</details>

## async_tree_memoization on linux-x86_64 default

<details>
<summary>Log for async_tree_memoization on linux-x86_64 default</summary>

```
# /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/bin/python -u /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_async_tree/run_benchmark.py memoization --inherit-environ PYPERFORMANCE_RUNID,PYTHON_JIT --output /tmp/tmphrdlcrlv
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 1662, in _check_help
    formatter._expand_help(action)
    ~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 604, in _expand_help
    return help_string % params
           ~~~~~~~~~~~~^~~~~~~~
TypeError: %o format: an integer is required, not dict

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_async_tree/run_benchmark.py", line 192, in <module>
    add_parser_args(runner.argparser)
    ~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_async_tree/run_benchmark.py", line 155, in add_parser_args
        parser.add_argument(
        ~~~~~~~~~~~~~~~~~~~^
            "benchmark",
            ^^^^^^^^^^^^
    ...<10 lines>...
    """,
    ^^^^
        )
        ^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 1476, in add_argument
    self._check_help(action)
    ~~~~~~~~~~~~~~~~^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 1664, in _check_help
    raise ValueError('badly formed help string') from exc
ValueError: badly formed help string
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
             ^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
            ^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 236, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Command failed with exit code 1
```

</details>

## async_tree_memoization_tg on linux-x86_64 default

<details>
<summary>Log for async_tree_memoization_tg on linux-x86_64 default</summary>

```
# /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/bin/python -u /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_async_tree/run_benchmark.py memoization --task-groups --inherit-environ PYPERFORMANCE_RUNID,PYTHON_JIT --output /tmp/tmpx03tfvi3
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 1662, in _check_help
    formatter._expand_help(action)
    ~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 604, in _expand_help
    return help_string % params
           ~~~~~~~~~~~~^~~~~~~~
TypeError: %o format: an integer is required, not dict

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_async_tree/run_benchmark.py", line 192, in <module>
    add_parser_args(runner.argparser)
    ~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_async_tree/run_benchmark.py", line 155, in add_parser_args
        parser.add_argument(
        ~~~~~~~~~~~~~~~~~~~^
            "benchmark",
            ^^^^^^^^^^^^
    ...<10 lines>...
    """,
    ^^^^
        )
        ^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 1476, in add_argument
    self._check_help(action)
    ~~~~~~~~~~~~~~~~^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 1664, in _check_help
    raise ValueError('badly formed help string') from exc
ValueError: badly formed help string
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
             ^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
            ^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 236, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Command failed with exit code 1
```

</details>

## async_tree_tg on linux-x86_64 default

<details>
<summary>Log for async_tree_tg on linux-x86_64 default</summary>

```
# /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/bin/python -u /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_async_tree/run_benchmark.py none --task-groups --inherit-environ PYPERFORMANCE_RUNID,PYTHON_JIT --output /tmp/tmp8mc2j0pm
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 1662, in _check_help
    formatter._expand_help(action)
    ~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 604, in _expand_help
    return help_string % params
           ~~~~~~~~~~~~^~~~~~~~
TypeError: %o format: an integer is required, not dict

The above exception was the direct cause of the following exception:

Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_async_tree/run_benchmark.py", line 192, in <module>
    add_parser_args(runner.argparser)
    ~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_async_tree/run_benchmark.py", line 155, in add_parser_args
        parser.add_argument(
        ~~~~~~~~~~~~~~~~~~~^
            "benchmark",
            ^^^^^^^^^^^^
    ...<10 lines>...
    """,
    ^^^^
        )
        ^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 1476, in add_argument
    self._check_help(action)
    ~~~~~~~~~~~~~~~~^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/argparse.py", line 1664, in _check_help
    raise ValueError('badly formed help string') from exc
ValueError: badly formed help string
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
             ^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
            ^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 236, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Command failed with exit code 1
```

</details>

## chameleon on linux-x86_64 default

<details>
<summary>Log for chameleon on linux-x86_64 default</summary>

```
    ~~~~^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_chameleon/run_benchmark.py", line 25, in main
    tmpl = PageTemplate(BIGTABLE_ZPT)
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/chameleon/zpt/template.py", line 205, in __init__
    super(PageTemplate, self).__init__(body, **config)
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/chameleon/template.py", line 137, in __init__
    self.write(body)
    ~~~~~~~~~~^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/chameleon/template.py", line 235, in write
    self.cook(body)
    ~~~~~~~~~^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/chameleon/template.py", line 167, in cook
    program = self._cook(body, digest, names)
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/chameleon/template.py", line 245, in _cook
    source = self._compile(body, builtins)
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/chameleon/template.py", line 276, in _compile
    program = self.parse(body)
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/chameleon/zpt/template.py", line 227, in parse
    return MacroProgram(
        body, self.mode, self.filename,
    ...<9 lines>...
        tokenizer=self.tokenizer
    )
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/chameleon/zpt/program.py", line 174, in __init__
    super(MacroProgram, self).__init__(*args, **kwargs)
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/chameleon/program.py", line 35, in __init__
    node = self.visit(kind, args)
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/chameleon/program.py", line 41, in visit
    return visitor(*args)
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/chameleon/zpt/program.py", line 320, in visit_element
    ATTRIBUTES = self._create_attributes_nodes(
        prepared, I18N_ATTRIBUTES, STATIC_ATTRIBUTES,
    )
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/chameleon/zpt/program.py", line 794, in _create_attributes_nodes
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
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 236, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Command failed with exit code 1
```

</details>

## dask on linux-x86_64 default

<details>
<summary>Log for dask on linux-x86_64 default</summary>

```
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/dask/highlevelgraph.py", line 425, in __dask_distributed_pack__
    dsk = toolz.valmap(dumps_task, dsk)
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/toolz/dicttoolz.py", line 85, in valmap
    rv.update(zip(d.keys(), map(func, d.values())))
    ~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/distributed/worker.py", line 4480, in dumps_task
    return {"function": dumps_function(task[0]), "args": warn_dumps(task[1:])}
                        ~~~~~~~~~~~~~~^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/distributed/worker.py", line 4444, in dumps_function
    result = pickle.dumps(func, protocol=4)
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/distributed/protocol/pickle.py", line 60, in dumps
    result = cloudpickle.dumps(x, **dump_kwargs)
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/cloudpickle/cloudpickle.py", line 1529, in dumps
    cp.dump(obj)
    ~~~~~~~^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/cloudpickle/cloudpickle.py", line 1299, in dump
    raise pickle.PicklingError(msg) from e
_pickle.PicklingError: Could not pickle object as excessively deep recursion required.
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_dask/run_benchmark.py", line 37, in <module>
    runner.bench_async_func('dask', benchmark)
    ~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/pyperf/_runner.py", line 605, in bench_async_func
    result = self._main(task)
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/pyperf/_runner.py", line 460, in _main
    bench = self._manager()
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/pyperf/_runner.py", line 673, in _manager
    bench = Manager(self).create_bench()
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/pyperf/_manager.py", line 232, in create_bench
    worker_bench, run = self.create_worker_bench()
                        ~~~~~~~~~~~~~~~~~~~~~~~~^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/pyperf/_manager.py", line 131, in create_worker_bench
    suite = self.create_suite()
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/pyperf/_manager.py", line 121, in create_suite
    suite = self.spawn_worker(self.calibrate_loops, 0)
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/pyperf/_manager.py", line 107, in spawn_worker
    raise RuntimeError("%s failed with exit code %s"
                       % (cmd[0], exitcode))
RuntimeError: /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/bin/python failed with exit code 1
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
             ^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
            ^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 236, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Command failed with exit code 1
```

</details>

## djangocms on linux-x86_64 default

<details>
<summary>Log for djangocms on linux-x86_64 default</summary>

```
Collecting html5lib==1.1
  Using cached html5lib-1.1-py2.py3-none-any.whl.metadata (16 kB)
Collecting idna==2.10
  Using cached idna-2.10-py2.py3-none-any.whl.metadata (9.1 kB)
Collecting legacy-cgi==2.6
  Using cached legacy_cgi-2.6-py3-none-any.whl.metadata (1.4 kB)
Collecting Pillow==8.0.0
  Using cached Pillow-8.0.0.tar.gz (44.6 MB)
  Preparing metadata (setup.py): started
  Preparing metadata (setup.py): finished with status 'error'
  error: subprocess-exited-with-error
  
  × python setup.py egg_info did not run successfully.
  │ exit code: 1
  ╰─> [18 lines of output]
      Traceback (most recent call last):
        File "<string>", line 2, in <module>
          exec(compile('''
          ~~~~^^^^^^^^^^^^
          # This is <pip-setuptools-caller> -- a caller that pip uses to run setup.py
          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
          ...<31 lines>...
          exec(compile(setup_py_code, filename, "exec"))
          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
          ''' % ('/tmp/pip-install-tuwz0wj8/pillow_306fb81069b24895a7df34c90e83edc9/setup.py',), "<pip-setuptools-caller>", "exec"))
          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
        File "<pip-setuptools-caller>", line 34, in <module>
        File "/tmp/pip-install-tuwz0wj8/pillow_306fb81069b24895a7df34c90e83edc9/setup.py", line 30, in <module>
          PILLOW_VERSION = get_version()
        File "/tmp/pip-install-tuwz0wj8/pillow_306fb81069b24895a7df34c90e83edc9/setup.py", line 26, in get_version
          return locals()["__version__"]
                 ~~~~~~~~^^^^^^^^^^^^^^^
      KeyError: '__version__'
      [end of output]
  
  note: This error originates from a subprocess, and is likely not a problem with pip.

[notice] A new release of pip is available: 24.2 -> 24.3.1
[notice] To update, run: /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33-bm-djangocms/bin/python -m pip install --upgrade pip
error: metadata-generation-failed

× Encountered error while generating package metadata.
╰─> See above for output.

note: This is an issue with the package mentioned above, not pip.
hint: See above for details.
Command failed with exit code 1


==================================================
```

</details>

## flaskblogging on linux-x86_64 default

<details>
<summary>Log for flaskblogging on linux-x86_64 default</summary>

```
# /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/bin/python -u /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_flaskblogging/run_benchmark.py --inherit-environ PYPERFORMANCE_RUNID,PYTHON_JIT --output /tmp/tmpb5lwq45c
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_flaskblogging/run_benchmark.py", line 76, in <module>
    with context:
         ^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/contextlib.py", line 141, in __enter__
    return next(self.gen)
Command failed with exit code 1
```

</details>

## gevent_hub on linux-x86_64 default

<details>
<summary>Log for gevent_hub on linux-x86_64 default</summary>

```
            src/greenlet/greenlet.c:881:38: error: ‘PyThreadState’ {aka ‘struct _ts’} has no member named ‘cframe’
              881 |     trace_info = *PyThreadState_GET()->cframe;
                  |                                      ^~
            src/greenlet/greenlet.c:888:17: error: request for member ‘previous’ in something not a structure or union
              888 |     self->cframe->previous = &PyThreadState_GET()->root_cframe;
                  |                 ^~
            src/greenlet/greenlet.c:888:50: error: ‘PyThreadState’ {aka ‘struct _ts’} has no member named ‘root_cframe’
              888 |     self->cframe->previous = &PyThreadState_GET()->root_cframe;
                  |                                                  ^~
            src/greenlet/greenlet.c:903:51: error: ‘PyThreadState’ {aka ‘struct _ts’} has no member named ‘recursion_limit’; did you mean ‘py_recursion_limit’?
              903 |     self->recursion_depth = (PyThreadState_GET()->recursion_limit
                  |                                                   ^~~~~~~~~~~~~~~
                  |                                                   py_recursion_limit
            src/greenlet/greenlet.c:904:53: error: ‘PyThreadState’ {aka ‘struct _ts’} has no member named ‘recursion_remaining’; did you mean ‘c_recursion_remaining’?
              904 |                              - PyThreadState_GET()->recursion_remaining);
                  |                                                     ^~~~~~~~~~~~~~~~~~~
                  |                                                     c_recursion_remaining
            src/greenlet/greenlet.c: In function ‘green_new’:
            src/greenlet/greenlet.c:1047:56: error: ‘PyThreadState’ {aka ‘struct _ts’} has no member named ‘root_cframe’
             1047 |         ((PyGreenlet*)o)->cframe = &PyThreadState_GET()->root_cframe;
                  |                                                        ^~
            src/greenlet/greenlet.c: In function ‘PyGreenlet_New’:
            src/greenlet/greenlet.c:1812:37: error: ‘PyThreadState’ {aka ‘struct _ts’} has no member named ‘root_cframe’
             1812 |     g->cframe = &PyThreadState_GET()->root_cframe;
                  |                                     ^~
            error: command '/usr/lib/ccache/gcc' failed with exit code 1
            [end of output]
      
        note: This error originates from a subprocess, and is likely not a problem with pip.
        ERROR: Failed building wheel for greenlet
        Running setup.py clean for greenlet
      Failed to build greenlet
      ERROR: ERROR: Failed to build installable wheels for some pyproject.toml based projects (greenlet)
      [end of output]
  
  note: This error originates from a subprocess, and is likely not a problem with pip.

[notice] A new release of pip is available: 24.2 -> 24.3.1
[notice] To update, run: /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33-bm-gevent_hub/bin/python -m pip install --upgrade pip
error: subprocess-exited-with-error

× pip subprocess to install build dependencies did not run successfully.
│ exit code: 1
╰─> See above for output.

note: This error originates from a subprocess, and is likely not a problem with pip.
Command failed with exit code 1


==================================================
```

</details>

## gunicorn on linux-x86_64 default

<details>
<summary>Log for gunicorn on linux-x86_64 default</summary>

```
# /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/bin/python -u /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_gunicorn/run_benchmark.py --inherit-environ PYPERFORMANCE_RUNID,PYTHON_JIT --output /tmp/tmp9rlst2b5
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_gunicorn/run_benchmark.py", line 84, in <module>
    with context:
Command failed with exit code 1
```

</details>

## kinto on linux-x86_64 default

<details>
<summary>Log for kinto on linux-x86_64 default</summary>

```
       1771 |   tstate->recursion_depth = up.current_main_recursion_depth;
            |         ^~
      plugins/python/python_plugin.c:1772:9: error: ‘PyThreadState’ {aka ‘struct _ts’} has no member named ‘frame’
       1772 |   tstate->frame = up.current_main_frame;
            |         ^~
      plugins/python/python_plugin.c: In function ‘uwsgi_python_mule’:
      plugins/python/python_plugin.c:1854:11: warning: assignment to ‘PyObject *’ {aka ‘struct _object *’} from ‘int’ makes pointer from integer without a cast [-Wint-conversion]
       1854 |    result = PyEval_CallObject(callable, arglist);
            |           ^
      plugins/python/python_plugin.c: In function ‘uwsgi_python_logger’:
      plugins/python/python_plugin.c:1944:28: warning: cast to pointer from integer of different size [-Wint-to-pointer-cast]
       1944 |                 ul->data = (void *) PyEval_CallObject(py_getLogger, py_getLogger_args);
            |                            ^
      plugins/gevent/gevent.c: In function ‘py_uwsgi_gevent_ctrl_gl’:
      plugins/gevent/gevent.c:36:37: warning: implicit declaration of function ‘PyEval_CallObject’; did you mean ‘PyObject_CallObject’? [-Wimplicit-function-declaration]
         36 |                 PyObject *gswitch = PyEval_CallObject(ugevent.greenlet_switch, gevent_sleep_args);
            |                                     ^~~~~~~~~~~~~~~~~
            |                                     PyObject_CallObject
      plugins/gevent/gevent.c:36:37: warning: initialization of ‘PyObject *’ {aka ‘struct _object *’} from ‘int’ makes pointer from integer without a cast [-Wint-conversion]
      plugins/python/raw.c: In function ‘uwsgi_request_python_raw’:
      plugins/python/raw.c:67:27: warning: implicit declaration of function ‘PyEval_CallObject’; did you mean ‘PyObject_CallObject’? [-Wimplicit-function-declaration]
         67 |  wsgi_req->async_result = PyEval_CallObject(up.raw_callable, args);
            |                           ^~~~~~~~~~~~~~~~~
            |                           PyObject_CallObject
      plugins/python/raw.c:67:25: warning: assignment to ‘void *’ from ‘int’ makes pointer from integer without a cast [-Wint-conversion]
         67 |  wsgi_req->async_result = PyEval_CallObject(up.raw_callable, args);
            |                         ^
      plugins/python/uwsgi_pymodule.c: In function ‘py_uwsgi_sharedarea_read’:
      plugins/python/uwsgi_pymodule.c:1825:15: error: lvalue required as left operand of assignment
       1825 |  Py_SIZE(ret) = rlen;
            |               ^
      plugins/python/profiler.c: In function ‘uwsgi_python_profiler_call’:
      plugins/python/profiler.c:38:28: error: dereferencing pointer to incomplete type ‘PyFrameObject’ {aka ‘struct _frame’}
         38 |     PyString_AsString(frame->f_code->co_filename),
            |                            ^~
      [end of output]
  
  note: This error originates from a subprocess, and is likely not a problem with pip.
  ERROR: Failed building wheel for uWSGI
  Running setup.py clean for uWSGI
Successfully built kinto
Failed to build uWSGI

[notice] A new release of pip is available: 24.2 -> 24.3.1
[notice] To update, run: /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33-bm-kinto/bin/python -m pip install --upgrade pip
ERROR: ERROR: Failed to build installable wheels for some pyproject.toml based projects (uWSGI)
Command failed with exit code 1


==================================================
```

</details>

## mypy2 on linux-x86_64 default

<details>
<summary>Log for mypy2 on linux-x86_64 default</summary>

```
Using cached pyperf-2.7.0-py3-none-any.whl (139 kB)
Using cached psutil-6.1.0-cp36-abi3-manylinux_2_12_x86_64.manylinux2010_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl (287 kB)
Building wheels for collected packages: typed-ast
  Building wheel for typed-ast (setup.py): started
  Building wheel for typed-ast (setup.py): finished with status 'error'
  error: subprocess-exited-with-error
  
  × python setup.py bdist_wheel did not run successfully.
  │ exit code: 1
  ╰─> [26 lines of output]
      running bdist_wheel
      running build
      running build_py
      creating build/lib.linux-x86_64-cpython-314/typed_ast
      copying typed_ast/__init__.py -> build/lib.linux-x86_64-cpython-314/typed_ast
      copying typed_ast/conversions.py -> build/lib.linux-x86_64-cpython-314/typed_ast
      copying typed_ast/ast3.py -> build/lib.linux-x86_64-cpython-314/typed_ast
      copying typed_ast/ast27.py -> build/lib.linux-x86_64-cpython-314/typed_ast
      creating build/lib.linux-x86_64-cpython-314/typed_ast/tests
      copying ast3/tests/test_basics.py -> build/lib.linux-x86_64-cpython-314/typed_ast/tests
      running build_ext
      building '_ast27' extension
      creating build/temp.linux-x86_64-cpython-314/ast27/Custom
      creating build/temp.linux-x86_64-cpython-314/ast27/Parser
      creating build/temp.linux-x86_64-cpython-314/ast27/Python
      gcc -pthread -fno-strict-overflow -Wsign-compare -DNDEBUG -g -O3 -Wall -fPIC -Iast27/Include -I/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33-bm-mypy2/include -I/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Include -I/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython -c ast27/Custom/typed_ast.c -o build/temp.linux-x86_64-cpython-314/ast27/Custom/typed_ast.o
      In file included from /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Include/pyport.h:377,
                       from /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Include/Python.h:63,
                       from ast27/Custom/typed_ast.c:1:
      ast27/Custom/../Include/compile.h:12:12: error: unknown type name ‘PyFutureFeatures’
         12 | PyAPI_FUNC(PyFutureFeatures *) PyFuture_FromAST(struct _mod *, const char *);
            |            ^~~~~~~~~~~~~~~~
      /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Include/exports.h:91:53: note: in definition of macro ‘PyAPI_FUNC’
         91 | #       define PyAPI_FUNC(RTYPE) Py_EXPORTED_SYMBOL RTYPE
            |                                                     ^~~~~
      error: command '/usr/lib/ccache/gcc' failed with exit code 1
      [end of output]
  
  note: This error originates from a subprocess, and is likely not a problem with pip.
  ERROR: Failed building wheel for typed-ast
  Running setup.py clean for typed-ast
Failed to build typed-ast

[notice] A new release of pip is available: 24.2 -> 24.3.1
[notice] To update, run: /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33-bm-mypy2/bin/python -m pip install --upgrade pip
ERROR: ERROR: Failed to build installable wheels for some pyproject.toml based projects (typed-ast)
Command failed with exit code 1


==================================================
```

</details>

## pytorch_alexnet_inference on linux-x86_64 default

<details>
<summary>Log for pytorch_alexnet_inference on linux-x86_64 default</summary>

```
  │ exit code: 1
  ╰─> [31 lines of output]
      Running from numpy source directory.
      <string>:460: UserWarning: Unrecognized setuptools command, proceeding with generating Cython sources and expanding templates
      Traceback (most recent call last):
        File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33-bm-pytorch_alexnet_inference/lib/python3.14/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 353, in <module>
          main()
          ~~~~^^
        File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33-bm-pytorch_alexnet_inference/lib/python3.14/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 335, in main
          json_out['return_val'] = hook(**hook_input['kwargs'])
                                   ~~~~^^^^^^^^^^^^^^^^^^^^^^^^
        File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33-bm-pytorch_alexnet_inference/lib/python3.14/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 149, in prepare_metadata_for_build_wheel
          return hook(metadata_directory, config_settings)
        File "/tmp/pip-build-env-rdwotyoy/overlay/lib/python3.14/site-packages/setuptools/build_meta.py", line 376, in prepare_metadata_for_build_wheel
          self.run_setup()
          ~~~~~~~~~~~~~~^^
        File "/tmp/pip-build-env-rdwotyoy/overlay/lib/python3.14/site-packages/setuptools/build_meta.py", line 521, in run_setup
          super().run_setup(setup_script=setup_script)
          ~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^
        File "/tmp/pip-build-env-rdwotyoy/overlay/lib/python3.14/site-packages/setuptools/build_meta.py", line 319, in run_setup
          exec(code, locals())
          ~~~~^^^^^^^^^^^^^^^^
        File "<string>", line 489, in <module>
        File "<string>", line 465, in setup_package
        File "/tmp/pip-install-m5somxdb/numpy_e7111ef83daa45be80a4f901ad0b3a2a/numpy/distutils/core.py", line 24, in <module>
          from numpy.distutils.command import config, config_compiler, \
          ...<2 lines>...
               install_clib
        File "/tmp/pip-install-m5somxdb/numpy_e7111ef83daa45be80a4f901ad0b3a2a/numpy/distutils/command/config.py", line 19, in <module>
          from numpy.distutils.mingw32ccompiler import generate_manifest
        File "/tmp/pip-install-m5somxdb/numpy_e7111ef83daa45be80a4f901ad0b3a2a/numpy/distutils/mingw32ccompiler.py", line 28, in <module>
          from distutils.msvccompiler import get_build_version as get_build_msvc_version
      ModuleNotFoundError: No module named 'distutils.msvccompiler'
      [end of output]
  
  note: This error originates from a subprocess, and is likely not a problem with pip.

[notice] A new release of pip is available: 24.2 -> 24.3.1
[notice] To update, run: /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33-bm-pytorch_alexnet_inference/bin/python -m pip install --upgrade pip
error: metadata-generation-failed

× Encountered error while generating package metadata.
╰─> See above for output.

note: This is an issue with the package mentioned above, not pip.
hint: See above for details.
Command failed with exit code 1


==================================================
```

</details>

## sqlalchemy_declarative on linux-x86_64 default

<details>
<summary>Log for sqlalchemy_declarative on linux-x86_64 default</summary>

```
        140 |     this->current_frame = tstate->cframe->current_frame;
            |                                   ^~~~~~
      src/greenlet/TPythonState.cpp:156:42: error: ‘const PyThreadState’ {aka ‘const struct _ts’} has no member named ‘trash’
        156 |     this->trash_delete_nesting = tstate->trash.delete_nesting;
            |                                          ^~~~~
      src/greenlet/TPythonState.cpp: In member function ‘void greenlet::PythonState::operator>>(PyThreadState*)’:
      src/greenlet/TPythonState.cpp:175:13: error: ‘PyThreadState’ {aka ‘struct _ts’} has no member named ‘cframe’
        175 |     tstate->cframe = this->cframe;
            |             ^~~~~~
      src/greenlet/TPythonState.cpp:175:28: error: ‘class greenlet::PythonState’ has no member named ‘cframe’
        175 |     tstate->cframe = this->cframe;
            |                            ^~~~~~
      src/greenlet/TPythonState.cpp:189:37: error: ‘C_RECURSION_LIMIT’ was not declared in this scope; did you mean ‘Py_C_RECURSION_LIMIT’?
        189 |     tstate->c_recursion_remaining = C_RECURSION_LIMIT - this->c_recursion_depth;
            |                                     ^~~~~~~~~~~~~~~~~
            |                                     Py_C_RECURSION_LIMIT
      src/greenlet/TPythonState.cpp:200:13: error: ‘PyThreadState’ {aka ‘struct _ts’} has no member named ‘cframe’
        200 |     tstate->cframe->current_frame = this->current_frame;
            |             ^~~~~~
      src/greenlet/TPythonState.cpp:206:13: error: ‘PyThreadState’ {aka ‘struct _ts’} has no member named ‘trash’
        206 |     tstate->trash.delete_nesting = this->trash_delete_nesting;
            |             ^~~~~
      src/greenlet/TPythonState.cpp: At global scope:
      src/greenlet/TPythonState.cpp:266:34: error: variable or field ‘set_new_cframe’ declared void
        266 | void PythonState::set_new_cframe(_PyCFrame& frame) noexcept
            |                                  ^~~~~~~~~
      src/greenlet/TPythonState.cpp:266:34: error: ‘_PyCFrame’ was not declared in this scope
      src/greenlet/TPythonState.cpp:266:45: error: ‘frame’ was not declared in this scope; did you mean ‘_frame’?
        266 | void PythonState::set_new_cframe(_PyCFrame& frame) noexcept
            |                                             ^~~~~
            |                                             _frame
      src/greenlet/greenlet.cpp: In function ‘PyObject* mod_get_tstate_trash_delete_nesting(PyObject*)’:
      src/greenlet/greenlet.cpp:1340:36: error: ‘PyThreadState’ {aka ‘struct _ts’} has no member named ‘trash’
       1340 |     return PyLong_FromLong(tstate->trash.delete_nesting);
            |                                    ^~~~~
      error: command '/usr/lib/ccache/g++' failed with exit code 1
      [end of output]
  
  note: This error originates from a subprocess, and is likely not a problem with pip.
  ERROR: Failed building wheel for greenlet
  Running setup.py clean for greenlet
Failed to build greenlet

[notice] A new release of pip is available: 24.2 -> 24.3.1
[notice] To update, run: /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33-bm-sqlalchemy_declarative/bin/python -m pip install --upgrade pip
ERROR: ERROR: Failed to build installable wheels for some pyproject.toml based projects (greenlet)
Command failed with exit code 1


==================================================
```

</details>

## sqlalchemy_imperative on linux-x86_64 default

<details>
<summary>Log for sqlalchemy_imperative on linux-x86_64 default</summary>

```
        140 |     this->current_frame = tstate->cframe->current_frame;
            |                                   ^~~~~~
      src/greenlet/TPythonState.cpp:156:42: error: ‘const PyThreadState’ {aka ‘const struct _ts’} has no member named ‘trash’
        156 |     this->trash_delete_nesting = tstate->trash.delete_nesting;
            |                                          ^~~~~
      src/greenlet/TPythonState.cpp: In member function ‘void greenlet::PythonState::operator>>(PyThreadState*)’:
      src/greenlet/TPythonState.cpp:175:13: error: ‘PyThreadState’ {aka ‘struct _ts’} has no member named ‘cframe’
        175 |     tstate->cframe = this->cframe;
            |             ^~~~~~
      src/greenlet/TPythonState.cpp:175:28: error: ‘class greenlet::PythonState’ has no member named ‘cframe’
        175 |     tstate->cframe = this->cframe;
            |                            ^~~~~~
      src/greenlet/TPythonState.cpp:189:37: error: ‘C_RECURSION_LIMIT’ was not declared in this scope; did you mean ‘Py_C_RECURSION_LIMIT’?
        189 |     tstate->c_recursion_remaining = C_RECURSION_LIMIT - this->c_recursion_depth;
            |                                     ^~~~~~~~~~~~~~~~~
            |                                     Py_C_RECURSION_LIMIT
      src/greenlet/TPythonState.cpp:200:13: error: ‘PyThreadState’ {aka ‘struct _ts’} has no member named ‘cframe’
        200 |     tstate->cframe->current_frame = this->current_frame;
            |             ^~~~~~
      src/greenlet/TPythonState.cpp:206:13: error: ‘PyThreadState’ {aka ‘struct _ts’} has no member named ‘trash’
        206 |     tstate->trash.delete_nesting = this->trash_delete_nesting;
            |             ^~~~~
      src/greenlet/TPythonState.cpp: At global scope:
      src/greenlet/TPythonState.cpp:266:34: error: variable or field ‘set_new_cframe’ declared void
        266 | void PythonState::set_new_cframe(_PyCFrame& frame) noexcept
            |                                  ^~~~~~~~~
      src/greenlet/TPythonState.cpp:266:34: error: ‘_PyCFrame’ was not declared in this scope
      src/greenlet/TPythonState.cpp:266:45: error: ‘frame’ was not declared in this scope; did you mean ‘_frame’?
        266 | void PythonState::set_new_cframe(_PyCFrame& frame) noexcept
            |                                             ^~~~~
            |                                             _frame
      src/greenlet/greenlet.cpp: In function ‘PyObject* mod_get_tstate_trash_delete_nesting(PyObject*)’:
      src/greenlet/greenlet.cpp:1340:36: error: ‘PyThreadState’ {aka ‘struct _ts’} has no member named ‘trash’
       1340 |     return PyLong_FromLong(tstate->trash.delete_nesting);
            |                                    ^~~~~
      error: command '/usr/lib/ccache/g++' failed with exit code 1
      [end of output]
  
  note: This error originates from a subprocess, and is likely not a problem with pip.
  ERROR: Failed building wheel for greenlet
  Running setup.py clean for greenlet
Failed to build greenlet

[notice] A new release of pip is available: 24.2 -> 24.3.1
[notice] To update, run: /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33-bm-sqlalchemy_imperative/bin/python -m pip install --upgrade pip
ERROR: ERROR: Failed to build installable wheels for some pyproject.toml based projects (greenlet)
Command failed with exit code 1


==================================================
```

</details>

## tornado_http on linux-x86_64 default

<details>
<summary>Log for tornado_http on linux-x86_64 default</summary>

```
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_tornado_http/run_benchmark.py", line 54, in make_http_server
    server.add_sockets(sockets)
    ~~~~~~~~~~~~~~~~~~^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/tornado/tcpserver.py", line 165, in add_sockets
    self._handlers[sock.fileno()] = add_accept_handler(
                                    ~~~~~~~~~~~~~~~~~~^
        sock, self._handle_connection
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/tornado/netutil.py", line 246, in add_accept_handler
    io_loop = IOLoop.current()
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/tornado/ioloop.py", line 263, in current
    loop = asyncio.get_event_loop()
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/asyncio/events.py", line 681, in get_event_loop
    raise RuntimeError('There is no current event loop in thread %r.'
                       % threading.current_thread().name)
RuntimeError: There is no current event loop in thread 'MainThread'.
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_tornado_http/run_benchmark.py", line 102, in <module>
    runner.bench_time_func('tornado_http', bench_tornado)
    ~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/pyperf/_runner.py", line 494, in bench_time_func
    result = self._main(task)
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/pyperf/_runner.py", line 460, in _main
    bench = self._manager()
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/pyperf/_runner.py", line 673, in _manager
    bench = Manager(self).create_bench()
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/pyperf/_manager.py", line 232, in create_bench
    worker_bench, run = self.create_worker_bench()
                        ~~~~~~~~~~~~~~~~~~~~~~~~^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/pyperf/_manager.py", line 131, in create_worker_bench
    suite = self.create_suite()
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/pyperf/_manager.py", line 121, in create_suite
    suite = self.spawn_worker(self.calibrate_loops, 0)
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/lib/python3.14/site-packages/pyperf/_manager.py", line 107, in spawn_worker
    raise RuntimeError("%s failed with exit code %s"
                       % (cmd[0], exitcode))
RuntimeError: /home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.14-00f3afba75e5-compat-abd8ee905c33/bin/python failed with exit code 1
Traceback (most recent call last):
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
             ^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
            ^^^^^^^^^^^^^^^^^
  File "/home/cloud-user/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/_benchmark.py", line 236, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Command failed with exit code 1
```

</details>

