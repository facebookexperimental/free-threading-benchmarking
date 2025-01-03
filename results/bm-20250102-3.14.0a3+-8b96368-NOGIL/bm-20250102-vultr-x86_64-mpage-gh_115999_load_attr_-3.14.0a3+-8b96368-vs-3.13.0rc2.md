# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 8b96368
- commit date: 2025-01-02
- overall geometric mean: 1.091x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 312 ms: 1.20x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.84 sec: 1.08x slower                                                |
| html5lib       | 67.0 ms                                                      | 73.6 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                        | 1.13x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 577 ms: 1.58x faster                                                  |
| async_tree_io              | 876 ms                                                       | 594 ms: 1.47x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 233 ms: 1.45x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 303 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 471 ms: 1.35x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 343 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 506 ms: 1.32x faster                                                  |
| async_tree_none            | 354 ms                                                       | 276 ms: 1.28x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 25.1 ms: 1.07x slower                                                 |
| async_generators           | 377 ms                                                       | 416 ms: 1.10x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.25x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 190 ms: 1.14x faster                                                  |
| nbody          | 85.1 ms                                                      | 127 ms: 1.49x slower                                                  |
| Geometric mean | (ref)                                                        | 1.09x slower                                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.88 ms: 1.07x faster                                                 |
| regex_dna      | 180 ms                                                       | 171 ms: 1.06x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 23.8 ms: 1.05x slower                                                 |
| regex_compile  | 132 ms                                                       | 150 ms: 1.13x slower                                                  |
| Geometric mean | (ref)                                                        | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.6 ms: 1.08x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                                  |
| json_loads           | 27.0 us                                                      | 27.7 us: 1.03x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 96.5 ms: 1.13x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 68.9 ms: 1.16x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 248 us: 1.18x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 12.9 ms: 1.23x slower                                                 |
| tomli_loads          | 2.01 sec                                                     | 2.51 sec: 1.25x slower                                                |
| pickle_pure_python   | 294 us                                                       | 375 us: 1.27x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.12x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.71 ms: 1.31x slower                                                 |
| python_startup         | 11.0 ms                                                      | 15.4 ms: 1.41x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.36x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 59.5 ms: 1.22x slower                                                 |
| django_template | 34.1 ms                                                      | 42.8 ms: 1.26x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 28.1 ms: 1.30x slower                                                 |
| mako            | 11.3 ms                                                      | 15.5 ms: 1.37x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.29x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 577 ms: 1.58x faster                                                  |
| async_tree_io              | 876 ms                                                       | 594 ms: 1.47x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 233 ms: 1.45x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 303 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 471 ms: 1.35x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 343 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 506 ms: 1.32x faster                                                  |
| async_tree_none            | 354 ms                                                       | 276 ms: 1.28x faster                                                  |
| pidigits                   | 217 ms                                                       | 190 ms: 1.14x faster                                                  |
| deepcopy                   | 355 us                                                       | 311 us: 1.14x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.6 ms: 1.08x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.88 ms: 1.07x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.08 us: 1.06x faster                                                 |
| regex_dna                  | 180 ms                                                       | 171 ms: 1.06x faster                                                  |
| json                       | 4.93 ms                                                      | 4.85 ms: 1.02x faster                                                 |
| deepcopy_memo              | 39.1 us                                                      | 38.7 us: 1.01x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| spectral_norm              | 111 ms                                                       | 111 ms: 1.00x slower                                                  |
| go                         | 141 ms                                                       | 144 ms: 1.02x slower                                                  |
| json_loads                 | 27.0 us                                                      | 27.7 us: 1.03x slower                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 3.25 us: 1.04x slower                                                 |
| regex_v8                   | 22.7 ms                                                      | 23.8 ms: 1.05x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 3.30 ms: 1.05x slower                                                 |
| generators                 | 28.8 ms                                                      | 30.6 ms: 1.06x slower                                                 |
| scimark_fft                | 349 ms                                                       | 371 ms: 1.06x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 25.1 ms: 1.07x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.20 sec: 1.07x slower                                                |
| telco                      | 7.82 ms                                                      | 8.40 ms: 1.07x slower                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.79 sec: 1.08x slower                                                |
| docutils                   | 2.62 sec                                                     | 2.84 sec: 1.08x slower                                                |
| html5lib                   | 67.0 ms                                                      | 73.6 ms: 1.10x slower                                                 |
| async_generators           | 377 ms                                                       | 416 ms: 1.10x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 82.6 ms: 1.10x slower                                                 |
| mdp                        | 2.36 sec                                                     | 2.61 sec: 1.11x slower                                                |
| logging_silent             | 103 ns                                                       | 115 ns: 1.12x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 827 ms: 1.12x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 96.5 ms: 1.13x slower                                                 |
| regex_compile              | 132 ms                                                       | 150 ms: 1.13x slower                                                  |
| sqlglot_normalize          | 106 ms                                                       | 121 ms: 1.14x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.71 sec: 1.14x slower                                                |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.41 ms: 1.15x slower                                                 |
| pyflate                    | 449 ms                                                       | 518 ms: 1.15x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 68.9 ms: 1.16x slower                                                 |
| sqlglot_optimize           | 52.7 ms                                                      | 62.0 ms: 1.17x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 248 us: 1.18x slower                                                  |
| logging_simple             | 6.16 us                                                      | 7.29 us: 1.18x slower                                                 |
| scimark_sor                | 134 ms                                                       | 161 ms: 1.20x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 186 ms: 1.20x slower                                                  |
| 2to3                       | 260 ms                                                       | 312 ms: 1.20x slower                                                  |
| thrift                     | 778 us                                                       | 940 us: 1.21x slower                                                  |
| sympy_expand               | 457 ms                                                       | 553 ms: 1.21x slower                                                  |
| richards                   | 45.2 ms                                                      | 54.9 ms: 1.21x slower                                                 |
| coverage                   | 83.0 ms                                                      | 101 ms: 1.21x slower                                                  |
| logging_format             | 6.84 us                                                      | 8.30 us: 1.21x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 24.2 ms: 1.22x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 59.5 ms: 1.22x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 138 ms: 1.23x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 12.9 ms: 1.23x slower                                                 |
| sympy_str                  | 275 ms                                                       | 340 ms: 1.24x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 1.93 ms: 1.24x slower                                                 |
| richards_super             | 51.6 ms                                                      | 64.1 ms: 1.24x slower                                                 |
| chaos                      | 57.3 ms                                                      | 71.3 ms: 1.24x slower                                                 |
| tomli_loads                | 2.01 sec                                                     | 2.51 sec: 1.25x slower                                                |
| django_template            | 34.1 ms                                                      | 42.8 ms: 1.26x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 99.4 ms: 1.26x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 7.59 ms: 1.27x slower                                                 |
| meteor_contest             | 102 ms                                                       | 129 ms: 1.27x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 375 us: 1.27x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.59 ms: 1.27x slower                                                 |
| raytrace                   | 253 ms                                                       | 322 ms: 1.28x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 86.6 ms: 1.28x slower                                                 |
| comprehensions             | 16.5 us                                                      | 21.1 us: 1.28x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 200 us: 1.29x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 85.0 ms: 1.30x slower                                                 |
| genshi_text                | 21.5 ms                                                      | 28.1 ms: 1.30x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 9.71 ms: 1.31x slower                                                 |
| fannkuch                   | 370 ms                                                       | 492 ms: 1.33x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.80 ms: 1.35x slower                                                 |
| mako                       | 11.3 ms                                                      | 15.5 ms: 1.37x slower                                                 |
| python_startup             | 11.0 ms                                                      | 15.4 ms: 1.41x slower                                                 |
| nbody                      | 85.1 ms                                                      | 127 ms: 1.49x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 4.81 ms: 1.54x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 3.35 ms: 3.64x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 97.7 ms: 8.88x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.14x slower                                                          |

Benchmark hidden because not significant (3): pathlib, float, pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250102-3.14.0a3+-8b96368-NOGIL/bm-20250102-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-8b96368.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.091x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.33x