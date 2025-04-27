# Results vs. base

- fork: python
- ref: 8a4d4f37abb9fa639fdc
- machine: linux-x86_64
- commit hash: 8a4d4f3
- commit date: 2025-04-25
- overall geometric mean: 1.083x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250425-3.14.0a7+-8a4d4f3/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3.json | results/bm-20250425-3.14.0a7+-8a4d4f3-NOGIL/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 247 ms                                                                                                            | 280 ms: 1.13x slower                                                                                                    |
| docutils       | 2.53 sec                                                                                                          | 2.70 sec: 1.07x slower                                                                                                  |
| sphinx         | 974 ms                                                                                                            | 1.07 sec: 1.10x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.10x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250425-3.14.0a7+-8a4d4f3/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3.json | results/bm-20250425-3.14.0a7+-8a4d4f3-NOGIL/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 604 ms                                                                                                            | 522 ms: 1.16x faster                                                                                                    |
| async_tree_none_tg         | 252 ms                                                                                                            | 228 ms: 1.11x faster                                                                                                    |
| async_tree_io              | 604 ms                                                                                                            | 549 ms: 1.10x faster                                                                                                    |
| async_tree_memoization_tg  | 311 ms                                                                                                            | 286 ms: 1.09x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 508 ms                                                                                                            | 480 ms: 1.06x faster                                                                                                    |
| coroutines                 | 24.1 ms                                                                                                           | 22.9 ms: 1.05x faster                                                                                                   |
| async_tree_none            | 267 ms                                                                                                            | 259 ms: 1.03x faster                                                                                                    |
| asyncio_websockets         | 517 ms                                                                                                            | 515 ms: 1.00x faster                                                                                                    |
| async_tree_memoization     | 305 ms                                                                                                            | 312 ms: 1.02x slower                                                                                                    |
| async_generators           | 326 ms                                                                                                            | 367 ms: 1.13x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.04x faster                                                                                                            |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250425-3.14.0a7+-8a4d4f3/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3.json | results/bm-20250425-3.14.0a7+-8a4d4f3-NOGIL/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| float          | 69.1 ms                                                                                                           | 67.2 ms: 1.03x faster                                                                                                   |
| pidigits       | 198 ms                                                                                                            | 198 ms: 1.00x faster                                                                                                    |
| nbody          | 87.8 ms                                                                                                           | 110 ms: 1.26x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.07x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250425-3.14.0a7+-8a4d4f3/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3.json | results/bm-20250425-3.14.0a7+-8a4d4f3-NOGIL/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 22.0 ms                                                                                                           | 21.4 ms: 1.03x faster                                                                                                   |
| regex_dna      | 175 ms                                                                                                            | 180 ms: 1.03x slower                                                                                                    |
| regex_effbot   | 2.68 ms                                                                                                           | 2.85 ms: 1.06x slower                                                                                                   |
| regex_compile  | 122 ms                                                                                                            | 143 ms: 1.17x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.06x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250425-3.14.0a7+-8a4d4f3/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3.json | results/bm-20250425-3.14.0a7+-8a4d4f3-NOGIL/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 91.9 ms                                                                                                           | 87.7 ms: 1.05x faster                                                                                                   |
| xml_etree_parse      | 131 ms                                                                                                            | 129 ms: 1.02x faster                                                                                                    |
| json_loads           | 27.8 us                                                                                                           | 29.3 us: 1.06x slower                                                                                                   |
| pickle_pure_python   | 307 us                                                                                                            | 328 us: 1.07x slower                                                                                                    |
| unpickle_pure_python | 213 us                                                                                                            | 230 us: 1.08x slower                                                                                                    |
| tomli_loads          | 1.87 sec                                                                                                          | 2.06 sec: 1.10x slower                                                                                                  |
| xml_etree_generate   | 82.0 ms                                                                                                           | 93.1 ms: 1.13x slower                                                                                                   |
| json_dumps           | 11.3 ms                                                                                                           | 12.8 ms: 1.14x slower                                                                                                   |
| xml_etree_process    | 57.7 ms                                                                                                           | 66.6 ms: 1.15x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.07x slower                                                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250425-3.14.0a7+-8a4d4f3/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3.json | results/bm-20250425-3.14.0a7+-8a4d4f3-NOGIL/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 15.1 ms                                                                                                           | 15.8 ms: 1.05x slower                                                                                                   |
| python_startup_no_site | 8.65 ms                                                                                                           | 11.1 ms: 1.29x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250425-3.14.0a7+-8a4d4f3/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3.json | results/bm-20250425-3.14.0a7+-8a4d4f3-NOGIL/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 47.6 ms                                                                                                           | 55.5 ms: 1.17x slower                                                                                                   |
| django_template | 33.9 ms                                                                                                           | 40.2 ms: 1.18x slower                                                                                                   |
| genshi_text     | 20.6 ms                                                                                                           | 25.9 ms: 1.26x slower                                                                                                   |
| mako            | 11.9 ms                                                                                                           | 15.4 ms: 1.30x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.22x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250425-3.14.0a7+-8a4d4f3/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3.json | results/bm-20250425-3.14.0a7+-8a4d4f3-NOGIL/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.45 ms                                                                                                           | 1.80 ms: 2.47x faster                                                                                                   |
| create_gc_cycles           | 1.86 ms                                                                                                           | 1.37 ms: 1.35x faster                                                                                                   |
| async_tree_io_tg           | 604 ms                                                                                                            | 522 ms: 1.16x faster                                                                                                    |
| async_tree_none_tg         | 252 ms                                                                                                            | 228 ms: 1.11x faster                                                                                                    |
| async_tree_io              | 604 ms                                                                                                            | 549 ms: 1.10x faster                                                                                                    |
| async_tree_memoization_tg  | 311 ms                                                                                                            | 286 ms: 1.09x faster                                                                                                    |
| sqlite_synth               | 2.19 us                                                                                                           | 2.01 us: 1.09x faster                                                                                                   |
| async_tree_cpu_io_mixed_tg | 508 ms                                                                                                            | 480 ms: 1.06x faster                                                                                                    |
| coroutines                 | 24.1 ms                                                                                                           | 22.9 ms: 1.05x faster                                                                                                   |
| xml_etree_iterparse        | 91.9 ms                                                                                                           | 87.7 ms: 1.05x faster                                                                                                   |
| async_tree_none            | 267 ms                                                                                                            | 259 ms: 1.03x faster                                                                                                    |
| float                      | 69.1 ms                                                                                                           | 67.2 ms: 1.03x faster                                                                                                   |
| regex_v8                   | 22.0 ms                                                                                                           | 21.4 ms: 1.03x faster                                                                                                   |
| xml_etree_parse            | 131 ms                                                                                                            | 129 ms: 1.02x faster                                                                                                    |
| pathlib                    | 19.3 ms                                                                                                           | 19.2 ms: 1.01x faster                                                                                                   |
| asyncio_websockets         | 517 ms                                                                                                            | 515 ms: 1.00x faster                                                                                                    |
| pidigits                   | 198 ms                                                                                                            | 198 ms: 1.00x faster                                                                                                    |
| json                       | 4.93 ms                                                                                                           | 5.03 ms: 1.02x slower                                                                                                   |
| async_tree_memoization     | 305 ms                                                                                                            | 312 ms: 1.02x slower                                                                                                    |
| regex_dna                  | 175 ms                                                                                                            | 180 ms: 1.03x slower                                                                                                    |
| pycparser                  | 1.09 sec                                                                                                          | 1.13 sec: 1.03x slower                                                                                                  |
| dulwich_log                | 67.7 ms                                                                                                           | 70.0 ms: 1.03x slower                                                                                                   |
| python_startup             | 15.1 ms                                                                                                           | 15.8 ms: 1.05x slower                                                                                                   |
| bpe_tokeniser              | 4.14 sec                                                                                                          | 4.37 sec: 1.05x slower                                                                                                  |
| scimark_fft                | 321 ms                                                                                                            | 339 ms: 1.06x slower                                                                                                    |
| json_loads                 | 27.8 us                                                                                                           | 29.3 us: 1.06x slower                                                                                                   |
| regex_effbot               | 2.68 ms                                                                                                           | 2.85 ms: 1.06x slower                                                                                                   |
| spectral_norm              | 94.2 ms                                                                                                           | 100 ms: 1.07x slower                                                                                                    |
| docutils                   | 2.53 sec                                                                                                          | 2.70 sec: 1.07x slower                                                                                                  |
| pickle_pure_python         | 307 us                                                                                                            | 328 us: 1.07x slower                                                                                                    |
| unpickle_pure_python       | 213 us                                                                                                            | 230 us: 1.08x slower                                                                                                    |
| logging_silent             | 96.1 ns                                                                                                           | 104 ns: 1.08x slower                                                                                                    |
| bench_mp_pool              | 88.1 ms                                                                                                           | 95.7 ms: 1.09x slower                                                                                                   |
| scimark_sor                | 109 ms                                                                                                            | 118 ms: 1.09x slower                                                                                                    |
| pylint                     | 279 ms                                                                                                            | 304 ms: 1.09x slower                                                                                                    |
| deltablue                  | 3.23 ms                                                                                                           | 3.53 ms: 1.09x slower                                                                                                   |
| generators                 | 27.8 ms                                                                                                           | 30.5 ms: 1.10x slower                                                                                                   |
| sphinx                     | 974 ms                                                                                                            | 1.07 sec: 1.10x slower                                                                                                  |
| many_optionals             | 1.00 ms                                                                                                           | 1.10 ms: 1.10x slower                                                                                                   |
| tomli_loads                | 1.87 sec                                                                                                          | 2.06 sec: 1.10x slower                                                                                                  |
| k_core                     | 2.03 sec                                                                                                          | 2.24 sec: 1.10x slower                                                                                                  |
| scimark_sparse_mat_mult    | 4.43 ms                                                                                                           | 4.94 ms: 1.11x slower                                                                                                   |
| subparsers                 | 21.8 ms                                                                                                           | 24.4 ms: 1.12x slower                                                                                                   |
| async_generators           | 326 ms                                                                                                            | 367 ms: 1.13x slower                                                                                                    |
| pprint_safe_repr           | 688 ms                                                                                                            | 776 ms: 1.13x slower                                                                                                    |
| chaos                      | 53.9 ms                                                                                                           | 60.9 ms: 1.13x slower                                                                                                   |
| 2to3                       | 247 ms                                                                                                            | 280 ms: 1.13x slower                                                                                                    |
| xml_etree_generate         | 82.0 ms                                                                                                           | 93.1 ms: 1.13x slower                                                                                                   |
| nqueens                    | 76.6 ms                                                                                                           | 87.0 ms: 1.14x slower                                                                                                   |
| json_dumps                 | 11.3 ms                                                                                                           | 12.8 ms: 1.14x slower                                                                                                   |
| pprint_pformat             | 1.40 sec                                                                                                          | 1.60 sec: 1.14x slower                                                                                                  |
| pyflate                    | 405 ms                                                                                                            | 463 ms: 1.14x slower                                                                                                    |
| comprehensions             | 16.7 us                                                                                                           | 19.2 us: 1.15x slower                                                                                                   |
| scimark_lu                 | 111 ms                                                                                                            | 127 ms: 1.15x slower                                                                                                    |
| sqlglot_v2_normalize       | 99.5 ms                                                                                                           | 114 ms: 1.15x slower                                                                                                    |
| go                         | 108 ms                                                                                                            | 125 ms: 1.15x slower                                                                                                    |
| xml_etree_process          | 57.7 ms                                                                                                           | 66.6 ms: 1.15x slower                                                                                                   |
| hexiom                     | 5.74 ms                                                                                                           | 6.65 ms: 1.16x slower                                                                                                   |
| deepcopy_reduce            | 2.56 us                                                                                                           | 2.97 us: 1.16x slower                                                                                                   |
| logging_simple             | 5.93 us                                                                                                           | 6.88 us: 1.16x slower                                                                                                   |
| sqlglot_v2_optimize        | 49.8 ms                                                                                                           | 57.9 ms: 1.16x slower                                                                                                   |
| mdp                        | 1.13 sec                                                                                                          | 1.32 sec: 1.16x slower                                                                                                  |
| genshi_xml                 | 47.6 ms                                                                                                           | 55.5 ms: 1.17x slower                                                                                                   |
| sympy_integrate            | 18.7 ms                                                                                                           | 21.8 ms: 1.17x slower                                                                                                   |
| sympy_sum                  | 151 ms                                                                                                            | 177 ms: 1.17x slower                                                                                                    |
| regex_compile              | 122 ms                                                                                                            | 143 ms: 1.17x slower                                                                                                    |
| sympy_expand               | 445 ms                                                                                                            | 523 ms: 1.17x slower                                                                                                    |
| sqlalchemy_declarative     | 129 ms                                                                                                            | 152 ms: 1.18x slower                                                                                                    |
| sympy_str                  | 265 ms                                                                                                            | 312 ms: 1.18x slower                                                                                                    |
| raytrace                   | 247 ms                                                                                                            | 292 ms: 1.18x slower                                                                                                    |
| deepcopy                   | 245 us                                                                                                            | 290 us: 1.18x slower                                                                                                    |
| django_template            | 33.9 ms                                                                                                           | 40.2 ms: 1.18x slower                                                                                                   |
| sqlglot_v2_transpile       | 1.50 ms                                                                                                           | 1.79 ms: 1.19x slower                                                                                                   |
| sqlalchemy_imperative      | 19.8 ms                                                                                                           | 23.5 ms: 1.19x slower                                                                                                   |
| scimark_monte_carlo        | 61.6 ms                                                                                                           | 73.4 ms: 1.19x slower                                                                                                   |
| deepcopy_memo              | 28.9 us                                                                                                           | 34.4 us: 1.19x slower                                                                                                   |
| fannkuch                   | 380 ms                                                                                                            | 454 ms: 1.19x slower                                                                                                    |
| logging_format             | 6.57 us                                                                                                           | 7.91 us: 1.20x slower                                                                                                   |
| shortest_path              | 439 ms                                                                                                            | 529 ms: 1.20x slower                                                                                                    |
| telco                      | 7.06 ms                                                                                                           | 8.50 ms: 1.20x slower                                                                                                   |
| connected_components       | 395 ms                                                                                                            | 479 ms: 1.21x slower                                                                                                    |
| sqlglot_v2_parse           | 1.21 ms                                                                                                           | 1.47 ms: 1.21x slower                                                                                                   |
| richards                   | 41.5 ms                                                                                                           | 50.6 ms: 1.22x slower                                                                                                   |
| typing_runtime_protocols   | 154 us                                                                                                            | 189 us: 1.23x slower                                                                                                    |
| richards_super             | 47.2 ms                                                                                                           | 58.3 ms: 1.24x slower                                                                                                   |
| crypto_pyaes               | 66.8 ms                                                                                                           | 82.7 ms: 1.24x slower                                                                                                   |
| nbody                      | 87.8 ms                                                                                                           | 110 ms: 1.26x slower                                                                                                    |
| genshi_text                | 20.6 ms                                                                                                           | 25.9 ms: 1.26x slower                                                                                                   |
| meteor_contest             | 98.9 ms                                                                                                           | 126 ms: 1.28x slower                                                                                                    |
| python_startup_no_site     | 8.65 ms                                                                                                           | 11.1 ms: 1.29x slower                                                                                                   |
| mako                       | 11.9 ms                                                                                                           | 15.4 ms: 1.30x slower                                                                                                   |
| coverage                   | 82.2 ms                                                                                                           | 108 ms: 1.32x slower                                                                                                    |
| bench_thread_pool          | 1.05 ms                                                                                                           | 3.12 ms: 2.98x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.10x slower                                                                                                            |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed
Ignored benchmarks (1) of results/bm-20250425-3.14.0a7+-8a4d4f3-NOGIL/bm-20250425-vultr-x86_64-python-8a4d4f37abb9fa639fdc-3.14.0a7+-8a4d4f3.json: html5lib

- Geometric mean (including insignificant results): 1.083x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.20x