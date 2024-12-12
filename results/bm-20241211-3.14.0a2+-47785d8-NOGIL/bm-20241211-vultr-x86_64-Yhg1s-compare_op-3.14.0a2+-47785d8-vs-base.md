# Results vs. base

- fork: Yhg1s
- ref: compare_op
- machine: linux-x86_64
- commit hash: 47785d8
- commit date: 2024-12-11
- overall geometric mean: 1.006x faster
- HPT reliability: 99.80%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241211-vultr-x86_64-python-359389ed51aecc107681-3.14.0a2+-359389e | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 368 ms                                                                 | 364 ms: 1.01x faster                                        |
| html5lib       | 96.9 ms                                                                | 95.2 ms: 1.02x faster                                       |
| sphinx         | 1.19 sec                                                               | 1.18 sec: 1.00x faster                                      |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20241211-vultr-x86_64-python-359389ed51aecc107681-3.14.0a2+-359389e | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| coroutines       | 24.7 ms                                                                | 24.4 ms: 1.01x faster                                       |
| async_tree_io_tg | 828 ms                                                                 | 818 ms: 1.01x faster                                        |
| async_generators | 454 ms                                                                 | 462 ms: 1.02x slower                                        |
| Geometric mean   | (ref)                                                                  | 1.00x faster                                                |

Benchmark hidden because not significant (8): async_tree_none_tg, asyncio_websockets, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_none, async_tree_io, async_tree_memoization, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241211-vultr-x86_64-python-359389ed51aecc107681-3.14.0a2+-359389e | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| float          | 137 ms                                                                 | 138 ms: 1.01x slower                                        |
| nbody          | 128 ms                                                                 | 130 ms: 1.01x slower                                        |
| pidigits       | 181 ms                                                                 | 184 ms: 1.01x slower                                        |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241211-vultr-x86_64-python-359389ed51aecc107681-3.14.0a2+-359389e | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_dna      | 184 ms                                                                 | 180 ms: 1.02x faster                                        |
| regex_effbot   | 2.75 ms                                                                | 2.81 ms: 1.02x slower                                       |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                |

