# Results vs. 3.13.0rc2

- fork: python
- ref: f5dd52df16e1b3f3f8cc
- machine: linux-x86_64
- commit hash: f5dd52d
- commit date: 2026-09-11
- overall geometric mean: 1.021x faster
- HPT reliability: 99.14%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 261 ms: 1.00x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.39 sec: 1.09x faster                                                |
| html5lib       | 67.0 ms                                                      | 60.0 ms: 1.12x faster                                                 |
| Geometric mean | (ref)                                                        | 1.07x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 760 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 565 ms: 1.18x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 403 ms: 1.14x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 558 ms: 1.14x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 296 ms: 1.14x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 365 ms: 1.14x faster                                                  |
| async_tree_io              | 876 ms                                                       | 776 ms: 1.13x faster                                                  |
| async_generators           | 377 ms                                                       | 342 ms: 1.10x faster                                                  |
| async_tree_none            | 354 ms                                                       | 329 ms: 1.08x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 23.8 ms: 1.01x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.11x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 187 ms: 1.16x faster                                                  |
| float          | 77.5 ms                                                      | 73.1 ms: 1.06x faster                                                 |
| nbody          | 85.1 ms                                                      | 92.4 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.89 ms: 1.07x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 21.8 ms: 1.04x faster                                                 |
| regex_dna      | 180 ms                                                       | 186 ms: 1.03x slower                                                  |
| regex_compile  | 132 ms                                                       | 148 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                        | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.36 ms: 1.13x faster                                                 |
| tomli_loads          | 2.01 sec                                                     | 1.80 sec: 1.12x faster                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.4 ms: 1.04x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 213 us: 1.01x slower                                                  |
| json_loads           | 27.0 us                                                      | 27.4 us: 1.01x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 88.2 ms: 1.03x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 305 us: 1.03x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 62.4 ms: 1.05x slower                                                 |
| xml_etree_parse      | 136 ms                                                       | 143 ms: 1.05x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.74 ms: 1.05x slower                                                 |
| python_startup         | 11.0 ms                                                      | 13.0 ms: 1.18x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.11x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 11.3 ms                                                      | 12.0 ms: 1.06x slower                                                 |
| django_template | 34.1 ms                                                      | 36.6 ms: 1.07x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.07x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 115 ms: 2.76x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.14 sec: 2.07x faster                                                |
| deepcopy                   | 355 us                                                       | 236 us: 1.50x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 26.8 us: 1.46x faster                                                 |
| go                         | 141 ms                                                       | 106 ms: 1.32x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 121 us: 1.28x faster                                                  |
| scimark_sor                | 134 ms                                                       | 110 ms: 1.22x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 760 ms: 1.20x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.59 us: 1.20x faster                                                 |
| spectral_norm              | 111 ms                                                       | 93.4 ms: 1.19x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 565 ms: 1.18x faster                                                  |
| pyflate                    | 449 ms                                                       | 386 ms: 1.16x faster                                                  |
| pidigits                   | 217 ms                                                       | 187 ms: 1.16x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 403 ms: 1.14x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 558 ms: 1.14x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 296 ms: 1.14x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 365 ms: 1.14x faster                                                  |
| async_tree_io              | 876 ms                                                       | 776 ms: 1.13x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.36 ms: 1.13x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.80 sec: 1.12x faster                                                |
| html5lib                   | 67.0 ms                                                      | 60.0 ms: 1.12x faster                                                 |
| scimark_fft                | 349 ms                                                       | 316 ms: 1.11x faster                                                  |
| async_generators           | 377 ms                                                       | 342 ms: 1.10x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 67.9 ms: 1.10x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.39 sec: 1.09x faster                                                |
| pathlib                    | 19.2 ms                                                      | 17.7 ms: 1.08x faster                                                 |
| async_tree_none            | 354 ms                                                       | 329 ms: 1.08x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 73.5 ms: 1.07x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.89 ms: 1.07x faster                                                 |
| float                      | 77.5 ms                                                      | 73.1 ms: 1.06x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.66 ms: 1.06x faster                                                 |
| chaos                      | 57.3 ms                                                      | 54.3 ms: 1.06x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.24 sec: 1.05x faster                                                |
| logging_simple             | 6.16 us                                                      | 5.88 us: 1.05x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 21.8 ms: 1.04x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.4 ms: 1.04x faster                                                 |
| logging_silent             | 103 ns                                                       | 98.8 ns: 1.04x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.0 ms: 1.04x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 19.3 ms: 1.03x faster                                                 |
| logging_format             | 6.84 us                                                      | 6.67 us: 1.03x faster                                                 |
| comprehensions             | 16.5 us                                                      | 16.1 us: 1.02x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.63 ms: 1.02x faster                                                 |
| richards_super             | 51.6 ms                                                      | 51.1 ms: 1.01x faster                                                 |
| richards                   | 45.2 ms                                                      | 44.8 ms: 1.01x faster                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 67.4 ms: 1.01x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 733 ms: 1.01x faster                                                  |
| raytrace                   | 253 ms                                                       | 253 ms: 1.00x slower                                                  |
| fannkuch                   | 370 ms                                                       | 371 ms: 1.00x slower                                                  |
| 2to3                       | 260 ms                                                       | 261 ms: 1.00x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.12 sec: 1.01x slower                                                |
| meteor_contest             | 102 ms                                                       | 102 ms: 1.01x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 23.8 ms: 1.01x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 213 us: 1.01x slower                                                  |
| json_loads                 | 27.0 us                                                      | 27.4 us: 1.01x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 158 ms: 1.02x slower                                                  |
| sympy_str                  | 275 ms                                                       | 279 ms: 1.02x slower                                                  |
| generators                 | 28.8 ms                                                      | 29.5 ms: 1.02x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 88.2 ms: 1.03x slower                                                 |
| regex_dna                  | 180 ms                                                       | 186 ms: 1.03x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 305 us: 1.03x slower                                                  |
| sympy_expand               | 457 ms                                                       | 475 ms: 1.04x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.31 us: 1.05x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 7.74 ms: 1.05x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 62.4 ms: 1.05x slower                                                 |
| xml_etree_parse            | 136 ms                                                       | 143 ms: 1.05x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 119 ms: 1.06x slower                                                  |
| mako                       | 11.3 ms                                                      | 12.0 ms: 1.06x slower                                                 |
| django_template            | 34.1 ms                                                      | 36.6 ms: 1.07x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.37 ms: 1.08x slower                                                 |
| nbody                      | 85.1 ms                                                      | 92.4 ms: 1.09x slower                                                 |
| regex_compile              | 132 ms                                                       | 148 ms: 1.12x slower                                                  |
| python_startup             | 11.0 ms                                                      | 13.0 ms: 1.18x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.66 ms: 1.24x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.04 ms: 1.28x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.34 ms: 1.46x slower                                                 |
| telco                      | 7.82 ms                                                      | 160 ms: 20.51x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 265 ms: 24.10x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.02x slower                                                          |

Benchmark hidden because not significant (4): json, pprint_pformat, thrift, coverage
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260911-3.16.0a0-f5dd52d/bm-20260911-vultr-x86_64-python-f5dd52df16e1b3f3f8cc-3.16.0a0-f5dd52d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.021x faster

# HPT report

- Reliability score: 99.14% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x