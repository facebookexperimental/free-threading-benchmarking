# Results vs. 3.13.0rc2

- fork: python
- ref: 9211b3dabeacb92713ac
- machine: linux-x86_64
- commit hash: 9211b3d
- commit date: 2025-02-28
- overall geometric mean: 1.043x slower
- HPT reliability: 99.75%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 504 ms: 1.13x slower                                                   |
| html5lib       | 92.6 ms                                                      | 97.3 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                        | 1.06x slower                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 738 ms: 1.90x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 797 ms: 1.74x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 427 ms: 1.57x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 330 ms: 1.52x faster                                                   |
| async_tree_none            | 572 ms                                                       | 391 ms: 1.46x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 513 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 654 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 704 ms: 1.26x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 741 ms: 1.03x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.35x faster                                                           |

Benchmark hidden because not significant (2): async_generators, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 116 ms                                                       | 99.4 ms: 1.17x faster                                                  |
| nbody          | 119 ms                                                       | 182 ms: 1.53x slower                                                   |
| Geometric mean | (ref)                                                        | 1.09x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.41 ms: 1.07x faster                                                  |
| regex_dna      | 282 ms                                                       | 303 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                        | 1.00x slower                                                           |

Benchmark hidden because not significant (2): regex_v8, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 177 ms                                                       | 133 ms: 1.33x faster                                                   |
| xml_etree_parse      | 231 ms                                                       | 199 ms: 1.16x faster                                                   |
| tomli_loads          | 2.78 sec                                                     | 3.05 sec: 1.10x slower                                                 |
| xml_etree_generate   | 122 ms                                                       | 135 ms: 1.10x slower                                                   |
| unpickle_pure_python | 290 us                                                       | 333 us: 1.15x slower                                                   |
| pickle_pure_python   | 416 us                                                       | 492 us: 1.18x slower                                                   |
| json_loads           | 34.3 us                                                      | 40.8 us: 1.19x slower                                                  |
| json_dumps           | 14.1 ms                                                      | 17.0 ms: 1.21x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.05x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 20.3 ms: 1.33x slower                                                  |
| python_startup         | 22.4 ms                                                      | 30.2 ms: 1.35x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.34x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 37.0 ms: 1.17x slower                                                  |
| genshi_xml      | 72.1 ms                                                      | 84.8 ms: 1.18x slower                                                  |
| django_template | 44.3 ms                                                      | 52.4 ms: 1.18x slower                                                  |
| mako            | 15.9 ms                                                      | 22.7 ms: 1.42x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.23x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 738 ms: 1.90x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 797 ms: 1.74x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 427 ms: 1.57x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 330 ms: 1.52x faster                                                   |
| gc_traversal               | 5.70 ms                                                      | 3.86 ms: 1.48x faster                                                  |
| async_tree_none            | 572 ms                                                       | 391 ms: 1.46x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 513 ms: 1.38x faster                                                   |
| xml_etree_iterparse        | 177 ms                                                       | 133 ms: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 654 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 704 ms: 1.26x faster                                                   |
| deepcopy                   | 498 us                                                       | 411 us: 1.21x faster                                                   |
| float                      | 116 ms                                                       | 99.4 ms: 1.17x faster                                                  |
| xml_etree_parse            | 231 ms                                                       | 199 ms: 1.16x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.44 us: 1.16x faster                                                  |
| spectral_norm              | 157 ms                                                       | 142 ms: 1.10x faster                                                   |
| go                         | 191 ms                                                       | 175 ms: 1.09x faster                                                   |
| regex_effbot               | 4.74 ms                                                      | 4.41 ms: 1.07x faster                                                  |
| telco                      | 12.2 ms                                                      | 11.7 ms: 1.04x faster                                                  |
| asyncio_websockets         | 766 ms                                                       | 741 ms: 1.03x faster                                                   |
| html5lib                   | 92.6 ms                                                      | 97.3 ms: 1.05x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 2.54 ms: 1.05x slower                                                  |
| richards                   | 65.5 ms                                                      | 69.5 ms: 1.06x slower                                                  |
| scimark_sor                | 179 ms                                                       | 190 ms: 1.06x slower                                                   |
| pathlib                    | 29.9 ms                                                      | 31.9 ms: 1.07x slower                                                  |
| sqlglot_normalize          | 140 ms                                                       | 150 ms: 1.07x slower                                                   |
| regex_dna                  | 282 ms                                                       | 303 ms: 1.07x slower                                                   |
| chaos                      | 83.6 ms                                                      | 89.8 ms: 1.07x slower                                                  |
| thrift                     | 1.10 ms                                                      | 1.19 ms: 1.08x slower                                                  |
| pprint_safe_repr           | 987 ms                                                       | 1.07 sec: 1.08x slower                                                 |
| richards_super             | 73.2 ms                                                      | 79.6 ms: 1.09x slower                                                  |
| deepcopy_reduce            | 4.10 us                                                      | 4.46 us: 1.09x slower                                                  |
| comprehensions             | 22.2 us                                                      | 24.3 us: 1.09x slower                                                  |
| tomli_loads                | 2.78 sec                                                     | 3.05 sec: 1.10x slower                                                 |
| generators                 | 40.0 ms                                                      | 43.9 ms: 1.10x slower                                                  |
| json                       | 6.51 ms                                                      | 7.18 ms: 1.10x slower                                                  |
| xml_etree_generate         | 122 ms                                                       | 135 ms: 1.10x slower                                                   |
| sympy_integrate            | 30.2 ms                                                      | 33.4 ms: 1.10x slower                                                  |
| dulwich_log                | 93.7 ms                                                      | 104 ms: 1.11x slower                                                   |
| logging_silent             | 130 ns                                                       | 145 ns: 1.11x slower                                                   |
| sqlglot_optimize           | 74.7 ms                                                      | 84.0 ms: 1.12x slower                                                  |
| nqueens                    | 112 ms                                                       | 126 ms: 1.13x slower                                                   |
| mdp                        | 3.80 sec                                                     | 4.28 sec: 1.13x slower                                                 |
| sympy_str                  | 379 ms                                                       | 427 ms: 1.13x slower                                                   |
| 2to3                       | 445 ms                                                       | 504 ms: 1.13x slower                                                   |
| sympy_expand               | 601 ms                                                       | 681 ms: 1.13x slower                                                   |
| pprint_pformat             | 1.94 sec                                                     | 2.20 sec: 1.13x slower                                                 |
| pyflate                    | 664 ms                                                       | 756 ms: 1.14x slower                                                   |
| unpickle_pure_python       | 290 us                                                       | 333 us: 1.15x slower                                                   |
| logging_simple             | 8.56 us                                                      | 9.83 us: 1.15x slower                                                  |
| meteor_contest             | 150 ms                                                       | 174 ms: 1.16x slower                                                   |
| deltablue                  | 4.44 ms                                                      | 5.17 ms: 1.17x slower                                                  |
| genshi_text                | 31.7 ms                                                      | 37.0 ms: 1.17x slower                                                  |
| genshi_xml                 | 72.1 ms                                                      | 84.8 ms: 1.18x slower                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 7.41 sec: 1.18x slower                                                 |
| pickle_pure_python         | 416 us                                                       | 492 us: 1.18x slower                                                   |
| typing_runtime_protocols   | 226 us                                                       | 266 us: 1.18x slower                                                   |
| django_template            | 44.3 ms                                                      | 52.4 ms: 1.18x slower                                                  |
| fannkuch                   | 547 ms                                                       | 648 ms: 1.18x slower                                                   |
| sqlglot_transpile          | 2.20 ms                                                      | 2.61 ms: 1.19x slower                                                  |
| crypto_pyaes               | 100 ms                                                       | 119 ms: 1.19x slower                                                   |
| json_loads                 | 34.3 us                                                      | 40.8 us: 1.19x slower                                                  |
| json_dumps                 | 14.1 ms                                                      | 17.0 ms: 1.21x slower                                                  |
| sympy_sum                  | 210 ms                                                       | 254 ms: 1.21x slower                                                   |
| hexiom                     | 8.11 ms                                                      | 9.90 ms: 1.22x slower                                                  |
| logging_format             | 9.24 us                                                      | 11.3 us: 1.22x slower                                                  |
| raytrace                   | 344 ms                                                       | 428 ms: 1.24x slower                                                   |
| sqlglot_parse              | 1.76 ms                                                      | 2.20 ms: 1.25x slower                                                  |
| coverage                   | 107 ms                                                       | 139 ms: 1.29x slower                                                   |
| python_startup_no_site     | 15.3 ms                                                      | 20.3 ms: 1.33x slower                                                  |
| python_startup             | 22.4 ms                                                      | 30.2 ms: 1.35x slower                                                  |
| scimark_lu                 | 146 ms                                                       | 201 ms: 1.37x slower                                                   |
| scimark_fft                | 473 ms                                                       | 653 ms: 1.38x slower                                                   |
| mako                       | 15.9 ms                                                      | 22.7 ms: 1.42x slower                                                  |
| scimark_monte_carlo        | 90.6 ms                                                      | 130 ms: 1.44x slower                                                   |
| bench_thread_pool          | 2.89 ms                                                      | 4.38 ms: 1.52x slower                                                  |
| nbody                      | 119 ms                                                       | 182 ms: 1.53x slower                                                   |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 10.5 ms: 1.55x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 88.2 ms: 4.72x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.07x slower                                                           |

Benchmark hidden because not significant (10): pylint, pidigits, deepcopy_memo, regex_v8, pycparser, async_generators, coroutines, docutils, regex_compile, xml_etree_process
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250228-3.14.0a5+-9211b3d-NOGIL/bm-20250228-linux-x86_64-python-9211b3dabeacb92713ac-3.14.0a5+-9211b3d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.043x slower

# HPT report

- Reliability score: 99.75% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.35x