Benchmark hidden because not significant (2): regex_v8, regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241211-vultr-x86_64-python-359389ed51aecc107681-3.14.0a2+-359389e | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| tomli_loads          | 2.67 sec                                                               | 2.47 sec: 1.08x faster                                      |
| pickle_pure_python   | 515 us                                                                 | 497 us: 1.04x faster                                        |
| json_dumps           | 14.4 ms                                                                | 14.2 ms: 1.01x faster                                       |
| unpickle_pure_python | 331 us                                                                 | 329 us: 1.01x faster                                        |
| xml_etree_process    | 78.1 ms                                                                | 78.6 ms: 1.01x slower                                       |
| xml_etree_iterparse  | 89.7 ms                                                                | 90.3 ms: 1.01x slower                                       |
| xml_etree_parse      | 129 ms                                                                 | 130 ms: 1.01x slower                                        |
| xml_etree_generate   | 97.6 ms                                                                | 98.9 ms: 1.01x slower                                       |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241211-vultr-x86_64-python-359389ed51aecc107681-3.14.0a2+-359389e | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup_no_site | 10.3 ms                                                                | 10.2 ms: 1.01x faster                                       |
| python_startup         | 17.5 ms                                                                | 17.4 ms: 1.01x faster                                       |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241211-vultr-x86_64-python-359389ed51aecc107681-3.14.0a2+-359389e | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| genshi_text     | 32.3 ms                                                                | 31.4 ms: 1.03x faster                                       |
| django_template | 50.8 ms                                                                | 50.1 ms: 1.01x faster                                       |
| genshi_xml      | 64.7 ms                                                                | 64.3 ms: 1.01x faster                                       |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                | bm-20241211-vultr-x86_64-python-359389ed51aecc107681-3.14.0a2+-359389e | bm-20241211-vultr-x86_64-Yhg1s-compare_op-3.14.0a2+-47785d8 |
|--------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| gc_traversal             | 3.53 ms                                                                | 3.18 ms: 1.11x faster                                       |
| tomli_loads              | 2.67 sec                                                               | 2.47 sec: 1.08x faster                                      |
| scimark_sor              | 236 ms                                                                 | 221 ms: 1.06x faster                                        |
| mdp                      | 2.88 sec                                                               | 2.76 sec: 1.05x faster                                      |
| pyflate                  | 694 ms                                                                 | 666 ms: 1.04x faster                                        |
| pickle_pure_python       | 515 us                                                                 | 497 us: 1.04x faster                                        |
| fannkuch                 | 496 ms                                                                 | 479 ms: 1.04x faster                                        |
| genshi_text              | 32.3 ms                                                                | 31.4 ms: 1.03x faster                                       |
| regex_dna                | 184 ms                                                                 | 180 ms: 1.02x faster                                        |
| logging_format           | 11.9 us                                                                | 11.7 us: 1.02x faster                                       |
| create_gc_cycles         | 1.86 ms                                                                | 1.82 ms: 1.02x faster                                       |
| coverage                 | 100 ms                                                                 | 98.2 ms: 1.02x faster                                       |
| scimark_sparse_mat_mult  | 6.01 ms                                                                | 5.88 ms: 1.02x faster                                       |
| pycparser                | 1.55 sec                                                               | 1.51 sec: 1.02x faster                                      |
| scimark_fft              | 405 ms                                                                 | 396 ms: 1.02x faster                                        |
| hexiom                   | 9.75 ms                                                                | 9.55 ms: 1.02x faster                                       |
| scimark_monte_carlo      | 118 ms                                                                 | 116 ms: 1.02x faster                                        |
| html5lib                 | 96.9 ms                                                                | 95.2 ms: 1.02x faster                                       |
| spectral_norm            | 124 ms                                                                 | 122 ms: 1.01x faster                                        |
| json_dumps               | 14.4 ms                                                                | 14.2 ms: 1.01x faster                                       |
| telco                    | 8.78 ms                                                                | 8.66 ms: 1.01x faster                                       |
| nqueens                  | 98.2 ms                                                                | 96.9 ms: 1.01x faster                                       |
| django_template          | 50.8 ms                                                                | 50.1 ms: 1.01x faster                                       |
| logging_simple           | 10.8 us                                                                | 10.7 us: 1.01x faster                                       |
| sympy_integrate          | 29.6 ms                                                                | 29.2 ms: 1.01x faster                                       |
| coroutines               | 24.7 ms                                                                | 24.4 ms: 1.01x faster                                       |
| async_tree_io_tg         | 828 ms                                                                 | 818 ms: 1.01x faster                                        |
| 2to3                     | 368 ms                                                                 | 364 ms: 1.01x faster                                        |
| sqlite_synth             | 2.30 us                                                                | 2.27 us: 1.01x faster                                       |
| sympy_expand             | 954 ms                                                                 | 945 ms: 1.01x faster                                        |
| shortest_path            | 554 ms                                                                 | 549 ms: 1.01x faster                                        |
| sympy_str                | 475 ms                                                                 | 472 ms: 1.01x faster                                        |
| genshi_xml               | 64.7 ms                                                                | 64.3 ms: 1.01x faster                                       |
| connected_components     | 502 ms                                                                 | 499 ms: 1.01x faster                                        |
| pprint_safe_repr         | 977 ms                                                                 | 970 ms: 1.01x faster                                        |
| dulwich_log              | 95.7 ms                                                                | 95.1 ms: 1.01x faster                                       |
| bench_mp_pool            | 109 ms                                                                 | 108 ms: 1.01x faster                                        |
| python_startup_no_site   | 10.3 ms                                                                | 10.2 ms: 1.01x faster                                       |
| python_startup           | 17.5 ms                                                                | 17.4 ms: 1.01x faster                                       |
| unpickle_pure_python     | 331 us                                                                 | 329 us: 1.01x faster                                        |
| sphinx                   | 1.19 sec                                                               | 1.18 sec: 1.00x faster                                      |
| sqlalchemy_declarative   | 204 ms                                                                 | 203 ms: 1.00x faster                                        |
| chaos                    | 105 ms                                                                 | 104 ms: 1.00x faster                                        |
| go                       | 267 ms                                                                 | 266 ms: 1.00x faster                                        |
| xml_etree_process        | 78.1 ms                                                                | 78.6 ms: 1.01x slower                                       |
| float                    | 137 ms                                                                 | 138 ms: 1.01x slower                                        |
| deepcopy_reduce          | 3.49 us                                                                | 3.51 us: 1.01x slower                                       |
| xml_etree_iterparse      | 89.7 ms                                                                | 90.3 ms: 1.01x slower                                       |
| json                     | 5.07 ms                                                                | 5.11 ms: 1.01x slower                                       |
| pathlib                  | 20.1 ms                                                                | 20.3 ms: 1.01x slower                                       |
| deepcopy_memo            | 40.0 us                                                                | 40.4 us: 1.01x slower                                       |
| xml_etree_parse          | 129 ms                                                                 | 130 ms: 1.01x slower                                        |
| deepcopy                 | 327 us                                                                 | 331 us: 1.01x slower                                        |
| xml_etree_generate       | 97.6 ms                                                                | 98.9 ms: 1.01x slower                                       |
| nbody                    | 128 ms                                                                 | 130 ms: 1.01x slower                                        |
| pidigits                 | 181 ms                                                                 | 184 ms: 1.01x slower                                        |
| async_generators         | 454 ms                                                                 | 462 ms: 1.02x slower                                        |
| regex_effbot             | 2.75 ms                                                                | 2.81 ms: 1.02x slower                                       |
| richards                 | 76.6 ms                                                                | 78.2 ms: 1.02x slower                                       |
| typing_runtime_protocols | 202 us                                                                 | 208 us: 1.03x slower                                        |
| scimark_lu               | 181 ms                                                                 | 186 ms: 1.03x slower                                        |
| generators               | 38.3 ms                                                                | 39.3 ms: 1.03x slower                                       |
| raytrace                 | 544 ms                                                                 | 559 ms: 1.03x slower                                        |
| richards_super           | 86.0 ms                                                                | 88.5 ms: 1.03x slower                                       |
| logging_silent           | 183 ns                                                                 | 188 ns: 1.03x slower                                        |
| Geometric mean           | (ref)                                                                  | 1.01x faster                                                |

Benchmark hidden because not significant (31): meteor_contest, pylint, k_core, pprint_pformat, sqlalchemy_imperative, sqlglot_transpile, subparsers, async_tree_none_tg, asyncio_websockets, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, comprehensions, json_loads, thrift, async_tree_none, bpe_tokeniser, sympy_sum, deltablue, regex_v8, mako, sqlglot_normalize, bench_thread_pool, crypto_pyaes, many_optionals, async_tree_io, docutils, regex_compile, async_tree_memoization, sqlglot_parse, sqlglot_optimize, async_tree_memoization_tg

- Geometric mean (including insignificant results): 1.006x faster

# HPT report

- Reliability score: 99.80% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x