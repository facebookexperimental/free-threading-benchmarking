# Results vs. base

- fork: python
- ref: 0dbaeb94a8b39972ebda
- machine: linux-x86_64
- commit hash: 0dbaeb9
- commit date: 2025-04-03
- overall geometric mean: 1.141x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250403-3.14.0a6+-0dbaeb9/bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json | results/bm-20250403-3.14.0a6+-0dbaeb9-NOGIL/bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                                                            | 311 ms: 1.22x slower                                                                                                    |
| docutils       | 2.60 sec                                                                                                          | 2.90 sec: 1.11x slower                                                                                                  |
| sphinx         | 1.01 sec                                                                                                          | 1.15 sec: 1.14x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250403-3.14.0a6+-0dbaeb9/bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json | results/bm-20250403-3.14.0a6+-0dbaeb9-NOGIL/bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 630 ms                                                                                                            | 574 ms: 1.10x faster                                                                                                    |
| async_tree_none_tg         | 271 ms                                                                                                            | 251 ms: 1.08x faster                                                                                                    |
| async_tree_io              | 638 ms                                                                                                            | 604 ms: 1.06x faster                                                                                                    |
| async_tree_memoization_tg  | 332 ms                                                                                                            | 317 ms: 1.05x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 510 ms                                                                                                            | 499 ms: 1.02x faster                                                                                                    |
| async_tree_cpu_io_mixed    | 516 ms                                                                                                            | 530 ms: 1.03x slower                                                                                                    |
| async_tree_memoization     | 327 ms                                                                                                            | 347 ms: 1.06x slower                                                                                                    |
| coroutines                 | 24.0 ms                                                                                                           | 27.2 ms: 1.13x slower                                                                                                   |
| async_generators           | 336 ms                                                                                                            | 392 ms: 1.17x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.01x slower                                                                                                            |

