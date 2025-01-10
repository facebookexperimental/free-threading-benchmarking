# Results vs. 3.13.0rc2

- fork: nascheme
- ref: nogil_gc_mark_alive
- machine: linux-x86_64
- commit hash: f509a13
- commit date: 2025-01-09
- overall geometric mean: 1.213x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.19x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 681 ms: 1.53x slower                                                    |
| docutils       | 4.01 sec                                                     | 4.92 sec: 1.23x slower                                                  |
| html5lib       | 92.6 ms                                                      | 129 ms: 1.39x slower                                                    |
| Geometric mean | (ref)                                                        | 1.38x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|---------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg          | 1.40 sec                                                     | 1.04 sec: 1.35x faster                                                  |
| async_tree_io             | 1.39 sec                                                     | 1.14 sec: 1.22x faster                                                  |
| async_tree_memoization_tg | 670 ms                                                       | 577 ms: 1.16x faster                                                    |
| async_tree_none_tg        | 504 ms                                                       | 436 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed   | 889 ms                                                       | 816 ms: 1.09x faster                                                    |
| async_tree_memoization    | 709 ms                                                       | 652 ms: 1.09x faster                                                    |
| asyncio_websockets        | 766 ms                                                       | 830 ms: 1.08x slower                                                    |
| async_generators          | 567 ms                                                       | 665 ms: 1.17x slower                                                    |
| coroutines                | 30.9 ms                                                      | 37.4 ms: 1.21x slower                                                   |
| Geometric mean            | (ref)                                                        | 1.05x faster                                                            |

Benchmark hidden because not significant (2): async_tree_none, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 236 ms: 1.06x faster                                                    |
| float          | 116 ms                                                       | 146 ms: 1.26x slower                                                    |
| nbody          | 119 ms                                                       | 197 ms: 1.66x slower                                                    |
| Geometric mean | (ref)                                                        | 1.25x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 34.8 ms: 1.06x slower                                                   |
| regex_compile  | 182 ms                                                       | 234 ms: 1.29x slower                                                    |
| Geometric mean | (ref)                                                        | 1.08x slower                                                            |

Benchmark hidden because not significant (2): regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 151 ms: 1.17x faster                                                    |
| xml_etree_parse      | 231 ms                                                       | 256 ms: 1.11x slower                                                    |
| tomli_loads          | 2.78 sec                                                     | 3.23 sec: 1.16x slower                                                  |
| xml_etree_generate   | 122 ms                                                       | 145 ms: 1.18x slower                                                    |
| json_loads           | 34.3 us                                                      | 41.7 us: 1.22x slower                                                   |
| xml_etree_process    | 85.9 ms                                                      | 108 ms: 1.26x slower                                                    |
| json_dumps           | 14.1 ms                                                      | 19.0 ms: 1.35x slower                                                   |
| unpickle_pure_python | 290 us                                                       | 468 us: 1.61x slower                                                    |
| pickle_pure_python   | 416 us                                                       | 813 us: 1.95x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.27x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 27.2 ms: 1.78x slower                                                   |
| python_startup         | 22.4 ms                                                      | 42.9 ms: 1.91x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.84x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 97.3 ms: 1.35x slower                                                   |
| genshi_text     | 31.7 ms                                                      | 43.1 ms: 1.36x slower                                                   |
| django_template | 44.3 ms                                                      | 61.3 ms: 1.38x slower                                                   |
| mako            | 15.9 ms                                                      | 27.5 ms: 1.73x slower                                                   |
| Geometric mean  | (ref)                                                        | 1.45x slower                                                            |

All benchmarks:
===============

