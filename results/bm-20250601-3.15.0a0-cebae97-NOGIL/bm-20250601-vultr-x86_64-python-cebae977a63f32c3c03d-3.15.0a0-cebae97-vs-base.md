# Results vs. base

- fork: python
- ref: cebae977a63f32c3c03d
- machine: linux-x86_64
- commit hash: cebae97
- commit date: 2025-06-01
- overall geometric mean: 1.081x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250601-3.15.0a0-cebae97/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json | results/bm-20250601-3.15.0a0-cebae97-NOGIL/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 254 ms                                                                                                          | 284 ms: 1.12x slower                                                                                                  |
| docutils       | 2.56 sec                                                                                                        | 2.70 sec: 1.05x slower                                                                                                |
| html5lib       | 61.7 ms                                                                                                         | 67.0 ms: 1.09x slower                                                                                                 |
| sphinx         | 984 ms                                                                                                          | 1.06 sec: 1.08x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250601-3.15.0a0-cebae97/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json | results/bm-20250601-3.15.0a0-cebae97-NOGIL/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 628 ms                                                                                                          | 528 ms: 1.19x faster                                                                                                  |
| async_tree_none_tg         | 255 ms                                                                                                          | 229 ms: 1.11x faster                                                                                                  |
| async_tree_memoization_tg  | 313 ms                                                                                                          | 287 ms: 1.09x faster                                                                                                  |
| async_tree_io              | 603 ms                                                                                                          | 559 ms: 1.08x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 507 ms                                                                                                          | 475 ms: 1.07x faster                                                                                                  |
| async_tree_none            | 275 ms                                                                                                          | 261 ms: 1.05x faster                                                                                                  |
| coroutines                 | 23.9 ms                                                                                                         | 22.8 ms: 1.05x faster                                                                                                 |
| async_tree_cpu_io_mixed    | 518 ms                                                                                                          | 503 ms: 1.03x faster                                                                                                  |
| asyncio_websockets         | 519 ms                                                                                                          | 516 ms: 1.01x faster                                                                                                  |
| asyncio_tcp                | 515 ms                                                                                                          | 535 ms: 1.04x slower                                                                                                  |
| async_generators           | 342 ms                                                                                                          | 370 ms: 1.08x slower                                                                                                  |
| asyncio_tcp_ssl            | 1.54 sec                                                                                                        | 1.79 sec: 1.16x slower                                                                                                |
| Geometric mean             | (ref)                                                                                                           | 1.03x faster                                                                                                          |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250601-3.15.0a0-cebae97/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json | results/bm-20250601-3.15.0a0-cebae97-NOGIL/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| float          | 72.4 ms                                                                                                         | 69.4 ms: 1.04x faster                                                                                                 |
| pidigits       | 199 ms                                                                                                          | 195 ms: 1.02x faster                                                                                                  |
| nbody          | 88.3 ms                                                                                                         | 118 ms: 1.34x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250601-3.15.0a0-cebae97/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json | results/bm-20250601-3.15.0a0-cebae97-NOGIL/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.0 ms                                                                                                         | 20.2 ms: 1.04x faster                                                                                                 |
| regex_effbot   | 2.55 ms                                                                                                         | 2.68 ms: 1.05x slower                                                                                                 |
| regex_dna      | 166 ms                                                                                                          | 175 ms: 1.06x slower                                                                                                  |
| regex_compile  | 124 ms                                                                                                          | 144 ms: 1.16x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250601-3.15.0a0-cebae97/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json | results/bm-20250601-3.15.0a0-cebae97-NOGIL/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.4 ms                                                                                                         | 87.2 ms: 1.11x faster                                                                                                 |
| xml_etree_parse      | 134 ms                                                                                                          | 130 ms: 1.03x faster                                                                                                  |
| pickle               | 12.5 us                                                                                                         | 12.3 us: 1.02x faster                                                                                                 |
| pickle_dict          | 31.5 us                                                                                                         | 31.8 us: 1.01x slower                                                                                                 |
| unpickle_list        | 5.03 us                                                                                                         | 5.38 us: 1.07x slower                                                                                                 |
| json_loads           | 29.2 us                                                                                                         | 31.5 us: 1.08x slower                                                                                                 |
| unpickle             | 14.2 us                                                                                                         | 15.3 us: 1.08x slower                                                                                                 |
| pickle_pure_python   | 308 us                                                                                                          | 335 us: 1.09x slower                                                                                                  |
| tomli_loads          | 1.95 sec                                                                                                        | 2.13 sec: 1.09x slower                                                                                                |
| unpickle_pure_python | 209 us                                                                                                          | 230 us: 1.10x slower                                                                                                  |
| json_dumps           | 10.7 ms                                                                                                         | 12.0 ms: 1.12x slower                                                                                                 |
| xml_etree_generate   | 83.6 ms                                                                                                         | 94.9 ms: 1.13x slower                                                                                                 |
| xml_etree_process    | 58.7 ms                                                                                                         | 68.7 ms: 1.17x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.05x slower                                                                                                          |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250601-3.15.0a0-cebae97/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json | results/bm-20250601-3.15.0a0-cebae97-NOGIL/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.8 ms                                                                                                         | 16.0 ms: 1.25x slower                                                                                                 |
| python_startup_no_site | 7.54 ms                                                                                                         | 9.62 ms: 1.28x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.26x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250601-3.15.0a0-cebae97/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json | results/bm-20250601-3.15.0a0-cebae97-NOGIL/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 34.6 ms                                                                                                         | 39.8 ms: 1.15x slower                                                                                                 |
| genshi_xml      | 48.0 ms                                                                                                         | 57.8 ms: 1.20x slower                                                                                                 |
| genshi_text     | 20.8 ms                                                                                                         | 26.6 ms: 1.28x slower                                                                                                 |
| mako            | 11.9 ms                                                                                                         | 15.7 ms: 1.31x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.23x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250601-3.15.0a0-cebae97/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json | results/bm-20250601-3.15.0a0-cebae97-NOGIL/bm-20250601-vultr-x86_64-python-cebae977a63f32c3c03d-3.15.0a0-cebae97.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.56 ms                                                                                                         | 1.93 ms: 2.37x faster                                                                                                 |
| create_gc_cycles           | 2.03 ms                                                                                                         | 1.50 ms: 1.35x faster                                                                                                 |
| async_tree_io_tg           | 628 ms                                                                                                          | 528 ms: 1.19x faster                                                                                                  |
| async_tree_none_tg         | 255 ms                                                                                                          | 229 ms: 1.11x faster                                                                                                  |
| xml_etree_iterparse        | 96.4 ms                                                                                                         | 87.2 ms: 1.11x faster                                                                                                 |
| sqlite_synth               | 2.23 us                                                                                                         | 2.04 us: 1.10x faster                                                                                                 |
| async_tree_memoization_tg  | 313 ms                                                                                                          | 287 ms: 1.09x faster                                                                                                  |
| async_tree_io              | 603 ms                                                                                                          | 559 ms: 1.08x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 507 ms                                                                                                          | 475 ms: 1.07x faster                                                                                                  |
| async_tree_none            | 275 ms                                                                                                          | 261 ms: 1.05x faster                                                                                                  |
| coroutines                 | 23.9 ms                                                                                                         | 22.8 ms: 1.05x faster                                                                                                 |
| float                      | 72.4 ms                                                                                                         | 69.4 ms: 1.04x faster                                                                                                 |
| regex_v8                   | 21.0 ms                                                                                                         | 20.2 ms: 1.04x faster                                                                                                 |
| xml_etree_parse            | 134 ms                                                                                                          | 130 ms: 1.03x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 518 ms                                                                                                          | 503 ms: 1.03x faster                                                                                                  |
| pidigits                   | 199 ms                                                                                                          | 195 ms: 1.02x faster                                                                                                  |
| pickle                     | 12.5 us                                                                                                         | 12.3 us: 1.02x faster                                                                                                 |
| asyncio_websockets         | 519 ms                                                                                                          | 516 ms: 1.01x faster                                                                                                  |
| pickle_dict                | 31.5 us                                                                                                         | 31.8 us: 1.01x slower                                                                                                 |
| bench_mp_pool              | 101 ms                                                                                                          | 103 ms: 1.01x slower                                                                                                  |
| json                       | 5.22 ms                                                                                                         | 5.37 ms: 1.03x slower                                                                                                 |
| bpe_tokeniser              | 4.19 sec                                                                                                        | 4.33 sec: 1.03x slower                                                                                                |
| k_core                     | 2.14 sec                                                                                                        | 2.22 sec: 1.04x slower                                                                                                |
| asyncio_tcp                | 515 ms                                                                                                          | 535 ms: 1.04x slower                                                                                                  |
| regex_effbot               | 2.55 ms                                                                                                         | 2.68 ms: 1.05x slower                                                                                                 |
| docutils                   | 2.56 sec                                                                                                        | 2.70 sec: 1.05x slower                                                                                                |
| regex_dna                  | 166 ms                                                                                                          | 175 ms: 1.06x slower                                                                                                  |
| unpickle_list              | 5.03 us                                                                                                         | 5.38 us: 1.07x slower                                                                                                 |
| spectral_norm              | 102 ms                                                                                                          | 109 ms: 1.07x slower                                                                                                  |
| dulwich_log                | 66.5 ms                                                                                                         | 71.4 ms: 1.07x slower                                                                                                 |
| scimark_fft                | 339 ms                                                                                                          | 365 ms: 1.08x slower                                                                                                  |
| json_loads                 | 29.2 us                                                                                                         | 31.5 us: 1.08x slower                                                                                                 |
| unpickle                   | 14.2 us                                                                                                         | 15.3 us: 1.08x slower                                                                                                 |
| sphinx                     | 984 ms                                                                                                          | 1.06 sec: 1.08x slower                                                                                                |
| pylint                     | 285 ms                                                                                                          | 309 ms: 1.08x slower                                                                                                  |
| async_generators           | 342 ms                                                                                                          | 370 ms: 1.08x slower                                                                                                  |
| html5lib                   | 61.7 ms                                                                                                         | 67.0 ms: 1.09x slower                                                                                                 |
| pickle_pure_python         | 308 us                                                                                                          | 335 us: 1.09x slower                                                                                                  |
| many_optionals             | 1.05 ms                                                                                                         | 1.14 ms: 1.09x slower                                                                                                 |
| tomli_loads                | 1.95 sec                                                                                                        | 2.13 sec: 1.09x slower                                                                                                |
| chaos                      | 56.6 ms                                                                                                         | 61.9 ms: 1.09x slower                                                                                                 |
| deltablue                  | 3.31 ms                                                                                                         | 3.63 ms: 1.10x slower                                                                                                 |
| mdp                        | 1.20 sec                                                                                                        | 1.32 sec: 1.10x slower                                                                                                |
| scimark_sor                | 111 ms                                                                                                          | 122 ms: 1.10x slower                                                                                                  |
| unpickle_pure_python       | 209 us                                                                                                          | 230 us: 1.10x slower                                                                                                  |
| scimark_sparse_mat_mult    | 4.80 ms                                                                                                         | 5.33 ms: 1.11x slower                                                                                                 |
| 2to3                       | 254 ms                                                                                                          | 284 ms: 1.12x slower                                                                                                  |
| json_dumps                 | 10.7 ms                                                                                                         | 12.0 ms: 1.12x slower                                                                                                 |
| comprehensions             | 15.7 us                                                                                                         | 17.6 us: 1.12x slower                                                                                                 |
| nqueens                    | 75.9 ms                                                                                                         | 85.4 ms: 1.13x slower                                                                                                 |
| hexiom                     | 5.63 ms                                                                                                         | 6.33 ms: 1.13x slower                                                                                                 |
| pyflate                    | 413 ms                                                                                                          | 465 ms: 1.13x slower                                                                                                  |
| subparsers                 | 25.4 ms                                                                                                         | 28.8 ms: 1.13x slower                                                                                                 |
| xml_etree_generate         | 83.6 ms                                                                                                         | 94.9 ms: 1.13x slower                                                                                                 |
| logging_silent             | 469 ns                                                                                                          | 533 ns: 1.14x slower                                                                                                  |
| deepcopy_reduce            | 2.69 us                                                                                                         | 3.06 us: 1.14x slower                                                                                                 |
| pprint_safe_repr           | 773 ms                                                                                                          | 883 ms: 1.14x slower                                                                                                  |
| sqlglot_v2_optimize        | 49.7 ms                                                                                                         | 56.8 ms: 1.14x slower                                                                                                 |
| go                         | 105 ms                                                                                                          | 121 ms: 1.15x slower                                                                                                  |
| django_template            | 34.6 ms                                                                                                         | 39.8 ms: 1.15x slower                                                                                                 |
| deepcopy                   | 253 us                                                                                                          | 291 us: 1.15x slower                                                                                                  |
| sqlglot_v2_normalize       | 98.5 ms                                                                                                         | 114 ms: 1.16x slower                                                                                                  |
| regex_compile              | 124 ms                                                                                                          | 144 ms: 1.16x slower                                                                                                  |
| scimark_lu                 | 110 ms                                                                                                          | 128 ms: 1.16x slower                                                                                                  |
| pprint_pformat             | 1.58 sec                                                                                                        | 1.83 sec: 1.16x slower                                                                                                |
| asyncio_tcp_ssl            | 1.54 sec                                                                                                        | 1.79 sec: 1.16x slower                                                                                                |
| shortest_path              | 456 ms                                                                                                          | 531 ms: 1.16x slower                                                                                                  |
| sympy_integrate            | 18.9 ms                                                                                                         | 22.0 ms: 1.17x slower                                                                                                 |
| sympy_sum                  | 154 ms                                                                                                          | 181 ms: 1.17x slower                                                                                                  |
| xml_etree_process          | 58.7 ms                                                                                                         | 68.7 ms: 1.17x slower                                                                                                 |
| sympy_expand               | 450 ms                                                                                                          | 528 ms: 1.17x slower                                                                                                  |
| raytrace                   | 253 ms                                                                                                          | 296 ms: 1.17x slower                                                                                                  |
| sympy_str                  | 268 ms                                                                                                          | 315 ms: 1.17x slower                                                                                                  |
| connected_components       | 411 ms                                                                                                          | 483 ms: 1.17x slower                                                                                                  |
| logging_simple             | 6.62 us                                                                                                         | 7.79 us: 1.18x slower                                                                                                 |
| deepcopy_memo              | 28.9 us                                                                                                         | 34.5 us: 1.19x slower                                                                                                 |
| telco                      | 7.31 ms                                                                                                         | 8.73 ms: 1.19x slower                                                                                                 |
| thrift                     | 745 us                                                                                                          | 893 us: 1.20x slower                                                                                                  |
| genshi_xml                 | 48.0 ms                                                                                                         | 57.8 ms: 1.20x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.51 ms                                                                                                         | 1.82 ms: 1.21x slower                                                                                                 |
| sqlglot_v2_parse           | 1.22 ms                                                                                                         | 1.48 ms: 1.22x slower                                                                                                 |
| logging_format             | 7.39 us                                                                                                         | 9.01 us: 1.22x slower                                                                                                 |
| meteor_contest             | 98.6 ms                                                                                                         | 120 ms: 1.22x slower                                                                                                  |
| fannkuch                   | 375 ms                                                                                                          | 459 ms: 1.22x slower                                                                                                  |
| typing_runtime_protocols   | 154 us                                                                                                          | 191 us: 1.24x slower                                                                                                  |
| crypto_pyaes               | 68.2 ms                                                                                                         | 85.1 ms: 1.25x slower                                                                                                 |
| python_startup             | 12.8 ms                                                                                                         | 16.0 ms: 1.25x slower                                                                                                 |
| scimark_monte_carlo        | 61.4 ms                                                                                                         | 77.1 ms: 1.26x slower                                                                                                 |
| richards                   | 40.9 ms                                                                                                         | 51.5 ms: 1.26x slower                                                                                                 |
| richards_super             | 46.5 ms                                                                                                         | 58.7 ms: 1.26x slower                                                                                                 |
| genshi_text                | 20.8 ms                                                                                                         | 26.6 ms: 1.28x slower                                                                                                 |
| python_startup_no_site     | 7.54 ms                                                                                                         | 9.62 ms: 1.28x slower                                                                                                 |
| unpack_sequence            | 41.3 ns                                                                                                         | 52.9 ns: 1.28x slower                                                                                                 |
| mako                       | 11.9 ms                                                                                                         | 15.7 ms: 1.31x slower                                                                                                 |
| nbody                      | 88.3 ms                                                                                                         | 118 ms: 1.34x slower                                                                                                  |
| coverage                   | 82.7 ms                                                                                                         | 111 ms: 1.35x slower                                                                                                  |
| bench_thread_pool          | 1.05 ms                                                                                                         | 3.12 ms: 2.98x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmark hidden because not significant (5): generators, pycparser, pathlib, async_tree_memoization, pickle_list

- Geometric mean (including insignificant results): 1.081x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.22x