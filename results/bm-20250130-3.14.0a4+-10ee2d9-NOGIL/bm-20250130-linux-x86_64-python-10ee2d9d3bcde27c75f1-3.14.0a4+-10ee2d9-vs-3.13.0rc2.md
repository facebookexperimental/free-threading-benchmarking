# Results vs. 3.13.0rc2

- fork: python
- ref: 10ee2d9d3bcde27c75f1
- machine: linux-x86_64
- commit hash: 10ee2d9
- commit date: 2025-01-30
- overall geometric mean: 1.083x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 555 ms: 1.25x slower                                                   |
| html5lib       | 92.6 ms                                                      | 99.8 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                        | 1.11x slower                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 837 ms: 1.67x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 845 ms: 1.64x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 442 ms: 1.52x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 376 ms: 1.34x faster                                                   |
| async_tree_none            | 572 ms                                                       | 431 ms: 1.33x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 549 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 708 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 701 ms: 1.22x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 703 ms: 1.09x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                           |

Benchmark hidden because not significant (2): async_generators, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 109 ms: 1.06x faster                                                   |
| nbody          | 119 ms                                                       | 186 ms: 1.56x slower                                                   |
| Geometric mean | (ref)                                                        | 1.12x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 282 ms                                                       | 293 ms: 1.04x slower                                                   |
| regex_compile  | 182 ms                                                       | 214 ms: 1.17x slower                                                   |
| Geometric mean | (ref)                                                        | 1.06x slower                                                           |

