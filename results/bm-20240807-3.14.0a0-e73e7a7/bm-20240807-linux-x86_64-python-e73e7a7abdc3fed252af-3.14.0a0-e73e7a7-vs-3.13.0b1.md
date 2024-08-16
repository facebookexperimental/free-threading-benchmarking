# Results vs. 3.13.0b1

- fork: python
- ref: e73e7a7abdc3fed252af
- machine: linux-x86_64
- commit hash: e73e7a7
- commit date: 2024-08-07
- overall geometric mean: 1.04x faster
- HPT reliability: 94.40%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 3.94 sec                                                              | 4.14 sec: 1.05x slower                                                |
| Geometric mean | (ref)                                                                 | 1.03x slower                                                          |

Benchmark hidden because not significant (3): 2to3, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.43 sec                                                              | 1.30 sec: 1.10x faster                                                |
| async_tree_memoization     | 775 ms                                                                | 705 ms: 1.10x faster                                                  |
| async_tree_none_tg         | 526 ms                                                                | 485 ms: 1.09x faster                                                  |
| async_tree_io              | 1.39 sec                                                              | 1.29 sec: 1.08x faster                                                |
| async_tree_memoization_tg  | 692 ms                                                                | 650 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 829 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed    | 898 ms                                                                | 856 ms: 1.05x faster                                                  |
| async_tree_none            | 523 ms                                                                | 501 ms: 1.04x faster                                                  |
| asyncio_websockets         | 728 ms                                                                | 767 ms: 1.05x slower                                                  |
| coroutines                 | 29.3 ms                                                               | 32.6 ms: 1.11x slower                                                 |
| Geometric mean             | (ref)                                                                 | 1.04x faster                                                          |

Benchmark hidden because not significant (3): asyncio_tcp, async_generators, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 256 ms                                                                | 245 ms: 1.04x faster                                                  |
| Geometric mean | (ref)                                                                 | 1.02x faster                                                          |

Benchmark hidden because not significant (2): nbody, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 284 ms                                                                | 300 ms: 1.06x slower                                                  |
| regex_effbot   | 4.63 ms                                                               | 5.47 ms: 1.18x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.07x slower                                                          |

Benchmark hidden because not significant (2): regex_compile, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark         | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|-------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_list       | 7.48 us                                                               | 6.74 us: 1.11x faster                                                 |
| tomli_loads       | 2.84 sec                                                              | 2.66 sec: 1.06x faster                                                |
| json_dumps        | 13.9 ms                                                               | 14.5 ms: 1.04x slower                                                 |
| xml_etree_parse   | 216 ms                                                                | 226 ms: 1.05x slower                                                  |
| xml_etree_process | 82.2 ms                                                               | 86.9 ms: 1.06x slower                                                 |
| Geometric mean    | (ref)                                                                 | 1.00x slower                                                          |

