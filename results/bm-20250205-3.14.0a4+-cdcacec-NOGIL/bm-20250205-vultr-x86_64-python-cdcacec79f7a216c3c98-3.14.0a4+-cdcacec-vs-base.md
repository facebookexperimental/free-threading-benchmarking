# Results vs. base

- fork: python
- ref: cdcacec79f7a216c3c98
- machine: linux-x86_64
- commit hash: cdcacec
- commit date: 2025-02-05
- overall geometric mean: 1.119x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250205-3.14.0a4+-cdcacec/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json | results/bm-20250205-3.14.0a4+-cdcacec-NOGIL/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 252 ms                                                                                                            | 302 ms: 1.20x slower                                                                                                    |
| docutils       | 2.54 sec                                                                                                          | 2.82 sec: 1.11x slower                                                                                                  |
| sphinx         | 975 ms                                                                                                            | 1.11 sec: 1.14x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.15x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250205-3.14.0a4+-cdcacec/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json | results/bm-20250205-3.14.0a4+-cdcacec-NOGIL/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 623 ms                                                                                                            | 564 ms: 1.10x faster                                                                                                    |
| async_tree_none_tg         | 259 ms                                                                                                            | 243 ms: 1.06x faster                                                                                                    |
| async_tree_io              | 621 ms                                                                                                            | 596 ms: 1.04x faster                                                                                                    |
| async_tree_memoization_tg  | 317 ms                                                                                                            | 312 ms: 1.02x faster                                                                                                    |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                                                            | 501 ms: 1.03x slower                                                                                                    |
| async_tree_none            | 268 ms                                                                                                            | 283 ms: 1.05x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 500 ms                                                                                                            | 534 ms: 1.07x slower                                                                                                    |
| async_tree_memoization     | 323 ms                                                                                                            | 347 ms: 1.07x slower                                                                                                    |
| coroutines                 | 21.6 ms                                                                                                           | 23.4 ms: 1.09x slower                                                                                                   |
| async_generators           | 321 ms                                                                                                            | 372 ms: 1.16x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.02x slower                                                                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250205-3.14.0a4+-cdcacec/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json | results/bm-20250205-3.14.0a4+-cdcacec-NOGIL/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 187 ms                                                                                                            | 196 ms: 1.05x slower                                                                                                    |
| float          | 71.5 ms                                                                                                           | 76.5 ms: 1.07x slower                                                                                                   |
| nbody          | 95.9 ms                                                                                                           | 130 ms: 1.36x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.15x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250205-3.14.0a4+-cdcacec/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json | results/bm-20250205-3.14.0a4+-cdcacec-NOGIL/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 23.8 ms                                                                                                           | 24.4 ms: 1.02x slower                                                                                                   |
| regex_effbot   | 2.71 ms                                                                                                           | 2.85 ms: 1.05x slower                                                                                                   |
| regex_dna      | 165 ms                                                                                                            | 187 ms: 1.13x slower                                                                                                    |
| regex_compile  | 126 ms                                                                                                            | 151 ms: 1.20x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.10x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250205-3.14.0a4+-cdcacec/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json | results/bm-20250205-3.14.0a4+-cdcacec-NOGIL/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 91.1 ms                                                                                                           | 87.4 ms: 1.04x faster                                                                                                   |
| json_loads           | 28.7 us                                                                                                           | 31.1 us: 1.08x slower                                                                                                   |
| json_dumps           | 11.2 ms                                                                                                           | 12.8 ms: 1.14x slower                                                                                                   |
| unpickle_pure_python | 212 us                                                                                                            | 244 us: 1.15x slower                                                                                                    |
| xml_etree_generate   | 82.7 ms                                                                                                           | 96.1 ms: 1.16x slower                                                                                                   |
| xml_etree_process    | 57.6 ms                                                                                                           | 68.3 ms: 1.19x slower                                                                                                   |
| pickle_pure_python   | 309 us                                                                                                            | 367 us: 1.19x slower                                                                                                    |
| tomli_loads          | 1.92 sec                                                                                                          | 2.35 sec: 1.23x slower                                                                                                  |
| Geometric mean       | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250205-3.14.0a4+-cdcacec/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json | results/bm-20250205-3.14.0a4+-cdcacec-NOGIL/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                                                           | 15.3 ms: 1.04x slower                                                                                                   |
| python_startup_no_site | 7.47 ms                                                                                                           | 9.62 ms: 1.29x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.16x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250205-3.14.0a4+-cdcacec/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json | results/bm-20250205-3.14.0a4+-cdcacec-NOGIL/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 48.0 ms                                                                                                           | 58.0 ms: 1.21x slower                                                                                                   |
| django_template | 33.6 ms                                                                                                           | 41.3 ms: 1.23x slower                                                                                                   |
| genshi_text     | 21.1 ms                                                                                                           | 27.5 ms: 1.30x slower                                                                                                   |
| mako            | 11.8 ms                                                                                                           | 16.0 ms: 1.35x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.27x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20250205-3.14.0a4+-cdcacec/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json | results/bm-20250205-3.14.0a4+-cdcacec-NOGIL/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.22 ms                                                                                                           | 1.75 ms: 2.41x faster                                                                                                   |
| sqlglot_normalize          | 281 ms                                                                                                            | 119 ms: 2.36x faster                                                                                                    |
| create_gc_cycles           | 1.86 ms                                                                                                           | 1.40 ms: 1.33x faster                                                                                                   |
| async_tree_io_tg           | 623 ms                                                                                                            | 564 ms: 1.10x faster                                                                                                    |
| sqlite_synth               | 2.19 us                                                                                                           | 2.02 us: 1.09x faster                                                                                                   |
| async_tree_none_tg         | 259 ms                                                                                                            | 243 ms: 1.06x faster                                                                                                    |
| xml_etree_iterparse        | 91.1 ms                                                                                                           | 87.4 ms: 1.04x faster                                                                                                   |
| async_tree_io              | 621 ms                                                                                                            | 596 ms: 1.04x faster                                                                                                    |
| async_tree_memoization_tg  | 317 ms                                                                                                            | 312 ms: 1.02x faster                                                                                                    |
| regex_v8                   | 23.8 ms                                                                                                           | 24.4 ms: 1.02x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                                                            | 501 ms: 1.03x slower                                                                                                    |
| pathlib                    | 18.1 ms                                                                                                           | 18.8 ms: 1.04x slower                                                                                                   |
| python_startup             | 14.7 ms                                                                                                           | 15.3 ms: 1.04x slower                                                                                                   |
| pidigits                   | 187 ms                                                                                                            | 196 ms: 1.05x slower                                                                                                    |
| regex_effbot               | 2.71 ms                                                                                                           | 2.85 ms: 1.05x slower                                                                                                   |
| async_tree_none            | 268 ms                                                                                                            | 283 ms: 1.05x slower                                                                                                    |
| json                       | 5.09 ms                                                                                                           | 5.38 ms: 1.06x slower                                                                                                   |
| pycparser                  | 1.11 sec                                                                                                          | 1.18 sec: 1.07x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 500 ms                                                                                                            | 534 ms: 1.07x slower                                                                                                    |
| float                      | 71.5 ms                                                                                                           | 76.5 ms: 1.07x slower                                                                                                   |
| async_tree_memoization     | 323 ms                                                                                                            | 347 ms: 1.07x slower                                                                                                    |
| bench_mp_pool              | 88.0 ms                                                                                                           | 94.8 ms: 1.08x slower                                                                                                   |
| json_loads                 | 28.7 us                                                                                                           | 31.1 us: 1.08x slower                                                                                                   |
| coroutines                 | 21.6 ms                                                                                                           | 23.4 ms: 1.09x slower                                                                                                   |
| dulwich_log                | 74.9 ms                                                                                                           | 82.5 ms: 1.10x slower                                                                                                   |
| bpe_tokeniser              | 4.19 sec                                                                                                          | 4.64 sec: 1.11x slower                                                                                                  |
| docutils                   | 2.54 sec                                                                                                          | 2.82 sec: 1.11x slower                                                                                                  |
| logging_silent             | 102 ns                                                                                                            | 113 ns: 1.11x slower                                                                                                    |
| generators                 | 28.8 ms                                                                                                           | 32.0 ms: 1.11x slower                                                                                                   |
| k_core                     | 2.05 sec                                                                                                          | 2.30 sec: 1.12x slower                                                                                                  |
| regex_dna                  | 165 ms                                                                                                            | 187 ms: 1.13x slower                                                                                                    |
| scimark_sor                | 115 ms                                                                                                            | 130 ms: 1.14x slower                                                                                                    |
| json_dumps                 | 11.2 ms                                                                                                           | 12.8 ms: 1.14x slower                                                                                                   |
| sphinx                     | 975 ms                                                                                                            | 1.11 sec: 1.14x slower                                                                                                  |
| pylint                     | 276 ms                                                                                                            | 316 ms: 1.15x slower                                                                                                    |
| unpickle_pure_python       | 212 us                                                                                                            | 244 us: 1.15x slower                                                                                                    |
| telco                      | 7.33 ms                                                                                                           | 8.42 ms: 1.15x slower                                                                                                   |
| mdp                        | 2.32 sec                                                                                                          | 2.68 sec: 1.16x slower                                                                                                  |
| async_generators           | 321 ms                                                                                                            | 372 ms: 1.16x slower                                                                                                    |
| xml_etree_generate         | 82.7 ms                                                                                                           | 96.1 ms: 1.16x slower                                                                                                   |
| many_optionals             | 1.01 ms                                                                                                           | 1.18 ms: 1.16x slower                                                                                                   |
| subparsers                 | 21.9 ms                                                                                                           | 25.6 ms: 1.17x slower                                                                                                   |
| pprint_safe_repr           | 686 ms                                                                                                            | 805 ms: 1.17x slower                                                                                                    |
| xml_etree_process          | 57.6 ms                                                                                                           | 68.3 ms: 1.19x slower                                                                                                   |
| pickle_pure_python         | 309 us                                                                                                            | 367 us: 1.19x slower                                                                                                    |
| sqlglot_optimize           | 51.0 ms                                                                                                           | 60.7 ms: 1.19x slower                                                                                                   |
| comprehensions             | 16.5 us                                                                                                           | 19.7 us: 1.19x slower                                                                                                   |
| pprint_pformat             | 1.40 sec                                                                                                          | 1.67 sec: 1.19x slower                                                                                                  |
| pyflate                    | 409 ms                                                                                                            | 489 ms: 1.20x slower                                                                                                    |
| 2to3                       | 252 ms                                                                                                            | 302 ms: 1.20x slower                                                                                                    |
| regex_compile              | 126 ms                                                                                                            | 151 ms: 1.20x slower                                                                                                    |
| spectral_norm              | 91.1 ms                                                                                                           | 109 ms: 1.20x slower                                                                                                    |
| chaos                      | 56.6 ms                                                                                                           | 68.1 ms: 1.20x slower                                                                                                   |
| scimark_lu                 | 113 ms                                                                                                            | 136 ms: 1.20x slower                                                                                                    |
| go                         | 114 ms                                                                                                            | 138 ms: 1.21x slower                                                                                                    |
| genshi_xml                 | 48.0 ms                                                                                                           | 58.0 ms: 1.21x slower                                                                                                   |
| sympy_expand               | 453 ms                                                                                                            | 549 ms: 1.21x slower                                                                                                    |
| sympy_sum                  | 152 ms                                                                                                            | 185 ms: 1.22x slower                                                                                                    |
| scimark_fft                | 317 ms                                                                                                            | 385 ms: 1.22x slower                                                                                                    |
| logging_format             | 6.80 us                                                                                                           | 8.28 us: 1.22x slower                                                                                                   |
| logging_simple             | 5.90 us                                                                                                           | 7.19 us: 1.22x slower                                                                                                   |
| nqueens                    | 78.2 ms                                                                                                           | 95.6 ms: 1.22x slower                                                                                                   |
| deepcopy_reduce            | 2.57 us                                                                                                           | 3.14 us: 1.22x slower                                                                                                   |
| coverage                   | 78.8 ms                                                                                                           | 96.5 ms: 1.22x slower                                                                                                   |
| sympy_integrate            | 19.5 ms                                                                                                           | 23.9 ms: 1.22x slower                                                                                                   |
| deepcopy                   | 249 us                                                                                                            | 306 us: 1.23x slower                                                                                                    |
| tomli_loads                | 1.92 sec                                                                                                          | 2.35 sec: 1.23x slower                                                                                                  |
| django_template            | 33.6 ms                                                                                                           | 41.3 ms: 1.23x slower                                                                                                   |
| thrift                     | 723 us                                                                                                            | 893 us: 1.24x slower                                                                                                    |
| sqlalchemy_declarative     | 127 ms                                                                                                            | 156 ms: 1.24x slower                                                                                                    |
| raytrace                   | 260 ms                                                                                                            | 322 ms: 1.24x slower                                                                                                    |
| scimark_sparse_mat_mult    | 4.47 ms                                                                                                           | 5.54 ms: 1.24x slower                                                                                                   |
| sympy_str                  | 270 ms                                                                                                            | 334 ms: 1.24x slower                                                                                                    |
| sqlglot_transpile          | 1.53 ms                                                                                                           | 1.90 ms: 1.24x slower                                                                                                   |
| deepcopy_memo              | 30.2 us                                                                                                           | 37.7 us: 1.25x slower                                                                                                   |
| connected_components       | 391 ms                                                                                                            | 492 ms: 1.26x slower                                                                                                    |
| shortest_path              | 430 ms                                                                                                            | 545 ms: 1.27x slower                                                                                                    |
| hexiom                     | 5.83 ms                                                                                                           | 7.40 ms: 1.27x slower                                                                                                   |
| sqlalchemy_imperative      | 19.0 ms                                                                                                           | 24.2 ms: 1.27x slower                                                                                                   |
| sqlglot_parse              | 1.23 ms                                                                                                           | 1.57 ms: 1.27x slower                                                                                                   |
| python_startup_no_site     | 7.47 ms                                                                                                           | 9.62 ms: 1.29x slower                                                                                                   |
| scimark_monte_carlo        | 63.1 ms                                                                                                           | 81.6 ms: 1.29x slower                                                                                                   |
| genshi_text                | 21.1 ms                                                                                                           | 27.5 ms: 1.30x slower                                                                                                   |
| fannkuch                   | 369 ms                                                                                                            | 484 ms: 1.31x slower                                                                                                    |
| crypto_pyaes               | 67.2 ms                                                                                                           | 88.2 ms: 1.31x slower                                                                                                   |
| richards                   | 41.9 ms                                                                                                           | 55.5 ms: 1.33x slower                                                                                                   |
| typing_runtime_protocols   | 150 us                                                                                                            | 199 us: 1.33x slower                                                                                                    |
| meteor_contest             | 97.8 ms                                                                                                           | 131 ms: 1.33x slower                                                                                                    |
| richards_super             | 48.0 ms                                                                                                           | 64.2 ms: 1.34x slower                                                                                                   |
| mako                       | 11.8 ms                                                                                                           | 16.0 ms: 1.35x slower                                                                                                   |
| nbody                      | 95.9 ms                                                                                                           | 130 ms: 1.36x slower                                                                                                    |
| deltablue                  | 3.12 ms                                                                                                           | 4.63 ms: 1.48x slower                                                                                                   |
| bench_thread_pool          | 1.03 ms                                                                                                           | 3.31 ms: 3.22x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.15x slower                                                                                                            |

Benchmark hidden because not significant (2): xml_etree_parse, asyncio_websockets
Ignored benchmarks (1) of results/bm-20250205-3.14.0a4+-cdcacec-NOGIL/bm-20250205-vultr-x86_64-python-cdcacec79f7a216c3c98-3.14.0a4+-cdcacec.json: html5lib

- Geometric mean (including insignificant results): 1.119x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.14x
- 95% likely to have a slowdown of 1.13x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.20x