# Results

- fork: python
- version: 3.14.0a0
- config: NOGIL
- commit hash: [44052b5](https://github.com/python/cpython/commit/44052b5)
- commit date: 2024-09-16T20:22:30+03:00
- commit merge base: [05235e3c16d755e292ebf6e2bd6c4903bb6849b9](https://github.com/python/cpython/commit/05235e3c16d755e292ebf6e2bd6c4903bb6849b9)
- ref: main

## linux x86_64 (linux)

- [GitHub Action run](https://github.com/facebookexperimental/free-threading-benchmarking/actions/runs/10890274730)
- cpu model: Intel(R) Xeon(R) Platinum 8259CL CPU @ 2.50GHz
- platform: Linux-5.15.0-1063-aws-x86_64-with-glibc2.31
- [raw results](bm-20240916-linux-x86_64-python-main-3.14.0a0-44052b5.json)

### vs. 3.12.6

- Geometric mean: not sig (HPT: reliability of 84.13%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: 2to3, aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, asyncio_tcp, asyncio_tcp_ssl, asyncio_websockets, bench_mp_pool, bench_thread_pool, bpe_tokeniser, chameleon, comprehensions, coroutines, coverage, create_gc_cycles, crypto_pyaes, dask, deepcopy, deepcopy_memo, deepcopy_reduce, deltablue, django_template, docutils, dulwich_log, fannkuch, flaskblogging, float, gc_traversal, generators, genshi_text, genshi_xml, go, gunicorn, hexiom, html5lib, json, json_dumps, json_loads, logging_format, logging_silent, logging_simple, mako, mdp, meteor_contest, mypy2, nbody, nqueens, pathlib, pickle, pickle_dict, pickle_list, pickle_pure_python, pidigits, pprint_pformat, pprint_safe_repr, pycparser, pyflate, pylint, python_startup, python_startup_no_site, raytrace, regex_compile, regex_dna, regex_effbot, regex_v8, richards, richards_super, scimark_fft, scimark_lu, scimark_monte_carlo, scimark_sor, scimark_sparse_mat_mult, spectral_norm, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, sqlite_synth, sympy_expand, sympy_integrate, sympy_str, sympy_sum, telco, thrift, tomli_loads, tornado_http, typing_runtime_protocols, unpack_sequence, unpickle, unpickle_list, unpickle_pure_python, xml_etree_generate, xml_etree_iterparse, xml_etree_parse, xml_etree_process
- [📄table](bm-20240916-linux-x86_64-python-main-3.14.0a0-44052b5-vs-3.12.6.md)
- [📈time plot](bm-20240916-linux-x86_64-python-main-3.14.0a0-44052b5-vs-3.12.6.svg)

### vs. 3.13.0rc2

- Geometric mean: not sig (HPT: reliability of 84.13%, 1.00x slower at 99th %ile)
- Memory usage: 1.11x
- missing benchmarks: 2to3, aiohttp, async_generators, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, asyncio_tcp, asyncio_tcp_ssl, asyncio_websockets, bench_mp_pool, bench_thread_pool, bpe_tokeniser, chameleon, comprehensions, coroutines, coverage, create_gc_cycles, crypto_pyaes, dask, deepcopy, deepcopy_memo, deepcopy_reduce, deltablue, django_template, docutils, dulwich_log, fannkuch, flaskblogging, float, gc_traversal, generators, genshi_text, genshi_xml, go, gunicorn, hexiom, html5lib, json, json_dumps, json_loads, logging_format, logging_silent, logging_simple, mako, mdp, meteor_contest, nbody, nqueens, pathlib, pickle, pickle_dict, pickle_list, pickle_pure_python, pidigits, pprint_pformat, pprint_safe_repr, pycparser, pyflate, pylint, python_startup, python_startup_no_site, raytrace, regex_compile, regex_dna, regex_effbot, regex_v8, richards, richards_super, scimark_fft, scimark_lu, scimark_monte_carlo, scimark_sor, scimark_sparse_mat_mult, spectral_norm, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, sqlite_synth, sympy_expand, sympy_integrate, sympy_str, sympy_sum, telco, thrift, tomli_loads, tornado_http, typing_runtime_protocols, unpack_sequence, unpickle, unpickle_list, unpickle_pure_python, xml_etree_generate, xml_etree_iterparse, xml_etree_parse, xml_etree_process
- [📄table](bm-20240916-linux-x86_64-python-main-3.14.0a0-44052b5-vs-3.13.0rc2.md)
- [📈time plot](bm-20240916-linux-x86_64-python-main-3.14.0a0-44052b5-vs-3.13.0rc2.svg)

### vs. base

- Geometric mean: not sig (HPT: reliability of 84.13%, 1.00x slower at 99th %ile)
- Memory usage: unknown
- [🧠memory plot](bm-20240916-linux-x86_64-python-main-3.14.0a0-44052b5-vs-base-mem.svg)
- [📄table](bm-20240916-linux-x86_64-python-main-3.14.0a0-44052b5-vs-base.md)
- [📈time plot](bm-20240916-linux-x86_64-python-main-3.14.0a0-44052b5-vs-base.svg)

### vs. 3.12.0b1

- [📄table](bm-20240916-linux-x86_64-python-main-3.14.0a0-44052b5-vs-3.12.0b1.md)
- [📈time plot](bm-20240916-linux-x86_64-python-main-3.14.0a0-44052b5-vs-3.12.0b1.svg)

### vs. 3.12.5+

- [📄table](bm-20240916-linux-x86_64-python-main-3.14.0a0-44052b5-vs-3.12.5%2B.md)
- [📈time plot](bm-20240916-linux-x86_64-python-main-3.14.0a0-44052b5-vs-3.12.5%2B.svg)

### vs. 3.13.0b1

- [📄table](bm-20240916-linux-x86_64-python-main-3.14.0a0-44052b5-vs-3.13.0b1.md)
- [📈time plot](bm-20240916-linux-x86_64-python-main-3.14.0a0-44052b5-vs-3.13.0b1.svg)

### vs. 3.13.0rc1+

- [📄table](bm-20240916-linux-x86_64-python-main-3.14.0a0-44052b5-vs-3.13.0rc1%2B.md)
- [📈time plot](bm-20240916-linux-x86_64-python-main-3.14.0a0-44052b5-vs-3.13.0rc1%2B.svg)

