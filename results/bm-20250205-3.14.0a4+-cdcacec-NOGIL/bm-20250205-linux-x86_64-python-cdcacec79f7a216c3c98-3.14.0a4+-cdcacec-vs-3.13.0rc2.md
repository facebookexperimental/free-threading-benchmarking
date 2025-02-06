# Results vs. 3.13.0rc2

- fork: python
- ref: cdcacec79f7a216c3c98
- machine: linux-x86_64
- commit hash: cdcacec
- commit date: 2025-02-05
- overall geometric mean: 1.069x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 554 ms: 1.24x slower                                                   |
| Geometric mean | (ref)                                                        | 1.08x slower                                                           |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 825 ms: 1.70x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 854 ms: 1.62x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 343 ms: 1.47x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 457 ms: 1.47x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 514 ms: 1.38x faster                                                   |
| async_tree_none            | 572 ms                                                       | 428 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 654 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 730 ms: 1.22x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.29x faster                                                           |

Benchmark hidden because not significant (3): asyncio_websockets, async_generators, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 107 ms: 1.08x faster                                                   |
| nbody          | 119 ms                                                       | 202 ms: 1.70x slower                                                   |
| Geometric mean | (ref)                                                        | 1.15x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 34.4 ms: 1.05x slower                                                  |
| regex_compile  | 182 ms                                                       | 197 ms: 1.08x slower                                                   |
| regex_dna      | 282 ms                                                       | 312 ms: 1.11x slower                                                   |
| regex_effbot   | 4.74 ms                                                      | 5.30 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                        | 1.09x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 144 ms: 1.23x faster                                                   |
| xml_etree_parse      | 231 ms                                                       | 213 ms: 1.08x faster                                                   |
| xml_etree_generate   | 122 ms                                                       | 130 ms: 1.06x slower                                                   |
| tomli_loads          | 2.78 sec                                                     | 2.99 sec: 1.08x slower                                                 |
| unpickle_pure_python | 290 us                                                       | 327 us: 1.13x slower                                                   |
| xml_etree_process    | 85.9 ms                                                      | 98.1 ms: 1.14x slower                                                  |
| pickle_pure_python   | 416 us                                                       | 491 us: 1.18x slower                                                   |
| json_dumps           | 14.1 ms                                                      | 17.7 ms: 1.25x slower                                                  |
| json_loads           | 34.3 us                                                      | 45.6 us: 1.33x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.09x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 20.0 ms: 1.31x slower                                                  |
| python_startup         | 22.4 ms                                                      | 32.4 ms: 1.45x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 82.6 ms: 1.15x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 36.8 ms: 1.16x slower                                                  |
| django_template | 44.3 ms                                                      | 52.7 ms: 1.19x slower                                                  |
| mako            | 15.9 ms                                                      | 25.2 ms: 1.58x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.26x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 825 ms: 1.70x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 854 ms: 1.62x faster                                                   |
| gc_traversal               | 5.70 ms                                                      | 3.76 ms: 1.52x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 343 ms: 1.47x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 457 ms: 1.47x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 514 ms: 1.38x faster                                                   |
| async_tree_none            | 572 ms                                                       | 428 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 654 ms: 1.30x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 144 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 730 ms: 1.22x faster                                                   |
| deepcopy                   | 498 us                                                       | 439 us: 1.13x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.59 us: 1.11x faster                                                  |
| xml_etree_parse            | 231 ms                                                       | 213 ms: 1.08x faster                                                   |
| float                      | 116 ms                                                       | 107 ms: 1.08x faster                                                   |
| spectral_norm              | 157 ms                                                       | 148 ms: 1.06x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 47.8 us: 1.05x faster                                                  |
| telco                      | 12.2 ms                                                      | 11.7 ms: 1.04x faster                                                  |
| regex_v8                   | 32.8 ms                                                      | 34.4 ms: 1.05x slower                                                  |
| xml_etree_generate         | 122 ms                                                       | 130 ms: 1.06x slower                                                   |
| tomli_loads                | 2.78 sec                                                     | 2.99 sec: 1.08x slower                                                 |
| regex_compile              | 182 ms                                                       | 197 ms: 1.08x slower                                                   |
| sympy_integrate            | 30.2 ms                                                      | 32.9 ms: 1.09x slower                                                  |
| scimark_sor                | 179 ms                                                       | 196 ms: 1.10x slower                                                   |
| logging_silent             | 130 ns                                                       | 143 ns: 1.10x slower                                                   |
| regex_dna                  | 282 ms                                                       | 312 ms: 1.11x slower                                                   |
| richards                   | 65.5 ms                                                      | 72.7 ms: 1.11x slower                                                  |
| mdp                        | 3.80 sec                                                     | 4.23 sec: 1.11x slower                                                 |
| regex_effbot               | 4.74 ms                                                      | 5.30 ms: 1.12x slower                                                  |
| pprint_safe_repr           | 987 ms                                                       | 1.11 sec: 1.13x slower                                                 |
| unpickle_pure_python       | 290 us                                                       | 327 us: 1.13x slower                                                   |
| sqlglot_optimize           | 74.7 ms                                                      | 84.4 ms: 1.13x slower                                                  |
| sqlglot_normalize          | 140 ms                                                       | 158 ms: 1.13x slower                                                   |
| sympy_sum                  | 210 ms                                                       | 238 ms: 1.13x slower                                                   |
| pyflate                    | 664 ms                                                       | 753 ms: 1.13x slower                                                   |
| pprint_pformat             | 1.94 sec                                                     | 2.21 sec: 1.14x slower                                                 |
| xml_etree_process          | 85.9 ms                                                      | 98.1 ms: 1.14x slower                                                  |
| richards_super             | 73.2 ms                                                      | 83.6 ms: 1.14x slower                                                  |
| thrift                     | 1.10 ms                                                      | 1.26 ms: 1.15x slower                                                  |
| genshi_xml                 | 72.1 ms                                                      | 82.6 ms: 1.15x slower                                                  |
| generators                 | 40.0 ms                                                      | 45.9 ms: 1.15x slower                                                  |
| scimark_fft                | 473 ms                                                       | 543 ms: 1.15x slower                                                   |
| fannkuch                   | 547 ms                                                       | 632 ms: 1.16x slower                                                   |
| bpe_tokeniser              | 6.28 sec                                                     | 7.27 sec: 1.16x slower                                                 |
| genshi_text                | 31.7 ms                                                      | 36.8 ms: 1.16x slower                                                  |
| sympy_str                  | 379 ms                                                       | 445 ms: 1.17x slower                                                   |
| pickle_pure_python         | 416 us                                                       | 491 us: 1.18x slower                                                   |
| meteor_contest             | 150 ms                                                       | 178 ms: 1.19x slower                                                   |
| django_template            | 44.3 ms                                                      | 52.7 ms: 1.19x slower                                                  |
| json                       | 6.51 ms                                                      | 7.83 ms: 1.20x slower                                                  |
| logging_format             | 9.24 us                                                      | 11.1 us: 1.20x slower                                                  |
| crypto_pyaes               | 100 ms                                                       | 121 ms: 1.20x slower                                                   |
| sympy_expand               | 601 ms                                                       | 730 ms: 1.22x slower                                                   |
| sqlglot_transpile          | 2.20 ms                                                      | 2.67 ms: 1.22x slower                                                  |
| comprehensions             | 22.2 us                                                      | 27.4 us: 1.23x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 2.97 ms: 1.23x slower                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 8.33 ms: 1.23x slower                                                  |
| 2to3                       | 445 ms                                                       | 554 ms: 1.24x slower                                                   |
| json_dumps                 | 14.1 ms                                                      | 17.7 ms: 1.25x slower                                                  |
| nqueens                    | 112 ms                                                       | 140 ms: 1.25x slower                                                   |
| logging_simple             | 8.56 us                                                      | 10.7 us: 1.25x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 187 ms: 1.28x slower                                                   |
| scimark_monte_carlo        | 90.6 ms                                                      | 116 ms: 1.28x slower                                                   |
| coverage                   | 107 ms                                                       | 139 ms: 1.29x slower                                                   |
| python_startup_no_site     | 15.3 ms                                                      | 20.0 ms: 1.31x slower                                                  |
| typing_runtime_protocols   | 226 us                                                       | 296 us: 1.31x slower                                                   |
| hexiom                     | 8.11 ms                                                      | 10.8 ms: 1.33x slower                                                  |
| sqlglot_parse              | 1.76 ms                                                      | 2.33 ms: 1.33x slower                                                  |
| json_loads                 | 34.3 us                                                      | 45.6 us: 1.33x slower                                                  |
| raytrace                   | 344 ms                                                       | 474 ms: 1.38x slower                                                   |
| deltablue                  | 4.44 ms                                                      | 6.28 ms: 1.42x slower                                                  |
| chaos                      | 83.6 ms                                                      | 120 ms: 1.44x slower                                                   |
| python_startup             | 22.4 ms                                                      | 32.4 ms: 1.45x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 4.32 ms: 1.50x slower                                                  |
| mako                       | 15.9 ms                                                      | 25.2 ms: 1.58x slower                                                  |
| nbody                      | 119 ms                                                       | 202 ms: 1.70x slower                                                   |
| bench_mp_pool              | 18.7 ms                                                      | 87.5 ms: 4.68x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.11x slower                                                           |

Benchmark hidden because not significant (12): pidigits, pylint, asyncio_websockets, async_generators, deepcopy_reduce, docutils, go, html5lib, pycparser, dulwich_log, coroutines, pathlib
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250205-3.14.0a4+-cdcacec-NOGIL/bm-20250205-linux-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.069x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.34x