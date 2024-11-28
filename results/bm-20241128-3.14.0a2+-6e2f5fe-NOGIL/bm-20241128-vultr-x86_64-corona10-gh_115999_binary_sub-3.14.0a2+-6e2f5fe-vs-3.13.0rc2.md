# Results vs. 3.13.0rc2

- fork: corona10
- ref: gh_115999_binary_sub
- machine: linux-x86_64
- commit hash: 6e2f5fe
- commit date: 2024-11-28
- overall geometric mean: 1.283x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.24x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 377 ms: 1.45x slower                                                     |
| docutils       | 2.62 sec                                                     | 3.19 sec: 1.22x slower                                                   |
| html5lib       | 67.0 ms                                                      | 101 ms: 1.50x slower                                                     |
| Geometric mean | (ref)                                                        | 1.39x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|---------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg          | 913 ms                                                       | 864 ms: 1.06x faster                                                     |
| async_tree_cpu_io_mixed   | 666 ms                                                       | 657 ms: 1.01x faster                                                     |
| async_tree_io             | 876 ms                                                       | 893 ms: 1.02x slower                                                     |
| async_tree_memoization    | 461 ms                                                       | 491 ms: 1.06x slower                                                     |
| async_tree_none_tg        | 336 ms                                                       | 367 ms: 1.09x slower                                                     |
| async_tree_memoization_tg | 414 ms                                                       | 461 ms: 1.11x slower                                                     |
| async_tree_none           | 354 ms                                                       | 400 ms: 1.13x slower                                                     |
| coroutines                | 23.6 ms                                                      | 28.2 ms: 1.20x slower                                                    |
| async_generators          | 377 ms                                                       | 469 ms: 1.24x slower                                                     |
| Geometric mean            | (ref)                                                        | 1.07x slower                                                             |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.19x faster                                                     |
| nbody          | 85.1 ms                                                      | 139 ms: 1.63x slower                                                     |
| float          | 77.5 ms                                                      | 144 ms: 1.86x slower                                                     |
| Geometric mean | (ref)                                                        | 1.36x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.77 ms: 1.11x faster                                                    |
| regex_dna      | 180 ms                                                       | 187 ms: 1.04x slower                                                     |
| regex_v8       | 22.7 ms                                                      | 24.9 ms: 1.10x slower                                                    |
| regex_compile  | 132 ms                                                       | 194 ms: 1.47x slower                                                     |
| Geometric mean | (ref)                                                        | 1.11x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                     |
| json_loads           | 27.0 us                                                      | 27.9 us: 1.03x slower                                                    |
| xml_etree_generate   | 85.4 ms                                                      | 102 ms: 1.20x slower                                                     |
| json_dumps           | 10.5 ms                                                      | 14.4 ms: 1.37x slower                                                    |
| tomli_loads          | 2.01 sec                                                     | 2.75 sec: 1.37x slower                                                   |
| xml_etree_process    | 59.3 ms                                                      | 82.6 ms: 1.39x slower                                                    |
| unpickle_pure_python | 210 us                                                       | 378 us: 1.80x slower                                                     |
| pickle_pure_python   | 294 us                                                       | 549 us: 1.86x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.30x slower                                                             |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                    |
| python_startup         | 11.0 ms                                                      | 17.5 ms: 1.59x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.49x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 67.2 ms: 1.38x slower                                                    |
| genshi_text     | 21.5 ms                                                      | 33.6 ms: 1.56x slower                                                    |
| django_template | 34.1 ms                                                      | 55.7 ms: 1.63x slower                                                    |
| mako            | 11.3 ms                                                      | 19.8 ms: 1.74x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.57x slower                                                             |

