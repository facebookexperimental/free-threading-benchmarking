# Results vs. 3.13.0rc2

- fork: python
- ref: 7e6ee50b6b8c760bcefb
- machine: linux-x86_64
- commit hash: 7e6ee50
- commit date: 2025-02-10
- overall geometric mean: 1.056x slower
- HPT reliability: 99.93%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 530 ms: 1.19x slower                                                   |
| docutils       | 4.01 sec                                                     | 4.12 sec: 1.03x slower                                                 |
| Geometric mean | (ref)                                                        | 1.07x slower                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 772 ms: 1.82x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 835 ms: 1.66x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 348 ms: 1.45x faster                                                   |
| async_tree_none            | 572 ms                                                       | 418 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 496 ms: 1.35x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 528 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 671 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 734 ms: 1.21x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 742 ms: 1.03x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.29x faster                                                           |

Benchmark hidden because not significant (2): async_generators, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 106 ms: 1.09x faster                                                   |
| pidigits       | 251 ms                                                       | 233 ms: 1.08x faster                                                   |
| nbody          | 119 ms                                                       | 179 ms: 1.51x slower                                                   |
| Geometric mean | (ref)                                                        | 1.09x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.49 ms: 1.05x faster                                                  |
| regex_dna      | 282 ms                                                       | 296 ms: 1.05x slower                                                   |
| regex_compile  | 182 ms                                                       | 196 ms: 1.08x slower                                                   |
| regex_v8       | 32.8 ms                                                      | 36.4 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 137 ms: 1.29x faster                                                   |
| xml_etree_parse      | 231 ms                                                       | 218 ms: 1.06x faster                                                   |
| tomli_loads          | 2.78 sec                                                     | 3.03 sec: 1.09x slower                                                 |
| xml_etree_generate   | 122 ms                                                       | 137 ms: 1.12x slower                                                   |
| unpickle_pure_python | 290 us                                                       | 326 us: 1.12x slower                                                   |
| xml_etree_process    | 85.9 ms                                                      | 99.8 ms: 1.16x slower                                                  |
| json_loads           | 34.3 us                                                      | 40.1 us: 1.17x slower                                                  |
| pickle_pure_python   | 416 us                                                       | 495 us: 1.19x slower                                                   |
| json_dumps           | 14.1 ms                                                      | 17.6 ms: 1.25x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.08x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 19.9 ms: 1.30x slower                                                  |
| python_startup         | 22.4 ms                                                      | 32.4 ms: 1.45x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 79.4 ms: 1.10x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 40.5 ms: 1.28x slower                                                  |
| django_template | 44.3 ms                                                      | 58.4 ms: 1.32x slower                                                  |
| mako            | 15.9 ms                                                      | 24.2 ms: 1.52x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.30x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 772 ms: 1.82x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 835 ms: 1.66x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 348 ms: 1.45x faster                                                   |
| gc_traversal               | 5.70 ms                                                      | 3.97 ms: 1.44x faster                                                  |
| async_tree_none            | 572 ms                                                       | 418 ms: 1.37x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 496 ms: 1.35x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 528 ms: 1.34x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 137 ms: 1.29x faster                                                   |
| deepcopy                   | 498 us                                                       | 388 us: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 671 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 734 ms: 1.21x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.61 us: 1.10x faster                                                  |
| float                      | 116 ms                                                       | 106 ms: 1.09x faster                                                   |
| pidigits                   | 251 ms                                                       | 233 ms: 1.08x faster                                                   |
| xml_etree_parse            | 231 ms                                                       | 218 ms: 1.06x faster                                                   |
| regex_effbot               | 4.74 ms                                                      | 4.49 ms: 1.05x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 742 ms: 1.03x faster                                                   |
| docutils                   | 4.01 sec                                                     | 4.12 sec: 1.03x slower                                                 |
| deepcopy_reduce            | 4.10 us                                                      | 4.22 us: 1.03x slower                                                  |
| regex_dna                  | 282 ms                                                       | 296 ms: 1.05x slower                                                   |
| logging_silent             | 130 ns                                                       | 139 ns: 1.07x slower                                                   |
| regex_compile              | 182 ms                                                       | 196 ms: 1.08x slower                                                   |
| scimark_fft                | 473 ms                                                       | 511 ms: 1.08x slower                                                   |
| tomli_loads                | 2.78 sec                                                     | 3.03 sec: 1.09x slower                                                 |
| sqlglot_normalize          | 140 ms                                                       | 152 ms: 1.09x slower                                                   |
| pyflate                    | 664 ms                                                       | 723 ms: 1.09x slower                                                   |
| sympy_integrate            | 30.2 ms                                                      | 33.0 ms: 1.09x slower                                                  |
| sympy_str                  | 379 ms                                                       | 414 ms: 1.09x slower                                                   |
| genshi_xml                 | 72.1 ms                                                      | 79.4 ms: 1.10x slower                                                  |
| crypto_pyaes               | 100 ms                                                       | 110 ms: 1.10x slower                                                   |
| sqlglot_optimize           | 74.7 ms                                                      | 82.8 ms: 1.11x slower                                                  |
| regex_v8                   | 32.8 ms                                                      | 36.4 ms: 1.11x slower                                                  |
| mdp                        | 3.80 sec                                                     | 4.22 sec: 1.11x slower                                                 |
| thrift                     | 1.10 ms                                                      | 1.22 ms: 1.11x slower                                                  |
| xml_etree_generate         | 122 ms                                                       | 137 ms: 1.12x slower                                                   |
| unpickle_pure_python       | 290 us                                                       | 326 us: 1.12x slower                                                   |
| richards_super             | 73.2 ms                                                      | 82.4 ms: 1.13x slower                                                  |
| meteor_contest             | 150 ms                                                       | 170 ms: 1.13x slower                                                   |
| sympy_sum                  | 210 ms                                                       | 238 ms: 1.13x slower                                                   |
| sympy_expand               | 601 ms                                                       | 681 ms: 1.13x slower                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 7.71 ms: 1.14x slower                                                  |
| nqueens                    | 112 ms                                                       | 128 ms: 1.14x slower                                                   |
| richards                   | 65.5 ms                                                      | 75.0 ms: 1.14x slower                                                  |
| pprint_safe_repr           | 987 ms                                                       | 1.13 sec: 1.15x slower                                                 |
| chaos                      | 83.6 ms                                                      | 96.2 ms: 1.15x slower                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 7.25 sec: 1.15x slower                                                 |
| create_gc_cycles           | 2.41 ms                                                      | 2.78 ms: 1.15x slower                                                  |
| xml_etree_process          | 85.9 ms                                                      | 99.8 ms: 1.16x slower                                                  |
| generators                 | 40.0 ms                                                      | 46.8 ms: 1.17x slower                                                  |
| json_loads                 | 34.3 us                                                      | 40.1 us: 1.17x slower                                                  |
| comprehensions             | 22.2 us                                                      | 26.1 us: 1.17x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 172 ms: 1.17x slower                                                   |
| fannkuch                   | 547 ms                                                       | 645 ms: 1.18x slower                                                   |
| sqlglot_transpile          | 2.20 ms                                                      | 2.59 ms: 1.18x slower                                                  |
| pprint_pformat             | 1.94 sec                                                     | 2.30 sec: 1.19x slower                                                 |
| pickle_pure_python         | 416 us                                                       | 495 us: 1.19x slower                                                   |
| 2to3                       | 445 ms                                                       | 530 ms: 1.19x slower                                                   |
| typing_runtime_protocols   | 226 us                                                       | 269 us: 1.19x slower                                                   |
| logging_format             | 9.24 us                                                      | 11.0 us: 1.19x slower                                                  |
| logging_simple             | 8.56 us                                                      | 10.2 us: 1.19x slower                                                  |
| json                       | 6.51 ms                                                      | 7.87 ms: 1.21x slower                                                  |
| dulwich_log                | 93.7 ms                                                      | 114 ms: 1.22x slower                                                   |
| scimark_monte_carlo        | 90.6 ms                                                      | 111 ms: 1.23x slower                                                   |
| hexiom                     | 8.11 ms                                                      | 10.0 ms: 1.23x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 17.6 ms: 1.25x slower                                                  |
| genshi_text                | 31.7 ms                                                      | 40.5 ms: 1.28x slower                                                  |
| sqlglot_parse              | 1.76 ms                                                      | 2.27 ms: 1.29x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 19.9 ms: 1.30x slower                                                  |
| django_template            | 44.3 ms                                                      | 58.4 ms: 1.32x slower                                                  |
| coverage                   | 107 ms                                                       | 142 ms: 1.32x slower                                                   |
| raytrace                   | 344 ms                                                       | 459 ms: 1.33x slower                                                   |
| bench_thread_pool          | 2.89 ms                                                      | 3.94 ms: 1.37x slower                                                  |
| python_startup             | 22.4 ms                                                      | 32.4 ms: 1.45x slower                                                  |
| deltablue                  | 4.44 ms                                                      | 6.49 ms: 1.46x slower                                                  |
| nbody                      | 119 ms                                                       | 179 ms: 1.51x slower                                                   |
| mako                       | 15.9 ms                                                      | 24.2 ms: 1.52x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 84.2 ms: 4.51x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.08x slower                                                           |

Benchmark hidden because not significant (11): spectral_norm, go, telco, pylint, deepcopy_memo, scimark_sor, async_generators, html5lib, pycparser, pathlib, coroutines
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250210-3.14.0a4+-7e6ee50-NOGIL/bm-20250210-linux-x86_64-python-7e6ee50b6b8c760bcefb-3.14.0a4+-7e6ee50.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.056x slower

# HPT report

- Reliability score: 99.93% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.35x