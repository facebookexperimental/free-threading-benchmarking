# Results vs. 3.13.0rc2

- fork: colesbury
- ref: stackpointer
- machine: linux-x86_64
- commit hash: bba99b4
- commit date: 2024-12-09
- overall geometric mean: 1.259x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.19x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 372 ms: 1.43x slower                                              |
| docutils       | 2.62 sec                                                     | 3.11 sec: 1.19x slower                                            |
| html5lib       | 67.0 ms                                                      | 98.0 ms: 1.46x slower                                             |
| Geometric mean | (ref)                                                        | 1.36x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|---------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io_tg          | 913 ms                                                       | 838 ms: 1.09x faster                                              |
| async_tree_cpu_io_mixed   | 666 ms                                                       | 654 ms: 1.02x faster                                              |
| async_tree_memoization    | 461 ms                                                       | 482 ms: 1.05x slower                                              |
| coroutines                | 23.6 ms                                                      | 25.1 ms: 1.07x slower                                             |
| async_tree_none_tg        | 336 ms                                                       | 366 ms: 1.09x slower                                              |
| async_tree_memoization_tg | 414 ms                                                       | 460 ms: 1.11x slower                                              |
| async_tree_none           | 354 ms                                                       | 399 ms: 1.13x slower                                              |
| async_generators          | 377 ms                                                       | 469 ms: 1.24x slower                                              |
| Geometric mean            | (ref)                                                        | 1.05x slower                                                      |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed_tg, async_tree_io, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                              |
| nbody          | 85.1 ms                                                      | 134 ms: 1.57x slower                                              |
| float          | 77.5 ms                                                      | 142 ms: 1.83x slower                                              |
| Geometric mean | (ref)                                                        | 1.35x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                             |
| regex_dna      | 180 ms                                                       | 176 ms: 1.03x faster                                              |
| regex_v8       | 22.7 ms                                                      | 24.1 ms: 1.06x slower                                             |
| regex_compile  | 132 ms                                                       | 185 ms: 1.40x slower                                              |
| Geometric mean | (ref)                                                        | 1.06x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                              |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.5 ms: 1.04x faster                                             |
| json_loads           | 27.0 us                                                      | 28.6 us: 1.06x slower                                             |
| xml_etree_generate   | 85.4 ms                                                      | 99.5 ms: 1.16x slower                                             |
| xml_etree_process    | 59.3 ms                                                      | 78.8 ms: 1.33x slower                                             |
| tomli_loads          | 2.01 sec                                                     | 2.72 sec: 1.36x slower                                            |
| json_dumps           | 10.5 ms                                                      | 14.3 ms: 1.36x slower                                             |
| unpickle_pure_python | 210 us                                                       | 339 us: 1.61x slower                                              |
| pickle_pure_python   | 294 us                                                       | 520 us: 1.76x slower                                              |
| Geometric mean       | (ref)                                                        | 1.26x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.39x slower                                             |
| python_startup         | 11.0 ms                                                      | 17.4 ms: 1.58x slower                                             |
| Geometric mean         | (ref)                                                        | 1.48x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 66.0 ms: 1.35x slower                                             |
| genshi_text     | 21.5 ms                                                      | 32.3 ms: 1.50x slower                                             |
| django_template | 34.1 ms                                                      | 51.5 ms: 1.51x slower                                             |
| mako            | 11.3 ms                                                      | 18.2 ms: 1.60x slower                                             |
| Geometric mean  | (ref)                                                        | 1.49x slower                                                      |

