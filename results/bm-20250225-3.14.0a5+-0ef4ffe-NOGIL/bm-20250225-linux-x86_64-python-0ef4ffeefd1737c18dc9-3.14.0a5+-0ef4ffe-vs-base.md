# Results vs. base

- fork: python
- ref: 0ef4ffeefd1737c18dc9
- machine: linux-x86_64
- commit hash: 0ef4ffe
- commit date: 2025-02-25
- overall geometric mean: 1.105x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250225-3.14.0a5+-0ef4ffe/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json | results/bm-20250225-3.14.0a5+-0ef4ffe-NOGIL/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 469 ms                                                                                                            | 514 ms: 1.10x slower                                                                                                    |
| docutils       | 3.74 sec                                                                                                          | 4.22 sec: 1.13x slower                                                                                                  |
| html5lib       | 83.7 ms                                                                                                           | 98.2 ms: 1.17x slower                                                                                                   |
| sphinx         | 1.41 sec                                                                                                          | 1.62 sec: 1.15x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.14x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | results/bm-20250225-3.14.0a5+-0ef4ffe/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json | results/bm-20250225-3.14.0a5+-0ef4ffe-NOGIL/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json |
|---------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg          | 967 ms                                                                                                            | 726 ms: 1.33x faster                                                                                                    |
| async_tree_none_tg        | 368 ms                                                                                                            | 334 ms: 1.10x faster                                                                                                    |
| async_tree_io             | 885 ms                                                                                                            | 822 ms: 1.08x faster                                                                                                    |
| async_tree_memoization_tg | 485 ms                                                                                                            | 459 ms: 1.06x faster                                                                                                    |
| asyncio_websockets        | 770 ms                                                                                                            | 742 ms: 1.04x faster                                                                                                    |
| coroutines                | 29.5 ms                                                                                                           | 30.8 ms: 1.04x slower                                                                                                   |
| async_tree_none           | 383 ms                                                                                                            | 406 ms: 1.06x slower                                                                                                    |
| async_generators          | 507 ms                                                                                                            | 556 ms: 1.10x slower                                                                                                    |
| async_tree_cpu_io_mixed   | 675 ms                                                                                                            | 758 ms: 1.12x slower                                                                                                    |
| Geometric mean            | (ref)                                                                                                             | 1.02x faster                                                                                                            |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250225-3.14.0a5+-0ef4ffe/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json | results/bm-20250225-3.14.0a5+-0ef4ffe-NOGIL/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| nbody          | 125 ms                                                                                                            | 174 ms: 1.39x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmark hidden because not significant (2): float, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250225-3.14.0a5+-0ef4ffe/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json | results/bm-20250225-3.14.0a5+-0ef4ffe-NOGIL/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 37.0 ms                                                                                                           | 32.0 ms: 1.16x faster                                                                                                   |
| regex_effbot   | 4.94 ms                                                                                                           | 4.50 ms: 1.10x faster                                                                                                   |
| regex_dna      | 291 ms                                                                                                            | 277 ms: 1.05x faster                                                                                                    |
| regex_compile  | 164 ms                                                                                                            | 197 ms: 1.20x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.03x faster                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250225-3.14.0a5+-0ef4ffe/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json | results/bm-20250225-3.14.0a5+-0ef4ffe-NOGIL/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_generate   | 118 ms                                                                                                            | 123 ms: 1.04x slower                                                                                                    |
| xml_etree_process    | 83.2 ms                                                                                                           | 88.5 ms: 1.06x slower                                                                                                   |
| unpickle_pure_python | 295 us                                                                                                            | 315 us: 1.07x slower                                                                                                    |
| json_loads           | 40.3 us                                                                                                           | 43.4 us: 1.08x slower                                                                                                   |
| xml_etree_parse      | 192 ms                                                                                                            | 222 ms: 1.16x slower                                                                                                    |
| json_dumps           | 15.2 ms                                                                                                           | 17.8 ms: 1.17x slower                                                                                                   |
| tomli_loads          | 2.51 sec                                                                                                          | 3.07 sec: 1.22x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                             | 1.08x slower                                                                                                            |

