# Results vs. base

- fork: python
- ref: 0ac40acec045c4ce780c
- machine: linux-x86_64
- commit hash: 0ac40ac
- commit date: 2024-12-14
- overall geometric mean: 1.246x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.23x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20241214-3.14.0a2+-0ac40ac/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json | results/bm-20241214-3.14.0a2+-0ac40ac-NOGIL/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 418 ms                                                                                                            | 577 ms: 1.38x slower                                                                                                    |
| docutils       | 3.55 sec                                                                                                          | 4.38 sec: 1.23x slower                                                                                                  |
| html5lib       | 82.9 ms                                                                                                           | 120 ms: 1.45x slower                                                                                                    |
| sphinx         | 1.38 sec                                                                                                          | 1.68 sec: 1.22x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.32x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20241214-3.14.0a2+-0ac40ac/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json | results/bm-20241214-3.14.0a2+-0ac40ac-NOGIL/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| asyncio_websockets         | 766 ms                                                                                                            | 735 ms: 1.04x faster                                                                                                    |
| coroutines                 | 31.8 ms                                                                                                           | 35.3 ms: 1.11x slower                                                                                                   |
| async_tree_io_tg           | 888 ms                                                                                                            | 1.01 sec: 1.14x slower                                                                                                  |
| async_tree_cpu_io_mixed_tg | 670 ms                                                                                                            | 772 ms: 1.15x slower                                                                                                    |
| async_generators           | 543 ms                                                                                                            | 659 ms: 1.21x slower                                                                                                    |
| async_tree_none_tg         | 362 ms                                                                                                            | 451 ms: 1.25x slower                                                                                                    |
| async_tree_io              | 862 ms                                                                                                            | 1.08 sec: 1.25x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 677 ms                                                                                                            | 850 ms: 1.26x slower                                                                                                    |
| async_tree_memoization_tg  | 444 ms                                                                                                            | 585 ms: 1.32x slower                                                                                                    |
| async_tree_none            | 383 ms                                                                                                            | 513 ms: 1.34x slower                                                                                                    |
| async_tree_memoization     | 478 ms                                                                                                            | 644 ms: 1.35x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.21x slower                                                                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20241214-3.14.0a2+-0ac40ac/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json | results/bm-20241214-3.14.0a2+-0ac40ac-NOGIL/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| nbody          | 120 ms                                                                                                            | 167 ms: 1.39x slower                                                                                                    |
| float          | 109 ms                                                                                                            | 168 ms: 1.55x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.29x slower                                                                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20241214-3.14.0a2+-0ac40ac/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json | results/bm-20241214-3.14.0a2+-0ac40ac-NOGIL/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 34.8 ms                                                                                                           | 32.7 ms: 1.07x faster                                                                                                   |
| regex_effbot   | 4.29 ms                                                                                                           | 4.51 ms: 1.05x slower                                                                                                   |
| regex_dna      | 269 ms                                                                                                            | 290 ms: 1.08x slower                                                                                                    |
| regex_compile  | 163 ms                                                                                                            | 235 ms: 1.44x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.11x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20241214-3.14.0a2+-0ac40ac/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json | results/bm-20241214-3.14.0a2+-0ac40ac-NOGIL/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 147 ms                                                                                                            | 137 ms: 1.07x faster                                                                                                    |
| json_loads           | 33.9 us                                                                                                           | 35.7 us: 1.05x slower                                                                                                   |
| xml_etree_parse      | 189 ms                                                                                                            | 204 ms: 1.08x slower                                                                                                    |
| json_dumps           | 15.4 ms                                                                                                           | 17.3 ms: 1.12x slower                                                                                                   |
| xml_etree_generate   | 115 ms                                                                                                            | 135 ms: 1.17x slower                                                                                                    |
| xml_etree_process    | 80.0 ms                                                                                                           | 104 ms: 1.30x slower                                                                                                    |
| tomli_loads          | 2.56 sec                                                                                                          | 3.36 sec: 1.31x slower                                                                                                  |
| unpickle_pure_python | 291 us                                                                                                            | 411 us: 1.41x slower                                                                                                    |
| pickle_pure_python   | 403 us                                                                                                            | 615 us: 1.53x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.20x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20241214-3.14.0a2+-0ac40ac/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json | results/bm-20241214-3.14.0a2+-0ac40ac-NOGIL/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 24.4 ms                                                                                                           | 31.5 ms: 1.29x slower                                                                                                   |
| python_startup_no_site | 14.3 ms                                                                                                           | 19.4 ms: 1.35x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.32x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20241214-3.14.0a2+-0ac40ac/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json | results/bm-20241214-3.14.0a2+-0ac40ac-NOGIL/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 66.3 ms                                                                                                           | 89.0 ms: 1.34x slower                                                                                                   |
| django_template | 45.2 ms                                                                                                           | 61.0 ms: 1.35x slower                                                                                                   |
| genshi_text     | 29.6 ms                                                                                                           | 41.0 ms: 1.38x slower                                                                                                   |
| mako            | 15.8 ms                                                                                                           | 26.3 ms: 1.66x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.43x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20241214-3.14.0a2+-0ac40ac/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json | results/bm-20241214-3.14.0a2+-0ac40ac-NOGIL/bm-20241214-linux-x86_64-python-0ac40acec045c4ce780c-3.14.0a2+-0ac40ac.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 7.90 ms                                                                                                           | 6.80 ms: 1.16x faster                                                                                                   |
| xml_etree_iterparse        | 147 ms                                                                                                            | 137 ms: 1.07x faster                                                                                                    |
| regex_v8                   | 34.8 ms                                                                                                           | 32.7 ms: 1.07x faster                                                                                                   |
| asyncio_websockets         | 766 ms                                                                                                            | 735 ms: 1.04x faster                                                                                                    |
| json_loads                 | 33.9 us                                                                                                           | 35.7 us: 1.05x slower                                                                                                   |
| regex_effbot               | 4.29 ms                                                                                                           | 4.51 ms: 1.05x slower                                                                                                   |
| json                       | 6.40 ms                                                                                                           | 6.83 ms: 1.07x slower                                                                                                   |
| regex_dna                  | 269 ms                                                                                                            | 290 ms: 1.08x slower                                                                                                    |
| xml_etree_parse            | 189 ms                                                                                                            | 204 ms: 1.08x slower                                                                                                    |
| k_core                     | 4.01 sec                                                                                                          | 4.37 sec: 1.09x slower                                                                                                  |
| coroutines                 | 31.8 ms                                                                                                           | 35.3 ms: 1.11x slower                                                                                                   |
| json_dumps                 | 15.4 ms                                                                                                           | 17.3 ms: 1.12x slower                                                                                                   |
| deepcopy_reduce            | 3.82 us                                                                                                           | 4.30 us: 1.13x slower                                                                                                   |
| shortest_path              | 887 ms                                                                                                            | 1.01 sec: 1.14x slower                                                                                                  |
| async_tree_io_tg           | 888 ms                                                                                                            | 1.01 sec: 1.14x slower                                                                                                  |
| connected_components       | 804 ms                                                                                                            | 920 ms: 1.14x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 670 ms                                                                                                            | 772 ms: 1.15x slower                                                                                                    |
| mdp                        | 3.77 sec                                                                                                          | 4.41 sec: 1.17x slower                                                                                                  |
| xml_etree_generate         | 115 ms                                                                                                            | 135 ms: 1.17x slower                                                                                                    |
| deepcopy_memo              | 42.7 us                                                                                                           | 50.2 us: 1.18x slower                                                                                                   |
| typing_runtime_protocols   | 231 us                                                                                                            | 274 us: 1.19x slower                                                                                                    |
| spectral_norm              | 134 ms                                                                                                            | 161 ms: 1.20x slower                                                                                                    |
| coverage                   | 117 ms                                                                                                            | 141 ms: 1.20x slower                                                                                                    |
| scimark_fft                | 454 ms                                                                                                            | 550 ms: 1.21x slower                                                                                                    |
| async_generators           | 543 ms                                                                                                            | 659 ms: 1.21x slower                                                                                                    |
| telco                      | 10.0 ms                                                                                                           | 12.2 ms: 1.21x slower                                                                                                   |
| deepcopy                   | 336 us                                                                                                            | 408 us: 1.21x slower                                                                                                    |
| sphinx                     | 1.38 sec                                                                                                          | 1.68 sec: 1.22x slower                                                                                                  |
| dulwich_log                | 96.0 ms                                                                                                           | 117 ms: 1.22x slower                                                                                                    |
| nqueens                    | 106 ms                                                                                                            | 130 ms: 1.23x slower                                                                                                    |
| pathlib                    | 25.7 ms                                                                                                           | 31.7 ms: 1.23x slower                                                                                                   |
| docutils                   | 3.55 sec                                                                                                          | 4.38 sec: 1.23x slower                                                                                                  |
| many_optionals             | 1.12 ms                                                                                                           | 1.39 ms: 1.24x slower                                                                                                   |
| sqlglot_normalize          | 136 ms                                                                                                            | 169 ms: 1.24x slower                                                                                                    |
| async_tree_none_tg         | 362 ms                                                                                                            | 451 ms: 1.25x slower                                                                                                    |
| async_tree_io              | 862 ms                                                                                                            | 1.08 sec: 1.25x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 677 ms                                                                                                            | 850 ms: 1.26x slower                                                                                                    |
| pylint                     | 398 ms                                                                                                            | 501 ms: 1.26x slower                                                                                                    |
| bpe_tokeniser              | 5.85 sec                                                                                                          | 7.46 sec: 1.28x slower                                                                                                  |
| meteor_contest             | 135 ms                                                                                                            | 173 ms: 1.28x slower                                                                                                    |
| python_startup             | 24.4 ms                                                                                                           | 31.5 ms: 1.29x slower                                                                                                   |
| fannkuch                   | 507 ms                                                                                                            | 653 ms: 1.29x slower                                                                                                    |
| pycparser                  | 1.48 sec                                                                                                          | 1.93 sec: 1.30x slower                                                                                                  |
| xml_etree_process          | 80.0 ms                                                                                                           | 104 ms: 1.30x slower                                                                                                    |
| bench_thread_pool          | 2.89 ms                                                                                                           | 3.76 ms: 1.30x slower                                                                                                   |
| sqlglot_optimize           | 69.7 ms                                                                                                           | 90.9 ms: 1.30x slower                                                                                                   |
| tomli_loads                | 2.56 sec                                                                                                          | 3.36 sec: 1.31x slower                                                                                                  |
| async_tree_memoization_tg  | 444 ms                                                                                                            | 585 ms: 1.32x slower                                                                                                    |
| crypto_pyaes               | 92.5 ms                                                                                                           | 123 ms: 1.33x slower                                                                                                    |
| async_tree_none            | 383 ms                                                                                                            | 513 ms: 1.34x slower                                                                                                    |
| thrift                     | 1.07 ms                                                                                                           | 1.43 ms: 1.34x slower                                                                                                   |
| genshi_xml                 | 66.3 ms                                                                                                           | 89.0 ms: 1.34x slower                                                                                                   |
| async_tree_memoization     | 478 ms                                                                                                            | 644 ms: 1.35x slower                                                                                                    |
| django_template            | 45.2 ms                                                                                                           | 61.0 ms: 1.35x slower                                                                                                   |
| python_startup_no_site     | 14.3 ms                                                                                                           | 19.4 ms: 1.35x slower                                                                                                   |
| generators                 | 38.4 ms                                                                                                           | 52.5 ms: 1.37x slower                                                                                                   |
| subparsers                 | 29.8 ms                                                                                                           | 41.2 ms: 1.38x slower                                                                                                   |
| 2to3                       | 418 ms                                                                                                            | 577 ms: 1.38x slower                                                                                                    |
| genshi_text                | 29.6 ms                                                                                                           | 41.0 ms: 1.38x slower                                                                                                   |
| pprint_safe_repr           | 935 ms                                                                                                            | 1.30 sec: 1.39x slower                                                                                                  |
| nbody                      | 120 ms                                                                                                            | 167 ms: 1.39x slower                                                                                                    |
| scimark_sparse_mat_mult    | 5.79 ms                                                                                                           | 8.07 ms: 1.39x slower                                                                                                   |
| sympy_integrate            | 28.0 ms                                                                                                           | 39.4 ms: 1.41x slower                                                                                                   |
| unpickle_pure_python       | 291 us                                                                                                            | 411 us: 1.41x slower                                                                                                    |
| pprint_pformat             | 1.89 sec                                                                                                          | 2.71 sec: 1.43x slower                                                                                                  |
| regex_compile              | 163 ms                                                                                                            | 235 ms: 1.44x slower                                                                                                    |
| html5lib                   | 82.9 ms                                                                                                           | 120 ms: 1.45x slower                                                                                                    |
| pyflate                    | 633 ms                                                                                                            | 939 ms: 1.48x slower                                                                                                    |
| logging_simple             | 8.08 us                                                                                                           | 12.1 us: 1.50x slower                                                                                                   |
| chaos                      | 80.6 ms                                                                                                           | 123 ms: 1.52x slower                                                                                                    |
| pickle_pure_python         | 403 us                                                                                                            | 615 us: 1.53x slower                                                                                                    |
| logging_format             | 8.84 us                                                                                                           | 13.6 us: 1.54x slower                                                                                                   |
| float                      | 109 ms                                                                                                            | 168 ms: 1.55x slower                                                                                                    |
| scimark_lu                 | 149 ms                                                                                                            | 232 ms: 1.56x slower                                                                                                    |
| richards_super             | 67.3 ms                                                                                                           | 106 ms: 1.58x slower                                                                                                    |
| sympy_str                  | 378 ms                                                                                                            | 600 ms: 1.59x slower                                                                                                    |
| logging_silent             | 138 ns                                                                                                            | 220 ns: 1.59x slower                                                                                                    |
| sqlalchemy_imperative      | 22.4 ms                                                                                                           | 36.1 ms: 1.61x slower                                                                                                   |
| hexiom                     | 7.85 ms                                                                                                           | 12.7 ms: 1.62x slower                                                                                                   |
| richards                   | 59.2 ms                                                                                                           | 96.2 ms: 1.62x slower                                                                                                   |
| comprehensions             | 21.3 us                                                                                                           | 34.7 us: 1.63x slower                                                                                                   |
| sqlalchemy_declarative     | 163 ms                                                                                                            | 269 ms: 1.65x slower                                                                                                    |
| mako                       | 15.8 ms                                                                                                           | 26.3 ms: 1.66x slower                                                                                                   |
| scimark_monte_carlo        | 87.8 ms                                                                                                           | 151 ms: 1.73x slower                                                                                                    |
| raytrace                   | 350 ms                                                                                                            | 620 ms: 1.77x slower                                                                                                    |
| sqlglot_parse              | 1.71 ms                                                                                                           | 3.05 ms: 1.78x slower                                                                                                   |
| sqlglot_transpile          | 2.09 ms                                                                                                           | 3.81 ms: 1.82x slower                                                                                                   |
| scimark_sor                | 154 ms                                                                                                            | 291 ms: 1.89x slower                                                                                                    |
| sympy_expand               | 574 ms                                                                                                            | 1.11 sec: 1.94x slower                                                                                                  |
| go                         | 153 ms                                                                                                            | 303 ms: 1.98x slower                                                                                                    |
| sympy_sum                  | 204 ms                                                                                                            | 424 ms: 2.08x slower                                                                                                    |
| deltablue                  | 4.06 ms                                                                                                           | 11.3 ms: 2.78x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.33x slower                                                                                                            |

Benchmark hidden because not significant (4): create_gc_cycles, pidigits, sqlite_synth, bench_mp_pool

- Geometric mean (including insignificant results): 1.246x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.25x
- 95% likely to have a slowdown of 1.25x
- 99% likely to have a slowdown of 1.23x

# Memory
- memory change: 1.18x