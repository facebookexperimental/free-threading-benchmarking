# Results vs. base

- fork: python
- ref: e66f87ca73516efb4aec
- machine: linux-x86_64
- commit hash: e66f87c
- commit date: 2025-11-02
- overall geometric mean: 1.096x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20251102-3.15.0a1+-e66f87c/bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c.json | results/bm-20251102-3.15.0a1+-e66f87c-NOGIL/bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 247 ms                                                                                                            | 281 ms: 1.13x slower                                                                                                    |
| docutils       | 2.57 sec                                                                                                          | 2.69 sec: 1.05x slower                                                                                                  |
| html5lib       | 60.8 ms                                                                                                           | 67.1 ms: 1.11x slower                                                                                                   |
| sphinx         | 968 ms                                                                                                            | 1.07 sec: 1.10x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.10x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20251102-3.15.0a1+-e66f87c/bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c.json | results/bm-20251102-3.15.0a1+-e66f87c-NOGIL/bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 593 ms                                                                                                            | 521 ms: 1.14x faster                                                                                                    |
| async_tree_memoization_tg  | 308 ms                                                                                                            | 283 ms: 1.09x faster                                                                                                    |
| async_tree_none_tg         | 246 ms                                                                                                            | 227 ms: 1.09x faster                                                                                                    |
| asyncio_websockets         | 545 ms                                                                                                            | 509 ms: 1.07x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 509 ms                                                                                                            | 483 ms: 1.06x faster                                                                                                    |
| async_tree_io              | 557 ms                                                                                                            | 543 ms: 1.03x faster                                                                                                    |
| async_tree_cpu_io_mixed    | 510 ms                                                                                                            | 505 ms: 1.01x faster                                                                                                    |
| coroutines                 | 24.1 ms                                                                                                           | 24.3 ms: 1.01x slower                                                                                                   |
| async_tree_none            | 246 ms                                                                                                            | 255 ms: 1.04x slower                                                                                                    |
| async_generators           | 337 ms                                                                                                            | 377 ms: 1.12x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.03x faster                                                                                                            |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20251102-3.15.0a1+-e66f87c/bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c.json | results/bm-20251102-3.15.0a1+-e66f87c-NOGIL/bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 214 ms                                                                                                            | 196 ms: 1.09x faster                                                                                                    |
| float          | 69.2 ms                                                                                                           | 70.1 ms: 1.01x slower                                                                                                   |
| nbody          | 86.9 ms                                                                                                           | 125 ms: 1.44x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.10x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20251102-3.15.0a1+-e66f87c/bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c.json | results/bm-20251102-3.15.0a1+-e66f87c-NOGIL/bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.2 ms                                                                                                           | 21.1 ms: 1.05x faster                                                                                                   |
| regex_dna      | 173 ms                                                                                                            | 182 ms: 1.05x slower                                                                                                    |
| regex_effbot   | 2.64 ms                                                                                                           | 2.92 ms: 1.11x slower                                                                                                   |
| regex_compile  | 124 ms                                                                                                            | 143 ms: 1.16x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.06x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20251102-3.15.0a1+-e66f87c/bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c.json | results/bm-20251102-3.15.0a1+-e66f87c-NOGIL/bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 129 ms                                                                                                            | 133 ms: 1.03x slower                                                                                                    |
| xml_etree_iterparse  | 84.4 ms                                                                                                           | 87.6 ms: 1.04x slower                                                                                                   |
| tomli_loads          | 1.90 sec                                                                                                          | 2.02 sec: 1.06x slower                                                                                                  |
| pickle_pure_python   | 306 us                                                                                                            | 338 us: 1.10x slower                                                                                                    |
| unpickle_pure_python | 211 us                                                                                                            | 235 us: 1.11x slower                                                                                                    |
| json_loads           | 27.9 us                                                                                                           | 31.7 us: 1.13x slower                                                                                                   |
| xml_etree_generate   | 82.4 ms                                                                                                           | 96.0 ms: 1.16x slower                                                                                                   |
| xml_etree_process    | 58.4 ms                                                                                                           | 68.7 ms: 1.18x slower                                                                                                   |
| json_dumps           | 9.49 ms                                                                                                           | 11.2 ms: 1.18x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.11x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20251102-3.15.0a1+-e66f87c/bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c.json | results/bm-20251102-3.15.0a1+-e66f87c-NOGIL/bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.3 ms                                                                                                           | 15.8 ms: 1.28x slower                                                                                                   |
| python_startup_no_site | 7.20 ms                                                                                                           | 9.58 ms: 1.33x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.30x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20251102-3.15.0a1+-e66f87c/bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c.json | results/bm-20251102-3.15.0a1+-e66f87c-NOGIL/bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 35.1 ms                                                                                                           | 40.2 ms: 1.14x slower                                                                                                   |
| genshi_xml      | 47.8 ms                                                                                                           | 58.1 ms: 1.21x slower                                                                                                   |
| genshi_text     | 20.6 ms                                                                                                           | 26.2 ms: 1.28x slower                                                                                                   |
| mako            | 11.9 ms                                                                                                           | 15.6 ms: 1.31x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.23x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20251102-3.15.0a1+-e66f87c/bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c.json | results/bm-20251102-3.15.0a1+-e66f87c-NOGIL/bm-20251102-vultr-x86_64-python-e66f87ca73516efb4aec-3.15.0a1+-e66f87c.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.09 ms                                                                                                           | 1.92 ms: 2.13x faster                                                                                                   |
| create_gc_cycles           | 1.92 ms                                                                                                           | 1.49 ms: 1.29x faster                                                                                                   |
| async_tree_io_tg           | 593 ms                                                                                                            | 521 ms: 1.14x faster                                                                                                    |
| sqlite_synth               | 2.26 us                                                                                                           | 2.05 us: 1.10x faster                                                                                                   |
| pidigits                   | 214 ms                                                                                                            | 196 ms: 1.09x faster                                                                                                    |
| async_tree_memoization_tg  | 308 ms                                                                                                            | 283 ms: 1.09x faster                                                                                                    |
| async_tree_none_tg         | 246 ms                                                                                                            | 227 ms: 1.09x faster                                                                                                    |
| asyncio_websockets         | 545 ms                                                                                                            | 509 ms: 1.07x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 509 ms                                                                                                            | 483 ms: 1.06x faster                                                                                                    |
| regex_v8                   | 22.2 ms                                                                                                           | 21.1 ms: 1.05x faster                                                                                                   |
| async_tree_io              | 557 ms                                                                                                            | 543 ms: 1.03x faster                                                                                                    |
| async_tree_cpu_io_mixed    | 510 ms                                                                                                            | 505 ms: 1.01x faster                                                                                                    |
| coroutines                 | 24.1 ms                                                                                                           | 24.3 ms: 1.01x slower                                                                                                   |
| pathlib                    | 17.7 ms                                                                                                           | 17.8 ms: 1.01x slower                                                                                                   |
| float                      | 69.2 ms                                                                                                           | 70.1 ms: 1.01x slower                                                                                                   |
| xml_etree_parse            | 129 ms                                                                                                            | 133 ms: 1.03x slower                                                                                                    |
| async_tree_none            | 246 ms                                                                                                            | 255 ms: 1.04x slower                                                                                                    |
| xml_etree_iterparse        | 84.4 ms                                                                                                           | 87.6 ms: 1.04x slower                                                                                                   |
| docutils                   | 2.57 sec                                                                                                          | 2.69 sec: 1.05x slower                                                                                                  |
| logging_silent             | 101 ns                                                                                                            | 106 ns: 1.05x slower                                                                                                    |
| bpe_tokeniser              | 4.20 sec                                                                                                          | 4.42 sec: 1.05x slower                                                                                                  |
| regex_dna                  | 173 ms                                                                                                            | 182 ms: 1.05x slower                                                                                                    |
| tomli_loads                | 1.90 sec                                                                                                          | 2.02 sec: 1.06x slower                                                                                                  |
| json                       | 5.04 ms                                                                                                           | 5.35 ms: 1.06x slower                                                                                                   |
| dulwich_log                | 68.4 ms                                                                                                           | 72.6 ms: 1.06x slower                                                                                                   |
| pylint                     | 287 ms                                                                                                            | 306 ms: 1.07x slower                                                                                                    |
| sympy_expand               | 475 ms                                                                                                            | 516 ms: 1.08x slower                                                                                                    |
| sphinx                     | 968 ms                                                                                                            | 1.07 sec: 1.10x slower                                                                                                  |
| pickle_pure_python         | 306 us                                                                                                            | 338 us: 1.10x slower                                                                                                    |
| html5lib                   | 60.8 ms                                                                                                           | 67.1 ms: 1.11x slower                                                                                                   |
| regex_effbot               | 2.64 ms                                                                                                           | 2.92 ms: 1.11x slower                                                                                                   |
| many_optionals             | 1.21 ms                                                                                                           | 1.34 ms: 1.11x slower                                                                                                   |
| pycparser                  | 1.07 sec                                                                                                          | 1.19 sec: 1.11x slower                                                                                                  |
| unpickle_pure_python       | 211 us                                                                                                            | 235 us: 1.11x slower                                                                                                    |
| deltablue                  | 3.31 ms                                                                                                           | 3.67 ms: 1.11x slower                                                                                                   |
| generators                 | 28.2 ms                                                                                                           | 31.3 ms: 1.11x slower                                                                                                   |
| pprint_safe_repr           | 696 ms                                                                                                            | 775 ms: 1.11x slower                                                                                                    |
| telco                      | 157 ms                                                                                                            | 176 ms: 1.11x slower                                                                                                    |
| async_generators           | 337 ms                                                                                                            | 377 ms: 1.12x slower                                                                                                    |
| scimark_fft                | 305 ms                                                                                                            | 342 ms: 1.12x slower                                                                                                    |
| nqueens                    | 77.2 ms                                                                                                           | 87.1 ms: 1.13x slower                                                                                                   |
| sympy_str                  | 274 ms                                                                                                            | 309 ms: 1.13x slower                                                                                                    |
| deepcopy                   | 245 us                                                                                                            | 277 us: 1.13x slower                                                                                                    |
| pprint_pformat             | 1.42 sec                                                                                                          | 1.60 sec: 1.13x slower                                                                                                  |
| json_loads                 | 27.9 us                                                                                                           | 31.7 us: 1.13x slower                                                                                                   |
| 2to3                       | 247 ms                                                                                                            | 281 ms: 1.13x slower                                                                                                    |
| comprehensions             | 15.9 us                                                                                                           | 18.0 us: 1.13x slower                                                                                                   |
| chaos                      | 56.0 ms                                                                                                           | 63.6 ms: 1.14x slower                                                                                                   |
| django_template            | 35.1 ms                                                                                                           | 40.2 ms: 1.14x slower                                                                                                   |
| pyflate                    | 406 ms                                                                                                            | 466 ms: 1.15x slower                                                                                                    |
| sympy_integrate            | 19.0 ms                                                                                                           | 21.8 ms: 1.15x slower                                                                                                   |
| sqlglot_v2_normalize       | 100.0 ms                                                                                                          | 115 ms: 1.15x slower                                                                                                    |
| scimark_sor                | 107 ms                                                                                                            | 123 ms: 1.15x slower                                                                                                    |
| hexiom                     | 5.57 ms                                                                                                           | 6.40 ms: 1.15x slower                                                                                                   |
| sqlglot_v2_optimize        | 50.5 ms                                                                                                           | 58.1 ms: 1.15x slower                                                                                                   |
| regex_compile              | 124 ms                                                                                                            | 143 ms: 1.16x slower                                                                                                    |
| mdp                        | 1.14 sec                                                                                                          | 1.32 sec: 1.16x slower                                                                                                  |
| sympy_sum                  | 155 ms                                                                                                            | 179 ms: 1.16x slower                                                                                                    |
| subparsers                 | 44.2 ms                                                                                                           | 51.2 ms: 1.16x slower                                                                                                   |
| go                         | 105 ms                                                                                                            | 122 ms: 1.16x slower                                                                                                    |
| deepcopy_reduce            | 2.58 us                                                                                                           | 3.01 us: 1.16x slower                                                                                                   |
| xml_etree_generate         | 82.4 ms                                                                                                           | 96.0 ms: 1.16x slower                                                                                                   |
| spectral_norm              | 95.0 ms                                                                                                           | 111 ms: 1.17x slower                                                                                                    |
| meteor_contest             | 101 ms                                                                                                            | 118 ms: 1.17x slower                                                                                                    |
| deepcopy_memo              | 26.5 us                                                                                                           | 30.9 us: 1.17x slower                                                                                                   |
| sqlglot_v2_transpile       | 1.51 ms                                                                                                           | 1.77 ms: 1.17x slower                                                                                                   |
| fannkuch                   | 387 ms                                                                                                            | 453 ms: 1.17x slower                                                                                                    |
| xml_etree_process          | 58.4 ms                                                                                                           | 68.7 ms: 1.18x slower                                                                                                   |
| json_dumps                 | 9.49 ms                                                                                                           | 11.2 ms: 1.18x slower                                                                                                   |
| logging_simple             | 5.79 us                                                                                                           | 6.84 us: 1.18x slower                                                                                                   |
| logging_format             | 6.58 us                                                                                                           | 7.79 us: 1.18x slower                                                                                                   |
| thrift                     | 754 us                                                                                                            | 894 us: 1.19x slower                                                                                                    |
| k_core                     | 1.88 sec                                                                                                          | 2.23 sec: 1.19x slower                                                                                                  |
| sqlglot_v2_parse           | 1.21 ms                                                                                                           | 1.45 ms: 1.19x slower                                                                                                   |
| typing_runtime_protocols   | 155 us                                                                                                            | 186 us: 1.20x slower                                                                                                    |
| connected_components       | 407 ms                                                                                                            | 490 ms: 1.20x slower                                                                                                    |
| shortest_path              | 443 ms                                                                                                            | 534 ms: 1.21x slower                                                                                                    |
| raytrace                   | 249 ms                                                                                                            | 301 ms: 1.21x slower                                                                                                    |
| scimark_lu                 | 108 ms                                                                                                            | 131 ms: 1.21x slower                                                                                                    |
| genshi_xml                 | 47.8 ms                                                                                                           | 58.1 ms: 1.21x slower                                                                                                   |
| bench_mp_pool              | 12.4 ms                                                                                                           | 15.1 ms: 1.22x slower                                                                                                   |
| richards                   | 42.2 ms                                                                                                           | 51.7 ms: 1.23x slower                                                                                                   |
| richards_super             | 47.8 ms                                                                                                           | 59.5 ms: 1.25x slower                                                                                                   |
| crypto_pyaes               | 69.3 ms                                                                                                           | 86.6 ms: 1.25x slower                                                                                                   |
| scimark_sparse_mat_mult    | 4.24 ms                                                                                                           | 5.40 ms: 1.27x slower                                                                                                   |
| genshi_text                | 20.6 ms                                                                                                           | 26.2 ms: 1.28x slower                                                                                                   |
| python_startup             | 12.3 ms                                                                                                           | 15.8 ms: 1.28x slower                                                                                                   |
| mako                       | 11.9 ms                                                                                                           | 15.6 ms: 1.31x slower                                                                                                   |
| scimark_monte_carlo        | 61.0 ms                                                                                                           | 80.1 ms: 1.31x slower                                                                                                   |
| python_startup_no_site     | 7.20 ms                                                                                                           | 9.58 ms: 1.33x slower                                                                                                   |
| coverage                   | 81.1 ms                                                                                                           | 110 ms: 1.36x slower                                                                                                    |
| nbody                      | 86.9 ms                                                                                                           | 125 ms: 1.44x slower                                                                                                    |
| bench_thread_pool          | 1.00 ms                                                                                                           | 3.05 ms: 3.05x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmark hidden because not significant (1): async_tree_memoization

- Geometric mean (including insignificant results): 1.096x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.20x