| benchmark | darwin-arm64 | linux-x86_64 |
| --- | --- | --- |
| aiohttp | [[default run]](#aiohttp-on-darwin-arm64-default) | [[default run]](#aiohttp-on-linux-x86_64-default) |
| chameleon | [[default run]](#chameleon-on-darwin-arm64-default) | [[default run]](#chameleon-on-linux-x86_64-default) |
| djangocms | [[default build]](#djangocms-on-darwin-arm64-default) | [[default build]](#djangocms-on-linux-x86_64-default) |
| flaskblogging | [[default run]](#flaskblogging-on-darwin-arm64-default) | [[default run]](#flaskblogging-on-linux-x86_64-default) |
| gevent_hub | [[default build]](#gevent_hub-on-darwin-arm64-default) | [[default build]](#gevent_hub-on-linux-x86_64-default) |
| gunicorn | [[default run]](#gunicorn-on-darwin-arm64-default) | [[default run]](#gunicorn-on-linux-x86_64-default) |
| kinto | [[default build]](#kinto-on-darwin-arm64-default) | [[default build]](#kinto-on-linux-x86_64-default) |
| mypy2 | [[default build]](#mypy2-on-darwin-arm64-default) | [[default build]](#mypy2-on-linux-x86_64-default) |
| networkx | [[default run]](#networkx-on-darwin-arm64-default) | [[default run]](#networkx-on-linux-x86_64-default) |
| networkx_connected_components | [[default run]](#networkx_connected_components-on-darwin-arm64-default) | [[default run]](#networkx_connected_components-on-linux-x86_64-default) |
| networkx_k_core | [[default run]](#networkx_k_core-on-darwin-arm64-default) | [[default run]](#networkx_k_core-on-linux-x86_64-default) |
| pytorch_alexnet_inference | [[default build]](#pytorch_alexnet_inference-on-darwin-arm64-default) | [[default build]](#pytorch_alexnet_inference-on-linux-x86_64-default) |
| sqlalchemy_declarative | [[default build]](#sqlalchemy_declarative-on-darwin-arm64-default) | [[default build]](#sqlalchemy_declarative-on-linux-x86_64-default) |
| sqlalchemy_imperative | [[default build]](#sqlalchemy_imperative-on-darwin-arm64-default) | [[default build]](#sqlalchemy_imperative-on-linux-x86_64-default) |
| tornado_http | [[default run]](#tornado_http-on-darwin-arm64-default) | [[default run]](#tornado_http-on-linux-x86_64-default) |
## aiohttp on linux-x86_64 default

<details>
<summary>Log for aiohttp on linux-x86_64 default</summary>

```
# /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/bin/python -u /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_aiohttp/run_benchmark.py --inherit-environ PYPERF_PERF_RECORD_EXTRA_OPTS,PYPERFORMANCE_RUNID,PYTHON_JIT --output /tmp/tmp3ozjlo20
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

## aiohttp on darwin-arm64 default

<details>
<summary>Log for aiohttp on darwin-arm64 default</summary>

```
# /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/bin/python -u /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_aiohttp/run_benchmark.py --inherit-environ PYTHON_JIT,PYPERF_PERF_RECORD_EXTRA_OPTS,PYPERFORMANCE_RUNID --output /tmp/tmp_3dli13a
Traceback (most recent call last):
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_aiohttp/run_benchmark.py", line 69, in <module>
    with context:
         ^^^^^^^
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/contextlib.py", line 141, in __enter__
    return next(self.gen)
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_aiohttp/netutils.py", line 36, in serving
    waitUntilUp(addr)
    ~~~~~~~~~~~^^^^^^
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_aiohttp/netutils.py", line 66, in waitUntilUp
    raise Exception('Timeout reached when trying to connect')
Exception: Timeout reached when trying to connect
Traceback (most recent call last):
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
        bench_venv.python,
    ...<3 lines>...
        verbose=options.verbose,
    )
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
        python,
    ...<4 lines>...
        verbose=verbose,
    )
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/_benchmark.py", line 240, in _run_perf_script
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
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_chameleon/run_benchmark.py", line 25, in main
    tmpl = PageTemplate(BIGTABLE_ZPT)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/chameleon/zpt/template.py", line 205, in __init__
    super(PageTemplate, self).__init__(body, **config)
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/chameleon/template.py", line 137, in __init__
    self.write(body)
    ~~~~~~~~~~^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/chameleon/template.py", line 235, in write
    self.cook(body)
    ~~~~~~~~~^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/chameleon/template.py", line 167, in cook
    program = self._cook(body, digest, names)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/chameleon/template.py", line 245, in _cook
    source = self._compile(body, builtins)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/chameleon/template.py", line 276, in _compile
    program = self.parse(body)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/chameleon/zpt/template.py", line 227, in parse
    return MacroProgram(
        body, self.mode, self.filename,
    ...<9 lines>...
        tokenizer=self.tokenizer
    )
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/chameleon/zpt/program.py", line 174, in __init__
    super(MacroProgram, self).__init__(*args, **kwargs)
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/chameleon/program.py", line 35, in __init__
    node = self.visit(kind, args)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/chameleon/program.py", line 41, in visit
    return visitor(*args)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/chameleon/zpt/program.py", line 320, in visit_element
    ATTRIBUTES = self._create_attributes_nodes(
        prepared, I18N_ATTRIBUTES, STATIC_ATTRIBUTES,
    )
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/chameleon/zpt/program.py", line 794, in _create_attributes_nodes
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
```

</details>

## chameleon on darwin-arm64 default

<details>
<summary>Log for chameleon on darwin-arm64 default</summary>

```
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/chameleon/template.py", line 137, in __init__
    self.write(body)
    ~~~~~~~~~~^^^^^^
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/chameleon/template.py", line 235, in write
    self.cook(body)
    ~~~~~~~~~^^^^^^
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/chameleon/template.py", line 167, in cook
    program = self._cook(body, digest, names)
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/chameleon/template.py", line 245, in _cook
    source = self._compile(body, builtins)
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/chameleon/template.py", line 276, in _compile
    program = self.parse(body)
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/chameleon/zpt/template.py", line 227, in parse
    return MacroProgram(
        body, self.mode, self.filename,
    ...<9 lines>...
        tokenizer=self.tokenizer
    )
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/chameleon/zpt/program.py", line 174, in __init__
    super(MacroProgram, self).__init__(*args, **kwargs)
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/chameleon/program.py", line 35, in __init__
    node = self.visit(kind, args)
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/chameleon/program.py", line 41, in visit
    return visitor(*args)
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/chameleon/zpt/program.py", line 320, in visit_element
    ATTRIBUTES = self._create_attributes_nodes(
        prepared, I18N_ATTRIBUTES, STATIC_ATTRIBUTES,
    )
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/chameleon/zpt/program.py", line 794, in _create_attributes_nodes
    default = ast.Str(s=text) if text is not None else None
              ^^^^^^^
AttributeError: module 'ast' has no attribute 'Str'
Traceback (most recent call last):
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
        bench_venv.python,
    ...<3 lines>...
        verbose=options.verbose,
    )
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
        python,
    ...<4 lines>...
        verbose=verbose,
    )
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/_benchmark.py", line 240, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Command failed with exit code 1
```

</details>

## djangocms on linux-x86_64 default

<details>
<summary>Log for djangocms on linux-x86_64 default</summary>

```
  Using cached django_fsm-2.8.2-py2.py3-none-any.whl.metadata (1.9 kB)
Collecting django-parler==2.3
  Using cached django_parler-2.3-py3-none-any.whl.metadata (8.6 kB)
Collecting django-polymorphic==3.1.0
  Using cached django_polymorphic-3.1.0-py3-none-any.whl.metadata (4.6 kB)
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
      <string>:67: UserWarning: pkg_resources is deprecated as an API. See https://setuptools.pypa.io/en/latest/pkg_resources.html. The pkg_resources package is slated for removal as early as 2025-11-30. Refrain from using this package or pin to Setuptools<81.
      Building lxml version 5.3.0.
      Building without Cython.
      Error: Please make sure the libxml2 and libxslt development packages are installed.
      [end of output]
  
  note: This error originates from a subprocess, and is likely not a problem with pip.
ERROR: Failed to build 'lxml' when getting requirements to build wheel
Command failed with exit code 1


==================================================
```

</details>

## djangocms on darwin-arm64 default

<details>
<summary>Log for djangocms on darwin-arm64 default</summary>

```
              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
          )
          ^
        File "/private/tmp/pip-install-4o0iv3y5/pillow_abd49e7b4d13473b99b67f14d6ee32fc/_custom_build/backend.py", line 26, in build_wheel
          return super().build_wheel(wheel_directory, config_settings, metadata_directory)
                 ~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
        File "/private/tmp/pip-build-env-b4h4bg3r/overlay/lib/python3.15/site-packages/setuptools/build_meta.py", line 435, in build_wheel
          return _build(['bdist_wheel', '--dist-info-dir', str(metadata_directory)])
        File "/private/tmp/pip-build-env-b4h4bg3r/overlay/lib/python3.15/site-packages/setuptools/build_meta.py", line 423, in _build
          return self._build_with_temp_dir(
                 ~~~~~~~~~~~~~~~~~~~~~~~~~^
              cmd,
              ^^^^
          ...<3 lines>...
              self._arbitrary_args(config_settings),
              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
          )
          ^
        File "/private/tmp/pip-build-env-b4h4bg3r/overlay/lib/python3.15/site-packages/setuptools/build_meta.py", line 404, in _build_with_temp_dir
          self.run_setup()
          ~~~~~~~~~~~~~~^^
        File "/private/tmp/pip-install-4o0iv3y5/pillow_abd49e7b4d13473b99b67f14d6ee32fc/_custom_build/backend.py", line 20, in run_setup
          return super().run_setup(setup_script)
                 ~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^
        File "/private/tmp/pip-build-env-b4h4bg3r/overlay/lib/python3.15/site-packages/setuptools/build_meta.py", line 317, in run_setup
          exec(code, locals())
          ~~~~^^^^^^^^^^^^^^^^
        File "<string>", line 1042, in <module>
      RequiredDependencyException:
      
      The headers or library files could not be found for jpeg,
      a required dependency when compiling Pillow from source.
      
      Please see the install instructions at:
         https://pillow.readthedocs.io/en/latest/installation/basic-installation.html
      
      
      [end of output]
  
  note: This error originates from a subprocess, and is likely not a problem with pip.
  ERROR: Failed building wheel for pillow
error: failed-wheel-build-for-install

× Failed to build installable wheels for some pyproject.toml based projects
╰─> pillow
Failed to build pillow
Command failed with exit code 1


==================================================
```

</details>

## flaskblogging on linux-x86_64 default

<details>
<summary>Log for flaskblogging on linux-x86_64 default</summary>

```
# /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/bin/python -u /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_flaskblogging/run_benchmark.py --inherit-environ PYPERF_PERF_RECORD_EXTRA_OPTS,PYPERFORMANCE_RUNID,PYTHON_JIT --output /tmp/tmpty84bdjc
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

## flaskblogging on darwin-arm64 default

<details>
<summary>Log for flaskblogging on darwin-arm64 default</summary>

```
# /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/bin/python -u /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_flaskblogging/run_benchmark.py --inherit-environ PYTHON_JIT,PYPERF_PERF_RECORD_EXTRA_OPTS,PYPERFORMANCE_RUNID --output /tmp/tmp4cd_lp0u
Traceback (most recent call last):
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_flaskblogging/run_benchmark.py", line 76, in <module>
    with context:
         ^^^^^^^
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/contextlib.py", line 141, in __enter__
    return next(self.gen)
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_flaskblogging/netutils.py", line 36, in serving
    waitUntilUp(addr)
    ~~~~~~~~~~~^^^^^^
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_flaskblogging/netutils.py", line 66, in waitUntilUp
    raise Exception('Timeout reached when trying to connect')
Exception: Timeout reached when trying to connect
Traceback (most recent call last):
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
        bench_venv.python,
    ...<3 lines>...
        verbose=options.verbose,
    )
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
        python,
    ...<4 lines>...
        verbose=verbose,
    )
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/_benchmark.py", line 240, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Command failed with exit code 1
```

</details>

## gevent_hub on linux-x86_64 default

<details>
<summary>Log for gevent_hub on linux-x86_64 default</summary>

```
      else:
          integer_types = (int, long)
                                ^
      ------------------------------------------------------------
      src/gevent/libev/corecext.pyx:69:26: undeclared name not builtin: long
      Compiling src/gevent/libev/corecext.pyx because it changed.
      [1/1] Cythonizing src/gevent/libev/corecext.pyx
      Traceback (most recent call last):
        File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b-bm-gevent_hub/lib/python3.15/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 389, in <module>
          main()
          ~~~~^^
        File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b-bm-gevent_hub/lib/python3.15/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 373, in main
          json_out["return_val"] = hook(**hook_input["kwargs"])
                                   ~~~~^^^^^^^^^^^^^^^^^^^^^^^^
        File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b-bm-gevent_hub/lib/python3.15/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 143, in get_requires_for_build_wheel
          return hook(config_settings)
        File "/tmp/pip-build-env-g198laud/overlay/lib/python3.15/site-packages/setuptools/build_meta.py", line 331, in get_requires_for_build_wheel
          return self._get_build_requires(config_settings, requirements=[])
                 ~~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
        File "/tmp/pip-build-env-g198laud/overlay/lib/python3.15/site-packages/setuptools/build_meta.py", line 301, in _get_build_requires
          self.run_setup()
          ~~~~~~~~~~~~~~^^
        File "/tmp/pip-build-env-g198laud/overlay/lib/python3.15/site-packages/setuptools/build_meta.py", line 317, in run_setup
          exec(code, locals())
          ~~~~^^^^^^^^^^^^^^^^
        File "<string>", line 54, in <module>
        File "/tmp/pip-install-gcwxhk7l/gevent_209219b4b55a41d0816049c333852593/_setuputils.py", line 249, in cythonize1
          new_ext = cythonize(
                    ~~~~~~~~~^
              [ext],
              ^^^^^^
          ...<46 lines>...
              # cache="build/cycache",
              ^^^^^^^^^^^^^^^^^^^^^^^^
          )[0]
          ^
        File "/tmp/pip-build-env-g198laud/overlay/lib/python3.15/site-packages/Cython/Build/Dependencies.py", line 1153, in cythonize
          cythonize_one(*args)
          ~~~~~~~~~~~~~^^^^^^^
        File "/tmp/pip-build-env-g198laud/overlay/lib/python3.15/site-packages/Cython/Build/Dependencies.py", line 1297, in cythonize_one
          raise CompileError(None, pyx_file)
      Cython.Compiler.Errors.CompileError: src/gevent/libev/corecext.pyx
      [end of output]
  
  note: This error originates from a subprocess, and is likely not a problem with pip.
ERROR: Failed to build 'gevent' when getting requirements to build wheel
Command failed with exit code 1


==================================================
```

</details>

## gevent_hub on darwin-arm64 default

<details>
<summary>Log for gevent_hub on darwin-arm64 default</summary>

```
      else:
          integer_types = (int, long)
                                ^
      ------------------------------------------------------------
      src/gevent/libev/corecext.pyx:69:26: undeclared name not builtin: long
      Compiling src/gevent/libev/corecext.pyx because it changed.
      [1/1] Cythonizing src/gevent/libev/corecext.pyx
      Traceback (most recent call last):
        File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b-bm-gevent_hub/lib/python3.15/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 389, in <module>
          main()
          ~~~~^^
        File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b-bm-gevent_hub/lib/python3.15/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 373, in main
          json_out["return_val"] = hook(**hook_input["kwargs"])
                                   ~~~~^^^^^^^^^^^^^^^^^^^^^^^^
        File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b-bm-gevent_hub/lib/python3.15/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 143, in get_requires_for_build_wheel
          return hook(config_settings)
        File "/private/tmp/pip-build-env-u7w2v0e6/overlay/lib/python3.15/site-packages/setuptools/build_meta.py", line 331, in get_requires_for_build_wheel
          return self._get_build_requires(config_settings, requirements=[])
                 ~~~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
        File "/private/tmp/pip-build-env-u7w2v0e6/overlay/lib/python3.15/site-packages/setuptools/build_meta.py", line 301, in _get_build_requires
          self.run_setup()
          ~~~~~~~~~~~~~~^^
        File "/private/tmp/pip-build-env-u7w2v0e6/overlay/lib/python3.15/site-packages/setuptools/build_meta.py", line 317, in run_setup
          exec(code, locals())
          ~~~~^^^^^^^^^^^^^^^^
        File "<string>", line 54, in <module>
        File "/private/tmp/pip-install-zn7r4g98/gevent_54ab54adf66544bdb2d7e2d67e411164/_setuputils.py", line 249, in cythonize1
          new_ext = cythonize(
                    ~~~~~~~~~^
              [ext],
              ^^^^^^
          ...<46 lines>...
              # cache="build/cycache",
              ^^^^^^^^^^^^^^^^^^^^^^^^
          )[0]
          ^
        File "/private/tmp/pip-build-env-u7w2v0e6/overlay/lib/python3.15/site-packages/Cython/Build/Dependencies.py", line 1153, in cythonize
          cythonize_one(*args)
          ~~~~~~~~~~~~~^^^^^^^
        File "/private/tmp/pip-build-env-u7w2v0e6/overlay/lib/python3.15/site-packages/Cython/Build/Dependencies.py", line 1297, in cythonize_one
          raise CompileError(None, pyx_file)
      Cython.Compiler.Errors.CompileError: src/gevent/libev/corecext.pyx
      [end of output]
  
  note: This error originates from a subprocess, and is likely not a problem with pip.
ERROR: Failed to build 'gevent' when getting requirements to build wheel
Command failed with exit code 1


==================================================
```

</details>

## gunicorn on linux-x86_64 default

<details>
<summary>Log for gunicorn on linux-x86_64 default</summary>

```
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_gunicorn/run_benchmark.py", line 31, in bench_gunicorn
    elapsed, _ = _bench_gunicorn(loops)
                 ~~~~~~~~~~~~~~~^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_gunicorn/run_benchmark.py", line 58, in _bench_gunicorn
    requests_get("http://localhost:8000/blog/").text
    ~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/requests/api.py", line 73, in get
    return request("get", url, params=params, **kwargs)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/requests/api.py", line 59, in request
    return session.request(method=method, url=url, **kwargs)
           ~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/requests/sessions.py", line 587, in request
    resp = self.send(prep, **send_kwargs)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/requests/sessions.py", line 701, in send
    r = adapter.send(request, **kwargs)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/requests/adapters.py", line 519, in send
    raise ConnectionError(e, request=request)
requests.exceptions.ConnectionError: HTTPConnectionPool(host='localhost', port=8000): Max retries exceeded with url: /blog/ (Caused by NewConnectionError('<urllib3.connection.HTTPConnection object at 0x75d8fc9dd6a0>: Failed to establish a new connection: [Errno 111] Connection refused'))
Traceback (most recent call last):
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_gunicorn/run_benchmark.py", line 87, in <module>
    runner.bench_time_func("gunicorn", bench_gunicorn)
    ~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_runner.py", line 499, in bench_time_func
    result = self._main(task)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_runner.py", line 465, in _main
    bench = self._manager()
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_runner.py", line 678, in _manager
    bench = Manager(self).create_bench()
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_manager.py", line 243, in create_bench
    worker_bench, run = self.create_worker_bench()
                        ~~~~~~~~~~~~~~~~~~~~~~~~^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_manager.py", line 142, in create_worker_bench
    suite = self.create_suite()
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_manager.py", line 132, in create_suite
    suite = self.spawn_worker(self.calibrate_loops, 0)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_manager.py", line 118, in spawn_worker
    raise RuntimeError("%s failed with exit code %s"
                       % (cmd[0], exitcode))
RuntimeError: /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/bin/python failed with exit code 1
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

## gunicorn on darwin-arm64 default

<details>
<summary>Log for gunicorn on darwin-arm64 default</summary>

```
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/requests/api.py", line 73, in get
    return request("get", url, params=params, **kwargs)
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/requests/api.py", line 59, in request
    return session.request(method=method, url=url, **kwargs)
           ~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/requests/sessions.py", line 587, in request
    resp = self.send(prep, **send_kwargs)
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/requests/sessions.py", line 701, in send
    r = adapter.send(request, **kwargs)
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/requests/adapters.py", line 519, in send
    raise ConnectionError(e, request=request)
requests.exceptions.ConnectionError: HTTPConnectionPool(host='localhost', port=8000): Max retries exceeded with url: /blog/ (Caused by NewConnectionError('<urllib3.connection.HTTPConnection object at 0x10a88b620>: Failed to establish a new connection: [Errno 61] Connection refused'))
Traceback (most recent call last):
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/pyston-benchmarks/benchmarks/bm_gunicorn/run_benchmark.py", line 87, in <module>
    runner.bench_time_func("gunicorn", bench_gunicorn)
    ~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_runner.py", line 499, in bench_time_func
    result = self._main(task)
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_runner.py", line 465, in _main
    bench = self._manager()
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_runner.py", line 678, in _manager
    bench = Manager(self).create_bench()
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_manager.py", line 243, in create_bench
    worker_bench, run = self.create_worker_bench()
                        ~~~~~~~~~~~~~~~~~~~~~~~~^^
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_manager.py", line 142, in create_worker_bench
    suite = self.create_suite()
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_manager.py", line 132, in create_suite
    suite = self.spawn_worker(self.calibrate_loops, 0)
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_manager.py", line 118, in spawn_worker
    raise RuntimeError("%s failed with exit code %s"
                       % (cmd[0], exitcode))
RuntimeError: /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/bin/python failed with exit code 1
Traceback (most recent call last):
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
        bench_venv.python,
    ...<3 lines>...
        verbose=options.verbose,
    )
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
        python,
    ...<4 lines>...
        verbose=verbose,
    )
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/_benchmark.py", line 240, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Command failed with exit code 1
```

</details>

## kinto on linux-x86_64 default

<details>
<summary>Log for kinto on linux-x86_64 default</summary>

```
         37 | Py_DEPRECATED(3.11) PyAPI_FUNC(void) Py_SetProgramName(const wchar_t *);
            |                                      ^~~~~~~~~~~~~~~~~
      plugins/python/python_plugin.c:287:9: warning: ‘Py_OptimizeFlag’ is deprecated [-Wdeprecated-declarations]
        287 |         Py_OptimizeFlag = up.optimize;
            |         ^~~~~~~~~~~~~~~
      /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Include/cpython/pydebug.h:13:37: note: declared here
         13 | Py_DEPRECATED(3.12) PyAPI_DATA(int) Py_OptimizeFlag;
            |                                     ^~~~~~~~~~~~~~~
      plugins/python/python_plugin.c: In function ‘uwsgi_python_suspend’:
      plugins/python/python_plugin.c:1612:80: error: ‘PyThreadState’ {aka ‘struct _ts’} has no member named ‘c_recursion_remaining’; did you mean ‘py_recursion_remaining’?
       1612 |                 up.current_c_recursion_remaining[wsgi_req->async_id] = tstate->c_recursion_remaining;
            |                                                                                ^~~~~~~~~~~~~~~~~~~~~
            |                                                                                py_recursion_remaining
      plugins/python/python_plugin.c:1629:65: error: ‘PyThreadState’ {aka ‘struct _ts’} has no member named ‘c_recursion_remaining’; did you mean ‘py_recursion_remaining’?
       1629 |                 up.current_main_c_recursion_remaining = tstate->c_recursion_remaining;
            |                                                                 ^~~~~~~~~~~~~~~~~~~~~
            |                                                                 py_recursion_remaining
      plugins/python/python_plugin.c: In function ‘uwsgi_python_resume’:
      plugins/python/python_plugin.c:1873:25: error: ‘PyThreadState’ {aka ‘struct _ts’} has no member named ‘c_recursion_remaining’; did you mean ‘py_recursion_remaining’?
       1873 |                 tstate->c_recursion_remaining = up.current_c_recursion_remaining[wsgi_req->async_id];
            |                         ^~~~~~~~~~~~~~~~~~~~~
            |                         py_recursion_remaining
      plugins/python/python_plugin.c:1890:25: error: ‘PyThreadState’ {aka ‘struct _ts’} has no member named ‘c_recursion_remaining’; did you mean ‘py_recursion_remaining’?
       1890 |                 tstate->c_recursion_remaining = up.current_main_c_recursion_remaining;
            |                         ^~~~~~~~~~~~~~~~~~~~~
            |                         py_recursion_remaining
      plugins/python/pyutils.c: In function ‘init_pyargv’:
      plugins/python/pyutils.c:391:9: warning: ‘PySys_SetArgv’ is deprecated [-Wdeprecated-declarations]
        391 |         PySys_SetArgv(up.argc, up.py_argv);
            |         ^~~~~~~~~~~~~
      In file included from /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Include/Python.h:137,
                       from plugins/python/uwsgi_python.h:4,
                       from plugins/python/pyutils.c:1:
      /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Include/sysmodule.h:16:38: note: declared here
         16 | Py_DEPRECATED(3.11) PyAPI_FUNC(void) PySys_SetArgv(int, wchar_t **);
            |                                      ^~~~~~~~~~~~~
      [end of output]
  
  note: This error originates from a subprocess, and is likely not a problem with pip.
  ERROR: Failed building wheel for uWSGI
Successfully built kinto
error: failed-wheel-build-for-install

× Failed to build installable wheels for some pyproject.toml based projects
╰─> uWSGI
Failed to build uWSGI
Command failed with exit code 1


==================================================
```

</details>

## kinto on darwin-arm64 default

<details>
<summary>Log for kinto on darwin-arm64 default</summary>

```
            |         ^
      /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Include/cpython/pydebug.h:13:1: note: 'Py_OptimizeFlag' has been explicitly marked deprecated here
         13 | Py_DEPRECATED(3.12) PyAPI_DATA(int) Py_OptimizeFlag;
            | ^
      /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Include/pyport.h:281:54: note: expanded from macro 'Py_DEPRECATED'
        281 | #define Py_DEPRECATED(VERSION_UNUSED) __attribute__((__deprecated__))
            |                                                      ^
      plugins/python/python_plugin.c:1612:66: error: no member named 'c_recursion_remaining' in 'struct _ts'; did you mean 'py_recursion_remaining'?
       1612 |                 up.current_c_recursion_remaining[wsgi_req->async_id] = tstate->c_recursion_remaining;
            |                                                                                ^~~~~~~~~~~~~~~~~~~~~
            |                                                                                py_recursion_remaining
      /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Include/cpython/pystate.h:122:9: note: 'py_recursion_remaining' declared here
        122 |     int py_recursion_remaining;
            |         ^
      plugins/python/python_plugin.c:1629:51: error: no member named 'c_recursion_remaining' in 'struct _ts'; did you mean 'py_recursion_remaining'?
       1629 |                 up.current_main_c_recursion_remaining = tstate->c_recursion_remaining;
            |                                                                 ^~~~~~~~~~~~~~~~~~~~~
            |                                                                 py_recursion_remaining
      /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Include/cpython/pystate.h:122:9: note: 'py_recursion_remaining' declared here
        122 |     int py_recursion_remaining;
            |         ^
      plugins/python/python_plugin.c:1873:11: error: no member named 'c_recursion_remaining' in 'struct _ts'; did you mean 'py_recursion_remaining'?
       1873 |                 tstate->c_recursion_remaining = up.current_c_recursion_remaining[wsgi_req->async_id];
            |                         ^~~~~~~~~~~~~~~~~~~~~
            |                         py_recursion_remaining
      /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Include/cpython/pystate.h:122:9: note: 'py_recursion_remaining' declared here
        122 |     int py_recursion_remaining;
            |         ^
      plugins/python/python_plugin.c:1890:11: error: no member named 'c_recursion_remaining' in 'struct _ts'; did you mean 'py_recursion_remaining'?
       1890 |                 tstate->c_recursion_remaining = up.current_main_c_recursion_remaining;
            |                         ^~~~~~~~~~~~~~~~~~~~~
            |                         py_recursion_remaining
      /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Include/cpython/pystate.h:122:9: note: 'py_recursion_remaining' declared here
        122 |     int py_recursion_remaining;
            |         ^
      4 warnings and 4 errors generated.
      [end of output]
  
  note: This error originates from a subprocess, and is likely not a problem with pip.
  ERROR: Failed building wheel for uWSGI
Successfully built kinto
Failed to build uWSGI
error: failed-wheel-build-for-install

× Failed to build installable wheels for some pyproject.toml based projects
╰─> uWSGI
Command failed with exit code 1


==================================================
```

</details>

## mypy2 on linux-x86_64 default

<details>
<summary>Log for mypy2 on linux-x86_64 default</summary>

```
  changing mode of /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b-bm-mypy2/bin/pip3 to 755
  changing mode of /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b-bm-mypy2/bin/pip3.15 to 755
Successfully installed pip-25.3
# /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b-bm-mypy2/bin/python -m pip install -U 'setuptools>=18.5' wheel
Collecting setuptools>=18.5
  Using cached setuptools-80.9.0-py3-none-any.whl.metadata (6.6 kB)
Collecting wheel
  Using cached wheel-0.45.1-py3-none-any.whl.metadata (2.3 kB)
Using cached setuptools-80.9.0-py3-none-any.whl (1.2 MB)
Using cached wheel-0.45.1-py3-none-any.whl (72 kB)
Installing collected packages: wheel, setuptools

Successfully installed setuptools-80.9.0 wheel-0.45.1
# /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b-bm-mypy2/bin/python -m pip --version
pip 25.3 from /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b-bm-mypy2/lib/python3.15/site-packages/pip (python 3.15)
Installing requirements into the virtual environment /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b-bm-mypy2
# /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b-bm-mypy2/bin/python -m pip install --no-binary=mypy mypy==1.13.0 mypy-extensions==1.0.0 typing-extensions==4.2.0 pyperf==2.9.0
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
Collecting pyperf==2.9.0
  Using cached pyperf-2.9.0-py3-none-any.whl.metadata (5.9 kB)
INFO: pip is looking at multiple versions of mypy to determine which version is compatible with other requirements. This could take a while.
ERROR: Cannot install mypy==1.13.0 and typing-extensions==4.2.0 because these package versions have conflicting dependencies.

The conflict is caused by:
    The user requested typing-extensions==4.2.0
    mypy 1.13.0 depends on typing_extensions>=4.6.0

Additionally, some packages in these conflicts have no matching distributions available for your environment:
    typing-extensions

To fix this you could try to:
1. loosen the range of package versions you've specified
2. remove package versions to allow pip to attempt to solve the dependency conflict

ERROR: ResolutionImpossible: for help visit https://pip.pypa.io/en/latest/topics/dependency-resolution/#dealing-with-dependency-conflicts
Command failed with exit code 1


==================================================
```

</details>

## mypy2 on darwin-arm64 default

<details>
<summary>Log for mypy2 on darwin-arm64 default</summary>

```
  changing mode of /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b-bm-mypy2/bin/pip3 to 755
  changing mode of /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b-bm-mypy2/bin/pip3.15 to 755
Successfully installed pip-25.3
# /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b-bm-mypy2/bin/python -m pip install -U 'setuptools>=18.5' wheel
Collecting setuptools>=18.5
  Using cached setuptools-80.9.0-py3-none-any.whl.metadata (6.6 kB)
Collecting wheel
  Using cached wheel-0.45.1-py3-none-any.whl.metadata (2.3 kB)
Using cached setuptools-80.9.0-py3-none-any.whl (1.2 MB)
Using cached wheel-0.45.1-py3-none-any.whl (72 kB)
Installing collected packages: wheel, setuptools

Successfully installed setuptools-80.9.0 wheel-0.45.1
# /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b-bm-mypy2/bin/python -m pip --version
pip 25.3 from /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b-bm-mypy2/lib/python3.15/site-packages/pip (python 3.15)
Installing requirements into the virtual environment /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b-bm-mypy2
# /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b-bm-mypy2/bin/python -m pip install --no-binary=mypy mypy==1.13.0 mypy-extensions==1.0.0 typing-extensions==4.2.0 pyperf==2.9.0
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
Collecting pyperf==2.9.0
  Using cached pyperf-2.9.0-py3-none-any.whl.metadata (5.9 kB)
INFO: pip is looking at multiple versions of mypy to determine which version is compatible with other requirements. This could take a while.
ERROR: Cannot install mypy==1.13.0 and typing-extensions==4.2.0 because these package versions have conflicting dependencies.

The conflict is caused by:
    The user requested typing-extensions==4.2.0
    mypy 1.13.0 depends on typing_extensions>=4.6.0

Additionally, some packages in these conflicts have no matching distributions available for your environment:
    typing-extensions

To fix this you could try to:
1. loosen the range of package versions you've specified
2. remove package versions to allow pip to attempt to solve the dependency conflict

ERROR: ResolutionImpossible: for help visit https://pip.pypa.io/en/latest/topics/dependency-resolution/#dealing-with-dependency-conflicts
Command failed with exit code 1


==================================================
```

</details>

## networkx on linux-x86_64 default

<details>
<summary>Log for networkx on linux-x86_64 default</summary>

```
# /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/bin/python -u /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_networkx/run_benchmark.py shortest_path --inherit-environ PYPERF_PERF_RECORD_EXTRA_OPTS,PYPERFORMANCE_RUNID,PYTHON_JIT --output /tmp/tmpg9xckulf
Traceback (most recent call last):
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_networkx/run_benchmark.py", line 16, in <module>
    import networkx
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/networkx/__init__.py", line 19, in <module>
    from networkx import utils
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/networkx/utils/__init__.py", line 7, in <module>
    from networkx.utils.configs import *
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/networkx/utils/configs.py", line 10, in <module>
    @dataclass(init=False, eq=False, slots=True, kw_only=True, match_args=False)
     ~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/dataclasses.py", line 1427, in wrap
    return _process_class(cls, init, repr, eq, order, unsafe_hash,
                          frozen, match_args, kw_only, slots,
                          weakref_slot)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/dataclasses.py", line 1234, in _process_class
    cls = _add_slots(cls, frozen, weakref_slot, fields)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/dataclasses.py", line 1402, in _add_slots
    init_annotate = newcls.__init__.__annotate__
                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^
AttributeError: 'wrapper_descriptor' object has no attribute '__annotate__'. Did you mean: '__getstate__'?
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

## networkx on darwin-arm64 default

<details>
<summary>Log for networkx on darwin-arm64 default</summary>

```
# /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/bin/python -u /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/data-files/benchmarks/bm_networkx/run_benchmark.py shortest_path --inherit-environ PYTHON_JIT,PYPERF_PERF_RECORD_EXTRA_OPTS,PYPERFORMANCE_RUNID --output /tmp/tmppc2_irvw
Traceback (most recent call last):
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/data-files/benchmarks/bm_networkx/run_benchmark.py", line 16, in <module>
    import networkx
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/networkx/__init__.py", line 19, in <module>
    from networkx import utils
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/networkx/utils/__init__.py", line 7, in <module>
    from networkx.utils.configs import *
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/networkx/utils/configs.py", line 10, in <module>
    @dataclass(init=False, eq=False, slots=True, kw_only=True, match_args=False)
     ~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/dataclasses.py", line 1427, in wrap
    return _process_class(cls, init, repr, eq, order, unsafe_hash,
                          frozen, match_args, kw_only, slots,
                          weakref_slot)
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/dataclasses.py", line 1234, in _process_class
    cls = _add_slots(cls, frozen, weakref_slot, fields)
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/dataclasses.py", line 1402, in _add_slots
    init_annotate = newcls.__init__.__annotate__
                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^
AttributeError: 'wrapper_descriptor' object has no attribute '__annotate__'. Did you mean: '__getstate__'?
Traceback (most recent call last):
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
        bench_venv.python,
    ...<3 lines>...
        verbose=options.verbose,
    )
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
        python,
    ...<4 lines>...
        verbose=verbose,
    )
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/_benchmark.py", line 240, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Command failed with exit code 1
```

</details>

## networkx_connected_components on linux-x86_64 default

<details>
<summary>Log for networkx_connected_components on linux-x86_64 default</summary>

```
# /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/bin/python -u /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_networkx/run_benchmark.py connected_components --inherit-environ PYPERF_PERF_RECORD_EXTRA_OPTS,PYPERFORMANCE_RUNID,PYTHON_JIT --output /tmp/tmpgsa45ve_
Traceback (most recent call last):
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_networkx/run_benchmark.py", line 16, in <module>
    import networkx
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/networkx/__init__.py", line 19, in <module>
    from networkx import utils
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/networkx/utils/__init__.py", line 7, in <module>
    from networkx.utils.configs import *
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/networkx/utils/configs.py", line 10, in <module>
    @dataclass(init=False, eq=False, slots=True, kw_only=True, match_args=False)
     ~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/dataclasses.py", line 1427, in wrap
    return _process_class(cls, init, repr, eq, order, unsafe_hash,
                          frozen, match_args, kw_only, slots,
                          weakref_slot)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/dataclasses.py", line 1234, in _process_class
    cls = _add_slots(cls, frozen, weakref_slot, fields)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/dataclasses.py", line 1402, in _add_slots
    init_annotate = newcls.__init__.__annotate__
                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^
AttributeError: 'wrapper_descriptor' object has no attribute '__annotate__'. Did you mean: '__getstate__'?
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

## networkx_connected_components on darwin-arm64 default

<details>
<summary>Log for networkx_connected_components on darwin-arm64 default</summary>

```
# /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/bin/python -u /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/data-files/benchmarks/bm_networkx/run_benchmark.py connected_components --inherit-environ PYTHON_JIT,PYPERF_PERF_RECORD_EXTRA_OPTS,PYPERFORMANCE_RUNID --output /tmp/tmpsc4oxpp2
Traceback (most recent call last):
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/data-files/benchmarks/bm_networkx/run_benchmark.py", line 16, in <module>
    import networkx
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/networkx/__init__.py", line 19, in <module>
    from networkx import utils
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/networkx/utils/__init__.py", line 7, in <module>
    from networkx.utils.configs import *
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/networkx/utils/configs.py", line 10, in <module>
    @dataclass(init=False, eq=False, slots=True, kw_only=True, match_args=False)
     ~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/dataclasses.py", line 1427, in wrap
    return _process_class(cls, init, repr, eq, order, unsafe_hash,
                          frozen, match_args, kw_only, slots,
                          weakref_slot)
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/dataclasses.py", line 1234, in _process_class
    cls = _add_slots(cls, frozen, weakref_slot, fields)
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/dataclasses.py", line 1402, in _add_slots
    init_annotate = newcls.__init__.__annotate__
                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^
AttributeError: 'wrapper_descriptor' object has no attribute '__annotate__'. Did you mean: '__getstate__'?
Traceback (most recent call last):
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
        bench_venv.python,
    ...<3 lines>...
        verbose=options.verbose,
    )
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
        python,
    ...<4 lines>...
        verbose=verbose,
    )
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/_benchmark.py", line 240, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Command failed with exit code 1
```

</details>

## networkx_k_core on linux-x86_64 default

<details>
<summary>Log for networkx_k_core on linux-x86_64 default</summary>

```
# /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/bin/python -u /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_networkx/run_benchmark.py k_core --inherit-environ PYPERF_PERF_RECORD_EXTRA_OPTS,PYPERFORMANCE_RUNID,PYTHON_JIT --output /tmp/tmpnuh9wyzx
Traceback (most recent call last):
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_networkx/run_benchmark.py", line 16, in <module>
    import networkx
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/networkx/__init__.py", line 19, in <module>
    from networkx import utils
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/networkx/utils/__init__.py", line 7, in <module>
    from networkx.utils.configs import *
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/networkx/utils/configs.py", line 10, in <module>
    @dataclass(init=False, eq=False, slots=True, kw_only=True, match_args=False)
     ~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/dataclasses.py", line 1427, in wrap
    return _process_class(cls, init, repr, eq, order, unsafe_hash,
                          frozen, match_args, kw_only, slots,
                          weakref_slot)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/dataclasses.py", line 1234, in _process_class
    cls = _add_slots(cls, frozen, weakref_slot, fields)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/dataclasses.py", line 1402, in _add_slots
    init_annotate = newcls.__init__.__annotate__
                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^
AttributeError: 'wrapper_descriptor' object has no attribute '__annotate__'. Did you mean: '__getstate__'?
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

## networkx_k_core on darwin-arm64 default

<details>
<summary>Log for networkx_k_core on darwin-arm64 default</summary>

```
# /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/bin/python -u /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/data-files/benchmarks/bm_networkx/run_benchmark.py k_core --inherit-environ PYTHON_JIT,PYPERF_PERF_RECORD_EXTRA_OPTS,PYPERFORMANCE_RUNID --output /tmp/tmp_70vevsw
Traceback (most recent call last):
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/data-files/benchmarks/bm_networkx/run_benchmark.py", line 16, in <module>
    import networkx
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/networkx/__init__.py", line 19, in <module>
    from networkx import utils
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/networkx/utils/__init__.py", line 7, in <module>
    from networkx.utils.configs import *
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/networkx/utils/configs.py", line 10, in <module>
    @dataclass(init=False, eq=False, slots=True, kw_only=True, match_args=False)
     ~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/dataclasses.py", line 1427, in wrap
    return _process_class(cls, init, repr, eq, order, unsafe_hash,
                          frozen, match_args, kw_only, slots,
                          weakref_slot)
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/dataclasses.py", line 1234, in _process_class
    cls = _add_slots(cls, frozen, weakref_slot, fields)
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/dataclasses.py", line 1402, in _add_slots
    init_annotate = newcls.__init__.__annotate__
                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^
AttributeError: 'wrapper_descriptor' object has no attribute '__annotate__'. Did you mean: '__getstate__'?
Traceback (most recent call last):
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
        bench_venv.python,
    ...<3 lines>...
        verbose=options.verbose,
    )
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
        python,
    ...<4 lines>...
        verbose=verbose,
    )
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/_benchmark.py", line 240, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
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
        File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b-bm-pytorch_alexnet_inference/lib/python3.15/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 389, in <module>
          main()
          ~~~~^^
        File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b-bm-pytorch_alexnet_inference/lib/python3.15/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 373, in main
          json_out["return_val"] = hook(**hook_input["kwargs"])
                                   ~~~~^^^^^^^^^^^^^^^^^^^^^^^^
        File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b-bm-pytorch_alexnet_inference/lib/python3.15/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 175, in prepare_metadata_for_build_wheel
          return hook(metadata_directory, config_settings)
        File "/tmp/pip-build-env-pd3x4bv7/overlay/lib/python3.15/site-packages/setuptools/build_meta.py", line 374, in prepare_metadata_for_build_wheel
          self.run_setup()
          ~~~~~~~~~~~~~~^^
        File "/tmp/pip-build-env-pd3x4bv7/overlay/lib/python3.15/site-packages/setuptools/build_meta.py", line 512, in run_setup
          super().run_setup(setup_script=setup_script)
          ~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^
        File "/tmp/pip-build-env-pd3x4bv7/overlay/lib/python3.15/site-packages/setuptools/build_meta.py", line 317, in run_setup
          exec(code, locals())
          ~~~~^^^^^^^^^^^^^^^^
        File "<string>", line 489, in <module>
        File "<string>", line 465, in setup_package
        File "/tmp/pip-install-tllwfswp/numpy_d5e9cb6f284c439cb62ecbd9d8634a97/numpy/distutils/core.py", line 24, in <module>
          from numpy.distutils.command import config, config_compiler, \
          ...<2 lines>...
               install_clib
        File "/tmp/pip-install-tllwfswp/numpy_d5e9cb6f284c439cb62ecbd9d8634a97/numpy/distutils/command/config.py", line 19, in <module>
          from numpy.distutils.mingw32ccompiler import generate_manifest
        File "/tmp/pip-install-tllwfswp/numpy_d5e9cb6f284c439cb62ecbd9d8634a97/numpy/distutils/mingw32ccompiler.py", line 28, in <module>
          from distutils.msvccompiler import get_build_version as get_build_msvc_version
      ModuleNotFoundError: No module named 'distutils.msvccompiler'
      [end of output]
  
  note: This error originates from a subprocess, and is likely not a problem with pip.
error: metadata-generation-failed

× Encountered error while generating package metadata.
╰─> numpy

note: This is an issue with the package mentioned above, not pip.
hint: See above for details.
Command failed with exit code 1


==================================================
```

</details>

## pytorch_alexnet_inference on darwin-arm64 default

<details>
<summary>Log for pytorch_alexnet_inference on darwin-arm64 default</summary>

```
  error: subprocess-exited-with-error
  
  × Preparing metadata (pyproject.toml) did not run successfully.
  │ exit code: 1
  ╰─> [31 lines of output]
      Running from numpy source directory.
      <string>:460: UserWarning: Unrecognized setuptools command, proceeding with generating Cython sources and expanding templates
      Traceback (most recent call last):
        File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b-bm-pytorch_alexnet_inference/lib/python3.15/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 389, in <module>
          main()
          ~~~~^^
        File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b-bm-pytorch_alexnet_inference/lib/python3.15/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 373, in main
          json_out["return_val"] = hook(**hook_input["kwargs"])
                                   ~~~~^^^^^^^^^^^^^^^^^^^^^^^^
        File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b-bm-pytorch_alexnet_inference/lib/python3.15/site-packages/pip/_vendor/pyproject_hooks/_in_process/_in_process.py", line 175, in prepare_metadata_for_build_wheel
          return hook(metadata_directory, config_settings)
        File "/private/tmp/pip-build-env-vubnqz44/overlay/lib/python3.15/site-packages/setuptools/build_meta.py", line 374, in prepare_metadata_for_build_wheel
          self.run_setup()
          ~~~~~~~~~~~~~~^^
        File "/private/tmp/pip-build-env-vubnqz44/overlay/lib/python3.15/site-packages/setuptools/build_meta.py", line 512, in run_setup
          super().run_setup(setup_script=setup_script)
          ~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^
        File "/private/tmp/pip-build-env-vubnqz44/overlay/lib/python3.15/site-packages/setuptools/build_meta.py", line 317, in run_setup
          exec(code, locals())
          ~~~~^^^^^^^^^^^^^^^^
        File "<string>", line 489, in <module>
        File "<string>", line 465, in setup_package
        File "/private/tmp/pip-install-psgj37ui/numpy_e2a4a95beac9409d959d72baf7c9ac3e/numpy/distutils/core.py", line 24, in <module>
          from numpy.distutils.command import config, config_compiler, \
          ...<2 lines>...
               install_clib
        File "/private/tmp/pip-install-psgj37ui/numpy_e2a4a95beac9409d959d72baf7c9ac3e/numpy/distutils/command/config.py", line 19, in <module>
          from numpy.distutils.mingw32ccompiler import generate_manifest
        File "/private/tmp/pip-install-psgj37ui/numpy_e2a4a95beac9409d959d72baf7c9ac3e/numpy/distutils/mingw32ccompiler.py", line 28, in <module>
          from distutils.msvccompiler import get_build_version as get_build_msvc_version
      ModuleNotFoundError: No module named 'distutils.msvccompiler'
      [end of output]
  
  note: This error originates from a subprocess, and is likely not a problem with pip.
error: metadata-generation-failed

× Encountered error while generating package metadata.
╰─> numpy

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
      In file included from src/greenlet/greenlet.cpp:36:
      src/greenlet/TPythonState.cpp: In member function ‘void greenlet::PythonState::operator<<(const PyThreadState*)’:
      src/greenlet/TPythonState.cpp:137:31: error: ‘Py_C_RECURSION_LIMIT’ was not declared in this scope
        137 |     this->c_recursion_depth = Py_C_RECURSION_LIMIT - tstate->c_recursion_remaining;
            |                               ^~~~~~~~~~~~~~~~~~~~
      src/greenlet/TPythonState.cpp:137:62: error: ‘const PyThreadState’ {aka ‘const struct _ts’} has no member named ‘c_recursion_remaining’; did you mean ‘py_recursion_remaining’?
        137 |     this->c_recursion_depth = Py_C_RECURSION_LIMIT - tstate->c_recursion_remaining;
            |                                                              ^~~~~~~~~~~~~~~~~~~~~
            |                                                              py_recursion_remaining
      src/greenlet/TPythonState.cpp: In member function ‘void greenlet::PythonState::unexpose_frames()’:
      src/greenlet/TPythonState.cpp:179:51: error: invalid use of incomplete type ‘_PyInterpreterFrame’ {aka ‘struct _PyInterpreterFrame’}
        179 |         _PyInterpreterFrame *prev_exposed = iframe->previous;
            |                                                   ^~
      /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Include/cpython/pyframe.h:25:8: note: forward declaration of ‘_PyInterpreterFrame’ {aka ‘struct _PyInterpreterFrame’}
         25 | struct _PyInterpreterFrame;
            |        ^~~~~~~~~~~~~~~~~~~
      src/greenlet/TPythonState.cpp:181:23: error: invalid use of incomplete type ‘_PyInterpreterFrame’ {aka ‘struct _PyInterpreterFrame’}
        181 |         memcpy(&iframe->previous, &iframe->frame_obj->_f_frame_data[0],
            |                       ^~
      /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Include/cpython/pyframe.h:25:8: note: forward declaration of ‘_PyInterpreterFrame’ {aka ‘struct _PyInterpreterFrame’}
         25 | struct _PyInterpreterFrame;
            |        ^~~~~~~~~~~~~~~~~~~
      src/greenlet/TPythonState.cpp:181:42: error: invalid use of incomplete type ‘_PyInterpreterFrame’ {aka ‘struct _PyInterpreterFrame’}
        181 |         memcpy(&iframe->previous, &iframe->frame_obj->_f_frame_data[0],
            |                                          ^~
      /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Include/cpython/pyframe.h:25:8: note: forward declaration of ‘_PyInterpreterFrame’ {aka ‘struct _PyInterpreterFrame’}
         25 | struct _PyInterpreterFrame;
            |        ^~~~~~~~~~~~~~~~~~~
      src/greenlet/TPythonState.cpp: In member function ‘void greenlet::PythonState::operator>>(PyThreadState*)’:
      src/greenlet/TPythonState.cpp:212:13: error: ‘PyThreadState’ {aka ‘struct _ts’} has no member named ‘c_recursion_remaining’; did you mean ‘py_recursion_remaining’?
        212 |     tstate->c_recursion_remaining = Py_C_RECURSION_LIMIT - this->c_recursion_depth;
            |             ^~~~~~~~~~~~~~~~~~~~~
            |             py_recursion_remaining
      src/greenlet/TPythonState.cpp:212:37: error: ‘Py_C_RECURSION_LIMIT’ was not declared in this scope
        212 |     tstate->c_recursion_remaining = Py_C_RECURSION_LIMIT - this->c_recursion_depth;
            |                                     ^~~~~~~~~~~~~~~~~~~~
      error: command '/usr/bin/g++' failed with exit code 1
      [end of output]
  
  note: This error originates from a subprocess, and is likely not a problem with pip.
  ERROR: Failed building wheel for greenlet
Failed to build greenlet
error: failed-wheel-build-for-install

× Failed to build installable wheels for some pyproject.toml based projects
╰─> greenlet
Command failed with exit code 1


==================================================
```

</details>

## sqlalchemy_declarative on darwin-arm64 default

<details>
<summary>Log for sqlalchemy_declarative on darwin-arm64 default</summary>

```
            |        ^
      In file included from src/greenlet/greenlet.cpp:36:
      src/greenlet/TPythonState.cpp:137:31: error: use of undeclared identifier 'Py_C_RECURSION_LIMIT'
        137 |     this->c_recursion_depth = Py_C_RECURSION_LIMIT - tstate->c_recursion_remaining;
            |                               ^
      src/greenlet/TPythonState.cpp:137:62: error: no member named 'c_recursion_remaining' in '_ts'
        137 |     this->c_recursion_depth = Py_C_RECURSION_LIMIT - tstate->c_recursion_remaining;
            |                                                      ~~~~~~  ^
      src/greenlet/TPythonState.cpp:179:51: error: member access into incomplete type '_PyInterpreterFrame'
        179 |         _PyInterpreterFrame *prev_exposed = iframe->previous;
            |                                                   ^
      /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Include/cpython/pyframe.h:25:8: note: forward declaration of '_PyInterpreterFrame'
         25 | struct _PyInterpreterFrame;
            |        ^
      In file included from src/greenlet/greenlet.cpp:36:
      src/greenlet/TPythonState.cpp:181:23: error: member access into incomplete type '_PyInterpreterFrame'
        181 |         memcpy(&iframe->previous, &iframe->frame_obj->_f_frame_data[0],
            |                       ^
      /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Include/cpython/pyframe.h:25:8: note: forward declaration of '_PyInterpreterFrame'
         25 | struct _PyInterpreterFrame;
            |        ^
      In file included from src/greenlet/greenlet.cpp:36:
      src/greenlet/TPythonState.cpp:181:42: error: member access into incomplete type '_PyInterpreterFrame'
        181 |         memcpy(&iframe->previous, &iframe->frame_obj->_f_frame_data[0],
            |                                          ^
      /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Include/cpython/pyframe.h:25:8: note: forward declaration of '_PyInterpreterFrame'
         25 | struct _PyInterpreterFrame;
            |        ^
      In file included from src/greenlet/greenlet.cpp:36:
      src/greenlet/TPythonState.cpp:212:13: error: no member named 'c_recursion_remaining' in '_ts'
        212 |     tstate->c_recursion_remaining = Py_C_RECURSION_LIMIT - this->c_recursion_depth;
            |     ~~~~~~  ^
      src/greenlet/TPythonState.cpp:212:37: error: use of undeclared identifier 'Py_C_RECURSION_LIMIT'
        212 |     tstate->c_recursion_remaining = Py_C_RECURSION_LIMIT - this->c_recursion_depth;
            |                                     ^
      18 errors generated.
      error: command '/opt/homebrew/opt/ccache/libexec/clang++' failed with exit code 1
      [end of output]
  
  note: This error originates from a subprocess, and is likely not a problem with pip.
  ERROR: Failed building wheel for greenlet
error: failed-wheel-build-for-install

× Failed to build installable wheels for some pyproject.toml based projects
╰─> greenlet
Failed to build greenlet
Command failed with exit code 1


==================================================
```

</details>

## sqlalchemy_imperative on linux-x86_64 default

<details>
<summary>Log for sqlalchemy_imperative on linux-x86_64 default</summary>

```
      In file included from src/greenlet/greenlet.cpp:36:
      src/greenlet/TPythonState.cpp: In member function ‘void greenlet::PythonState::operator<<(const PyThreadState*)’:
      src/greenlet/TPythonState.cpp:137:31: error: ‘Py_C_RECURSION_LIMIT’ was not declared in this scope
        137 |     this->c_recursion_depth = Py_C_RECURSION_LIMIT - tstate->c_recursion_remaining;
            |                               ^~~~~~~~~~~~~~~~~~~~
      src/greenlet/TPythonState.cpp:137:62: error: ‘const PyThreadState’ {aka ‘const struct _ts’} has no member named ‘c_recursion_remaining’; did you mean ‘py_recursion_remaining’?
        137 |     this->c_recursion_depth = Py_C_RECURSION_LIMIT - tstate->c_recursion_remaining;
            |                                                              ^~~~~~~~~~~~~~~~~~~~~
            |                                                              py_recursion_remaining
      src/greenlet/TPythonState.cpp: In member function ‘void greenlet::PythonState::unexpose_frames()’:
      src/greenlet/TPythonState.cpp:179:51: error: invalid use of incomplete type ‘_PyInterpreterFrame’ {aka ‘struct _PyInterpreterFrame’}
        179 |         _PyInterpreterFrame *prev_exposed = iframe->previous;
            |                                                   ^~
      /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Include/cpython/pyframe.h:25:8: note: forward declaration of ‘_PyInterpreterFrame’ {aka ‘struct _PyInterpreterFrame’}
         25 | struct _PyInterpreterFrame;
            |        ^~~~~~~~~~~~~~~~~~~
      src/greenlet/TPythonState.cpp:181:23: error: invalid use of incomplete type ‘_PyInterpreterFrame’ {aka ‘struct _PyInterpreterFrame’}
        181 |         memcpy(&iframe->previous, &iframe->frame_obj->_f_frame_data[0],
            |                       ^~
      /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Include/cpython/pyframe.h:25:8: note: forward declaration of ‘_PyInterpreterFrame’ {aka ‘struct _PyInterpreterFrame’}
         25 | struct _PyInterpreterFrame;
            |        ^~~~~~~~~~~~~~~~~~~
      src/greenlet/TPythonState.cpp:181:42: error: invalid use of incomplete type ‘_PyInterpreterFrame’ {aka ‘struct _PyInterpreterFrame’}
        181 |         memcpy(&iframe->previous, &iframe->frame_obj->_f_frame_data[0],
            |                                          ^~
      /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Include/cpython/pyframe.h:25:8: note: forward declaration of ‘_PyInterpreterFrame’ {aka ‘struct _PyInterpreterFrame’}
         25 | struct _PyInterpreterFrame;
            |        ^~~~~~~~~~~~~~~~~~~
      src/greenlet/TPythonState.cpp: In member function ‘void greenlet::PythonState::operator>>(PyThreadState*)’:
      src/greenlet/TPythonState.cpp:212:13: error: ‘PyThreadState’ {aka ‘struct _ts’} has no member named ‘c_recursion_remaining’; did you mean ‘py_recursion_remaining’?
        212 |     tstate->c_recursion_remaining = Py_C_RECURSION_LIMIT - this->c_recursion_depth;
            |             ^~~~~~~~~~~~~~~~~~~~~
            |             py_recursion_remaining
      src/greenlet/TPythonState.cpp:212:37: error: ‘Py_C_RECURSION_LIMIT’ was not declared in this scope
        212 |     tstate->c_recursion_remaining = Py_C_RECURSION_LIMIT - this->c_recursion_depth;
            |                                     ^~~~~~~~~~~~~~~~~~~~
      error: command '/usr/bin/g++' failed with exit code 1
      [end of output]
  
  note: This error originates from a subprocess, and is likely not a problem with pip.
  ERROR: Failed building wheel for greenlet
error: failed-wheel-build-for-install

× Failed to build installable wheels for some pyproject.toml based projects
╰─> greenlet
Failed to build greenlet
Command failed with exit code 1


==================================================
```

</details>

## sqlalchemy_imperative on darwin-arm64 default

<details>
<summary>Log for sqlalchemy_imperative on darwin-arm64 default</summary>

```
            |        ^
      In file included from src/greenlet/greenlet.cpp:36:
      src/greenlet/TPythonState.cpp:137:31: error: use of undeclared identifier 'Py_C_RECURSION_LIMIT'
        137 |     this->c_recursion_depth = Py_C_RECURSION_LIMIT - tstate->c_recursion_remaining;
            |                               ^
      src/greenlet/TPythonState.cpp:137:62: error: no member named 'c_recursion_remaining' in '_ts'
        137 |     this->c_recursion_depth = Py_C_RECURSION_LIMIT - tstate->c_recursion_remaining;
            |                                                      ~~~~~~  ^
      src/greenlet/TPythonState.cpp:179:51: error: member access into incomplete type '_PyInterpreterFrame'
        179 |         _PyInterpreterFrame *prev_exposed = iframe->previous;
            |                                                   ^
      /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Include/cpython/pyframe.h:25:8: note: forward declaration of '_PyInterpreterFrame'
         25 | struct _PyInterpreterFrame;
            |        ^
      In file included from src/greenlet/greenlet.cpp:36:
      src/greenlet/TPythonState.cpp:181:23: error: member access into incomplete type '_PyInterpreterFrame'
        181 |         memcpy(&iframe->previous, &iframe->frame_obj->_f_frame_data[0],
            |                       ^
      /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Include/cpython/pyframe.h:25:8: note: forward declaration of '_PyInterpreterFrame'
         25 | struct _PyInterpreterFrame;
            |        ^
      In file included from src/greenlet/greenlet.cpp:36:
      src/greenlet/TPythonState.cpp:181:42: error: member access into incomplete type '_PyInterpreterFrame'
        181 |         memcpy(&iframe->previous, &iframe->frame_obj->_f_frame_data[0],
            |                                          ^
      /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Include/cpython/pyframe.h:25:8: note: forward declaration of '_PyInterpreterFrame'
         25 | struct _PyInterpreterFrame;
            |        ^
      In file included from src/greenlet/greenlet.cpp:36:
      src/greenlet/TPythonState.cpp:212:13: error: no member named 'c_recursion_remaining' in '_ts'
        212 |     tstate->c_recursion_remaining = Py_C_RECURSION_LIMIT - this->c_recursion_depth;
            |     ~~~~~~  ^
      src/greenlet/TPythonState.cpp:212:37: error: use of undeclared identifier 'Py_C_RECURSION_LIMIT'
        212 |     tstate->c_recursion_remaining = Py_C_RECURSION_LIMIT - this->c_recursion_depth;
            |                                     ^
      18 errors generated.
      error: command '/opt/homebrew/opt/ccache/libexec/clang++' failed with exit code 1
      [end of output]
  
  note: This error originates from a subprocess, and is likely not a problem with pip.
  ERROR: Failed building wheel for greenlet
error: failed-wheel-build-for-install

× Failed to build installable wheels for some pyproject.toml based projects
╰─> greenlet
Failed to build greenlet
Command failed with exit code 1


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
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/tornado/tcpserver.py", line 204, in add_sockets
    self._handlers[sock.fileno()] = add_accept_handler(
                                    ~~~~~~~~~~~~~~~~~~^
        sock, self._handle_connection
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/tornado/netutil.py", line 247, in add_accept_handler
    io_loop = IOLoop.current()
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/tornado/ioloop.py", line 265, in current
    loop = asyncio.get_event_loop()
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/asyncio/events.py", line 715, in get_event_loop
    raise RuntimeError('There is no current event loop in thread %r.'
                       % threading.current_thread().name)
RuntimeError: There is no current event loop in thread 'MainThread'.
Traceback (most recent call last):
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.11/site-packages/pyperformance/data-files/benchmarks/bm_tornado_http/run_benchmark.py", line 102, in <module>
    runner.bench_time_func('tornado_http', bench_tornado)
    ~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_runner.py", line 499, in bench_time_func
    result = self._main(task)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_runner.py", line 465, in _main
    bench = self._manager()
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_runner.py", line 678, in _manager
    bench = Manager(self).create_bench()
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_manager.py", line 243, in create_bench
    worker_bench, run = self.create_worker_bench()
                        ~~~~~~~~~~~~~~~~~~~~~~~~^^
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_manager.py", line 142, in create_worker_bench
    suite = self.create_suite()
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_manager.py", line 132, in create_suite
    suite = self.spawn_worker(self.calibrate_loops, 0)
  File "/home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_manager.py", line 118, in spawn_worker
    raise RuntimeError("%s failed with exit code %s"
                       % (cmd[0], exitcode))
RuntimeError: /home/actions_runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-af4fd726c5ba-compat-64aaec271e6b/bin/python failed with exit code 1
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

## tornado_http on darwin-arm64 default

<details>
<summary>Log for tornado_http on darwin-arm64 default</summary>

```
        sock, self._handle_connection
        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    )
    ^
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/tornado/netutil.py", line 247, in add_accept_handler
    io_loop = IOLoop.current()
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/tornado/ioloop.py", line 265, in current
    loop = asyncio.get_event_loop()
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/cpython/Lib/asyncio/events.py", line 715, in get_event_loop
    raise RuntimeError('There is no current event loop in thread %r.'
                       % threading.current_thread().name)
RuntimeError: There is no current event loop in thread 'MainThread'.
Traceback (most recent call last):
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/data-files/benchmarks/bm_tornado_http/run_benchmark.py", line 102, in <module>
    runner.bench_time_func('tornado_http', bench_tornado)
    ~~~~~~~~~~~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_runner.py", line 499, in bench_time_func
    result = self._main(task)
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_runner.py", line 465, in _main
    bench = self._manager()
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_runner.py", line 678, in _manager
    bench = Manager(self).create_bench()
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_manager.py", line 243, in create_bench
    worker_bench, run = self.create_worker_bench()
                        ~~~~~~~~~~~~~~~~~~~~~~~~^^
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_manager.py", line 142, in create_worker_bench
    suite = self.create_suite()
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_manager.py", line 132, in create_suite
    suite = self.spawn_worker(self.calibrate_loops, 0)
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/lib/python3.15/site-packages/pyperf/_manager.py", line 118, in spawn_worker
    raise RuntimeError("%s failed with exit code %s"
                       % (cmd[0], exitcode))
RuntimeError: /Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/cpython3.15-3630c6d41b41-compat-64aaec271e6b/bin/python failed with exit code 1
Traceback (most recent call last):
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/run.py", line 170, in run_benchmarks
    result = bench.run(
        bench_venv.python,
    ...<3 lines>...
        verbose=options.verbose,
    )
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/_benchmark.py", line 189, in run
    bench = _run_perf_script(
        python,
    ...<4 lines>...
        verbose=verbose,
    )
  File "/Users/meta-runner/actions-runner/_work/free-threading-benchmarking/free-threading-benchmarking/venv/lib/python3.13/site-packages/pyperformance/_benchmark.py", line 240, in _run_perf_script
    raise RuntimeError("Benchmark died")
RuntimeError: Benchmark died
Command failed with exit code 1
```

</details>

