# Results vs. base

- fork: nascheme
- ref: gh_132380_tp_getattr
- machine: linux-x86_64
- commit hash: 04ccde3
- commit date: 2025-06-05
- overall geometric mean: 1.001x slower
- HPT reliability: 75.11%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 283 ms                                                                | 281 ms: 1.01x faster                                                    |
| docutils       | 2.70 sec                                                              | 2.65 sec: 1.02x faster                                                  |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                            |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_generators           | 373 ms                                                                | 365 ms: 1.02x faster                                                    |
| async_tree_io_tg           | 527 ms                                                                | 519 ms: 1.01x faster                                                    |
| async_tree_io              | 555 ms                                                                | 549 ms: 1.01x faster                                                    |
| asyncio_websockets         | 514 ms                                                                | 518 ms: 1.01x slower                                                    |
| async_tree_memoization     | 312 ms                                                                | 315 ms: 1.01x slower                                                    |
| async_tree_none            | 258 ms                                                                | 260 ms: 1.01x slower                                                    |
| async_tree_cpu_io_mixed_tg | 464 ms                                                                | 471 ms: 1.01x slower                                                    |
| async_tree_cpu_io_mixed    | 489 ms                                                                | 499 ms: 1.02x slower                                                    |
| coroutines                 | 23.1 ms                                                               | 24.0 ms: 1.04x slower                                                   |
| Geometric mean             | (ref)                                                                 | 1.00x slower                                                            |

Benchmark hidden because not significant (2): async_tree_none_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 190 ms                                                                | 189 ms: 1.01x faster                                                    |
| nbody          | 120 ms                                                                | 121 ms: 1.01x slower                                                    |
| float          | 68.8 ms                                                               | 69.7 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 172 ms                                                                | 170 ms: 1.02x faster                                                    |
| regex_effbot   | 2.66 ms                                                               | 2.63 ms: 1.01x faster                                                   |
| regex_compile  | 144 ms                                                                | 143 ms: 1.01x faster                                                    |
| regex_v8       | 20.2 ms                                                               | 20.7 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                                 | 1.00x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pickle_pure_python   | 336 us                                                                | 334 us: 1.01x faster                                                    |
| json_loads           | 31.0 us                                                               | 31.2 us: 1.01x slower                                                   |
| xml_etree_generate   | 94.8 ms                                                               | 95.5 ms: 1.01x slower                                                   |
| xml_etree_parse      | 128 ms                                                                | 130 ms: 1.01x slower                                                    |
| unpickle_pure_python | 229 us                                                                | 231 us: 1.01x slower                                                    |
| tomli_loads          | 2.14 sec                                                              | 2.16 sec: 1.01x slower                                                  |
| Geometric mean       | (ref)                                                                 | 1.00x slower                                                            |