Benchmark hidden because not significant (9): unpickle, json_loads, pickle_dict, unpickle_list, pickle, pickle_pure_python, xml_etree_iterparse, xml_etree_generate, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 16.0 ms                                                               | 14.9 ms: 1.07x faster                                                 |
| Geometric mean         | (ref)                                                                 | 1.03x faster                                                          |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 46.1 ms                                                               | 48.3 ms: 1.05x slower                                                 |
| mako            | 16.7 ms                                                               | 18.3 ms: 1.10x slower                                                 |
| Geometric mean  | (ref)                                                                 | 1.04x slower                                                          |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240807-linux-x86_64-python-e73e7a7abdc3fed252af-3.14.0a0-e73e7a7 |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| telco                      | 229 ms                                                                | 11.5 ms: 19.91x faster                                                |
| deepcopy                   | 498 us                                                                | 359 us: 1.39x faster                                                  |
| deepcopy_memo              | 50.9 us                                                               | 40.2 us: 1.27x faster                                                 |
| deepcopy_reduce            | 4.31 us                                                               | 3.63 us: 1.19x faster                                                 |
| meteor_contest             | 156 ms                                                                | 139 ms: 1.12x faster                                                  |
| pickle_list                | 7.48 us                                                               | 6.74 us: 1.11x faster                                                 |
| async_tree_io_tg           | 1.43 sec                                                              | 1.30 sec: 1.10x faster                                                |
| async_tree_memoization     | 775 ms                                                                | 705 ms: 1.10x faster                                                  |
| async_tree_none_tg         | 526 ms                                                                | 485 ms: 1.09x faster                                                  |
| logging_simple             | 9.16 us                                                               | 8.46 us: 1.08x faster                                                 |
| mdp                        | 4.01 sec                                                              | 3.71 sec: 1.08x faster                                                |
| async_tree_io              | 1.39 sec                                                              | 1.29 sec: 1.08x faster                                                |
| bpe_tokeniser              | 6.53 sec                                                              | 6.08 sec: 1.07x faster                                                |
| python_startup_no_site     | 16.0 ms                                                               | 14.9 ms: 1.07x faster                                                 |
| pathlib                    | 31.8 ms                                                               | 29.7 ms: 1.07x faster                                                 |
| tomli_loads                | 2.84 sec                                                              | 2.66 sec: 1.06x faster                                                |
| async_tree_memoization_tg  | 692 ms                                                                | 650 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 829 ms: 1.06x faster                                                  |
| sympy_expand               | 638 ms                                                                | 606 ms: 1.05x faster                                                  |
| async_tree_cpu_io_mixed    | 898 ms                                                                | 856 ms: 1.05x faster                                                  |
| pprint_pformat             | 2.04 sec                                                              | 1.94 sec: 1.05x faster                                                |
| async_tree_none            | 523 ms                                                                | 501 ms: 1.04x faster                                                  |
| pidigits                   | 256 ms                                                                | 245 ms: 1.04x faster                                                  |
| pyflate                    | 710 ms                                                                | 682 ms: 1.04x faster                                                  |
| json_dumps                 | 13.9 ms                                                               | 14.5 ms: 1.04x slower                                                 |
| xml_etree_parse            | 216 ms                                                                | 226 ms: 1.05x slower                                                  |
| django_template            | 46.1 ms                                                               | 48.3 ms: 1.05x slower                                                 |
| docutils                   | 3.94 sec                                                              | 4.14 sec: 1.05x slower                                                |
| scimark_lu                 | 150 ms                                                                | 158 ms: 1.05x slower                                                  |
| asyncio_websockets         | 728 ms                                                                | 767 ms: 1.05x slower                                                  |
| xml_etree_process          | 82.2 ms                                                               | 86.9 ms: 1.06x slower                                                 |
| regex_dna                  | 284 ms                                                                | 300 ms: 1.06x slower                                                  |
| thrift                     | 1.09 ms                                                               | 1.15 ms: 1.06x slower                                                 |
| comprehensions             | 22.6 us                                                               | 24.0 us: 1.06x slower                                                 |
| sqlglot_transpile          | 2.24 ms                                                               | 2.37 ms: 1.06x slower                                                 |
| sqlglot_optimize           | 77.9 ms                                                               | 83.9 ms: 1.08x slower                                                 |
| chaos                      | 81.5 ms                                                               | 88.2 ms: 1.08x slower                                                 |
| bench_mp_pool              | 19.7 ms                                                               | 21.4 ms: 1.08x slower                                                 |
| logging_format             | 9.36 us                                                               | 10.2 us: 1.09x slower                                                 |
| mako                       | 16.7 ms                                                               | 18.3 ms: 1.10x slower                                                 |
| coroutines                 | 29.3 ms                                                               | 32.6 ms: 1.11x slower                                                 |
| unpack_sequence            | 54.6 ns                                                               | 61.3 ns: 1.12x slower                                                 |
| bench_thread_pool          | 3.01 ms                                                               | 3.44 ms: 1.14x slower                                                 |
| regex_effbot               | 4.63 ms                                                               | 5.47 ms: 1.18x slower                                                 |
| Geometric mean             | (ref)                                                                 | 1.04x faster                                                          |

Benchmark hidden because not significant (52): nbody, gc_traversal, scimark_sparse_mat_mult, asyncio_tcp, scimark_sor, raytrace, nqueens, create_gc_cycles, sqlglot_normalize, coverage, deltablue, sympy_integrate, pycparser, unpickle, typing_runtime_protocols, async_generators, asyncio_tcp_ssl, sqlglot_parse, sympy_str, json_loads, pickle_dict, json, fannkuch, sympy_sum, genshi_xml, pprint_safe_repr, scimark_monte_carlo, richards, unpickle_list, genshi_text, pickle, hexiom, scimark_fft, 2to3, regex_compile, python_startup, logging_silent, generators, pickle_pure_python, pylint, go, html5lib, regex_v8, crypto_pyaes, tornado_http, xml_etree_iterparse, xml_etree_generate, unpickle_pure_python, float, richards_super, sqlite_synth, spectral_norm
Ignored benchmarks (6) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 94.40% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x