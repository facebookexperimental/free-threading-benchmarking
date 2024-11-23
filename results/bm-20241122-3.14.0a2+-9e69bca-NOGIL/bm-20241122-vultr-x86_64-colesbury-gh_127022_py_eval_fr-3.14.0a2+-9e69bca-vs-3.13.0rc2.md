# Results vs. 3.13.0rc2

- fork: colesbury
- ref: gh_127022_py_eval_fr
- machine: linux-x86_64
- commit hash: 9e69bca
- commit date: 2024-11-22
- overall geometric mean: 1.45x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-colesbury-gh_127022_py_eval_fr-3.14.0a2+-9e69bca |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 380 ms: 1.47x slower                                                      |
| docutils       | 2.62 sec                                                     | 3.23 sec: 1.23x slower                                                    |
| html5lib       | 67.0 ms                                                      | 103 ms: 1.53x slower                                                      |
| Geometric mean | (ref)                                                        | 1.40x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-colesbury-gh_127022_py_eval_fr-3.14.0a2+-9e69bca |
|---------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg          | 913 ms                                                       | 865 ms: 1.06x faster                                                      |
| async_tree_cpu_io_mixed   | 666 ms                                                       | 653 ms: 1.02x faster                                                      |
| async_tree_memoization    | 461 ms                                                       | 491 ms: 1.07x slower                                                      |
| async_tree_none_tg        | 336 ms                                                       | 369 ms: 1.10x slower                                                      |
| async_tree_memoization_tg | 414 ms                                                       | 466 ms: 1.12x slower                                                      |
| async_tree_none           | 354 ms                                                       | 401 ms: 1.13x slower                                                      |
| coroutines                | 23.6 ms                                                      | 28.0 ms: 1.19x slower                                                     |
| async_generators          | 377 ms                                                       | 476 ms: 1.26x slower                                                      |
| Geometric mean            | (ref)                                                        | 1.07x slower                                                              |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed_tg, asyncio_websockets, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-colesbury-gh_127022_py_eval_fr-3.14.0a2+-9e69bca |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 185 ms: 1.17x faster                                                      |
| float          | 77.5 ms                                                      | 144 ms: 1.86x slower                                                      |
| nbody          | 85.1 ms                                                      | 160 ms: 1.88x slower                                                      |
| Geometric mean | (ref)                                                        | 1.44x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-colesbury-gh_127022_py_eval_fr-3.14.0a2+-9e69bca |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.71 ms: 1.14x faster                                                     |
| regex_dna      | 180 ms                                                       | 182 ms: 1.01x slower                                                      |
| regex_v8       | 22.7 ms                                                      | 24.5 ms: 1.08x slower                                                     |
| regex_compile  | 132 ms                                                       | 195 ms: 1.48x slower                                                      |
| Geometric mean | (ref)                                                        | 1.09x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-colesbury-gh_127022_py_eval_fr-3.14.0a2+-9e69bca |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                      |
| json_loads           | 27.0 us                                                      | 27.9 us: 1.03x slower                                                     |
| xml_etree_generate   | 85.4 ms                                                      | 102 ms: 1.19x slower                                                      |
| json_dumps           | 10.5 ms                                                      | 14.5 ms: 1.38x slower                                                     |
| xml_etree_process    | 59.3 ms                                                      | 82.2 ms: 1.38x slower                                                     |
| tomli_loads          | 2.01 sec                                                     | 2.95 sec: 1.47x slower                                                    |
| unpickle_pure_python | 210 us                                                       | 378 us: 1.80x slower                                                      |
| pickle_pure_python   | 294 us                                                       | 562 us: 1.91x slower                                                      |
| Geometric mean       | (ref)                                                        | 1.31x slower                                                              |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-colesbury-gh_127022_py_eval_fr-3.14.0a2+-9e69bca |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.40x slower                                                     |
| python_startup         | 11.0 ms                                                      | 17.6 ms: 1.60x slower                                                     |
| Geometric mean         | (ref)                                                        | 1.50x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-colesbury-gh_127022_py_eval_fr-3.14.0a2+-9e69bca |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 67.0 ms: 1.37x slower                                                     |
| genshi_text     | 21.5 ms                                                      | 34.0 ms: 1.58x slower                                                     |
| django_template | 34.1 ms                                                      | 55.7 ms: 1.63x slower                                                     |
| mako            | 11.3 ms                                                      | 19.7 ms: 1.74x slower                                                     |
| Geometric mean  | (ref)                                                        | 1.58x slower                                                              |

