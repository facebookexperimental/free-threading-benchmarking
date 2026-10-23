# Results vs. base

- fork: corona10
- ref: MI_SEGMENT_SLICE_SHI
- machine: linux-x86_64
- commit hash: 2e2a547
- commit date: 2026-10-22
- overall geometric mean: 1.004x faster
- HPT reliability: 64.60%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20261022-vultr-x86_64-python-5b55b502221b67660a4d-3.16.0a1+dev-5b55b50 | bm-20261022-vultr-x86_64-corona10-MI_SEGMENT_SLICE_SHI-3.16.0a1+dev-2e2a547 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 292 ms                                                                    | 294 ms: 1.01x slower                                                        |
| docutils       | 2.90 sec                                                                  | 2.86 sec: 1.01x faster                                                      |
| sphinx         | 1.11 sec                                                                  | 1.11 sec: 1.01x slower                                                      |
| Geometric mean | (ref)                                                                     | 1.00x slower                                                                |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20261022-vultr-x86_64-python-5b55b502221b67660a4d-3.16.0a1+dev-5b55b50 | bm-20261022-vultr-x86_64-corona10-MI_SEGMENT_SLICE_SHI-3.16.0a1+dev-2e2a547 |
|----------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 694 ms                                                                    | 577 ms: 1.20x faster                                                        |
| async_tree_cpu_io_mixed_tg | 681 ms                                                                    | 574 ms: 1.19x faster                                                        |
| async_tree_none            | 343 ms                                                                    | 336 ms: 1.02x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                                    | 399 ms: 1.02x faster                                                        |
| async_tree_memoization     | 426 ms                                                                    | 419 ms: 1.02x faster                                                        |
| asyncio_websockets         | 509 ms                                                                    | 502 ms: 1.01x faster                                                        |
| async_tree_io              | 714 ms                                                                    | 706 ms: 1.01x faster                                                        |
| async_tree_io_tg           | 705 ms                                                                    | 699 ms: 1.01x faster                                                        |
| coroutines                 | 26.0 ms                                                                   | 26.1 ms: 1.00x slower                                                       |
| Geometric mean             | (ref)                                                                     | 1.04x faster                                                                |

Benchmark hidden because not significant (2): async_tree_none_tg, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20261022-vultr-x86_64-python-5b55b502221b67660a4d-3.16.0a1+dev-5b55b50 | bm-20261022-vultr-x86_64-corona10-MI_SEGMENT_SLICE_SHI-3.16.0a1+dev-2e2a547 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 231 ms                                                                    | 188 ms: 1.23x faster                                                        |
| nbody          | 116 ms                                                                    | 122 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                                     | 1.06x faster                                                                |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20261022-vultr-x86_64-python-5b55b502221b67660a4d-3.16.0a1+dev-5b55b50 | bm-20261022-vultr-x86_64-corona10-MI_SEGMENT_SLICE_SHI-3.16.0a1+dev-2e2a547 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 186 ms                                                                    | 180 ms: 1.03x faster                                                        |
| regex_v8       | 21.4 ms                                                                   | 21.1 ms: 1.01x faster                                                       |
| regex_effbot   | 2.98 ms                                                                   | 2.96 ms: 1.01x faster                                                       |
| regex_compile  | 170 ms                                                                    | 170 ms: 1.00x faster                                                        |
| Geometric mean | (ref)                                                                     | 1.01x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20261022-vultr-x86_64-python-5b55b502221b67660a4d-3.16.0a1+dev-5b55b50 | bm-20261022-vultr-x86_64-corona10-MI_SEGMENT_SLICE_SHI-3.16.0a1+dev-2e2a547 |
|----------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pickle_pure_python   | 345 us                                                                    | 343 us: 1.01x faster                                                        |
| tomli_loads          | 1.95 sec                                                                  | 1.97 sec: 1.01x slower                                                      |
| unpickle_pure_python | 236 us                                                                    | 237 us: 1.01x slower                                                        |
| xml_etree_iterparse  | 96.6 ms                                                                   | 97.4 ms: 1.01x slower                                                       |
| xml_etree_generate   | 101 ms                                                                    | 102 ms: 1.01x slower                                                        |
| xml_etree_parse      | 143 ms                                                                    | 145 ms: 1.01x slower                                                        |
| json_dumps           | 10.00 ms                                                                  | 10.2 ms: 1.02x slower                                                       |
| Geometric mean       | (ref)                                                                     | 1.01x slower                                                                |