Benchmark hidden because not significant (2): pickle_pure_python, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250225-3.14.0a5+-0ef4ffe/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json | results/bm-20250225-3.14.0a5+-0ef4ffe-NOGIL/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 27.8 ms                                                                                                           | 33.2 ms: 1.20x slower                                                                                                   |
| python_startup_no_site | 16.1 ms                                                                                                           | 21.3 ms: 1.32x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.26x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250225-3.14.0a5+-0ef4ffe/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json | results/bm-20250225-3.14.0a5+-0ef4ffe-NOGIL/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_text     | 31.1 ms                                                                                                           | 37.2 ms: 1.20x slower                                                                                                   |
| genshi_xml      | 68.5 ms                                                                                                           | 84.1 ms: 1.23x slower                                                                                                   |
| django_template | 44.2 ms                                                                                                           | 55.1 ms: 1.25x slower                                                                                                   |
| mako            | 15.8 ms                                                                                                           | 23.2 ms: 1.47x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.28x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                 | results/bm-20250225-3.14.0a5+-0ef4ffe/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json | results/bm-20250225-3.14.0a5+-0ef4ffe-NOGIL/bm-20250225-linux-x86_64-python-0ef4ffeefd1737c18dc9-3.14.0a5+-0ef4ffe.json |
|---------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal              | 7.80 ms                                                                                                           | 3.72 ms: 2.10x faster                                                                                                   |
| create_gc_cycles          | 4.16 ms                                                                                                           | 2.48 ms: 1.68x faster                                                                                                   |
| async_tree_io_tg          | 967 ms                                                                                                            | 726 ms: 1.33x faster                                                                                                    |
| regex_v8                  | 37.0 ms                                                                                                           | 32.0 ms: 1.16x faster                                                                                                   |
| sqlite_synth              | 3.89 us                                                                                                           | 3.44 us: 1.13x faster                                                                                                   |
| async_tree_none_tg        | 368 ms                                                                                                            | 334 ms: 1.10x faster                                                                                                    |
| bench_mp_pool             | 96.3 ms                                                                                                           | 87.6 ms: 1.10x faster                                                                                                   |
| regex_effbot              | 4.94 ms                                                                                                           | 4.50 ms: 1.10x faster                                                                                                   |
| async_tree_io             | 885 ms                                                                                                            | 822 ms: 1.08x faster                                                                                                    |
| async_tree_memoization_tg | 485 ms                                                                                                            | 459 ms: 1.06x faster                                                                                                    |
| regex_dna                 | 291 ms                                                                                                            | 277 ms: 1.05x faster                                                                                                    |
| asyncio_websockets        | 770 ms                                                                                                            | 742 ms: 1.04x faster                                                                                                    |
| xml_etree_generate        | 118 ms                                                                                                            | 123 ms: 1.04x slower                                                                                                    |
| coroutines                | 29.5 ms                                                                                                           | 30.8 ms: 1.04x slower                                                                                                   |
| json                      | 7.15 ms                                                                                                           | 7.46 ms: 1.04x slower                                                                                                   |
| async_tree_none           | 383 ms                                                                                                            | 406 ms: 1.06x slower                                                                                                    |
| xml_etree_process         | 83.2 ms                                                                                                           | 88.5 ms: 1.06x slower                                                                                                   |
| k_core                    | 4.16 sec                                                                                                          | 4.44 sec: 1.07x slower                                                                                                  |
| unpickle_pure_python      | 295 us                                                                                                            | 315 us: 1.07x slower                                                                                                    |
| deepcopy_reduce           | 3.96 us                                                                                                           | 4.25 us: 1.07x slower                                                                                                   |
| sqlglot_optimize          | 74.7 ms                                                                                                           | 80.3 ms: 1.08x slower                                                                                                   |
| pathlib                   | 30.2 ms                                                                                                           | 32.5 ms: 1.08x slower                                                                                                   |
| json_loads                | 40.3 us                                                                                                           | 43.4 us: 1.08x slower                                                                                                   |
| 2to3                      | 469 ms                                                                                                            | 514 ms: 1.10x slower                                                                                                    |
| async_generators          | 507 ms                                                                                                            | 556 ms: 1.10x slower                                                                                                    |
| scimark_sor               | 160 ms                                                                                                            | 176 ms: 1.10x slower                                                                                                    |
| many_optionals            | 1.37 ms                                                                                                           | 1.50 ms: 1.10x slower                                                                                                   |
| pylint                    | 410 ms                                                                                                            | 458 ms: 1.12x slower                                                                                                    |
| async_tree_cpu_io_mixed   | 675 ms                                                                                                            | 758 ms: 1.12x slower                                                                                                    |
| docutils                  | 3.74 sec                                                                                                          | 4.22 sec: 1.13x slower                                                                                                  |
| mdp                       | 3.62 sec                                                                                                          | 4.11 sec: 1.13x slower                                                                                                  |
| richards                  | 62.4 ms                                                                                                           | 71.2 ms: 1.14x slower                                                                                                   |
| sphinx                    | 1.41 sec                                                                                                          | 1.62 sec: 1.15x slower                                                                                                  |
| shortest_path             | 921 ms                                                                                                            | 1.06 sec: 1.15x slower                                                                                                  |
| xml_etree_parse           | 192 ms                                                                                                            | 222 ms: 1.16x slower                                                                                                    |
| go                        | 156 ms                                                                                                            | 181 ms: 1.16x slower                                                                                                    |
| meteor_contest            | 148 ms                                                                                                            | 173 ms: 1.17x slower                                                                                                    |
| generators                | 40.3 ms                                                                                                           | 47.0 ms: 1.17x slower                                                                                                   |
| scimark_lu                | 152 ms                                                                                                            | 177 ms: 1.17x slower                                                                                                    |
| json_dumps                | 15.2 ms                                                                                                           | 17.8 ms: 1.17x slower                                                                                                   |
| html5lib                  | 83.7 ms                                                                                                           | 98.2 ms: 1.17x slower                                                                                                   |
| logging_format            | 8.69 us                                                                                                           | 10.2 us: 1.18x slower                                                                                                   |
| comprehensions            | 22.8 us                                                                                                           | 26.9 us: 1.18x slower                                                                                                   |
| deepcopy                  | 341 us                                                                                                            | 404 us: 1.18x slower                                                                                                    |
| scimark_sparse_mat_mult   | 6.78 ms                                                                                                           | 8.05 ms: 1.19x slower                                                                                                   |
| telco                     | 10.2 ms                                                                                                           | 12.2 ms: 1.19x slower                                                                                                   |
| thrift                    | 1.00 ms                                                                                                           | 1.19 ms: 1.19x slower                                                                                                   |
| python_startup            | 27.8 ms                                                                                                           | 33.2 ms: 1.20x slower                                                                                                   |
| genshi_text               | 31.1 ms                                                                                                           | 37.2 ms: 1.20x slower                                                                                                   |
| regex_compile             | 164 ms                                                                                                            | 197 ms: 1.20x slower                                                                                                    |
| sympy_str                 | 359 ms                                                                                                            | 430 ms: 1.20x slower                                                                                                    |
| spectral_norm             | 123 ms                                                                                                            | 147 ms: 1.20x slower                                                                                                    |
| sympy_expand              | 590 ms                                                                                                            | 711 ms: 1.21x slower                                                                                                    |
| logging_simple            | 7.65 us                                                                                                           | 9.25 us: 1.21x slower                                                                                                   |
| pprint_pformat            | 1.87 sec                                                                                                          | 2.29 sec: 1.22x slower                                                                                                  |
| tomli_loads               | 2.51 sec                                                                                                          | 3.07 sec: 1.22x slower                                                                                                  |
| genshi_xml                | 68.5 ms                                                                                                           | 84.1 ms: 1.23x slower                                                                                                   |
| sqlalchemy_imperative     | 23.9 ms                                                                                                           | 29.3 ms: 1.23x slower                                                                                                   |
| pprint_safe_repr          | 931 ms                                                                                                            | 1.15 sec: 1.23x slower                                                                                                  |
| sympy_integrate           | 27.3 ms                                                                                                           | 33.8 ms: 1.24x slower                                                                                                   |
| deepcopy_memo             | 43.2 us                                                                                                           | 53.5 us: 1.24x slower                                                                                                   |
| scimark_fft               | 431 ms                                                                                                            | 533 ms: 1.24x slower                                                                                                    |
| sympy_sum                 | 197 ms                                                                                                            | 245 ms: 1.24x slower                                                                                                    |
| django_template           | 44.2 ms                                                                                                           | 55.1 ms: 1.25x slower                                                                                                   |
| connected_components      | 797 ms                                                                                                            | 999 ms: 1.25x slower                                                                                                    |
| coverage                  | 116 ms                                                                                                            | 146 ms: 1.26x slower                                                                                                    |
| chaos                     | 74.1 ms                                                                                                           | 94.1 ms: 1.27x slower                                                                                                   |
| crypto_pyaes              | 94.4 ms                                                                                                           | 120 ms: 1.27x slower                                                                                                    |
| subparsers                | 27.9 ms                                                                                                           | 35.5 ms: 1.27x slower                                                                                                   |
| pyflate                   | 599 ms                                                                                                            | 765 ms: 1.28x slower                                                                                                    |
| sqlglot_transpile         | 2.00 ms                                                                                                           | 2.55 ms: 1.28x slower                                                                                                   |
| hexiom                    | 8.17 ms                                                                                                           | 10.5 ms: 1.28x slower                                                                                                   |
| bench_thread_pool         | 3.17 ms                                                                                                           | 4.06 ms: 1.28x slower                                                                                                   |
| raytrace                  | 346 ms                                                                                                            | 443 ms: 1.28x slower                                                                                                    |
| scimark_monte_carlo       | 84.1 ms                                                                                                           | 108 ms: 1.29x slower                                                                                                    |
| bpe_tokeniser             | 5.86 sec                                                                                                          | 7.55 sec: 1.29x slower                                                                                                  |
| nqueens                   | 106 ms                                                                                                            | 137 ms: 1.29x slower                                                                                                    |
| richards_super            | 64.4 ms                                                                                                           | 83.4 ms: 1.29x slower                                                                                                   |
| fannkuch                  | 528 ms                                                                                                            | 684 ms: 1.30x slower                                                                                                    |
| sqlglot_parse             | 1.71 ms                                                                                                           | 2.22 ms: 1.30x slower                                                                                                   |
| deltablue                 | 4.10 ms                                                                                                           | 5.40 ms: 1.32x slower                                                                                                   |
| python_startup_no_site    | 16.1 ms                                                                                                           | 21.3 ms: 1.32x slower                                                                                                   |
| sqlalchemy_declarative    | 172 ms                                                                                                            | 235 ms: 1.37x slower                                                                                                    |
| nbody                     | 125 ms                                                                                                            | 174 ms: 1.39x slower                                                                                                    |
| typing_runtime_protocols  | 201 us                                                                                                            | 289 us: 1.44x slower                                                                                                    |
| mako                      | 15.8 ms                                                                                                           | 23.2 ms: 1.47x slower                                                                                                   |
| Geometric mean            | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmark hidden because not significant (10): pickle_pure_python, pycparser, xml_etree_iterparse, float, dulwich_log, pidigits, logging_silent, async_tree_cpu_io_mixed_tg, sqlglot_normalize, async_tree_memoization

- Geometric mean (including insignificant results): 1.105x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.19x