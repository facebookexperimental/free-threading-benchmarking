# Results vs. base

- fork: python
- ref: 3a8cefba0b60bd25c6b1
- machine: linux-x86_64
- commit hash: 3a8cefb
- commit date: 2025-04-01
- overall geometric mean: 1.146x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250401-3.14.0a6+-3a8cefb/bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json | results/bm-20250401-3.14.0a6+-3a8cefb-NOGIL/bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                                                            | 312 ms: 1.22x slower                                                                                                    |
| docutils       | 2.61 sec                                                                                                          | 2.90 sec: 1.11x slower                                                                                                  |
| sphinx         | 1.01 sec                                                                                                          | 1.16 sec: 1.14x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250401-3.14.0a6+-3a8cefb/bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json | results/bm-20250401-3.14.0a6+-3a8cefb-NOGIL/bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 653 ms                                                                                                            | 570 ms: 1.14x faster                                                                                                    |
| async_tree_none_tg         | 266 ms                                                                                                            | 251 ms: 1.06x faster                                                                                                    |
| async_tree_io              | 638 ms                                                                                                            | 601 ms: 1.06x faster                                                                                                    |
| async_tree_memoization_tg  | 325 ms                                                                                                            | 314 ms: 1.04x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 508 ms                                                                                                            | 498 ms: 1.02x faster                                                                                                    |
| async_tree_cpu_io_mixed    | 518 ms                                                                                                            | 530 ms: 1.02x slower                                                                                                    |
| async_tree_memoization     | 327 ms                                                                                                            | 344 ms: 1.05x slower                                                                                                    |
| coroutines                 | 24.0 ms                                                                                                           | 26.9 ms: 1.12x slower                                                                                                   |
| async_generators           | 340 ms                                                                                                            | 392 ms: 1.15x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.00x slower                                                                                                            |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250401-3.14.0a6+-3a8cefb/bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json | results/bm-20250401-3.14.0a6+-3a8cefb-NOGIL/bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| float          | 73.2 ms                                                                                                           | 77.6 ms: 1.06x slower                                                                                                   |
| pidigits       | 197 ms                                                                                                            | 215 ms: 1.09x slower                                                                                                    |
| nbody          | 94.6 ms                                                                                                           | 139 ms: 1.47x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.19x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250401-3.14.0a6+-3a8cefb/bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json | results/bm-20250401-3.14.0a6+-3a8cefb-NOGIL/bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.2 ms                                                                                                           | 21.9 ms: 1.01x faster                                                                                                   |
| regex_effbot   | 2.82 ms                                                                                                           | 2.79 ms: 1.01x faster                                                                                                   |
| regex_compile  | 132 ms                                                                                                            | 171 ms: 1.29x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.06x slower                                                                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250401-3.14.0a6+-3a8cefb/bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json | results/bm-20250401-3.14.0a6+-3a8cefb-NOGIL/bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 130 ms                                                                                                            | 129 ms: 1.01x faster                                                                                                    |
| json_loads           | 27.1 us                                                                                                           | 30.8 us: 1.14x slower                                                                                                   |
| json_dumps           | 11.3 ms                                                                                                           | 13.3 ms: 1.18x slower                                                                                                   |
| xml_etree_generate   | 86.2 ms                                                                                                           | 102 ms: 1.19x slower                                                                                                    |
| pickle_pure_python   | 320 us                                                                                                            | 387 us: 1.21x slower                                                                                                    |
| unpickle_pure_python | 223 us                                                                                                            | 272 us: 1.22x slower                                                                                                    |
| xml_etree_process    | 61.3 ms                                                                                                           | 75.0 ms: 1.22x slower                                                                                                   |
| tomli_loads          | 2.02 sec                                                                                                          | 2.57 sec: 1.28x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                             | 1.15x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250401-3.14.0a6+-3a8cefb/bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json | results/bm-20250401-3.14.0a6+-3a8cefb-NOGIL/bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 15.1 ms                                                                                                           | 15.9 ms: 1.05x slower                                                                                                   |
| python_startup_no_site | 8.65 ms                                                                                                           | 11.2 ms: 1.29x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.17x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250401-3.14.0a6+-3a8cefb/bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json | results/bm-20250401-3.14.0a6+-3a8cefb-NOGIL/bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 36.6 ms                                                                                                           | 45.5 ms: 1.24x slower                                                                                                   |
| genshi_xml      | 50.3 ms                                                                                                           | 67.5 ms: 1.34x slower                                                                                                   |
| mako            | 12.2 ms                                                                                                           | 16.7 ms: 1.36x slower                                                                                                   |
| genshi_text     | 21.8 ms                                                                                                           | 31.7 ms: 1.45x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.35x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250401-3.14.0a6+-3a8cefb/bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json | results/bm-20250401-3.14.0a6+-3a8cefb-NOGIL/bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.19 ms                                                                                                           | 1.78 ms: 2.35x faster                                                                                                   |
| create_gc_cycles           | 1.84 ms                                                                                                           | 1.35 ms: 1.36x faster                                                                                                   |
| async_tree_io_tg           | 653 ms                                                                                                            | 570 ms: 1.14x faster                                                                                                    |
| async_tree_none_tg         | 266 ms                                                                                                            | 251 ms: 1.06x faster                                                                                                    |
| async_tree_io              | 638 ms                                                                                                            | 601 ms: 1.06x faster                                                                                                    |
| sqlite_synth               | 2.21 us                                                                                                           | 2.09 us: 1.06x faster                                                                                                   |
| async_tree_memoization_tg  | 325 ms                                                                                                            | 314 ms: 1.04x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 508 ms                                                                                                            | 498 ms: 1.02x faster                                                                                                    |
| regex_v8                   | 22.2 ms                                                                                                           | 21.9 ms: 1.01x faster                                                                                                   |
| regex_effbot               | 2.82 ms                                                                                                           | 2.79 ms: 1.01x faster                                                                                                   |
| xml_etree_parse            | 130 ms                                                                                                            | 129 ms: 1.01x faster                                                                                                    |
| async_tree_cpu_io_mixed    | 518 ms                                                                                                            | 530 ms: 1.02x slower                                                                                                    |
| pathlib                    | 19.4 ms                                                                                                           | 20.0 ms: 1.03x slower                                                                                                   |
| async_tree_memoization     | 327 ms                                                                                                            | 344 ms: 1.05x slower                                                                                                    |
| python_startup             | 15.1 ms                                                                                                           | 15.9 ms: 1.05x slower                                                                                                   |
| float                      | 73.2 ms                                                                                                           | 77.6 ms: 1.06x slower                                                                                                   |
| pycparser                  | 1.15 sec                                                                                                          | 1.26 sec: 1.09x slower                                                                                                  |
| pidigits                   | 197 ms                                                                                                            | 215 ms: 1.09x slower                                                                                                    |
| json                       | 4.91 ms                                                                                                           | 5.36 ms: 1.09x slower                                                                                                   |
| bench_mp_pool              | 90.1 ms                                                                                                           | 98.7 ms: 1.10x slower                                                                                                   |
| docutils                   | 2.61 sec                                                                                                          | 2.90 sec: 1.11x slower                                                                                                  |
| k_core                     | 2.06 sec                                                                                                          | 2.29 sec: 1.12x slower                                                                                                  |
| coroutines                 | 24.0 ms                                                                                                           | 26.9 ms: 1.12x slower                                                                                                   |
| bpe_tokeniser              | 4.36 sec                                                                                                          | 4.91 sec: 1.13x slower                                                                                                  |
| json_loads                 | 27.1 us                                                                                                           | 30.8 us: 1.14x slower                                                                                                   |
| sphinx                     | 1.01 sec                                                                                                          | 1.16 sec: 1.14x slower                                                                                                  |
| dulwich_log                | 68.7 ms                                                                                                           | 78.5 ms: 1.14x slower                                                                                                   |
| many_optionals             | 1.05 ms                                                                                                           | 1.21 ms: 1.15x slower                                                                                                   |
| async_generators           | 340 ms                                                                                                            | 392 ms: 1.15x slower                                                                                                    |
| pylint                     | 288 ms                                                                                                            | 332 ms: 1.15x slower                                                                                                    |
| json_dumps                 | 11.3 ms                                                                                                           | 13.3 ms: 1.18x slower                                                                                                   |
| scimark_fft                | 321 ms                                                                                                            | 380 ms: 1.18x slower                                                                                                    |
| subparsers                 | 22.8 ms                                                                                                           | 27.1 ms: 1.18x slower                                                                                                   |
| xml_etree_generate         | 86.2 ms                                                                                                           | 102 ms: 1.19x slower                                                                                                    |
| telco                      | 7.41 ms                                                                                                           | 8.84 ms: 1.19x slower                                                                                                   |
| pprint_safe_repr           | 737 ms                                                                                                            | 880 ms: 1.19x slower                                                                                                    |
| spectral_norm              | 99.1 ms                                                                                                           | 119 ms: 1.20x slower                                                                                                    |
| sqlglot_v2_optimize        | 54.0 ms                                                                                                           | 65.0 ms: 1.20x slower                                                                                                   |
| deepcopy_reduce            | 2.71 us                                                                                                           | 3.27 us: 1.20x slower                                                                                                   |
| scimark_lu                 | 118 ms                                                                                                            | 143 ms: 1.21x slower                                                                                                    |
| pickle_pure_python         | 320 us                                                                                                            | 387 us: 1.21x slower                                                                                                    |
| pprint_pformat             | 1.51 sec                                                                                                          | 1.83 sec: 1.21x slower                                                                                                  |
| 2to3                       | 256 ms                                                                                                            | 312 ms: 1.22x slower                                                                                                    |
| sqlglot_v2_normalize       | 108 ms                                                                                                            | 131 ms: 1.22x slower                                                                                                    |
| unpickle_pure_python       | 223 us                                                                                                            | 272 us: 1.22x slower                                                                                                    |
| scimark_sparse_mat_mult    | 4.46 ms                                                                                                           | 5.44 ms: 1.22x slower                                                                                                   |
| sympy_sum                  | 162 ms                                                                                                            | 198 ms: 1.22x slower                                                                                                    |
| xml_etree_process          | 61.3 ms                                                                                                           | 75.0 ms: 1.22x slower                                                                                                   |
| logging_silent             | 101 ns                                                                                                            | 124 ns: 1.23x slower                                                                                                    |
| sympy_integrate            | 19.9 ms                                                                                                           | 24.5 ms: 1.23x slower                                                                                                   |
| sqlalchemy_declarative     | 134 ms                                                                                                            | 166 ms: 1.23x slower                                                                                                    |
| sympy_expand               | 480 ms                                                                                                            | 593 ms: 1.24x slower                                                                                                    |
| sqlalchemy_imperative      | 20.5 ms                                                                                                           | 25.4 ms: 1.24x slower                                                                                                   |
| mdp                        | 1.18 sec                                                                                                          | 1.47 sec: 1.24x slower                                                                                                  |
| deepcopy                   | 260 us                                                                                                            | 324 us: 1.24x slower                                                                                                    |
| django_template            | 36.6 ms                                                                                                           | 45.5 ms: 1.24x slower                                                                                                   |
| nqueens                    | 81.8 ms                                                                                                           | 102 ms: 1.25x slower                                                                                                    |
| sympy_str                  | 283 ms                                                                                                            | 354 ms: 1.25x slower                                                                                                    |
| shortest_path              | 439 ms                                                                                                            | 556 ms: 1.26x slower                                                                                                    |
| sqlglot_v2_transpile       | 1.60 ms                                                                                                           | 2.03 ms: 1.27x slower                                                                                                   |
| tomli_loads                | 2.02 sec                                                                                                          | 2.57 sec: 1.28x slower                                                                                                  |
| pyflate                    | 417 ms                                                                                                            | 531 ms: 1.28x slower                                                                                                    |
| typing_runtime_protocols   | 161 us                                                                                                            | 206 us: 1.28x slower                                                                                                    |
| connected_components       | 399 ms                                                                                                            | 512 ms: 1.28x slower                                                                                                    |
| comprehensions             | 17.3 us                                                                                                           | 22.2 us: 1.28x slower                                                                                                   |
| regex_compile              | 132 ms                                                                                                            | 171 ms: 1.29x slower                                                                                                    |
| python_startup_no_site     | 8.65 ms                                                                                                           | 11.2 ms: 1.29x slower                                                                                                   |
| crypto_pyaes               | 70.5 ms                                                                                                           | 91.6 ms: 1.30x slower                                                                                                   |
| hexiom                     | 6.18 ms                                                                                                           | 8.09 ms: 1.31x slower                                                                                                   |
| raytrace                   | 260 ms                                                                                                            | 340 ms: 1.31x slower                                                                                                    |
| meteor_contest             | 102 ms                                                                                                            | 133 ms: 1.31x slower                                                                                                    |
| sqlglot_v2_parse           | 1.28 ms                                                                                                           | 1.68 ms: 1.31x slower                                                                                                   |
| chaos                      | 56.0 ms                                                                                                           | 73.5 ms: 1.31x slower                                                                                                   |
| fannkuch                   | 394 ms                                                                                                            | 519 ms: 1.32x slower                                                                                                    |
| scimark_monte_carlo        | 63.4 ms                                                                                                           | 84.2 ms: 1.33x slower                                                                                                   |
| scimark_sor                | 114 ms                                                                                                            | 153 ms: 1.34x slower                                                                                                    |
| deltablue                  | 3.36 ms                                                                                                           | 4.50 ms: 1.34x slower                                                                                                   |
| genshi_xml                 | 50.3 ms                                                                                                           | 67.5 ms: 1.34x slower                                                                                                   |
| go                         | 114 ms                                                                                                            | 154 ms: 1.35x slower                                                                                                    |
| deepcopy_memo              | 29.9 us                                                                                                           | 40.4 us: 1.35x slower                                                                                                   |
| mako                       | 12.2 ms                                                                                                           | 16.7 ms: 1.36x slower                                                                                                   |
| logging_simple             | 6.26 us                                                                                                           | 8.58 us: 1.37x slower                                                                                                   |
| richards_super             | 49.8 ms                                                                                                           | 69.1 ms: 1.39x slower                                                                                                   |
| logging_format             | 7.01 us                                                                                                           | 9.75 us: 1.39x slower                                                                                                   |
| richards                   | 43.7 ms                                                                                                           | 60.9 ms: 1.39x slower                                                                                                   |
| coverage                   | 79.4 ms                                                                                                           | 111 ms: 1.39x slower                                                                                                    |
| generators                 | 31.2 ms                                                                                                           | 44.3 ms: 1.42x slower                                                                                                   |
| genshi_text                | 21.8 ms                                                                                                           | 31.7 ms: 1.45x slower                                                                                                   |
| nbody                      | 94.6 ms                                                                                                           | 139 ms: 1.47x slower                                                                                                    |
| bench_thread_pool          | 1.06 ms                                                                                                           | 3.20 ms: 3.00x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.18x slower                                                                                                            |

Benchmark hidden because not significant (4): xml_etree_iterparse, asyncio_websockets, regex_dna, async_tree_none
Ignored benchmarks (1) of results/bm-20250401-3.14.0a6+-3a8cefb-NOGIL/bm-20250401-vultr-x86_64-python-3a8cefba0b60bd25c6b1-3.14.0a6+-3a8cefb.json: html5lib

- Geometric mean (including insignificant results): 1.146x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.16x
- 95% likely to have a slowdown of 1.15x
- 99% likely to have a slowdown of 1.13x

# Memory
- memory change: 1.20x