All benchmarks:
===============

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|---------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits                  | 217 ms                                                       | 184 ms: 1.18x faster                                              |
| regex_effbot              | 3.08 ms                                                      | 2.73 ms: 1.13x faster                                             |
| async_tree_io_tg          | 913 ms                                                       | 838 ms: 1.09x faster                                              |
| deepcopy                  | 355 us                                                       | 333 us: 1.07x faster                                              |
| xml_etree_parse           | 136 ms                                                       | 131 ms: 1.04x faster                                              |
| xml_etree_iterparse       | 94.9 ms                                                      | 91.5 ms: 1.04x faster                                             |
| regex_dna                 | 180 ms                                                       | 176 ms: 1.03x faster                                              |
| async_tree_cpu_io_mixed   | 666 ms                                                       | 654 ms: 1.02x faster                                              |
| gc_traversal              | 3.14 ms                                                      | 3.17 ms: 1.01x slower                                             |
| json                      | 4.93 ms                                                      | 5.07 ms: 1.03x slower                                             |
| deepcopy_memo             | 39.1 us                                                      | 40.6 us: 1.04x slower                                             |
| async_tree_memoization    | 461 ms                                                       | 482 ms: 1.05x slower                                              |
| sqlite_synth              | 2.21 us                                                      | 2.32 us: 1.05x slower                                             |
| json_loads                | 27.0 us                                                      | 28.6 us: 1.06x slower                                             |
| regex_v8                  | 22.7 ms                                                      | 24.1 ms: 1.06x slower                                             |
| coroutines                | 23.6 ms                                                      | 25.1 ms: 1.07x slower                                             |
| pathlib                   | 19.2 ms                                                      | 20.6 ms: 1.08x slower                                             |
| async_tree_none_tg        | 336 ms                                                       | 366 ms: 1.09x slower                                              |
| spectral_norm             | 111 ms                                                       | 123 ms: 1.10x slower                                              |
| async_tree_memoization_tg | 414 ms                                                       | 460 ms: 1.11x slower                                              |
| telco                     | 7.82 ms                                                      | 8.82 ms: 1.13x slower                                             |
| async_tree_none           | 354 ms                                                       | 399 ms: 1.13x slower                                              |
| bpe_tokeniser             | 4.45 sec                                                     | 5.05 sec: 1.13x slower                                            |
| deepcopy_reduce           | 3.11 us                                                      | 3.56 us: 1.14x slower                                             |
| xml_etree_generate        | 85.4 ms                                                      | 99.5 ms: 1.16x slower                                             |
| scimark_fft               | 349 ms                                                       | 410 ms: 1.17x slower                                              |
| mdp                       | 2.36 sec                                                     | 2.80 sec: 1.19x slower                                            |
| docutils                  | 2.62 sec                                                     | 3.11 sec: 1.19x slower                                            |
| coverage                  | 83.0 ms                                                      | 101 ms: 1.21x slower                                              |
| pylint                    | 317 ms                                                       | 385 ms: 1.22x slower                                              |
| async_generators          | 377 ms                                                       | 469 ms: 1.24x slower                                              |
| scimark_sparse_mat_mult   | 4.71 ms                                                      | 5.93 ms: 1.26x slower                                             |
| nqueens                   | 78.6 ms                                                      | 99.5 ms: 1.27x slower                                             |
| meteor_contest            | 102 ms                                                       | 131 ms: 1.29x slower                                              |
| dulwich_log               | 74.8 ms                                                      | 97.6 ms: 1.30x slower                                             |
| xml_etree_process         | 59.3 ms                                                      | 78.8 ms: 1.33x slower                                             |
| sqlglot_optimize          | 52.7 ms                                                      | 70.6 ms: 1.34x slower                                             |
| sqlglot_normalize         | 106 ms                                                       | 142 ms: 1.34x slower                                              |
| typing_runtime_protocols  | 155 us                                                       | 208 us: 1.35x slower                                              |
| genshi_xml                | 48.8 ms                                                      | 66.0 ms: 1.35x slower                                             |
| create_gc_cycles          | 1.34 ms                                                      | 1.81 ms: 1.36x slower                                             |
| tomli_loads               | 2.01 sec                                                     | 2.72 sec: 1.36x slower                                            |
| json_dumps                | 10.5 ms                                                      | 14.3 ms: 1.36x slower                                             |
| pprint_safe_repr          | 738 ms                                                       | 1.01 sec: 1.37x slower                                            |
| generators                | 28.8 ms                                                      | 39.8 ms: 1.38x slower                                             |
| python_startup_no_site    | 7.39 ms                                                      | 10.2 ms: 1.39x slower                                             |
| crypto_pyaes              | 67.9 ms                                                      | 94.3 ms: 1.39x slower                                             |
| fannkuch                  | 370 ms                                                       | 514 ms: 1.39x slower                                              |
| pprint_pformat            | 1.50 sec                                                     | 2.08 sec: 1.39x slower                                            |
| regex_compile             | 132 ms                                                       | 185 ms: 1.40x slower                                              |
| pycparser                 | 1.12 sec                                                     | 1.58 sec: 1.41x slower                                            |
| 2to3                      | 260 ms                                                       | 372 ms: 1.43x slower                                              |
| html5lib                  | 67.0 ms                                                      | 98.0 ms: 1.46x slower                                             |
| thrift                    | 778 us                                                       | 1.16 ms: 1.50x slower                                             |
| sympy_integrate           | 19.8 ms                                                      | 29.7 ms: 1.50x slower                                             |
| genshi_text               | 21.5 ms                                                      | 32.3 ms: 1.50x slower                                             |
| django_template           | 34.1 ms                                                      | 51.5 ms: 1.51x slower                                             |
| pyflate                   | 449 ms                                                       | 693 ms: 1.55x slower                                              |
| nbody                     | 85.1 ms                                                      | 134 ms: 1.57x slower                                              |
| python_startup            | 11.0 ms                                                      | 17.4 ms: 1.58x slower                                             |
| mako                      | 11.3 ms                                                      | 18.2 ms: 1.60x slower                                             |
| unpickle_pure_python      | 210 us                                                       | 339 us: 1.61x slower                                              |
| scimark_lu                | 113 ms                                                       | 184 ms: 1.63x slower                                              |
| hexiom                    | 5.99 ms                                                      | 10.1 ms: 1.69x slower                                             |
| comprehensions            | 16.5 us                                                      | 27.9 us: 1.70x slower                                             |
| richards_super            | 51.6 ms                                                      | 89.0 ms: 1.72x slower                                             |
| richards                  | 45.2 ms                                                      | 79.0 ms: 1.75x slower                                             |
| sympy_str                 | 275 ms                                                       | 482 ms: 1.75x slower                                              |
| pickle_pure_python        | 294 us                                                       | 520 us: 1.76x slower                                              |
| scimark_sor               | 134 ms                                                       | 237 ms: 1.77x slower                                              |
| logging_format            | 6.84 us                                                      | 12.2 us: 1.78x slower                                             |
| logging_simple            | 6.16 us                                                      | 11.0 us: 1.79x slower                                             |
| logging_silent            | 103 ns                                                       | 187 ns: 1.82x slower                                              |
| float                     | 77.5 ms                                                      | 142 ms: 1.83x slower                                              |
| scimark_monte_carlo       | 65.4 ms                                                      | 121 ms: 1.84x slower                                              |
| chaos                     | 57.3 ms                                                      | 106 ms: 1.85x slower                                              |
| sqlglot_transpile         | 1.56 ms                                                      | 3.00 ms: 1.92x slower                                             |
| go                        | 141 ms                                                       | 274 ms: 1.95x slower                                              |
| sqlglot_parse             | 1.25 ms                                                      | 2.60 ms: 2.08x slower                                             |
| sympy_expand              | 457 ms                                                       | 963 ms: 2.11x slower                                              |
| raytrace                  | 253 ms                                                       | 555 ms: 2.20x slower                                              |
| sympy_sum                 | 156 ms                                                       | 352 ms: 2.26x slower                                              |
| deltablue                 | 3.12 ms                                                      | 8.21 ms: 2.63x slower                                             |
| bench_thread_pool         | 919 us                                                       | 3.44 ms: 3.74x slower                                             |
| bench_mp_pool             | 11.0 ms                                                      | 109 ms: 9.91x slower                                              |
| Geometric mean            | (ref)                                                        | 1.40x slower                                                      |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed_tg, async_tree_io, asyncio_websockets
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241209-3.14.0a2+-bba99b4-NOGIL/bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.259x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.25x
- 95% likely to have a slowdown of 1.24x
- 99% likely to have a slowdown of 1.19x

# Memory
- memory change: 1.31x