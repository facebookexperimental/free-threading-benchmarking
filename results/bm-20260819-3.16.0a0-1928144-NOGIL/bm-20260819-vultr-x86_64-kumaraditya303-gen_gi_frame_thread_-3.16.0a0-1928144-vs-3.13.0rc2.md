# Results vs. 3.13.0rc2

- fork: kumaraditya303
- ref: gen_gi_frame_thread_
- machine: linux-x86_64
- commit hash: 1928144
- commit date: 2026-08-19
- overall geometric mean: 1.082x slower
- HPT reliability: 98.14%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260819-vultr-x86_64-kumaraditya303-gen_gi_frame_thread_-3.16.0a0-1928144 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 300 ms: 1.15x slower                                                          |
| docutils       | 2.62 sec                                                     | 2.93 sec: 1.12x slower                                                        |
| Geometric mean | (ref)                                                        | 1.09x slower                                                                  |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260819-vultr-x86_64-kumaraditya303-gen_gi_frame_thread_-3.16.0a0-1928144 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 708 ms: 1.29x faster                                                          |
| async_tree_io              | 876 ms                                                       | 723 ms: 1.21x faster                                                          |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 609 ms: 1.09x faster                                                          |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 587 ms: 1.09x faster                                                          |
| async_tree_memoization     | 461 ms                                                       | 430 ms: 1.07x faster                                                          |
| asyncio_websockets         | 520 ms                                                       | 509 ms: 1.02x faster                                                          |
| async_generators           | 377 ms                                                       | 420 ms: 1.11x slower                                                          |
| coroutines                 | 23.6 ms                                                      | 26.6 ms: 1.13x slower                                                         |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                                  |

