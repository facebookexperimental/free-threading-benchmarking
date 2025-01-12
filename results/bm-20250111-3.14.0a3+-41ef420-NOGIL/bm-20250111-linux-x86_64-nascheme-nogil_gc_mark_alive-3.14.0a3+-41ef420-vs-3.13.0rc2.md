# Results vs. 3.13.0rc2

- fork: nascheme
- ref: nogil_gc_mark_alive
- machine: linux-x86_64
- commit hash: 41ef420
- commit date: 2025-01-11
- overall geometric mean: 1.203x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 660 ms: 1.48x slower                                                    |
| docutils       | 4.01 sec                                                     | 4.79 sec: 1.20x slower                                                  |
| html5lib       | 92.6 ms                                                      | 133 ms: 1.43x slower                                                    |
| Geometric mean | (ref)                                                        | 1.36x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 996 ms: 1.41x faster                                                    |
| async_tree_io              | 1.39 sec                                                     | 1.12 sec: 1.23x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 445 ms: 1.13x faster                                                    |
| async_tree_none            | 572 ms                                                       | 535 ms: 1.07x faster                                                    |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 806 ms: 1.06x faster                                                    |
| asyncio_websockets         | 766 ms                                                       | 827 ms: 1.08x slower                                                    |
| async_generators           | 567 ms                                                       | 681 ms: 1.20x slower                                                    |
| coroutines                 | 30.9 ms                                                      | 38.7 ms: 1.25x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                            |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 236 ms: 1.06x faster                                                    |
| float          | 116 ms                                                       | 151 ms: 1.30x slower                                                    |
| nbody          | 119 ms                                                       | 177 ms: 1.49x slower                                                    |
| Geometric mean | (ref)                                                        | 1.22x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.49 ms: 1.06x faster                                                   |
| regex_v8       | 32.8 ms                                                      | 34.0 ms: 1.04x slower                                                   |
| regex_dna      | 282 ms                                                       | 325 ms: 1.16x slower                                                    |
| regex_compile  | 182 ms                                                       | 256 ms: 1.40x slower                                                    |
| Geometric mean | (ref)                                                        | 1.12x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 143 ms: 1.24x faster                                                    |
| xml_etree_parse      | 231 ms                                                       | 206 ms: 1.12x faster                                                    |
| tomli_loads          | 2.78 sec                                                     | 3.20 sec: 1.15x slower                                                  |
| xml_etree_generate   | 122 ms                                                       | 150 ms: 1.23x slower                                                    |
| xml_etree_process    | 85.9 ms                                                      | 108 ms: 1.26x slower                                                    |
| json_loads           | 34.3 us                                                      | 43.1 us: 1.26x slower                                                   |
| json_dumps           | 14.1 ms                                                      | 18.0 ms: 1.28x slower                                                   |
| pickle_pure_python   | 416 us                                                       | 615 us: 1.48x slower                                                    |
| unpickle_pure_python | 290 us                                                       | 475 us: 1.64x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.19x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 22.4 ms                                                      | 36.2 ms: 1.62x slower                                                   |
| python_startup_no_site | 15.3 ms                                                      | 26.0 ms: 1.70x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.66x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 89.7 ms: 1.24x slower                                                   |
| genshi_text     | 31.7 ms                                                      | 41.6 ms: 1.32x slower                                                   |
| django_template | 44.3 ms                                                      | 65.3 ms: 1.47x slower                                                   |
| mako            | 15.9 ms                                                      | 25.5 ms: 1.60x slower                                                   |
| Geometric mean  | (ref)                                                        | 1.40x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 996 ms: 1.41x faster                                                    |
| xml_etree_iterparse        | 177 ms                                                       | 143 ms: 1.24x faster                                                    |
| async_tree_io              | 1.39 sec                                                     | 1.12 sec: 1.23x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 445 ms: 1.13x faster                                                    |
| xml_etree_parse            | 231 ms                                                       | 206 ms: 1.12x faster                                                    |
| deepcopy                   | 498 us                                                       | 449 us: 1.11x faster                                                    |
| async_tree_none            | 572 ms                                                       | 535 ms: 1.07x faster                                                    |
| pidigits                   | 251 ms                                                       | 236 ms: 1.06x faster                                                    |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 806 ms: 1.06x faster                                                    |
| regex_effbot               | 4.74 ms                                                      | 4.49 ms: 1.06x faster                                                   |
| telco                      | 12.2 ms                                                      | 11.6 ms: 1.05x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.82 us: 1.04x faster                                                   |
| regex_v8                   | 32.8 ms                                                      | 34.0 ms: 1.04x slower                                                   |
| asyncio_websockets         | 766 ms                                                       | 827 ms: 1.08x slower                                                    |
| spectral_norm              | 157 ms                                                       | 175 ms: 1.12x slower                                                    |
| pathlib                    | 29.9 ms                                                      | 33.5 ms: 1.12x slower                                                   |
| deepcopy_memo              | 50.1 us                                                      | 57.4 us: 1.15x slower                                                   |
| tomli_loads                | 2.78 sec                                                     | 3.20 sec: 1.15x slower                                                  |
| regex_dna                  | 282 ms                                                       | 325 ms: 1.16x slower                                                    |
| scimark_fft                | 473 ms                                                       | 549 ms: 1.16x slower                                                    |
| pycparser                  | 1.57 sec                                                     | 1.86 sec: 1.19x slower                                                  |
| meteor_contest             | 150 ms                                                       | 178 ms: 1.19x slower                                                    |
| deepcopy_reduce            | 4.10 us                                                      | 4.89 us: 1.19x slower                                                   |
| docutils                   | 4.01 sec                                                     | 4.79 sec: 1.20x slower                                                  |
| nqueens                    | 112 ms                                                       | 134 ms: 1.20x slower                                                    |
| async_generators           | 567 ms                                                       | 681 ms: 1.20x slower                                                    |
| xml_etree_generate         | 122 ms                                                       | 150 ms: 1.23x slower                                                    |
| coverage                   | 107 ms                                                       | 133 ms: 1.24x slower                                                    |
| genshi_xml                 | 72.1 ms                                                      | 89.7 ms: 1.24x slower                                                   |
| fannkuch                   | 547 ms                                                       | 684 ms: 1.25x slower                                                    |
| coroutines                 | 30.9 ms                                                      | 38.7 ms: 1.25x slower                                                   |
| xml_etree_process          | 85.9 ms                                                      | 108 ms: 1.26x slower                                                    |
| json_loads                 | 34.3 us                                                      | 43.1 us: 1.26x slower                                                   |
| richards                   | 65.5 ms                                                      | 83.0 ms: 1.27x slower                                                   |
| sympy_expand               | 601 ms                                                       | 762 ms: 1.27x slower                                                    |
| dulwich_log                | 93.7 ms                                                      | 119 ms: 1.27x slower                                                    |
| json_dumps                 | 14.1 ms                                                      | 18.0 ms: 1.28x slower                                                   |
| mdp                        | 3.80 sec                                                     | 4.89 sec: 1.29x slower                                                  |
| sqlglot_normalize          | 140 ms                                                       | 180 ms: 1.29x slower                                                    |
| float                      | 116 ms                                                       | 151 ms: 1.30x slower                                                    |
| genshi_text                | 31.7 ms                                                      | 41.6 ms: 1.32x slower                                                   |
| sympy_integrate            | 30.2 ms                                                      | 39.8 ms: 1.32x slower                                                   |
| sqlglot_optimize           | 74.7 ms                                                      | 98.4 ms: 1.32x slower                                                   |
| logging_format             | 9.24 us                                                      | 12.2 us: 1.32x slower                                                   |
| crypto_pyaes               | 100 ms                                                       | 133 ms: 1.33x slower                                                    |
| sympy_str                  | 379 ms                                                       | 513 ms: 1.35x slower                                                    |
| scimark_lu                 | 146 ms                                                       | 201 ms: 1.37x slower                                                    |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 9.40 ms: 1.39x slower                                                   |
| scimark_sor                | 179 ms                                                       | 249 ms: 1.39x slower                                                    |
| sympy_sum                  | 210 ms                                                       | 293 ms: 1.40x slower                                                    |
| bpe_tokeniser              | 6.28 sec                                                     | 8.78 sec: 1.40x slower                                                  |
| pyflate                    | 664 ms                                                       | 928 ms: 1.40x slower                                                    |
| regex_compile              | 182 ms                                                       | 256 ms: 1.40x slower                                                    |
| go                         | 191 ms                                                       | 269 ms: 1.41x slower                                                    |
| pprint_safe_repr           | 987 ms                                                       | 1.40 sec: 1.42x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 8.15 ms: 1.43x slower                                                   |
| create_gc_cycles           | 2.41 ms                                                      | 3.45 ms: 1.43x slower                                                   |
| html5lib                   | 92.6 ms                                                      | 133 ms: 1.43x slower                                                    |
| generators                 | 40.0 ms                                                      | 57.7 ms: 1.44x slower                                                   |
| typing_runtime_protocols   | 226 us                                                       | 326 us: 1.45x slower                                                    |
| logging_simple             | 8.56 us                                                      | 12.4 us: 1.45x slower                                                   |
| thrift                     | 1.10 ms                                                      | 1.60 ms: 1.46x slower                                                   |
| pprint_pformat             | 1.94 sec                                                     | 2.83 sec: 1.46x slower                                                  |
| django_template            | 44.3 ms                                                      | 65.3 ms: 1.47x slower                                                   |
| pickle_pure_python         | 416 us                                                       | 615 us: 1.48x slower                                                    |
| 2to3                       | 445 ms                                                       | 660 ms: 1.48x slower                                                    |
| nbody                      | 119 ms                                                       | 177 ms: 1.49x slower                                                    |
| chaos                      | 83.6 ms                                                      | 131 ms: 1.57x slower                                                    |
| richards_super             | 73.2 ms                                                      | 116 ms: 1.58x slower                                                    |
| mako                       | 15.9 ms                                                      | 25.5 ms: 1.60x slower                                                   |
| python_startup             | 22.4 ms                                                      | 36.2 ms: 1.62x slower                                                   |
| scimark_monte_carlo        | 90.6 ms                                                      | 148 ms: 1.64x slower                                                    |
| unpickle_pure_python       | 290 us                                                       | 475 us: 1.64x slower                                                    |
| hexiom                     | 8.11 ms                                                      | 13.8 ms: 1.70x slower                                                   |
| python_startup_no_site     | 15.3 ms                                                      | 26.0 ms: 1.70x slower                                                   |
| logging_silent             | 130 ns                                                       | 222 ns: 1.71x slower                                                    |
| sqlglot_transpile          | 2.20 ms                                                      | 3.80 ms: 1.73x slower                                                   |
| comprehensions             | 22.2 us                                                      | 39.7 us: 1.79x slower                                                   |
| bench_thread_pool          | 2.89 ms                                                      | 5.23 ms: 1.81x slower                                                   |
| raytrace                   | 344 ms                                                       | 659 ms: 1.91x slower                                                    |
| sqlglot_parse              | 1.76 ms                                                      | 3.37 ms: 1.92x slower                                                   |
| deltablue                  | 4.44 ms                                                      | 10.6 ms: 2.38x slower                                                   |
| bench_mp_pool              | 18.7 ms                                                      | 96.3 ms: 5.15x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.30x slower                                                            |

Benchmark hidden because not significant (5): async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_memoization, json, pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250111-3.14.0a3+-41ef420-NOGIL/bm-20250111-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-41ef420.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.203x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.21x
- 95% likely to have a slowdown of 1.20x
- 99% likely to have a slowdown of 1.18x

# Memory
- memory change: 1.33x