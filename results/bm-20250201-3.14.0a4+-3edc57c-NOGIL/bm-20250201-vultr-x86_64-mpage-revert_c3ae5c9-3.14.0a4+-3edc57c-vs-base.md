# Results vs. base

- fork: mpage
- ref: revert_c3ae5c9
- machine: linux-x86_64
- commit hash: 3edc57c
- commit date: 2025-02-01
- overall geometric mean: 1.027x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| 2to3           | 295 ms                                                                 | 304 ms: 1.03x slower                                            |
| docutils       | 2.75 sec                                                               | 2.80 sec: 1.02x slower                                          |
| html5lib       | 69.1 ms                                                                | 70.9 ms: 1.03x slower                                           |
| sphinx         | 1.09 sec                                                               | 1.11 sec: 1.02x slower                                          |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| async_generators           | 371 ms                                                                 | 375 ms: 1.01x slower                                            |
| async_tree_cpu_io_mixed    | 531 ms                                                                 | 540 ms: 1.02x slower                                            |
| async_tree_memoization     | 348 ms                                                                 | 354 ms: 1.02x slower                                            |
| async_tree_cpu_io_mixed_tg | 496 ms                                                                 | 506 ms: 1.02x slower                                            |
| async_tree_none            | 283 ms                                                                 | 289 ms: 1.02x slower                                            |
| coroutines                 | 22.6 ms                                                                | 23.2 ms: 1.03x slower                                           |
| async_tree_none_tg         | 244 ms                                                                 | 252 ms: 1.03x slower                                            |
| async_tree_io              | 592 ms                                                                 | 614 ms: 1.04x slower                                            |
| async_tree_io_tg           | 561 ms                                                                 | 587 ms: 1.05x slower                                            |
| async_tree_memoization_tg  | 311 ms                                                                 | 326 ms: 1.05x slower                                            |
| Geometric mean             | (ref)                                                                  | 1.03x slower                                                    |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| pidigits       | 195 ms                                                                 | 192 ms: 1.01x faster                                            |
| float          | 74.5 ms                                                                | 76.7 ms: 1.03x slower                                           |
| nbody          | 125 ms                                                                 | 137 ms: 1.10x slower                                            |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| regex_dna      | 185 ms                                                                 | 181 ms: 1.02x faster                                            |
| regex_effbot   | 2.76 ms                                                                | 2.79 ms: 1.01x slower                                           |
| regex_compile  | 145 ms                                                                 | 150 ms: 1.03x slower                                            |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                    |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| xml_etree_iterparse  | 86.3 ms                                                                | 87.5 ms: 1.01x slower                                           |
| json_loads           | 31.1 us                                                                | 31.6 us: 1.01x slower                                           |
| json_dumps           | 12.7 ms                                                                | 12.9 ms: 1.02x slower                                           |
| xml_etree_generate   | 94.2 ms                                                                | 96.1 ms: 1.02x slower                                           |
| xml_etree_process    | 67.1 ms                                                                | 68.9 ms: 1.03x slower                                           |
| unpickle_pure_python | 238 us                                                                 | 246 us: 1.03x slower                                            |
| pickle_pure_python   | 357 us                                                                 | 374 us: 1.05x slower                                            |
| tomli_loads          | 2.26 sec                                                               | 2.38 sec: 1.06x slower                                          |
| Geometric mean       | (ref)                                                                  | 1.03x slower                                                    |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| python_startup_no_site | 9.61 ms                                                                | 9.64 ms: 1.00x slower                                           |
| python_startup         | 15.3 ms                                                                | 15.4 ms: 1.01x slower                                           |
| Geometric mean         | (ref)                                                                  | 1.01x slower                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| mako            | 15.6 ms                                                                | 15.9 ms: 1.02x slower                                           |
| django_template | 40.9 ms                                                                | 42.1 ms: 1.03x slower                                           |
| genshi_text     | 27.1 ms                                                                | 28.3 ms: 1.04x slower                                           |
| genshi_xml      | 57.6 ms                                                                | 61.1 ms: 1.06x slower                                           |
| Geometric mean  | (ref)                                                                  | 1.04x slower                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| gc_traversal               | 1.73 ms                                                                | 1.66 ms: 1.04x faster                                           |
| regex_dna                  | 185 ms                                                                 | 181 ms: 1.02x faster                                            |
| pidigits                   | 195 ms                                                                 | 192 ms: 1.01x faster                                            |
| k_core                     | 2.30 sec                                                               | 2.31 sec: 1.00x slower                                          |
| python_startup_no_site     | 9.61 ms                                                                | 9.64 ms: 1.00x slower                                           |
| python_startup             | 15.3 ms                                                                | 15.4 ms: 1.01x slower                                           |
| bench_mp_pool              | 90.4 ms                                                                | 91.1 ms: 1.01x slower                                           |
| meteor_contest             | 129 ms                                                                 | 130 ms: 1.01x slower                                            |
| async_generators           | 371 ms                                                                 | 375 ms: 1.01x slower                                            |
| regex_effbot               | 2.76 ms                                                                | 2.79 ms: 1.01x slower                                           |
| shortest_path              | 540 ms                                                                 | 546 ms: 1.01x slower                                            |
| logging_format             | 8.00 us                                                                | 8.10 us: 1.01x slower                                           |
| xml_etree_iterparse        | 86.3 ms                                                                | 87.5 ms: 1.01x slower                                           |
| bpe_tokeniser              | 4.57 sec                                                               | 4.64 sec: 1.01x slower                                          |
| json_loads                 | 31.1 us                                                                | 31.6 us: 1.01x slower                                           |
| connected_components       | 488 ms                                                                 | 496 ms: 1.01x slower                                            |
| mako                       | 15.6 ms                                                                | 15.9 ms: 1.02x slower                                           |
| sqlalchemy_imperative      | 23.7 ms                                                                | 24.1 ms: 1.02x slower                                           |
| logging_simple             | 7.18 us                                                                | 7.30 us: 1.02x slower                                           |
| typing_runtime_protocols   | 196 us                                                                 | 199 us: 1.02x slower                                            |
| pathlib                    | 18.2 ms                                                                | 18.5 ms: 1.02x slower                                           |
| async_tree_cpu_io_mixed    | 531 ms                                                                 | 540 ms: 1.02x slower                                            |
| json_dumps                 | 12.7 ms                                                                | 12.9 ms: 1.02x slower                                           |
| async_tree_memoization     | 348 ms                                                                 | 354 ms: 1.02x slower                                            |
| telco                      | 8.46 ms                                                                | 8.61 ms: 1.02x slower                                           |
| docutils                   | 2.75 sec                                                               | 2.80 sec: 1.02x slower                                          |
| logging_silent             | 107 ns                                                                 | 109 ns: 1.02x slower                                            |
| xml_etree_generate         | 94.2 ms                                                                | 96.1 ms: 1.02x slower                                           |
| sympy_expand               | 539 ms                                                                 | 550 ms: 1.02x slower                                            |
| async_tree_cpu_io_mixed_tg | 496 ms                                                                 | 506 ms: 1.02x slower                                            |
| async_tree_none            | 283 ms                                                                 | 289 ms: 1.02x slower                                            |
| coverage                   | 96.5 ms                                                                | 98.5 ms: 1.02x slower                                           |
| crypto_pyaes               | 87.1 ms                                                                | 89.0 ms: 1.02x slower                                           |
| json                       | 5.34 ms                                                                | 5.46 ms: 1.02x slower                                           |
| sympy_sum                  | 182 ms                                                                 | 186 ms: 1.02x slower                                            |
| fannkuch                   | 482 ms                                                                 | 493 ms: 1.02x slower                                            |
| sqlalchemy_declarative     | 153 ms                                                                 | 157 ms: 1.02x slower                                            |
| sphinx                     | 1.09 sec                                                               | 1.11 sec: 1.02x slower                                          |
| chaos                      | 67.0 ms                                                                | 68.6 ms: 1.02x slower                                           |
| create_gc_cycles           | 1.37 ms                                                                | 1.40 ms: 1.02x slower                                           |
| sympy_str                  | 329 ms                                                                 | 337 ms: 1.02x slower                                            |
| pycparser                  | 1.15 sec                                                               | 1.18 sec: 1.02x slower                                          |
| pylint                     | 308 ms                                                                 | 316 ms: 1.03x slower                                            |
| dulwich_log                | 80.8 ms                                                                | 82.9 ms: 1.03x slower                                           |
| html5lib                   | 69.1 ms                                                                | 70.9 ms: 1.03x slower                                           |
| coroutines                 | 22.6 ms                                                                | 23.2 ms: 1.03x slower                                           |
| xml_etree_process          | 67.1 ms                                                                | 68.9 ms: 1.03x slower                                           |
| sqlglot_parse              | 1.54 ms                                                                | 1.58 ms: 1.03x slower                                           |
| sqlglot_normalize          | 117 ms                                                                 | 120 ms: 1.03x slower                                            |
| thrift                     | 896 us                                                                 | 922 us: 1.03x slower                                            |
| sympy_integrate            | 23.5 ms                                                                | 24.2 ms: 1.03x slower                                           |
| nqueens                    | 93.8 ms                                                                | 96.6 ms: 1.03x slower                                           |
| django_template            | 40.9 ms                                                                | 42.1 ms: 1.03x slower                                           |
| many_optionals             | 1.15 ms                                                                | 1.18 ms: 1.03x slower                                           |
| sqlglot_optimize           | 59.4 ms                                                                | 61.2 ms: 1.03x slower                                           |
| float                      | 74.5 ms                                                                | 76.7 ms: 1.03x slower                                           |
| 2to3                       | 295 ms                                                                 | 304 ms: 1.03x slower                                            |
| sqlglot_transpile          | 1.85 ms                                                                | 1.91 ms: 1.03x slower                                           |
| regex_compile              | 145 ms                                                                 | 150 ms: 1.03x slower                                            |
| unpickle_pure_python       | 238 us                                                                 | 246 us: 1.03x slower                                            |
| scimark_fft                | 376 ms                                                                 | 389 ms: 1.03x slower                                            |
| async_tree_none_tg         | 244 ms                                                                 | 252 ms: 1.03x slower                                            |
| pyflate                    | 483 ms                                                                 | 501 ms: 1.04x slower                                            |
| comprehensions             | 19.1 us                                                                | 19.9 us: 1.04x slower                                           |
| async_tree_io              | 592 ms                                                                 | 614 ms: 1.04x slower                                            |
| deepcopy_reduce            | 3.11 us                                                                | 3.23 us: 1.04x slower                                           |
| scimark_sor                | 128 ms                                                                 | 133 ms: 1.04x slower                                            |
| mdp                        | 2.54 sec                                                               | 2.64 sec: 1.04x slower                                          |
| scimark_monte_carlo        | 79.9 ms                                                                | 83.1 ms: 1.04x slower                                           |
| raytrace                   | 313 ms                                                                 | 327 ms: 1.04x slower                                            |
| deepcopy                   | 299 us                                                                 | 312 us: 1.04x slower                                            |
| genshi_text                | 27.1 ms                                                                | 28.3 ms: 1.04x slower                                           |
| hexiom                     | 7.08 ms                                                                | 7.41 ms: 1.05x slower                                           |
| async_tree_io_tg           | 561 ms                                                                 | 587 ms: 1.05x slower                                            |
| richards                   | 54.0 ms                                                                | 56.5 ms: 1.05x slower                                           |
| scimark_lu                 | 131 ms                                                                 | 137 ms: 1.05x slower                                            |
| async_tree_memoization_tg  | 311 ms                                                                 | 326 ms: 1.05x slower                                            |
| pickle_pure_python         | 357 us                                                                 | 374 us: 1.05x slower                                            |
| spectral_norm              | 104 ms                                                                 | 109 ms: 1.05x slower                                            |
| go                         | 130 ms                                                                 | 137 ms: 1.05x slower                                            |
| deltablue                  | 4.43 ms                                                                | 4.67 ms: 1.05x slower                                           |
| pprint_pformat             | 1.61 sec                                                               | 1.70 sec: 1.05x slower                                          |
| richards_super             | 62.5 ms                                                                | 66.0 ms: 1.05x slower                                           |
| tomli_loads                | 2.26 sec                                                               | 2.38 sec: 1.06x slower                                          |
| deepcopy_memo              | 37.0 us                                                                | 39.1 us: 1.06x slower                                           |
| pprint_safe_repr           | 779 ms                                                                 | 823 ms: 1.06x slower                                            |
| genshi_xml                 | 57.6 ms                                                                | 61.1 ms: 1.06x slower                                           |
| scimark_sparse_mat_mult    | 5.49 ms                                                                | 5.83 ms: 1.06x slower                                           |
| generators                 | 30.4 ms                                                                | 33.3 ms: 1.10x slower                                           |
| nbody                      | 125 ms                                                                 | 137 ms: 1.10x slower                                            |
| Geometric mean             | (ref)                                                                  | 1.03x slower                                                    |

Benchmark hidden because not significant (6): xml_etree_parse, sqlite_synth, bench_thread_pool, asyncio_websockets, regex_v8, subparsers

- Geometric mean (including insignificant results): 1.027x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.00x