Benchmark hidden because not significant (3): async_tree_memoization_tg, async_tree_none, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260819-vultr-x86_64-kumaraditya303-gen_gi_frame_thread_-3.16.0a0-1928144 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 188 ms: 1.15x faster                                                          |
| float          | 77.5 ms                                                      | 86.6 ms: 1.12x slower                                                         |
| nbody          | 85.1 ms                                                      | 120 ms: 1.41x slower                                                          |
| Geometric mean | (ref)                                                        | 1.11x slower                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260819-vultr-x86_64-kumaraditya303-gen_gi_frame_thread_-3.16.0a0-1928144 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                      | 20.1 ms: 1.13x faster                                                         |
| regex_effbot   | 3.08 ms                                                      | 3.00 ms: 1.03x faster                                                         |
| regex_dna      | 180 ms                                                       | 177 ms: 1.02x faster                                                          |
| regex_compile  | 132 ms                                                       | 172 ms: 1.30x slower                                                          |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260819-vultr-x86_64-kumaraditya303-gen_gi_frame_thread_-3.16.0a0-1928144 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 10.2 ms: 1.04x faster                                                         |
| tomli_loads          | 2.01 sec                                                     | 1.99 sec: 1.01x faster                                                        |
| xml_etree_iterparse  | 94.9 ms                                                      | 95.5 ms: 1.01x slower                                                         |
| xml_etree_parse      | 136 ms                                                       | 140 ms: 1.03x slower                                                          |
| json_loads           | 27.0 us                                                      | 30.8 us: 1.14x slower                                                         |
| pickle_pure_python   | 294 us                                                       | 340 us: 1.16x slower                                                          |
| unpickle_pure_python | 210 us                                                       | 245 us: 1.17x slower                                                          |
| xml_etree_generate   | 85.4 ms                                                      | 102 ms: 1.20x slower                                                          |
| xml_etree_process    | 59.3 ms                                                      | 76.8 ms: 1.29x slower                                                         |
| Geometric mean       | (ref)                                                        | 1.10x slower                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260819-vultr-x86_64-kumaraditya303-gen_gi_frame_thread_-3.16.0a0-1928144 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.28 ms: 1.25x slower                                                         |
| python_startup         | 11.0 ms                                                      | 15.8 ms: 1.43x slower                                                         |
| Geometric mean         | (ref)                                                        | 1.34x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260819-vultr-x86_64-kumaraditya303-gen_gi_frame_thread_-3.16.0a0-1928144 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 42.6 ms: 1.25x slower                                                         |
| mako            | 11.3 ms                                                      | 15.9 ms: 1.40x slower                                                         |
| Geometric mean  | (ref)                                                        | 1.32x slower                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260819-vultr-x86_64-kumaraditya303-gen_gi_frame_thread_-3.16.0a0-1928144 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 131 ms: 2.42x faster                                                          |
| mdp                        | 2.36 sec                                                     | 1.32 sec: 1.79x faster                                                        |
| gc_traversal               | 3.14 ms                                                      | 1.81 ms: 1.74x faster                                                         |
| bench_mp_pool              | 11.0 ms                                                      | 6.71 ms: 1.64x faster                                                         |
| deepcopy                   | 355 us                                                       | 272 us: 1.30x faster                                                          |
| async_tree_io_tg           | 913 ms                                                       | 708 ms: 1.29x faster                                                          |
| deepcopy_memo              | 39.1 us                                                      | 31.9 us: 1.22x faster                                                         |
| async_tree_io              | 876 ms                                                       | 723 ms: 1.21x faster                                                          |
| pidigits                   | 217 ms                                                       | 188 ms: 1.15x faster                                                          |
| go                         | 141 ms                                                       | 122 ms: 1.15x faster                                                          |
| sqlite_synth               | 2.21 us                                                      | 1.95 us: 1.13x faster                                                         |
| regex_v8                   | 22.7 ms                                                      | 20.1 ms: 1.13x faster                                                         |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 609 ms: 1.09x faster                                                          |
| scimark_sor                | 134 ms                                                       | 123 ms: 1.09x faster                                                          |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 587 ms: 1.09x faster                                                          |
| async_tree_memoization     | 461 ms                                                       | 430 ms: 1.07x faster                                                          |
| pathlib                    | 19.2 ms                                                      | 18.0 ms: 1.06x faster                                                         |
| typing_runtime_protocols   | 155 us                                                       | 146 us: 1.06x faster                                                          |
| dulwich_log                | 74.8 ms                                                      | 71.2 ms: 1.05x faster                                                         |
| deepcopy_reduce            | 3.11 us                                                      | 2.97 us: 1.05x faster                                                         |
| scimark_fft                | 349 ms                                                       | 336 ms: 1.04x faster                                                          |
| json_dumps                 | 10.5 ms                                                      | 10.2 ms: 1.04x faster                                                         |
| regex_effbot               | 3.08 ms                                                      | 3.00 ms: 1.03x faster                                                         |
| asyncio_websockets         | 520 ms                                                       | 509 ms: 1.02x faster                                                          |
| regex_dna                  | 180 ms                                                       | 177 ms: 1.02x faster                                                          |
| spectral_norm              | 111 ms                                                       | 110 ms: 1.01x faster                                                          |
| bpe_tokeniser              | 4.45 sec                                                     | 4.39 sec: 1.01x faster                                                        |
| tomli_loads                | 2.01 sec                                                     | 1.99 sec: 1.01x faster                                                        |
| xml_etree_iterparse        | 94.9 ms                                                      | 95.5 ms: 1.01x slower                                                         |
| xml_etree_parse            | 136 ms                                                       | 140 ms: 1.03x slower                                                          |
| pyflate                    | 449 ms                                                       | 465 ms: 1.04x slower                                                          |
| create_gc_cycles           | 1.34 ms                                                      | 1.39 ms: 1.04x slower                                                         |
| pycparser                  | 1.12 sec                                                     | 1.17 sec: 1.05x slower                                                        |
| logging_silent             | 103 ns                                                       | 110 ns: 1.08x slower                                                          |
| chaos                      | 57.3 ms                                                      | 62.2 ms: 1.08x slower                                                         |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.16 ms: 1.10x slower                                                         |
| json                       | 4.93 ms                                                      | 5.44 ms: 1.10x slower                                                         |
| pprint_safe_repr           | 738 ms                                                       | 816 ms: 1.11x slower                                                          |
| sympy_integrate            | 19.8 ms                                                      | 22.0 ms: 1.11x slower                                                         |
| hexiom                     | 5.99 ms                                                      | 6.64 ms: 1.11x slower                                                         |
| async_generators           | 377 ms                                                       | 420 ms: 1.11x slower                                                          |
| comprehensions             | 16.5 us                                                      | 18.3 us: 1.11x slower                                                         |
| float                      | 77.5 ms                                                      | 86.6 ms: 1.12x slower                                                         |
| nqueens                    | 78.6 ms                                                      | 88.0 ms: 1.12x slower                                                         |
| docutils                   | 2.62 sec                                                     | 2.93 sec: 1.12x slower                                                        |
| coroutines                 | 23.6 ms                                                      | 26.6 ms: 1.13x slower                                                         |
| pprint_pformat             | 1.50 sec                                                     | 1.69 sec: 1.13x slower                                                        |
| json_loads                 | 27.0 us                                                      | 30.8 us: 1.14x slower                                                         |
| 2to3                       | 260 ms                                                       | 300 ms: 1.15x slower                                                          |
| pickle_pure_python         | 294 us                                                       | 340 us: 1.16x slower                                                          |
| sympy_str                  | 275 ms                                                       | 319 ms: 1.16x slower                                                          |
| generators                 | 28.8 ms                                                      | 33.6 ms: 1.17x slower                                                         |
| scimark_lu                 | 113 ms                                                       | 131 ms: 1.17x slower                                                          |
| unpickle_pure_python       | 210 us                                                       | 245 us: 1.17x slower                                                          |
| logging_simple             | 6.16 us                                                      | 7.21 us: 1.17x slower                                                         |
| sympy_sum                  | 156 ms                                                       | 182 ms: 1.17x slower                                                          |
| sympy_expand               | 457 ms                                                       | 538 ms: 1.18x slower                                                          |
| richards                   | 45.2 ms                                                      | 53.6 ms: 1.18x slower                                                         |
| thrift                     | 778 us                                                       | 925 us: 1.19x slower                                                          |
| richards_super             | 51.6 ms                                                      | 61.4 ms: 1.19x slower                                                         |
| scimark_monte_carlo        | 65.4 ms                                                      | 78.2 ms: 1.20x slower                                                         |
| xml_etree_generate         | 85.4 ms                                                      | 102 ms: 1.20x slower                                                          |
| logging_format             | 6.84 us                                                      | 8.29 us: 1.21x slower                                                         |
| raytrace                   | 253 ms                                                       | 306 ms: 1.21x slower                                                          |
| deltablue                  | 3.12 ms                                                      | 3.88 ms: 1.24x slower                                                         |
| django_template            | 34.1 ms                                                      | 42.6 ms: 1.25x slower                                                         |
| python_startup_no_site     | 7.39 ms                                                      | 9.28 ms: 1.25x slower                                                         |
| fannkuch                   | 370 ms                                                       | 468 ms: 1.27x slower                                                          |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.27x slower                                                          |
| xml_etree_process          | 59.3 ms                                                      | 76.8 ms: 1.29x slower                                                         |
| regex_compile              | 132 ms                                                       | 172 ms: 1.30x slower                                                          |
| crypto_pyaes               | 67.9 ms                                                      | 89.7 ms: 1.32x slower                                                         |
| mako                       | 11.3 ms                                                      | 15.9 ms: 1.40x slower                                                         |
| nbody                      | 85.1 ms                                                      | 120 ms: 1.41x slower                                                          |
| coverage                   | 83.0 ms                                                      | 118 ms: 1.42x slower                                                          |
| python_startup             | 11.0 ms                                                      | 15.8 ms: 1.43x slower                                                         |
| bench_thread_pool          | 919 us                                                       | 1.49 ms: 1.62x slower                                                         |
| telco                      | 7.82 ms                                                      | 179 ms: 22.86x slower                                                         |
| Geometric mean             | (ref)                                                        | 1.08x slower                                                                  |

Benchmark hidden because not significant (4): async_tree_memoization_tg, async_tree_none, html5lib, async_tree_none_tg
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260819-3.16.0a0-1928144-NOGIL/bm-20260819-vultr-x86_64-kumaraditya303-gen_gi_frame_thread_-3.16.0a0-1928144.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.082x slower

# HPT report

- Reliability score: 98.14% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x