# Results vs. base

- fork: python
- ref: 5c89adf385aaaca97c2e
- machine: linux-x86_64
- commit hash: 5c89adf
- commit date: 2024-12-09
- overall geometric mean: 1.247x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20241209-3.14.0a2+-5c89adf/bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json | results/bm-20241209-3.14.0a2+-5c89adf-NOGIL/bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 433 ms                                                                                                            | 616 ms: 1.42x slower                                                                                                    |
| docutils       | 3.57 sec                                                                                                          | 4.37 sec: 1.22x slower                                                                                                  |
| html5lib       | 84.6 ms                                                                                                           | 129 ms: 1.53x slower                                                                                                    |
| sphinx         | 1.37 sec                                                                                                          | 1.69 sec: 1.23x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.35x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20241209-3.14.0a2+-5c89adf/bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json | results/bm-20241209-3.14.0a2+-5c89adf-NOGIL/bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 892 ms                                                                                                            | 1.05 sec: 1.18x slower                                                                                                  |
| coroutines                 | 28.4 ms                                                                                                           | 33.6 ms: 1.18x slower                                                                                                   |
| async_generators           | 541 ms                                                                                                            | 654 ms: 1.21x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 671 ms                                                                                                            | 823 ms: 1.23x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 675 ms                                                                                                            | 842 ms: 1.25x slower                                                                                                    |
| async_tree_memoization_tg  | 482 ms                                                                                                            | 609 ms: 1.26x slower                                                                                                    |
| async_tree_none_tg         | 367 ms                                                                                                            | 464 ms: 1.26x slower                                                                                                    |
| async_tree_io              | 825 ms                                                                                                            | 1.08 sec: 1.31x slower                                                                                                  |
| async_tree_memoization     | 479 ms                                                                                                            | 657 ms: 1.37x slower                                                                                                    |
| async_tree_none            | 380 ms                                                                                                            | 530 ms: 1.40x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.24x slower                                                                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20241209-3.14.0a2+-5c89adf/bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json | results/bm-20241209-3.14.0a2+-5c89adf-NOGIL/bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 237 ms                                                                                                            | 229 ms: 1.04x faster                                                                                                    |
| nbody          | 122 ms                                                                                                            | 176 ms: 1.44x slower                                                                                                    |
| float          | 113 ms                                                                                                            | 169 ms: 1.50x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.28x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20241209-3.14.0a2+-5c89adf/bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json | results/bm-20241209-3.14.0a2+-5c89adf-NOGIL/bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_compile  | 157 ms                                                                                                            | 225 ms: 1.43x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmark hidden because not significant (3): regex_effbot, regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20241209-3.14.0a2+-5c89adf/bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json | results/bm-20241209-3.14.0a2+-5c89adf-NOGIL/bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 205 ms                                                                                                            | 216 ms: 1.05x slower                                                                                                    |
| json_loads           | 34.4 us                                                                                                           | 38.4 us: 1.11x slower                                                                                                   |
| xml_etree_generate   | 117 ms                                                                                                            | 131 ms: 1.12x slower                                                                                                    |
| json_dumps           | 15.3 ms                                                                                                           | 17.8 ms: 1.17x slower                                                                                                   |
| xml_etree_process    | 82.8 ms                                                                                                           | 101 ms: 1.22x slower                                                                                                    |
| tomli_loads          | 2.59 sec                                                                                                          | 3.50 sec: 1.35x slower                                                                                                  |
| unpickle_pure_python | 284 us                                                                                                            | 411 us: 1.45x slower                                                                                                    |
| pickle_pure_python   | 429 us                                                                                                            | 626 us: 1.46x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.21x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20241209-3.14.0a2+-5c89adf/bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json | results/bm-20241209-3.14.0a2+-5c89adf-NOGIL/bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 25.9 ms                                                                                                           | 32.3 ms: 1.25x slower                                                                                                   |
| python_startup_no_site | 15.2 ms                                                                                                           | 19.9 ms: 1.31x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.28x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20241209-3.14.0a2+-5c89adf/bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json | results/bm-20241209-3.14.0a2+-5c89adf-NOGIL/bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| django_template | 46.6 ms                                                                                                           | 63.7 ms: 1.37x slower                                                                                                   |
| genshi_text     | 30.3 ms                                                                                                           | 42.8 ms: 1.41x slower                                                                                                   |
| genshi_xml      | 63.1 ms                                                                                                           | 91.5 ms: 1.45x slower                                                                                                   |
| mako            | 16.9 ms                                                                                                           | 26.9 ms: 1.59x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.45x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20241209-3.14.0a2+-5c89adf/bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json | results/bm-20241209-3.14.0a2+-5c89adf-NOGIL/bm-20241209-linux-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 7.78 ms                                                                                                           | 6.22 ms: 1.25x faster                                                                                                   |
| pidigits                   | 237 ms                                                                                                            | 229 ms: 1.04x faster                                                                                                    |
| xml_etree_parse            | 205 ms                                                                                                            | 216 ms: 1.05x slower                                                                                                    |
| create_gc_cycles           | 3.17 ms                                                                                                           | 3.38 ms: 1.07x slower                                                                                                   |
| telco                      | 10.6 ms                                                                                                           | 11.5 ms: 1.09x slower                                                                                                   |
| k_core                     | 3.98 sec                                                                                                          | 4.43 sec: 1.11x slower                                                                                                  |
| json_loads                 | 34.4 us                                                                                                           | 38.4 us: 1.11x slower                                                                                                   |
| xml_etree_generate         | 117 ms                                                                                                            | 131 ms: 1.12x slower                                                                                                    |
| connected_components       | 809 ms                                                                                                            | 942 ms: 1.16x slower                                                                                                    |
| bench_mp_pool              | 84.3 ms                                                                                                           | 98.3 ms: 1.17x slower                                                                                                   |
| json_dumps                 | 15.3 ms                                                                                                           | 17.8 ms: 1.17x slower                                                                                                   |
| pathlib                    | 27.5 ms                                                                                                           | 32.2 ms: 1.17x slower                                                                                                   |
| shortest_path              | 867 ms                                                                                                            | 1.02 sec: 1.18x slower                                                                                                  |
| async_tree_io_tg           | 892 ms                                                                                                            | 1.05 sec: 1.18x slower                                                                                                  |
| coroutines                 | 28.4 ms                                                                                                           | 33.6 ms: 1.18x slower                                                                                                   |
| dulwich_log                | 98.0 ms                                                                                                           | 118 ms: 1.21x slower                                                                                                    |
| async_generators           | 541 ms                                                                                                            | 654 ms: 1.21x slower                                                                                                    |
| deepcopy                   | 345 us                                                                                                            | 417 us: 1.21x slower                                                                                                    |
| scimark_fft                | 469 ms                                                                                                            | 570 ms: 1.22x slower                                                                                                    |
| docutils                   | 3.57 sec                                                                                                          | 4.37 sec: 1.22x slower                                                                                                  |
| xml_etree_process          | 82.8 ms                                                                                                           | 101 ms: 1.22x slower                                                                                                    |
| async_tree_cpu_io_mixed_tg | 671 ms                                                                                                            | 823 ms: 1.23x slower                                                                                                    |
| sphinx                     | 1.37 sec                                                                                                          | 1.69 sec: 1.23x slower                                                                                                  |
| scimark_sparse_mat_mult    | 6.50 ms                                                                                                           | 8.09 ms: 1.24x slower                                                                                                   |
| coverage                   | 110 ms                                                                                                            | 137 ms: 1.24x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 675 ms                                                                                                            | 842 ms: 1.25x slower                                                                                                    |
| python_startup             | 25.9 ms                                                                                                           | 32.3 ms: 1.25x slower                                                                                                   |
| sqlglot_optimize           | 72.6 ms                                                                                                           | 90.7 ms: 1.25x slower                                                                                                   |
| pycparser                  | 1.53 sec                                                                                                          | 1.92 sec: 1.26x slower                                                                                                  |
| async_tree_memoization_tg  | 482 ms                                                                                                            | 609 ms: 1.26x slower                                                                                                    |
| async_tree_none_tg         | 367 ms                                                                                                            | 464 ms: 1.26x slower                                                                                                    |
| meteor_contest             | 135 ms                                                                                                            | 171 ms: 1.27x slower                                                                                                    |
| spectral_norm              | 139 ms                                                                                                            | 177 ms: 1.27x slower                                                                                                    |
| deepcopy_reduce            | 3.70 us                                                                                                           | 4.73 us: 1.28x slower                                                                                                   |
| generators                 | 40.4 ms                                                                                                           | 51.8 ms: 1.28x slower                                                                                                   |
| nqueens                    | 104 ms                                                                                                            | 134 ms: 1.28x slower                                                                                                    |
| mdp                        | 3.50 sec                                                                                                          | 4.50 sec: 1.29x slower                                                                                                  |
| sqlglot_normalize          | 136 ms                                                                                                            | 177 ms: 1.30x slower                                                                                                    |
| async_tree_io              | 825 ms                                                                                                            | 1.08 sec: 1.31x slower                                                                                                  |
| many_optionals             | 1.11 ms                                                                                                           | 1.46 ms: 1.31x slower                                                                                                   |
| python_startup_no_site     | 15.2 ms                                                                                                           | 19.9 ms: 1.31x slower                                                                                                   |
| deepcopy_memo              | 38.7 us                                                                                                           | 50.9 us: 1.32x slower                                                                                                   |
| subparsers                 | 30.7 ms                                                                                                           | 40.5 ms: 1.32x slower                                                                                                   |
| crypto_pyaes               | 94.6 ms                                                                                                           | 125 ms: 1.32x slower                                                                                                    |
| bpe_tokeniser              | 5.60 sec                                                                                                          | 7.47 sec: 1.34x slower                                                                                                  |
| fannkuch                   | 510 ms                                                                                                            | 682 ms: 1.34x slower                                                                                                    |
| typing_runtime_protocols   | 204 us                                                                                                            | 273 us: 1.34x slower                                                                                                    |
| pylint                     | 392 ms                                                                                                            | 526 ms: 1.34x slower                                                                                                    |
| tomli_loads                | 2.59 sec                                                                                                          | 3.50 sec: 1.35x slower                                                                                                  |
| pyflate                    | 684 ms                                                                                                            | 929 ms: 1.36x slower                                                                                                    |
| richards_super             | 75.4 ms                                                                                                           | 103 ms: 1.36x slower                                                                                                    |
| django_template            | 46.6 ms                                                                                                           | 63.7 ms: 1.37x slower                                                                                                   |
| async_tree_memoization     | 479 ms                                                                                                            | 657 ms: 1.37x slower                                                                                                    |
| pprint_safe_repr           | 928 ms                                                                                                            | 1.29 sec: 1.39x slower                                                                                                  |
| async_tree_none            | 380 ms                                                                                                            | 530 ms: 1.40x slower                                                                                                    |
| pprint_pformat             | 1.89 sec                                                                                                          | 2.67 sec: 1.41x slower                                                                                                  |
| genshi_text                | 30.3 ms                                                                                                           | 42.8 ms: 1.41x slower                                                                                                   |
| richards                   | 63.7 ms                                                                                                           | 90.6 ms: 1.42x slower                                                                                                   |
| 2to3                       | 433 ms                                                                                                            | 616 ms: 1.42x slower                                                                                                    |
| thrift                     | 1.03 ms                                                                                                           | 1.47 ms: 1.43x slower                                                                                                   |
| regex_compile              | 157 ms                                                                                                            | 225 ms: 1.43x slower                                                                                                    |
| scimark_lu                 | 150 ms                                                                                                            | 215 ms: 1.44x slower                                                                                                    |
| nbody                      | 122 ms                                                                                                            | 176 ms: 1.44x slower                                                                                                    |
| unpickle_pure_python       | 284 us                                                                                                            | 411 us: 1.45x slower                                                                                                    |
| genshi_xml                 | 63.1 ms                                                                                                           | 91.5 ms: 1.45x slower                                                                                                   |
| pickle_pure_python         | 429 us                                                                                                            | 626 us: 1.46x slower                                                                                                    |
| comprehensions             | 21.1 us                                                                                                           | 31.0 us: 1.47x slower                                                                                                   |
| sympy_integrate            | 26.1 ms                                                                                                           | 39.0 ms: 1.50x slower                                                                                                   |
| float                      | 113 ms                                                                                                            | 169 ms: 1.50x slower                                                                                                    |
| html5lib                   | 84.6 ms                                                                                                           | 129 ms: 1.53x slower                                                                                                    |
| sqlalchemy_declarative     | 172 ms                                                                                                            | 266 ms: 1.55x slower                                                                                                    |
| mako                       | 16.9 ms                                                                                                           | 26.9 ms: 1.59x slower                                                                                                   |
| bench_thread_pool          | 2.72 ms                                                                                                           | 4.35 ms: 1.60x slower                                                                                                   |
| logging_simple             | 8.09 us                                                                                                           | 13.1 us: 1.62x slower                                                                                                   |
| chaos                      | 80.2 ms                                                                                                           | 130 ms: 1.63x slower                                                                                                    |
| scimark_monte_carlo        | 87.4 ms                                                                                                           | 142 ms: 1.63x slower                                                                                                    |
| sqlalchemy_imperative      | 23.3 ms                                                                                                           | 38.1 ms: 1.64x slower                                                                                                   |
| logging_format             | 8.70 us                                                                                                           | 14.3 us: 1.65x slower                                                                                                   |
| hexiom                     | 8.26 ms                                                                                                           | 13.9 ms: 1.68x slower                                                                                                   |
| sympy_str                  | 349 ms                                                                                                            | 589 ms: 1.69x slower                                                                                                    |
| logging_silent             | 143 ns                                                                                                            | 250 ns: 1.75x slower                                                                                                    |
| scimark_sor                | 167 ms                                                                                                            | 302 ms: 1.81x slower                                                                                                    |
| raytrace                   | 341 ms                                                                                                            | 634 ms: 1.86x slower                                                                                                    |
| sympy_expand               | 573 ms                                                                                                            | 1.10 sec: 1.92x slower                                                                                                  |
| sqlglot_parse              | 1.67 ms                                                                                                           | 3.25 ms: 1.95x slower                                                                                                   |
| sqlglot_transpile          | 2.13 ms                                                                                                           | 4.19 ms: 1.96x slower                                                                                                   |
| go                         | 160 ms                                                                                                            | 322 ms: 2.01x slower                                                                                                    |
| sympy_sum                  | 194 ms                                                                                                            | 413 ms: 2.13x slower                                                                                                    |
| deltablue                  | 4.35 ms                                                                                                           | 10.3 ms: 2.37x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.34x slower                                                                                                            |

Benchmark hidden because not significant (7): regex_effbot, sqlite_synth, regex_dna, regex_v8, asyncio_websockets, json, xml_etree_iterparse

- Geometric mean (including insignificant results): 1.247x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.27x
- 95% likely to have a slowdown of 1.26x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 1.18x