# Results vs. 3.13.0rc2

- fork: python
- ref: v3.13.0rc2
- machine: linux-x86_64
- commit hash: ec61006
- commit date: 2024-09-06
- overall geometric mean: 1.00x slower
- HPT reliability: 98.90%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| chameleon      | 6.67 ms                                                                | 6.79 ms: 1.02x slower                                        |
| docutils       | 2.63 sec                                                               | 2.62 sec: 1.00x faster                                       |
| html5lib       | 68.6 ms                                                                | 67.0 ms: 1.02x faster                                        |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                 |

Benchmark hidden because not significant (2): 2to3, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|--------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| asyncio_websockets | 517 ms                                                                 | 520 ms: 1.01x slower                                         |
| async_generators   | 375 ms                                                                 | 377 ms: 1.01x slower                                         |
| coroutines         | 23.3 ms                                                                | 23.6 ms: 1.01x slower                                        |
| Geometric mean     | (ref)                                                                  | 1.01x slower                                                 |

Benchmark hidden because not significant (10): async_tree_io, asyncio_tcp_ssl, async_tree_cpu_io_mixed, async_tree_none, async_tree_memoization, asyncio_tcp, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_memoization_tg, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 217 ms: 1.00x slower                                         |
| float          | 76.7 ms                                                                | 77.5 ms: 1.01x slower                                        |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                 |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_dna      | 189 ms                                                                 | 180 ms: 1.05x faster                                         |
| regex_effbot   | 3.21 ms                                                                | 3.08 ms: 1.04x faster                                        |
| regex_v8       | 23.2 ms                                                                | 22.7 ms: 1.02x faster                                        |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                 |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| json_loads           | 27.3 us                                                                | 27.0 us: 1.01x faster                                        |
| json_dumps           | 10.6 ms                                                                | 10.5 ms: 1.01x faster                                        |
| pickle_dict          | 32.7 us                                                                | 32.5 us: 1.01x faster                                        |
| pickle               | 11.4 us                                                                | 11.3 us: 1.00x faster                                        |
| xml_etree_iterparse  | 94.4 ms                                                                | 94.9 ms: 1.01x slower                                        |
| unpickle_pure_python | 208 us                                                                 | 210 us: 1.01x slower                                         |
| pickle_pure_python   | 292 us                                                                 | 294 us: 1.01x slower                                         |
| pickle_list          | 4.81 us                                                                | 4.93 us: 1.02x slower                                        |
| unpickle_list        | 4.60 us                                                                | 4.71 us: 1.02x slower                                        |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                 |

