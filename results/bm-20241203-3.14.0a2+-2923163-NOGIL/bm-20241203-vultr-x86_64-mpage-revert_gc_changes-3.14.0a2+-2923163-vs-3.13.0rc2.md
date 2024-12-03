# Results vs. 3.13.0rc2

- fork: mpage
- ref: revert_gc_changes
- machine: linux-x86_64
- commit hash: 2923163
- commit date: 2024-12-03
- overall geometric mean: 1.279x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.23x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2+-2923163 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 377 ms: 1.45x slower                                               |
| docutils       | 2.62 sec                                                     | 3.18 sec: 1.22x slower                                             |
| html5lib       | 67.0 ms                                                      | 99.7 ms: 1.49x slower                                              |
| Geometric mean | (ref)                                                        | 1.38x slower                                                       |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2+-2923163 |
|---------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| async_tree_io_tg          | 913 ms                                                       | 870 ms: 1.05x faster                                               |
| async_tree_cpu_io_mixed   | 666 ms                                                       | 652 ms: 1.02x faster                                               |
| async_tree_memoization    | 461 ms                                                       | 491 ms: 1.06x slower                                               |
| async_tree_none_tg        | 336 ms                                                       | 367 ms: 1.09x slower                                               |
| async_tree_memoization_tg | 414 ms                                                       | 463 ms: 1.12x slower                                               |
| async_tree_none           | 354 ms                                                       | 401 ms: 1.13x slower                                               |
| coroutines                | 23.6 ms                                                      | 27.6 ms: 1.17x slower                                              |
| async_generators          | 377 ms                                                       | 468 ms: 1.24x slower                                               |
| Geometric mean            | (ref)                                                        | 1.07x slower                                                       |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed_tg, asyncio_websockets, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2+-2923163 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 182 ms: 1.19x faster                                               |
| nbody          | 85.1 ms                                                      | 133 ms: 1.57x slower                                               |
| float          | 77.5 ms                                                      | 144 ms: 1.86x slower                                               |
| Geometric mean | (ref)                                                        | 1.35x slower                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2+-2923163 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.67 ms: 1.15x faster                                              |
| regex_dna      | 180 ms                                                       | 175 ms: 1.03x faster                                               |
| regex_v8       | 22.7 ms                                                      | 23.3 ms: 1.03x slower                                              |
| regex_compile  | 132 ms                                                       | 193 ms: 1.46x slower                                               |
| Geometric mean | (ref)                                                        | 1.06x slower                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2+-2923163 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                               |
| json_loads           | 27.0 us                                                      | 28.2 us: 1.04x slower                                              |
| xml_etree_generate   | 85.4 ms                                                      | 102 ms: 1.20x slower                                               |
| tomli_loads          | 2.01 sec                                                     | 2.76 sec: 1.38x slower                                             |
| xml_etree_process    | 59.3 ms                                                      | 82.3 ms: 1.39x slower                                              |
| json_dumps           | 10.5 ms                                                      | 14.6 ms: 1.39x slower                                              |
| unpickle_pure_python | 210 us                                                       | 381 us: 1.82x slower                                               |
| pickle_pure_python   | 294 us                                                       | 567 us: 1.93x slower                                               |
| Geometric mean       | (ref)                                                        | 1.31x slower                                                       |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2+-2923163 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                              |
| python_startup         | 11.0 ms                                                      | 17.5 ms: 1.59x slower                                              |
| Geometric mean         | (ref)                                                        | 1.49x slower                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2+-2923163 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 66.9 ms: 1.37x slower                                              |
| genshi_text     | 21.5 ms                                                      | 33.9 ms: 1.57x slower                                              |
| django_template | 34.1 ms                                                      | 56.0 ms: 1.64x slower                                              |
| mako            | 11.3 ms                                                      | 20.1 ms: 1.77x slower                                              |
| Geometric mean  | (ref)                                                        | 1.58x slower                                                       |

