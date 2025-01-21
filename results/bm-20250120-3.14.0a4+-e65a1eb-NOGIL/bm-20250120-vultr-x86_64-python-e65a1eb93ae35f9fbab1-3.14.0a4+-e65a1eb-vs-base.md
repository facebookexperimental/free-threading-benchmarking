# Results vs. base

- fork: python
- ref: e65a1eb93ae35f9fbab1
- machine: linux-x86_64
- commit hash: e65a1eb
- commit date: 2025-01-20
- overall geometric mean: 1.158x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250120-3.14.0a4+-e65a1eb/bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json | results/bm-20250120-3.14.0a4+-e65a1eb-NOGIL/bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 254 ms                                                                                                            | 314 ms: 1.24x slower                                                                                                    |
| docutils       | 2.55 sec                                                                                                          | 2.86 sec: 1.12x slower                                                                                                  |
| sphinx         | 983 ms                                                                                                            | 1.14 sec: 1.15x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.17x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250120-3.14.0a4+-e65a1eb/bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json | results/bm-20250120-3.14.0a4+-e65a1eb-NOGIL/bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_none_tg         | 256 ms                                                                                                            | 245 ms: 1.05x faster                                                                                                    |
| async_tree_io_tg           | 610 ms                                                                                                            | 584 ms: 1.04x faster                                                                                                    |
| asyncio_websockets         | 523 ms                                                                                                            | 518 ms: 1.01x faster                                                                                                    |
| async_tree_memoization_tg  | 306 ms                                                                                                            | 315 ms: 1.03x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 481 ms                                                                                                            | 505 ms: 1.05x slower                                                                                                    |
| async_tree_none            | 263 ms                                                                                                            | 286 ms: 1.09x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 493 ms                                                                                                            | 538 ms: 1.09x slower                                                                                                    |
| async_tree_memoization     | 319 ms                                                                                                            | 353 ms: 1.11x slower                                                                                                    |
| coroutines                 | 22.1 ms                                                                                                           | 25.0 ms: 1.13x slower                                                                                                   |
| async_generators           | 318 ms                                                                                                            | 377 ms: 1.18x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.05x slower                                                                                                            |

