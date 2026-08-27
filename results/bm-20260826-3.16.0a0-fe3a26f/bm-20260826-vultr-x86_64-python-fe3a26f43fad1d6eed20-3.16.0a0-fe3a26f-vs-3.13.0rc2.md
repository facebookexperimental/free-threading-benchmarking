# Results vs. 3.13.0rc2

- fork: python
- ref: fe3a26f43fad1d6eed20
- machine: linux-x86_64
- commit hash: fe3a26f
- commit date: 2026-08-26
- overall geometric mean: 1.031x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 259 ms: 1.00x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.34 sec: 1.12x faster                                                |
| html5lib       | 67.0 ms                                                      | 59.4 ms: 1.13x faster                                                 |
| Geometric mean | (ref)                                                        | 1.08x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 666 ms                                                       | 536 ms: 1.24x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 374 ms: 1.23x faster                                                  |
| async_tree_io              | 876 ms                                                       | 723 ms: 1.21x faster                                                  |
| async_tree_none            | 354 ms                                                       | 292 ms: 1.21x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 765 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 560 ms: 1.14x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 366 ms: 1.13x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 301 ms: 1.12x faster                                                  |
| async_generators           | 377 ms                                                       | 349 ms: 1.08x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.1 ms: 1.02x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.04x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.14x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 187 ms: 1.16x faster                                                  |
| float          | 77.5 ms                                                      | 72.8 ms: 1.06x faster                                                 |
| nbody          | 85.1 ms                                                      | 92.3 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.55 ms: 1.21x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 21.5 ms: 1.05x faster                                                 |
| regex_dna      | 180 ms                                                       | 177 ms: 1.02x faster                                                  |
| regex_compile  | 132 ms                                                       | 147 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|---------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps          | 10.5 ms                                                      | 9.48 ms: 1.11x faster                                                 |
| tomli_loads         | 2.01 sec                                                     | 1.81 sec: 1.11x faster                                                |
| xml_etree_iterparse | 94.9 ms                                                      | 90.8 ms: 1.05x faster                                                 |
| json_loads          | 27.0 us                                                      | 27.1 us: 1.00x slower                                                 |
| xml_etree_generate  | 85.4 ms                                                      | 88.1 ms: 1.03x slower                                                 |
| pickle_pure_python  | 294 us                                                       | 304 us: 1.03x slower                                                  |
| xml_etree_process   | 59.3 ms                                                      | 62.0 ms: 1.05x slower                                                 |
| xml_etree_parse     | 136 ms                                                       | 143 ms: 1.05x slower                                                  |
| Geometric mean      | (ref)                                                        | 1.01x faster                                                          |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.74 ms: 1.05x slower                                                 |
| python_startup         | 11.0 ms                                                      | 13.0 ms: 1.18x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.11x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                 |
| django_template | 34.1 ms                                                      | 36.8 ms: 1.08x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.06x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 114 ms: 2.79x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.14 sec: 2.07x faster                                                |
| deepcopy                   | 355 us                                                       | 237 us: 1.50x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 26.7 us: 1.46x faster                                                 |
| go                         | 141 ms                                                       | 102 ms: 1.37x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 122 us: 1.27x faster                                                  |
| scimark_sor                | 134 ms                                                       | 106 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 536 ms: 1.24x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 374 ms: 1.23x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.56 us: 1.22x faster                                                 |
| async_tree_io              | 876 ms                                                       | 723 ms: 1.21x faster                                                  |
| async_tree_none            | 354 ms                                                       | 292 ms: 1.21x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.55 ms: 1.21x faster                                                 |
| spectral_norm              | 111 ms                                                       | 92.9 ms: 1.20x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 765 ms: 1.19x faster                                                  |
| pidigits                   | 217 ms                                                       | 187 ms: 1.16x faster                                                  |
| pyflate                    | 449 ms                                                       | 394 ms: 1.14x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 560 ms: 1.14x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 366 ms: 1.13x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 59.4 ms: 1.13x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.34 sec: 1.12x faster                                                |
| async_tree_none_tg         | 336 ms                                                       | 301 ms: 1.12x faster                                                  |
| scimark_fft                | 349 ms                                                       | 314 ms: 1.11x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.48 ms: 1.11x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.81 sec: 1.11x faster                                                |
| dulwich_log                | 74.8 ms                                                      | 68.3 ms: 1.10x faster                                                 |
| async_generators           | 377 ms                                                       | 349 ms: 1.08x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.8 ms: 1.08x faster                                                 |
| chaos                      | 57.3 ms                                                      | 53.4 ms: 1.07x faster                                                 |
| logging_silent             | 103 ns                                                       | 95.6 ns: 1.07x faster                                                 |
| nqueens                    | 78.6 ms                                                      | 73.5 ms: 1.07x faster                                                 |
| float                      | 77.5 ms                                                      | 72.8 ms: 1.06x faster                                                 |
| comprehensions             | 16.5 us                                                      | 15.5 us: 1.06x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 21.5 ms: 1.05x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.24 sec: 1.05x faster                                                |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.8 ms: 1.05x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.74 ms: 1.04x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 19.1 ms: 1.04x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.1 ms: 1.04x faster                                                 |
| richards                   | 45.2 ms                                                      | 44.0 ms: 1.03x faster                                                 |
| richards_super             | 51.6 ms                                                      | 50.5 ms: 1.02x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 23.1 ms: 1.02x faster                                                 |
| generators                 | 28.8 ms                                                      | 28.2 ms: 1.02x faster                                                 |
| logging_simple             | 6.16 us                                                      | 6.04 us: 1.02x faster                                                 |
| regex_dna                  | 180 ms                                                       | 177 ms: 1.02x faster                                                  |
| json                       | 4.93 ms                                                      | 4.87 ms: 1.01x faster                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 67.5 ms: 1.01x faster                                                 |
| raytrace                   | 253 ms                                                       | 251 ms: 1.01x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 734 ms: 1.00x faster                                                  |
| 2to3                       | 260 ms                                                       | 259 ms: 1.00x faster                                                  |
| fannkuch                   | 370 ms                                                       | 368 ms: 1.00x faster                                                  |
| meteor_contest             | 102 ms                                                       | 101 ms: 1.00x faster                                                  |
| json_loads                 | 27.0 us                                                      | 27.1 us: 1.00x slower                                                 |
| sympy_str                  | 275 ms                                                       | 278 ms: 1.01x slower                                                  |
| logging_format             | 6.84 us                                                      | 6.93 us: 1.01x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 158 ms: 1.02x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.27 us: 1.03x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 88.1 ms: 1.03x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 304 us: 1.03x slower                                                  |
| coverage                   | 83.0 ms                                                      | 85.7 ms: 1.03x slower                                                 |
| sympy_expand               | 457 ms                                                       | 473 ms: 1.04x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 117 ms: 1.04x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.04x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 62.0 ms: 1.05x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.74 ms: 1.05x slower                                                 |
| xml_etree_parse            | 136 ms                                                       | 143 ms: 1.05x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.9 ms: 1.05x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.30 ms: 1.06x slower                                                 |
| django_template            | 34.1 ms                                                      | 36.8 ms: 1.08x slower                                                 |
| nbody                      | 85.1 ms                                                      | 92.3 ms: 1.08x slower                                                 |
| regex_compile              | 132 ms                                                       | 147 ms: 1.11x slower                                                  |
| python_startup             | 11.0 ms                                                      | 13.0 ms: 1.18x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 3.77 ms: 1.20x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.70 ms: 1.27x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.34 ms: 1.46x slower                                                 |
| telco                      | 7.82 ms                                                      | 161 ms: 20.57x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 250 ms: 22.78x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                          |

Benchmark hidden because not significant (5): scimark_sparse_mat_mult, thrift, pprint_pformat, unpickle_pure_python, pycparser
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260826-3.16.0a0-fe3a26f/bm-20260826-vultr-x86_64-python-fe3a26f43fad1d6eed20-3.16.0a0-fe3a26f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.031x faster

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x