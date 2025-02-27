# Results vs. base

- fork: python
- ref: fda056e64bdfcac3dd3d
- machine: linux-x86_64
- commit hash: fda056e
- commit date: 2025-02-26
- overall geometric mean: 1.130x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250226-3.14.0a5+-fda056e/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json | results/bm-20250226-3.14.0a5+-fda056e-NOGIL/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 250 ms                                                                                                            | 305 ms: 1.22x slower                                                                                                    |
| docutils       | 2.53 sec                                                                                                          | 2.80 sec: 1.11x slower                                                                                                  |
| sphinx         | 968 ms                                                                                                            | 1.10 sec: 1.13x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.15x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250226-3.14.0a5+-fda056e/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json | results/bm-20250226-3.14.0a5+-fda056e-NOGIL/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 600 ms                                                                                                            | 552 ms: 1.09x faster                                                                                                    |
| async_tree_none_tg         | 254 ms                                                                                                            | 238 ms: 1.07x faster                                                                                                    |
| async_tree_io              | 599 ms                                                                                                            | 579 ms: 1.04x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 478 ms                                                                                                            | 492 ms: 1.03x slower                                                                                                    |
| async_tree_none            | 259 ms                                                                                                            | 276 ms: 1.07x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 487 ms                                                                                                            | 524 ms: 1.08x slower                                                                                                    |
| async_tree_memoization     | 311 ms                                                                                                            | 340 ms: 1.09x slower                                                                                                    |
| coroutines                 | 21.3 ms                                                                                                           | 23.4 ms: 1.10x slower                                                                                                   |
| async_generators           | 316 ms                                                                                                            | 373 ms: 1.18x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.03x slower                                                                                                            |

