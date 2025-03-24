# Results vs. base

- fork: python
- ref: bc26f95e8ff60ccca981
- machine: linux-x86_64
- commit hash: bc26f95
- commit date: 2025-03-22
- overall geometric mean: 1.026x slower
- HPT reliability: 98.27%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-CLANG/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 404 ms                                                                                                            | 487 ms: 1.21x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.07x slower                                                                                                            |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-CLANG/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| coroutines                 | 31.8 ms                                                                                                           | 27.2 ms: 1.17x faster                                                                                                   |
| async_tree_none_tg         | 359 ms                                                                                                            | 375 ms: 1.05x slower                                                                                                    |
| asyncio_tcp_ssl            | 2.71 sec                                                                                                          | 2.86 sec: 1.06x slower                                                                                                  |
| asyncio_tcp                | 853 ms                                                                                                            | 906 ms: 1.06x slower                                                                                                    |
| async_tree_io              | 854 ms                                                                                                            | 910 ms: 1.07x slower                                                                                                    |
| asyncio_websockets         | 714 ms                                                                                                            | 761 ms: 1.07x slower                                                                                                    |
| async_tree_io_tg           | 877 ms                                                                                                            | 942 ms: 1.07x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 664 ms                                                                                                            | 716 ms: 1.08x slower                                                                                                    |
| async_tree_memoization_tg  | 440 ms                                                                                                            | 489 ms: 1.11x slower                                                                                                    |
| async_tree_memoization     | 461 ms                                                                                                            | 521 ms: 1.13x slower                                                                                                    |
| async_generators           | 479 ms                                                                                                            | 542 ms: 1.13x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 665 ms                                                                                                            | 782 ms: 1.18x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.06x slower                                                                                                            |

Benchmark hidden because not significant (1): async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-CLANG/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| nbody          | 129 ms                                                                                                            | 114 ms: 1.13x faster                                                                                                    |
| float          | 95.4 ms                                                                                                           | 107 ms: 1.12x slower                                                                                                    |
| pidigits       | 240 ms                                                                                                            | 274 ms: 1.14x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.04x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-CLANG/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_compile  | 180 ms                                                                                                            | 165 ms: 1.09x faster                                                                                                    |
| regex_v8       | 30.2 ms                                                                                                           | 28.9 ms: 1.04x faster                                                                                                   |
| regex_effbot   | 3.99 ms                                                                                                           | 4.21 ms: 1.05x slower                                                                                                   |
| Geometric mean | (ref)                                                                                                             | 1.03x faster                                                                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-CLANG/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|---------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| unpickle_list       | 6.88 us                                                                                                           | 6.24 us: 1.10x faster                                                                                                   |
| json_loads          | 38.1 us                                                                                                           | 36.6 us: 1.04x faster                                                                                                   |
| tomli_loads         | 2.43 sec                                                                                                          | 2.50 sec: 1.03x slower                                                                                                  |
| unpickle            | 18.5 us                                                                                                           | 19.3 us: 1.04x slower                                                                                                   |
| xml_etree_process   | 77.6 ms                                                                                                           | 82.0 ms: 1.06x slower                                                                                                   |
| pickle_pure_python  | 399 us                                                                                                            | 436 us: 1.09x slower                                                                                                    |
| xml_etree_iterparse | 139 ms                                                                                                            | 154 ms: 1.11x slower                                                                                                    |
| pickle_list         | 6.61 us                                                                                                           | 7.37 us: 1.12x slower                                                                                                   |
| pickle              | 16.4 us                                                                                                           | 18.4 us: 1.12x slower                                                                                                   |
| xml_etree_generate  | 113 ms                                                                                                            | 129 ms: 1.14x slower                                                                                                    |
| json_dumps          | 15.1 ms                                                                                                           | 17.4 ms: 1.15x slower                                                                                                   |
| xml_etree_parse     | 186 ms                                                                                                            | 231 ms: 1.24x slower                                                                                                    |
| Geometric mean      | (ref)                                                                                                             | 1.06x slower                                                                                                            |

