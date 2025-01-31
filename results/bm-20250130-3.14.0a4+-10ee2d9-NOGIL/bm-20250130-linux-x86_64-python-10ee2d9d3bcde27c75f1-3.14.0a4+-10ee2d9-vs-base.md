# Results vs. base

- fork: python
- ref: 10ee2d9d3bcde27c75f1
- machine: linux-x86_64
- commit hash: 10ee2d9
- commit date: 2025-01-30
- overall geometric mean: 1.127x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250130-3.14.0a4+-10ee2d9/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json | results/bm-20250130-3.14.0a4+-10ee2d9-NOGIL/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 468 ms                                                                                                            | 555 ms: 1.18x slower                                                                                                    |
| docutils       | 3.71 sec                                                                                                          | 4.11 sec: 1.11x slower                                                                                                  |
| html5lib       | 85.9 ms                                                                                                           | 99.8 ms: 1.16x slower                                                                                                   |
| sphinx         | 1.42 sec                                                                                                          | 1.62 sec: 1.14x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.15x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | results/bm-20250130-3.14.0a4+-10ee2d9/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json | results/bm-20250130-3.14.0a4+-10ee2d9-NOGIL/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json |
|-------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg        | 958 ms                                                                                                            | 837 ms: 1.14x faster                                                                                                    |
| async_tree_io           | 888 ms                                                                                                            | 845 ms: 1.05x faster                                                                                                    |
| asyncio_websockets      | 735 ms                                                                                                            | 703 ms: 1.04x faster                                                                                                    |
| coroutines              | 31.0 ms                                                                                                           | 32.1 ms: 1.04x slower                                                                                                   |
| async_tree_none_tg      | 361 ms                                                                                                            | 376 ms: 1.04x slower                                                                                                    |
| async_tree_cpu_io_mixed | 679 ms                                                                                                            | 708 ms: 1.04x slower                                                                                                    |
| async_generators        | 546 ms                                                                                                            | 581 ms: 1.06x slower                                                                                                    |
| async_tree_none         | 380 ms                                                                                                            | 431 ms: 1.13x slower                                                                                                    |
| Geometric mean          | (ref)                                                                                                             | 1.01x slower                                                                                                            |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250130-3.14.0a4+-10ee2d9/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json | results/bm-20250130-3.14.0a4+-10ee2d9-NOGIL/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| float          | 101 ms                                                                                                            | 109 ms: 1.08x slower                                                                                                    |
| nbody          | 127 ms                                                                                                            | 186 ms: 1.46x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.17x slower                                                                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250130-3.14.0a4+-10ee2d9/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json | results/bm-20250130-3.14.0a4+-10ee2d9-NOGIL/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 34.2 ms                                                                                                           | 32.4 ms: 1.06x faster                                                                                                   |
| regex_dna      | 274 ms                                                                                                            | 293 ms: 1.07x slower                                                                                                    |
| regex_effbot   | 4.46 ms                                                                                                           | 4.90 ms: 1.10x slower                                                                                                   |
| regex_compile  | 173 ms                                                                                                            | 214 ms: 1.24x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.08x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250130-3.14.0a4+-10ee2d9/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json | results/bm-20250130-3.14.0a4+-10ee2d9-NOGIL/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 157 ms                                                                                                            | 144 ms: 1.09x faster                                                                                                    |
| xml_etree_parse      | 204 ms                                                                                                            | 216 ms: 1.06x slower                                                                                                    |
| pickle_pure_python   | 431 us                                                                                                            | 464 us: 1.08x slower                                                                                                    |
| unpickle_pure_python | 322 us                                                                                                            | 364 us: 1.13x slower                                                                                                    |
| tomli_loads          | 2.52 sec                                                                                                          | 3.09 sec: 1.23x slower                                                                                                  |
| xml_etree_generate   | 117 ms                                                                                                            | 145 ms: 1.24x slower                                                                                                    |
| json_loads           | 37.6 us                                                                                                           | 46.9 us: 1.25x slower                                                                                                   |
| xml_etree_process    | 83.8 ms                                                                                                           | 105 ms: 1.25x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmark hidden because not significant (1): json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250130-3.14.0a4+-10ee2d9/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json | results/bm-20250130-3.14.0a4+-10ee2d9-NOGIL/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 26.6 ms                                                                                                           | 33.7 ms: 1.27x slower                                                                                                   |
| python_startup_no_site | 15.9 ms                                                                                                           | 21.4 ms: 1.35x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.31x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250130-3.14.0a4+-10ee2d9/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json | results/bm-20250130-3.14.0a4+-10ee2d9-NOGIL/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 76.1 ms                                                                                                           | 86.5 ms: 1.14x slower                                                                                                   |
| django_template | 49.2 ms                                                                                                           | 56.2 ms: 1.14x slower                                                                                                   |
| genshi_text     | 30.2 ms                                                                                                           | 39.8 ms: 1.32x slower                                                                                                   |
| mako            | 16.7 ms                                                                                                           | 24.3 ms: 1.45x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.26x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                | results/bm-20250130-3.14.0a4+-10ee2d9/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json | results/bm-20250130-3.14.0a4+-10ee2d9-NOGIL/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json |
|--------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal             | 7.56 ms                                                                                                           | 4.01 ms: 1.89x faster                                                                                                   |
| create_gc_cycles         | 3.75 ms                                                                                                           | 3.12 ms: 1.20x faster                                                                                                   |
| async_tree_io_tg         | 958 ms                                                                                                            | 837 ms: 1.14x faster                                                                                                    |
| xml_etree_iterparse      | 157 ms                                                                                                            | 144 ms: 1.09x faster                                                                                                    |
| logging_format           | 11.1 us                                                                                                           | 10.3 us: 1.08x faster                                                                                                   |
| regex_v8                 | 34.2 ms                                                                                                           | 32.4 ms: 1.06x faster                                                                                                   |
| async_tree_io            | 888 ms                                                                                                            | 845 ms: 1.05x faster                                                                                                    |
| asyncio_websockets       | 735 ms                                                                                                            | 703 ms: 1.04x faster                                                                                                    |
| coroutines               | 31.0 ms                                                                                                           | 32.1 ms: 1.04x slower                                                                                                   |
| async_tree_none_tg       | 361 ms                                                                                                            | 376 ms: 1.04x slower                                                                                                    |
| async_tree_cpu_io_mixed  | 679 ms                                                                                                            | 708 ms: 1.04x slower                                                                                                    |
| xml_etree_parse          | 204 ms                                                                                                            | 216 ms: 1.06x slower                                                                                                    |
| pathlib                  | 29.2 ms                                                                                                           | 30.9 ms: 1.06x slower                                                                                                   |
| async_generators         | 546 ms                                                                                                            | 581 ms: 1.06x slower                                                                                                    |
| regex_dna                | 274 ms                                                                                                            | 293 ms: 1.07x slower                                                                                                    |
| sqlglot_normalize        | 154 ms                                                                                                            | 164 ms: 1.07x slower                                                                                                    |
| pickle_pure_python       | 431 us                                                                                                            | 464 us: 1.08x slower                                                                                                    |
| float                    | 101 ms                                                                                                            | 109 ms: 1.08x slower                                                                                                    |
| k_core                   | 4.07 sec                                                                                                          | 4.42 sec: 1.09x slower                                                                                                  |
| regex_effbot             | 4.46 ms                                                                                                           | 4.90 ms: 1.10x slower                                                                                                   |
| docutils                 | 3.71 sec                                                                                                          | 4.11 sec: 1.11x slower                                                                                                  |
| deepcopy_reduce          | 3.70 us                                                                                                           | 4.10 us: 1.11x slower                                                                                                   |
| nqueens                  | 109 ms                                                                                                            | 121 ms: 1.11x slower                                                                                                    |
| deepcopy                 | 371 us                                                                                                            | 413 us: 1.11x slower                                                                                                    |
| sympy_str                | 387 ms                                                                                                            | 431 ms: 1.11x slower                                                                                                    |
| pylint                   | 409 ms                                                                                                            | 460 ms: 1.13x slower                                                                                                    |
| generators               | 38.5 ms                                                                                                           | 43.6 ms: 1.13x slower                                                                                                   |
| unpickle_pure_python     | 322 us                                                                                                            | 364 us: 1.13x slower                                                                                                    |
| async_tree_none          | 380 ms                                                                                                            | 431 ms: 1.13x slower                                                                                                    |
| genshi_xml               | 76.1 ms                                                                                                           | 86.5 ms: 1.14x slower                                                                                                   |
| sphinx                   | 1.42 sec                                                                                                          | 1.62 sec: 1.14x slower                                                                                                  |
| comprehensions           | 22.6 us                                                                                                           | 25.8 us: 1.14x slower                                                                                                   |
| django_template          | 49.2 ms                                                                                                           | 56.2 ms: 1.14x slower                                                                                                   |
| json                     | 7.38 ms                                                                                                           | 8.48 ms: 1.15x slower                                                                                                   |
| richards_super           | 75.9 ms                                                                                                           | 87.3 ms: 1.15x slower                                                                                                   |
| thrift                   | 1.06 ms                                                                                                           | 1.22 ms: 1.15x slower                                                                                                   |
| pprint_safe_repr         | 941 ms                                                                                                            | 1.09 sec: 1.16x slower                                                                                                  |
| html5lib                 | 85.9 ms                                                                                                           | 99.8 ms: 1.16x slower                                                                                                   |
| logging_silent           | 147 ns                                                                                                            | 173 ns: 1.18x slower                                                                                                    |
| sympy_sum                | 218 ms                                                                                                            | 257 ms: 1.18x slower                                                                                                    |
| 2to3                     | 468 ms                                                                                                            | 555 ms: 1.18x slower                                                                                                    |
| hexiom                   | 8.43 ms                                                                                                           | 10.0 ms: 1.19x slower                                                                                                   |
| sympy_expand             | 596 ms                                                                                                            | 709 ms: 1.19x slower                                                                                                    |
| sqlglot_optimize         | 74.0 ms                                                                                                           | 88.7 ms: 1.20x slower                                                                                                   |
| telco                    | 10.1 ms                                                                                                           | 12.1 ms: 1.20x slower                                                                                                   |
| connected_components     | 821 ms                                                                                                            | 992 ms: 1.21x slower                                                                                                    |
| pprint_pformat           | 1.91 sec                                                                                                          | 2.31 sec: 1.21x slower                                                                                                  |
| richards                 | 62.3 ms                                                                                                           | 75.7 ms: 1.22x slower                                                                                                   |
| chaos                    | 80.2 ms                                                                                                           | 97.6 ms: 1.22x slower                                                                                                   |
| mdp                      | 3.49 sec                                                                                                          | 4.27 sec: 1.22x slower                                                                                                  |
| deepcopy_memo            | 42.8 us                                                                                                           | 52.4 us: 1.23x slower                                                                                                   |
| tomli_loads              | 2.52 sec                                                                                                          | 3.09 sec: 1.23x slower                                                                                                  |
| scimark_sor              | 160 ms                                                                                                            | 196 ms: 1.23x slower                                                                                                    |
| logging_simple           | 8.83 us                                                                                                           | 10.9 us: 1.23x slower                                                                                                   |
| subparsers               | 33.1 ms                                                                                                           | 40.7 ms: 1.23x slower                                                                                                   |
| scimark_monte_carlo      | 92.0 ms                                                                                                           | 113 ms: 1.23x slower                                                                                                    |
| regex_compile            | 173 ms                                                                                                            | 214 ms: 1.24x slower                                                                                                    |
| xml_etree_generate       | 117 ms                                                                                                            | 145 ms: 1.24x slower                                                                                                    |
| scimark_lu               | 146 ms                                                                                                            | 182 ms: 1.24x slower                                                                                                    |
| json_loads               | 37.6 us                                                                                                           | 46.9 us: 1.25x slower                                                                                                   |
| many_optionals           | 1.11 ms                                                                                                           | 1.38 ms: 1.25x slower                                                                                                   |
| xml_etree_process        | 83.8 ms                                                                                                           | 105 ms: 1.25x slower                                                                                                    |
| shortest_path            | 889 ms                                                                                                            | 1.11 sec: 1.25x slower                                                                                                  |
| scimark_fft              | 442 ms                                                                                                            | 558 ms: 1.26x slower                                                                                                    |
| coverage                 | 119 ms                                                                                                            | 151 ms: 1.26x slower                                                                                                    |
| python_startup           | 26.6 ms                                                                                                           | 33.7 ms: 1.27x slower                                                                                                   |
| sqlglot_transpile        | 2.29 ms                                                                                                           | 2.91 ms: 1.27x slower                                                                                                   |
| raytrace                 | 362 ms                                                                                                            | 461 ms: 1.27x slower                                                                                                    |
| sympy_integrate          | 28.3 ms                                                                                                           | 36.1 ms: 1.28x slower                                                                                                   |
| sqlalchemy_declarative   | 187 ms                                                                                                            | 242 ms: 1.29x slower                                                                                                    |
| pyflate                  | 602 ms                                                                                                            | 782 ms: 1.30x slower                                                                                                    |
| fannkuch                 | 545 ms                                                                                                            | 710 ms: 1.30x slower                                                                                                    |
| go                       | 151 ms                                                                                                            | 197 ms: 1.31x slower                                                                                                    |
| sqlglot_parse            | 1.70 ms                                                                                                           | 2.23 ms: 1.31x slower                                                                                                   |
| genshi_text              | 30.2 ms                                                                                                           | 39.8 ms: 1.32x slower                                                                                                   |
| bpe_tokeniser            | 5.64 sec                                                                                                          | 7.48 sec: 1.33x slower                                                                                                  |
| meteor_contest           | 155 ms                                                                                                            | 206 ms: 1.33x slower                                                                                                    |
| spectral_norm            | 119 ms                                                                                                            | 160 ms: 1.34x slower                                                                                                    |
| python_startup_no_site   | 15.9 ms                                                                                                           | 21.4 ms: 1.35x slower                                                                                                   |
| typing_runtime_protocols | 219 us                                                                                                            | 301 us: 1.38x slower                                                                                                    |
| bench_thread_pool        | 2.88 ms                                                                                                           | 3.99 ms: 1.38x slower                                                                                                   |
| scimark_sparse_mat_mult  | 6.41 ms                                                                                                           | 9.20 ms: 1.44x slower                                                                                                   |
| mako                     | 16.7 ms                                                                                                           | 24.3 ms: 1.45x slower                                                                                                   |
| nbody                    | 127 ms                                                                                                            | 186 ms: 1.46x slower                                                                                                    |
| crypto_pyaes             | 89.7 ms                                                                                                           | 132 ms: 1.47x slower                                                                                                    |
| deltablue                | 4.51 ms                                                                                                           | 6.68 ms: 1.48x slower                                                                                                   |
| sqlalchemy_imperative    | 22.5 ms                                                                                                           | 36.4 ms: 1.62x slower                                                                                                   |
| Geometric mean           | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmark hidden because not significant (9): bench_mp_pool, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, json_dumps, pidigits, pycparser, sqlite_synth, async_tree_memoization, dulwich_log

- Geometric mean (including insignificant results): 1.127x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.20x