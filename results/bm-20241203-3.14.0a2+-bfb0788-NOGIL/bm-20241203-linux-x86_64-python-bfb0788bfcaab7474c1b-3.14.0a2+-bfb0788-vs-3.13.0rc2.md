# Results vs. 3.13.0rc2

- fork: python
- ref: bfb0788bfcaab7474c1b
- machine: linux-x86_64
- commit hash: bfb0788
- commit date: 2024-12-03
- overall geometric mean: 1.231x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.19x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 649 ms: 1.46x slower                                                   |
| docutils       | 4.01 sec                                                     | 4.44 sec: 1.11x slower                                                 |
| html5lib       | 92.6 ms                                                      | 124 ms: 1.34x slower                                                   |
| Geometric mean | (ref)                                                        | 1.29x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|---------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg          | 1.40 sec                                                     | 1.10 sec: 1.28x faster                                                 |
| async_tree_io             | 1.39 sec                                                     | 1.25 sec: 1.11x faster                                                 |
| async_tree_memoization_tg | 670 ms                                                       | 615 ms: 1.09x faster                                                   |
| asyncio_websockets        | 766 ms                                                       | 739 ms: 1.04x faster                                                   |
| async_generators          | 567 ms                                                       | 709 ms: 1.25x slower                                                   |
| coroutines                | 30.9 ms                                                      | 38.6 ms: 1.25x slower                                                  |
| Geometric mean            | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (5): async_tree_memoization, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_none, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 177 ms: 1.53x slower                                                   |
| nbody          | 119 ms                                                       | 195 ms: 1.64x slower                                                   |
| Geometric mean | (ref)                                                        | 1.34x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.35 ms: 1.09x faster                                                  |
| regex_v8       | 32.8 ms                                                      | 34.6 ms: 1.05x slower                                                  |
| regex_dna      | 282 ms                                                       | 305 ms: 1.08x slower                                                   |
| regex_compile  | 182 ms                                                       | 244 ms: 1.34x slower                                                   |
| Geometric mean | (ref)                                                        | 1.09x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 134 ms: 1.32x faster                                                   |
| xml_etree_parse      | 231 ms                                                       | 195 ms: 1.18x faster                                                   |
| json_loads           | 34.3 us                                                      | 36.8 us: 1.07x slower                                                  |
| xml_etree_generate   | 122 ms                                                       | 148 ms: 1.21x slower                                                   |
| xml_etree_process    | 85.9 ms                                                      | 106 ms: 1.23x slower                                                   |
| tomli_loads          | 2.78 sec                                                     | 3.57 sec: 1.28x slower                                                 |
| json_dumps           | 14.1 ms                                                      | 18.9 ms: 1.34x slower                                                  |
| unpickle_pure_python | 290 us                                                       | 476 us: 1.64x slower                                                   |
| pickle_pure_python   | 416 us                                                       | 686 us: 1.65x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.19x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 20.3 ms: 1.33x slower                                                  |
| python_startup         | 22.4 ms                                                      | 32.7 ms: 1.46x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.39x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 43.4 ms: 1.37x slower                                                  |
| genshi_xml      | 72.1 ms                                                      | 101 ms: 1.40x slower                                                   |
| django_template | 44.3 ms                                                      | 71.0 ms: 1.60x slower                                                  |
| mako            | 15.9 ms                                                      | 27.7 ms: 1.74x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.52x slower                                                           |

All benchmarks:
===============