Benchmark hidden because not significant (3): json_dumps, xml_etree_process, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 16.0 ms                                                               | 15.9 ms: 1.01x faster                                                   |
| python_startup_no_site | 9.58 ms                                                               | 9.54 ms: 1.00x faster                                                   |
| Geometric mean         | (ref)                                                                 | 1.00x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 15.8 ms                                                               | 15.6 ms: 1.01x faster                                                   |
| django_template | 39.8 ms                                                               | 40.6 ms: 1.02x slower                                                   |
| Geometric mean  | (ref)                                                                 | 1.00x slower                                                            |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea | bm-20250605-vultr-x86_64-nascheme-gh_132380_tp_getattr-3.15.0a0-04ccde3 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| meteor_contest             | 124 ms                                                                | 120 ms: 1.04x faster                                                    |
| subparsers                 | 28.5 ms                                                               | 27.6 ms: 1.03x faster                                                   |
| async_generators           | 373 ms                                                                | 365 ms: 1.02x faster                                                    |
| docutils                   | 2.70 sec                                                              | 2.65 sec: 1.02x faster                                                  |
| many_optionals             | 1.14 ms                                                               | 1.12 ms: 1.02x faster                                                   |
| fannkuch                   | 465 ms                                                                | 457 ms: 1.02x faster                                                    |
| pprint_pformat             | 1.82 sec                                                              | 1.79 sec: 1.02x faster                                                  |
| regex_dna                  | 172 ms                                                                | 170 ms: 1.02x faster                                                    |
| async_tree_io_tg           | 527 ms                                                                | 519 ms: 1.01x faster                                                    |
| pprint_safe_repr           | 878 ms                                                                | 866 ms: 1.01x faster                                                    |
| sqlite_synth               | 2.07 us                                                               | 2.04 us: 1.01x faster                                                   |
| deepcopy                   | 295 us                                                                | 291 us: 1.01x faster                                                    |
| regex_effbot               | 2.66 ms                                                               | 2.63 ms: 1.01x faster                                                   |
| bench_mp_pool              | 103 ms                                                                | 102 ms: 1.01x faster                                                    |
| mako                       | 15.8 ms                                                               | 15.6 ms: 1.01x faster                                                   |
| logging_simple             | 7.71 us                                                               | 7.63 us: 1.01x faster                                                   |
| async_tree_io              | 555 ms                                                                | 549 ms: 1.01x faster                                                    |
| pyflate                    | 470 ms                                                                | 466 ms: 1.01x faster                                                    |
| regex_compile              | 144 ms                                                                | 143 ms: 1.01x faster                                                    |
| pathlib                    | 19.6 ms                                                               | 19.4 ms: 1.01x faster                                                   |
| sympy_integrate            | 22.1 ms                                                               | 21.9 ms: 1.01x faster                                                   |
| logging_format             | 8.75 us                                                               | 8.69 us: 1.01x faster                                                   |
| pickle_pure_python         | 336 us                                                                | 334 us: 1.01x faster                                                    |
| dulwich_log                | 71.4 ms                                                               | 70.9 ms: 1.01x faster                                                   |
| sympy_sum                  | 181 ms                                                                | 180 ms: 1.01x faster                                                    |
| 2to3                       | 283 ms                                                                | 281 ms: 1.01x faster                                                    |
| pidigits                   | 190 ms                                                                | 189 ms: 1.01x faster                                                    |
| gc_traversal               | 1.90 ms                                                               | 1.89 ms: 1.01x faster                                                   |
| python_startup             | 16.0 ms                                                               | 15.9 ms: 1.01x faster                                                   |
| python_startup_no_site     | 9.58 ms                                                               | 9.54 ms: 1.00x faster                                                   |
| bpe_tokeniser              | 4.37 sec                                                              | 4.36 sec: 1.00x faster                                                  |
| deepcopy_memo              | 34.8 us                                                               | 34.7 us: 1.00x faster                                                   |
| richards                   | 50.8 ms                                                               | 51.0 ms: 1.00x slower                                                   |
| sympy_expand               | 528 ms                                                                | 531 ms: 1.01x slower                                                    |
| logging_silent             | 524 ns                                                                | 528 ns: 1.01x slower                                                    |
| sqlglot_v2_normalize       | 113 ms                                                                | 114 ms: 1.01x slower                                                    |
| json_loads                 | 31.0 us                                                               | 31.2 us: 1.01x slower                                                   |
| hexiom                     | 6.30 ms                                                               | 6.35 ms: 1.01x slower                                                   |
| asyncio_websockets         | 514 ms                                                                | 518 ms: 1.01x slower                                                    |
| nbody                      | 120 ms                                                                | 121 ms: 1.01x slower                                                    |
| async_tree_memoization     | 312 ms                                                                | 315 ms: 1.01x slower                                                    |
| xml_etree_generate         | 94.8 ms                                                               | 95.5 ms: 1.01x slower                                                   |
| async_tree_none            | 258 ms                                                                | 260 ms: 1.01x slower                                                    |
| richards_super             | 58.2 ms                                                               | 58.7 ms: 1.01x slower                                                   |
| xml_etree_parse            | 128 ms                                                                | 130 ms: 1.01x slower                                                    |
| unpickle_pure_python       | 229 us                                                                | 231 us: 1.01x slower                                                    |
| nqueens                    | 84.6 ms                                                               | 85.4 ms: 1.01x slower                                                   |
| deepcopy_reduce            | 2.97 us                                                               | 3.00 us: 1.01x slower                                                   |
| scimark_sor                | 122 ms                                                                | 123 ms: 1.01x slower                                                    |
| tomli_loads                | 2.14 sec                                                              | 2.16 sec: 1.01x slower                                                  |
| float                      | 68.8 ms                                                               | 69.7 ms: 1.01x slower                                                   |
| async_tree_cpu_io_mixed_tg | 464 ms                                                                | 471 ms: 1.01x slower                                                    |
| chaos                      | 61.9 ms                                                               | 62.9 ms: 1.02x slower                                                   |
| sqlglot_v2_optimize        | 56.4 ms                                                               | 57.3 ms: 1.02x slower                                                   |
| generators                 | 31.1 ms                                                               | 31.6 ms: 1.02x slower                                                   |
| django_template            | 39.8 ms                                                               | 40.6 ms: 1.02x slower                                                   |
| async_tree_cpu_io_mixed    | 489 ms                                                                | 499 ms: 1.02x slower                                                    |
| regex_v8                   | 20.2 ms                                                               | 20.7 ms: 1.03x slower                                                   |
| scimark_lu                 | 128 ms                                                                | 131 ms: 1.03x slower                                                    |
| spectral_norm              | 110 ms                                                                | 114 ms: 1.04x slower                                                    |
| scimark_fft                | 356 ms                                                                | 370 ms: 1.04x slower                                                    |
| coroutines                 | 23.1 ms                                                               | 24.0 ms: 1.04x slower                                                   |
| scimark_sparse_mat_mult    | 5.17 ms                                                               | 5.56 ms: 1.07x slower                                                   |
| Geometric mean             | (ref)                                                                 | 1.00x slower                                                            |

Benchmark hidden because not significant (31): sqlglot_v2_transpile, pylint, html5lib, shortest_path, connected_components, sphinx, telco, typing_runtime_protocols, async_tree_none_tg, pycparser, create_gc_cycles, json_dumps, json, thrift, bench_thread_pool, crypto_pyaes, go, comprehensions, k_core, xml_etree_process, xml_etree_iterparse, async_tree_memoization_tg, raytrace, genshi_xml, scimark_monte_carlo, deltablue, sympy_str, sqlglot_v2_parse, mdp, genshi_text, coverage

- Geometric mean (including insignificant results): 1.001x slower

# HPT report

- Reliability score: 75.11% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x