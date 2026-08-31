# Results vs. base

- fork: kumaraditya303
- ref: gen_gi_frame_thread_
- machine: linux-x86_64
- commit hash: 1928144
- commit date: 2026-08-19
- overall geometric mean: 1.013x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260819-vultr-x86_64-python-20e6c2fc7c174342214d-3.16.0a0-20e6c2f | bm-20260819-vultr-x86_64-kumaraditya303-gen_gi_frame_thread_-3.16.0a0-1928144 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 296 ms                                                                | 300 ms: 1.01x slower                                                          |
| docutils       | 2.90 sec                                                              | 2.93 sec: 1.01x slower                                                        |
| html5lib       | 65.9 ms                                                               | 67.0 ms: 1.02x slower                                                         |
| sphinx         | 1.10 sec                                                              | 1.12 sec: 1.02x slower                                                        |
| Geometric mean | (ref)                                                                 | 1.02x slower                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20260819-vultr-x86_64-python-20e6c2fc7c174342214d-3.16.0a0-20e6c2f | bm-20260819-vultr-x86_64-kumaraditya303-gen_gi_frame_thread_-3.16.0a0-1928144 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_generators           | 419 ms                                                                | 420 ms: 1.00x slower                                                          |
| asyncio_websockets         | 507 ms                                                                | 509 ms: 1.01x slower                                                          |
| async_tree_cpu_io_mixed_tg | 582 ms                                                                | 587 ms: 1.01x slower                                                          |
| async_tree_cpu_io_mixed    | 599 ms                                                                | 609 ms: 1.02x slower                                                          |
| async_tree_memoization_tg  | 401 ms                                                                | 409 ms: 1.02x slower                                                          |
| async_tree_none_tg         | 333 ms                                                                | 340 ms: 1.02x slower                                                          |
| async_tree_io_tg           | 689 ms                                                                | 708 ms: 1.03x slower                                                          |
| async_tree_memoization     | 417 ms                                                                | 430 ms: 1.03x slower                                                          |
| async_tree_none            | 341 ms                                                                | 352 ms: 1.03x slower                                                          |
| async_tree_io              | 699 ms                                                                | 723 ms: 1.03x slower                                                          |
| coroutines                 | 24.9 ms                                                               | 26.6 ms: 1.07x slower                                                         |
| Geometric mean             | (ref)                                                                 | 1.02x slower                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260819-vultr-x86_64-python-20e6c2fc7c174342214d-3.16.0a0-20e6c2f | bm-20260819-vultr-x86_64-kumaraditya303-gen_gi_frame_thread_-3.16.0a0-1928144 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pidigits       | 187 ms                                                                | 188 ms: 1.00x slower                                                          |
| float          | 84.9 ms                                                               | 86.6 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                                  |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260819-vultr-x86_64-python-20e6c2fc7c174342214d-3.16.0a0-20e6c2f | bm-20260819-vultr-x86_64-kumaraditya303-gen_gi_frame_thread_-3.16.0a0-1928144 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_v8       | 20.5 ms                                                               | 20.1 ms: 1.02x faster                                                         |
| regex_dna      | 178 ms                                                                | 177 ms: 1.01x faster                                                          |
| regex_compile  | 170 ms                                                                | 172 ms: 1.01x slower                                                          |
| regex_effbot   | 2.78 ms                                                               | 3.00 ms: 1.08x slower                                                         |
| Geometric mean | (ref)                                                                 | 1.02x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260819-vultr-x86_64-python-20e6c2fc7c174342214d-3.16.0a0-20e6c2f | bm-20260819-vultr-x86_64-kumaraditya303-gen_gi_frame_thread_-3.16.0a0-1928144 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| xml_etree_parse      | 140 ms                                                                | 140 ms: 1.00x slower                                                          |
| pickle_pure_python   | 338 us                                                                | 340 us: 1.01x slower                                                          |
| json_dumps           | 10.1 ms                                                               | 10.2 ms: 1.01x slower                                                         |
| xml_etree_generate   | 101 ms                                                                | 102 ms: 1.01x slower                                                          |
| unpickle_pure_python | 241 us                                                                | 245 us: 1.02x slower                                                          |
| tomli_loads          | 1.95 sec                                                              | 1.99 sec: 1.02x slower                                                        |
| xml_etree_process    | 75.0 ms                                                               | 76.8 ms: 1.02x slower                                                         |
| Geometric mean       | (ref)                                                                 | 1.01x slower                                                                  |

