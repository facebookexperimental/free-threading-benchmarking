# Results vs. 3.13.0rc2

- fork: python
- ref: 180ee43bde99b8ce4c4f
- machine: linux-x86_64
- commit hash: 180ee43
- commit date: 2025-01-28
- overall geometric mean: 1.016x faster
- HPT reliability: 92.58%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 445 ms                                                       | 529 ms: 1.19x slower                                                   |
| html5lib       | 92.6 ms                                                      | 77.2 ms: 1.20x faster                                                  |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 906 ms: 1.55x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 455 ms: 1.47x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 491 ms: 1.45x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 981 ms: 1.41x faster                                                   |
| async_tree_none            | 572 ms                                                       | 425 ms: 1.35x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 376 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 686 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 727 ms: 1.22x faster                                                   |
| asyncio_websockets         | 766 ms                                                       | 701 ms: 1.09x faster                                                   |
| coroutines                 | 30.9 ms                                                      | 34.7 ms: 1.12x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.26x faster                                                           |

Benchmark hidden because not significant (1): async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 119 ms                                                       | 130 ms: 1.10x slower                                                   |
| Geometric mean | (ref)                                                        | 1.02x slower                                                           |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 4.74 ms                                                      | 4.20 ms: 1.13x faster                                                  |
| Geometric mean | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (3): regex_dna, regex_compile, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_generate   | 122 ms                                                       | 109 ms: 1.12x faster                                                   |
| tomli_loads          | 2.78 sec                                                     | 2.53 sec: 1.10x faster                                                 |
| xml_etree_process    | 85.9 ms                                                      | 78.6 ms: 1.09x faster                                                  |
| xml_etree_iterparse  | 177 ms                                                       | 164 ms: 1.08x faster                                                   |
| pickle_pure_python   | 416 us                                                       | 469 us: 1.13x slower                                                   |
| json_dumps           | 14.1 ms                                                      | 16.5 ms: 1.17x slower                                                  |
| unpickle_pure_python | 290 us                                                       | 345 us: 1.19x slower                                                   |
| json_loads           | 34.3 us                                                      | 41.3 us: 1.20x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.03x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 17.1 ms: 1.12x slower                                                  |
| python_startup         | 22.4 ms                                                      | 29.7 ms: 1.32x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.22x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                      | 29.2 ms: 1.09x faster                                                  |
| django_template | 44.3 ms                                                      | 50.1 ms: 1.13x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (2): genshi_xml, mako

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 906 ms: 1.55x faster                                                   |
| async_tree_memoization_tg  | 670 ms                                                       | 455 ms: 1.47x faster                                                   |
| async_tree_memoization     | 709 ms                                                       | 491 ms: 1.45x faster                                                   |
| async_tree_io              | 1.39 sec                                                     | 981 ms: 1.41x faster                                                   |
| deepcopy                   | 498 us                                                       | 363 us: 1.37x faster                                                   |
| async_tree_none            | 572 ms                                                       | 425 ms: 1.35x faster                                                   |
| async_tree_none_tg         | 504 ms                                                       | 376 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 686 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed    | 889 ms                                                       | 727 ms: 1.22x faster                                                   |
| go                         | 191 ms                                                       | 158 ms: 1.21x faster                                                   |
| html5lib                   | 92.6 ms                                                      | 77.2 ms: 1.20x faster                                                  |
| pylint                     | 470 ms                                                       | 399 ms: 1.18x faster                                                   |
| deepcopy_memo              | 50.1 us                                                      | 43.2 us: 1.16x faster                                                  |
| regex_effbot               | 4.74 ms                                                      | 4.20 ms: 1.13x faster                                                  |
| deepcopy_reduce            | 4.10 us                                                      | 3.63 us: 1.13x faster                                                  |
| spectral_norm              | 157 ms                                                       | 140 ms: 1.12x faster                                                   |
| xml_etree_generate         | 122 ms                                                       | 109 ms: 1.12x faster                                                   |
| sqlite_synth               | 3.99 us                                                      | 3.57 us: 1.12x faster                                                  |
| tomli_loads                | 2.78 sec                                                     | 2.53 sec: 1.10x faster                                                 |
| asyncio_websockets         | 766 ms                                                       | 701 ms: 1.09x faster                                                   |
| xml_etree_process          | 85.9 ms                                                      | 78.6 ms: 1.09x faster                                                  |
| pprint_safe_repr           | 987 ms                                                       | 904 ms: 1.09x faster                                                   |
| genshi_text                | 31.7 ms                                                      | 29.2 ms: 1.09x faster                                                  |
| xml_etree_iterparse        | 177 ms                                                       | 164 ms: 1.08x faster                                                   |
| pathlib                    | 29.9 ms                                                      | 28.2 ms: 1.06x faster                                                  |
| comprehensions             | 22.2 us                                                      | 21.0 us: 1.06x faster                                                  |
| typing_runtime_protocols   | 226 us                                                       | 214 us: 1.05x faster                                                   |
| sympy_sum                  | 210 ms                                                       | 221 ms: 1.05x slower                                                   |
| scimark_lu                 | 146 ms                                                       | 154 ms: 1.05x slower                                                   |
| dulwich_log                | 93.7 ms                                                      | 98.7 ms: 1.05x slower                                                  |
| sqlglot_parse              | 1.76 ms                                                      | 1.86 ms: 1.06x slower                                                  |
| pyflate                    | 664 ms                                                       | 708 ms: 1.07x slower                                                   |
| nqueens                    | 112 ms                                                       | 120 ms: 1.08x slower                                                   |
| chaos                      | 83.6 ms                                                      | 90.2 ms: 1.08x slower                                                  |
| scimark_fft                | 473 ms                                                       | 512 ms: 1.08x slower                                                   |
| sqlglot_transpile          | 2.20 ms                                                      | 2.38 ms: 1.08x slower                                                  |
| crypto_pyaes               | 100 ms                                                       | 109 ms: 1.09x slower                                                   |
| nbody                      | 119 ms                                                       | 130 ms: 1.10x slower                                                   |
| logging_simple             | 8.56 us                                                      | 9.40 us: 1.10x slower                                                  |
| python_startup_no_site     | 15.3 ms                                                      | 17.1 ms: 1.12x slower                                                  |
| coroutines                 | 30.9 ms                                                      | 34.7 ms: 1.12x slower                                                  |
| bench_thread_pool          | 2.89 ms                                                      | 3.24 ms: 1.12x slower                                                  |
| pickle_pure_python         | 416 us                                                       | 469 us: 1.13x slower                                                   |
| sqlglot_optimize           | 74.7 ms                                                      | 84.3 ms: 1.13x slower                                                  |
| django_template            | 44.3 ms                                                      | 50.1 ms: 1.13x slower                                                  |
| json                       | 6.51 ms                                                      | 7.43 ms: 1.14x slower                                                  |
| hexiom                     | 8.11 ms                                                      | 9.34 ms: 1.15x slower                                                  |
| sympy_integrate            | 30.2 ms                                                      | 34.8 ms: 1.15x slower                                                  |
| logging_silent             | 130 ns                                                       | 150 ns: 1.16x slower                                                   |
| json_dumps                 | 14.1 ms                                                      | 16.5 ms: 1.17x slower                                                  |
| coverage                   | 107 ms                                                       | 127 ms: 1.18x slower                                                   |
| 2to3                       | 445 ms                                                       | 529 ms: 1.19x slower                                                   |
| unpickle_pure_python       | 290 us                                                       | 345 us: 1.19x slower                                                   |
| logging_format             | 9.24 us                                                      | 11.0 us: 1.19x slower                                                  |
| json_loads                 | 34.3 us                                                      | 41.3 us: 1.20x slower                                                  |
| python_startup             | 22.4 ms                                                      | 29.7 ms: 1.32x slower                                                  |
| create_gc_cycles           | 2.41 ms                                                      | 3.51 ms: 1.45x slower                                                  |
| gc_traversal               | 5.70 ms                                                      | 9.75 ms: 1.71x slower                                                  |
| bench_mp_pool              | 18.7 ms                                                      | 100 ms: 5.35x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                           |

Benchmark hidden because not significant (29): pidigits, scimark_sparse_mat_mult, mdp, sympy_str, docutils, generators, genshi_xml, async_generators, telco, bpe_tokeniser, pycparser, deltablue, richards_super, scimark_sor, raytrace, richards, float, scimark_monte_carlo, fannkuch, regex_dna, pprint_pformat, sympy_expand, mako, sqlglot_normalize, xml_etree_parse, thrift, regex_compile, regex_v8, meteor_contest
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250128-3.14.0a4+-180ee43/bm-20250128-linux-x86_64-python-180ee43bde99b8ce4c4f-3.14.0a4+-180ee43.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.016x faster

# HPT report

- Reliability score: 92.58% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x