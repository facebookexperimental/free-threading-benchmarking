# Results vs. base

- fork: python
- ref: 9ad0c7b0f14c5fcda6bf
- machine: linux-x86_64
- commit hash: 9ad0c7b
- commit date: 2025-05-13
- overall geometric mean: 1.090x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250513-3.15.0a0-9ad0c7b/bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json | results/bm-20250513-3.15.0a0-9ad0c7b-NOGIL/bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 250 ms                                                                                                          | 285 ms: 1.14x slower                                                                                                  |
| docutils       | 2.51 sec                                                                                                        | 2.70 sec: 1.08x slower                                                                                                |
| html5lib       | 60.8 ms                                                                                                         | 65.4 ms: 1.07x slower                                                                                                 |
| sphinx         | 972 ms                                                                                                          | 1.07 sec: 1.10x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250513-3.15.0a0-9ad0c7b/bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json | results/bm-20250513-3.15.0a0-9ad0c7b-NOGIL/bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 629 ms                                                                                                          | 517 ms: 1.22x faster                                                                                                  |
| async_tree_none_tg         | 255 ms                                                                                                          | 225 ms: 1.13x faster                                                                                                  |
| async_tree_memoization_tg  | 311 ms                                                                                                          | 282 ms: 1.10x faster                                                                                                  |
| async_tree_io              | 598 ms                                                                                                          | 545 ms: 1.10x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 512 ms                                                                                                          | 481 ms: 1.06x faster                                                                                                  |
| async_tree_none            | 271 ms                                                                                                          | 257 ms: 1.06x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 522 ms                                                                                                          | 508 ms: 1.03x faster                                                                                                  |
| coroutines                 | 23.6 ms                                                                                                         | 23.0 ms: 1.03x faster                                                                                                 |
| async_tree_memoization     | 310 ms                                                                                                          | 308 ms: 1.01x faster                                                                                                  |
| async_generators           | 336 ms                                                                                                          | 367 ms: 1.09x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.06x faster                                                                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250513-3.15.0a0-9ad0c7b/bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json | results/bm-20250513-3.15.0a0-9ad0c7b-NOGIL/bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 197 ms                                                                                                          | 190 ms: 1.04x faster                                                                                                  |
| float          | 70.3 ms                                                                                                         | 69.4 ms: 1.01x faster                                                                                                 |
| nbody          | 88.8 ms                                                                                                         | 117 ms: 1.32x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250513-3.15.0a0-9ad0c7b/bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json | results/bm-20250513-3.15.0a0-9ad0c7b-NOGIL/bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.3 ms                                                                                                         | 20.8 ms: 1.07x faster                                                                                                 |
| regex_dna      | 173 ms                                                                                                          | 181 ms: 1.05x slower                                                                                                  |
| regex_effbot   | 2.69 ms                                                                                                         | 2.82 ms: 1.05x slower                                                                                                 |
| regex_compile  | 123 ms                                                                                                          | 145 ms: 1.17x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.05x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250513-3.15.0a0-9ad0c7b/bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json | results/bm-20250513-3.15.0a0-9ad0c7b-NOGIL/bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 91.0 ms                                                                                                         | 86.7 ms: 1.05x faster                                                                                                 |
| xml_etree_parse      | 131 ms                                                                                                          | 130 ms: 1.01x faster                                                                                                  |
| json_loads           | 29.4 us                                                                                                         | 30.1 us: 1.02x slower                                                                                                 |
| json_dumps           | 10.8 ms                                                                                                         | 11.5 ms: 1.07x slower                                                                                                 |
| unpickle_pure_python | 208 us                                                                                                          | 229 us: 1.10x slower                                                                                                  |
| pickle_pure_python   | 303 us                                                                                                          | 334 us: 1.10x slower                                                                                                  |
| tomli_loads          | 1.89 sec                                                                                                        | 2.15 sec: 1.14x slower                                                                                                |
| xml_etree_generate   | 82.4 ms                                                                                                         | 97.0 ms: 1.18x slower                                                                                                 |
| xml_etree_process    | 57.5 ms                                                                                                         | 69.6 ms: 1.21x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250513-3.15.0a0-9ad0c7b/bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json | results/bm-20250513-3.15.0a0-9ad0c7b-NOGIL/bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                                                                         | 16.0 ms: 1.27x slower                                                                                                 |
| python_startup_no_site | 7.33 ms                                                                                                         | 9.60 ms: 1.31x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250513-3.15.0a0-9ad0c7b/bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json | results/bm-20250513-3.15.0a0-9ad0c7b-NOGIL/bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 47.6 ms                                                                                                         | 54.9 ms: 1.15x slower                                                                                                 |
| django_template | 34.1 ms                                                                                                         | 39.6 ms: 1.16x slower                                                                                                 |
| genshi_text     | 20.2 ms                                                                                                         | 26.0 ms: 1.29x slower                                                                                                 |
| mako            | 11.9 ms                                                                                                         | 15.8 ms: 1.33x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.23x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250513-3.15.0a0-9ad0c7b/bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json | results/bm-20250513-3.15.0a0-9ad0c7b-NOGIL/bm-20250513-vultr-x86_64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.72 ms                                                                                                         | 1.91 ms: 2.47x faster                                                                                                 |
| create_gc_cycles           | 1.90 ms                                                                                                         | 1.49 ms: 1.28x faster                                                                                                 |
| async_tree_io_tg           | 629 ms                                                                                                          | 517 ms: 1.22x faster                                                                                                  |
| async_tree_none_tg         | 255 ms                                                                                                          | 225 ms: 1.13x faster                                                                                                  |
| async_tree_memoization_tg  | 311 ms                                                                                                          | 282 ms: 1.10x faster                                                                                                  |
| async_tree_io              | 598 ms                                                                                                          | 545 ms: 1.10x faster                                                                                                  |
| sqlite_synth               | 2.23 us                                                                                                         | 2.07 us: 1.08x faster                                                                                                 |
| regex_v8                   | 22.3 ms                                                                                                         | 20.8 ms: 1.07x faster                                                                                                 |
| async_tree_cpu_io_mixed_tg | 512 ms                                                                                                          | 481 ms: 1.06x faster                                                                                                  |
| async_tree_none            | 271 ms                                                                                                          | 257 ms: 1.06x faster                                                                                                  |
| xml_etree_iterparse        | 91.0 ms                                                                                                         | 86.7 ms: 1.05x faster                                                                                                 |
| pidigits                   | 197 ms                                                                                                          | 190 ms: 1.04x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 522 ms                                                                                                          | 508 ms: 1.03x faster                                                                                                  |
| coroutines                 | 23.6 ms                                                                                                         | 23.0 ms: 1.03x faster                                                                                                 |
| json                       | 5.28 ms                                                                                                         | 5.20 ms: 1.02x faster                                                                                                 |
| float                      | 70.3 ms                                                                                                         | 69.4 ms: 1.01x faster                                                                                                 |
| async_tree_memoization     | 310 ms                                                                                                          | 308 ms: 1.01x faster                                                                                                  |
| xml_etree_parse            | 131 ms                                                                                                          | 130 ms: 1.01x faster                                                                                                  |
| pathlib                    | 19.5 ms                                                                                                         | 19.7 ms: 1.01x slower                                                                                                 |
| json_loads                 | 29.4 us                                                                                                         | 30.1 us: 1.02x slower                                                                                                 |
| pycparser                  | 1.09 sec                                                                                                        | 1.14 sec: 1.04x slower                                                                                                |
| regex_dna                  | 173 ms                                                                                                          | 181 ms: 1.05x slower                                                                                                  |
| regex_effbot               | 2.69 ms                                                                                                         | 2.82 ms: 1.05x slower                                                                                                 |
| bench_mp_pool              | 99.0 ms                                                                                                         | 104 ms: 1.05x slower                                                                                                  |
| json_dumps                 | 10.8 ms                                                                                                         | 11.5 ms: 1.07x slower                                                                                                 |
| bpe_tokeniser              | 4.13 sec                                                                                                        | 4.44 sec: 1.07x slower                                                                                                |
| html5lib                   | 60.8 ms                                                                                                         | 65.4 ms: 1.07x slower                                                                                                 |
| docutils                   | 2.51 sec                                                                                                        | 2.70 sec: 1.08x slower                                                                                                |
| dulwich_log                | 66.9 ms                                                                                                         | 72.0 ms: 1.08x slower                                                                                                 |
| async_generators           | 336 ms                                                                                                          | 367 ms: 1.09x slower                                                                                                  |
| pprint_safe_repr           | 708 ms                                                                                                          | 774 ms: 1.09x slower                                                                                                  |
| deepcopy_reduce            | 2.66 us                                                                                                         | 2.92 us: 1.10x slower                                                                                                 |
| scimark_fft                | 330 ms                                                                                                          | 362 ms: 1.10x slower                                                                                                  |
| unpickle_pure_python       | 208 us                                                                                                          | 229 us: 1.10x slower                                                                                                  |
| pylint                     | 278 ms                                                                                                          | 306 ms: 1.10x slower                                                                                                  |
| scimark_sparse_mat_mult    | 4.78 ms                                                                                                         | 5.26 ms: 1.10x slower                                                                                                 |
| many_optionals             | 1.05 ms                                                                                                         | 1.15 ms: 1.10x slower                                                                                                 |
| sphinx                     | 972 ms                                                                                                          | 1.07 sec: 1.10x slower                                                                                                |
| pickle_pure_python         | 303 us                                                                                                          | 334 us: 1.10x slower                                                                                                  |
| k_core                     | 2.03 sec                                                                                                        | 2.24 sec: 1.11x slower                                                                                                |
| pprint_pformat             | 1.45 sec                                                                                                        | 1.60 sec: 1.11x slower                                                                                                |
| generators                 | 27.7 ms                                                                                                         | 30.9 ms: 1.12x slower                                                                                                 |
| nqueens                    | 78.1 ms                                                                                                         | 87.6 ms: 1.12x slower                                                                                                 |
| deltablue                  | 3.16 ms                                                                                                         | 3.54 ms: 1.12x slower                                                                                                 |
| scimark_sor                | 109 ms                                                                                                          | 123 ms: 1.13x slower                                                                                                  |
| tomli_loads                | 1.89 sec                                                                                                        | 2.15 sec: 1.14x slower                                                                                                |
| 2to3                       | 250 ms                                                                                                          | 285 ms: 1.14x slower                                                                                                  |
| chaos                      | 54.9 ms                                                                                                         | 62.8 ms: 1.14x slower                                                                                                 |
| deepcopy                   | 252 us                                                                                                          | 288 us: 1.14x slower                                                                                                  |
| mdp                        | 1.16 sec                                                                                                        | 1.33 sec: 1.15x slower                                                                                                |
| sqlglot_v2_optimize        | 49.7 ms                                                                                                         | 57.0 ms: 1.15x slower                                                                                                 |
| subparsers                 | 24.8 ms                                                                                                         | 28.5 ms: 1.15x slower                                                                                                 |
| logging_silent             | 467 ns                                                                                                          | 538 ns: 1.15x slower                                                                                                  |
| genshi_xml                 | 47.6 ms                                                                                                         | 54.9 ms: 1.15x slower                                                                                                 |
| sqlglot_v2_normalize       | 98.8 ms                                                                                                         | 114 ms: 1.15x slower                                                                                                  |
| sympy_sum                  | 153 ms                                                                                                          | 178 ms: 1.16x slower                                                                                                  |
| comprehensions             | 16.8 us                                                                                                         | 19.6 us: 1.16x slower                                                                                                 |
| go                         | 106 ms                                                                                                          | 123 ms: 1.16x slower                                                                                                  |
| django_template            | 34.1 ms                                                                                                         | 39.6 ms: 1.16x slower                                                                                                 |
| raytrace                   | 252 ms                                                                                                          | 295 ms: 1.17x slower                                                                                                  |
| sympy_expand               | 453 ms                                                                                                          | 530 ms: 1.17x slower                                                                                                  |
| scimark_lu                 | 107 ms                                                                                                          | 126 ms: 1.17x slower                                                                                                  |
| regex_compile              | 123 ms                                                                                                          | 145 ms: 1.17x slower                                                                                                  |
| xml_etree_generate         | 82.4 ms                                                                                                         | 97.0 ms: 1.18x slower                                                                                                 |
| sympy_str                  | 267 ms                                                                                                          | 315 ms: 1.18x slower                                                                                                  |
| sympy_integrate            | 18.8 ms                                                                                                         | 22.1 ms: 1.18x slower                                                                                                 |
| telco                      | 7.35 ms                                                                                                         | 8.77 ms: 1.19x slower                                                                                                 |
| thrift                     | 731 us                                                                                                          | 873 us: 1.20x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.51 ms                                                                                                         | 1.81 ms: 1.20x slower                                                                                                 |
| logging_simple             | 6.58 us                                                                                                         | 7.88 us: 1.20x slower                                                                                                 |
| sqlglot_v2_parse           | 1.21 ms                                                                                                         | 1.45 ms: 1.20x slower                                                                                                 |
| hexiom                     | 5.57 ms                                                                                                         | 6.69 ms: 1.20x slower                                                                                                 |
| spectral_norm              | 94.8 ms                                                                                                         | 114 ms: 1.20x slower                                                                                                  |
| pyflate                    | 397 ms                                                                                                          | 479 ms: 1.21x slower                                                                                                  |
| xml_etree_process          | 57.5 ms                                                                                                         | 69.6 ms: 1.21x slower                                                                                                 |
| logging_format             | 7.24 us                                                                                                         | 8.81 us: 1.22x slower                                                                                                 |
| scimark_monte_carlo        | 62.4 ms                                                                                                         | 76.1 ms: 1.22x slower                                                                                                 |
| shortest_path              | 433 ms                                                                                                          | 530 ms: 1.23x slower                                                                                                  |
| deepcopy_memo              | 28.8 us                                                                                                         | 35.4 us: 1.23x slower                                                                                                 |
| connected_components       | 392 ms                                                                                                          | 483 ms: 1.23x slower                                                                                                  |
| crypto_pyaes               | 68.6 ms                                                                                                         | 84.7 ms: 1.23x slower                                                                                                 |
| richards_super             | 45.6 ms                                                                                                         | 57.1 ms: 1.25x slower                                                                                                 |
| richards                   | 39.8 ms                                                                                                         | 49.9 ms: 1.25x slower                                                                                                 |
| typing_runtime_protocols   | 153 us                                                                                                          | 192 us: 1.26x slower                                                                                                  |
| fannkuch                   | 372 ms                                                                                                          | 468 ms: 1.26x slower                                                                                                  |
| python_startup             | 12.6 ms                                                                                                         | 16.0 ms: 1.27x slower                                                                                                 |
| genshi_text                | 20.2 ms                                                                                                         | 26.0 ms: 1.29x slower                                                                                                 |
| meteor_contest             | 99.3 ms                                                                                                         | 129 ms: 1.30x slower                                                                                                  |
| python_startup_no_site     | 7.33 ms                                                                                                         | 9.60 ms: 1.31x slower                                                                                                 |
| nbody                      | 88.8 ms                                                                                                         | 117 ms: 1.32x slower                                                                                                  |
| mako                       | 11.9 ms                                                                                                         | 15.8 ms: 1.33x slower                                                                                                 |
| coverage                   | 81.7 ms                                                                                                         | 109 ms: 1.33x slower                                                                                                  |
| bench_thread_pool          | 1.05 ms                                                                                                         | 3.13 ms: 2.99x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.11x slower                                                                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

- Geometric mean (including insignificant results): 1.090x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.23x