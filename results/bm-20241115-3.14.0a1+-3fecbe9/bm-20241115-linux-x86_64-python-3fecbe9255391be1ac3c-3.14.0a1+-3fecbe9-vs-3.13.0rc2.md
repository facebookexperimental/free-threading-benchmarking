# Results vs. 3.13.0rc2

- fork: python
- ref: 3fecbe9255391be1ac3c
- machine: linux-x86_64
- commit hash: 3fecbe9
- commit date: 2024-11-15
- overall geometric mean: 1.01x faster
- HPT reliability: 99.82%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| docutils       | 4.01 sec                                                     | 3.70 sec: 1.08x faster                                                 |
| html5lib       | 92.6 ms                                                      | 86.7 ms: 1.07x faster                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                           |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_tcp      | 948 ms                                                       | 903 ms: 1.05x faster                                                   |
| async_generators | 567 ms                                                       | 542 ms: 1.05x faster                                                   |
| coroutines       | 30.9 ms                                                      | 33.0 ms: 1.07x slower                                                  |
| Geometric mean   | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (2): asyncio_tcp_ssl, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 119 ms                                                       | 124 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 34.4 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (3): regex_compile, regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|---------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse | 177 ms                                                       | 154 ms: 1.15x faster                                                   |
| xml_etree_parse     | 231 ms                                                       | 219 ms: 1.05x faster                                                   |
| unpickle            | 20.5 us                                                      | 19.5 us: 1.05x faster                                                  |
| tomli_loads         | 2.78 sec                                                     | 2.68 sec: 1.04x faster                                                 |
| pickle_pure_python  | 416 us                                                       | 437 us: 1.05x slower                                                   |
| json_loads          | 34.3 us                                                      | 36.6 us: 1.07x slower                                                  |
| json_dumps          | 14.1 ms                                                      | 15.3 ms: 1.09x slower                                                  |
| pickle              | 15.1 us                                                      | 17.3 us: 1.14x slower                                                  |
| Geometric mean      | (ref)                                                        | 1.00x faster                                                           |

