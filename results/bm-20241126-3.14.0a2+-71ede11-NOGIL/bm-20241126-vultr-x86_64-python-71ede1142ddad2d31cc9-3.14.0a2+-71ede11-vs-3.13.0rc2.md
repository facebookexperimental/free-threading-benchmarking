# Results vs. 3.13.0rc2

- fork: python
- ref: 71ede1142ddad2d31cc9
- machine: linux-x86_64
- commit hash: 71ede11
- commit date: 2024-11-26
- overall geometric mean: 1.287x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.24x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 380 ms: 1.46x slower                                                   |
| docutils       | 2.62 sec                                                     | 3.19 sec: 1.22x slower                                                 |
| html5lib       | 67.0 ms                                                      | 100 ms: 1.50x slower                                                   |
| Geometric mean | (ref)                                                        | 1.39x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|---------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg          | 913 ms                                                       | 877 ms: 1.04x faster                                                   |
| async_tree_io             | 876 ms                                                       | 905 ms: 1.03x slower                                                   |
| async_tree_memoization    | 461 ms                                                       | 496 ms: 1.08x slower                                                   |
| async_tree_none_tg        | 336 ms                                                       | 372 ms: 1.10x slower                                                   |
| async_tree_memoization_tg | 414 ms                                                       | 469 ms: 1.13x slower                                                   |
| async_tree_none           | 354 ms                                                       | 406 ms: 1.15x slower                                                   |
| coroutines                | 23.6 ms                                                      | 28.0 ms: 1.19x slower                                                  |
| async_generators          | 377 ms                                                       | 468 ms: 1.24x slower                                                   |
| Geometric mean            | (ref)                                                        | 1.08x slower                                                           |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                   |
| nbody          | 85.1 ms                                                      | 141 ms: 1.66x slower                                                   |
| float          | 77.5 ms                                                      | 144 ms: 1.86x slower                                                   |
| Geometric mean | (ref)                                                        | 1.38x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.84 ms: 1.09x faster                                                  |
| regex_dna      | 180 ms                                                       | 184 ms: 1.02x slower                                                   |
| regex_v8       | 22.7 ms                                                      | 24.6 ms: 1.09x slower                                                  |
| regex_compile  | 132 ms                                                       | 195 ms: 1.47x slower                                                   |
| Geometric mean | (ref)                                                        | 1.11x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| json_loads           | 27.0 us                                                      | 28.2 us: 1.04x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 102 ms: 1.20x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 14.5 ms: 1.38x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 82.8 ms: 1.40x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.92 sec: 1.46x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 376 us: 1.79x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 554 us: 1.88x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.31x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                  |
| python_startup         | 11.0 ms                                                      | 17.5 ms: 1.59x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.49x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 68.1 ms: 1.40x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 34.4 ms: 1.60x slower                                                  |
| django_template | 34.1 ms                                                      | 55.7 ms: 1.63x slower                                                  |
| mako            | 11.3 ms                                                      | 19.6 ms: 1.73x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.58x slower                                                           |