| Benchmark                 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|---------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse       | 177 ms                                                       | 134 ms: 1.32x faster                                                   |
| async_tree_io_tg          | 1.40 sec                                                     | 1.10 sec: 1.28x faster                                                 |
| xml_etree_parse           | 231 ms                                                       | 195 ms: 1.18x faster                                                   |
| deepcopy                  | 498 us                                                       | 438 us: 1.14x faster                                                   |
| async_tree_io             | 1.39 sec                                                     | 1.25 sec: 1.11x faster                                                 |
| async_tree_memoization_tg | 670 ms                                                       | 615 ms: 1.09x faster                                                   |
| regex_effbot              | 4.74 ms                                                      | 4.35 ms: 1.09x faster                                                  |
| sqlite_synth              | 3.99 us                                                      | 3.76 us: 1.06x faster                                                  |
| asyncio_websockets        | 766 ms                                                       | 739 ms: 1.04x faster                                                   |
| gc_traversal              | 5.70 ms                                                      | 5.93 ms: 1.04x slower                                                  |
| regex_v8                  | 32.8 ms                                                      | 34.6 ms: 1.05x slower                                                  |
| telco                     | 12.2 ms                                                      | 13.1 ms: 1.07x slower                                                  |
| json_loads                | 34.3 us                                                      | 36.8 us: 1.07x slower                                                  |
| regex_dna                 | 282 ms                                                       | 305 ms: 1.08x slower                                                   |
| docutils                  | 4.01 sec                                                     | 4.44 sec: 1.11x slower                                                 |
| json                      | 6.51 ms                                                      | 7.26 ms: 1.11x slower                                                  |
| nqueens                   | 112 ms                                                       | 127 ms: 1.14x slower                                                   |
| deepcopy_reduce           | 4.10 us                                                      | 4.66 us: 1.14x slower                                                  |
| scimark_fft               | 473 ms                                                       | 539 ms: 1.14x slower                                                   |
| spectral_norm             | 157 ms                                                       | 179 ms: 1.15x slower                                                   |
| meteor_contest            | 150 ms                                                       | 174 ms: 1.16x slower                                                   |
| deepcopy_memo             | 50.1 us                                                      | 59.4 us: 1.18x slower                                                  |
| pylint                    | 470 ms                                                       | 561 ms: 1.19x slower                                                   |
| crypto_pyaes              | 100 ms                                                       | 120 ms: 1.19x slower                                                   |
| scimark_sparse_mat_mult   | 6.76 ms                                                      | 8.09 ms: 1.20x slower                                                  |
| xml_etree_generate        | 122 ms                                                       | 148 ms: 1.21x slower                                                   |
| mdp                       | 3.80 sec                                                     | 4.65 sec: 1.22x slower                                                 |
| xml_etree_process         | 85.9 ms                                                      | 106 ms: 1.23x slower                                                   |
| async_generators          | 567 ms                                                       | 709 ms: 1.25x slower                                                   |
| coroutines                | 30.9 ms                                                      | 38.6 ms: 1.25x slower                                                  |
| fannkuch                  | 547 ms                                                       | 687 ms: 1.26x slower                                                   |
| dulwich_log               | 93.7 ms                                                      | 119 ms: 1.27x slower                                                   |
| tomli_loads               | 2.78 sec                                                     | 3.57 sec: 1.28x slower                                                 |
| sqlglot_optimize          | 74.7 ms                                                      | 96.8 ms: 1.30x slower                                                  |
| pycparser                 | 1.57 sec                                                     | 2.04 sec: 1.30x slower                                                 |
| bench_thread_pool         | 2.89 ms                                                      | 3.76 ms: 1.30x slower                                                  |
| bpe_tokeniser             | 6.28 sec                                                     | 8.23 sec: 1.31x slower                                                 |
| python_startup_no_site    | 15.3 ms                                                      | 20.3 ms: 1.33x slower                                                  |
| typing_runtime_protocols  | 226 us                                                       | 300 us: 1.33x slower                                                   |
| json_dumps                | 14.1 ms                                                      | 18.9 ms: 1.34x slower                                                  |
| regex_compile             | 182 ms                                                       | 244 ms: 1.34x slower                                                   |
| html5lib                  | 92.6 ms                                                      | 124 ms: 1.34x slower                                                   |
| sympy_integrate           | 30.2 ms                                                      | 40.7 ms: 1.35x slower                                                  |
| generators                | 40.0 ms                                                      | 54.0 ms: 1.35x slower                                                  |
| create_gc_cycles          | 2.41 ms                                                      | 3.28 ms: 1.36x slower                                                  |
| thrift                    | 1.10 ms                                                      | 1.49 ms: 1.36x slower                                                  |
| pprint_safe_repr          | 987 ms                                                       | 1.34 sec: 1.36x slower                                                 |
| genshi_text               | 31.7 ms                                                      | 43.4 ms: 1.37x slower                                                  |
| coverage                  | 107 ms                                                       | 148 ms: 1.38x slower                                                   |
| genshi_xml                | 72.1 ms                                                      | 101 ms: 1.40x slower                                                   |
| sqlglot_normalize         | 140 ms                                                       | 198 ms: 1.42x slower                                                   |
| 2to3                      | 445 ms                                                       | 649 ms: 1.46x slower                                                   |
| pyflate                   | 664 ms                                                       | 967 ms: 1.46x slower                                                   |
| python_startup            | 22.4 ms                                                      | 32.7 ms: 1.46x slower                                                  |
| pprint_pformat            | 1.94 sec                                                     | 2.84 sec: 1.46x slower                                                 |
| float                     | 116 ms                                                       | 177 ms: 1.53x slower                                                   |
| richards_super            | 73.2 ms                                                      | 115 ms: 1.56x slower                                                   |
| richards                  | 65.5 ms                                                      | 103 ms: 1.57x slower                                                   |
| django_template           | 44.3 ms                                                      | 71.0 ms: 1.60x slower                                                  |
| comprehensions            | 22.2 us                                                      | 36.0 us: 1.62x slower                                                  |
| sympy_str                 | 379 ms                                                       | 617 ms: 1.63x slower                                                   |
| scimark_monte_carlo       | 90.6 ms                                                      | 148 ms: 1.64x slower                                                   |
| unpickle_pure_python      | 290 us                                                       | 476 us: 1.64x slower                                                   |
| nbody                     | 119 ms                                                       | 195 ms: 1.64x slower                                                   |
| pickle_pure_python        | 416 us                                                       | 686 us: 1.65x slower                                                   |
| scimark_lu                | 146 ms                                                       | 244 ms: 1.67x slower                                                   |
| logging_simple            | 8.56 us                                                      | 14.4 us: 1.68x slower                                                  |
| go                        | 191 ms                                                       | 325 ms: 1.70x slower                                                   |
| scimark_sor               | 179 ms                                                       | 308 ms: 1.72x slower                                                   |
| mako                      | 15.9 ms                                                      | 27.7 ms: 1.74x slower                                                  |
| logging_format            | 9.24 us                                                      | 16.1 us: 1.74x slower                                                  |
| chaos                     | 83.6 ms                                                      | 150 ms: 1.79x slower                                                   |
| logging_silent            | 130 ns                                                       | 241 ns: 1.86x slower                                                   |
| sqlglot_parse             | 1.76 ms                                                      | 3.28 ms: 1.87x slower                                                  |
| hexiom                    | 8.11 ms                                                      | 15.4 ms: 1.90x slower                                                  |
| sqlglot_transpile         | 2.20 ms                                                      | 4.42 ms: 2.01x slower                                                  |
| raytrace                  | 344 ms                                                       | 702 ms: 2.04x slower                                                   |
| sympy_expand              | 601 ms                                                       | 1.23 sec: 2.04x slower                                                 |
| sympy_sum                 | 210 ms                                                       | 452 ms: 2.15x slower                                                   |
| deltablue                 | 4.44 ms                                                      | 11.1 ms: 2.51x slower                                                  |
| bench_mp_pool             | 18.7 ms                                                      | 105 ms: 5.62x slower                                                   |
| Geometric mean            | (ref)                                                        | 1.33x slower                                                           |

Benchmark hidden because not significant (7): async_tree_memoization, pidigits, async_tree_none_tg, async_tree_cpu_io_mixed, async_tree_none, pathlib, async_tree_cpu_io_mixed_tg
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241203-3.14.0a2+-bfb0788-NOGIL/bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.231x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.23x
- 95% likely to have a slowdown of 1.22x
- 99% likely to have a slowdown of 1.19x

# Memory
- memory change: 1.33x