# Results vs. base

- fork: python
- ref: a936af924efc6e2fb59e
- machine: linux-x86_64
- commit hash: a936af9
- commit date: 2025-03-17
- overall geometric mean: 1.113x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250317-3.14.0a6+-a936af9/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json | results/bm-20250317-3.14.0a6+-a936af9-NOGIL/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 258 ms                                                                                                            | 301 ms: 1.17x slower                                                                                                    |
| docutils       | 2.62 sec                                                                                                          | 2.81 sec: 1.07x slower                                                                                                  |
| sphinx         | 1.01 sec                                                                                                          | 1.10 sec: 1.09x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.11x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250317-3.14.0a6+-a936af9/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json | results/bm-20250317-3.14.0a6+-a936af9-NOGIL/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 636 ms                                                                                                            | 562 ms: 1.13x faster                                                                                                    |
| async_tree_none_tg         | 265 ms                                                                                                            | 240 ms: 1.10x faster                                                                                                    |
| async_tree_io              | 636 ms                                                                                                            | 587 ms: 1.08x faster                                                                                                    |
| async_tree_memoization_tg  | 314 ms                                                                                                            | 309 ms: 1.02x faster                                                                                                    |
| async_tree_none            | 276 ms                                                                                                            | 280 ms: 1.02x slower                                                                                                    |
| coroutines                 | 23.2 ms                                                                                                           | 23.9 ms: 1.03x slower                                                                                                   |
| async_tree_memoization     | 332 ms                                                                                                            | 343 ms: 1.03x slower                                                                                                    |
| async_generators           | 339 ms                                                                                                            | 380 ms: 1.12x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 499 ms                                                                                                            | 576 ms: 1.15x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 512 ms                                                                                                            | 610 ms: 1.19x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.02x slower                                                                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250317-3.14.0a6+-a936af9/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json | results/bm-20250317-3.14.0a6+-a936af9-NOGIL/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| float          | 75.8 ms                                                                                                           | 79.0 ms: 1.04x slower                                                                                                   |
| pidigits       | 195 ms                                                                                                            | 221 ms: 1.13x slower                                                                                                    |
| nbody          | 104 ms                                                                                                            | 134 ms: 1.29x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.15x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250317-3.14.0a6+-a936af9/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json | results/bm-20250317-3.14.0a6+-a936af9-NOGIL/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 2.76 ms                                                                                                           | 2.67 ms: 1.03x faster                                                                                                   |
| regex_v8       | 24.6 ms                                                                                                           | 24.1 ms: 1.02x faster                                                                                                   |
| regex_dna      | 171 ms                                                                                                            | 176 ms: 1.02x slower                                                                                                    |
| regex_compile  | 130 ms                                                                                                            | 160 ms: 1.24x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.05x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250317-3.14.0a6+-a936af9/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json | results/bm-20250317-3.14.0a6+-a936af9-NOGIL/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 93.0 ms                                                                                                           | 88.8 ms: 1.05x faster                                                                                                   |
| xml_etree_parse      | 129 ms                                                                                                            | 130 ms: 1.00x slower                                                                                                    |
| json_loads           | 27.5 us                                                                                                           | 29.5 us: 1.07x slower                                                                                                   |
| pickle_pure_python   | 326 us                                                                                                            | 364 us: 1.12x slower                                                                                                    |
| json_dumps           | 11.3 ms                                                                                                           | 12.9 ms: 1.14x slower                                                                                                   |
| xml_etree_generate   | 85.3 ms                                                                                                           | 97.8 ms: 1.15x slower                                                                                                   |
| unpickle_pure_python | 225 us                                                                                                            | 259 us: 1.15x slower                                                                                                    |
| tomli_loads          | 2.01 sec                                                                                                          | 2.36 sec: 1.18x slower                                                                                                  |
| xml_etree_process    | 59.8 ms                                                                                                           | 70.9 ms: 1.19x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.10x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250317-3.14.0a6+-a936af9/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json | results/bm-20250317-3.14.0a6+-a936af9-NOGIL/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 14.9 ms                                                                                                           | 15.8 ms: 1.06x slower                                                                                                   |
| python_startup_no_site | 8.61 ms                                                                                                           | 11.1 ms: 1.29x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.17x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250317-3.14.0a6+-a936af9/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json | results/bm-20250317-3.14.0a6+-a936af9-NOGIL/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 51.8 ms                                                                                                           | 61.5 ms: 1.19x slower                                                                                                   |
| django_template | 36.5 ms                                                                                                           | 44.1 ms: 1.21x slower                                                                                                   |
| genshi_text     | 22.2 ms                                                                                                           | 29.1 ms: 1.31x slower                                                                                                   |
| mako            | 12.1 ms                                                                                                           | 16.0 ms: 1.31x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.25x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250317-3.14.0a6+-a936af9/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json | results/bm-20250317-3.14.0a6+-a936af9-NOGIL/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.16 ms                                                                                                           | 1.71 ms: 2.44x faster                                                                                                   |
| create_gc_cycles           | 1.82 ms                                                                                                           | 1.29 ms: 1.41x faster                                                                                                   |
| async_tree_io_tg           | 636 ms                                                                                                            | 562 ms: 1.13x faster                                                                                                    |
| async_tree_none_tg         | 265 ms                                                                                                            | 240 ms: 1.10x faster                                                                                                    |
| async_tree_io              | 636 ms                                                                                                            | 587 ms: 1.08x faster                                                                                                    |
| sqlite_synth               | 2.21 us                                                                                                           | 2.06 us: 1.07x faster                                                                                                   |
| xml_etree_iterparse        | 93.0 ms                                                                                                           | 88.8 ms: 1.05x faster                                                                                                   |
| regex_effbot               | 2.76 ms                                                                                                           | 2.67 ms: 1.03x faster                                                                                                   |
| regex_v8                   | 24.6 ms                                                                                                           | 24.1 ms: 1.02x faster                                                                                                   |
| async_tree_memoization_tg  | 314 ms                                                                                                            | 309 ms: 1.02x faster                                                                                                    |
| xml_etree_parse            | 129 ms                                                                                                            | 130 ms: 1.00x slower                                                                                                    |
| async_tree_none            | 276 ms                                                                                                            | 280 ms: 1.02x slower                                                                                                    |
| regex_dna                  | 171 ms                                                                                                            | 176 ms: 1.02x slower                                                                                                    |
| coroutines                 | 23.2 ms                                                                                                           | 23.9 ms: 1.03x slower                                                                                                   |
| async_tree_memoization     | 332 ms                                                                                                            | 343 ms: 1.03x slower                                                                                                    |
| float                      | 75.8 ms                                                                                                           | 79.0 ms: 1.04x slower                                                                                                   |
| pycparser                  | 1.15 sec                                                                                                          | 1.21 sec: 1.04x slower                                                                                                  |
| json                       | 4.89 ms                                                                                                           | 5.12 ms: 1.05x slower                                                                                                   |
| pathlib                    | 19.3 ms                                                                                                           | 20.2 ms: 1.05x slower                                                                                                   |
| python_startup             | 14.9 ms                                                                                                           | 15.8 ms: 1.06x slower                                                                                                   |
| generators                 | 29.5 ms                                                                                                           | 31.6 ms: 1.07x slower                                                                                                   |
| json_loads                 | 27.5 us                                                                                                           | 29.5 us: 1.07x slower                                                                                                   |
| docutils                   | 2.62 sec                                                                                                          | 2.81 sec: 1.07x slower                                                                                                  |
| bench_mp_pool              | 88.3 ms                                                                                                           | 95.8 ms: 1.09x slower                                                                                                   |
| sphinx                     | 1.01 sec                                                                                                          | 1.10 sec: 1.09x slower                                                                                                  |
| dulwich_log                | 67.8 ms                                                                                                           | 74.8 ms: 1.10x slower                                                                                                   |
| bpe_tokeniser              | 4.40 sec                                                                                                          | 4.90 sec: 1.11x slower                                                                                                  |
| k_core                     | 2.07 sec                                                                                                          | 2.31 sec: 1.11x slower                                                                                                  |
| pylint                     | 285 ms                                                                                                            | 318 ms: 1.12x slower                                                                                                    |
| pickle_pure_python         | 326 us                                                                                                            | 364 us: 1.12x slower                                                                                                    |
| telco                      | 7.80 ms                                                                                                           | 8.74 ms: 1.12x slower                                                                                                   |
| subparsers                 | 22.9 ms                                                                                                           | 25.7 ms: 1.12x slower                                                                                                   |
| async_generators           | 339 ms                                                                                                            | 380 ms: 1.12x slower                                                                                                    |
| pidigits                   | 195 ms                                                                                                            | 221 ms: 1.13x slower                                                                                                    |
| json_dumps                 | 11.3 ms                                                                                                           | 12.9 ms: 1.14x slower                                                                                                   |
| many_optionals             | 1.04 ms                                                                                                           | 1.19 ms: 1.15x slower                                                                                                   |
| xml_etree_generate         | 85.3 ms                                                                                                           | 97.8 ms: 1.15x slower                                                                                                   |
| logging_silent             | 101 ns                                                                                                            | 116 ns: 1.15x slower                                                                                                    |
| unpickle_pure_python       | 225 us                                                                                                            | 259 us: 1.15x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 499 ms                                                                                                            | 576 ms: 1.15x slower                                                                                                    |
| mdp                        | 2.36 sec                                                                                                          | 2.72 sec: 1.15x slower                                                                                                  |
| sqlglot_optimize           | 53.2 ms                                                                                                           | 61.9 ms: 1.16x slower                                                                                                   |
| 2to3                       | 258 ms                                                                                                            | 301 ms: 1.17x slower                                                                                                    |
| sqlglot_normalize          | 105 ms                                                                                                            | 123 ms: 1.17x slower                                                                                                    |
| scimark_sor                | 117 ms                                                                                                            | 137 ms: 1.17x slower                                                                                                    |
| spectral_norm              | 97.1 ms                                                                                                           | 114 ms: 1.18x slower                                                                                                    |
| deepcopy_reduce            | 2.71 us                                                                                                           | 3.19 us: 1.18x slower                                                                                                   |
| tomli_loads                | 2.01 sec                                                                                                          | 2.36 sec: 1.18x slower                                                                                                  |
| sympy_expand               | 472 ms                                                                                                            | 556 ms: 1.18x slower                                                                                                    |
| deepcopy                   | 265 us                                                                                                            | 313 us: 1.18x slower                                                                                                    |
| logging_simple             | 6.13 us                                                                                                           | 7.25 us: 1.18x slower                                                                                                   |
| thrift                     | 755 us                                                                                                            | 896 us: 1.19x slower                                                                                                    |
| xml_etree_process          | 59.8 ms                                                                                                           | 70.9 ms: 1.19x slower                                                                                                   |
| genshi_xml                 | 51.8 ms                                                                                                           | 61.5 ms: 1.19x slower                                                                                                   |
| nqueens                    | 82.6 ms                                                                                                           | 98.1 ms: 1.19x slower                                                                                                   |
| pprint_safe_repr           | 737 ms                                                                                                            | 876 ms: 1.19x slower                                                                                                    |
| scimark_fft                | 336 ms                                                                                                            | 400 ms: 1.19x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 512 ms                                                                                                            | 610 ms: 1.19x slower                                                                                                    |
| chaos                      | 58.9 ms                                                                                                           | 70.2 ms: 1.19x slower                                                                                                   |
| pyflate                    | 428 ms                                                                                                            | 513 ms: 1.20x slower                                                                                                    |
| sympy_sum                  | 157 ms                                                                                                            | 188 ms: 1.20x slower                                                                                                    |
| sqlglot_transpile          | 1.62 ms                                                                                                           | 1.94 ms: 1.20x slower                                                                                                   |
| raytrace                   | 273 ms                                                                                                            | 328 ms: 1.20x slower                                                                                                    |
| sqlalchemy_imperative      | 19.8 ms                                                                                                           | 23.9 ms: 1.20x slower                                                                                                   |
| pprint_pformat             | 1.51 sec                                                                                                          | 1.82 sec: 1.20x slower                                                                                                  |
| logging_format             | 6.77 us                                                                                                           | 8.19 us: 1.21x slower                                                                                                   |
| django_template            | 36.5 ms                                                                                                           | 44.1 ms: 1.21x slower                                                                                                   |
| coverage                   | 80.4 ms                                                                                                           | 97.3 ms: 1.21x slower                                                                                                   |
| sqlalchemy_declarative     | 131 ms                                                                                                            | 159 ms: 1.21x slower                                                                                                    |
| scimark_lu                 | 117 ms                                                                                                            | 142 ms: 1.21x slower                                                                                                    |
| comprehensions             | 17.3 us                                                                                                           | 21.1 us: 1.22x slower                                                                                                   |
| sympy_str                  | 280 ms                                                                                                            | 341 ms: 1.22x slower                                                                                                    |
| sympy_integrate            | 20.0 ms                                                                                                           | 24.5 ms: 1.22x slower                                                                                                   |
| fannkuch                   | 408 ms                                                                                                            | 500 ms: 1.22x slower                                                                                                    |
| crypto_pyaes               | 72.7 ms                                                                                                           | 89.1 ms: 1.23x slower                                                                                                   |
| sqlglot_parse              | 1.31 ms                                                                                                           | 1.61 ms: 1.23x slower                                                                                                   |
| deltablue                  | 3.16 ms                                                                                                           | 3.89 ms: 1.23x slower                                                                                                   |
| go                         | 117 ms                                                                                                            | 145 ms: 1.24x slower                                                                                                    |
| regex_compile              | 130 ms                                                                                                            | 160 ms: 1.24x slower                                                                                                    |
| connected_components       | 400 ms                                                                                                            | 497 ms: 1.24x slower                                                                                                    |
| shortest_path              | 440 ms                                                                                                            | 548 ms: 1.24x slower                                                                                                    |
| hexiom                     | 6.14 ms                                                                                                           | 7.70 ms: 1.25x slower                                                                                                   |
| typing_runtime_protocols   | 158 us                                                                                                            | 198 us: 1.25x slower                                                                                                    |
| scimark_monte_carlo        | 67.3 ms                                                                                                           | 85.5 ms: 1.27x slower                                                                                                   |
| richards                   | 44.3 ms                                                                                                           | 56.3 ms: 1.27x slower                                                                                                   |
| richards_super             | 51.0 ms                                                                                                           | 65.1 ms: 1.27x slower                                                                                                   |
| python_startup_no_site     | 8.61 ms                                                                                                           | 11.1 ms: 1.29x slower                                                                                                   |
| scimark_sparse_mat_mult    | 4.55 ms                                                                                                           | 5.88 ms: 1.29x slower                                                                                                   |
| nbody                      | 104 ms                                                                                                            | 134 ms: 1.29x slower                                                                                                    |
| deepcopy_memo              | 30.7 us                                                                                                           | 39.8 us: 1.30x slower                                                                                                   |
| meteor_contest             | 102 ms                                                                                                            | 134 ms: 1.31x slower                                                                                                    |
| genshi_text                | 22.2 ms                                                                                                           | 29.1 ms: 1.31x slower                                                                                                   |
| mako                       | 12.1 ms                                                                                                           | 16.0 ms: 1.31x slower                                                                                                   |
| bench_thread_pool          | 1.05 ms                                                                                                           | 3.17 ms: 3.02x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.14x slower                                                                                                            |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (1) of results/bm-20250317-3.14.0a6+-a936af9-NOGIL/bm-20250317-vultr-x86_64-python-a936af924efc6e2fb59e-3.14.0a6+-a936af9.json: html5lib

- Geometric mean (including insignificant results): 1.113x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.20x