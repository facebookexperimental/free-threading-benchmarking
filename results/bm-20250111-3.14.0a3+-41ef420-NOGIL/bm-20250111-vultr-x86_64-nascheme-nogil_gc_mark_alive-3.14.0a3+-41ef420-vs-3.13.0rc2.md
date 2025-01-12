# Results vs. 3.13.0rc2

- fork: nascheme
- ref: nogil_gc_mark_alive
- machine: linux-x86_64
- commit hash: 41ef420
- commit date: 2025-01-11
- overall geometric mean: 1.178x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 339 ms: 1.31x slower                                                    |
| docutils       | 2.62 sec                                                     | 2.97 sec: 1.14x slower                                                  |
| html5lib       | 67.0 ms                                                      | 88.3 ms: 1.32x slower                                                   |
| Geometric mean | (ref)                                                        | 1.25x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 727 ms: 1.26x faster                                                    |
| async_tree_io              | 876 ms                                                       | 757 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 574 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 601 ms: 1.11x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 427 ms: 1.08x faster                                                    |
| async_tree_none_tg         | 336 ms                                                       | 315 ms: 1.07x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 398 ms: 1.04x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 22.8 ms: 1.03x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                    |
| async_generators           | 377 ms                                                       | 447 ms: 1.18x slower                                                    |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                            |

