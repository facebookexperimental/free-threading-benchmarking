# Results vs. base

- fork: python
- ref: 71ede1142ddad2d31cc9
- machine: linux-x86_64
- commit hash: 71ede11
- commit date: 2024-11-26
- overall geometric mean: 1.267x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.23x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20241126-3.14.0a2+-71ede11/bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json | results/bm-20241126-3.14.0a2+-71ede11-NOGIL/bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 470 ms                                                                                                            | 647 ms: 1.38x slower                                                                                                    |
| docutils       | 3.76 sec                                                                                                          | 4.75 sec: 1.27x slower                                                                                                  |
| html5lib       | 84.0 ms                                                                                                           | 136 ms: 1.62x slower                                                                                                    |
| sphinx         | 1.53 sec                                                                                                          | 1.83 sec: 1.19x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.35x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | results/bm-20241126-3.14.0a2+-71ede11/bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json | results/bm-20241126-3.14.0a2+-71ede11-NOGIL/bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json |
|-------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg        | 1.43 sec                                                                                                          | 1.13 sec: 1.26x faster                                                                                                  |
| async_tree_io           | 1.40 sec                                                                                                          | 1.15 sec: 1.22x faster                                                                                                  |
| asyncio_websockets      | 751 ms                                                                                                            | 778 ms: 1.04x slower                                                                                                    |
| async_tree_memoization  | 652 ms                                                                                                            | 684 ms: 1.05x slower                                                                                                    |
| async_tree_cpu_io_mixed | 804 ms                                                                                                            | 883 ms: 1.10x slower                                                                                                    |
| async_tree_none         | 493 ms                                                                                                            | 557 ms: 1.13x slower                                                                                                    |
| coroutines              | 31.9 ms                                                                                                           | 38.7 ms: 1.21x slower                                                                                                   |
| async_generators        | 562 ms                                                                                                            | 711 ms: 1.27x slower                                                                                                    |
| Geometric mean          | (ref)                                                                                                             | 1.03x slower                                                                                                            |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20241126-3.14.0a2+-71ede11/bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json | results/bm-20241126-3.14.0a2+-71ede11-NOGIL/bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 255 ms                                                                                                            | 237 ms: 1.08x faster                                                                                                    |
| float          | 117 ms                                                                                                            | 172 ms: 1.48x slower                                                                                                    |
| nbody          | 118 ms                                                                                                            | 217 ms: 1.84x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.36x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20241126-3.14.0a2+-71ede11/bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json | results/bm-20241126-3.14.0a2+-71ede11-NOGIL/bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 33.3 ms                                                                                                           | 34.4 ms: 1.03x slower                                                                                                   |
| regex_effbot   | 4.32 ms                                                                                                           | 4.54 ms: 1.05x slower                                                                                                   |
| regex_compile  | 172 ms                                                                                                            | 253 ms: 1.47x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20241126-3.14.0a2+-71ede11/bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json | results/bm-20241126-3.14.0a2+-71ede11-NOGIL/bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| json_loads           | 34.1 us                                                                                                           | 37.4 us: 1.09x slower                                                                                                   |
| xml_etree_parse      | 199 ms                                                                                                            | 238 ms: 1.19x slower                                                                                                    |
| json_dumps           | 14.7 ms                                                                                                           | 18.8 ms: 1.28x slower                                                                                                   |
| xml_etree_generate   | 116 ms                                                                                                            | 150 ms: 1.29x slower                                                                                                    |
| tomli_loads          | 2.65 sec                                                                                                          | 3.91 sec: 1.47x slower                                                                                                  |
| xml_etree_process    | 82.3 ms                                                                                                           | 133 ms: 1.61x slower                                                                                                    |
| unpickle_pure_python | 287 us                                                                                                            | 479 us: 1.67x slower                                                                                                    |
| pickle_pure_python   | 435 us                                                                                                            | 756 us: 1.74x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.35x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20241126-3.14.0a2+-71ede11/bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json | results/bm-20241126-3.14.0a2+-71ede11-NOGIL/bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 27.9 ms                                                                                                           | 37.0 ms: 1.33x slower                                                                                                   |
| python_startup_no_site | 15.5 ms                                                                                                           | 23.8 ms: 1.53x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.43x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20241126-3.14.0a2+-71ede11/bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json | results/bm-20241126-3.14.0a2+-71ede11-NOGIL/bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_text     | 31.0 ms                                                                                                           | 47.4 ms: 1.53x slower                                                                                                   |
| genshi_xml      | 65.8 ms                                                                                                           | 102 ms: 1.55x slower                                                                                                    |
| django_template | 46.4 ms                                                                                                           | 72.1 ms: 1.55x slower                                                                                                   |
| mako            | 17.2 ms                                                                                                           | 32.2 ms: 1.87x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.62x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                | results/bm-20241126-3.14.0a2+-71ede11/bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json | results/bm-20241126-3.14.0a2+-71ede11-NOGIL/bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json |
|--------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg         | 1.43 sec                                                                                                          | 1.13 sec: 1.26x faster                                                                                                  |
| async_tree_io            | 1.40 sec                                                                                                          | 1.15 sec: 1.22x faster                                                                                                  |
| gc_traversal             | 7.58 ms                                                                                                           | 6.47 ms: 1.17x faster                                                                                                   |
| k_core                   | 5.21 sec                                                                                                          | 4.66 sec: 1.12x faster                                                                                                  |
| create_gc_cycles         | 3.96 ms                                                                                                           | 3.66 ms: 1.08x faster                                                                                                   |
| pidigits                 | 255 ms                                                                                                            | 237 ms: 1.08x faster                                                                                                    |
| regex_v8                 | 33.3 ms                                                                                                           | 34.4 ms: 1.03x slower                                                                                                   |
| asyncio_websockets       | 751 ms                                                                                                            | 778 ms: 1.04x slower                                                                                                    |
| async_tree_memoization   | 652 ms                                                                                                            | 684 ms: 1.05x slower                                                                                                    |
| regex_effbot             | 4.32 ms                                                                                                           | 4.54 ms: 1.05x slower                                                                                                   |
| sqlite_synth             | 3.83 us                                                                                                           | 4.10 us: 1.07x slower                                                                                                   |
| bench_mp_pool            | 90.5 ms                                                                                                           | 98.2 ms: 1.09x slower                                                                                                   |
| json_loads               | 34.1 us                                                                                                           | 37.4 us: 1.09x slower                                                                                                   |
| async_tree_cpu_io_mixed  | 804 ms                                                                                                            | 883 ms: 1.10x slower                                                                                                    |
| pathlib                  | 28.8 ms                                                                                                           | 32.5 ms: 1.13x slower                                                                                                   |
| async_tree_none          | 493 ms                                                                                                            | 557 ms: 1.13x slower                                                                                                    |
| shortest_path            | 886 ms                                                                                                            | 1.02 sec: 1.15x slower                                                                                                  |
| connected_components     | 819 ms                                                                                                            | 942 ms: 1.15x slower                                                                                                    |
| scimark_fft              | 474 ms                                                                                                            | 556 ms: 1.17x slower                                                                                                    |
| pycparser                | 1.67 sec                                                                                                          | 1.97 sec: 1.18x slower                                                                                                  |
| sphinx                   | 1.53 sec                                                                                                          | 1.83 sec: 1.19x slower                                                                                                  |
| xml_etree_parse          | 199 ms                                                                                                            | 238 ms: 1.19x slower                                                                                                    |
| coroutines               | 31.9 ms                                                                                                           | 38.7 ms: 1.21x slower                                                                                                   |
| dulwich_log              | 104 ms                                                                                                            | 128 ms: 1.22x slower                                                                                                    |
| spectral_norm            | 152 ms                                                                                                            | 188 ms: 1.23x slower                                                                                                    |
| coverage                 | 112 ms                                                                                                            | 140 ms: 1.26x slower                                                                                                    |
| sqlglot_optimize         | 73.8 ms                                                                                                           | 93.3 ms: 1.26x slower                                                                                                   |
| docutils                 | 3.76 sec                                                                                                          | 4.75 sec: 1.27x slower                                                                                                  |
| async_generators         | 562 ms                                                                                                            | 711 ms: 1.27x slower                                                                                                    |
| scimark_sparse_mat_mult  | 6.46 ms                                                                                                           | 8.19 ms: 1.27x slower                                                                                                   |
| json_dumps               | 14.7 ms                                                                                                           | 18.8 ms: 1.28x slower                                                                                                   |
| json                     | 6.43 ms                                                                                                           | 8.24 ms: 1.28x slower                                                                                                   |
| xml_etree_generate       | 116 ms                                                                                                            | 150 ms: 1.29x slower                                                                                                    |
| nqueens                  | 116 ms                                                                                                            | 152 ms: 1.31x slower                                                                                                    |
| mdp                      | 3.58 sec                                                                                                          | 4.69 sec: 1.31x slower                                                                                                  |
| python_startup           | 27.9 ms                                                                                                           | 37.0 ms: 1.33x slower                                                                                                   |
| deepcopy                 | 337 us                                                                                                            | 447 us: 1.33x slower                                                                                                    |
| many_optionals           | 1.09 ms                                                                                                           | 1.45 ms: 1.33x slower                                                                                                   |
| meteor_contest           | 152 ms                                                                                                            | 205 ms: 1.35x slower                                                                                                    |
| sqlglot_normalize        | 144 ms                                                                                                            | 197 ms: 1.36x slower                                                                                                    |
| crypto_pyaes             | 100 ms                                                                                                            | 137 ms: 1.37x slower                                                                                                    |
| 2to3                     | 470 ms                                                                                                            | 647 ms: 1.38x slower                                                                                                    |
| generators               | 40.9 ms                                                                                                           | 56.7 ms: 1.39x slower                                                                                                   |
| bench_thread_pool        | 3.53 ms                                                                                                           | 4.91 ms: 1.39x slower                                                                                                   |
| bpe_tokeniser            | 6.30 sec                                                                                                          | 8.88 sec: 1.41x slower                                                                                                  |
| telco                    | 10.0 ms                                                                                                           | 14.2 ms: 1.42x slower                                                                                                   |
| pprint_safe_repr         | 980 ms                                                                                                            | 1.40 sec: 1.43x slower                                                                                                  |
| thrift                   | 1.11 ms                                                                                                           | 1.60 ms: 1.44x slower                                                                                                   |
| sympy_integrate          | 29.5 ms                                                                                                           | 42.8 ms: 1.45x slower                                                                                                   |
| deepcopy_reduce          | 3.56 us                                                                                                           | 5.21 us: 1.46x slower                                                                                                   |
| typing_runtime_protocols | 220 us                                                                                                            | 323 us: 1.47x slower                                                                                                    |
| regex_compile            | 172 ms                                                                                                            | 253 ms: 1.47x slower                                                                                                    |
| tomli_loads              | 2.65 sec                                                                                                          | 3.91 sec: 1.47x slower                                                                                                  |
| float                    | 117 ms                                                                                                            | 172 ms: 1.48x slower                                                                                                    |
| fannkuch                 | 522 ms                                                                                                            | 775 ms: 1.48x slower                                                                                                    |
| pylint                   | 376 ms                                                                                                            | 563 ms: 1.50x slower                                                                                                    |
| genshi_text              | 31.0 ms                                                                                                           | 47.4 ms: 1.53x slower                                                                                                   |
| python_startup_no_site   | 15.5 ms                                                                                                           | 23.8 ms: 1.53x slower                                                                                                   |
| deepcopy_memo            | 39.8 us                                                                                                           | 61.1 us: 1.54x slower                                                                                                   |
| genshi_xml               | 65.8 ms                                                                                                           | 102 ms: 1.55x slower                                                                                                    |
| pyflate                  | 671 ms                                                                                                            | 1.04 sec: 1.55x slower                                                                                                  |
| django_template          | 46.4 ms                                                                                                           | 72.1 ms: 1.55x slower                                                                                                   |
| scimark_lu               | 161 ms                                                                                                            | 254 ms: 1.58x slower                                                                                                    |
| pprint_pformat           | 1.85 sec                                                                                                          | 2.96 sec: 1.60x slower                                                                                                  |
| subparsers               | 32.8 ms                                                                                                           | 52.8 ms: 1.61x slower                                                                                                   |
| xml_etree_process        | 82.3 ms                                                                                                           | 133 ms: 1.61x slower                                                                                                    |
| html5lib                 | 84.0 ms                                                                                                           | 136 ms: 1.62x slower                                                                                                    |
| logging_format           | 9.15 us                                                                                                           | 15.0 us: 1.64x slower                                                                                                   |
| unpickle_pure_python     | 287 us                                                                                                            | 479 us: 1.67x slower                                                                                                    |
| scimark_monte_carlo      | 88.5 ms                                                                                                           | 149 ms: 1.68x slower                                                                                                    |
| richards_super           | 70.5 ms                                                                                                           | 119 ms: 1.69x slower                                                                                                    |
| chaos                    | 85.1 ms                                                                                                           | 147 ms: 1.73x slower                                                                                                    |
| pickle_pure_python       | 435 us                                                                                                            | 756 us: 1.74x slower                                                                                                    |
| logging_silent           | 135 ns                                                                                                            | 241 ns: 1.78x slower                                                                                                    |
| hexiom                   | 8.34 ms                                                                                                           | 15.0 ms: 1.79x slower                                                                                                   |
| richards                 | 59.9 ms                                                                                                           | 109 ms: 1.82x slower                                                                                                    |
| nbody                    | 118 ms                                                                                                            | 217 ms: 1.84x slower                                                                                                    |
| sympy_str                | 350 ms                                                                                                            | 650 ms: 1.86x slower                                                                                                    |
| mako                     | 17.2 ms                                                                                                           | 32.2 ms: 1.87x slower                                                                                                   |
| comprehensions           | 21.9 us                                                                                                           | 41.3 us: 1.89x slower                                                                                                   |
| scimark_sor              | 157 ms                                                                                                            | 301 ms: 1.92x slower                                                                                                    |
| logging_simple           | 7.96 us                                                                                                           | 15.7 us: 1.97x slower                                                                                                   |
| sqlglot_parse            | 1.72 ms                                                                                                           | 3.40 ms: 1.97x slower                                                                                                   |
| sympy_expand             | 590 ms                                                                                                            | 1.17 sec: 1.98x slower                                                                                                  |
| sqlglot_transpile        | 2.26 ms                                                                                                           | 4.52 ms: 2.00x slower                                                                                                   |
| raytrace                 | 355 ms                                                                                                            | 712 ms: 2.00x slower                                                                                                    |
| go                       | 152 ms                                                                                                            | 342 ms: 2.25x slower                                                                                                    |
| sympy_sum                | 202 ms                                                                                                            | 470 ms: 2.33x slower                                                                                                    |
| deltablue                | 4.41 ms                                                                                                           | 10.4 ms: 2.36x slower                                                                                                   |
| Geometric mean           | (ref)                                                                                                             | 1.38x slower                                                                                                            |

Benchmark hidden because not significant (5): async_tree_cpu_io_mixed_tg, async_tree_none_tg, regex_dna, xml_etree_iterparse, async_tree_memoization_tg
Ignored benchmarks (2) of results/bm-20241126-3.14.0a2+-71ede11/bm-20241126-linux-x86_64-python-71ede1142ddad2d31cc9-3.14.0a2+-71ede11.json: sqlalchemy_declarative, sqlalchemy_imperative

- Geometric mean (including insignificant results): 1.267x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.27x
- 95% likely to have a slowdown of 1.26x
- 99% likely to have a slowdown of 1.23x

# Memory
- memory change: 1.19x