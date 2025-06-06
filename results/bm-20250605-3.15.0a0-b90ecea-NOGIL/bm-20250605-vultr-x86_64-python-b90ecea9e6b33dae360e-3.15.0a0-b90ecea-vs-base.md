# Results vs. base

- fork: python
- ref: b90ecea9e6b33dae360e
- machine: linux-x86_64
- commit hash: b90ecea
- commit date: 2025-06-05
- overall geometric mean: 1.086x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250605-3.15.0a0-b90ecea/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea.json | results/bm-20250605-3.15.0a0-b90ecea-NOGIL/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                                                          | 283 ms: 1.13x slower                                                                                                  |
| docutils       | 2.53 sec                                                                                                        | 2.70 sec: 1.07x slower                                                                                                |
| html5lib       | 60.9 ms                                                                                                         | 66.9 ms: 1.10x slower                                                                                                 |
| sphinx         | 976 ms                                                                                                          | 1.06 sec: 1.09x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250605-3.15.0a0-b90ecea/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea.json | results/bm-20250605-3.15.0a0-b90ecea-NOGIL/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 618 ms                                                                                                          | 527 ms: 1.17x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 507 ms                                                                                                          | 464 ms: 1.09x faster                                                                                                  |
| async_tree_none_tg         | 249 ms                                                                                                          | 228 ms: 1.09x faster                                                                                                  |
| async_tree_memoization_tg  | 307 ms                                                                                                          | 285 ms: 1.08x faster                                                                                                  |
| async_tree_io              | 593 ms                                                                                                          | 555 ms: 1.07x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 518 ms                                                                                                          | 489 ms: 1.06x faster                                                                                                  |
| async_tree_none            | 265 ms                                                                                                          | 258 ms: 1.03x faster                                                                                                  |
| coroutines                 | 23.8 ms                                                                                                         | 23.1 ms: 1.03x faster                                                                                                 |
| asyncio_websockets         | 517 ms                                                                                                          | 514 ms: 1.01x faster                                                                                                  |
| async_generators           | 332 ms                                                                                                          | 373 ms: 1.12x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.04x faster                                                                                                          |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250605-3.15.0a0-b90ecea/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea.json | results/bm-20250605-3.15.0a0-b90ecea-NOGIL/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 195 ms                                                                                                          | 190 ms: 1.03x faster                                                                                                  |
| float          | 70.8 ms                                                                                                         | 68.8 ms: 1.03x faster                                                                                                 |
| nbody          | 86.4 ms                                                                                                         | 120 ms: 1.39x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250605-3.15.0a0-b90ecea/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea.json | results/bm-20250605-3.15.0a0-b90ecea-NOGIL/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                                                                         | 20.2 ms: 1.12x faster                                                                                                 |
| regex_effbot   | 2.92 ms                                                                                                         | 2.66 ms: 1.10x faster                                                                                                 |
| regex_dna      | 176 ms                                                                                                          | 172 ms: 1.02x faster                                                                                                  |
| regex_compile  | 124 ms                                                                                                          | 144 ms: 1.16x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.02x faster                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250605-3.15.0a0-b90ecea/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea.json | results/bm-20250605-3.15.0a0-b90ecea-NOGIL/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 91.8 ms                                                                                                         | 87.5 ms: 1.05x faster                                                                                                 |
| xml_etree_parse      | 130 ms                                                                                                          | 128 ms: 1.01x faster                                                                                                  |
| unpickle_pure_python | 210 us                                                                                                          | 229 us: 1.09x slower                                                                                                  |
| json_loads           | 28.2 us                                                                                                         | 31.0 us: 1.10x slower                                                                                                 |
| pickle_pure_python   | 306 us                                                                                                          | 336 us: 1.10x slower                                                                                                  |
| json_dumps           | 10.8 ms                                                                                                         | 12.1 ms: 1.12x slower                                                                                                 |
| tomli_loads          | 1.90 sec                                                                                                        | 2.14 sec: 1.12x slower                                                                                                |
| xml_etree_generate   | 82.7 ms                                                                                                         | 94.8 ms: 1.15x slower                                                                                                 |
| xml_etree_process    | 58.2 ms                                                                                                         | 68.8 ms: 1.18x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250605-3.15.0a0-b90ecea/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea.json | results/bm-20250605-3.15.0a0-b90ecea-NOGIL/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.5 ms                                                                                                         | 16.0 ms: 1.28x slower                                                                                                 |
| python_startup_no_site | 7.28 ms                                                                                                         | 9.58 ms: 1.32x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.30x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250605-3.15.0a0-b90ecea/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea.json | results/bm-20250605-3.15.0a0-b90ecea-NOGIL/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 34.6 ms                                                                                                         | 39.8 ms: 1.15x slower                                                                                                 |
| genshi_xml      | 48.1 ms                                                                                                         | 58.3 ms: 1.21x slower                                                                                                 |
| genshi_text     | 20.3 ms                                                                                                         | 26.4 ms: 1.30x slower                                                                                                 |
| mako            | 11.8 ms                                                                                                         | 15.8 ms: 1.34x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.25x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250605-3.15.0a0-b90ecea/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea.json | results/bm-20250605-3.15.0a0-b90ecea-NOGIL/bm-20250605-vultr-x86_64-python-b90ecea9e6b33dae360e-3.15.0a0-b90ecea.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.37 ms                                                                                                         | 1.90 ms: 2.30x faster                                                                                                 |
| create_gc_cycles           | 1.91 ms                                                                                                         | 1.46 ms: 1.30x faster                                                                                                 |
| async_tree_io_tg           | 618 ms                                                                                                          | 527 ms: 1.17x faster                                                                                                  |
| regex_v8                   | 22.7 ms                                                                                                         | 20.2 ms: 1.12x faster                                                                                                 |
| regex_effbot               | 2.92 ms                                                                                                         | 2.66 ms: 1.10x faster                                                                                                 |
| async_tree_cpu_io_mixed_tg | 507 ms                                                                                                          | 464 ms: 1.09x faster                                                                                                  |
| async_tree_none_tg         | 249 ms                                                                                                          | 228 ms: 1.09x faster                                                                                                  |
| sqlite_synth               | 2.23 us                                                                                                         | 2.07 us: 1.08x faster                                                                                                 |
| async_tree_memoization_tg  | 307 ms                                                                                                          | 285 ms: 1.08x faster                                                                                                  |
| async_tree_io              | 593 ms                                                                                                          | 555 ms: 1.07x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 518 ms                                                                                                          | 489 ms: 1.06x faster                                                                                                  |
| xml_etree_iterparse        | 91.8 ms                                                                                                         | 87.5 ms: 1.05x faster                                                                                                 |
| async_tree_none            | 265 ms                                                                                                          | 258 ms: 1.03x faster                                                                                                  |
| pidigits                   | 195 ms                                                                                                          | 190 ms: 1.03x faster                                                                                                  |
| float                      | 70.8 ms                                                                                                         | 68.8 ms: 1.03x faster                                                                                                 |
| coroutines                 | 23.8 ms                                                                                                         | 23.1 ms: 1.03x faster                                                                                                 |
| regex_dna                  | 176 ms                                                                                                          | 172 ms: 1.02x faster                                                                                                  |
| xml_etree_parse            | 130 ms                                                                                                          | 128 ms: 1.01x faster                                                                                                  |
| asyncio_websockets         | 517 ms                                                                                                          | 514 ms: 1.01x faster                                                                                                  |
| pathlib                    | 19.3 ms                                                                                                         | 19.6 ms: 1.01x slower                                                                                                 |
| json                       | 5.09 ms                                                                                                         | 5.30 ms: 1.04x slower                                                                                                 |
| bench_mp_pool              | 98.0 ms                                                                                                         | 103 ms: 1.05x slower                                                                                                  |
| bpe_tokeniser              | 4.15 sec                                                                                                        | 4.37 sec: 1.05x slower                                                                                                |
| docutils                   | 2.53 sec                                                                                                        | 2.70 sec: 1.07x slower                                                                                                |
| dulwich_log                | 66.2 ms                                                                                                         | 71.4 ms: 1.08x slower                                                                                                 |
| deltablue                  | 3.31 ms                                                                                                         | 3.58 ms: 1.08x slower                                                                                                 |
| scimark_sor                | 112 ms                                                                                                          | 122 ms: 1.08x slower                                                                                                  |
| scimark_fft                | 327 ms                                                                                                          | 356 ms: 1.09x slower                                                                                                  |
| sphinx                     | 976 ms                                                                                                          | 1.06 sec: 1.09x slower                                                                                                |
| unpickle_pure_python       | 210 us                                                                                                          | 229 us: 1.09x slower                                                                                                  |
| k_core                     | 2.04 sec                                                                                                        | 2.24 sec: 1.10x slower                                                                                                |
| hexiom                     | 5.74 ms                                                                                                         | 6.30 ms: 1.10x slower                                                                                                 |
| comprehensions             | 15.8 us                                                                                                         | 17.4 us: 1.10x slower                                                                                                 |
| json_loads                 | 28.2 us                                                                                                         | 31.0 us: 1.10x slower                                                                                                 |
| html5lib                   | 60.9 ms                                                                                                         | 66.9 ms: 1.10x slower                                                                                                 |
| pickle_pure_python         | 306 us                                                                                                          | 336 us: 1.10x slower                                                                                                  |
| chaos                      | 56.1 ms                                                                                                         | 61.9 ms: 1.10x slower                                                                                                 |
| many_optionals             | 1.03 ms                                                                                                         | 1.14 ms: 1.10x slower                                                                                                 |
| spectral_norm              | 99.3 ms                                                                                                         | 110 ms: 1.10x slower                                                                                                  |
| pylint                     | 277 ms                                                                                                          | 307 ms: 1.11x slower                                                                                                  |
| scimark_sparse_mat_mult    | 4.64 ms                                                                                                         | 5.17 ms: 1.11x slower                                                                                                 |
| nqueens                    | 75.8 ms                                                                                                         | 84.6 ms: 1.12x slower                                                                                                 |
| logging_silent             | 469 ns                                                                                                          | 524 ns: 1.12x slower                                                                                                  |
| json_dumps                 | 10.8 ms                                                                                                         | 12.1 ms: 1.12x slower                                                                                                 |
| deepcopy_reduce            | 2.65 us                                                                                                         | 2.97 us: 1.12x slower                                                                                                 |
| async_generators           | 332 ms                                                                                                          | 373 ms: 1.12x slower                                                                                                  |
| generators                 | 27.7 ms                                                                                                         | 31.1 ms: 1.12x slower                                                                                                 |
| tomli_loads                | 1.90 sec                                                                                                        | 2.14 sec: 1.12x slower                                                                                                |
| pprint_safe_repr           | 777 ms                                                                                                          | 878 ms: 1.13x slower                                                                                                  |
| 2to3                       | 249 ms                                                                                                          | 283 ms: 1.13x slower                                                                                                  |
| subparsers                 | 25.1 ms                                                                                                         | 28.5 ms: 1.14x slower                                                                                                 |
| sqlglot_v2_optimize        | 49.6 ms                                                                                                         | 56.4 ms: 1.14x slower                                                                                                 |
| go                         | 106 ms                                                                                                          | 121 ms: 1.14x slower                                                                                                  |
| pprint_pformat             | 1.59 sec                                                                                                        | 1.82 sec: 1.14x slower                                                                                                |
| xml_etree_generate         | 82.7 ms                                                                                                         | 94.8 ms: 1.15x slower                                                                                                 |
| mdp                        | 1.14 sec                                                                                                        | 1.31 sec: 1.15x slower                                                                                                |
| scimark_lu                 | 111 ms                                                                                                          | 128 ms: 1.15x slower                                                                                                  |
| django_template            | 34.6 ms                                                                                                         | 39.8 ms: 1.15x slower                                                                                                 |
| pyflate                    | 407 ms                                                                                                          | 470 ms: 1.16x slower                                                                                                  |
| sqlglot_v2_normalize       | 98.1 ms                                                                                                         | 113 ms: 1.16x slower                                                                                                  |
| thrift                     | 752 us                                                                                                          | 870 us: 1.16x slower                                                                                                  |
| regex_compile              | 124 ms                                                                                                          | 144 ms: 1.16x slower                                                                                                  |
| deepcopy                   | 253 us                                                                                                          | 295 us: 1.17x slower                                                                                                  |
| raytrace                   | 251 ms                                                                                                          | 294 ms: 1.17x slower                                                                                                  |
| xml_etree_process          | 58.2 ms                                                                                                         | 68.8 ms: 1.18x slower                                                                                                 |
| sympy_integrate            | 18.7 ms                                                                                                         | 22.1 ms: 1.18x slower                                                                                                 |
| telco                      | 7.27 ms                                                                                                         | 8.59 ms: 1.18x slower                                                                                                 |
| sympy_expand               | 447 ms                                                                                                          | 528 ms: 1.18x slower                                                                                                  |
| sympy_str                  | 266 ms                                                                                                          | 315 ms: 1.18x slower                                                                                                  |
| sympy_sum                  | 152 ms                                                                                                          | 181 ms: 1.19x slower                                                                                                  |
| logging_simple             | 6.48 us                                                                                                         | 7.71 us: 1.19x slower                                                                                                 |
| deepcopy_memo              | 29.1 us                                                                                                         | 34.8 us: 1.20x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.49 ms                                                                                                         | 1.79 ms: 1.20x slower                                                                                                 |
| fannkuch                   | 387 ms                                                                                                          | 465 ms: 1.20x slower                                                                                                  |
| logging_format             | 7.28 us                                                                                                         | 8.75 us: 1.20x slower                                                                                                 |
| genshi_xml                 | 48.1 ms                                                                                                         | 58.3 ms: 1.21x slower                                                                                                 |
| sqlglot_v2_parse           | 1.20 ms                                                                                                         | 1.46 ms: 1.21x slower                                                                                                 |
| richards                   | 41.6 ms                                                                                                         | 50.8 ms: 1.22x slower                                                                                                 |
| shortest_path              | 438 ms                                                                                                          | 540 ms: 1.23x slower                                                                                                  |
| meteor_contest             | 100 ms                                                                                                          | 124 ms: 1.24x slower                                                                                                  |
| typing_runtime_protocols   | 151 us                                                                                                          | 188 us: 1.24x slower                                                                                                  |
| richards_super             | 46.8 ms                                                                                                         | 58.2 ms: 1.24x slower                                                                                                 |
| connected_components       | 395 ms                                                                                                          | 491 ms: 1.24x slower                                                                                                  |
| scimark_monte_carlo        | 61.6 ms                                                                                                         | 76.8 ms: 1.25x slower                                                                                                 |
| python_startup             | 12.5 ms                                                                                                         | 16.0 ms: 1.28x slower                                                                                                 |
| crypto_pyaes               | 67.0 ms                                                                                                         | 85.9 ms: 1.28x slower                                                                                                 |
| genshi_text                | 20.3 ms                                                                                                         | 26.4 ms: 1.30x slower                                                                                                 |
| python_startup_no_site     | 7.28 ms                                                                                                         | 9.58 ms: 1.32x slower                                                                                                 |
| mako                       | 11.8 ms                                                                                                         | 15.8 ms: 1.34x slower                                                                                                 |
| coverage                   | 81.5 ms                                                                                                         | 111 ms: 1.36x slower                                                                                                  |
| nbody                      | 86.4 ms                                                                                                         | 120 ms: 1.39x slower                                                                                                  |
| bench_thread_pool          | 1.04 ms                                                                                                         | 3.11 ms: 2.99x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.11x slower                                                                                                          |

Benchmark hidden because not significant (2): pycparser, async_tree_memoization

- Geometric mean (including insignificant results): 1.086x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.23x