All benchmarks:
===============

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2+-2923163 |
|---------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| pidigits                  | 217 ms                                                       | 182 ms: 1.19x faster                                               |
| regex_effbot              | 3.08 ms                                                      | 2.67 ms: 1.15x faster                                              |
| async_tree_io_tg          | 913 ms                                                       | 870 ms: 1.05x faster                                               |
| xml_etree_parse           | 136 ms                                                       | 130 ms: 1.05x faster                                               |
| regex_dna                 | 180 ms                                                       | 175 ms: 1.03x faster                                               |
| async_tree_cpu_io_mixed   | 666 ms                                                       | 652 ms: 1.02x faster                                               |
| gc_traversal              | 3.14 ms                                                      | 3.18 ms: 1.01x slower                                              |
| regex_v8                  | 22.7 ms                                                      | 23.3 ms: 1.03x slower                                              |
| json                      | 4.93 ms                                                      | 5.09 ms: 1.03x slower                                              |
| sqlite_synth              | 2.21 us                                                      | 2.30 us: 1.04x slower                                              |
| json_loads                | 27.0 us                                                      | 28.2 us: 1.04x slower                                              |
| async_tree_memoization    | 461 ms                                                       | 491 ms: 1.06x slower                                               |
| async_tree_none_tg        | 336 ms                                                       | 367 ms: 1.09x slower                                               |
| pathlib                   | 19.2 ms                                                      | 21.1 ms: 1.10x slower                                              |
| async_tree_memoization_tg | 414 ms                                                       | 463 ms: 1.12x slower                                               |
| async_tree_none           | 354 ms                                                       | 401 ms: 1.13x slower                                               |
| telco                     | 7.82 ms                                                      | 8.87 ms: 1.13x slower                                              |
| scimark_fft               | 349 ms                                                       | 406 ms: 1.16x slower                                               |
| deepcopy_memo             | 39.1 us                                                      | 45.7 us: 1.17x slower                                              |
| coroutines                | 23.6 ms                                                      | 27.6 ms: 1.17x slower                                              |
| spectral_norm             | 111 ms                                                       | 132 ms: 1.18x slower                                               |
| xml_etree_generate        | 85.4 ms                                                      | 102 ms: 1.20x slower                                               |
| deepcopy_reduce           | 3.11 us                                                      | 3.76 us: 1.21x slower                                              |
| coverage                  | 83.0 ms                                                      | 101 ms: 1.22x slower                                               |
| docutils                  | 2.62 sec                                                     | 3.18 sec: 1.22x slower                                             |
| bpe_tokeniser             | 4.45 sec                                                     | 5.46 sec: 1.23x slower                                             |
| async_generators          | 377 ms                                                       | 468 ms: 1.24x slower                                               |
| pylint                    | 317 ms                                                       | 394 ms: 1.24x slower                                               |
| scimark_sparse_mat_mult   | 4.71 ms                                                      | 5.87 ms: 1.25x slower                                              |
| mdp                       | 2.36 sec                                                     | 2.98 sec: 1.26x slower                                             |
| nqueens                   | 78.6 ms                                                      | 103 ms: 1.31x slower                                               |
| dulwich_log               | 74.8 ms                                                      | 98.8 ms: 1.32x slower                                              |
| meteor_contest            | 102 ms                                                       | 135 ms: 1.33x slower                                               |
| generators                | 28.8 ms                                                      | 38.6 ms: 1.34x slower                                              |
| create_gc_cycles          | 1.34 ms                                                      | 1.83 ms: 1.37x slower                                              |
| fannkuch                  | 370 ms                                                       | 506 ms: 1.37x slower                                               |
| genshi_xml                | 48.8 ms                                                      | 66.9 ms: 1.37x slower                                              |
| crypto_pyaes              | 67.9 ms                                                      | 93.4 ms: 1.38x slower                                              |
| tomli_loads               | 2.01 sec                                                     | 2.76 sec: 1.38x slower                                             |
| typing_runtime_protocols  | 155 us                                                       | 213 us: 1.38x slower                                               |
| xml_etree_process         | 59.3 ms                                                      | 82.3 ms: 1.39x slower                                              |
| python_startup_no_site    | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                              |
| json_dumps                | 10.5 ms                                                      | 14.6 ms: 1.39x slower                                              |
| sqlglot_optimize          | 52.7 ms                                                      | 75.4 ms: 1.43x slower                                              |
| sqlglot_normalize         | 106 ms                                                       | 152 ms: 1.44x slower                                               |
| pprint_safe_repr          | 738 ms                                                       | 1.06 sec: 1.44x slower                                             |
| pycparser                 | 1.12 sec                                                     | 1.62 sec: 1.45x slower                                             |
| 2to3                      | 260 ms                                                       | 377 ms: 1.45x slower                                               |
| regex_compile             | 132 ms                                                       | 193 ms: 1.46x slower                                               |
| pprint_pformat            | 1.50 sec                                                     | 2.20 sec: 1.47x slower                                             |
| html5lib                  | 67.0 ms                                                      | 99.7 ms: 1.49x slower                                              |
| thrift                    | 778 us                                                       | 1.21 ms: 1.55x slower                                              |
| sympy_integrate           | 19.8 ms                                                      | 30.8 ms: 1.55x slower                                              |
| nbody                     | 85.1 ms                                                      | 133 ms: 1.57x slower                                               |
| genshi_text               | 21.5 ms                                                      | 33.9 ms: 1.57x slower                                              |
| python_startup            | 11.0 ms                                                      | 17.5 ms: 1.59x slower                                              |
| pyflate                   | 449 ms                                                       | 728 ms: 1.62x slower                                               |
| django_template           | 34.1 ms                                                      | 56.0 ms: 1.64x slower                                              |
| scimark_lu                | 113 ms                                                       | 195 ms: 1.73x slower                                               |
| comprehensions            | 16.5 us                                                      | 29.0 us: 1.76x slower                                              |
| mako                      | 11.3 ms                                                      | 20.1 ms: 1.77x slower                                              |
| logging_simple            | 6.16 us                                                      | 11.0 us: 1.78x slower                                              |
| logging_format            | 6.84 us                                                      | 12.2 us: 1.78x slower                                              |
| sympy_str                 | 275 ms                                                       | 494 ms: 1.80x slower                                               |
| hexiom                    | 5.99 ms                                                      | 10.8 ms: 1.80x slower                                              |
| unpickle_pure_python      | 210 us                                                       | 381 us: 1.82x slower                                               |
| richards                  | 45.2 ms                                                      | 82.2 ms: 1.82x slower                                              |
| scimark_sor               | 134 ms                                                       | 245 ms: 1.82x slower                                               |
| float                     | 77.5 ms                                                      | 144 ms: 1.86x slower                                               |
| scimark_monte_carlo       | 65.4 ms                                                      | 123 ms: 1.88x slower                                               |
| richards_super            | 51.6 ms                                                      | 98.5 ms: 1.91x slower                                              |
| pickle_pure_python        | 294 us                                                       | 567 us: 1.93x slower                                               |
| chaos                     | 57.3 ms                                                      | 111 ms: 1.94x slower                                               |
| logging_silent            | 103 ns                                                       | 200 ns: 1.95x slower                                               |
| sqlglot_transpile         | 1.56 ms                                                      | 3.07 ms: 1.97x slower                                              |
| go                        | 141 ms                                                       | 280 ms: 1.99x slower                                               |
| sqlglot_parse             | 1.25 ms                                                      | 2.68 ms: 2.15x slower                                              |
| sympy_expand              | 457 ms                                                       | 982 ms: 2.15x slower                                               |
| sympy_sum                 | 156 ms                                                       | 357 ms: 2.30x slower                                               |
| raytrace                  | 253 ms                                                       | 599 ms: 2.37x slower                                               |
| deltablue                 | 3.12 ms                                                      | 8.83 ms: 2.83x slower                                              |
| bench_thread_pool         | 919 us                                                       | 3.39 ms: 3.68x slower                                              |
| bench_mp_pool             | 11.0 ms                                                      | 110 ms: 9.97x slower                                               |
| Geometric mean            | (ref)                                                        | 1.44x slower                                                       |

Benchmark hidden because not significant (5): async_tree_cpu_io_mixed_tg, xml_etree_iterparse, asyncio_websockets, deepcopy, async_tree_io
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241203-3.14.0a2+-2923163-NOGIL/bm-20241203-vultr-x86_64-mpage-revert_gc_changes-3.14.0a2+-2923163.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.279x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.28x
- 95% likely to have a slowdown of 1.26x
- 99% likely to have a slowdown of 1.23x

# Memory
- memory change: 1.31x