Benchmark hidden because not significant (1): async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250120-3.14.0a4+-e65a1eb/bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json | results/bm-20250120-3.14.0a4+-e65a1eb-NOGIL/bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 207 ms                                                                                                            | 198 ms: 1.04x faster                                                                                                    |
| float          | 69.8 ms                                                                                                           | 78.9 ms: 1.13x slower                                                                                                   |
| nbody          | 91.2 ms                                                                                                           | 137 ms: 1.50x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.18x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250120-3.14.0a4+-e65a1eb/bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json | results/bm-20250120-3.14.0a4+-e65a1eb-NOGIL/bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 23.5 ms                                                                                                           | 24.1 ms: 1.03x slower                                                                                                   |
| regex_dna      | 169 ms                                                                                                            | 187 ms: 1.10x slower                                                                                                    |
| regex_effbot   | 2.60 ms                                                                                                           | 2.86 ms: 1.10x slower                                                                                                   |
| regex_compile  | 127 ms                                                                                                            | 159 ms: 1.25x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250120-3.14.0a4+-e65a1eb/bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json | results/bm-20250120-3.14.0a4+-e65a1eb-NOGIL/bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.5 ms                                                                                                           | 88.9 ms: 1.02x faster                                                                                                   |
| xml_etree_parse      | 128 ms                                                                                                            | 129 ms: 1.01x slower                                                                                                    |
| json_loads           | 27.6 us                                                                                                           | 30.7 us: 1.11x slower                                                                                                   |
| json_dumps           | 11.4 ms                                                                                                           | 13.1 ms: 1.15x slower                                                                                                   |
| xml_etree_generate   | 82.7 ms                                                                                                           | 98.8 ms: 1.19x slower                                                                                                   |
| pickle_pure_python   | 317 us                                                                                                            | 393 us: 1.24x slower                                                                                                    |
| xml_etree_process    | 60.3 ms                                                                                                           | 74.9 ms: 1.24x slower                                                                                                   |
| unpickle_pure_python | 221 us                                                                                                            | 279 us: 1.26x slower                                                                                                    |
| tomli_loads          | 1.89 sec                                                                                                          | 2.45 sec: 1.30x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250120-3.14.0a4+-e65a1eb/bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json | results/bm-20250120-3.14.0a4+-e65a1eb-NOGIL/bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                                                           | 15.3 ms: 1.04x slower                                                                                                   |
| python_startup_no_site | 7.49 ms                                                                                                           | 9.59 ms: 1.28x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250120-3.14.0a4+-e65a1eb/bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json | results/bm-20250120-3.14.0a4+-e65a1eb-NOGIL/bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 35.8 ms                                                                                                           | 45.2 ms: 1.26x slower                                                                                                   |
| genshi_xml      | 49.0 ms                                                                                                           | 64.2 ms: 1.31x slower                                                                                                   |
| mako            | 11.7 ms                                                                                                           | 16.2 ms: 1.38x slower                                                                                                   |
| genshi_text     | 21.4 ms                                                                                                           | 30.3 ms: 1.42x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.34x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250120-3.14.0a4+-e65a1eb/bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json | results/bm-20250120-3.14.0a4+-e65a1eb-NOGIL/bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| create_gc_cycles           | 1.84 ms                                                                                                           | 1.32 ms: 1.40x faster                                                                                                   |
| gc_traversal               | 3.99 ms                                                                                                           | 3.35 ms: 1.19x faster                                                                                                   |
| sqlite_synth               | 2.19 us                                                                                                           | 2.03 us: 1.07x faster                                                                                                   |
| async_tree_none_tg         | 256 ms                                                                                                            | 245 ms: 1.05x faster                                                                                                    |
| async_tree_io_tg           | 610 ms                                                                                                            | 584 ms: 1.04x faster                                                                                                    |
| pidigits                   | 207 ms                                                                                                            | 198 ms: 1.04x faster                                                                                                    |
| xml_etree_iterparse        | 90.5 ms                                                                                                           | 88.9 ms: 1.02x faster                                                                                                   |
| asyncio_websockets         | 523 ms                                                                                                            | 518 ms: 1.01x faster                                                                                                    |
| xml_etree_parse            | 128 ms                                                                                                            | 129 ms: 1.01x slower                                                                                                    |
| regex_v8                   | 23.5 ms                                                                                                           | 24.1 ms: 1.03x slower                                                                                                   |
| pathlib                    | 18.2 ms                                                                                                           | 18.7 ms: 1.03x slower                                                                                                   |
| async_tree_memoization_tg  | 306 ms                                                                                                            | 315 ms: 1.03x slower                                                                                                    |
| python_startup             | 14.7 ms                                                                                                           | 15.3 ms: 1.04x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg | 481 ms                                                                                                            | 505 ms: 1.05x slower                                                                                                    |
| bench_mp_pool              | 89.7 ms                                                                                                           | 95.8 ms: 1.07x slower                                                                                                   |
| json                       | 4.98 ms                                                                                                           | 5.36 ms: 1.08x slower                                                                                                   |
| async_tree_none            | 263 ms                                                                                                            | 286 ms: 1.09x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 493 ms                                                                                                            | 538 ms: 1.09x slower                                                                                                    |
| pycparser                  | 1.13 sec                                                                                                          | 1.24 sec: 1.10x slower                                                                                                  |
| regex_dna                  | 169 ms                                                                                                            | 187 ms: 1.10x slower                                                                                                    |
| regex_effbot               | 2.60 ms                                                                                                           | 2.86 ms: 1.10x slower                                                                                                   |
| async_tree_memoization     | 319 ms                                                                                                            | 353 ms: 1.11x slower                                                                                                    |
| dulwich_log                | 76.5 ms                                                                                                           | 84.8 ms: 1.11x slower                                                                                                   |
| json_loads                 | 27.6 us                                                                                                           | 30.7 us: 1.11x slower                                                                                                   |
| docutils                   | 2.55 sec                                                                                                          | 2.86 sec: 1.12x slower                                                                                                  |
| float                      | 69.8 ms                                                                                                           | 78.9 ms: 1.13x slower                                                                                                   |
| coroutines                 | 22.1 ms                                                                                                           | 25.0 ms: 1.13x slower                                                                                                   |
| k_core                     | 2.05 sec                                                                                                          | 2.32 sec: 1.13x slower                                                                                                  |
| bpe_tokeniser              | 4.23 sec                                                                                                          | 4.83 sec: 1.14x slower                                                                                                  |
| mdp                        | 2.30 sec                                                                                                          | 2.62 sec: 1.14x slower                                                                                                  |
| json_dumps                 | 11.4 ms                                                                                                           | 13.1 ms: 1.15x slower                                                                                                   |
| sphinx                     | 983 ms                                                                                                            | 1.14 sec: 1.15x slower                                                                                                  |
| pylint                     | 279 ms                                                                                                            | 323 ms: 1.16x slower                                                                                                    |
| many_optionals             | 1.04 ms                                                                                                           | 1.22 ms: 1.17x slower                                                                                                   |
| logging_silent             | 104 ns                                                                                                            | 122 ns: 1.17x slower                                                                                                    |
| telco                      | 7.28 ms                                                                                                           | 8.57 ms: 1.18x slower                                                                                                   |
| async_generators           | 318 ms                                                                                                            | 377 ms: 1.18x slower                                                                                                    |
| subparsers                 | 22.2 ms                                                                                                           | 26.3 ms: 1.19x slower                                                                                                   |
| spectral_norm              | 92.2 ms                                                                                                           | 110 ms: 1.19x slower                                                                                                    |
| sqlglot_normalize          | 104 ms                                                                                                            | 124 ms: 1.19x slower                                                                                                    |
| xml_etree_generate         | 82.7 ms                                                                                                           | 98.8 ms: 1.19x slower                                                                                                   |
| generators                 | 27.5 ms                                                                                                           | 33.2 ms: 1.21x slower                                                                                                   |
| pprint_safe_repr           | 703 ms                                                                                                            | 850 ms: 1.21x slower                                                                                                    |
| sqlglot_optimize           | 52.4 ms                                                                                                           | 63.4 ms: 1.21x slower                                                                                                   |
| logging_simple             | 6.36 us                                                                                                           | 7.74 us: 1.22x slower                                                                                                   |
| sympy_expand               | 459 ms                                                                                                            | 561 ms: 1.22x slower                                                                                                    |
| coverage                   | 79.6 ms                                                                                                           | 97.4 ms: 1.22x slower                                                                                                   |
| pprint_pformat             | 1.43 sec                                                                                                          | 1.75 sec: 1.23x slower                                                                                                  |
| pyflate                    | 415 ms                                                                                                            | 511 ms: 1.23x slower                                                                                                    |
| logging_format             | 7.18 us                                                                                                           | 8.88 us: 1.24x slower                                                                                                   |
| sympy_sum                  | 154 ms                                                                                                            | 191 ms: 1.24x slower                                                                                                    |
| 2to3                       | 254 ms                                                                                                            | 314 ms: 1.24x slower                                                                                                    |
| pickle_pure_python         | 317 us                                                                                                            | 393 us: 1.24x slower                                                                                                    |
| xml_etree_process          | 60.3 ms                                                                                                           | 74.9 ms: 1.24x slower                                                                                                   |
| scimark_sor                | 111 ms                                                                                                            | 139 ms: 1.25x slower                                                                                                    |
| regex_compile              | 127 ms                                                                                                            | 159 ms: 1.25x slower                                                                                                    |
| sympy_integrate            | 19.8 ms                                                                                                           | 24.9 ms: 1.25x slower                                                                                                   |
| sympy_str                  | 274 ms                                                                                                            | 343 ms: 1.25x slower                                                                                                    |
| thrift                     | 749 us                                                                                                            | 941 us: 1.26x slower                                                                                                    |
| unpickle_pure_python       | 221 us                                                                                                            | 279 us: 1.26x slower                                                                                                    |
| django_template            | 35.8 ms                                                                                                           | 45.2 ms: 1.26x slower                                                                                                   |
| scimark_lu                 | 112 ms                                                                                                            | 142 ms: 1.27x slower                                                                                                    |
| sqlglot_transpile          | 1.55 ms                                                                                                           | 1.97 ms: 1.27x slower                                                                                                   |
| scimark_fft                | 305 ms                                                                                                            | 387 ms: 1.27x slower                                                                                                    |
| connected_components       | 390 ms                                                                                                            | 497 ms: 1.28x slower                                                                                                    |
| sqlalchemy_imperative      | 19.4 ms                                                                                                           | 24.7 ms: 1.28x slower                                                                                                   |
| shortest_path              | 432 ms                                                                                                            | 551 ms: 1.28x slower                                                                                                    |
| python_startup_no_site     | 7.49 ms                                                                                                           | 9.59 ms: 1.28x slower                                                                                                   |
| raytrace                   | 262 ms                                                                                                            | 336 ms: 1.28x slower                                                                                                    |
| nqueens                    | 76.9 ms                                                                                                           | 98.9 ms: 1.29x slower                                                                                                   |
| sqlalchemy_declarative     | 129 ms                                                                                                            | 167 ms: 1.29x slower                                                                                                    |
| go                         | 112 ms                                                                                                            | 144 ms: 1.29x slower                                                                                                    |
| deepcopy                   | 254 us                                                                                                            | 328 us: 1.29x slower                                                                                                    |
| deepcopy_reduce            | 2.60 us                                                                                                           | 3.36 us: 1.29x slower                                                                                                   |
| tomli_loads                | 1.89 sec                                                                                                          | 2.45 sec: 1.30x slower                                                                                                  |
| chaos                      | 54.8 ms                                                                                                           | 71.4 ms: 1.30x slower                                                                                                   |
| sqlglot_parse              | 1.25 ms                                                                                                           | 1.63 ms: 1.31x slower                                                                                                   |
| comprehensions             | 16.6 us                                                                                                           | 21.7 us: 1.31x slower                                                                                                   |
| genshi_xml                 | 49.0 ms                                                                                                           | 64.2 ms: 1.31x slower                                                                                                   |
| scimark_monte_carlo        | 63.2 ms                                                                                                           | 83.3 ms: 1.32x slower                                                                                                   |
| crypto_pyaes               | 67.0 ms                                                                                                           | 88.8 ms: 1.33x slower                                                                                                   |
| typing_runtime_protocols   | 157 us                                                                                                            | 211 us: 1.34x slower                                                                                                    |
| hexiom                     | 5.70 ms                                                                                                           | 7.65 ms: 1.34x slower                                                                                                   |
| deepcopy_memo              | 29.9 us                                                                                                           | 40.2 us: 1.34x slower                                                                                                   |
| fannkuch                   | 367 ms                                                                                                            | 495 ms: 1.35x slower                                                                                                    |
| meteor_contest             | 97.4 ms                                                                                                           | 131 ms: 1.35x slower                                                                                                    |
| scimark_sparse_mat_mult    | 4.10 ms                                                                                                           | 5.58 ms: 1.36x slower                                                                                                   |
| mako                       | 11.7 ms                                                                                                           | 16.2 ms: 1.38x slower                                                                                                   |
| richards                   | 41.0 ms                                                                                                           | 56.7 ms: 1.38x slower                                                                                                   |
| richards_super             | 47.2 ms                                                                                                           | 65.4 ms: 1.39x slower                                                                                                   |
| genshi_text                | 21.4 ms                                                                                                           | 30.3 ms: 1.42x slower                                                                                                   |
| nbody                      | 91.2 ms                                                                                                           | 137 ms: 1.50x slower                                                                                                    |
| deltablue                  | 3.05 ms                                                                                                           | 4.75 ms: 1.56x slower                                                                                                   |
| bench_thread_pool          | 1.03 ms                                                                                                           | 3.34 ms: 3.25x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.20x slower                                                                                                            |

Benchmark hidden because not significant (1): async_tree_io
Ignored benchmarks (1) of results/bm-20250120-3.14.0a4+-e65a1eb-NOGIL/bm-20250120-vultr-x86_64-python-e65a1eb93ae35f9fbab1-3.14.0a4+-e65a1eb.json: html5lib

- Geometric mean (including insignificant results): 1.158x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.16x
- 95% likely to have a slowdown of 1.15x
- 99% likely to have a slowdown of 1.14x

# Memory
- memory change: 1.20x