Benchmark hidden because not significant (2): async_tree_none, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250403-3.14.0a6+-0dbaeb9/bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json | results/bm-20250403-3.14.0a6+-0dbaeb9-NOGIL/bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| float          | 72.0 ms                                                                                                           | 77.1 ms: 1.07x slower                                                                                                   |
| pidigits       | 191 ms                                                                                                            | 210 ms: 1.10x slower                                                                                                    |
| nbody          | 92.5 ms                                                                                                           | 135 ms: 1.46x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.20x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250403-3.14.0a6+-0dbaeb9/bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json | results/bm-20250403-3.14.0a6+-0dbaeb9-NOGIL/bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.0 ms                                                                                                           | 21.3 ms: 1.03x faster                                                                                                   |
| regex_effbot   | 2.78 ms                                                                                                           | 2.72 ms: 1.02x faster                                                                                                   |
| regex_dna      | 176 ms                                                                                                            | 177 ms: 1.00x slower                                                                                                    |
| regex_compile  | 131 ms                                                                                                            | 170 ms: 1.30x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.05x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250403-3.14.0a6+-0dbaeb9/bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json | results/bm-20250403-3.14.0a6+-0dbaeb9-NOGIL/bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| json_loads           | 27.5 us                                                                                                           | 29.6 us: 1.08x slower                                                                                                   |
| json_dumps           | 11.2 ms                                                                                                           | 13.1 ms: 1.17x slower                                                                                                   |
| xml_etree_generate   | 86.9 ms                                                                                                           | 102 ms: 1.17x slower                                                                                                    |
| pickle_pure_python   | 321 us                                                                                                            | 378 us: 1.18x slower                                                                                                    |
| xml_etree_process    | 61.4 ms                                                                                                           | 74.1 ms: 1.21x slower                                                                                                   |
| unpickle_pure_python | 223 us                                                                                                            | 270 us: 1.21x slower                                                                                                    |
| tomli_loads          | 2.01 sec                                                                                                          | 2.53 sec: 1.26x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                             | 1.14x slower                                                                                                            |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250403-3.14.0a6+-0dbaeb9/bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json | results/bm-20250403-3.14.0a6+-0dbaeb9-NOGIL/bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 15.2 ms                                                                                                           | 15.9 ms: 1.05x slower                                                                                                   |
| python_startup_no_site | 8.72 ms                                                                                                           | 11.2 ms: 1.28x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250403-3.14.0a6+-0dbaeb9/bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json | results/bm-20250403-3.14.0a6+-0dbaeb9-NOGIL/bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 36.8 ms                                                                                                           | 44.6 ms: 1.21x slower                                                                                                   |
| genshi_xml      | 50.7 ms                                                                                                           | 67.5 ms: 1.33x slower                                                                                                   |
| mako            | 12.2 ms                                                                                                           | 16.5 ms: 1.35x slower                                                                                                   |
| genshi_text     | 22.2 ms                                                                                                           | 31.5 ms: 1.42x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.33x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250403-3.14.0a6+-0dbaeb9/bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json | results/bm-20250403-3.14.0a6+-0dbaeb9-NOGIL/bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.64 ms                                                                                                           | 1.79 ms: 2.59x faster                                                                                                   |
| create_gc_cycles           | 1.86 ms                                                                                                           | 1.35 ms: 1.37x faster                                                                                                   |
| async_tree_io_tg           | 630 ms                                                                                                            | 574 ms: 1.10x faster                                                                                                    |
| async_tree_none_tg         | 271 ms                                                                                                            | 251 ms: 1.08x faster                                                                                                    |
| sqlite_synth               | 2.19 us                                                                                                           | 2.04 us: 1.07x faster                                                                                                   |
| async_tree_io              | 638 ms                                                                                                            | 604 ms: 1.06x faster                                                                                                    |
| async_tree_memoization_tg  | 332 ms                                                                                                            | 317 ms: 1.05x faster                                                                                                    |
| regex_v8                   | 22.0 ms                                                                                                           | 21.3 ms: 1.03x faster                                                                                                   |
| regex_effbot               | 2.78 ms                                                                                                           | 2.72 ms: 1.02x faster                                                                                                   |
| async_tree_cpu_io_mixed_tg | 510 ms                                                                                                            | 499 ms: 1.02x faster                                                                                                    |
| regex_dna                  | 176 ms                                                                                                            | 177 ms: 1.00x slower                                                                                                    |
| pathlib                    | 19.4 ms                                                                                                           | 19.9 ms: 1.03x slower                                                                                                   |
| async_tree_cpu_io_mixed    | 516 ms                                                                                                            | 530 ms: 1.03x slower                                                                                                    |
| json                       | 4.90 ms                                                                                                           | 5.13 ms: 1.05x slower                                                                                                   |
| python_startup             | 15.2 ms                                                                                                           | 15.9 ms: 1.05x slower                                                                                                   |
| async_tree_memoization     | 327 ms                                                                                                            | 347 ms: 1.06x slower                                                                                                    |
| float                      | 72.0 ms                                                                                                           | 77.1 ms: 1.07x slower                                                                                                   |
| json_loads                 | 27.5 us                                                                                                           | 29.6 us: 1.08x slower                                                                                                   |
| pycparser                  | 1.15 sec                                                                                                          | 1.23 sec: 1.08x slower                                                                                                  |
| bench_mp_pool              | 89.7 ms                                                                                                           | 97.1 ms: 1.08x slower                                                                                                   |
| pidigits                   | 191 ms                                                                                                            | 210 ms: 1.10x slower                                                                                                    |
| k_core                     | 2.06 sec                                                                                                          | 2.29 sec: 1.11x slower                                                                                                  |
| docutils                   | 2.60 sec                                                                                                          | 2.90 sec: 1.11x slower                                                                                                  |
| bpe_tokeniser              | 4.40 sec                                                                                                          | 4.94 sec: 1.12x slower                                                                                                  |
| coroutines                 | 24.0 ms                                                                                                           | 27.2 ms: 1.13x slower                                                                                                   |
| dulwich_log                | 68.6 ms                                                                                                           | 78.2 ms: 1.14x slower                                                                                                   |
| sphinx                     | 1.01 sec                                                                                                          | 1.15 sec: 1.14x slower                                                                                                  |
| pylint                     | 289 ms                                                                                                            | 332 ms: 1.15x slower                                                                                                    |
| async_generators           | 336 ms                                                                                                            | 392 ms: 1.17x slower                                                                                                    |
| many_optionals             | 1.04 ms                                                                                                           | 1.22 ms: 1.17x slower                                                                                                   |
| json_dumps                 | 11.2 ms                                                                                                           | 13.1 ms: 1.17x slower                                                                                                   |
| xml_etree_generate         | 86.9 ms                                                                                                           | 102 ms: 1.17x slower                                                                                                    |
| telco                      | 7.45 ms                                                                                                           | 8.75 ms: 1.17x slower                                                                                                   |
| scimark_sparse_mat_mult    | 4.69 ms                                                                                                           | 5.51 ms: 1.18x slower                                                                                                   |
| pprint_safe_repr           | 742 ms                                                                                                            | 876 ms: 1.18x slower                                                                                                    |
| pickle_pure_python         | 321 us                                                                                                            | 378 us: 1.18x slower                                                                                                    |
| scimark_fft                | 325 ms                                                                                                            | 384 ms: 1.18x slower                                                                                                    |
| pprint_pformat             | 1.52 sec                                                                                                          | 1.81 sec: 1.19x slower                                                                                                  |
| scimark_lu                 | 118 ms                                                                                                            | 141 ms: 1.20x slower                                                                                                    |
| xml_etree_process          | 61.4 ms                                                                                                           | 74.1 ms: 1.21x slower                                                                                                   |
| subparsers                 | 22.4 ms                                                                                                           | 27.0 ms: 1.21x slower                                                                                                   |
| unpickle_pure_python       | 223 us                                                                                                            | 270 us: 1.21x slower                                                                                                    |
| sqlglot_v2_optimize        | 53.9 ms                                                                                                           | 65.2 ms: 1.21x slower                                                                                                   |
| django_template            | 36.8 ms                                                                                                           | 44.6 ms: 1.21x slower                                                                                                   |
| sqlalchemy_imperative      | 20.8 ms                                                                                                           | 25.3 ms: 1.21x slower                                                                                                   |
| sqlglot_v2_normalize       | 108 ms                                                                                                            | 131 ms: 1.21x slower                                                                                                    |
| 2to3                       | 255 ms                                                                                                            | 311 ms: 1.22x slower                                                                                                    |
| sympy_sum                  | 160 ms                                                                                                            | 196 ms: 1.22x slower                                                                                                    |
| sqlalchemy_declarative     | 134 ms                                                                                                            | 164 ms: 1.22x slower                                                                                                    |
| spectral_norm              | 98.5 ms                                                                                                           | 121 ms: 1.22x slower                                                                                                    |
| sympy_integrate            | 19.8 ms                                                                                                           | 24.3 ms: 1.23x slower                                                                                                   |
| logging_silent             | 102 ns                                                                                                            | 125 ns: 1.23x slower                                                                                                    |
| sympy_expand               | 479 ms                                                                                                            | 590 ms: 1.23x slower                                                                                                    |
| mdp                        | 1.18 sec                                                                                                          | 1.46 sec: 1.24x slower                                                                                                  |
| deepcopy_reduce            | 2.70 us                                                                                                           | 3.34 us: 1.24x slower                                                                                                   |
| nqueens                    | 81.7 ms                                                                                                           | 102 ms: 1.25x slower                                                                                                    |
| sympy_str                  | 283 ms                                                                                                            | 354 ms: 1.25x slower                                                                                                    |
| shortest_path              | 443 ms                                                                                                            | 556 ms: 1.25x slower                                                                                                    |
| deepcopy                   | 262 us                                                                                                            | 329 us: 1.26x slower                                                                                                    |
| sqlglot_v2_transpile       | 1.60 ms                                                                                                           | 2.01 ms: 1.26x slower                                                                                                   |
| tomli_loads                | 2.01 sec                                                                                                          | 2.53 sec: 1.26x slower                                                                                                  |
| pyflate                    | 419 ms                                                                                                            | 533 ms: 1.27x slower                                                                                                    |
| comprehensions             | 17.2 us                                                                                                           | 21.9 us: 1.27x slower                                                                                                   |
| crypto_pyaes               | 70.9 ms                                                                                                           | 90.7 ms: 1.28x slower                                                                                                   |
| python_startup_no_site     | 8.72 ms                                                                                                           | 11.2 ms: 1.28x slower                                                                                                   |
| connected_components       | 398 ms                                                                                                            | 513 ms: 1.29x slower                                                                                                    |
| sqlglot_v2_parse           | 1.29 ms                                                                                                           | 1.66 ms: 1.29x slower                                                                                                   |
| chaos                      | 56.2 ms                                                                                                           | 72.9 ms: 1.30x slower                                                                                                   |
| regex_compile              | 131 ms                                                                                                            | 170 ms: 1.30x slower                                                                                                    |
| typing_runtime_protocols   | 162 us                                                                                                            | 210 us: 1.30x slower                                                                                                    |
| fannkuch                   | 395 ms                                                                                                            | 515 ms: 1.31x slower                                                                                                    |
| raytrace                   | 257 ms                                                                                                            | 337 ms: 1.31x slower                                                                                                    |
| hexiom                     | 6.18 ms                                                                                                           | 8.15 ms: 1.32x slower                                                                                                   |
| scimark_monte_carlo        | 63.4 ms                                                                                                           | 84.0 ms: 1.32x slower                                                                                                   |
| deltablue                  | 3.36 ms                                                                                                           | 4.47 ms: 1.33x slower                                                                                                   |
| genshi_xml                 | 50.7 ms                                                                                                           | 67.5 ms: 1.33x slower                                                                                                   |
| go                         | 115 ms                                                                                                            | 153 ms: 1.33x slower                                                                                                    |
| scimark_sor                | 114 ms                                                                                                            | 152 ms: 1.33x slower                                                                                                    |
| meteor_contest             | 102 ms                                                                                                            | 137 ms: 1.34x slower                                                                                                    |
| mako                       | 12.2 ms                                                                                                           | 16.5 ms: 1.35x slower                                                                                                   |
| deepcopy_memo              | 29.9 us                                                                                                           | 40.4 us: 1.35x slower                                                                                                   |
| richards_super             | 50.5 ms                                                                                                           | 68.3 ms: 1.35x slower                                                                                                   |
| logging_simple             | 6.21 us                                                                                                           | 8.46 us: 1.36x slower                                                                                                   |
| richards                   | 44.1 ms                                                                                                           | 60.4 ms: 1.37x slower                                                                                                   |
| coverage                   | 80.3 ms                                                                                                           | 110 ms: 1.37x slower                                                                                                    |
| logging_format             | 6.94 us                                                                                                           | 9.66 us: 1.39x slower                                                                                                   |
| genshi_text                | 22.2 ms                                                                                                           | 31.5 ms: 1.42x slower                                                                                                   |
| generators                 | 31.1 ms                                                                                                           | 44.1 ms: 1.42x slower                                                                                                   |
| nbody                      | 92.5 ms                                                                                                           | 135 ms: 1.46x slower                                                                                                    |
| bench_thread_pool          | 1.06 ms                                                                                                           | 3.19 ms: 3.00x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.18x slower                                                                                                            |

Benchmark hidden because not significant (4): async_tree_none, xml_etree_parse, asyncio_websockets, xml_etree_iterparse
Ignored benchmarks (1) of results/bm-20250403-3.14.0a6+-0dbaeb9-NOGIL/bm-20250403-vultr-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json: html5lib

- Geometric mean (including insignificant results): 1.141x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.16x
- 95% likely to have a slowdown of 1.15x
- 99% likely to have a slowdown of 1.13x

# Memory
- memory change: 1.20x