| Benchmark                 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13 |
|---------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg          | 1.40 sec                                                     | 1.04 sec: 1.35x faster                                                  |
| async_tree_io             | 1.39 sec                                                     | 1.14 sec: 1.22x faster                                                  |
| xml_etree_iterparse       | 177 ms                                                       | 151 ms: 1.17x faster                                                    |
| async_tree_memoization_tg | 670 ms                                                       | 577 ms: 1.16x faster                                                    |
| async_tree_none_tg        | 504 ms                                                       | 436 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed   | 889 ms                                                       | 816 ms: 1.09x faster                                                    |
| async_tree_memoization    | 709 ms                                                       | 652 ms: 1.09x faster                                                    |
| pidigits                  | 251 ms                                                       | 236 ms: 1.06x faster                                                    |
| sqlite_synth              | 3.99 us                                                      | 4.22 us: 1.06x slower                                                   |
| regex_v8                  | 32.8 ms                                                      | 34.8 ms: 1.06x slower                                                   |
| asyncio_websockets        | 766 ms                                                       | 830 ms: 1.08x slower                                                    |
| xml_etree_parse           | 231 ms                                                       | 256 ms: 1.11x slower                                                    |
| pathlib                   | 29.9 ms                                                      | 33.7 ms: 1.13x slower                                                   |
| deepcopy_reduce           | 4.10 us                                                      | 4.63 us: 1.13x slower                                                   |
| pylint                    | 470 ms                                                       | 540 ms: 1.15x slower                                                    |
| tomli_loads               | 2.78 sec                                                     | 3.23 sec: 1.16x slower                                                  |
| async_generators          | 567 ms                                                       | 665 ms: 1.17x slower                                                    |
| xml_etree_generate        | 122 ms                                                       | 145 ms: 1.18x slower                                                    |
| deepcopy_memo             | 50.1 us                                                      | 59.6 us: 1.19x slower                                                   |
| scimark_fft               | 473 ms                                                       | 563 ms: 1.19x slower                                                    |
| coroutines                | 30.9 ms                                                      | 37.4 ms: 1.21x slower                                                   |
| json_loads                | 34.3 us                                                      | 41.7 us: 1.22x slower                                                   |
| json                      | 6.51 ms                                                      | 7.98 ms: 1.23x slower                                                   |
| docutils                  | 4.01 sec                                                     | 4.92 sec: 1.23x slower                                                  |
| sympy_expand              | 601 ms                                                       | 750 ms: 1.25x slower                                                    |
| sqlglot_normalize         | 140 ms                                                       | 175 ms: 1.25x slower                                                    |
| pycparser                 | 1.57 sec                                                     | 1.98 sec: 1.26x slower                                                  |
| xml_etree_process         | 85.9 ms                                                      | 108 ms: 1.26x slower                                                    |
| fannkuch                  | 547 ms                                                       | 691 ms: 1.26x slower                                                    |
| thrift                    | 1.10 ms                                                      | 1.39 ms: 1.26x slower                                                   |
| float                     | 116 ms                                                       | 146 ms: 1.26x slower                                                    |
| sympy_integrate           | 30.2 ms                                                      | 38.5 ms: 1.27x slower                                                   |
| mdp                       | 3.80 sec                                                     | 4.86 sec: 1.28x slower                                                  |
| sqlglot_optimize          | 74.7 ms                                                      | 95.7 ms: 1.28x slower                                                   |
| regex_compile             | 182 ms                                                       | 234 ms: 1.29x slower                                                    |
| typing_runtime_protocols  | 226 us                                                       | 290 us: 1.29x slower                                                    |
| nqueens                   | 112 ms                                                       | 145 ms: 1.30x slower                                                    |
| meteor_contest            | 150 ms                                                       | 196 ms: 1.30x slower                                                    |
| coverage                  | 107 ms                                                       | 142 ms: 1.32x slower                                                    |
| crypto_pyaes              | 100 ms                                                       | 134 ms: 1.33x slower                                                    |
| richards                  | 65.5 ms                                                      | 88.2 ms: 1.35x slower                                                   |
| json_dumps                | 14.1 ms                                                      | 19.0 ms: 1.35x slower                                                   |
| genshi_xml                | 72.1 ms                                                      | 97.3 ms: 1.35x slower                                                   |
| pprint_pformat            | 1.94 sec                                                     | 2.64 sec: 1.36x slower                                                  |
| richards_super            | 73.2 ms                                                      | 99.6 ms: 1.36x slower                                                   |
| genshi_text               | 31.7 ms                                                      | 43.1 ms: 1.36x slower                                                   |
| scimark_lu                | 146 ms                                                       | 200 ms: 1.37x slower                                                    |
| sympy_str                 | 379 ms                                                       | 520 ms: 1.37x slower                                                    |
| pprint_safe_repr          | 987 ms                                                       | 1.36 sec: 1.38x slower                                                  |
| pyflate                   | 664 ms                                                       | 917 ms: 1.38x slower                                                    |
| scimark_sparse_mat_mult   | 6.76 ms                                                      | 9.34 ms: 1.38x slower                                                   |
| scimark_sor               | 179 ms                                                       | 247 ms: 1.38x slower                                                    |
| django_template           | 44.3 ms                                                      | 61.3 ms: 1.38x slower                                                   |
| sympy_sum                 | 210 ms                                                       | 292 ms: 1.39x slower                                                    |
| html5lib                  | 92.6 ms                                                      | 129 ms: 1.39x slower                                                    |
| generators                | 40.0 ms                                                      | 56.0 ms: 1.40x slower                                                   |
| bpe_tokeniser             | 6.28 sec                                                     | 8.87 sec: 1.41x slower                                                  |
| logging_format            | 9.24 us                                                      | 13.2 us: 1.42x slower                                                   |
| scimark_monte_carlo       | 90.6 ms                                                      | 133 ms: 1.47x slower                                                    |
| 2to3                      | 445 ms                                                       | 681 ms: 1.53x slower                                                    |
| hexiom                    | 8.11 ms                                                      | 12.4 ms: 1.53x slower                                                   |
| logging_simple            | 8.56 us                                                      | 13.1 us: 1.53x slower                                                   |
| unpickle_pure_python      | 290 us                                                       | 468 us: 1.61x slower                                                    |
| comprehensions            | 22.2 us                                                      | 36.2 us: 1.63x slower                                                   |
| go                        | 191 ms                                                       | 314 ms: 1.65x slower                                                    |
| create_gc_cycles          | 2.41 ms                                                      | 3.97 ms: 1.65x slower                                                   |
| chaos                     | 83.6 ms                                                      | 138 ms: 1.65x slower                                                    |
| nbody                     | 119 ms                                                       | 197 ms: 1.66x slower                                                    |
| dulwich_log               | 93.7 ms                                                      | 155 ms: 1.66x slower                                                    |
| mako                      | 15.9 ms                                                      | 27.5 ms: 1.73x slower                                                   |
| sqlglot_parse             | 1.76 ms                                                      | 3.12 ms: 1.78x slower                                                   |
| python_startup_no_site    | 15.3 ms                                                      | 27.2 ms: 1.78x slower                                                   |
| gc_traversal              | 5.70 ms                                                      | 10.2 ms: 1.78x slower                                                   |
| logging_silent            | 130 ns                                                       | 233 ns: 1.79x slower                                                    |
| raytrace                  | 344 ms                                                       | 644 ms: 1.87x slower                                                    |
| sqlglot_transpile         | 2.20 ms                                                      | 4.15 ms: 1.89x slower                                                   |
| python_startup            | 22.4 ms                                                      | 42.9 ms: 1.91x slower                                                   |
| pickle_pure_python        | 416 us                                                       | 813 us: 1.95x slower                                                    |
| bench_thread_pool         | 2.89 ms                                                      | 5.81 ms: 2.01x slower                                                   |
| deltablue                 | 4.44 ms                                                      | 10.3 ms: 2.33x slower                                                   |
| bench_mp_pool             | 18.7 ms                                                      | 101 ms: 5.41x slower                                                    |
| Geometric mean            | (ref)                                                        | 1.32x slower                                                            |

Benchmark hidden because not significant (7): deepcopy, telco, regex_dna, async_tree_none, async_tree_cpu_io_mixed_tg, regex_effbot, spectral_norm
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250109-3.14.0a3+-f509a13-NOGIL/bm-20250109-linux-x86_64-nascheme-nogil_gc_mark_alive-3.14.0a3+-f509a13.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.213x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.23x
- 95% likely to have a slowdown of 1.22x
- 99% likely to have a slowdown of 1.19x

# Memory
- memory change: 1.34x