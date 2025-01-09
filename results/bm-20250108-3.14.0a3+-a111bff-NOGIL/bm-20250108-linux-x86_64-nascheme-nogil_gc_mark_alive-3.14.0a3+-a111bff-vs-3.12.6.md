# Results vs. 3.12.6

- fork: nascheme
- ref: nogil_gc_mark_alive
- machine: linux-x86_64
- commit hash: a111bff
- commit date: 2025-01-08
- overall geometric mean: 1.120x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 600 ms: 1.31x slower                                                    |
| docutils       | 4.00 sec                                               | 4.23 sec: 1.06x slower                                                  |
| html5lib       | 88.9 ms                                                | 108 ms: 1.21x slower                                                    |
| Geometric mean | (ref)                                                  | 1.19x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 960 ms: 2.02x faster                                                    |
| async_tree_io              | 1.85 sec                                               | 1.07 sec: 1.73x faster                                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 542 ms: 1.72x faster                                                    |
| async_tree_none_tg         | 704 ms                                                 | 439 ms: 1.60x faster                                                    |
| async_tree_memoization     | 977 ms                                                 | 634 ms: 1.54x faster                                                    |
| async_tree_none            | 741 ms                                                 | 495 ms: 1.50x faster                                                    |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 748 ms: 1.47x faster                                                    |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 867 ms: 1.24x faster                                                    |
| async_generators           | 589 ms                                                 | 602 ms: 1.02x slower                                                    |
| coroutines                 | 29.5 ms                                                | 31.4 ms: 1.06x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.39x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 131 ms: 1.06x slower                                                    |
| nbody          | 119 ms                                                 | 173 ms: 1.45x slower                                                    |
| Geometric mean | (ref)                                                  | 1.14x slower                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.27 ms: 1.20x faster                                                   |
| regex_dna      | 278 ms                                                 | 321 ms: 1.15x slower                                                    |
| regex_compile  | 187 ms                                                 | 221 ms: 1.18x slower                                                    |
| Geometric mean | (ref)                                                  | 1.04x slower                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 135 ms: 1.25x faster                                                    |
| xml_etree_parse      | 241 ms                                                 | 222 ms: 1.08x faster                                                    |
| tomli_loads          | 2.88 sec                                               | 3.03 sec: 1.05x slower                                                  |
| xml_etree_generate   | 127 ms                                                 | 137 ms: 1.08x slower                                                    |
| json_dumps           | 14.3 ms                                                | 18.1 ms: 1.26x slower                                                   |
| unpickle_pure_python | 300 us                                                 | 389 us: 1.30x slower                                                    |
| xml_etree_process    | 83.7 ms                                                | 113 ms: 1.35x slower                                                    |
| pickle_pure_python   | 436 us                                                 | 702 us: 1.61x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.13x slower                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 20.2 ms: 1.15x slower                                                   |
| python_startup         | 23.7 ms                                                | 32.7 ms: 1.38x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.26x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 91.2 ms: 1.35x slower                                                   |
| genshi_text     | 30.2 ms                                                | 41.2 ms: 1.36x slower                                                   |
| django_template | 44.9 ms                                                | 70.3 ms: 1.56x slower                                                   |
| mako            | 15.7 ms                                                | 25.7 ms: 1.63x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.47x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 960 ms: 2.02x faster                                                    |
| async_tree_io              | 1.85 sec                                               | 1.07 sec: 1.73x faster                                                  |
| async_tree_memoization_tg  | 930 ms                                                 | 542 ms: 1.72x faster                                                    |
| async_tree_none_tg         | 704 ms                                                 | 439 ms: 1.60x faster                                                    |
| async_tree_memoization     | 977 ms                                                 | 634 ms: 1.54x faster                                                    |
| async_tree_none            | 741 ms                                                 | 495 ms: 1.50x faster                                                    |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 748 ms: 1.47x faster                                                    |
| xml_etree_iterparse        | 169 ms                                                 | 135 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 867 ms: 1.24x faster                                                    |
| regex_effbot               | 5.13 ms                                                | 4.27 ms: 1.20x faster                                                   |
| sqlite_synth               | 3.87 us                                                | 3.51 us: 1.10x faster                                                   |
| deepcopy                   | 468 us                                                 | 426 us: 1.10x faster                                                    |
| xml_etree_parse            | 241 ms                                                 | 222 ms: 1.08x faster                                                    |
| pycparser                  | 1.79 sec                                               | 1.67 sec: 1.07x faster                                                  |
| deepcopy_memo              | 52.4 us                                                | 50.3 us: 1.04x faster                                                   |
| async_generators           | 589 ms                                                 | 602 ms: 1.02x slower                                                    |
| tomli_loads                | 2.88 sec                                               | 3.03 sec: 1.05x slower                                                  |
| docutils                   | 4.00 sec                                               | 4.23 sec: 1.06x slower                                                  |
| float                      | 123 ms                                                 | 131 ms: 1.06x slower                                                    |
| coroutines                 | 29.5 ms                                                | 31.4 ms: 1.06x slower                                                   |
| json                       | 6.85 ms                                                | 7.29 ms: 1.06x slower                                                   |
| xml_etree_generate         | 127 ms                                                 | 137 ms: 1.08x slower                                                    |
| logging_simple             | 9.45 us                                                | 10.3 us: 1.09x slower                                                   |
| mdp                        | 3.97 sec                                               | 4.40 sec: 1.11x slower                                                  |
| scimark_fft                | 500 ms                                                 | 558 ms: 1.12x slower                                                    |
| deepcopy_reduce            | 4.04 us                                                | 4.56 us: 1.13x slower                                                   |
| pylint                     | 465 ms                                                 | 526 ms: 1.13x slower                                                    |
| dulwich_log                | 100 ms                                                 | 114 ms: 1.14x slower                                                    |
| sympy_sum                  | 222 ms                                                 | 255 ms: 1.15x slower                                                    |
| python_startup_no_site     | 17.6 ms                                                | 20.2 ms: 1.15x slower                                                   |
| regex_dna                  | 278 ms                                                 | 321 ms: 1.15x slower                                                    |
| crypto_pyaes               | 107 ms                                                 | 124 ms: 1.16x slower                                                    |
| bpe_tokeniser              | 6.59 sec                                               | 7.64 sec: 1.16x slower                                                  |
| comprehensions             | 27.1 us                                                | 31.8 us: 1.17x slower                                                   |
| sympy_expand               | 582 ms                                                 | 682 ms: 1.17x slower                                                    |
| sqlalchemy_declarative     | 218 ms                                                 | 256 ms: 1.18x slower                                                    |
| nqueens                    | 117 ms                                                 | 138 ms: 1.18x slower                                                    |
| regex_compile              | 187 ms                                                 | 221 ms: 1.18x slower                                                    |
| pyflate                    | 727 ms                                                 | 868 ms: 1.19x slower                                                    |
| telco                      | 9.59 ms                                                | 11.6 ms: 1.21x slower                                                   |
| html5lib                   | 88.9 ms                                                | 108 ms: 1.21x slower                                                    |
| sqlglot_normalize          | 157 ms                                                 | 191 ms: 1.21x slower                                                    |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.17 ms: 1.22x slower                                                   |
| sympy_integrate            | 29.8 ms                                                | 36.4 ms: 1.22x slower                                                   |
| thrift                     | 1.06 ms                                                | 1.31 ms: 1.24x slower                                                   |
| sqlglot_optimize           | 76.0 ms                                                | 94.0 ms: 1.24x slower                                                   |
| sympy_str                  | 385 ms                                                 | 478 ms: 1.24x slower                                                    |
| typing_runtime_protocols   | 224 us                                                 | 279 us: 1.24x slower                                                    |
| fannkuch                   | 540 ms                                                 | 674 ms: 1.25x slower                                                    |
| pprint_safe_repr           | 967 ms                                                 | 1.21 sec: 1.25x slower                                                  |
| meteor_contest             | 146 ms                                                 | 184 ms: 1.26x slower                                                    |
| richards_super             | 72.8 ms                                                | 91.6 ms: 1.26x slower                                                   |
| json_dumps                 | 14.3 ms                                                | 18.1 ms: 1.26x slower                                                   |
| unpickle_pure_python       | 300 us                                                 | 389 us: 1.30x slower                                                    |
| richards                   | 60.3 ms                                                | 78.5 ms: 1.30x slower                                                   |
| 2to3                       | 456 ms                                                 | 600 ms: 1.31x slower                                                    |
| logging_format             | 9.59 us                                                | 12.7 us: 1.33x slower                                                   |
| scimark_lu                 | 152 ms                                                 | 202 ms: 1.33x slower                                                    |
| chaos                      | 84.9 ms                                                | 113 ms: 1.33x slower                                                    |
| scimark_sor                | 167 ms                                                 | 222 ms: 1.33x slower                                                    |
| generators                 | 41.1 ms                                                | 54.8 ms: 1.33x slower                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 129 ms: 1.33x slower                                                    |
| pprint_pformat             | 1.98 sec                                               | 2.66 sec: 1.34x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 91.2 ms: 1.35x slower                                                   |
| xml_etree_process          | 83.7 ms                                                | 113 ms: 1.35x slower                                                    |
| genshi_text                | 30.2 ms                                                | 41.2 ms: 1.36x slower                                                   |
| coverage                   | 95.4 ms                                                | 131 ms: 1.37x slower                                                    |
| hexiom                     | 8.27 ms                                                | 11.4 ms: 1.38x slower                                                   |
| python_startup             | 23.7 ms                                                | 32.7 ms: 1.38x slower                                                   |
| raytrace                   | 408 ms                                                 | 563 ms: 1.38x slower                                                    |
| gc_traversal               | 5.86 ms                                                | 8.36 ms: 1.43x slower                                                   |
| nbody                      | 119 ms                                                 | 173 ms: 1.45x slower                                                    |
| sqlglot_transpile          | 2.34 ms                                                | 3.44 ms: 1.47x slower                                                   |
| create_gc_cycles           | 1.94 ms                                                | 2.89 ms: 1.49x slower                                                   |
| django_template            | 44.9 ms                                                | 70.3 ms: 1.56x slower                                                   |
| go                         | 172 ms                                                 | 272 ms: 1.58x slower                                                    |
| logging_silent             | 139 ns                                                 | 224 ns: 1.61x slower                                                    |
| pickle_pure_python         | 436 us                                                 | 702 us: 1.61x slower                                                    |
| sqlalchemy_imperative      | 24.7 ms                                                | 39.8 ms: 1.61x slower                                                   |
| mako                       | 15.7 ms                                                | 25.7 ms: 1.63x slower                                                   |
| sqlglot_parse              | 1.79 ms                                                | 3.07 ms: 1.72x slower                                                   |
| deltablue                  | 4.27 ms                                                | 9.71 ms: 2.28x slower                                                   |
| bench_mp_pool              | 20.7 ms                                                | 91.2 ms: 4.41x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.16x slower                                                            |

Benchmark hidden because not significant (7): pidigits, json_loads, pathlib, spectral_norm, asyncio_websockets, bench_thread_pool, regex_v8
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250108-3.14.0a3+-a111bff-NOGIL/bm-20250108-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-a111bff.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.120x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.34x