All benchmarks:
===============

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe |
|---------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits                  | 217 ms                                                       | 181 ms: 1.19x faster                                                     |
| regex_effbot              | 3.08 ms                                                      | 2.77 ms: 1.11x faster                                                    |
| async_tree_io_tg          | 913 ms                                                       | 864 ms: 1.06x faster                                                     |
| xml_etree_parse           | 136 ms                                                       | 131 ms: 1.04x faster                                                     |
| async_tree_cpu_io_mixed   | 666 ms                                                       | 657 ms: 1.01x faster                                                     |
| async_tree_io             | 876 ms                                                       | 893 ms: 1.02x slower                                                     |
| json                      | 4.93 ms                                                      | 5.07 ms: 1.03x slower                                                    |
| json_loads                | 27.0 us                                                      | 27.9 us: 1.03x slower                                                    |
| regex_dna                 | 180 ms                                                       | 187 ms: 1.04x slower                                                     |
| sqlite_synth              | 2.21 us                                                      | 2.30 us: 1.04x slower                                                    |
| gc_traversal              | 3.14 ms                                                      | 3.29 ms: 1.05x slower                                                    |
| async_tree_memoization    | 461 ms                                                       | 491 ms: 1.06x slower                                                     |
| pathlib                   | 19.2 ms                                                      | 20.8 ms: 1.09x slower                                                    |
| async_tree_none_tg        | 336 ms                                                       | 367 ms: 1.09x slower                                                     |
| regex_v8                  | 22.7 ms                                                      | 24.9 ms: 1.10x slower                                                    |
| async_tree_memoization_tg | 414 ms                                                       | 461 ms: 1.11x slower                                                     |
| async_tree_none           | 354 ms                                                       | 400 ms: 1.13x slower                                                     |
| telco                     | 7.82 ms                                                      | 8.95 ms: 1.14x slower                                                    |
| scimark_fft               | 349 ms                                                       | 402 ms: 1.15x slower                                                     |
| deepcopy_memo             | 39.1 us                                                      | 45.9 us: 1.18x slower                                                    |
| coroutines                | 23.6 ms                                                      | 28.2 ms: 1.20x slower                                                    |
| xml_etree_generate        | 85.4 ms                                                      | 102 ms: 1.20x slower                                                     |
| deepcopy_reduce           | 3.11 us                                                      | 3.76 us: 1.21x slower                                                    |
| spectral_norm             | 111 ms                                                       | 135 ms: 1.22x slower                                                     |
| docutils                  | 2.62 sec                                                     | 3.19 sec: 1.22x slower                                                   |
| mdp                       | 2.36 sec                                                     | 2.91 sec: 1.23x slower                                                   |
| coverage                  | 83.0 ms                                                      | 102 ms: 1.23x slower                                                     |
| pylint                    | 317 ms                                                       | 394 ms: 1.24x slower                                                     |
| async_generators          | 377 ms                                                       | 469 ms: 1.24x slower                                                     |
| bpe_tokeniser             | 4.45 sec                                                     | 5.55 sec: 1.25x slower                                                   |
| scimark_sparse_mat_mult   | 4.71 ms                                                      | 5.99 ms: 1.27x slower                                                    |
| nqueens                   | 78.6 ms                                                      | 103 ms: 1.31x slower                                                     |
| dulwich_log               | 74.8 ms                                                      | 99.8 ms: 1.33x slower                                                    |
| meteor_contest            | 102 ms                                                       | 136 ms: 1.34x slower                                                     |
| create_gc_cycles          | 1.34 ms                                                      | 1.82 ms: 1.36x slower                                                    |
| generators                | 28.8 ms                                                      | 39.4 ms: 1.37x slower                                                    |
| json_dumps                | 10.5 ms                                                      | 14.4 ms: 1.37x slower                                                    |
| tomli_loads               | 2.01 sec                                                     | 2.75 sec: 1.37x slower                                                   |
| genshi_xml                | 48.8 ms                                                      | 67.2 ms: 1.38x slower                                                    |
| python_startup_no_site    | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                    |
| xml_etree_process         | 59.3 ms                                                      | 82.6 ms: 1.39x slower                                                    |
| typing_runtime_protocols  | 155 us                                                       | 217 us: 1.40x slower                                                     |
| fannkuch                  | 370 ms                                                       | 521 ms: 1.41x slower                                                     |
| sqlglot_optimize          | 52.7 ms                                                      | 75.0 ms: 1.42x slower                                                    |
| sqlglot_normalize         | 106 ms                                                       | 150 ms: 1.42x slower                                                     |
| pycparser                 | 1.12 sec                                                     | 1.60 sec: 1.43x slower                                                   |
| 2to3                      | 260 ms                                                       | 377 ms: 1.45x slower                                                     |
| crypto_pyaes              | 67.9 ms                                                      | 98.6 ms: 1.45x slower                                                    |
| pprint_safe_repr          | 738 ms                                                       | 1.07 sec: 1.45x slower                                                   |
| regex_compile             | 132 ms                                                       | 194 ms: 1.47x slower                                                     |
| pprint_pformat            | 1.50 sec                                                     | 2.22 sec: 1.48x slower                                                   |
| html5lib                  | 67.0 ms                                                      | 101 ms: 1.50x slower                                                     |
| thrift                    | 778 us                                                       | 1.20 ms: 1.54x slower                                                    |
| sympy_integrate           | 19.8 ms                                                      | 30.9 ms: 1.56x slower                                                    |
| genshi_text               | 21.5 ms                                                      | 33.6 ms: 1.56x slower                                                    |
| python_startup            | 11.0 ms                                                      | 17.5 ms: 1.59x slower                                                    |
| django_template           | 34.1 ms                                                      | 55.7 ms: 1.63x slower                                                    |
| nbody                     | 85.1 ms                                                      | 139 ms: 1.63x slower                                                     |
| pyflate                   | 449 ms                                                       | 741 ms: 1.65x slower                                                     |
| scimark_lu                | 113 ms                                                       | 195 ms: 1.73x slower                                                     |
| mako                      | 11.3 ms                                                      | 19.8 ms: 1.74x slower                                                    |
| comprehensions            | 16.5 us                                                      | 29.2 us: 1.78x slower                                                    |
| scimark_sor               | 134 ms                                                       | 242 ms: 1.80x slower                                                     |
| unpickle_pure_python      | 210 us                                                       | 378 us: 1.80x slower                                                     |
| sympy_str                 | 275 ms                                                       | 495 ms: 1.80x slower                                                     |
| hexiom                    | 5.99 ms                                                      | 11.0 ms: 1.84x slower                                                    |
| logging_format            | 6.84 us                                                      | 12.6 us: 1.84x slower                                                    |
| richards                  | 45.2 ms                                                      | 83.6 ms: 1.85x slower                                                    |
| logging_simple            | 6.16 us                                                      | 11.4 us: 1.85x slower                                                    |
| scimark_monte_carlo       | 65.4 ms                                                      | 121 ms: 1.86x slower                                                     |
| float                     | 77.5 ms                                                      | 144 ms: 1.86x slower                                                     |
| pickle_pure_python        | 294 us                                                       | 549 us: 1.86x slower                                                     |
| richards_super            | 51.6 ms                                                      | 99.7 ms: 1.93x slower                                                    |
| logging_silent            | 103 ns                                                       | 200 ns: 1.95x slower                                                     |
| chaos                     | 57.3 ms                                                      | 112 ms: 1.95x slower                                                     |
| sqlglot_transpile         | 1.56 ms                                                      | 3.04 ms: 1.95x slower                                                    |
| go                        | 141 ms                                                       | 281 ms: 1.99x slower                                                     |
| sympy_expand              | 457 ms                                                       | 982 ms: 2.15x slower                                                     |
| sqlglot_parse             | 1.25 ms                                                      | 2.69 ms: 2.15x slower                                                    |
| sympy_sum                 | 156 ms                                                       | 357 ms: 2.30x slower                                                     |
| raytrace                  | 253 ms                                                       | 599 ms: 2.37x slower                                                     |
| deltablue                 | 3.12 ms                                                      | 8.80 ms: 2.82x slower                                                    |
| bench_thread_pool         | 919 us                                                       | 3.38 ms: 3.68x slower                                                    |
| bench_mp_pool             | 11.0 ms                                                      | 110 ms: 9.97x slower                                                     |
| Geometric mean            | (ref)                                                        | 1.45x slower                                                             |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed_tg, asyncio_websockets, xml_etree_iterparse, deepcopy
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241128-3.14.0a2+-6e2f5fe-NOGIL/bm-20241128-vultr-x86_64-corona10-gh_115999_binary_sub-3.14.0a2+-6e2f5fe.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.283x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.29x
- 95% likely to have a slowdown of 1.26x
- 99% likely to have a slowdown of 1.24x

# Memory
- memory change: 1.31x