Benchmark hidden because not significant (2): xml_etree_iterparse, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20260819-vultr-x86_64-python-20e6c2fc7c174342214d-3.16.0a0-20e6c2f | bm-20260819-vultr-x86_64-kumaraditya303-gen_gi_frame_thread_-3.16.0a0-1928144 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup | 15.8 ms                                                               | 15.8 ms: 1.00x faster                                                         |
| Geometric mean | (ref)                                                                 | 1.00x faster                                                                  |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260819-vultr-x86_64-python-20e6c2fc7c174342214d-3.16.0a0-20e6c2f | bm-20260819-vultr-x86_64-kumaraditya303-gen_gi_frame_thread_-3.16.0a0-1928144 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 16.0 ms                                                               | 15.9 ms: 1.01x faster                                                         |
| django_template | 41.5 ms                                                               | 42.6 ms: 1.03x slower                                                         |
| Geometric mean  | (ref)                                                                 | 1.01x slower                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20260819-vultr-x86_64-python-20e6c2fc7c174342214d-3.16.0a0-20e6c2f | bm-20260819-vultr-x86_64-kumaraditya303-gen_gi_frame_thread_-3.16.0a0-1928144 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| scimark_fft                | 344 ms                                                                | 336 ms: 1.02x faster                                                          |
| regex_v8                   | 20.5 ms                                                               | 20.1 ms: 1.02x faster                                                         |
| thrift                     | 938 us                                                                | 925 us: 1.01x faster                                                          |
| scimark_sparse_mat_mult    | 5.22 ms                                                               | 5.16 ms: 1.01x faster                                                         |
| mako                       | 16.0 ms                                                               | 15.9 ms: 1.01x faster                                                         |
| bench_mp_pool              | 6.75 ms                                                               | 6.71 ms: 1.01x faster                                                         |
| regex_dna                  | 178 ms                                                                | 177 ms: 1.01x faster                                                          |
| python_startup             | 15.8 ms                                                               | 15.8 ms: 1.00x faster                                                         |
| shortest_path              | 535 ms                                                                | 534 ms: 1.00x faster                                                          |
| async_generators           | 419 ms                                                                | 420 ms: 1.00x slower                                                          |
| sympy_integrate            | 21.9 ms                                                               | 22.0 ms: 1.00x slower                                                         |
| xml_etree_parse            | 140 ms                                                                | 140 ms: 1.00x slower                                                          |
| pidigits                   | 187 ms                                                                | 188 ms: 1.00x slower                                                          |
| asyncio_websockets         | 507 ms                                                                | 509 ms: 1.01x slower                                                          |
| comprehensions             | 18.2 us                                                               | 18.3 us: 1.01x slower                                                         |
| sympy_str                  | 317 ms                                                                | 319 ms: 1.01x slower                                                          |
| pickle_pure_python         | 338 us                                                                | 340 us: 1.01x slower                                                          |
| sympy_expand               | 535 ms                                                                | 538 ms: 1.01x slower                                                          |
| connected_components       | 491 ms                                                                | 495 ms: 1.01x slower                                                          |
| scimark_lu                 | 130 ms                                                                | 131 ms: 1.01x slower                                                          |
| bpe_tokeniser              | 4.36 sec                                                              | 4.39 sec: 1.01x slower                                                        |
| json_dumps                 | 10.1 ms                                                               | 10.2 ms: 1.01x slower                                                         |
| async_tree_cpu_io_mixed_tg | 582 ms                                                                | 587 ms: 1.01x slower                                                          |
| json                       | 5.39 ms                                                               | 5.44 ms: 1.01x slower                                                         |
| crypto_pyaes               | 88.9 ms                                                               | 89.7 ms: 1.01x slower                                                         |
| logging_format             | 8.21 us                                                               | 8.29 us: 1.01x slower                                                         |
| mdp                        | 1.30 sec                                                              | 1.32 sec: 1.01x slower                                                        |
| pyflate                    | 459 ms                                                                | 465 ms: 1.01x slower                                                          |
| docutils                   | 2.90 sec                                                              | 2.93 sec: 1.01x slower                                                        |
| regex_compile              | 170 ms                                                                | 172 ms: 1.01x slower                                                          |
| 2to3                       | 296 ms                                                                | 300 ms: 1.01x slower                                                          |
| hexiom                     | 6.56 ms                                                               | 6.64 ms: 1.01x slower                                                         |
| xml_etree_generate         | 101 ms                                                                | 102 ms: 1.01x slower                                                          |
| pprint_safe_repr           | 804 ms                                                                | 816 ms: 1.01x slower                                                          |
| sqlglot_v2_optimize        | 57.7 ms                                                               | 58.5 ms: 1.01x slower                                                         |
| sqlglot_v2_parse           | 1.42 ms                                                               | 1.44 ms: 1.01x slower                                                         |
| k_core                     | 2.24 sec                                                              | 2.27 sec: 1.02x slower                                                        |
| telco                      | 176 ms                                                                | 179 ms: 1.02x slower                                                          |
| go                         | 120 ms                                                                | 122 ms: 1.02x slower                                                          |
| async_tree_cpu_io_mixed    | 599 ms                                                                | 609 ms: 1.02x slower                                                          |
| sqlglot_v2_transpile       | 1.74 ms                                                               | 1.77 ms: 1.02x slower                                                         |
| deepcopy_reduce            | 2.92 us                                                               | 2.97 us: 1.02x slower                                                         |
| html5lib                   | 65.9 ms                                                               | 67.0 ms: 1.02x slower                                                         |
| pathlib                    | 17.7 ms                                                               | 18.0 ms: 1.02x slower                                                         |
| pprint_pformat             | 1.66 sec                                                              | 1.69 sec: 1.02x slower                                                        |
| unpickle_pure_python       | 241 us                                                                | 245 us: 1.02x slower                                                          |
| logging_simple             | 7.08 us                                                               | 7.21 us: 1.02x slower                                                         |
| tomli_loads                | 1.95 sec                                                              | 1.99 sec: 1.02x slower                                                        |
| fannkuch                   | 459 ms                                                                | 468 ms: 1.02x slower                                                          |
| sqlglot_v2_normalize       | 114 ms                                                                | 116 ms: 1.02x slower                                                          |
| async_tree_memoization_tg  | 401 ms                                                                | 409 ms: 1.02x slower                                                          |
| float                      | 84.9 ms                                                               | 86.6 ms: 1.02x slower                                                         |
| gc_traversal               | 1.77 ms                                                               | 1.81 ms: 1.02x slower                                                         |
| sphinx                     | 1.10 sec                                                              | 1.12 sec: 1.02x slower                                                        |
| async_tree_none_tg         | 333 ms                                                                | 340 ms: 1.02x slower                                                          |
| xml_etree_process          | 75.0 ms                                                               | 76.8 ms: 1.02x slower                                                         |
| subparsers                 | 10.3 ms                                                               | 10.5 ms: 1.02x slower                                                         |
| richards                   | 52.2 ms                                                               | 53.6 ms: 1.03x slower                                                         |
| create_gc_cycles           | 1.35 ms                                                               | 1.39 ms: 1.03x slower                                                         |
| chaos                      | 60.5 ms                                                               | 62.2 ms: 1.03x slower                                                         |
| async_tree_io_tg           | 689 ms                                                                | 708 ms: 1.03x slower                                                          |
| deepcopy_memo              | 31.1 us                                                               | 31.9 us: 1.03x slower                                                         |
| coverage                   | 115 ms                                                                | 118 ms: 1.03x slower                                                          |
| richards_super             | 59.7 ms                                                               | 61.4 ms: 1.03x slower                                                         |
| django_template            | 41.5 ms                                                               | 42.6 ms: 1.03x slower                                                         |
| pycparser                  | 1.14 sec                                                              | 1.17 sec: 1.03x slower                                                        |
| async_tree_memoization     | 417 ms                                                                | 430 ms: 1.03x slower                                                          |
| deepcopy                   | 264 us                                                                | 272 us: 1.03x slower                                                          |
| spectral_norm              | 106 ms                                                                | 110 ms: 1.03x slower                                                          |
| logging_silent             | 107 ns                                                                | 110 ns: 1.03x slower                                                          |
| async_tree_none            | 341 ms                                                                | 352 ms: 1.03x slower                                                          |
| meteor_contest             | 125 ms                                                                | 130 ms: 1.03x slower                                                          |
| async_tree_io              | 699 ms                                                                | 723 ms: 1.03x slower                                                          |
| deltablue                  | 3.74 ms                                                               | 3.88 ms: 1.04x slower                                                         |
| raytrace                   | 295 ms                                                                | 306 ms: 1.04x slower                                                          |
| coroutines                 | 24.9 ms                                                               | 26.6 ms: 1.07x slower                                                         |
| regex_effbot               | 2.78 ms                                                               | 3.00 ms: 1.08x slower                                                         |
| Geometric mean             | (ref)                                                                 | 1.01x slower                                                                  |

Benchmark hidden because not significant (15): generators, dulwich_log, scimark_monte_carlo, bench_thread_pool, nqueens, xml_etree_iterparse, python_startup_no_site, json_loads, nbody, many_optionals, scimark_sor, sqlite_synth, sympy_sum, typing_runtime_protocols, pylint

- Geometric mean (including insignificant results): 1.013x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x