Benchmark hidden because not significant (1): async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 182 ms: 1.19x faster                                                    |
| float          | 77.5 ms                                                      | 105 ms: 1.36x slower                                                    |
| nbody          | 85.1 ms                                                      | 126 ms: 1.48x slower                                                    |
| Geometric mean | (ref)                                                        | 1.19x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.74 ms: 1.13x faster                                                   |
| regex_dna      | 180 ms                                                       | 173 ms: 1.04x faster                                                    |
| regex_v8       | 22.7 ms                                                      | 23.6 ms: 1.04x slower                                                   |
| regex_compile  | 132 ms                                                       | 165 ms: 1.25x slower                                                    |
| Geometric mean | (ref)                                                        | 1.03x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.4 ms: 1.07x faster                                                   |
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.06x faster                                                    |
| json_loads           | 27.0 us                                                      | 29.3 us: 1.08x slower                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 96.9 ms: 1.13x slower                                                   |
| tomli_loads          | 2.01 sec                                                     | 2.34 sec: 1.17x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 73.0 ms: 1.23x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 13.8 ms: 1.31x slower                                                   |
| unpickle_pure_python | 210 us                                                       | 320 us: 1.52x slower                                                    |
| pickle_pure_python   | 294 us                                                       | 489 us: 1.66x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.20x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.76 ms: 1.32x slower                                                   |
| python_startup         | 11.0 ms                                                      | 15.6 ms: 1.42x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 62.0 ms: 1.27x slower                                                   |
| genshi_text     | 21.5 ms                                                      | 30.3 ms: 1.41x slower                                                   |
| django_template | 34.1 ms                                                      | 49.5 ms: 1.45x slower                                                   |
| mako            | 11.3 ms                                                      | 17.1 ms: 1.51x slower                                                   |
| Geometric mean  | (ref)                                                        | 1.41x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 727 ms: 1.26x faster                                                    |
| pidigits                   | 217 ms                                                       | 182 ms: 1.19x faster                                                    |
| async_tree_io              | 876 ms                                                       | 757 ms: 1.16x faster                                                    |
| regex_effbot               | 3.08 ms                                                      | 2.74 ms: 1.13x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 574 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 601 ms: 1.11x faster                                                    |
| deepcopy                   | 355 us                                                       | 323 us: 1.10x faster                                                    |
| async_tree_memoization     | 461 ms                                                       | 427 ms: 1.08x faster                                                    |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.4 ms: 1.07x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 315 ms: 1.07x faster                                                    |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.06x faster                                                    |
| sqlite_synth               | 2.21 us                                                      | 2.10 us: 1.05x faster                                                   |
| regex_dna                  | 180 ms                                                       | 173 ms: 1.04x faster                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 398 ms: 1.04x faster                                                    |
| coroutines                 | 23.6 ms                                                      | 22.8 ms: 1.03x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                    |
| pathlib                    | 19.2 ms                                                      | 19.3 ms: 1.00x slower                                                   |
| spectral_norm              | 111 ms                                                       | 112 ms: 1.01x slower                                                    |
| deepcopy_memo              | 39.1 us                                                      | 40.4 us: 1.03x slower                                                   |
| regex_v8                   | 22.7 ms                                                      | 23.6 ms: 1.04x slower                                                   |
| pylint                     | 317 ms                                                       | 335 ms: 1.06x slower                                                    |
| json                       | 4.93 ms                                                      | 5.22 ms: 1.06x slower                                                   |
| gc_traversal               | 3.14 ms                                                      | 3.35 ms: 1.07x slower                                                   |
| scimark_fft                | 349 ms                                                       | 376 ms: 1.08x slower                                                    |
| deepcopy_reduce            | 3.11 us                                                      | 3.37 us: 1.08x slower                                                   |
| json_loads                 | 27.0 us                                                      | 29.3 us: 1.08x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.45 ms: 1.08x slower                                                   |
| telco                      | 7.82 ms                                                      | 8.58 ms: 1.10x slower                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.90 sec: 1.10x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.67 sec: 1.13x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 96.9 ms: 1.13x slower                                                   |
| docutils                   | 2.62 sec                                                     | 2.97 sec: 1.14x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.34 sec: 1.17x slower                                                  |
| coverage                   | 83.0 ms                                                      | 97.4 ms: 1.17x slower                                                   |
| async_generators           | 377 ms                                                       | 447 ms: 1.18x slower                                                    |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.59 ms: 1.19x slower                                                   |
| dulwich_log                | 74.8 ms                                                      | 89.9 ms: 1.20x slower                                                   |
| pycparser                  | 1.12 sec                                                     | 1.35 sec: 1.21x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 95.6 ms: 1.22x slower                                                   |
| xml_etree_process          | 59.3 ms                                                      | 73.0 ms: 1.23x slower                                                   |
| sqlglot_optimize           | 52.7 ms                                                      | 65.0 ms: 1.23x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 192 ms: 1.24x slower                                                    |
| sqlglot_normalize          | 106 ms                                                       | 131 ms: 1.24x slower                                                    |
| sympy_integrate            | 19.8 ms                                                      | 24.8 ms: 1.25x slower                                                   |
| regex_compile              | 132 ms                                                       | 165 ms: 1.25x slower                                                    |
| sympy_expand               | 457 ms                                                       | 577 ms: 1.26x slower                                                    |
| genshi_xml                 | 48.8 ms                                                      | 62.0 ms: 1.27x slower                                                   |
| pprint_safe_repr           | 738 ms                                                       | 939 ms: 1.27x slower                                                    |
| sympy_str                  | 275 ms                                                       | 350 ms: 1.28x slower                                                    |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                                    |
| fannkuch                   | 370 ms                                                       | 474 ms: 1.28x slower                                                    |
| thrift                     | 778 us                                                       | 999 us: 1.28x slower                                                    |
| typing_runtime_protocols   | 155 us                                                       | 201 us: 1.30x slower                                                    |
| 2to3                       | 260 ms                                                       | 339 ms: 1.31x slower                                                    |
| pprint_pformat             | 1.50 sec                                                     | 1.95 sec: 1.31x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 13.8 ms: 1.31x slower                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 89.2 ms: 1.31x slower                                                   |
| html5lib                   | 67.0 ms                                                      | 88.3 ms: 1.32x slower                                                   |
| python_startup_no_site     | 7.39 ms                                                      | 9.76 ms: 1.32x slower                                                   |
| float                      | 77.5 ms                                                      | 105 ms: 1.36x slower                                                    |
| generators                 | 28.8 ms                                                      | 39.4 ms: 1.37x slower                                                   |
| scimark_lu                 | 113 ms                                                       | 155 ms: 1.38x slower                                                    |
| pyflate                    | 449 ms                                                       | 625 ms: 1.39x slower                                                    |
| genshi_text                | 21.5 ms                                                      | 30.3 ms: 1.41x slower                                                   |
| python_startup             | 11.0 ms                                                      | 15.6 ms: 1.42x slower                                                   |
| richards_super             | 51.6 ms                                                      | 73.8 ms: 1.43x slower                                                   |
| richards                   | 45.2 ms                                                      | 64.7 ms: 1.43x slower                                                   |
| django_template            | 34.1 ms                                                      | 49.5 ms: 1.45x slower                                                   |
| logging_simple             | 6.16 us                                                      | 8.96 us: 1.45x slower                                                   |
| logging_format             | 6.84 us                                                      | 10.0 us: 1.46x slower                                                   |
| scimark_sor                | 134 ms                                                       | 199 ms: 1.48x slower                                                    |
| nbody                      | 85.1 ms                                                      | 126 ms: 1.48x slower                                                    |
| mako                       | 11.3 ms                                                      | 17.1 ms: 1.51x slower                                                   |
| hexiom                     | 5.99 ms                                                      | 9.11 ms: 1.52x slower                                                   |
| unpickle_pure_python       | 210 us                                                       | 320 us: 1.52x slower                                                    |
| scimark_monte_carlo        | 65.4 ms                                                      | 101 ms: 1.54x slower                                                    |
| chaos                      | 57.3 ms                                                      | 91.7 ms: 1.60x slower                                                   |
| go                         | 141 ms                                                       | 226 ms: 1.60x slower                                                    |
| comprehensions             | 16.5 us                                                      | 26.9 us: 1.64x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 489 us: 1.66x slower                                                    |
| sqlglot_transpile          | 1.56 ms                                                      | 2.62 ms: 1.68x slower                                                   |
| logging_silent             | 103 ns                                                       | 184 ns: 1.79x slower                                                    |
| sqlglot_parse              | 1.25 ms                                                      | 2.25 ms: 1.80x slower                                                   |
| raytrace                   | 253 ms                                                       | 483 ms: 1.91x slower                                                    |
| deltablue                  | 3.12 ms                                                      | 7.06 ms: 2.26x slower                                                   |
| bench_thread_pool          | 919 us                                                       | 3.38 ms: 3.68x slower                                                   |
| bench_mp_pool              | 11.0 ms                                                      | 93.8 ms: 8.53x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.26x slower                                                            |

Benchmark hidden because not significant (1): async_tree_none
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250111-3.14.0a3+-41ef420-NOGIL/bm-20250111-vultr-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.178x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.16x
- 95% likely to have a slowdown of 1.14x
- 99% likely to have a slowdown of 1.13x

# Memory
- memory change: 1.33x