Benchmark hidden because not significant (5): unpickle, tomli_loads, xml_etree_generate, xml_etree_process, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 11.0 ms                                                                | 11.0 ms: 1.00x faster                                        |
| python_startup_no_site | 7.41 ms                                                                | 7.39 ms: 1.00x faster                                        |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_text    | 21.7 ms                                                                | 21.5 ms: 1.01x faster                                        |
| genshi_xml     | 49.1 ms                                                                | 48.8 ms: 1.01x faster                                        |
| mako           | 11.2 ms                                                                | 11.3 ms: 1.01x slower                                        |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                 |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark              | bm-20240920-vultr-x86_64-python-4981ec59ded050919eb2-3.13.0rc2-4981ec5 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------:|
| gc_traversal           | 3.32 ms                                                                | 3.14 ms: 1.06x faster                                        |
| regex_dna              | 189 ms                                                                 | 180 ms: 1.05x faster                                         |
| regex_effbot           | 3.21 ms                                                                | 3.08 ms: 1.04x faster                                        |
| html5lib               | 68.6 ms                                                                | 67.0 ms: 1.02x faster                                        |
| regex_v8               | 23.2 ms                                                                | 22.7 ms: 1.02x faster                                        |
| sqlite_synth           | 2.25 us                                                                | 2.21 us: 1.02x faster                                        |
| fannkuch               | 376 ms                                                                 | 370 ms: 1.02x faster                                         |
| json_loads             | 27.3 us                                                                | 27.0 us: 1.01x faster                                        |
| json                   | 4.98 ms                                                                | 4.93 ms: 1.01x faster                                        |
| logging_format         | 6.92 us                                                                | 6.84 us: 1.01x faster                                        |
| genshi_text            | 21.7 ms                                                                | 21.5 ms: 1.01x faster                                        |
| json_dumps             | 10.6 ms                                                                | 10.5 ms: 1.01x faster                                        |
| comprehensions         | 16.6 us                                                                | 16.5 us: 1.01x faster                                        |
| scimark_monte_carlo    | 65.8 ms                                                                | 65.4 ms: 1.01x faster                                        |
| genshi_xml             | 49.1 ms                                                                | 48.8 ms: 1.01x faster                                        |
| bench_thread_pool      | 924 us                                                                 | 919 us: 1.01x faster                                         |
| pickle_dict            | 32.7 us                                                                | 32.5 us: 1.01x faster                                        |
| deepcopy               | 357 us                                                                 | 355 us: 1.01x faster                                         |
| crypto_pyaes           | 68.2 ms                                                                | 67.9 ms: 1.00x faster                                        |
| docutils               | 2.63 sec                                                               | 2.62 sec: 1.00x faster                                       |
| python_startup         | 11.0 ms                                                                | 11.0 ms: 1.00x faster                                        |
| pickle                 | 11.4 us                                                                | 11.3 us: 1.00x faster                                        |
| python_startup_no_site | 7.41 ms                                                                | 7.39 ms: 1.00x faster                                        |
| bpe_tokeniser          | 4.46 sec                                                               | 4.45 sec: 1.00x faster                                       |
| pidigits               | 216 ms                                                                 | 217 ms: 1.00x slower                                         |
| scimark_fft            | 348 ms                                                                 | 349 ms: 1.00x slower                                         |
| dulwich_log            | 74.5 ms                                                                | 74.8 ms: 1.00x slower                                        |
| sympy_integrate        | 19.7 ms                                                                | 19.8 ms: 1.01x slower                                        |
| asyncio_websockets     | 517 ms                                                                 | 520 ms: 1.01x slower                                         |
| xml_etree_iterparse    | 94.4 ms                                                                | 94.9 ms: 1.01x slower                                        |
| coverage               | 82.5 ms                                                                | 83.0 ms: 1.01x slower                                        |
| mdp                    | 2.34 sec                                                               | 2.36 sec: 1.01x slower                                       |
| hexiom                 | 5.95 ms                                                                | 5.99 ms: 1.01x slower                                        |
| scimark_sor            | 134 ms                                                                 | 134 ms: 1.01x slower                                         |
| async_generators       | 375 ms                                                                 | 377 ms: 1.01x slower                                         |
| sympy_expand           | 454 ms                                                                 | 457 ms: 1.01x slower                                         |
| sympy_sum              | 154 ms                                                                 | 156 ms: 1.01x slower                                         |
| unpickle_pure_python   | 208 us                                                                 | 210 us: 1.01x slower                                         |
| thrift                 | 772 us                                                                 | 778 us: 1.01x slower                                         |
| deltablue              | 3.10 ms                                                                | 3.12 ms: 1.01x slower                                        |
| float                  | 76.7 ms                                                                | 77.5 ms: 1.01x slower                                        |
| generators             | 28.5 ms                                                                | 28.8 ms: 1.01x slower                                        |
| pickle_pure_python     | 292 us                                                                 | 294 us: 1.01x slower                                         |
| coroutines             | 23.3 ms                                                                | 23.6 ms: 1.01x slower                                        |
| nqueens                | 77.7 ms                                                                | 78.6 ms: 1.01x slower                                        |
| mako                   | 11.2 ms                                                                | 11.3 ms: 1.01x slower                                        |
| raytrace               | 250 ms                                                                 | 253 ms: 1.01x slower                                         |
| chameleon              | 6.67 ms                                                                | 6.79 ms: 1.02x slower                                        |
| chaos                  | 56.3 ms                                                                | 57.3 ms: 1.02x slower                                        |
| richards               | 44.4 ms                                                                | 45.2 ms: 1.02x slower                                        |
| pickle_list            | 4.81 us                                                                | 4.93 us: 1.02x slower                                        |
| unpickle_list          | 4.60 us                                                                | 4.71 us: 1.02x slower                                        |
| richards_super         | 50.4 ms                                                                | 51.6 ms: 1.02x slower                                        |
| deepcopy_memo          | 38.1 us                                                                | 39.1 us: 1.03x slower                                        |
| pprint_safe_repr       | 719 ms                                                                 | 738 ms: 1.03x slower                                         |
| pprint_pformat         | 1.46 sec                                                               | 1.50 sec: 1.03x slower                                       |
| spectral_norm          | 108 ms                                                                 | 111 ms: 1.03x slower                                         |
| logging_silent         | 98.2 ns                                                                | 103 ns: 1.04x slower                                         |
| unpack_sequence        | 39.3 ns                                                                | 44.8 ns: 1.14x slower                                        |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                 |

Benchmark hidden because not significant (43): unpickle, scimark_sparse_mat_mult, typing_runtime_protocols, async_tree_io, aiohttp, pathlib, deepcopy_reduce, flaskblogging, nbody, tomli_loads, asyncio_tcp_ssl, pycparser, django_template, pyflate, bench_mp_pool, tornado_http, pylint, async_tree_cpu_io_mixed, xml_etree_generate, dask, go, 2to3, sqlglot_normalize, sqlglot_optimize, async_tree_none, sqlglot_parse, scimark_lu, xml_etree_process, sympy_str, meteor_contest, logging_simple, xml_etree_parse, sqlglot_transpile, create_gc_cycles, async_tree_memoization, gunicorn, asyncio_tcp, async_tree_cpu_io_mixed_tg, regex_compile, telco, async_tree_none_tg, async_tree_memoization_tg, async_tree_io_tg

# HPT report

- Reliability score: 98.90% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x