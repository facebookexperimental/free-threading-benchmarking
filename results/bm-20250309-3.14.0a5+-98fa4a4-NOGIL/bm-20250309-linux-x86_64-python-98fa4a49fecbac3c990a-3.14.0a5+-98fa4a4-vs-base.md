# Results vs. base

- fork: python
- ref: 98fa4a49fecbac3c990a
- machine: linux-x86_64
- commit hash: 98fa4a4
- commit date: 2025-03-09
- overall geometric mean: 1.117x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250309-3.14.0a5+-98fa4a4/bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json | results/bm-20250309-3.14.0a5+-98fa4a4-NOGIL/bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 441 ms                                                                                                            | 553 ms: 1.25x slower                                                                                                    |
| docutils       | 3.67 sec                                                                                                          | 4.18 sec: 1.14x slower                                                                                                  |
| html5lib       | 84.6 ms                                                                                                           | 98.4 ms: 1.16x slower                                                                                                   |
| sphinx         | 1.42 sec                                                                                                          | 1.66 sec: 1.17x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.18x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | results/bm-20250309-3.14.0a5+-98fa4a4/bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json | results/bm-20250309-3.14.0a5+-98fa4a4-NOGIL/bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json |
|-------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg        | 904 ms                                                                                                            | 772 ms: 1.17x faster                                                                                                    |
| async_tree_cpu_io_mixed | 677 ms                                                                                                            | 712 ms: 1.05x slower                                                                                                    |
| asyncio_websockets      | 719 ms                                                                                                            | 763 ms: 1.06x slower                                                                                                    |
| async_tree_memoization  | 472 ms                                                                                                            | 509 ms: 1.08x slower                                                                                                    |
| async_generators        | 505 ms                                                                                                            | 577 ms: 1.14x slower                                                                                                    |
| Geometric mean          | (ref)                                                                                                             | 1.01x slower                                                                                                            |

Benchmark hidden because not significant (6): async_tree_io, async_tree_none_tg, coroutines, async_tree_cpu_io_mixed_tg, async_tree_none, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250309-3.14.0a5+-98fa4a4/bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json | results/bm-20250309-3.14.0a5+-98fa4a4-NOGIL/bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| float          | 97.8 ms                                                                                                           | 103 ms: 1.05x slower                                                                                                    |
| nbody          | 130 ms                                                                                                            | 181 ms: 1.39x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.14x slower                                                                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250309-3.14.0a5+-98fa4a4/bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json | results/bm-20250309-3.14.0a5+-98fa4a4-NOGIL/bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_compile  | 170 ms                                                                                                            | 198 ms: 1.17x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.04x slower                                                                                                            |