All benchmarks:
===============

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11 |
|---------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits                  | 217 ms                                                       | 184 ms: 1.18x faster                                                   |
| regex_effbot              | 3.08 ms                                                      | 2.84 ms: 1.09x faster                                                  |
| async_tree_io_tg          | 913 ms                                                       | 877 ms: 1.04x faster                                                   |
| xml_etree_parse           | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| deepcopy                  | 355 us                                                       | 358 us: 1.01x slower                                                   |
| regex_dna                 | 180 ms                                                       | 184 ms: 1.02x slower                                                   |
| async_tree_io             | 876 ms                                                       | 905 ms: 1.03x slower                                                   |
| json_loads                | 27.0 us                                                      | 28.2 us: 1.04x slower                                                  |
| json                      | 4.93 ms                                                      | 5.15 ms: 1.05x slower                                                  |
| sqlite_synth              | 2.21 us                                                      | 2.31 us: 1.05x slower                                                  |
| gc_traversal              | 3.14 ms                                                      | 3.30 ms: 1.05x slower                                                  |
| async_tree_memoization    | 461 ms                                                       | 496 ms: 1.08x slower                                                   |
| pathlib                   | 19.2 ms                                                      | 20.7 ms: 1.08x slower                                                  |
| regex_v8                  | 22.7 ms                                                      | 24.6 ms: 1.09x slower                                                  |
| async_tree_none_tg        | 336 ms                                                       | 372 ms: 1.10x slower                                                   |
| async_tree_memoization_tg | 414 ms                                                       | 469 ms: 1.13x slower                                                   |
| async_tree_none           | 354 ms                                                       | 406 ms: 1.15x slower                                                   |
| telco                     | 7.82 ms                                                      | 9.00 ms: 1.15x slower                                                  |
| scimark_fft               | 349 ms                                                       | 402 ms: 1.15x slower                                                   |
| deepcopy_memo             | 39.1 us                                                      | 45.4 us: 1.16x slower                                                  |
| coroutines                | 23.6 ms                                                      | 28.0 ms: 1.19x slower                                                  |
| spectral_norm             | 111 ms                                                       | 133 ms: 1.20x slower                                                   |
| xml_etree_generate        | 85.4 ms                                                      | 102 ms: 1.20x slower                                                   |
| docutils                  | 2.62 sec                                                     | 3.19 sec: 1.22x slower                                                 |
| deepcopy_reduce           | 3.11 us                                                      | 3.80 us: 1.22x slower                                                  |
| scimark_sparse_mat_mult   | 4.71 ms                                                      | 5.76 ms: 1.22x slower                                                  |
| mdp                       | 2.36 sec                                                     | 2.89 sec: 1.23x slower                                                 |
| coverage                  | 83.0 ms                                                      | 102 ms: 1.23x slower                                                   |
| async_generators          | 377 ms                                                       | 468 ms: 1.24x slower                                                   |
| pylint                    | 317 ms                                                       | 396 ms: 1.25x slower                                                   |
| bpe_tokeniser             | 4.45 sec                                                     | 5.58 sec: 1.25x slower                                                 |
| dulwich_log               | 74.8 ms                                                      | 99.5 ms: 1.33x slower                                                  |
| meteor_contest            | 102 ms                                                       | 136 ms: 1.34x slower                                                   |
| create_gc_cycles          | 1.34 ms                                                      | 1.82 ms: 1.36x slower                                                  |
| generators                | 28.8 ms                                                      | 39.3 ms: 1.37x slower                                                  |
| typing_runtime_protocols  | 155 us                                                       | 211 us: 1.37x slower                                                   |
| nqueens                   | 78.6 ms                                                      | 108 ms: 1.37x slower                                                   |
| json_dumps                | 10.5 ms                                                      | 14.5 ms: 1.38x slower                                                  |
| python_startup_no_site    | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                  |
| xml_etree_process         | 59.3 ms                                                      | 82.8 ms: 1.40x slower                                                  |
| genshi_xml                | 48.8 ms                                                      | 68.1 ms: 1.40x slower                                                  |
| pycparser                 | 1.12 sec                                                     | 1.60 sec: 1.43x slower                                                 |
| sqlglot_optimize          | 52.7 ms                                                      | 75.5 ms: 1.43x slower                                                  |
| sqlglot_normalize         | 106 ms                                                       | 151 ms: 1.43x slower                                                   |
| pprint_safe_repr          | 738 ms                                                       | 1.07 sec: 1.45x slower                                                 |
| tomli_loads               | 2.01 sec                                                     | 2.92 sec: 1.46x slower                                                 |
| 2to3                      | 260 ms                                                       | 380 ms: 1.46x slower                                                   |
| fannkuch                  | 370 ms                                                       | 545 ms: 1.47x slower                                                   |
| regex_compile             | 132 ms                                                       | 195 ms: 1.47x slower                                                   |
| pprint_pformat            | 1.50 sec                                                     | 2.23 sec: 1.49x slower                                                 |
| html5lib                  | 67.0 ms                                                      | 100 ms: 1.50x slower                                                   |
| crypto_pyaes              | 67.9 ms                                                      | 103 ms: 1.52x slower                                                   |
| thrift                    | 778 us                                                       | 1.21 ms: 1.55x slower                                                  |
| sympy_integrate           | 19.8 ms                                                      | 31.0 ms: 1.56x slower                                                  |
| python_startup            | 11.0 ms                                                      | 17.5 ms: 1.59x slower                                                  |
| genshi_text               | 21.5 ms                                                      | 34.4 ms: 1.60x slower                                                  |
| django_template           | 34.1 ms                                                      | 55.7 ms: 1.63x slower                                                  |
| pyflate                   | 449 ms                                                       | 737 ms: 1.64x slower                                                   |
| nbody                     | 85.1 ms                                                      | 141 ms: 1.66x slower                                                   |
| mako                      | 11.3 ms                                                      | 19.6 ms: 1.73x slower                                                  |
| comprehensions            | 16.5 us                                                      | 29.1 us: 1.77x slower                                                  |
| scimark_lu                | 113 ms                                                       | 199 ms: 1.77x slower                                                   |
| unpickle_pure_python      | 210 us                                                       | 376 us: 1.79x slower                                                   |
| scimark_sor               | 134 ms                                                       | 243 ms: 1.81x slower                                                   |
| sympy_str                 | 275 ms                                                       | 498 ms: 1.81x slower                                                   |
| logging_simple            | 6.16 us                                                      | 11.4 us: 1.84x slower                                                  |
| logging_format            | 6.84 us                                                      | 12.7 us: 1.85x slower                                                  |
| float                     | 77.5 ms                                                      | 144 ms: 1.86x slower                                                   |
| richards                  | 45.2 ms                                                      | 84.6 ms: 1.87x slower                                                  |
| scimark_monte_carlo       | 65.4 ms                                                      | 122 ms: 1.87x slower                                                   |
| pickle_pure_python        | 294 us                                                       | 554 us: 1.88x slower                                                   |
| hexiom                    | 5.99 ms                                                      | 11.4 ms: 1.90x slower                                                  |
| logging_silent            | 103 ns                                                       | 199 ns: 1.94x slower                                                   |
| richards_super            | 51.6 ms                                                      | 101 ms: 1.95x slower                                                   |
| sqlglot_transpile         | 1.56 ms                                                      | 3.09 ms: 1.98x slower                                                  |
| chaos                     | 57.3 ms                                                      | 116 ms: 2.02x slower                                                   |
| go                        | 141 ms                                                       | 285 ms: 2.02x slower                                                   |
| sqlglot_parse             | 1.25 ms                                                      | 2.68 ms: 2.14x slower                                                  |
| sympy_expand              | 457 ms                                                       | 987 ms: 2.16x slower                                                   |
| sympy_sum                 | 156 ms                                                       | 360 ms: 2.31x slower                                                   |
| raytrace                  | 253 ms                                                       | 608 ms: 2.41x slower                                                   |
| deltablue                 | 3.12 ms                                                      | 8.87 ms: 2.84x slower                                                  |
| bench_thread_pool         | 919 us                                                       | 3.41 ms: 3.71x slower                                                  |
| bench_mp_pool             | 11.0 ms                                                      | 110 ms: 9.99x slower                                                   |
| Geometric mean            | (ref)                                                        | 1.45x slower                                                           |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, asyncio_websockets, xml_etree_iterparse
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241126-3.14.0a2+-71ede11-NOGIL/bm-20241126-vultr-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.287x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.29x
- 95% likely to have a slowdown of 1.27x
- 99% likely to have a slowdown of 1.24x

# Memory
- memory change: 1.31x