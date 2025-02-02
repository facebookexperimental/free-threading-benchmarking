# Results vs. base

- fork: python
- ref: cf4c4ecc26c7e3b89f2e
- machine: linux-x86_64
- commit hash: cf4c4ec
- commit date: 2025-02-01
- overall geometric mean: 1.117x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250201-3.14.0a4+-cf4c4ec/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json | results/bm-20250201-3.14.0a4+-cf4c4ec-NOGIL/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 252 ms                                                                                                            | 295 ms: 1.17x slower                                                                                                    |
| docutils       | 2.52 sec                                                                                                          | 2.75 sec: 1.09x slower                                                                                                  |
| sphinx         | 964 ms                                                                                                            | 1.09 sec: 1.13x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.13x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250201-3.14.0a4+-cf4c4ec/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json | results/bm-20250201-3.14.0a4+-cf4c4ec-NOGIL/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 628 ms                                                                                                            | 561 ms: 1.12x faster                                                                                                    |
| async_tree_none_tg         | 261 ms                                                                                                            | 244 ms: 1.07x faster                                                                                                    |
| async_tree_io              | 620 ms                                                                                                            | 592 ms: 1.05x faster                                                                                                    |
| async_tree_memoization_tg  | 314 ms                                                                                                            | 311 ms: 1.01x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 483 ms                                                                                                            | 496 ms: 1.03x slower                                                                                                    |
| coroutines                 | 21.5 ms                                                                                                           | 22.6 ms: 1.05x slower                                                                                                   |
| async_tree_none            | 269 ms                                                                                                            | 283 ms: 1.05x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 500 ms                                                                                                            | 531 ms: 1.06x slower                                                                                                    |
| async_tree_memoization     | 323 ms                                                                                                            | 348 ms: 1.07x slower                                                                                                    |
| async_generators           | 324 ms                                                                                                            | 371 ms: 1.15x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.01x slower                                                                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250201-3.14.0a4+-cf4c4ec/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json | results/bm-20250201-3.14.0a4+-cf4c4ec-NOGIL/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 197 ms                                                                                                            | 195 ms: 1.01x faster                                                                                                    |
| float          | 71.4 ms                                                                                                           | 74.5 ms: 1.04x slower                                                                                                   |
| nbody          | 88.6 ms                                                                                                           | 125 ms: 1.41x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.13x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250201-3.14.0a4+-cf4c4ec/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json | results/bm-20250201-3.14.0a4+-cf4c4ec-NOGIL/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.8 ms                                                                                                           | 23.7 ms: 1.04x slower                                                                                                   |
| regex_effbot   | 2.57 ms                                                                                                           | 2.76 ms: 1.07x slower                                                                                                   |
| regex_dna      | 170 ms                                                                                                            | 185 ms: 1.09x slower                                                                                                    |
| regex_compile  | 125 ms                                                                                                            | 145 ms: 1.16x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250201-3.14.0a4+-cf4c4ec/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json | results/bm-20250201-3.14.0a4+-cf4c4ec-NOGIL/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 91.7 ms                                                                                                           | 86.3 ms: 1.06x faster                                                                                                   |
| xml_etree_parse      | 129 ms                                                                                                            | 128 ms: 1.01x faster                                                                                                    |
| json_loads           | 28.5 us                                                                                                           | 31.1 us: 1.09x slower                                                                                                   |
| json_dumps           | 11.3 ms                                                                                                           | 12.7 ms: 1.12x slower                                                                                                   |
| unpickle_pure_python | 210 us                                                                                                            | 238 us: 1.13x slower                                                                                                    |
| xml_etree_generate   | 82.6 ms                                                                                                           | 94.2 ms: 1.14x slower                                                                                                   |
| pickle_pure_python   | 307 us                                                                                                            | 357 us: 1.16x slower                                                                                                    |
| xml_etree_process    | 57.5 ms                                                                                                           | 67.1 ms: 1.17x slower                                                                                                   |
| tomli_loads          | 1.87 sec                                                                                                          | 2.26 sec: 1.21x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                             | 1.10x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250201-3.14.0a4+-cf4c4ec/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json | results/bm-20250201-3.14.0a4+-cf4c4ec-NOGIL/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                                                           | 15.3 ms: 1.04x slower                                                                                                   |
| python_startup_no_site | 7.44 ms                                                                                                           | 9.61 ms: 1.29x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250201-3.14.0a4+-cf4c4ec/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json | results/bm-20250201-3.14.0a4+-cf4c4ec-NOGIL/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 47.9 ms                                                                                                           | 57.6 ms: 1.20x slower                                                                                                   |
| django_template | 33.9 ms                                                                                                           | 40.9 ms: 1.21x slower                                                                                                   |
| genshi_text     | 20.8 ms                                                                                                           | 27.1 ms: 1.31x slower                                                                                                   |
| mako            | 11.8 ms                                                                                                           | 15.6 ms: 1.32x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.26x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250201-3.14.0a4+-cf4c4ec/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json | results/bm-20250201-3.14.0a4+-cf4c4ec-NOGIL/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.44 ms                                                                                                           | 1.73 ms: 2.56x faster                                                                                                   |
| create_gc_cycles           | 1.86 ms                                                                                                           | 1.37 ms: 1.36x faster                                                                                                   |
| async_tree_io_tg           | 628 ms                                                                                                            | 561 ms: 1.12x faster                                                                                                    |
| async_tree_none_tg         | 261 ms                                                                                                            | 244 ms: 1.07x faster                                                                                                    |
| sqlite_synth               | 2.19 us                                                                                                           | 2.06 us: 1.07x faster                                                                                                   |
| xml_etree_iterparse        | 91.7 ms                                                                                                           | 86.3 ms: 1.06x faster                                                                                                   |
| async_tree_io              | 620 ms                                                                                                            | 592 ms: 1.05x faster                                                                                                    |
| xml_etree_parse            | 129 ms                                                                                                            | 128 ms: 1.01x faster                                                                                                    |
| pathlib                    | 18.5 ms                                                                                                           | 18.2 ms: 1.01x faster                                                                                                   |
| async_tree_memoization_tg  | 314 ms                                                                                                            | 311 ms: 1.01x faster                                                                                                    |
| pidigits                   | 197 ms                                                                                                            | 195 ms: 1.01x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 483 ms                                                                                                            | 496 ms: 1.03x slower                                                                                                    |
| bench_mp_pool              | 87.7 ms                                                                                                           | 90.4 ms: 1.03x slower                                                                                                   |
| regex_v8                   | 22.8 ms                                                                                                           | 23.7 ms: 1.04x slower                                                                                                   |
| pycparser                  | 1.11 sec                                                                                                          | 1.15 sec: 1.04x slower                                                                                                  |
| float                      | 71.4 ms                                                                                                           | 74.5 ms: 1.04x slower                                                                                                   |
| python_startup             | 14.6 ms                                                                                                           | 15.3 ms: 1.04x slower                                                                                                   |
| mdp                        | 2.43 sec                                                                                                          | 2.54 sec: 1.04x slower                                                                                                  |
| json                       | 5.10 ms                                                                                                           | 5.34 ms: 1.05x slower                                                                                                   |
| coroutines                 | 21.5 ms                                                                                                           | 22.6 ms: 1.05x slower                                                                                                   |
| async_tree_none            | 269 ms                                                                                                            | 283 ms: 1.05x slower                                                                                                    |
| logging_silent             | 101 ns                                                                                                            | 107 ns: 1.06x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 500 ms                                                                                                            | 531 ms: 1.06x slower                                                                                                    |
| dulwich_log                | 75.2 ms                                                                                                           | 80.8 ms: 1.07x slower                                                                                                   |
| async_tree_memoization     | 323 ms                                                                                                            | 348 ms: 1.07x slower                                                                                                    |
| regex_effbot               | 2.57 ms                                                                                                           | 2.76 ms: 1.07x slower                                                                                                   |
| generators                 | 28.2 ms                                                                                                           | 30.4 ms: 1.08x slower                                                                                                   |
| regex_dna                  | 170 ms                                                                                                            | 185 ms: 1.09x slower                                                                                                    |
| docutils                   | 2.52 sec                                                                                                          | 2.75 sec: 1.09x slower                                                                                                  |
| json_loads                 | 28.5 us                                                                                                           | 31.1 us: 1.09x slower                                                                                                   |
| bpe_tokeniser              | 4.14 sec                                                                                                          | 4.57 sec: 1.10x slower                                                                                                  |
| json_dumps                 | 11.3 ms                                                                                                           | 12.7 ms: 1.12x slower                                                                                                   |
| pylint                     | 275 ms                                                                                                            | 308 ms: 1.12x slower                                                                                                    |
| sphinx                     | 964 ms                                                                                                            | 1.09 sec: 1.13x slower                                                                                                  |
| pprint_safe_repr           | 689 ms                                                                                                            | 779 ms: 1.13x slower                                                                                                    |
| unpickle_pure_python       | 210 us                                                                                                            | 238 us: 1.13x slower                                                                                                    |
| many_optionals             | 1.01 ms                                                                                                           | 1.15 ms: 1.13x slower                                                                                                   |
| sqlglot_normalize          | 103 ms                                                                                                            | 117 ms: 1.14x slower                                                                                                    |
| k_core                     | 2.03 sec                                                                                                          | 2.30 sec: 1.14x slower                                                                                                  |
| scimark_sor                | 113 ms                                                                                                            | 128 ms: 1.14x slower                                                                                                    |
| xml_etree_generate         | 82.6 ms                                                                                                           | 94.2 ms: 1.14x slower                                                                                                   |
| async_generators           | 324 ms                                                                                                            | 371 ms: 1.15x slower                                                                                                    |
| spectral_norm              | 90.2 ms                                                                                                           | 104 ms: 1.15x slower                                                                                                    |
| pprint_pformat             | 1.40 sec                                                                                                          | 1.61 sec: 1.15x slower                                                                                                  |
| regex_compile              | 125 ms                                                                                                            | 145 ms: 1.16x slower                                                                                                    |
| go                         | 112 ms                                                                                                            | 130 ms: 1.16x slower                                                                                                    |
| pickle_pure_python         | 307 us                                                                                                            | 357 us: 1.16x slower                                                                                                    |
| subparsers                 | 21.9 ms                                                                                                           | 25.4 ms: 1.16x slower                                                                                                   |
| sqlglot_optimize           | 50.9 ms                                                                                                           | 59.4 ms: 1.17x slower                                                                                                   |
| telco                      | 7.25 ms                                                                                                           | 8.46 ms: 1.17x slower                                                                                                   |
| xml_etree_process          | 57.5 ms                                                                                                           | 67.1 ms: 1.17x slower                                                                                                   |
| 2to3                       | 252 ms                                                                                                            | 295 ms: 1.17x slower                                                                                                    |
| comprehensions             | 16.1 us                                                                                                           | 19.1 us: 1.19x slower                                                                                                   |
| deepcopy                   | 251 us                                                                                                            | 299 us: 1.19x slower                                                                                                    |
| sympy_expand               | 452 ms                                                                                                            | 539 ms: 1.19x slower                                                                                                    |
| sympy_sum                  | 152 ms                                                                                                            | 182 ms: 1.19x slower                                                                                                    |
| pyflate                    | 404 ms                                                                                                            | 483 ms: 1.20x slower                                                                                                    |
| raytrace                   | 261 ms                                                                                                            | 313 ms: 1.20x slower                                                                                                    |
| deepcopy_reduce            | 2.59 us                                                                                                           | 3.11 us: 1.20x slower                                                                                                   |
| genshi_xml                 | 47.9 ms                                                                                                           | 57.6 ms: 1.20x slower                                                                                                   |
| logging_format             | 6.64 us                                                                                                           | 8.00 us: 1.21x slower                                                                                                   |
| sqlglot_transpile          | 1.54 ms                                                                                                           | 1.85 ms: 1.21x slower                                                                                                   |
| django_template            | 33.9 ms                                                                                                           | 40.9 ms: 1.21x slower                                                                                                   |
| sympy_integrate            | 19.5 ms                                                                                                           | 23.5 ms: 1.21x slower                                                                                                   |
| tomli_loads                | 1.87 sec                                                                                                          | 2.26 sec: 1.21x slower                                                                                                  |
| nqueens                    | 77.5 ms                                                                                                           | 93.8 ms: 1.21x slower                                                                                                   |
| chaos                      | 55.2 ms                                                                                                           | 67.0 ms: 1.21x slower                                                                                                   |
| sqlalchemy_declarative     | 126 ms                                                                                                            | 153 ms: 1.22x slower                                                                                                    |
| logging_simple             | 5.89 us                                                                                                           | 7.18 us: 1.22x slower                                                                                                   |
| sympy_str                  | 269 ms                                                                                                            | 329 ms: 1.22x slower                                                                                                    |
| scimark_lu                 | 107 ms                                                                                                            | 131 ms: 1.22x slower                                                                                                    |
| coverage                   | 78.7 ms                                                                                                           | 96.5 ms: 1.23x slower                                                                                                   |
| thrift                     | 731 us                                                                                                            | 896 us: 1.23x slower                                                                                                    |
| sqlalchemy_imperative      | 19.2 ms                                                                                                           | 23.7 ms: 1.24x slower                                                                                                   |
| sqlglot_parse              | 1.24 ms                                                                                                           | 1.54 ms: 1.24x slower                                                                                                   |
| scimark_fft                | 304 ms                                                                                                            | 376 ms: 1.24x slower                                                                                                    |
| hexiom                     | 5.69 ms                                                                                                           | 7.08 ms: 1.24x slower                                                                                                   |
| deepcopy_memo              | 29.7 us                                                                                                           | 37.0 us: 1.25x slower                                                                                                   |
| connected_components       | 390 ms                                                                                                            | 488 ms: 1.25x slower                                                                                                    |
| shortest_path              | 430 ms                                                                                                            | 540 ms: 1.26x slower                                                                                                    |
| python_startup_no_site     | 7.44 ms                                                                                                           | 9.61 ms: 1.29x slower                                                                                                   |
| scimark_monte_carlo        | 61.4 ms                                                                                                           | 79.9 ms: 1.30x slower                                                                                                   |
| typing_runtime_protocols   | 150 us                                                                                                            | 196 us: 1.30x slower                                                                                                    |
| genshi_text                | 20.8 ms                                                                                                           | 27.1 ms: 1.31x slower                                                                                                   |
| richards                   | 41.1 ms                                                                                                           | 54.0 ms: 1.31x slower                                                                                                   |
| fannkuch                   | 366 ms                                                                                                            | 482 ms: 1.32x slower                                                                                                    |
| mako                       | 11.8 ms                                                                                                           | 15.6 ms: 1.32x slower                                                                                                   |
| richards_super             | 47.1 ms                                                                                                           | 62.5 ms: 1.33x slower                                                                                                   |
| meteor_contest             | 96.9 ms                                                                                                           | 129 ms: 1.33x slower                                                                                                    |
| scimark_sparse_mat_mult    | 4.12 ms                                                                                                           | 5.49 ms: 1.33x slower                                                                                                   |
| crypto_pyaes               | 64.9 ms                                                                                                           | 87.1 ms: 1.34x slower                                                                                                   |
| nbody                      | 88.6 ms                                                                                                           | 125 ms: 1.41x slower                                                                                                    |
| deltablue                  | 3.04 ms                                                                                                           | 4.43 ms: 1.46x slower                                                                                                   |
| bench_thread_pool          | 1.02 ms                                                                                                           | 3.30 ms: 3.23x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.14x slower                                                                                                            |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (8) of results/bm-20250201-3.14.0a4+-cf4c4ec/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (1) of results/bm-20250201-3.14.0a4+-cf4c4ec-NOGIL/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json: html5lib

- Geometric mean (including insignificant results): 1.117x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.20x