All benchmarks:
===============

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241122-vultr-x86_64-colesbury-gh_127022_py_eval_fr-3.14.0a2+-9e69bca |
|---------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits                  | 217 ms                                                       | 185 ms: 1.17x faster                                                      |
| regex_effbot              | 3.08 ms                                                      | 2.71 ms: 1.14x faster                                                     |
| async_tree_io_tg          | 913 ms                                                       | 865 ms: 1.06x faster                                                      |
| xml_etree_parse           | 136 ms                                                       | 130 ms: 1.05x faster                                                      |
| async_tree_cpu_io_mixed   | 666 ms                                                       | 653 ms: 1.02x faster                                                      |
| regex_dna                 | 180 ms                                                       | 182 ms: 1.01x slower                                                      |
| deepcopy                  | 355 us                                                       | 358 us: 1.01x slower                                                      |
| json                      | 4.93 ms                                                      | 5.05 ms: 1.03x slower                                                     |
| json_loads                | 27.0 us                                                      | 27.9 us: 1.03x slower                                                     |
| sqlite_synth              | 2.21 us                                                      | 2.32 us: 1.05x slower                                                     |
| async_tree_memoization    | 461 ms                                                       | 491 ms: 1.07x slower                                                      |
| pathlib                   | 19.2 ms                                                      | 20.6 ms: 1.07x slower                                                     |
| regex_v8                  | 22.7 ms                                                      | 24.5 ms: 1.08x slower                                                     |
| async_tree_none_tg        | 336 ms                                                       | 369 ms: 1.10x slower                                                      |
| gc_traversal              | 3.14 ms                                                      | 3.52 ms: 1.12x slower                                                     |
| async_tree_memoization_tg | 414 ms                                                       | 466 ms: 1.12x slower                                                      |
| async_tree_none           | 354 ms                                                       | 401 ms: 1.13x slower                                                      |
| telco                     | 7.82 ms                                                      | 8.89 ms: 1.14x slower                                                     |
| scimark_fft               | 349 ms                                                       | 406 ms: 1.16x slower                                                      |
| deepcopy_memo             | 39.1 us                                                      | 45.7 us: 1.17x slower                                                     |
| scimark_sparse_mat_mult   | 4.71 ms                                                      | 5.56 ms: 1.18x slower                                                     |
| coroutines                | 23.6 ms                                                      | 28.0 ms: 1.19x slower                                                     |
| xml_etree_generate        | 85.4 ms                                                      | 102 ms: 1.19x slower                                                      |
| spectral_norm             | 111 ms                                                       | 132 ms: 1.19x slower                                                      |
| deepcopy_reduce           | 3.11 us                                                      | 3.75 us: 1.20x slower                                                     |
| docutils                  | 2.62 sec                                                     | 3.23 sec: 1.23x slower                                                    |
| coverage                  | 83.0 ms                                                      | 103 ms: 1.24x slower                                                      |
| mdp                       | 2.36 sec                                                     | 2.94 sec: 1.25x slower                                                    |
| pylint                    | 317 ms                                                       | 398 ms: 1.25x slower                                                      |
| async_generators          | 377 ms                                                       | 476 ms: 1.26x slower                                                      |
| bpe_tokeniser             | 4.45 sec                                                     | 5.62 sec: 1.27x slower                                                    |
| dulwich_log               | 74.8 ms                                                      | 98.8 ms: 1.32x slower                                                     |
| meteor_contest            | 102 ms                                                       | 136 ms: 1.34x slower                                                      |
| typing_runtime_protocols  | 155 us                                                       | 212 us: 1.37x slower                                                      |
| genshi_xml                | 48.8 ms                                                      | 67.0 ms: 1.37x slower                                                     |
| json_dumps                | 10.5 ms                                                      | 14.5 ms: 1.38x slower                                                     |
| xml_etree_process         | 59.3 ms                                                      | 82.2 ms: 1.38x slower                                                     |
| create_gc_cycles          | 1.34 ms                                                      | 1.86 ms: 1.39x slower                                                     |
| python_startup_no_site    | 7.39 ms                                                      | 10.3 ms: 1.40x slower                                                     |
| nqueens                   | 78.6 ms                                                      | 110 ms: 1.40x slower                                                      |
| generators                | 28.8 ms                                                      | 40.6 ms: 1.41x slower                                                     |
| sqlglot_normalize         | 106 ms                                                       | 150 ms: 1.42x slower                                                      |
| sqlglot_optimize          | 52.7 ms                                                      | 75.6 ms: 1.43x slower                                                     |
| pycparser                 | 1.12 sec                                                     | 1.61 sec: 1.44x slower                                                    |
| pprint_safe_repr          | 738 ms                                                       | 1.08 sec: 1.46x slower                                                    |
| 2to3                      | 260 ms                                                       | 380 ms: 1.47x slower                                                      |
| fannkuch                  | 370 ms                                                       | 543 ms: 1.47x slower                                                      |
| tomli_loads               | 2.01 sec                                                     | 2.95 sec: 1.47x slower                                                    |
| regex_compile             | 132 ms                                                       | 195 ms: 1.48x slower                                                      |
| pprint_pformat            | 1.50 sec                                                     | 2.23 sec: 1.49x slower                                                    |
| crypto_pyaes              | 67.9 ms                                                      | 103 ms: 1.52x slower                                                      |
| html5lib                  | 67.0 ms                                                      | 103 ms: 1.53x slower                                                      |
| thrift                    | 778 us                                                       | 1.21 ms: 1.56x slower                                                     |
| genshi_text               | 21.5 ms                                                      | 34.0 ms: 1.58x slower                                                     |
| sympy_integrate           | 19.8 ms                                                      | 31.4 ms: 1.59x slower                                                     |
| python_startup            | 11.0 ms                                                      | 17.6 ms: 1.60x slower                                                     |
| django_template           | 34.1 ms                                                      | 55.7 ms: 1.63x slower                                                     |
| pyflate                   | 449 ms                                                       | 750 ms: 1.67x slower                                                      |
| mako                      | 11.3 ms                                                      | 19.7 ms: 1.74x slower                                                     |
| scimark_lu                | 113 ms                                                       | 196 ms: 1.74x slower                                                      |
| comprehensions            | 16.5 us                                                      | 29.0 us: 1.76x slower                                                     |
| logging_format            | 6.84 us                                                      | 12.1 us: 1.77x slower                                                     |
| scimark_sor               | 134 ms                                                       | 241 ms: 1.79x slower                                                      |
| logging_simple            | 6.16 us                                                      | 11.1 us: 1.80x slower                                                     |
| unpickle_pure_python      | 210 us                                                       | 378 us: 1.80x slower                                                      |
| sympy_str                 | 275 ms                                                       | 496 ms: 1.80x slower                                                      |
| float                     | 77.5 ms                                                      | 144 ms: 1.86x slower                                                      |
| scimark_monte_carlo       | 65.4 ms                                                      | 122 ms: 1.87x slower                                                      |
| richards                  | 45.2 ms                                                      | 84.5 ms: 1.87x slower                                                     |
| nbody                     | 85.1 ms                                                      | 160 ms: 1.88x slower                                                      |
| logging_silent            | 103 ns                                                       | 194 ns: 1.89x slower                                                      |
| pickle_pure_python        | 294 us                                                       | 562 us: 1.91x slower                                                      |
| hexiom                    | 5.99 ms                                                      | 11.5 ms: 1.91x slower                                                     |
| richards_super            | 51.6 ms                                                      | 99.9 ms: 1.93x slower                                                     |
| sqlglot_transpile         | 1.56 ms                                                      | 3.08 ms: 1.97x slower                                                     |
| chaos                     | 57.3 ms                                                      | 115 ms: 2.00x slower                                                      |
| go                        | 141 ms                                                       | 287 ms: 2.04x slower                                                      |
| sqlglot_parse             | 1.25 ms                                                      | 2.67 ms: 2.14x slower                                                     |
| sympy_expand              | 457 ms                                                       | 986 ms: 2.16x slower                                                      |
| sympy_sum                 | 156 ms                                                       | 358 ms: 2.30x slower                                                      |
| raytrace                  | 253 ms                                                       | 608 ms: 2.41x slower                                                      |
| deltablue                 | 3.12 ms                                                      | 8.80 ms: 2.82x slower                                                     |
| bench_thread_pool         | 919 us                                                       | 3.38 ms: 3.68x slower                                                     |
| bench_mp_pool             | 11.0 ms                                                      | 111 ms: 10.07x slower                                                     |
| Geometric mean            | (ref)                                                        | 1.45x slower                                                              |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed_tg, asyncio_websockets, xml_etree_iterparse, async_tree_io
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241122-3.14.0a2+-9e69bca-NOGIL/bm-20241122-vultr-x86_64-colesbury-gh_127022_py_eval_fr-3.14.0a2+-9e69bca.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.30x
- 95% likely to have a slowdown of 1.27x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 1.32x