Benchmark hidden because not significant (6): xml_etree_generate, xml_etree_process, pickle_dict, unpickle_list, unpickle_pure_python, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 13.9 ms: 1.10x faster                                                  |
| python_startup         | 22.4 ms                                                      | 20.5 ms: 1.09x faster                                                  |
| Geometric mean         | (ref)                                                        | 1.10x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text    | 31.7 ms                                                      | 30.2 ms: 1.05x faster                                                  |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (3): genshi_xml, django_template, mako

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-linux-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| deepcopy                 | 498 us                                                       | 352 us: 1.42x faster                                                   |
| deepcopy_memo            | 50.1 us                                                      | 39.9 us: 1.26x faster                                                  |
| unpack_sequence          | 74.3 ns                                                      | 59.7 ns: 1.24x faster                                                  |
| go                       | 191 ms                                                       | 160 ms: 1.19x faster                                                   |
| telco                    | 12.2 ms                                                      | 10.4 ms: 1.17x faster                                                  |
| xml_etree_iterparse      | 177 ms                                                       | 154 ms: 1.15x faster                                                   |
| python_startup_no_site   | 15.3 ms                                                      | 13.9 ms: 1.10x faster                                                  |
| sympy_integrate          | 30.2 ms                                                      | 27.5 ms: 1.10x faster                                                  |
| python_startup           | 22.4 ms                                                      | 20.5 ms: 1.09x faster                                                  |
| fannkuch                 | 547 ms                                                       | 501 ms: 1.09x faster                                                   |
| deepcopy_reduce          | 4.10 us                                                      | 3.76 us: 1.09x faster                                                  |
| docutils                 | 4.01 sec                                                     | 3.70 sec: 1.08x faster                                                 |
| bpe_tokeniser            | 6.28 sec                                                     | 5.83 sec: 1.08x faster                                                 |
| meteor_contest           | 150 ms                                                       | 140 ms: 1.07x faster                                                   |
| typing_runtime_protocols | 226 us                                                       | 211 us: 1.07x faster                                                   |
| html5lib                 | 92.6 ms                                                      | 86.7 ms: 1.07x faster                                                  |
| sqlglot_optimize         | 74.7 ms                                                      | 70.2 ms: 1.06x faster                                                  |
| nqueens                  | 112 ms                                                       | 105 ms: 1.06x faster                                                   |
| scimark_sparse_mat_mult  | 6.76 ms                                                      | 6.39 ms: 1.06x faster                                                  |
| xml_etree_parse          | 231 ms                                                       | 219 ms: 1.05x faster                                                   |
| pprint_safe_repr         | 987 ms                                                       | 937 ms: 1.05x faster                                                   |
| unpickle                 | 20.5 us                                                      | 19.5 us: 1.05x faster                                                  |
| asyncio_tcp              | 948 ms                                                       | 903 ms: 1.05x faster                                                   |
| sympy_str                | 379 ms                                                       | 362 ms: 1.05x faster                                                   |
| sqlite_synth             | 3.99 us                                                      | 3.80 us: 1.05x faster                                                  |
| genshi_text              | 31.7 ms                                                      | 30.2 ms: 1.05x faster                                                  |
| thrift                   | 1.10 ms                                                      | 1.05 ms: 1.05x faster                                                  |
| gc_traversal             | 5.70 ms                                                      | 5.44 ms: 1.05x faster                                                  |
| async_generators         | 567 ms                                                       | 542 ms: 1.05x faster                                                   |
| richards                 | 65.5 ms                                                      | 62.9 ms: 1.04x faster                                                  |
| tomli_loads              | 2.78 sec                                                     | 2.68 sec: 1.04x faster                                                 |
| pyflate                  | 664 ms                                                       | 641 ms: 1.04x faster                                                   |
| pprint_pformat           | 1.94 sec                                                     | 1.88 sec: 1.04x faster                                                 |
| scimark_monte_carlo      | 90.6 ms                                                      | 87.7 ms: 1.03x faster                                                  |
| sqlglot_normalize        | 140 ms                                                       | 145 ms: 1.04x slower                                                   |
| nbody                    | 119 ms                                                       | 124 ms: 1.05x slower                                                   |
| regex_v8                 | 32.8 ms                                                      | 34.4 ms: 1.05x slower                                                  |
| pickle_pure_python       | 416 us                                                       | 437 us: 1.05x slower                                                   |
| raytrace                 | 344 ms                                                       | 362 ms: 1.05x slower                                                   |
| coverage                 | 107 ms                                                       | 113 ms: 1.05x slower                                                   |
| scimark_lu               | 146 ms                                                       | 155 ms: 1.06x slower                                                   |
| json                     | 6.51 ms                                                      | 6.92 ms: 1.06x slower                                                  |
| logging_silent           | 130 ns                                                       | 139 ns: 1.07x slower                                                   |
| json_loads               | 34.3 us                                                      | 36.6 us: 1.07x slower                                                  |
| coroutines               | 30.9 ms                                                      | 33.0 ms: 1.07x slower                                                  |
| dulwich_log              | 93.7 ms                                                      | 100 ms: 1.07x slower                                                   |
| json_dumps               | 14.1 ms                                                      | 15.3 ms: 1.09x slower                                                  |
| pickle                   | 15.1 us                                                      | 17.3 us: 1.14x slower                                                  |
| bench_mp_pool            | 18.7 ms                                                      | 66.7 ms: 3.57x slower                                                  |
| Geometric mean           | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (39): genshi_xml, pathlib, scimark_sor, xml_etree_generate, regex_compile, xml_etree_process, 2to3, pidigits, crypto_pyaes, richards_super, generators, pylint, comprehensions, pickle_dict, logging_simple, asyncio_tcp_ssl, pycparser, mdp, asyncio_websockets, sqlglot_parse, unpickle_list, chaos, sympy_expand, create_gc_cycles, django_template, spectral_norm, unpickle_pure_python, sympy_sum, float, bench_thread_pool, regex_dna, scimark_fft, hexiom, regex_effbot, pickle_list, logging_format, sqlglot_transpile, deltablue, mako
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 99.82% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x