Benchmark hidden because not significant (2): xml_etree_process, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20261022-vultr-x86_64-python-5b55b502221b67660a4d-3.16.0a1+dev-5b55b50 | bm-20261022-vultr-x86_64-corona10-MI_SEGMENT_SLICE_SHI-3.16.0a1+dev-2e2a547 |
|------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 9.13 ms                                                                   | 9.11 ms: 1.00x faster                                                       |
| Geometric mean         | (ref)                                                                     | 1.00x faster                                                                |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20261022-vultr-x86_64-python-5b55b502221b67660a4d-3.16.0a1+dev-5b55b50 | bm-20261022-vultr-x86_64-corona10-MI_SEGMENT_SLICE_SHI-3.16.0a1+dev-2e2a547 |
|----------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 16.0 ms                                                                   | 15.8 ms: 1.01x faster                                                       |
| Geometric mean | (ref)                                                                     | 1.00x faster                                                                |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20261022-vultr-x86_64-python-5b55b502221b67660a4d-3.16.0a1+dev-5b55b50 | bm-20261022-vultr-x86_64-corona10-MI_SEGMENT_SLICE_SHI-3.16.0a1+dev-2e2a547 |
|----------------------------|:-------------------------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits                   | 231 ms                                                                    | 188 ms: 1.23x faster                                                        |
| async_tree_cpu_io_mixed    | 694 ms                                                                    | 577 ms: 1.20x faster                                                        |
| async_tree_cpu_io_mixed_tg | 681 ms                                                                    | 574 ms: 1.19x faster                                                        |
| thrift                     | 948 us                                                                    | 912 us: 1.04x faster                                                        |
| regex_dna                  | 186 ms                                                                    | 180 ms: 1.03x faster                                                        |
| logging_silent             | 110 ns                                                                    | 107 ns: 1.03x faster                                                        |
| async_tree_none            | 343 ms                                                                    | 336 ms: 1.02x faster                                                        |
| pprint_pformat             | 1.72 sec                                                                  | 1.68 sec: 1.02x faster                                                      |
| deepcopy_memo              | 33.2 us                                                                   | 32.6 us: 1.02x faster                                                       |
| async_tree_memoization_tg  | 405 ms                                                                    | 399 ms: 1.02x faster                                                        |
| async_tree_memoization     | 426 ms                                                                    | 419 ms: 1.02x faster                                                        |
| richards                   | 53.0 ms                                                                   | 52.2 ms: 1.02x faster                                                       |
| logging_format             | 8.04 us                                                                   | 7.93 us: 1.02x faster                                                       |
| pyflate                    | 445 ms                                                                    | 439 ms: 1.01x faster                                                        |
| asyncio_websockets         | 509 ms                                                                    | 502 ms: 1.01x faster                                                        |
| docutils                   | 2.90 sec                                                                  | 2.86 sec: 1.01x faster                                                      |
| subparsers                 | 10.3 ms                                                                   | 10.2 ms: 1.01x faster                                                       |
| mako                       | 16.0 ms                                                                   | 15.8 ms: 1.01x faster                                                       |
| mdp                        | 1.29 sec                                                                  | 1.28 sec: 1.01x faster                                                      |
| regex_v8                   | 21.4 ms                                                                   | 21.1 ms: 1.01x faster                                                       |
| sqlite_synth               | 1.93 us                                                                   | 1.91 us: 1.01x faster                                                       |
| pprint_safe_repr           | 825 ms                                                                    | 816 ms: 1.01x faster                                                        |
| async_tree_io              | 714 ms                                                                    | 706 ms: 1.01x faster                                                        |
| go                         | 120 ms                                                                    | 119 ms: 1.01x faster                                                        |
| chaos                      | 60.6 ms                                                                   | 60.0 ms: 1.01x faster                                                       |
| async_tree_io_tg           | 705 ms                                                                    | 699 ms: 1.01x faster                                                        |
| sqlglot_v2_parse           | 1.40 ms                                                                   | 1.39 ms: 1.01x faster                                                       |
| pickle_pure_python         | 345 us                                                                    | 343 us: 1.01x faster                                                        |
| regex_effbot               | 2.98 ms                                                                   | 2.96 ms: 1.01x faster                                                       |
| richards_super             | 60.3 ms                                                                   | 60.0 ms: 1.01x faster                                                       |
| regex_compile              | 170 ms                                                                    | 170 ms: 1.00x faster                                                        |
| fannkuch                   | 469 ms                                                                    | 467 ms: 1.00x faster                                                        |
| python_startup_no_site     | 9.13 ms                                                                   | 9.11 ms: 1.00x faster                                                       |
| bpe_tokeniser              | 4.40 sec                                                                  | 4.40 sec: 1.00x faster                                                      |
| hexiom                     | 6.59 ms                                                                   | 6.58 ms: 1.00x faster                                                       |
| k_core                     | 2.24 sec                                                                  | 2.25 sec: 1.00x slower                                                      |
| coroutines                 | 26.0 ms                                                                   | 26.1 ms: 1.00x slower                                                       |
| 2to3                       | 292 ms                                                                    | 294 ms: 1.01x slower                                                        |
| bench_thread_pool          | 1.39 ms                                                                   | 1.40 ms: 1.01x slower                                                       |
| sympy_expand               | 532 ms                                                                    | 535 ms: 1.01x slower                                                        |
| raytrace                   | 291 ms                                                                    | 293 ms: 1.01x slower                                                        |
| tomli_loads                | 1.95 sec                                                                  | 1.97 sec: 1.01x slower                                                      |
| create_gc_cycles           | 1.33 ms                                                                   | 1.34 ms: 1.01x slower                                                       |
| sphinx                     | 1.11 sec                                                                  | 1.11 sec: 1.01x slower                                                      |
| sqlglot_v2_optimize        | 56.5 ms                                                                   | 56.9 ms: 1.01x slower                                                       |
| unpickle_pure_python       | 236 us                                                                    | 237 us: 1.01x slower                                                        |
| xml_etree_iterparse        | 96.6 ms                                                                   | 97.4 ms: 1.01x slower                                                       |
| scimark_sor                | 119 ms                                                                    | 120 ms: 1.01x slower                                                        |
| meteor_contest             | 124 ms                                                                    | 125 ms: 1.01x slower                                                        |
| coverage                   | 117 ms                                                                    | 119 ms: 1.01x slower                                                        |
| xml_etree_generate         | 101 ms                                                                    | 102 ms: 1.01x slower                                                        |
| bench_mp_pool              | 6.57 ms                                                                   | 6.66 ms: 1.01x slower                                                       |
| xml_etree_parse            | 143 ms                                                                    | 145 ms: 1.01x slower                                                        |
| deepcopy                   | 267 us                                                                    | 271 us: 1.01x slower                                                        |
| gc_traversal               | 1.79 ms                                                                   | 1.81 ms: 1.01x slower                                                       |
| sympy_integrate            | 21.8 ms                                                                   | 22.1 ms: 1.01x slower                                                       |
| sqlglot_v2_normalize       | 113 ms                                                                    | 115 ms: 1.02x slower                                                        |
| sympy_str                  | 316 ms                                                                    | 321 ms: 1.02x slower                                                        |
| many_optionals             | 972 us                                                                    | 989 us: 1.02x slower                                                        |
| json_dumps                 | 10.00 ms                                                                  | 10.2 ms: 1.02x slower                                                       |
| deepcopy_reduce            | 2.91 us                                                                   | 2.96 us: 1.02x slower                                                       |
| shortest_path              | 526 ms                                                                    | 536 ms: 1.02x slower                                                        |
| dulwich_log                | 71.0 ms                                                                   | 72.4 ms: 1.02x slower                                                       |
| comprehensions             | 18.1 us                                                                   | 18.5 us: 1.02x slower                                                       |
| pycparser                  | 1.13 sec                                                                  | 1.16 sec: 1.02x slower                                                      |
| generators                 | 32.8 ms                                                                   | 33.5 ms: 1.02x slower                                                       |
| sympy_sum                  | 180 ms                                                                    | 184 ms: 1.02x slower                                                        |
| nqueens                    | 87.2 ms                                                                   | 89.3 ms: 1.02x slower                                                       |
| spectral_norm              | 101 ms                                                                    | 103 ms: 1.02x slower                                                        |
| scimark_lu                 | 127 ms                                                                    | 131 ms: 1.03x slower                                                        |
| scimark_fft                | 324 ms                                                                    | 338 ms: 1.04x slower                                                        |
| nbody                      | 116 ms                                                                    | 122 ms: 1.05x slower                                                        |
| scimark_sparse_mat_mult    | 4.90 ms                                                                   | 5.19 ms: 1.06x slower                                                       |
| Geometric mean             | (ref)                                                                     | 1.00x faster                                                                |

Benchmark hidden because not significant (19): async_tree_none_tg, logging_simple, telco, pathlib, pylint, xml_etree_process, connected_components, async_generators, deltablue, python_startup, json_loads, float, sqlglot_v2_transpile, typing_runtime_protocols, crypto_pyaes, html5lib, json, scimark_monte_carlo, django_template

- Geometric mean (including insignificant results): 1.004x faster

# HPT report

- Reliability score: 64.60% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.97x