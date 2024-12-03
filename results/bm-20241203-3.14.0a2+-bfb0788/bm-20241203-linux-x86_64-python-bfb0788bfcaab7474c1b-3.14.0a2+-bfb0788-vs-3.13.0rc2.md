# Results vs. 3.13.0rc2

- fork: python
- ref: bfb0788bfcaab7474c1b
- machine: linux-x86_64
- commit hash: bfb0788
- commit date: 2024-12-03
- overall geometric mean: 1.070x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.01 sec                                                     | 3.56 sec: 1.13x faster                                                 |
| html5lib       | 92.6 ms                                                      | 83.4 ms: 1.11x faster                                                  |
| Geometric mean | (ref)                                                        | 1.08x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 864 ms: 1.61x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 879 ms: 1.59x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 483 ms: 1.47x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 469 ms: 1.43x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 355 ms: 1.42x faster                                                   |
| async_tree_none            | 572 ms                                                       | 426 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 682 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 680 ms: 1.25x faster                                                   |
| async_generators           | 567 ms                                                       | 546 ms: 1.04x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 739 ms: 1.04x faster                                                   |
| Geometric mean             | (ref)                                                        | 1.30x faster                                                           |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 234 ms: 1.07x faster                                                   |
| float          | 116 ms                                                       | 108 ms: 1.07x faster                                                   |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.26 ms: 1.11x faster                                                  |
| regex_dna      | 282 ms                                                       | 268 ms: 1.05x faster                                                   |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmark hidden because not significant (2): regex_compile, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|---------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse     | 231 ms                                                       | 203 ms: 1.14x faster                                                   |
| xml_etree_iterparse | 177 ms                                                       | 163 ms: 1.09x faster                                                   |
| xml_etree_generate  | 122 ms                                                       | 114 ms: 1.07x faster                                                   |
| xml_etree_process   | 85.9 ms                                                      | 80.3 ms: 1.07x faster                                                  |
| tomli_loads         | 2.78 sec                                                     | 2.71 sec: 1.03x faster                                                 |
| pickle_pure_python  | 416 us                                                       | 438 us: 1.05x slower                                                   |
| json_dumps          | 14.1 ms                                                      | 15.3 ms: 1.08x slower                                                  |
| Geometric mean      | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (2): json_loads, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 14.4 ms: 1.06x faster                                                  |
| python_startup         | 22.4 ms                                                      | 23.9 ms: 1.07x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.00x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 28.8 ms: 1.10x faster                                                  |
| genshi_xml      | 72.1 ms                                                      | 65.9 ms: 1.09x faster                                                  |
| django_template | 44.3 ms                                                      | 46.1 ms: 1.04x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.03x faster                                                           |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.39 sec                                                     | 864 ms: 1.61x faster                                                   |
| async_tree_io_tg           | 1.40 sec                                                     | 879 ms: 1.59x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 483 ms: 1.47x faster                                                   |
| deepcopy                   | 498 us                                                       | 344 us: 1.45x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 469 ms: 1.43x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 355 ms: 1.42x faster                                                   |
| async_tree_none            | 572 ms                                                       | 426 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 682 ms: 1.30x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 40.0 us: 1.25x faster                                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 680 ms: 1.25x faster                                                   |
| go                         | 191 ms                                                       | 154 ms: 1.24x faster                                                   |
| telco                      | 12.2 ms                                                      | 10.2 ms: 1.20x faster                                                  |
| pylint                     | 470 ms                                                       | 393 ms: 1.20x faster                                                   |
| deepcopy_reduce            | 4.10 us                                                      | 3.58 us: 1.14x faster                                                  |
| xml_etree_parse            | 231 ms                                                       | 203 ms: 1.14x faster                                                   |
| scimark_sor                | 179 ms                                                       | 158 ms: 1.13x faster                                                   |
| docutils                   | 4.01 sec                                                     | 3.56 sec: 1.13x faster                                                 |
| sqlglot_optimize           | 74.7 ms                                                      | 66.4 ms: 1.13x faster                                                  |
| logging_format             | 9.24 us                                                      | 8.29 us: 1.12x faster                                                  |
| regex_effbot               | 4.74 ms                                                      | 4.26 ms: 1.11x faster                                                  |
| mdp                        | 3.80 sec                                                     | 3.42 sec: 1.11x faster                                                 |
| html5lib                   | 92.6 ms                                                      | 83.4 ms: 1.11x faster                                                  |
| bpe_tokeniser              | 6.28 sec                                                     | 5.68 sec: 1.11x faster                                                 |
| pathlib                    | 29.9 ms                                                      | 27.1 ms: 1.10x faster                                                  |
| genshi_text                | 31.7 ms                                                      | 28.8 ms: 1.10x faster                                                  |
| nqueens                    | 112 ms                                                       | 102 ms: 1.10x faster                                                   |
| genshi_xml                 | 72.1 ms                                                      | 65.9 ms: 1.09x faster                                                  |
| xml_etree_iterparse        | 177 ms                                                       | 163 ms: 1.09x faster                                                   |
| logging_simple             | 8.56 us                                                      | 7.91 us: 1.08x faster                                                  |
| xml_etree_generate         | 122 ms                                                       | 114 ms: 1.07x faster                                                   |
| pprint_safe_repr           | 987 ms                                                       | 920 ms: 1.07x faster                                                   |
| pidigits                   | 251 ms                                                       | 234 ms: 1.07x faster                                                   |
| xml_etree_process          | 85.9 ms                                                      | 80.3 ms: 1.07x faster                                                  |
| float                      | 116 ms                                                       | 108 ms: 1.07x faster                                                   |
| thrift                     | 1.10 ms                                                      | 1.03 ms: 1.07x faster                                                  |
| sympy_sum                  | 210 ms                                                       | 197 ms: 1.06x faster                                                   |
| python_startup_no_site     | 15.3 ms                                                      | 14.4 ms: 1.06x faster                                                  |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 6.41 ms: 1.05x faster                                                  |
| richards_super             | 73.2 ms                                                      | 69.6 ms: 1.05x faster                                                  |
| json                       | 6.51 ms                                                      | 6.19 ms: 1.05x faster                                                  |
| coverage                   | 107 ms                                                       | 102 ms: 1.05x faster                                                   |
| regex_dna                  | 282 ms                                                       | 268 ms: 1.05x faster                                                   |
| chaos                      | 83.6 ms                                                      | 79.8 ms: 1.05x faster                                                  |
| pprint_pformat             | 1.94 sec                                                     | 1.86 sec: 1.05x faster                                                 |
| meteor_contest             | 150 ms                                                       | 144 ms: 1.04x faster                                                   |
| richards                   | 65.5 ms                                                      | 62.9 ms: 1.04x faster                                                  |
| async_generators           | 567 ms                                                       | 546 ms: 1.04x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 739 ms: 1.04x faster                                                   |
| fannkuch                   | 547 ms                                                       | 528 ms: 1.04x faster                                                   |
| tomli_loads                | 2.78 sec                                                     | 2.71 sec: 1.03x faster                                                 |
| django_template            | 44.3 ms                                                      | 46.1 ms: 1.04x slower                                                  |
| pickle_pure_python         | 416 us                                                       | 438 us: 1.05x slower                                                   |
| hexiom                     | 8.11 ms                                                      | 8.57 ms: 1.06x slower                                                  |
| python_startup             | 22.4 ms                                                      | 23.9 ms: 1.07x slower                                                  |
| logging_silent             | 130 ns                                                       | 139 ns: 1.07x slower                                                   |
| json_dumps                 | 14.1 ms                                                      | 15.3 ms: 1.08x slower                                                  |
| sqlglot_normalize          | 140 ms                                                       | 168 ms: 1.20x slower                                                   |
| gc_traversal               | 5.70 ms                                                      | 7.02 ms: 1.23x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 3.23 ms: 1.34x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 88.9 ms: 4.76x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                           |

Benchmark hidden because not significant (28): sympy_integrate, sympy_str, deltablue, json_loads, typing_runtime_protocols, unpickle_pure_python, generators, bench_thread_pool, crypto_pyaes, comprehensions, scimark_monte_carlo, spectral_norm, regex_compile, coroutines, pyflate, sqlglot_parse, pycparser, sympy_expand, 2to3, dulwich_log, sqlglot_transpile, raytrace, scimark_fft, sqlite_synth, regex_v8, mako, nbody, scimark_lu
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241203-3.14.0a2+-bfb0788/bm-20241203-linux-x86_64-python-bfb0788bfcaab7474c1b-3.14.0a2+-bfb0788.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.070x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.12x