Benchmark hidden because not significant (3): regex_v8, regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250309-3.14.0a5+-98fa4a4/bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json | results/bm-20250309-3.14.0a5+-98fa4a4-NOGIL/bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 151 ms                                                                                                            | 132 ms: 1.14x faster                                                                                                    |
| xml_etree_parse      | 224 ms                                                                                                            | 205 ms: 1.09x faster                                                                                                    |
| json_loads           | 39.8 us                                                                                                           | 42.8 us: 1.08x slower                                                                                                   |
| pickle_pure_python   | 460 us                                                                                                            | 500 us: 1.09x slower                                                                                                    |
| xml_etree_generate   | 120 ms                                                                                                            | 132 ms: 1.10x slower                                                                                                    |
| xml_etree_process    | 86.0 ms                                                                                                           | 96.3 ms: 1.12x slower                                                                                                   |
| unpickle_pure_python | 298 us                                                                                                            | 338 us: 1.14x slower                                                                                                    |
| tomli_loads          | 2.60 sec                                                                                                          | 3.05 sec: 1.17x slower                                                                                                  |
| json_dumps           | 16.3 ms                                                                                                           | 19.4 ms: 1.19x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.07x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250309-3.14.0a5+-98fa4a4/bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json | results/bm-20250309-3.14.0a5+-98fa4a4-NOGIL/bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 29.0 ms                                                                                                           | 35.5 ms: 1.22x slower                                                                                                   |
| python_startup_no_site | 19.0 ms                                                                                                           | 23.9 ms: 1.26x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.24x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250309-3.14.0a5+-98fa4a4/bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json | results/bm-20250309-3.14.0a5+-98fa4a4-NOGIL/bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 46.2 ms                                                                                                           | 54.7 ms: 1.19x slower                                                                                                   |
| genshi_xml      | 66.9 ms                                                                                                           | 86.9 ms: 1.30x slower                                                                                                   |
| genshi_text     | 29.9 ms                                                                                                           | 39.5 ms: 1.32x slower                                                                                                   |
| mako            | 16.0 ms                                                                                                           | 23.6 ms: 1.47x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.32x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                | results/bm-20250309-3.14.0a5+-98fa4a4/bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json | results/bm-20250309-3.14.0a5+-98fa4a4-NOGIL/bm-20250309-linux-x86_64-python-98fa4a49fecbac3c990a-3.14.0a5+-98fa4a4.json |
|--------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal             | 8.12 ms                                                                                                           | 4.03 ms: 2.02x faster                                                                                                   |
| create_gc_cycles         | 3.64 ms                                                                                                           | 2.52 ms: 1.45x faster                                                                                                   |
| async_tree_io_tg         | 904 ms                                                                                                            | 772 ms: 1.17x faster                                                                                                    |
| xml_etree_iterparse      | 151 ms                                                                                                            | 132 ms: 1.14x faster                                                                                                    |
| xml_etree_parse          | 224 ms                                                                                                            | 205 ms: 1.09x faster                                                                                                    |
| pycparser                | 1.68 sec                                                                                                          | 1.56 sec: 1.08x faster                                                                                                  |
| bench_mp_pool            | 93.1 ms                                                                                                           | 87.1 ms: 1.07x faster                                                                                                   |
| json                     | 7.51 ms                                                                                                           | 7.04 ms: 1.07x faster                                                                                                   |
| float                    | 97.8 ms                                                                                                           | 103 ms: 1.05x slower                                                                                                    |
| async_tree_cpu_io_mixed  | 677 ms                                                                                                            | 712 ms: 1.05x slower                                                                                                    |
| asyncio_websockets       | 719 ms                                                                                                            | 763 ms: 1.06x slower                                                                                                    |
| async_tree_memoization   | 472 ms                                                                                                            | 509 ms: 1.08x slower                                                                                                    |
| json_loads               | 39.8 us                                                                                                           | 42.8 us: 1.08x slower                                                                                                   |
| k_core                   | 4.09 sec                                                                                                          | 4.41 sec: 1.08x slower                                                                                                  |
| scimark_sor              | 155 ms                                                                                                            | 168 ms: 1.09x slower                                                                                                    |
| pickle_pure_python       | 460 us                                                                                                            | 500 us: 1.09x slower                                                                                                    |
| xml_etree_generate       | 120 ms                                                                                                            | 132 ms: 1.10x slower                                                                                                    |
| xml_etree_process        | 86.0 ms                                                                                                           | 96.3 ms: 1.12x slower                                                                                                   |
| telco                    | 11.3 ms                                                                                                           | 12.7 ms: 1.12x slower                                                                                                   |
| dulwich_log              | 88.3 ms                                                                                                           | 99.6 ms: 1.13x slower                                                                                                   |
| unpickle_pure_python     | 298 us                                                                                                            | 338 us: 1.14x slower                                                                                                    |
| sympy_expand             | 631 ms                                                                                                            | 717 ms: 1.14x slower                                                                                                    |
| sympy_sum                | 217 ms                                                                                                            | 247 ms: 1.14x slower                                                                                                    |
| docutils                 | 3.67 sec                                                                                                          | 4.18 sec: 1.14x slower                                                                                                  |
| connected_components     | 824 ms                                                                                                            | 941 ms: 1.14x slower                                                                                                    |
| async_generators         | 505 ms                                                                                                            | 577 ms: 1.14x slower                                                                                                    |
| scimark_lu               | 157 ms                                                                                                            | 180 ms: 1.15x slower                                                                                                    |
| logging_silent           | 129 ns                                                                                                            | 148 ns: 1.15x slower                                                                                                    |
| deepcopy                 | 372 us                                                                                                            | 430 us: 1.16x slower                                                                                                    |
| sqlglot_optimize         | 71.8 ms                                                                                                           | 83.0 ms: 1.16x slower                                                                                                   |
| thrift                   | 1.04 ms                                                                                                           | 1.20 ms: 1.16x slower                                                                                                   |
| sympy_integrate          | 29.3 ms                                                                                                           | 34.0 ms: 1.16x slower                                                                                                   |
| html5lib                 | 84.6 ms                                                                                                           | 98.4 ms: 1.16x slower                                                                                                   |
| sphinx                   | 1.42 sec                                                                                                          | 1.66 sec: 1.17x slower                                                                                                  |
| regex_compile            | 170 ms                                                                                                            | 198 ms: 1.17x slower                                                                                                    |
| generators               | 39.0 ms                                                                                                           | 45.6 ms: 1.17x slower                                                                                                   |
| shortest_path            | 901 ms                                                                                                            | 1.05 sec: 1.17x slower                                                                                                  |
| tomli_loads              | 2.60 sec                                                                                                          | 3.05 sec: 1.17x slower                                                                                                  |
| pylint                   | 388 ms                                                                                                            | 457 ms: 1.18x slower                                                                                                    |
| many_optionals           | 1.28 ms                                                                                                           | 1.51 ms: 1.18x slower                                                                                                   |
| django_template          | 46.2 ms                                                                                                           | 54.7 ms: 1.19x slower                                                                                                   |
| go                       | 150 ms                                                                                                            | 178 ms: 1.19x slower                                                                                                    |
| json_dumps               | 16.3 ms                                                                                                           | 19.4 ms: 1.19x slower                                                                                                   |
| sqlalchemy_imperative    | 25.0 ms                                                                                                           | 29.9 ms: 1.20x slower                                                                                                   |
| deepcopy_reduce          | 3.58 us                                                                                                           | 4.28 us: 1.20x slower                                                                                                   |
| pprint_pformat           | 1.90 sec                                                                                                          | 2.28 sec: 1.20x slower                                                                                                  |
| subparsers               | 29.7 ms                                                                                                           | 35.9 ms: 1.21x slower                                                                                                   |
| mdp                      | 3.51 sec                                                                                                          | 4.30 sec: 1.22x slower                                                                                                  |
| fannkuch                 | 547 ms                                                                                                            | 669 ms: 1.22x slower                                                                                                    |
| python_startup           | 29.0 ms                                                                                                           | 35.5 ms: 1.22x slower                                                                                                   |
| sympy_str                | 353 ms                                                                                                            | 435 ms: 1.23x slower                                                                                                    |
| hexiom                   | 8.07 ms                                                                                                           | 9.93 ms: 1.23x slower                                                                                                   |
| logging_simple           | 7.71 us                                                                                                           | 9.51 us: 1.23x slower                                                                                                   |
| spectral_norm            | 121 ms                                                                                                            | 150 ms: 1.24x slower                                                                                                    |
| crypto_pyaes             | 94.6 ms                                                                                                           | 118 ms: 1.24x slower                                                                                                    |
| sqlglot_parse            | 1.75 ms                                                                                                           | 2.18 ms: 1.25x slower                                                                                                   |
| 2to3                     | 441 ms                                                                                                            | 553 ms: 1.25x slower                                                                                                    |
| pprint_safe_repr         | 901 ms                                                                                                            | 1.13 sec: 1.26x slower                                                                                                  |
| python_startup_no_site   | 19.0 ms                                                                                                           | 23.9 ms: 1.26x slower                                                                                                   |
| logging_format           | 8.28 us                                                                                                           | 10.4 us: 1.26x slower                                                                                                   |
| richards                 | 55.8 ms                                                                                                           | 70.4 ms: 1.26x slower                                                                                                   |
| coverage                 | 116 ms                                                                                                            | 147 ms: 1.27x slower                                                                                                    |
| sqlglot_transpile        | 2.10 ms                                                                                                           | 2.68 ms: 1.27x slower                                                                                                   |
| scimark_sparse_mat_mult  | 6.70 ms                                                                                                           | 8.54 ms: 1.27x slower                                                                                                   |
| pyflate                  | 612 ms                                                                                                            | 780 ms: 1.27x slower                                                                                                    |
| deltablue                | 4.17 ms                                                                                                           | 5.31 ms: 1.27x slower                                                                                                   |
| raytrace                 | 350 ms                                                                                                            | 446 ms: 1.28x slower                                                                                                    |
| scimark_fft              | 442 ms                                                                                                            | 565 ms: 1.28x slower                                                                                                    |
| deepcopy_memo            | 38.9 us                                                                                                           | 49.9 us: 1.28x slower                                                                                                   |
| richards_super           | 72.0 ms                                                                                                           | 92.8 ms: 1.29x slower                                                                                                   |
| sqlalchemy_declarative   | 170 ms                                                                                                            | 221 ms: 1.30x slower                                                                                                    |
| genshi_xml               | 66.9 ms                                                                                                           | 86.9 ms: 1.30x slower                                                                                                   |
| comprehensions           | 21.7 us                                                                                                           | 28.2 us: 1.30x slower                                                                                                   |
| nqueens                  | 109 ms                                                                                                            | 142 ms: 1.31x slower                                                                                                    |
| chaos                    | 73.8 ms                                                                                                           | 96.8 ms: 1.31x slower                                                                                                   |
| typing_runtime_protocols | 202 us                                                                                                            | 267 us: 1.32x slower                                                                                                    |
| genshi_text              | 29.9 ms                                                                                                           | 39.5 ms: 1.32x slower                                                                                                   |
| scimark_monte_carlo      | 87.4 ms                                                                                                           | 116 ms: 1.33x slower                                                                                                    |
| bpe_tokeniser            | 5.69 sec                                                                                                          | 7.55 sec: 1.33x slower                                                                                                  |
| bench_thread_pool        | 3.34 ms                                                                                                           | 4.46 ms: 1.33x slower                                                                                                   |
| meteor_contest           | 136 ms                                                                                                            | 185 ms: 1.36x slower                                                                                                    |
| nbody                    | 130 ms                                                                                                            | 181 ms: 1.39x slower                                                                                                    |
| mako                     | 16.0 ms                                                                                                           | 23.6 ms: 1.47x slower                                                                                                   |
| Geometric mean           | (ref)                                                                                                             | 1.14x slower                                                                                                            |

Benchmark hidden because not significant (13): async_tree_io, regex_v8, async_tree_none_tg, coroutines, pathlib, sqlite_synth, regex_effbot, async_tree_cpu_io_mixed_tg, pidigits, async_tree_none, regex_dna, async_tree_memoization_tg, sqlglot_normalize

- Geometric mean (including insignificant results): 1.117x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.20x