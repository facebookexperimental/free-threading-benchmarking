# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: revert_c3ae5c9
- machine: linux-x86_64
- commit hash: 3edc57c
- commit date: 2025-02-01
- overall geometric mean: 1.141x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| 2to3           | 252 ms                                                                 | 304 ms: 1.21x slower                                            |
| docutils       | 2.52 sec                                                               | 2.80 sec: 1.11x slower                                          |
| sphinx         | 964 ms                                                                 | 1.11 sec: 1.16x slower                                          |
| Geometric mean | (ref)                                                                  | 1.16x slower                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| async_tree_io_tg           | 628 ms                                                                 | 587 ms: 1.07x faster                                            |
| async_tree_none_tg         | 261 ms                                                                 | 252 ms: 1.04x faster                                            |
| async_tree_io              | 620 ms                                                                 | 614 ms: 1.01x faster                                            |
| async_tree_memoization_tg  | 314 ms                                                                 | 326 ms: 1.04x slower                                            |
| async_tree_cpu_io_mixed_tg | 483 ms                                                                 | 506 ms: 1.05x slower                                            |
| async_tree_none            | 269 ms                                                                 | 289 ms: 1.08x slower                                            |
| async_tree_cpu_io_mixed    | 500 ms                                                                 | 540 ms: 1.08x slower                                            |
| coroutines                 | 21.5 ms                                                                | 23.2 ms: 1.08x slower                                           |
| async_tree_memoization     | 323 ms                                                                 | 354 ms: 1.09x slower                                            |
| async_generators           | 324 ms                                                                 | 375 ms: 1.16x slower                                            |
| Geometric mean             | (ref)                                                                  | 1.04x slower                                                    |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| pidigits       | 197 ms                                                                 | 192 ms: 1.02x faster                                            |
| float          | 71.4 ms                                                                | 76.7 ms: 1.08x slower                                           |
| nbody          | 88.6 ms                                                                | 137 ms: 1.55x slower                                            |
| Geometric mean | (ref)                                                                  | 1.18x slower                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| regex_v8       | 22.8 ms                                                                | 23.7 ms: 1.04x slower                                           |
| regex_dna      | 170 ms                                                                 | 181 ms: 1.06x slower                                            |
| regex_effbot   | 2.57 ms                                                                | 2.79 ms: 1.09x slower                                           |
| regex_compile  | 125 ms                                                                 | 150 ms: 1.20x slower                                            |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| xml_etree_iterparse  | 91.7 ms                                                                | 87.5 ms: 1.05x faster                                           |
| xml_etree_parse      | 129 ms                                                                 | 127 ms: 1.02x faster                                            |
| json_loads           | 28.5 us                                                                | 31.6 us: 1.11x slower                                           |
| json_dumps           | 11.3 ms                                                                | 12.9 ms: 1.14x slower                                           |
| xml_etree_generate   | 82.6 ms                                                                | 96.1 ms: 1.16x slower                                           |
| unpickle_pure_python | 210 us                                                                 | 246 us: 1.17x slower                                            |
| xml_etree_process    | 57.5 ms                                                                | 68.9 ms: 1.20x slower                                           |
| pickle_pure_python   | 307 us                                                                 | 374 us: 1.22x slower                                            |
| tomli_loads          | 1.87 sec                                                               | 2.38 sec: 1.28x slower                                          |
| Geometric mean       | (ref)                                                                  | 1.13x slower                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 15.4 ms: 1.05x slower                                           |
| python_startup_no_site | 7.44 ms                                                                | 9.64 ms: 1.30x slower                                           |
| Geometric mean         | (ref)                                                                  | 1.17x slower                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| django_template | 33.9 ms                                                                | 42.1 ms: 1.24x slower                                           |
| genshi_xml      | 47.9 ms                                                                | 61.1 ms: 1.28x slower                                           |
| mako            | 11.8 ms                                                                | 15.9 ms: 1.34x slower                                           |
| genshi_text     | 20.8 ms                                                                | 28.3 ms: 1.36x slower                                           |
| Geometric mean  | (ref)                                                                  | 1.31x slower                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec | bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------:|
| gc_traversal               | 4.44 ms                                                                | 1.66 ms: 2.67x faster                                           |
| create_gc_cycles           | 1.86 ms                                                                | 1.40 ms: 1.33x faster                                           |
| sqlite_synth               | 2.19 us                                                                | 2.05 us: 1.07x faster                                           |
| async_tree_io_tg           | 628 ms                                                                 | 587 ms: 1.07x faster                                            |
| xml_etree_iterparse        | 91.7 ms                                                                | 87.5 ms: 1.05x faster                                           |
| async_tree_none_tg         | 261 ms                                                                 | 252 ms: 1.04x faster                                            |
| pidigits                   | 197 ms                                                                 | 192 ms: 1.02x faster                                            |
| xml_etree_parse            | 129 ms                                                                 | 127 ms: 1.02x faster                                            |
| async_tree_io              | 620 ms                                                                 | 614 ms: 1.01x faster                                            |
| pathlib                    | 18.5 ms                                                                | 18.5 ms: 1.00x slower                                           |
| regex_v8                   | 22.8 ms                                                                | 23.7 ms: 1.04x slower                                           |
| async_tree_memoization_tg  | 314 ms                                                                 | 326 ms: 1.04x slower                                            |
| bench_mp_pool              | 87.7 ms                                                                | 91.1 ms: 1.04x slower                                           |
| async_tree_cpu_io_mixed_tg | 483 ms                                                                 | 506 ms: 1.05x slower                                            |
| python_startup             | 14.6 ms                                                                | 15.4 ms: 1.05x slower                                           |
| regex_dna                  | 170 ms                                                                 | 181 ms: 1.06x slower                                            |
| pycparser                  | 1.11 sec                                                               | 1.18 sec: 1.07x slower                                          |
| json                       | 5.10 ms                                                                | 5.46 ms: 1.07x slower                                           |
| float                      | 71.4 ms                                                                | 76.7 ms: 1.08x slower                                           |
| async_tree_none            | 269 ms                                                                 | 289 ms: 1.08x slower                                            |
| logging_silent             | 101 ns                                                                 | 109 ns: 1.08x slower                                            |
| async_tree_cpu_io_mixed    | 500 ms                                                                 | 540 ms: 1.08x slower                                            |
| coroutines                 | 21.5 ms                                                                | 23.2 ms: 1.08x slower                                           |
| mdp                        | 2.43 sec                                                               | 2.64 sec: 1.09x slower                                          |
| regex_effbot               | 2.57 ms                                                                | 2.79 ms: 1.09x slower                                           |
| async_tree_memoization     | 323 ms                                                                 | 354 ms: 1.09x slower                                            |
| dulwich_log                | 75.2 ms                                                                | 82.9 ms: 1.10x slower                                           |
| json_loads                 | 28.5 us                                                                | 31.6 us: 1.11x slower                                           |
| docutils                   | 2.52 sec                                                               | 2.80 sec: 1.11x slower                                          |
| bpe_tokeniser              | 4.14 sec                                                               | 4.64 sec: 1.12x slower                                          |
| k_core                     | 2.03 sec                                                               | 2.31 sec: 1.14x slower                                          |
| json_dumps                 | 11.3 ms                                                                | 12.9 ms: 1.14x slower                                           |
| pylint                     | 275 ms                                                                 | 316 ms: 1.15x slower                                            |
| sphinx                     | 964 ms                                                                 | 1.11 sec: 1.16x slower                                          |
| async_generators           | 324 ms                                                                 | 375 ms: 1.16x slower                                            |
| xml_etree_generate         | 82.6 ms                                                                | 96.1 ms: 1.16x slower                                           |
| many_optionals             | 1.01 ms                                                                | 1.18 ms: 1.17x slower                                           |
| sqlglot_normalize          | 103 ms                                                                 | 120 ms: 1.17x slower                                            |
| subparsers                 | 21.9 ms                                                                | 25.5 ms: 1.17x slower                                           |
| unpickle_pure_python       | 210 us                                                                 | 246 us: 1.17x slower                                            |
| scimark_sor                | 113 ms                                                                 | 133 ms: 1.18x slower                                            |
| generators                 | 28.2 ms                                                                | 33.3 ms: 1.18x slower                                           |
| telco                      | 7.25 ms                                                                | 8.61 ms: 1.19x slower                                           |
| pprint_safe_repr           | 689 ms                                                                 | 823 ms: 1.19x slower                                            |
| regex_compile              | 125 ms                                                                 | 150 ms: 1.20x slower                                            |
| xml_etree_process          | 57.5 ms                                                                | 68.9 ms: 1.20x slower                                           |
| sqlglot_optimize           | 50.9 ms                                                                | 61.2 ms: 1.20x slower                                           |
| spectral_norm              | 90.2 ms                                                                | 109 ms: 1.21x slower                                            |
| 2to3                       | 252 ms                                                                 | 304 ms: 1.21x slower                                            |
| pprint_pformat             | 1.40 sec                                                               | 1.70 sec: 1.21x slower                                          |
| sympy_expand               | 452 ms                                                                 | 550 ms: 1.22x slower                                            |
| pickle_pure_python         | 307 us                                                                 | 374 us: 1.22x slower                                            |
| logging_format             | 6.64 us                                                                | 8.10 us: 1.22x slower                                           |
| go                         | 112 ms                                                                 | 137 ms: 1.22x slower                                            |
| sympy_sum                  | 152 ms                                                                 | 186 ms: 1.22x slower                                            |
| comprehensions             | 16.1 us                                                                | 19.9 us: 1.23x slower                                           |
| logging_simple             | 5.89 us                                                                | 7.30 us: 1.24x slower                                           |
| pyflate                    | 404 ms                                                                 | 501 ms: 1.24x slower                                            |
| deepcopy                   | 251 us                                                                 | 312 us: 1.24x slower                                            |
| chaos                      | 55.2 ms                                                                | 68.6 ms: 1.24x slower                                           |
| sympy_integrate            | 19.5 ms                                                                | 24.2 ms: 1.24x slower                                           |
| django_template            | 33.9 ms                                                                | 42.1 ms: 1.24x slower                                           |
| sqlglot_transpile          | 1.54 ms                                                                | 1.91 ms: 1.24x slower                                           |
| sqlalchemy_declarative     | 126 ms                                                                 | 157 ms: 1.25x slower                                            |
| nqueens                    | 77.5 ms                                                                | 96.6 ms: 1.25x slower                                           |
| deepcopy_reduce            | 2.59 us                                                                | 3.23 us: 1.25x slower                                           |
| raytrace                   | 261 ms                                                                 | 327 ms: 1.25x slower                                            |
| sympy_str                  | 269 ms                                                                 | 337 ms: 1.25x slower                                            |
| coverage                   | 78.7 ms                                                                | 98.5 ms: 1.25x slower                                           |
| sqlalchemy_imperative      | 19.2 ms                                                                | 24.1 ms: 1.26x slower                                           |
| thrift                     | 731 us                                                                 | 922 us: 1.26x slower                                            |
| sqlglot_parse              | 1.24 ms                                                                | 1.58 ms: 1.27x slower                                           |
| connected_components       | 390 ms                                                                 | 496 ms: 1.27x slower                                            |
| shortest_path              | 430 ms                                                                 | 546 ms: 1.27x slower                                            |
| tomli_loads                | 1.87 sec                                                               | 2.38 sec: 1.28x slower                                          |
| genshi_xml                 | 47.9 ms                                                                | 61.1 ms: 1.28x slower                                           |
| scimark_fft                | 304 ms                                                                 | 389 ms: 1.28x slower                                            |
| scimark_lu                 | 107 ms                                                                 | 137 ms: 1.28x slower                                            |
| python_startup_no_site     | 7.44 ms                                                                | 9.64 ms: 1.30x slower                                           |
| hexiom                     | 5.69 ms                                                                | 7.41 ms: 1.30x slower                                           |
| deepcopy_memo              | 29.7 us                                                                | 39.1 us: 1.32x slower                                           |
| typing_runtime_protocols   | 150 us                                                                 | 199 us: 1.33x slower                                            |
| meteor_contest             | 96.9 ms                                                                | 130 ms: 1.34x slower                                            |
| mako                       | 11.8 ms                                                                | 15.9 ms: 1.34x slower                                           |
| fannkuch                   | 366 ms                                                                 | 493 ms: 1.35x slower                                            |
| scimark_monte_carlo        | 61.4 ms                                                                | 83.1 ms: 1.35x slower                                           |
| genshi_text                | 20.8 ms                                                                | 28.3 ms: 1.36x slower                                           |
| crypto_pyaes               | 64.9 ms                                                                | 89.0 ms: 1.37x slower                                           |
| richards                   | 41.1 ms                                                                | 56.5 ms: 1.38x slower                                           |
| richards_super             | 47.1 ms                                                                | 66.0 ms: 1.40x slower                                           |
| scimark_sparse_mat_mult    | 4.12 ms                                                                | 5.83 ms: 1.42x slower                                           |
| deltablue                  | 3.04 ms                                                                | 4.67 ms: 1.54x slower                                           |
| nbody                      | 88.6 ms                                                                | 137 ms: 1.55x slower                                            |
| bench_thread_pool          | 1.02 ms                                                                | 3.29 ms: 3.22x slower                                           |
| Geometric mean             | (ref)                                                                  | 1.18x slower                                                    |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (8) of results/bm-20250201-3.14.0a4+-cf4c4ec/bm-20250201-vultr-x86_64-python-cf4c4ecc26c7e3b89f2e-3.14.0a4+-cf4c4ec.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (1) of results/bm-20250201-3.14.0a4+-3edc57c-NOGIL/bm-20250201-vultr-x86_64-mpage-revert_c3ae5c9-3.14.0a4+-3edc57c.json: html5lib

- Geometric mean (including insignificant results): 1.141x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.15x
- 95% likely to have a slowdown of 1.14x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.20x