Benchmark hidden because not significant (2): async_tree_memoization_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250226-3.14.0a5+-fda056e/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json | results/bm-20250226-3.14.0a5+-fda056e-NOGIL/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 212 ms                                                                                                            | 191 ms: 1.11x faster                                                                                                    |
| float          | 70.4 ms                                                                                                           | 76.1 ms: 1.08x slower                                                                                                   |
| nbody          | 84.1 ms                                                                                                           | 136 ms: 1.61x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250226-3.14.0a5+-fda056e/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json | results/bm-20250226-3.14.0a5+-fda056e-NOGIL/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 24.8 ms                                                                                                           | 23.9 ms: 1.04x faster                                                                                                   |
| regex_effbot   | 2.73 ms                                                                                                           | 2.67 ms: 1.02x faster                                                                                                   |
| regex_dna      | 173 ms                                                                                                            | 178 ms: 1.03x slower                                                                                                    |
| regex_compile  | 124 ms                                                                                                            | 155 ms: 1.25x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.05x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250226-3.14.0a5+-fda056e/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json | results/bm-20250226-3.14.0a5+-fda056e-NOGIL/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 89.7 ms                                                                                                           | 87.6 ms: 1.02x faster                                                                                                   |
| json_loads           | 28.6 us                                                                                                           | 29.4 us: 1.03x slower                                                                                                   |
| json_dumps           | 11.2 ms                                                                                                           | 12.9 ms: 1.15x slower                                                                                                   |
| xml_etree_generate   | 81.5 ms                                                                                                           | 95.7 ms: 1.17x slower                                                                                                   |
| pickle_pure_python   | 304 us                                                                                                            | 362 us: 1.19x slower                                                                                                    |
| unpickle_pure_python | 208 us                                                                                                            | 250 us: 1.20x slower                                                                                                    |
| xml_etree_process    | 56.8 ms                                                                                                           | 69.8 ms: 1.23x slower                                                                                                   |
| tomli_loads          | 1.85 sec                                                                                                          | 2.38 sec: 1.29x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                             | 1.13x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250226-3.14.0a5+-fda056e/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json | results/bm-20250226-3.14.0a5+-fda056e-NOGIL/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 14.8 ms                                                                                                           | 15.7 ms: 1.06x slower                                                                                                   |
| python_startup_no_site | 7.54 ms                                                                                                           | 9.68 ms: 1.28x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.17x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250226-3.14.0a5+-fda056e/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json | results/bm-20250226-3.14.0a5+-fda056e-NOGIL/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 47.1 ms                                                                                                           | 60.3 ms: 1.28x slower                                                                                                   |
| django_template | 32.8 ms                                                                                                           | 42.6 ms: 1.30x slower                                                                                                   |
| mako            | 11.5 ms                                                                                                           | 15.8 ms: 1.37x slower                                                                                                   |
| genshi_text     | 20.3 ms                                                                                                           | 28.3 ms: 1.39x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.33x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250226-3.14.0a5+-fda056e/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json | results/bm-20250226-3.14.0a5+-fda056e-NOGIL/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.44 ms                                                                                                           | 1.74 ms: 2.55x faster                                                                                                   |
| sqlglot_normalize          | 277 ms                                                                                                            | 121 ms: 2.28x faster                                                                                                    |
| create_gc_cycles           | 1.83 ms                                                                                                           | 1.32 ms: 1.38x faster                                                                                                   |
| pidigits                   | 212 ms                                                                                                            | 191 ms: 1.11x faster                                                                                                    |
| async_tree_io_tg           | 600 ms                                                                                                            | 552 ms: 1.09x faster                                                                                                    |
| sqlite_synth               | 2.20 us                                                                                                           | 2.03 us: 1.08x faster                                                                                                   |
| async_tree_none_tg         | 254 ms                                                                                                            | 238 ms: 1.07x faster                                                                                                    |
| regex_v8                   | 24.8 ms                                                                                                           | 23.9 ms: 1.04x faster                                                                                                   |
| async_tree_io              | 599 ms                                                                                                            | 579 ms: 1.04x faster                                                                                                    |
| xml_etree_iterparse        | 89.7 ms                                                                                                           | 87.6 ms: 1.02x faster                                                                                                   |
| regex_effbot               | 2.73 ms                                                                                                           | 2.67 ms: 1.02x faster                                                                                                   |
| pathlib                    | 19.1 ms                                                                                                           | 19.6 ms: 1.03x slower                                                                                                   |
| json_loads                 | 28.6 us                                                                                                           | 29.4 us: 1.03x slower                                                                                                   |
| regex_dna                  | 173 ms                                                                                                            | 178 ms: 1.03x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 478 ms                                                                                                            | 492 ms: 1.03x slower                                                                                                    |
| python_startup             | 14.8 ms                                                                                                           | 15.7 ms: 1.06x slower                                                                                                   |
| async_tree_none            | 259 ms                                                                                                            | 276 ms: 1.07x slower                                                                                                    |
| pycparser                  | 1.10 sec                                                                                                          | 1.19 sec: 1.07x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 487 ms                                                                                                            | 524 ms: 1.08x slower                                                                                                    |
| mdp                        | 2.42 sec                                                                                                          | 2.60 sec: 1.08x slower                                                                                                  |
| float                      | 70.4 ms                                                                                                           | 76.1 ms: 1.08x slower                                                                                                   |
| bench_mp_pool              | 88.0 ms                                                                                                           | 95.7 ms: 1.09x slower                                                                                                   |
| async_tree_memoization     | 311 ms                                                                                                            | 340 ms: 1.09x slower                                                                                                    |
| dulwich_log                | 75.9 ms                                                                                                           | 83.0 ms: 1.09x slower                                                                                                   |
| logging_silent             | 102 ns                                                                                                            | 112 ns: 1.10x slower                                                                                                    |
| coroutines                 | 21.3 ms                                                                                                           | 23.4 ms: 1.10x slower                                                                                                   |
| docutils                   | 2.53 sec                                                                                                          | 2.80 sec: 1.11x slower                                                                                                  |
| sphinx                     | 968 ms                                                                                                            | 1.10 sec: 1.13x slower                                                                                                  |
| k_core                     | 2.03 sec                                                                                                          | 2.30 sec: 1.13x slower                                                                                                  |
| pylint                     | 274 ms                                                                                                            | 315 ms: 1.15x slower                                                                                                    |
| json_dumps                 | 11.2 ms                                                                                                           | 12.9 ms: 1.15x slower                                                                                                   |
| bpe_tokeniser              | 4.12 sec                                                                                                          | 4.78 sec: 1.16x slower                                                                                                  |
| many_optionals             | 1.00 ms                                                                                                           | 1.17 ms: 1.17x slower                                                                                                   |
| subparsers                 | 21.5 ms                                                                                                           | 25.2 ms: 1.17x slower                                                                                                   |
| xml_etree_generate         | 81.5 ms                                                                                                           | 95.7 ms: 1.17x slower                                                                                                   |
| async_generators           | 316 ms                                                                                                            | 373 ms: 1.18x slower                                                                                                    |
| generators                 | 26.6 ms                                                                                                           | 31.6 ms: 1.19x slower                                                                                                   |
| pickle_pure_python         | 304 us                                                                                                            | 362 us: 1.19x slower                                                                                                    |
| thrift                     | 741 us                                                                                                            | 883 us: 1.19x slower                                                                                                    |
| unpickle_pure_python       | 208 us                                                                                                            | 250 us: 1.20x slower                                                                                                    |
| logging_simple             | 5.92 us                                                                                                           | 7.17 us: 1.21x slower                                                                                                   |
| logging_format             | 6.71 us                                                                                                           | 8.17 us: 1.22x slower                                                                                                   |
| 2to3                       | 250 ms                                                                                                            | 305 ms: 1.22x slower                                                                                                    |
| sqlglot_optimize           | 50.4 ms                                                                                                           | 61.5 ms: 1.22x slower                                                                                                   |
| pprint_safe_repr           | 681 ms                                                                                                            | 832 ms: 1.22x slower                                                                                                    |
| scimark_sor                | 110 ms                                                                                                            | 135 ms: 1.23x slower                                                                                                    |
| xml_etree_process          | 56.8 ms                                                                                                           | 69.8 ms: 1.23x slower                                                                                                   |
| deltablue                  | 3.07 ms                                                                                                           | 3.77 ms: 1.23x slower                                                                                                   |
| coverage                   | 78.9 ms                                                                                                           | 97.2 ms: 1.23x slower                                                                                                   |
| pprint_pformat             | 1.39 sec                                                                                                          | 1.72 sec: 1.23x slower                                                                                                  |
| sympy_expand               | 446 ms                                                                                                            | 551 ms: 1.23x slower                                                                                                    |
| sqlalchemy_declarative     | 126 ms                                                                                                            | 156 ms: 1.24x slower                                                                                                    |
| sympy_sum                  | 150 ms                                                                                                            | 186 ms: 1.24x slower                                                                                                    |
| telco                      | 7.17 ms                                                                                                           | 8.90 ms: 1.24x slower                                                                                                   |
| comprehensions             | 16.0 us                                                                                                           | 19.8 us: 1.24x slower                                                                                                   |
| sympy_integrate            | 19.3 ms                                                                                                           | 24.0 ms: 1.25x slower                                                                                                   |
| sqlalchemy_imperative      | 18.9 ms                                                                                                           | 23.6 ms: 1.25x slower                                                                                                   |
| raytrace                   | 255 ms                                                                                                            | 318 ms: 1.25x slower                                                                                                    |
| sqlglot_transpile          | 1.52 ms                                                                                                           | 1.91 ms: 1.25x slower                                                                                                   |
| regex_compile              | 124 ms                                                                                                            | 155 ms: 1.25x slower                                                                                                    |
| sympy_str                  | 266 ms                                                                                                            | 336 ms: 1.26x slower                                                                                                    |
| deepcopy_reduce            | 2.52 us                                                                                                           | 3.18 us: 1.26x slower                                                                                                   |
| scimark_lu                 | 111 ms                                                                                                            | 140 ms: 1.27x slower                                                                                                    |
| go                         | 111 ms                                                                                                            | 140 ms: 1.27x slower                                                                                                    |
| spectral_norm              | 86.6 ms                                                                                                           | 110 ms: 1.27x slower                                                                                                    |
| scimark_fft                | 311 ms                                                                                                            | 397 ms: 1.28x slower                                                                                                    |
| genshi_xml                 | 47.1 ms                                                                                                           | 60.3 ms: 1.28x slower                                                                                                   |
| connected_components       | 387 ms                                                                                                            | 496 ms: 1.28x slower                                                                                                    |
| deepcopy                   | 244 us                                                                                                            | 313 us: 1.28x slower                                                                                                    |
| python_startup_no_site     | 7.54 ms                                                                                                           | 9.68 ms: 1.28x slower                                                                                                   |
| pyflate                    | 396 ms                                                                                                            | 509 ms: 1.28x slower                                                                                                    |
| sqlglot_parse              | 1.23 ms                                                                                                           | 1.58 ms: 1.29x slower                                                                                                   |
| tomli_loads                | 1.85 sec                                                                                                          | 2.38 sec: 1.29x slower                                                                                                  |
| shortest_path              | 426 ms                                                                                                            | 551 ms: 1.30x slower                                                                                                    |
| chaos                      | 53.7 ms                                                                                                           | 69.6 ms: 1.30x slower                                                                                                   |
| django_template            | 32.8 ms                                                                                                           | 42.6 ms: 1.30x slower                                                                                                   |
| nqueens                    | 74.6 ms                                                                                                           | 97.5 ms: 1.31x slower                                                                                                   |
| hexiom                     | 5.59 ms                                                                                                           | 7.32 ms: 1.31x slower                                                                                                   |
| typing_runtime_protocols   | 151 us                                                                                                            | 199 us: 1.32x slower                                                                                                    |
| richards                   | 41.4 ms                                                                                                           | 54.9 ms: 1.33x slower                                                                                                   |
| deepcopy_memo              | 28.7 us                                                                                                           | 38.0 us: 1.33x slower                                                                                                   |
| crypto_pyaes               | 65.9 ms                                                                                                           | 88.1 ms: 1.34x slower                                                                                                   |
| fannkuch                   | 367 ms                                                                                                            | 494 ms: 1.34x slower                                                                                                    |
| meteor_contest             | 95.8 ms                                                                                                           | 130 ms: 1.35x slower                                                                                                    |
| scimark_monte_carlo        | 61.7 ms                                                                                                           | 83.6 ms: 1.36x slower                                                                                                   |
| richards_super             | 47.0 ms                                                                                                           | 64.0 ms: 1.36x slower                                                                                                   |
| mako                       | 11.5 ms                                                                                                           | 15.8 ms: 1.37x slower                                                                                                   |
| genshi_text                | 20.3 ms                                                                                                           | 28.3 ms: 1.39x slower                                                                                                   |
| scimark_sparse_mat_mult    | 4.19 ms                                                                                                           | 5.84 ms: 1.39x slower                                                                                                   |
| nbody                      | 84.1 ms                                                                                                           | 136 ms: 1.61x slower                                                                                                    |
| bench_thread_pool          | 1.03 ms                                                                                                           | 3.31 ms: 3.23x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmark hidden because not significant (4): async_tree_memoization_tg, asyncio_websockets, json, xml_etree_parse
Ignored benchmarks (1) of results/bm-20250226-3.14.0a5+-fda056e-NOGIL/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json: html5lib

- Geometric mean (including insignificant results): 1.130x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.15x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.20x