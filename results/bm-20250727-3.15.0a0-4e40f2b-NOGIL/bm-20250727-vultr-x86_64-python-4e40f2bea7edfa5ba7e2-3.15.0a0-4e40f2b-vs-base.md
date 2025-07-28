# Results vs. base

- fork: python
- ref: 4e40f2bea7edfa5ba7e2
- machine: linux-x86_64
- commit hash: 4e40f2b
- commit date: 2025-07-27
- overall geometric mean: 1.093x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250727-3.15.0a0-4e40f2b/bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b.json | results/bm-20250727-3.15.0a0-4e40f2b-NOGIL/bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 250 ms                                                                                                          | 286 ms: 1.14x slower                                                                                                  |
| docutils       | 2.57 sec                                                                                                        | 2.73 sec: 1.06x slower                                                                                                |
| html5lib       | 62.3 ms                                                                                                         | 67.0 ms: 1.08x slower                                                                                                 |
| sphinx         | 975 ms                                                                                                          | 1.05 sec: 1.08x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250727-3.15.0a0-4e40f2b/bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b.json | results/bm-20250727-3.15.0a0-4e40f2b-NOGIL/bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 622 ms                                                                                                          | 517 ms: 1.20x faster                                                                                                  |
| async_tree_none_tg         | 259 ms                                                                                                          | 224 ms: 1.16x faster                                                                                                  |
| async_tree_memoization_tg  | 317 ms                                                                                                          | 282 ms: 1.12x faster                                                                                                  |
| async_tree_io              | 596 ms                                                                                                          | 537 ms: 1.11x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 501 ms                                                                                                          | 474 ms: 1.06x faster                                                                                                  |
| async_tree_none            | 265 ms                                                                                                          | 256 ms: 1.04x faster                                                                                                  |
| async_tree_memoization     | 315 ms                                                                                                          | 310 ms: 1.02x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 513 ms: 1.01x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 498 ms                                                                                                          | 500 ms: 1.00x slower                                                                                                  |
| coroutines                 | 23.7 ms                                                                                                         | 24.5 ms: 1.03x slower                                                                                                 |
| async_generators           | 341 ms                                                                                                          | 377 ms: 1.11x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.05x faster                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250727-3.15.0a0-4e40f2b/bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b.json | results/bm-20250727-3.15.0a0-4e40f2b-NOGIL/bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 194 ms                                                                                                          | 190 ms: 1.02x faster                                                                                                  |
| float          | 70.5 ms                                                                                                         | 70.9 ms: 1.01x slower                                                                                                 |
| nbody          | 89.5 ms                                                                                                         | 127 ms: 1.41x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.12x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250727-3.15.0a0-4e40f2b/bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b.json | results/bm-20250727-3.15.0a0-4e40f2b-NOGIL/bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.3 ms                                                                                                         | 20.6 ms: 1.04x faster                                                                                                 |
| regex_dna      | 175 ms                                                                                                          | 172 ms: 1.02x faster                                                                                                  |
| regex_compile  | 124 ms                                                                                                          | 144 ms: 1.16x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.03x slower                                                                                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250727-3.15.0a0-4e40f2b/bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b.json | results/bm-20250727-3.15.0a0-4e40f2b-NOGIL/bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 93.5 ms                                                                                                         | 88.1 ms: 1.06x faster                                                                                                 |
| xml_etree_parse      | 132 ms                                                                                                          | 131 ms: 1.01x faster                                                                                                  |
| json_dumps           | 10.8 ms                                                                                                         | 11.7 ms: 1.09x slower                                                                                                 |
| unpickle_pure_python | 208 us                                                                                                          | 233 us: 1.12x slower                                                                                                  |
| pickle_pure_python   | 309 us                                                                                                          | 347 us: 1.12x slower                                                                                                  |
| tomli_loads          | 1.92 sec                                                                                                        | 2.16 sec: 1.12x slower                                                                                                |
| json_loads           | 28.1 us                                                                                                         | 31.7 us: 1.13x slower                                                                                                 |
| xml_etree_generate   | 83.3 ms                                                                                                         | 95.9 ms: 1.15x slower                                                                                                 |
| xml_etree_process    | 58.1 ms                                                                                                         | 69.5 ms: 1.20x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250727-3.15.0a0-4e40f2b/bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b.json | results/bm-20250727-3.15.0a0-4e40f2b-NOGIL/bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.5 ms                                                                                                         | 15.7 ms: 1.26x slower                                                                                                 |
| python_startup_no_site | 7.24 ms                                                                                                         | 9.54 ms: 1.32x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250727-3.15.0a0-4e40f2b/bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b.json | results/bm-20250727-3.15.0a0-4e40f2b-NOGIL/bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 34.5 ms                                                                                                         | 40.7 ms: 1.18x slower                                                                                                 |
| genshi_xml      | 49.4 ms                                                                                                         | 58.5 ms: 1.18x slower                                                                                                 |
| genshi_text     | 20.9 ms                                                                                                         | 27.3 ms: 1.31x slower                                                                                                 |
| mako            | 11.5 ms                                                                                                         | 15.8 ms: 1.37x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.26x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250727-3.15.0a0-4e40f2b/bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b.json | results/bm-20250727-3.15.0a0-4e40f2b-NOGIL/bm-20250727-vultr-x86_64-python-4e40f2bea7edfa5ba7e2-3.15.0a0-4e40f2b.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.73 ms                                                                                                         | 1.96 ms: 2.41x faster                                                                                                 |
| create_gc_cycles           | 1.97 ms                                                                                                         | 1.54 ms: 1.28x faster                                                                                                 |
| async_tree_io_tg           | 622 ms                                                                                                          | 517 ms: 1.20x faster                                                                                                  |
| async_tree_none_tg         | 259 ms                                                                                                          | 224 ms: 1.16x faster                                                                                                  |
| async_tree_memoization_tg  | 317 ms                                                                                                          | 282 ms: 1.12x faster                                                                                                  |
| sqlite_synth               | 2.30 us                                                                                                         | 2.06 us: 1.12x faster                                                                                                 |
| async_tree_io              | 596 ms                                                                                                          | 537 ms: 1.11x faster                                                                                                  |
| xml_etree_iterparse        | 93.5 ms                                                                                                         | 88.1 ms: 1.06x faster                                                                                                 |
| async_tree_cpu_io_mixed_tg | 501 ms                                                                                                          | 474 ms: 1.06x faster                                                                                                  |
| regex_v8                   | 21.3 ms                                                                                                         | 20.6 ms: 1.04x faster                                                                                                 |
| async_tree_none            | 265 ms                                                                                                          | 256 ms: 1.04x faster                                                                                                  |
| pidigits                   | 194 ms                                                                                                          | 190 ms: 1.02x faster                                                                                                  |
| async_tree_memoization     | 315 ms                                                                                                          | 310 ms: 1.02x faster                                                                                                  |
| regex_dna                  | 175 ms                                                                                                          | 172 ms: 1.02x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 513 ms: 1.01x faster                                                                                                  |
| xml_etree_parse            | 132 ms                                                                                                          | 131 ms: 1.01x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 498 ms                                                                                                          | 500 ms: 1.00x slower                                                                                                  |
| float                      | 70.5 ms                                                                                                         | 70.9 ms: 1.01x slower                                                                                                 |
| pathlib                    | 19.0 ms                                                                                                         | 19.7 ms: 1.03x slower                                                                                                 |
| coroutines                 | 23.7 ms                                                                                                         | 24.5 ms: 1.03x slower                                                                                                 |
| json                       | 5.10 ms                                                                                                         | 5.39 ms: 1.06x slower                                                                                                 |
| bench_mp_pool              | 103 ms                                                                                                          | 108 ms: 1.06x slower                                                                                                  |
| docutils                   | 2.57 sec                                                                                                        | 2.73 sec: 1.06x slower                                                                                                |
| bpe_tokeniser              | 4.18 sec                                                                                                        | 4.44 sec: 1.06x slower                                                                                                |
| pycparser                  | 1.10 sec                                                                                                        | 1.19 sec: 1.08x slower                                                                                                |
| html5lib                   | 62.3 ms                                                                                                         | 67.0 ms: 1.08x slower                                                                                                 |
| sphinx                     | 975 ms                                                                                                          | 1.05 sec: 1.08x slower                                                                                                |
| logging_silent             | 97.5 ns                                                                                                         | 105 ns: 1.08x slower                                                                                                  |
| scimark_sparse_mat_mult    | 5.01 ms                                                                                                         | 5.42 ms: 1.08x slower                                                                                                 |
| dulwich_log                | 66.2 ms                                                                                                         | 71.9 ms: 1.09x slower                                                                                                 |
| json_dumps                 | 10.8 ms                                                                                                         | 11.7 ms: 1.09x slower                                                                                                 |
| scimark_fft                | 332 ms                                                                                                          | 366 ms: 1.10x slower                                                                                                  |
| k_core                     | 2.03 sec                                                                                                        | 2.24 sec: 1.10x slower                                                                                                |
| async_generators           | 341 ms                                                                                                          | 377 ms: 1.11x slower                                                                                                  |
| telco                      | 160 ms                                                                                                          | 177 ms: 1.11x slower                                                                                                  |
| many_optionals             | 1.21 ms                                                                                                         | 1.34 ms: 1.11x slower                                                                                                 |
| pylint                     | 279 ms                                                                                                          | 309 ms: 1.11x slower                                                                                                  |
| generators                 | 28.5 ms                                                                                                         | 31.9 ms: 1.12x slower                                                                                                 |
| unpickle_pure_python       | 208 us                                                                                                          | 233 us: 1.12x slower                                                                                                  |
| pickle_pure_python         | 309 us                                                                                                          | 347 us: 1.12x slower                                                                                                  |
| tomli_loads                | 1.92 sec                                                                                                        | 2.16 sec: 1.12x slower                                                                                                |
| hexiom                     | 5.67 ms                                                                                                         | 6.39 ms: 1.13x slower                                                                                                 |
| json_loads                 | 28.1 us                                                                                                         | 31.7 us: 1.13x slower                                                                                                 |
| comprehensions             | 15.7 us                                                                                                         | 17.7 us: 1.13x slower                                                                                                 |
| nqueens                    | 76.9 ms                                                                                                         | 87.3 ms: 1.14x slower                                                                                                 |
| sympy_expand               | 464 ms                                                                                                          | 528 ms: 1.14x slower                                                                                                  |
| chaos                      | 56.1 ms                                                                                                         | 63.9 ms: 1.14x slower                                                                                                 |
| pyflate                    | 401 ms                                                                                                          | 458 ms: 1.14x slower                                                                                                  |
| 2to3                       | 250 ms                                                                                                          | 286 ms: 1.14x slower                                                                                                  |
| pprint_safe_repr           | 691 ms                                                                                                          | 793 ms: 1.15x slower                                                                                                  |
| xml_etree_generate         | 83.3 ms                                                                                                         | 95.9 ms: 1.15x slower                                                                                                 |
| scimark_lu                 | 111 ms                                                                                                          | 128 ms: 1.15x slower                                                                                                  |
| subparsers                 | 42.7 ms                                                                                                         | 49.4 ms: 1.15x slower                                                                                                 |
| go                         | 105 ms                                                                                                          | 122 ms: 1.16x slower                                                                                                  |
| pprint_pformat             | 1.41 sec                                                                                                        | 1.63 sec: 1.16x slower                                                                                                |
| mdp                        | 1.14 sec                                                                                                        | 1.33 sec: 1.16x slower                                                                                                |
| regex_compile              | 124 ms                                                                                                          | 144 ms: 1.16x slower                                                                                                  |
| logging_simple             | 6.00 us                                                                                                         | 6.98 us: 1.16x slower                                                                                                 |
| scimark_sor                | 108 ms                                                                                                          | 126 ms: 1.17x slower                                                                                                  |
| sqlglot_v2_optimize        | 49.8 ms                                                                                                         | 58.2 ms: 1.17x slower                                                                                                 |
| thrift                     | 757 us                                                                                                          | 887 us: 1.17x slower                                                                                                  |
| spectral_norm              | 94.5 ms                                                                                                         | 111 ms: 1.17x slower                                                                                                  |
| sympy_str                  | 270 ms                                                                                                          | 317 ms: 1.17x slower                                                                                                  |
| logging_format             | 6.80 us                                                                                                         | 7.99 us: 1.17x slower                                                                                                 |
| sympy_integrate            | 18.9 ms                                                                                                         | 22.2 ms: 1.18x slower                                                                                                 |
| deepcopy_reduce            | 2.68 us                                                                                                         | 3.16 us: 1.18x slower                                                                                                 |
| django_template            | 34.5 ms                                                                                                         | 40.7 ms: 1.18x slower                                                                                                 |
| sqlglot_v2_normalize       | 98.5 ms                                                                                                         | 116 ms: 1.18x slower                                                                                                  |
| fannkuch                   | 381 ms                                                                                                          | 450 ms: 1.18x slower                                                                                                  |
| genshi_xml                 | 49.4 ms                                                                                                         | 58.5 ms: 1.18x slower                                                                                                 |
| sympy_sum                  | 153 ms                                                                                                          | 181 ms: 1.19x slower                                                                                                  |
| xml_etree_process          | 58.1 ms                                                                                                         | 69.5 ms: 1.20x slower                                                                                                 |
| deepcopy                   | 251 us                                                                                                          | 301 us: 1.20x slower                                                                                                  |
| deltablue                  | 3.05 ms                                                                                                         | 3.66 ms: 1.20x slower                                                                                                 |
| shortest_path              | 441 ms                                                                                                          | 531 ms: 1.20x slower                                                                                                  |
| meteor_contest             | 99.0 ms                                                                                                         | 120 ms: 1.21x slower                                                                                                  |
| deepcopy_memo              | 28.5 us                                                                                                         | 34.8 us: 1.22x slower                                                                                                 |
| raytrace                   | 249 ms                                                                                                          | 305 ms: 1.22x slower                                                                                                  |
| connected_components       | 398 ms                                                                                                          | 490 ms: 1.23x slower                                                                                                  |
| typing_runtime_protocols   | 154 us                                                                                                          | 189 us: 1.23x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.50 ms                                                                                                         | 1.85 ms: 1.23x slower                                                                                                 |
| sqlglot_v2_parse           | 1.20 ms                                                                                                         | 1.49 ms: 1.24x slower                                                                                                 |
| scimark_monte_carlo        | 63.0 ms                                                                                                         | 78.7 ms: 1.25x slower                                                                                                 |
| crypto_pyaes               | 68.8 ms                                                                                                         | 86.3 ms: 1.25x slower                                                                                                 |
| python_startup             | 12.5 ms                                                                                                         | 15.7 ms: 1.26x slower                                                                                                 |
| richards                   | 41.1 ms                                                                                                         | 51.9 ms: 1.26x slower                                                                                                 |
| richards_super             | 47.1 ms                                                                                                         | 60.0 ms: 1.27x slower                                                                                                 |
| genshi_text                | 20.9 ms                                                                                                         | 27.3 ms: 1.31x slower                                                                                                 |
| python_startup_no_site     | 7.24 ms                                                                                                         | 9.54 ms: 1.32x slower                                                                                                 |
| coverage                   | 81.2 ms                                                                                                         | 111 ms: 1.36x slower                                                                                                  |
| mako                       | 11.5 ms                                                                                                         | 15.8 ms: 1.37x slower                                                                                                 |
| nbody                      | 89.5 ms                                                                                                         | 127 ms: 1.41x slower                                                                                                  |
| bench_thread_pool          | 1.04 ms                                                                                                         | 3.16 ms: 3.02x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.12x slower                                                                                                          |

Benchmark hidden because not significant (1): regex_effbot

- Geometric mean (including insignificant results): 1.093x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.20x