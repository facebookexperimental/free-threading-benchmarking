# Results vs. base

- fork: python
- ref: bdd23c0bb95faa37130f
- machine: linux-x86_64
- commit hash: bdd23c0
- commit date: 2025-04-28
- overall geometric mean: 1.079x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250428-3.14.0a7+-bdd23c0/bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json | results/bm-20250428-3.14.0a7+-bdd23c0-NOGIL/bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                                                                            | 281 ms: 1.14x slower                                                                                                    |
| docutils       | 2.52 sec                                                                                                          | 2.70 sec: 1.07x slower                                                                                                  |
| sphinx         | 972 ms                                                                                                            | 1.07 sec: 1.10x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.10x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250428-3.14.0a7+-bdd23c0/bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json | results/bm-20250428-3.14.0a7+-bdd23c0-NOGIL/bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 610 ms                                                                                                            | 515 ms: 1.18x faster                                                                                                    |
| async_tree_none_tg         | 254 ms                                                                                                            | 223 ms: 1.14x faster                                                                                                    |
| async_tree_io              | 610 ms                                                                                                            | 543 ms: 1.12x faster                                                                                                    |
| async_tree_memoization_tg  | 313 ms                                                                                                            | 281 ms: 1.11x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 515 ms                                                                                                            | 465 ms: 1.11x faster                                                                                                    |
| async_tree_none            | 269 ms                                                                                                            | 255 ms: 1.05x faster                                                                                                    |
| async_tree_cpu_io_mixed    | 518 ms                                                                                                            | 493 ms: 1.05x faster                                                                                                    |
| asyncio_websockets         | 518 ms                                                                                                            | 516 ms: 1.00x faster                                                                                                    |
| coroutines                 | 22.5 ms                                                                                                           | 22.9 ms: 1.02x slower                                                                                                   |
| async_generators           | 327 ms                                                                                                            | 356 ms: 1.09x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.06x faster                                                                                                            |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250428-3.14.0a7+-bdd23c0/bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json | results/bm-20250428-3.14.0a7+-bdd23c0-NOGIL/bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 209 ms                                                                                                            | 185 ms: 1.13x faster                                                                                                    |
| float          | 68.7 ms                                                                                                           | 67.3 ms: 1.02x faster                                                                                                   |
| nbody          | 87.0 ms                                                                                                           | 111 ms: 1.27x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.03x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250428-3.14.0a7+-bdd23c0/bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json | results/bm-20250428-3.14.0a7+-bdd23c0-NOGIL/bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.7 ms                                                                                                           | 21.2 ms: 1.02x faster                                                                                                   |
| regex_dna      | 174 ms                                                                                                            | 184 ms: 1.06x slower                                                                                                    |
| regex_effbot   | 2.59 ms                                                                                                           | 2.87 ms: 1.11x slower                                                                                                   |
| regex_compile  | 121 ms                                                                                                            | 143 ms: 1.18x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.08x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250428-3.14.0a7+-bdd23c0/bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json | results/bm-20250428-3.14.0a7+-bdd23c0-NOGIL/bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 92.7 ms                                                                                                           | 86.4 ms: 1.07x faster                                                                                                   |
| xml_etree_parse      | 131 ms                                                                                                            | 129 ms: 1.01x faster                                                                                                    |
| json_loads           | 27.8 us                                                                                                           | 29.6 us: 1.07x slower                                                                                                   |
| unpickle_pure_python | 210 us                                                                                                            | 225 us: 1.07x slower                                                                                                    |
| pickle_pure_python   | 304 us                                                                                                            | 328 us: 1.08x slower                                                                                                    |
| xml_etree_generate   | 82.3 ms                                                                                                           | 91.8 ms: 1.12x slower                                                                                                   |
| json_dumps           | 11.3 ms                                                                                                           | 12.7 ms: 1.12x slower                                                                                                   |
| tomli_loads          | 1.85 sec                                                                                                          | 2.09 sec: 1.13x slower                                                                                                  |
| xml_etree_process    | 57.7 ms                                                                                                           | 66.2 ms: 1.15x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.07x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250428-3.14.0a7+-bdd23c0/bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json | results/bm-20250428-3.14.0a7+-bdd23c0-NOGIL/bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 14.9 ms                                                                                                           | 15.6 ms: 1.05x slower                                                                                                   |
| python_startup_no_site | 7.28 ms                                                                                                           | 9.27 ms: 1.27x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.15x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250428-3.14.0a7+-bdd23c0/bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json | results/bm-20250428-3.14.0a7+-bdd23c0-NOGIL/bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 48.0 ms                                                                                                           | 55.4 ms: 1.15x slower                                                                                                   |
| django_template | 34.3 ms                                                                                                           | 40.1 ms: 1.17x slower                                                                                                   |
| genshi_text     | 21.0 ms                                                                                                           | 26.2 ms: 1.25x slower                                                                                                   |
| mako            | 11.9 ms                                                                                                           | 15.4 ms: 1.30x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.22x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250428-3.14.0a7+-bdd23c0/bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json | results/bm-20250428-3.14.0a7+-bdd23c0-NOGIL/bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.25 ms                                                                                                           | 1.78 ms: 2.39x faster                                                                                                   |
| create_gc_cycles           | 1.84 ms                                                                                                           | 1.35 ms: 1.36x faster                                                                                                   |
| async_tree_io_tg           | 610 ms                                                                                                            | 515 ms: 1.18x faster                                                                                                    |
| async_tree_none_tg         | 254 ms                                                                                                            | 223 ms: 1.14x faster                                                                                                    |
| pidigits                   | 209 ms                                                                                                            | 185 ms: 1.13x faster                                                                                                    |
| async_tree_io              | 610 ms                                                                                                            | 543 ms: 1.12x faster                                                                                                    |
| async_tree_memoization_tg  | 313 ms                                                                                                            | 281 ms: 1.11x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 515 ms                                                                                                            | 465 ms: 1.11x faster                                                                                                    |
| sqlite_synth               | 2.21 us                                                                                                           | 2.01 us: 1.10x faster                                                                                                   |
| xml_etree_iterparse        | 92.7 ms                                                                                                           | 86.4 ms: 1.07x faster                                                                                                   |
| async_tree_none            | 269 ms                                                                                                            | 255 ms: 1.05x faster                                                                                                    |
| async_tree_cpu_io_mixed    | 518 ms                                                                                                            | 493 ms: 1.05x faster                                                                                                    |
| regex_v8                   | 21.7 ms                                                                                                           | 21.2 ms: 1.02x faster                                                                                                   |
| float                      | 68.7 ms                                                                                                           | 67.3 ms: 1.02x faster                                                                                                   |
| xml_etree_parse            | 131 ms                                                                                                            | 129 ms: 1.01x faster                                                                                                    |
| asyncio_websockets         | 518 ms                                                                                                            | 516 ms: 1.00x faster                                                                                                    |
| coroutines                 | 22.5 ms                                                                                                           | 22.9 ms: 1.02x slower                                                                                                   |
| pathlib                    | 19.0 ms                                                                                                           | 19.4 ms: 1.02x slower                                                                                                   |
| pycparser                  | 1.10 sec                                                                                                          | 1.13 sec: 1.03x slower                                                                                                  |
| json                       | 4.85 ms                                                                                                           | 5.01 ms: 1.03x slower                                                                                                   |
| logging_silent             | 96.8 ns                                                                                                           | 101 ns: 1.05x slower                                                                                                    |
| python_startup             | 14.9 ms                                                                                                           | 15.6 ms: 1.05x slower                                                                                                   |
| dulwich_log                | 67.4 ms                                                                                                           | 70.6 ms: 1.05x slower                                                                                                   |
| scimark_sor                | 110 ms                                                                                                            | 117 ms: 1.06x slower                                                                                                    |
| regex_dna                  | 174 ms                                                                                                            | 184 ms: 1.06x slower                                                                                                    |
| scimark_fft                | 318 ms                                                                                                            | 338 ms: 1.06x slower                                                                                                    |
| bpe_tokeniser              | 4.07 sec                                                                                                          | 4.33 sec: 1.06x slower                                                                                                  |
| json_loads                 | 27.8 us                                                                                                           | 29.6 us: 1.07x slower                                                                                                   |
| unpickle_pure_python       | 210 us                                                                                                            | 225 us: 1.07x slower                                                                                                    |
| docutils                   | 2.52 sec                                                                                                          | 2.70 sec: 1.07x slower                                                                                                  |
| spectral_norm              | 93.1 ms                                                                                                           | 100 ms: 1.08x slower                                                                                                    |
| generators                 | 27.8 ms                                                                                                           | 30.0 ms: 1.08x slower                                                                                                   |
| pickle_pure_python         | 304 us                                                                                                            | 328 us: 1.08x slower                                                                                                    |
| deltablue                  | 3.24 ms                                                                                                           | 3.50 ms: 1.08x slower                                                                                                   |
| bench_mp_pool              | 88.2 ms                                                                                                           | 95.4 ms: 1.08x slower                                                                                                   |
| async_generators           | 327 ms                                                                                                            | 356 ms: 1.09x slower                                                                                                    |
| pylint                     | 278 ms                                                                                                            | 304 ms: 1.09x slower                                                                                                    |
| pprint_safe_repr           | 693 ms                                                                                                            | 762 ms: 1.10x slower                                                                                                    |
| sphinx                     | 972 ms                                                                                                            | 1.07 sec: 1.10x slower                                                                                                  |
| many_optionals             | 997 us                                                                                                            | 1.10 ms: 1.11x slower                                                                                                   |
| regex_effbot               | 2.59 ms                                                                                                           | 2.87 ms: 1.11x slower                                                                                                   |
| subparsers                 | 22.0 ms                                                                                                           | 24.4 ms: 1.11x slower                                                                                                   |
| pprint_pformat             | 1.41 sec                                                                                                          | 1.57 sec: 1.11x slower                                                                                                  |
| k_core                     | 2.02 sec                                                                                                          | 2.24 sec: 1.11x slower                                                                                                  |
| xml_etree_generate         | 82.3 ms                                                                                                           | 91.8 ms: 1.12x slower                                                                                                   |
| json_dumps                 | 11.3 ms                                                                                                           | 12.7 ms: 1.12x slower                                                                                                   |
| scimark_lu                 | 113 ms                                                                                                            | 127 ms: 1.12x slower                                                                                                    |
| scimark_sparse_mat_mult    | 4.50 ms                                                                                                           | 5.05 ms: 1.12x slower                                                                                                   |
| tomli_loads                | 1.85 sec                                                                                                          | 2.09 sec: 1.13x slower                                                                                                  |
| pyflate                    | 405 ms                                                                                                            | 457 ms: 1.13x slower                                                                                                    |
| nqueens                    | 75.4 ms                                                                                                           | 85.6 ms: 1.14x slower                                                                                                   |
| 2to3                       | 246 ms                                                                                                            | 281 ms: 1.14x slower                                                                                                    |
| sqlglot_v2_normalize       | 99.1 ms                                                                                                           | 113 ms: 1.14x slower                                                                                                    |
| deepcopy_reduce            | 2.58 us                                                                                                           | 2.94 us: 1.14x slower                                                                                                   |
| go                         | 108 ms                                                                                                            | 123 ms: 1.15x slower                                                                                                    |
| xml_etree_process          | 57.7 ms                                                                                                           | 66.2 ms: 1.15x slower                                                                                                   |
| chaos                      | 53.0 ms                                                                                                           | 60.8 ms: 1.15x slower                                                                                                   |
| mdp                        | 1.13 sec                                                                                                          | 1.30 sec: 1.15x slower                                                                                                  |
| sqlglot_v2_optimize        | 50.0 ms                                                                                                           | 57.6 ms: 1.15x slower                                                                                                   |
| genshi_xml                 | 48.0 ms                                                                                                           | 55.4 ms: 1.15x slower                                                                                                   |
| telco                      | 7.14 ms                                                                                                           | 8.25 ms: 1.15x slower                                                                                                   |
| deepcopy                   | 249 us                                                                                                            | 288 us: 1.16x slower                                                                                                    |
| raytrace                   | 247 ms                                                                                                            | 286 ms: 1.16x slower                                                                                                    |
| logging_simple             | 5.94 us                                                                                                           | 6.89 us: 1.16x slower                                                                                                   |
| sympy_expand               | 451 ms                                                                                                            | 523 ms: 1.16x slower                                                                                                    |
| sqlalchemy_imperative      | 20.2 ms                                                                                                           | 23.5 ms: 1.16x slower                                                                                                   |
| logging_format             | 6.64 us                                                                                                           | 7.74 us: 1.17x slower                                                                                                   |
| hexiom                     | 5.64 ms                                                                                                           | 6.59 ms: 1.17x slower                                                                                                   |
| django_template            | 34.3 ms                                                                                                           | 40.1 ms: 1.17x slower                                                                                                   |
| sympy_sum                  | 151 ms                                                                                                            | 177 ms: 1.17x slower                                                                                                    |
| sqlglot_v2_transpile       | 1.51 ms                                                                                                           | 1.77 ms: 1.17x slower                                                                                                   |
| sympy_integrate            | 18.7 ms                                                                                                           | 21.9 ms: 1.18x slower                                                                                                   |
| sympy_str                  | 267 ms                                                                                                            | 314 ms: 1.18x slower                                                                                                    |
| comprehensions             | 16.4 us                                                                                                           | 19.3 us: 1.18x slower                                                                                                   |
| deepcopy_memo              | 29.2 us                                                                                                           | 34.5 us: 1.18x slower                                                                                                   |
| regex_compile              | 121 ms                                                                                                            | 143 ms: 1.18x slower                                                                                                    |
| sqlalchemy_declarative     | 129 ms                                                                                                            | 153 ms: 1.19x slower                                                                                                    |
| scimark_monte_carlo        | 62.0 ms                                                                                                           | 73.7 ms: 1.19x slower                                                                                                   |
| fannkuch                   | 374 ms                                                                                                            | 447 ms: 1.20x slower                                                                                                    |
| sqlglot_v2_parse           | 1.21 ms                                                                                                           | 1.46 ms: 1.21x slower                                                                                                   |
| typing_runtime_protocols   | 156 us                                                                                                            | 190 us: 1.21x slower                                                                                                    |
| richards                   | 40.9 ms                                                                                                           | 49.7 ms: 1.22x slower                                                                                                   |
| shortest_path              | 435 ms                                                                                                            | 530 ms: 1.22x slower                                                                                                    |
| richards_super             | 46.8 ms                                                                                                           | 57.4 ms: 1.23x slower                                                                                                   |
| connected_components       | 391 ms                                                                                                            | 481 ms: 1.23x slower                                                                                                    |
| crypto_pyaes               | 66.8 ms                                                                                                           | 83.3 ms: 1.25x slower                                                                                                   |
| genshi_text                | 21.0 ms                                                                                                           | 26.2 ms: 1.25x slower                                                                                                   |
| nbody                      | 87.0 ms                                                                                                           | 111 ms: 1.27x slower                                                                                                    |
| python_startup_no_site     | 7.28 ms                                                                                                           | 9.27 ms: 1.27x slower                                                                                                   |
| meteor_contest             | 98.6 ms                                                                                                           | 127 ms: 1.29x slower                                                                                                    |
| mako                       | 11.9 ms                                                                                                           | 15.4 ms: 1.30x slower                                                                                                   |
| coverage                   | 82.3 ms                                                                                                           | 109 ms: 1.33x slower                                                                                                    |
| bench_thread_pool          | 1.05 ms                                                                                                           | 3.13 ms: 2.98x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.10x slower                                                                                                            |

Benchmark hidden because not significant (1): async_tree_memoization
Ignored benchmarks (1) of results/bm-20250428-3.14.0a7+-bdd23c0-NOGIL/bm-20250428-vultr-x86_64-python-bdd23c0bb95faa37130f-3.14.0a7+-bdd23c0.json: html5lib

- Geometric mean (including insignificant results): 1.079x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.20x