Benchmark hidden because not significant (2): pickle_dict, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-CLANG/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 28.8 ms                                                                                                           | 32.5 ms: 1.13x slower                                                                                                   |
| python_startup_no_site | 17.0 ms                                                                                                           | 19.4 ms: 1.14x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.13x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-CLANG/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 44.1 ms                                                                                                           | 47.5 ms: 1.08x slower                                                                                                   |
| mako            | 16.5 ms                                                                                                           | 18.5 ms: 1.12x slower                                                                                                   |
| genshi_xml      | 63.7 ms                                                                                                           | 71.9 ms: 1.13x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | results/bm-20250322-3.14.0a6+-bc26f95/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json | results/bm-20250322-3.14.0a6+-bc26f95-CLANG/bm-20250322-linux-x86_64-python-bc26f95e8ff60ccca981-3.14.0a6+-bc26f95.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| spectral_norm              | 125 ms                                                                                                            | 105 ms: 1.19x faster                                                                                                    |
| coverage                   | 122 ms                                                                                                            | 104 ms: 1.17x faster                                                                                                    |
| coroutines                 | 31.8 ms                                                                                                           | 27.2 ms: 1.17x faster                                                                                                   |
| nbody                      | 129 ms                                                                                                            | 114 ms: 1.13x faster                                                                                                    |
| hexiom                     | 8.50 ms                                                                                                           | 7.55 ms: 1.13x faster                                                                                                   |
| scimark_fft                | 438 ms                                                                                                            | 390 ms: 1.12x faster                                                                                                    |
| unpickle_list              | 6.88 us                                                                                                           | 6.24 us: 1.10x faster                                                                                                   |
| scimark_sparse_mat_mult    | 6.32 ms                                                                                                           | 5.73 ms: 1.10x faster                                                                                                   |
| regex_compile              | 180 ms                                                                                                            | 165 ms: 1.09x faster                                                                                                    |
| pyflate                    | 620 ms                                                                                                            | 570 ms: 1.09x faster                                                                                                    |
| richards                   | 57.6 ms                                                                                                           | 53.3 ms: 1.08x faster                                                                                                   |
| telco                      | 10.2 ms                                                                                                           | 9.47 ms: 1.08x faster                                                                                                   |
| scimark_sor                | 152 ms                                                                                                            | 141 ms: 1.08x faster                                                                                                    |
| scimark_monte_carlo        | 86.9 ms                                                                                                           | 81.9 ms: 1.06x faster                                                                                                   |
| typing_runtime_protocols   | 214 us                                                                                                            | 202 us: 1.06x faster                                                                                                    |
| deltablue                  | 4.04 ms                                                                                                           | 3.82 ms: 1.06x faster                                                                                                   |
| richards_super             | 66.4 ms                                                                                                           | 63.0 ms: 1.05x faster                                                                                                   |
| comprehensions             | 20.9 us                                                                                                           | 19.9 us: 1.05x faster                                                                                                   |
| scimark_lu                 | 150 ms                                                                                                            | 143 ms: 1.05x faster                                                                                                    |
| regex_v8                   | 30.2 ms                                                                                                           | 28.9 ms: 1.04x faster                                                                                                   |
| json_loads                 | 38.1 us                                                                                                           | 36.6 us: 1.04x faster                                                                                                   |
| bpe_tokeniser              | 5.81 sec                                                                                                          | 5.65 sec: 1.03x faster                                                                                                  |
| crypto_pyaes               | 93.4 ms                                                                                                           | 91.2 ms: 1.02x faster                                                                                                   |
| tomli_loads                | 2.43 sec                                                                                                          | 2.50 sec: 1.03x slower                                                                                                  |
| pprint_pformat             | 1.88 sec                                                                                                          | 1.94 sec: 1.03x slower                                                                                                  |
| logging_silent             | 117 ns                                                                                                            | 121 ns: 1.03x slower                                                                                                    |
| go                         | 156 ms                                                                                                            | 163 ms: 1.04x slower                                                                                                    |
| unpickle                   | 18.5 us                                                                                                           | 19.3 us: 1.04x slower                                                                                                   |
| async_tree_none_tg         | 359 ms                                                                                                            | 375 ms: 1.05x slower                                                                                                    |
| sympy_expand               | 575 ms                                                                                                            | 604 ms: 1.05x slower                                                                                                    |
| regex_effbot               | 3.99 ms                                                                                                           | 4.21 ms: 1.05x slower                                                                                                   |
| asyncio_tcp_ssl            | 2.71 sec                                                                                                          | 2.86 sec: 1.06x slower                                                                                                  |
| xml_etree_process          | 77.6 ms                                                                                                           | 82.0 ms: 1.06x slower                                                                                                   |
| connected_components       | 786 ms                                                                                                            | 832 ms: 1.06x slower                                                                                                    |
| shortest_path              | 869 ms                                                                                                            | 921 ms: 1.06x slower                                                                                                    |
| asyncio_tcp                | 853 ms                                                                                                            | 906 ms: 1.06x slower                                                                                                    |
| async_tree_io              | 854 ms                                                                                                            | 910 ms: 1.07x slower                                                                                                    |
| asyncio_websockets         | 714 ms                                                                                                            | 761 ms: 1.07x slower                                                                                                    |
| k_core                     | 3.99 sec                                                                                                          | 4.27 sec: 1.07x slower                                                                                                  |
| logging_format             | 8.82 us                                                                                                           | 9.44 us: 1.07x slower                                                                                                   |
| mdp                        | 3.46 sec                                                                                                          | 3.71 sec: 1.07x slower                                                                                                  |
| async_tree_io_tg           | 877 ms                                                                                                            | 942 ms: 1.07x slower                                                                                                    |
| django_template            | 44.1 ms                                                                                                           | 47.5 ms: 1.08x slower                                                                                                   |
| sympy_integrate            | 26.6 ms                                                                                                           | 28.7 ms: 1.08x slower                                                                                                   |
| async_tree_cpu_io_mixed    | 664 ms                                                                                                            | 716 ms: 1.08x slower                                                                                                    |
| sqlglot_v2_parse           | 1.70 ms                                                                                                           | 1.85 ms: 1.09x slower                                                                                                   |
| sqlalchemy_imperative      | 21.9 ms                                                                                                           | 23.9 ms: 1.09x slower                                                                                                   |
| pickle_pure_python         | 399 us                                                                                                            | 436 us: 1.09x slower                                                                                                    |
| sqlglot_v2_normalize       | 136 ms                                                                                                            | 148 ms: 1.09x slower                                                                                                    |
| sqlalchemy_declarative     | 173 ms                                                                                                            | 191 ms: 1.10x slower                                                                                                    |
| deepcopy_memo              | 36.3 us                                                                                                           | 40.2 us: 1.11x slower                                                                                                   |
| async_tree_memoization_tg  | 440 ms                                                                                                            | 489 ms: 1.11x slower                                                                                                    |
| xml_etree_iterparse        | 139 ms                                                                                                            | 154 ms: 1.11x slower                                                                                                    |
| pickle_list                | 6.61 us                                                                                                           | 7.37 us: 1.12x slower                                                                                                   |
| sqlglot_v2_optimize        | 68.6 ms                                                                                                           | 76.7 ms: 1.12x slower                                                                                                   |
| float                      | 95.4 ms                                                                                                           | 107 ms: 1.12x slower                                                                                                    |
| pickle                     | 16.4 us                                                                                                           | 18.4 us: 1.12x slower                                                                                                   |
| mako                       | 16.5 ms                                                                                                           | 18.5 ms: 1.12x slower                                                                                                   |
| json                       | 6.57 ms                                                                                                           | 7.38 ms: 1.12x slower                                                                                                   |
| sqlite_synth               | 3.52 us                                                                                                           | 3.96 us: 1.12x slower                                                                                                   |
| python_startup             | 28.8 ms                                                                                                           | 32.5 ms: 1.13x slower                                                                                                   |
| genshi_xml                 | 63.7 ms                                                                                                           | 71.9 ms: 1.13x slower                                                                                                   |
| async_tree_memoization     | 461 ms                                                                                                            | 521 ms: 1.13x slower                                                                                                    |
| async_generators           | 479 ms                                                                                                            | 542 ms: 1.13x slower                                                                                                    |
| unpack_sequence            | 62.7 ns                                                                                                           | 71.3 ns: 1.14x slower                                                                                                   |
| python_startup_no_site     | 17.0 ms                                                                                                           | 19.4 ms: 1.14x slower                                                                                                   |
| pidigits                   | 240 ms                                                                                                            | 274 ms: 1.14x slower                                                                                                    |
| xml_etree_generate         | 113 ms                                                                                                            | 129 ms: 1.14x slower                                                                                                    |
| json_dumps                 | 15.1 ms                                                                                                           | 17.4 ms: 1.15x slower                                                                                                   |
| gc_traversal               | 7.93 ms                                                                                                           | 9.28 ms: 1.17x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg | 665 ms                                                                                                            | 782 ms: 1.18x slower                                                                                                    |
| many_optionals             | 1.18 ms                                                                                                           | 1.39 ms: 1.18x slower                                                                                                   |
| 2to3                       | 404 ms                                                                                                            | 487 ms: 1.21x slower                                                                                                    |
| xml_etree_parse            | 186 ms                                                                                                            | 231 ms: 1.24x slower                                                                                                    |
| create_gc_cycles           | 3.29 ms                                                                                                           | 4.37 ms: 1.33x slower                                                                                                   |
| subparsers                 | 28.4 ms                                                                                                           | 41.7 ms: 1.47x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.04x slower                                                                                                            |

Benchmark hidden because not significant (27): dulwich_log, regex_dna, deepcopy, deepcopy_reduce, raytrace, pickle_dict, async_tree_none, pycparser, generators, docutils, fannkuch, sqlglot_v2_transpile, pathlib, chaos, meteor_contest, unpickle_pure_python, bench_mp_pool, nqueens, pprint_safe_repr, pylint, sympy_str, thrift, sympy_sum, sphinx, logging_simple, genshi_text, bench_thread_pool

- Geometric mean (including insignificant results): 1.026x slower

# HPT report

- Reliability score: 98.27% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x