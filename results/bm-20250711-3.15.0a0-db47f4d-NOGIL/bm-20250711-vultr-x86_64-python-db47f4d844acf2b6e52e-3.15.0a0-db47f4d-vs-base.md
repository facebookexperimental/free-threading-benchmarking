# Results vs. base

- fork: python
- ref: db47f4d844acf2b6e52e
- machine: linux-x86_64
- commit hash: db47f4d
- commit date: 2025-07-11
- overall geometric mean: 1.093x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250711-3.15.0a0-db47f4d/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d.json | results/bm-20250711-3.15.0a0-db47f4d-NOGIL/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                                                          | 284 ms: 1.14x slower                                                                                                  |
| docutils       | 2.55 sec                                                                                                        | 2.70 sec: 1.06x slower                                                                                                |
| html5lib       | 60.3 ms                                                                                                         | 66.3 ms: 1.10x slower                                                                                                 |
| sphinx         | 968 ms                                                                                                          | 1.04 sec: 1.08x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250711-3.15.0a0-db47f4d/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d.json | results/bm-20250711-3.15.0a0-db47f4d-NOGIL/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 608 ms                                                                                                          | 521 ms: 1.17x faster                                                                                                  |
| async_tree_none_tg         | 253 ms                                                                                                          | 228 ms: 1.11x faster                                                                                                  |
| async_tree_io              | 594 ms                                                                                                          | 551 ms: 1.08x faster                                                                                                  |
| async_tree_memoization_tg  | 310 ms                                                                                                          | 287 ms: 1.08x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 496 ms                                                                                                          | 483 ms: 1.03x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 513 ms: 1.01x faster                                                                                                  |
| async_tree_none            | 257 ms                                                                                                          | 259 ms: 1.01x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 495 ms                                                                                                          | 510 ms: 1.03x slower                                                                                                  |
| coroutines                 | 23.4 ms                                                                                                         | 24.9 ms: 1.07x slower                                                                                                 |
| async_generators           | 340 ms                                                                                                          | 369 ms: 1.09x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.02x faster                                                                                                          |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250711-3.15.0a0-db47f4d/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d.json | results/bm-20250711-3.15.0a0-db47f4d-NOGIL/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 200 ms                                                                                                          | 187 ms: 1.07x faster                                                                                                  |
| float          | 70.5 ms                                                                                                         | 69.2 ms: 1.02x faster                                                                                                 |
| nbody          | 89.9 ms                                                                                                         | 124 ms: 1.38x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250711-3.15.0a0-db47f4d/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d.json | results/bm-20250711-3.15.0a0-db47f4d-NOGIL/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.6 ms                                                                                                         | 21.5 ms: 1.05x faster                                                                                                 |
| regex_dna      | 174 ms                                                                                                          | 178 ms: 1.02x slower                                                                                                  |
| regex_effbot   | 2.66 ms                                                                                                         | 2.85 ms: 1.07x slower                                                                                                 |
| regex_compile  | 123 ms                                                                                                          | 143 ms: 1.16x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.05x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250711-3.15.0a0-db47f4d/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d.json | results/bm-20250711-3.15.0a0-db47f4d-NOGIL/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 93.0 ms                                                                                                         | 87.4 ms: 1.06x faster                                                                                                 |
| json_dumps           | 10.9 ms                                                                                                         | 12.1 ms: 1.11x slower                                                                                                 |
| pickle_pure_python   | 306 us                                                                                                          | 340 us: 1.11x slower                                                                                                  |
| unpickle_pure_python | 207 us                                                                                                          | 231 us: 1.11x slower                                                                                                  |
| json_loads           | 28.2 us                                                                                                         | 31.6 us: 1.12x slower                                                                                                 |
| tomli_loads          | 1.91 sec                                                                                                        | 2.16 sec: 1.13x slower                                                                                                |
| xml_etree_generate   | 82.4 ms                                                                                                         | 95.4 ms: 1.16x slower                                                                                                 |
| xml_etree_process    | 57.3 ms                                                                                                         | 68.8 ms: 1.20x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250711-3.15.0a0-db47f4d/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d.json | results/bm-20250711-3.15.0a0-db47f4d-NOGIL/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                                                         | 16.0 ms: 1.28x slower                                                                                                 |
| python_startup_no_site | 7.33 ms                                                                                                         | 9.57 ms: 1.31x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250711-3.15.0a0-db47f4d/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d.json | results/bm-20250711-3.15.0a0-db47f4d-NOGIL/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 34.1 ms                                                                                                         | 39.4 ms: 1.16x slower                                                                                                 |
| genshi_xml      | 48.2 ms                                                                                                         | 57.1 ms: 1.19x slower                                                                                                 |
| genshi_text     | 20.9 ms                                                                                                         | 27.0 ms: 1.29x slower                                                                                                 |
| mako            | 11.5 ms                                                                                                         | 15.7 ms: 1.36x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.24x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250711-3.15.0a0-db47f4d/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d.json | results/bm-20250711-3.15.0a0-db47f4d-NOGIL/bm-20250711-vultr-x86_64-python-db47f4d844acf2b6e52e-3.15.0a0-db47f4d.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.52 ms                                                                                                         | 1.89 ms: 2.39x faster                                                                                                 |
| create_gc_cycles           | 1.97 ms                                                                                                         | 1.48 ms: 1.33x faster                                                                                                 |
| async_tree_io_tg           | 608 ms                                                                                                          | 521 ms: 1.17x faster                                                                                                  |
| sqlite_synth               | 2.31 us                                                                                                         | 2.05 us: 1.13x faster                                                                                                 |
| async_tree_none_tg         | 253 ms                                                                                                          | 228 ms: 1.11x faster                                                                                                  |
| async_tree_io              | 594 ms                                                                                                          | 551 ms: 1.08x faster                                                                                                  |
| async_tree_memoization_tg  | 310 ms                                                                                                          | 287 ms: 1.08x faster                                                                                                  |
| pidigits                   | 200 ms                                                                                                          | 187 ms: 1.07x faster                                                                                                  |
| xml_etree_iterparse        | 93.0 ms                                                                                                         | 87.4 ms: 1.06x faster                                                                                                 |
| regex_v8                   | 22.6 ms                                                                                                         | 21.5 ms: 1.05x faster                                                                                                 |
| async_tree_cpu_io_mixed_tg | 496 ms                                                                                                          | 483 ms: 1.03x faster                                                                                                  |
| float                      | 70.5 ms                                                                                                         | 69.2 ms: 1.02x faster                                                                                                 |
| pathlib                    | 19.6 ms                                                                                                         | 19.2 ms: 1.02x faster                                                                                                 |
| asyncio_websockets         | 517 ms                                                                                                          | 513 ms: 1.01x faster                                                                                                  |
| async_tree_none            | 257 ms                                                                                                          | 259 ms: 1.01x slower                                                                                                  |
| regex_dna                  | 174 ms                                                                                                          | 178 ms: 1.02x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 495 ms                                                                                                          | 510 ms: 1.03x slower                                                                                                  |
| json                       | 5.11 ms                                                                                                         | 5.33 ms: 1.04x slower                                                                                                 |
| bpe_tokeniser              | 4.20 sec                                                                                                        | 4.39 sec: 1.04x slower                                                                                                |
| pycparser                  | 1.09 sec                                                                                                        | 1.14 sec: 1.05x slower                                                                                                |
| bench_mp_pool              | 103 ms                                                                                                          | 108 ms: 1.05x slower                                                                                                  |
| docutils                   | 2.55 sec                                                                                                        | 2.70 sec: 1.06x slower                                                                                                |
| generators                 | 28.6 ms                                                                                                         | 30.3 ms: 1.06x slower                                                                                                 |
| coroutines                 | 23.4 ms                                                                                                         | 24.9 ms: 1.07x slower                                                                                                 |
| regex_effbot               | 2.66 ms                                                                                                         | 2.85 ms: 1.07x slower                                                                                                 |
| dulwich_log                | 66.5 ms                                                                                                         | 71.4 ms: 1.07x slower                                                                                                 |
| sphinx                     | 968 ms                                                                                                          | 1.04 sec: 1.08x slower                                                                                                |
| async_generators           | 340 ms                                                                                                          | 369 ms: 1.09x slower                                                                                                  |
| scimark_fft                | 334 ms                                                                                                          | 363 ms: 1.09x slower                                                                                                  |
| many_optionals             | 1.04 ms                                                                                                         | 1.14 ms: 1.10x slower                                                                                                 |
| html5lib                   | 60.3 ms                                                                                                         | 66.3 ms: 1.10x slower                                                                                                 |
| k_core                     | 2.03 sec                                                                                                        | 2.24 sec: 1.10x slower                                                                                                |
| pylint                     | 279 ms                                                                                                          | 308 ms: 1.11x slower                                                                                                  |
| pprint_safe_repr           | 693 ms                                                                                                          | 767 ms: 1.11x slower                                                                                                  |
| json_dumps                 | 10.9 ms                                                                                                         | 12.1 ms: 1.11x slower                                                                                                 |
| pickle_pure_python         | 306 us                                                                                                          | 340 us: 1.11x slower                                                                                                  |
| subparsers                 | 25.4 ms                                                                                                         | 28.2 ms: 1.11x slower                                                                                                 |
| unpickle_pure_python       | 207 us                                                                                                          | 231 us: 1.11x slower                                                                                                  |
| sympy_expand               | 467 ms                                                                                                          | 522 ms: 1.12x slower                                                                                                  |
| json_loads                 | 28.2 us                                                                                                         | 31.6 us: 1.12x slower                                                                                                 |
| pprint_pformat             | 1.42 sec                                                                                                        | 1.59 sec: 1.12x slower                                                                                                |
| logging_silent             | 95.3 ns                                                                                                         | 107 ns: 1.12x slower                                                                                                  |
| telco                      | 155 ms                                                                                                          | 175 ms: 1.13x slower                                                                                                  |
| deepcopy_reduce            | 2.70 us                                                                                                         | 3.04 us: 1.13x slower                                                                                                 |
| tomli_loads                | 1.91 sec                                                                                                        | 2.16 sec: 1.13x slower                                                                                                |
| chaos                      | 55.8 ms                                                                                                         | 63.1 ms: 1.13x slower                                                                                                 |
| scimark_sparse_mat_mult    | 4.80 ms                                                                                                         | 5.44 ms: 1.13x slower                                                                                                 |
| nqueens                    | 77.0 ms                                                                                                         | 87.7 ms: 1.14x slower                                                                                                 |
| 2to3                       | 249 ms                                                                                                          | 284 ms: 1.14x slower                                                                                                  |
| comprehensions             | 15.4 us                                                                                                         | 17.5 us: 1.14x slower                                                                                                 |
| scimark_sor                | 106 ms                                                                                                          | 121 ms: 1.14x slower                                                                                                  |
| deepcopy                   | 253 us                                                                                                          | 290 us: 1.15x slower                                                                                                  |
| mdp                        | 1.14 sec                                                                                                        | 1.32 sec: 1.15x slower                                                                                                |
| spectral_norm              | 96.3 ms                                                                                                         | 111 ms: 1.15x slower                                                                                                  |
| django_template            | 34.1 ms                                                                                                         | 39.4 ms: 1.16x slower                                                                                                 |
| hexiom                     | 5.58 ms                                                                                                         | 6.45 ms: 1.16x slower                                                                                                 |
| regex_compile              | 123 ms                                                                                                          | 143 ms: 1.16x slower                                                                                                  |
| go                         | 104 ms                                                                                                          | 120 ms: 1.16x slower                                                                                                  |
| xml_etree_generate         | 82.4 ms                                                                                                         | 95.4 ms: 1.16x slower                                                                                                 |
| sympy_str                  | 269 ms                                                                                                          | 313 ms: 1.16x slower                                                                                                  |
| sqlglot_v2_optimize        | 49.7 ms                                                                                                         | 58.1 ms: 1.17x slower                                                                                                 |
| thrift                     | 754 us                                                                                                          | 883 us: 1.17x slower                                                                                                  |
| deltablue                  | 3.05 ms                                                                                                         | 3.58 ms: 1.17x slower                                                                                                 |
| sympy_integrate            | 18.7 ms                                                                                                         | 21.9 ms: 1.17x slower                                                                                                 |
| sympy_sum                  | 153 ms                                                                                                          | 180 ms: 1.18x slower                                                                                                  |
| scimark_lu                 | 111 ms                                                                                                          | 130 ms: 1.18x slower                                                                                                  |
| logging_simple             | 5.91 us                                                                                                         | 6.96 us: 1.18x slower                                                                                                 |
| sqlglot_v2_normalize       | 98.1 ms                                                                                                         | 116 ms: 1.18x slower                                                                                                  |
| pyflate                    | 396 ms                                                                                                          | 468 ms: 1.18x slower                                                                                                  |
| genshi_xml                 | 48.2 ms                                                                                                         | 57.1 ms: 1.19x slower                                                                                                 |
| raytrace                   | 251 ms                                                                                                          | 300 ms: 1.20x slower                                                                                                  |
| fannkuch                   | 381 ms                                                                                                          | 458 ms: 1.20x slower                                                                                                  |
| meteor_contest             | 99.0 ms                                                                                                         | 119 ms: 1.20x slower                                                                                                  |
| xml_etree_process          | 57.3 ms                                                                                                         | 68.8 ms: 1.20x slower                                                                                                 |
| shortest_path              | 445 ms                                                                                                          | 538 ms: 1.21x slower                                                                                                  |
| deepcopy_memo              | 28.6 us                                                                                                         | 34.7 us: 1.21x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.50 ms                                                                                                         | 1.83 ms: 1.22x slower                                                                                                 |
| logging_format             | 6.63 us                                                                                                         | 8.10 us: 1.22x slower                                                                                                 |
| sqlglot_v2_parse           | 1.20 ms                                                                                                         | 1.47 ms: 1.22x slower                                                                                                 |
| connected_components       | 398 ms                                                                                                          | 495 ms: 1.24x slower                                                                                                  |
| typing_runtime_protocols   | 153 us                                                                                                          | 191 us: 1.25x slower                                                                                                  |
| scimark_monte_carlo        | 61.3 ms                                                                                                         | 77.7 ms: 1.27x slower                                                                                                 |
| richards                   | 40.5 ms                                                                                                         | 51.5 ms: 1.27x slower                                                                                                 |
| richards_super             | 46.2 ms                                                                                                         | 58.9 ms: 1.27x slower                                                                                                 |
| python_startup             | 12.6 ms                                                                                                         | 16.0 ms: 1.28x slower                                                                                                 |
| crypto_pyaes               | 67.7 ms                                                                                                         | 86.8 ms: 1.28x slower                                                                                                 |
| genshi_text                | 20.9 ms                                                                                                         | 27.0 ms: 1.29x slower                                                                                                 |
| python_startup_no_site     | 7.33 ms                                                                                                         | 9.57 ms: 1.31x slower                                                                                                 |
| mako                       | 11.5 ms                                                                                                         | 15.7 ms: 1.36x slower                                                                                                 |
| coverage                   | 81.8 ms                                                                                                         | 111 ms: 1.36x slower                                                                                                  |
| nbody                      | 89.9 ms                                                                                                         | 124 ms: 1.38x slower                                                                                                  |
| bench_thread_pool          | 1.05 ms                                                                                                         | 3.16 ms: 3.00x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.11x slower                                                                                                          |

Benchmark hidden because not significant (2): async_tree_memoization, xml_etree_parse

- Geometric mean (including insignificant results): 1.093x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.20x