Benchmark hidden because not significant (2): regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 144 ms: 1.23x faster                                                   |
| xml_etree_parse      | 231 ms                                                       | 216 ms: 1.07x faster                                                   |
| tomli_loads          | 2.78 sec                                                     | 3.09 sec: 1.11x slower                                                 |
| pickle_pure_python   | 416 us                                                       | 464 us: 1.11x slower                                                   |
| json_dumps           | 14.1 ms                                                      | 16.6 ms: 1.18x slower                                                  |
| xml_etree_generate   | 122 ms                                                       | 145 ms: 1.19x slower                                                   |
| xml_etree_process    | 85.9 ms                                                      | 105 ms: 1.22x slower                                                   |
| unpickle_pure_python | 290 us                                                       | 364 us: 1.25x slower                                                   |
| json_loads           | 34.3 us                                                      | 46.9 us: 1.37x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.12x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 21.4 ms: 1.40x slower                                                  |
| python_startup         | 22.4 ms                                                      | 33.7 ms: 1.50x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.45x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 86.5 ms: 1.20x slower                                                  |
| genshi_text     | 31.7 ms                                                      | 39.8 ms: 1.26x slower                                                  |
| django_template | 44.3 ms                                                      | 56.2 ms: 1.27x slower                                                  |
| mako            | 15.9 ms                                                      | 24.3 ms: 1.52x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.31x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 837 ms: 1.67x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 845 ms: 1.64x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 442 ms: 1.52x faster                                                   |
| gc_traversal               | 5.70 ms                                                      | 4.01 ms: 1.42x faster                                                  |
| async_tree_none_tg         | 504 ms                                                       | 376 ms: 1.34x faster                                                   |
| async_tree_none            | 572 ms                                                       | 431 ms: 1.33x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 549 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 708 ms: 1.25x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 144 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 701 ms: 1.22x faster                                                   |
| deepcopy                   | 498 us                                                       | 413 us: 1.21x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 703 ms: 1.09x faster                                                   |
| xml_etree_parse            | 231 ms                                                       | 216 ms: 1.07x faster                                                   |
| float                      | 116 ms                                                       | 109 ms: 1.06x faster                                                   |
| regex_dna                  | 282 ms                                                       | 293 ms: 1.04x slower                                                   |
| deepcopy_memo              | 50.1 us                                                      | 52.4 us: 1.05x slower                                                  |
| html5lib                   | 92.6 ms                                                      | 99.8 ms: 1.08x slower                                                  |
| nqueens                    | 112 ms                                                       | 121 ms: 1.08x slower                                                   |
| generators                 | 40.0 ms                                                      | 43.6 ms: 1.09x slower                                                  |
| scimark_sor                | 179 ms                                                       | 196 ms: 1.10x slower                                                   |
| pprint_safe_repr           | 987 ms                                                       | 1.09 sec: 1.11x slower                                                 |
| thrift                     | 1.10 ms                                                      | 1.22 ms: 1.11x slower                                                  |
| tomli_loads                | 2.78 sec                                                     | 3.09 sec: 1.11x slower                                                 |
| logging_format             | 9.24 us                                                      | 10.3 us: 1.11x slower                                                  |
| pickle_pure_python         | 416 us                                                       | 464 us: 1.11x slower                                                   |
| mdp                        | 3.80 sec                                                     | 4.27 sec: 1.12x slower                                                 |
| dulwich_log                | 93.7 ms                                                      | 106 ms: 1.13x slower                                                   |
| sympy_str                  | 379 ms                                                       | 431 ms: 1.14x slower                                                   |
| richards                   | 65.5 ms                                                      | 75.7 ms: 1.16x slower                                                  |
| comprehensions             | 22.2 us                                                      | 25.8 us: 1.16x slower                                                  |
| chaos                      | 83.6 ms                                                      | 97.6 ms: 1.17x slower                                                  |
| regex_compile              | 182 ms                                                       | 214 ms: 1.17x slower                                                   |
| json_dumps                 | 14.1 ms                                                      | 16.6 ms: 1.18x slower                                                  |
| sqlglot_normalize          | 140 ms                                                       | 164 ms: 1.18x slower                                                   |
| pyflate                    | 664 ms                                                       | 782 ms: 1.18x slower                                                   |
| scimark_fft                | 473 ms                                                       | 558 ms: 1.18x slower                                                   |
| sympy_expand               | 601 ms                                                       | 709 ms: 1.18x slower                                                   |
| xml_etree_generate         | 122 ms                                                       | 145 ms: 1.19x slower                                                   |
| sqlglot_optimize           | 74.7 ms                                                      | 88.7 ms: 1.19x slower                                                  |
| pprint_pformat             | 1.94 sec                                                     | 2.31 sec: 1.19x slower                                                 |
| bpe_tokeniser              | 6.28 sec                                                     | 7.48 sec: 1.19x slower                                                 |
| richards_super             | 73.2 ms                                                      | 87.3 ms: 1.19x slower                                                  |
| sympy_integrate            | 30.2 ms                                                      | 36.1 ms: 1.20x slower                                                  |
| genshi_xml                 | 72.1 ms                                                      | 86.5 ms: 1.20x slower                                                  |
| xml_etree_process          | 85.9 ms                                                      | 105 ms: 1.22x slower                                                   |
| sympy_sum                  | 210 ms                                                       | 257 ms: 1.23x slower                                                   |
| hexiom                     | 8.11 ms                                                      | 10.0 ms: 1.23x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 182 ms: 1.24x slower                                                   |
| 2to3                       | 445 ms                                                       | 555 ms: 1.25x slower                                                   |
| scimark_monte_carlo        | 90.6 ms                                                      | 113 ms: 1.25x slower                                                   |
| unpickle_pure_python       | 290 us                                                       | 364 us: 1.25x slower                                                   |
| genshi_text                | 31.7 ms                                                      | 39.8 ms: 1.26x slower                                                  |
| logging_simple             | 8.56 us                                                      | 10.9 us: 1.27x slower                                                  |
| django_template            | 44.3 ms                                                      | 56.2 ms: 1.27x slower                                                  |
| sqlglot_parse              | 1.76 ms                                                      | 2.23 ms: 1.27x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 3.12 ms: 1.29x slower                                                  |
| fannkuch                   | 547 ms                                                       | 710 ms: 1.30x slower                                                   |
| json                       | 6.51 ms                                                      | 8.48 ms: 1.30x slower                                                  |
| crypto_pyaes               | 100 ms                                                       | 132 ms: 1.32x slower                                                   |
| sqlglot_transpile          | 2.20 ms                                                      | 2.91 ms: 1.32x slower                                                  |
| logging_silent             | 130 ns                                                       | 173 ns: 1.33x slower                                                   |
| typing_runtime_protocols   | 226 us                                                       | 301 us: 1.33x slower                                                   |
| raytrace                   | 344 ms                                                       | 461 ms: 1.34x slower                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 9.20 ms: 1.36x slower                                                  |
| json_loads                 | 34.3 us                                                      | 46.9 us: 1.37x slower                                                  |
| meteor_contest             | 150 ms                                                       | 206 ms: 1.37x slower                                                   |
| bench_thread_pool          | 2.89 ms                                                      | 3.99 ms: 1.38x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 21.4 ms: 1.40x slower                                                  |
| coverage                   | 107 ms                                                       | 151 ms: 1.41x slower                                                   |
| deltablue                  | 4.44 ms                                                      | 6.68 ms: 1.50x slower                                                  |
| python_startup             | 22.4 ms                                                      | 33.7 ms: 1.50x slower                                                  |
| mako                       | 15.9 ms                                                      | 24.3 ms: 1.52x slower                                                  |
| nbody                      | 119 ms                                                       | 186 ms: 1.56x slower                                                   |
| bench_mp_pool              | 18.7 ms                                                      | 94.9 ms: 5.08x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.12x slower                                                           |

Benchmark hidden because not significant (14): sqlite_synth, pidigits, pylint, regex_v8, telco, deepcopy_reduce, pycparser, spectral_norm, async_generators, docutils, go, regex_effbot, pathlib, coroutines
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250130-3.14.0a4+-10ee2d9-NOGIL/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.083x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.35x