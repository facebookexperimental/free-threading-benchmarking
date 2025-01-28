# Results vs. 3.13.0rc2

- fork: python
- ref: 180ee43bde99b8ce4c4f
- machine: linux-x86_64
- commit hash: 180ee43
- commit date: 2025-01-28
- overall geometric mean: 1.055x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 253 ms: 1.03x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                 |
| Geometric mean | (ref)                                                        | 1.02x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 623 ms: 1.47x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 322 ms: 1.43x faster                                                   |
| async_tree_io              | 876 ms                                                       | 620 ms: 1.41x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 497 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 483 ms: 1.32x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 316 ms: 1.31x faster                                                   |
| async_tree_none            | 354 ms                                                       | 271 ms: 1.31x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 263 ms: 1.28x faster                                                   |
| async_generators           | 377 ms                                                       | 325 ms: 1.16x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 21.7 ms: 1.09x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 200 ms: 1.08x faster                                                   |
| float          | 77.5 ms                                                      | 72.5 ms: 1.07x faster                                                  |
| nbody          | 85.1 ms                                                      | 88.0 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.76 ms: 1.12x faster                                                  |
| regex_dna      | 180 ms                                                       | 169 ms: 1.06x faster                                                   |
| regex_compile  | 132 ms                                                       | 126 ms: 1.05x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 23.7 ms: 1.04x slower                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 126 ms: 1.08x faster                                                   |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.5 ms: 1.05x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.92 sec: 1.04x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 83.3 ms: 1.03x faster                                                  |
| xml_etree_process    | 59.3 ms                                                      | 58.4 ms: 1.02x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 212 us: 1.01x slower                                                   |
| json_loads           | 27.0 us                                                      | 28.7 us: 1.06x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 313 us: 1.06x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 11.2 ms: 1.06x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.41 ms: 1.00x slower                                                  |
| python_startup         | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.15x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.0 ms: 1.02x faster                                                  |
| genshi_xml      | 48.8 ms                                                      | 48.3 ms: 1.01x faster                                                  |
| mako            | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                  |
| django_template | 34.1 ms                                                      | 35.1 ms: 1.03x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.00x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 623 ms: 1.47x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 322 ms: 1.43x faster                                                   |
| async_tree_io              | 876 ms                                                       | 620 ms: 1.41x faster                                                   |
| deepcopy                   | 355 us                                                       | 256 us: 1.39x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 497 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 483 ms: 1.32x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 316 ms: 1.31x faster                                                   |
| async_tree_none            | 354 ms                                                       | 271 ms: 1.31x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 29.9 us: 1.30x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 263 ms: 1.28x faster                                                   |
| go                         | 141 ms                                                       | 115 ms: 1.23x faster                                                   |
| spectral_norm              | 111 ms                                                       | 92.6 ms: 1.20x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.63 us: 1.18x faster                                                  |
| scimark_sor                | 134 ms                                                       | 114 ms: 1.18x faster                                                   |
| async_generators           | 377 ms                                                       | 325 ms: 1.16x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.12 ms: 1.14x faster                                                  |
| pylint                     | 317 ms                                                       | 279 ms: 1.14x faster                                                   |
| scimark_fft                | 349 ms                                                       | 310 ms: 1.13x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.76 ms: 1.12x faster                                                  |
| telco                      | 7.82 ms                                                      | 7.14 ms: 1.10x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 21.7 ms: 1.09x faster                                                  |
| richards                   | 45.2 ms                                                      | 41.7 ms: 1.08x faster                                                  |
| pyflate                    | 449 ms                                                       | 414 ms: 1.08x faster                                                   |
| pidigits                   | 217 ms                                                       | 200 ms: 1.08x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 126 ms: 1.08x faster                                                   |
| richards_super             | 51.6 ms                                                      | 48.2 ms: 1.07x faster                                                  |
| float                      | 77.5 ms                                                      | 72.5 ms: 1.07x faster                                                  |
| regex_dna                  | 180 ms                                                       | 169 ms: 1.06x faster                                                   |
| thrift                     | 778 us                                                       | 732 us: 1.06x faster                                                   |
| pathlib                    | 19.2 ms                                                      | 18.0 ms: 1.06x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.22 sec: 1.05x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.70 ms: 1.05x faster                                                  |
| regex_compile              | 132 ms                                                       | 126 ms: 1.05x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.5 ms: 1.05x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 705 ms: 1.05x faster                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.43 sec: 1.04x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.92 sec: 1.04x faster                                                 |
| coverage                   | 83.0 ms                                                      | 79.6 ms: 1.04x faster                                                  |
| meteor_contest             | 102 ms                                                       | 97.7 ms: 1.04x faster                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 65.9 ms: 1.03x faster                                                  |
| chaos                      | 57.3 ms                                                      | 55.7 ms: 1.03x faster                                                  |
| 2to3                       | 260 ms                                                       | 253 ms: 1.03x faster                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 83.3 ms: 1.03x faster                                                  |
| genshi_text                | 21.5 ms                                                      | 21.0 ms: 1.02x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                 |
| logging_simple             | 6.16 us                                                      | 6.03 us: 1.02x faster                                                  |
| scimark_lu                 | 113 ms                                                       | 111 ms: 1.02x faster                                                   |
| sympy_sum                  | 156 ms                                                       | 153 ms: 1.02x faster                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 64.3 ms: 1.02x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 58.4 ms: 1.02x faster                                                  |
| deltablue                  | 3.12 ms                                                      | 3.08 ms: 1.01x faster                                                  |
| logging_format             | 6.84 us                                                      | 6.75 us: 1.01x faster                                                  |
| sqlglot_normalize          | 106 ms                                                       | 104 ms: 1.01x faster                                                   |
| sympy_str                  | 275 ms                                                       | 271 ms: 1.01x faster                                                   |
| sqlglot_optimize           | 52.7 ms                                                      | 52.1 ms: 1.01x faster                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 1.54 ms: 1.01x faster                                                  |
| genshi_xml                 | 48.8 ms                                                      | 48.3 ms: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                   |
| sqlglot_parse              | 1.25 ms                                                      | 1.24 ms: 1.01x faster                                                  |
| pycparser                  | 1.12 sec                                                     | 1.11 sec: 1.01x faster                                                 |
| nqueens                    | 78.6 ms                                                      | 78.2 ms: 1.00x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 19.8 ms: 1.00x faster                                                  |
| fannkuch                   | 370 ms                                                       | 371 ms: 1.00x slower                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 7.41 ms: 1.00x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 75.1 ms: 1.00x slower                                                  |
| logging_silent             | 103 ns                                                       | 103 ns: 1.01x slower                                                   |
| unpickle_pure_python       | 210 us                                                       | 212 us: 1.01x slower                                                   |
| comprehensions             | 16.5 us                                                      | 16.7 us: 1.01x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 157 us: 1.01x slower                                                   |
| mako                       | 11.3 ms                                                      | 11.6 ms: 1.02x slower                                                  |
| django_template            | 34.1 ms                                                      | 35.1 ms: 1.03x slower                                                  |
| json                       | 4.93 ms                                                      | 5.07 ms: 1.03x slower                                                  |
| nbody                      | 85.1 ms                                                      | 88.0 ms: 1.03x slower                                                  |
| raytrace                   | 253 ms                                                       | 263 ms: 1.04x slower                                                   |
| regex_v8                   | 22.7 ms                                                      | 23.7 ms: 1.04x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.47 sec: 1.05x slower                                                 |
| json_loads                 | 27.0 us                                                      | 28.7 us: 1.06x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 313 us: 1.06x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 11.2 ms: 1.06x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.12x slower                                                  |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.85 ms: 1.38x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 4.37 ms: 1.39x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 88.1 ms: 8.01x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (3): sqlite_synth, generators, sympy_expand
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250128-3.14.0a4+-180ee43/bm-20250128-vultr-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.055x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.10x