# Results vs. base

- fork: kumaraditya303
- ref: asyncio_perf
- machine: linux-x86_64
- commit hash: 89e46c7
- commit date: 2025-07-15
- overall geometric mean: 1.002x faster
- HPT reliability: 99.19%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250715-vultr-x86_64-python-5b969fd64502a6e2ba65-3.15.0a0-5b969fd | bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 284 ms                                                                | 283 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                                 | 1.00x faster                                                          |

Benchmark hidden because not significant (3): docutils, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250715-vultr-x86_64-python-5b969fd64502a6e2ba65-3.15.0a0-5b969fd | bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7 |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io              | 557 ms                                                                | 540 ms: 1.03x faster                                                  |
| async_tree_memoization     | 318 ms                                                                | 308 ms: 1.03x faster                                                  |
| async_tree_io_tg           | 530 ms                                                                | 514 ms: 1.03x faster                                                  |
| async_tree_memoization_tg  | 290 ms                                                                | 281 ms: 1.03x faster                                                  |
| async_tree_none_tg         | 230 ms                                                                | 224 ms: 1.02x faster                                                  |
| async_tree_none            | 260 ms                                                                | 254 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed    | 509 ms                                                                | 499 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed_tg | 479 ms                                                                | 473 ms: 1.01x faster                                                  |
| async_generators           | 366 ms                                                                | 363 ms: 1.01x faster                                                  |
| coroutines                 | 24.6 ms                                                               | 24.8 ms: 1.01x slower                                                 |
| Geometric mean             | (ref)                                                                 | 1.02x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250715-vultr-x86_64-python-5b969fd64502a6e2ba65-3.15.0a0-5b969fd | bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 68.6 ms                                                               | 68.9 ms: 1.00x slower                                                 |
| nbody          | 122 ms                                                                | 122 ms: 1.00x slower                                                  |
| pidigits       | 188 ms                                                                | 204 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.03x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250715-vultr-x86_64-python-5b969fd64502a6e2ba65-3.15.0a0-5b969fd | bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 143 ms                                                                | 143 ms: 1.00x faster                                                  |
| regex_dna      | 171 ms                                                                | 173 ms: 1.01x slower                                                  |
| regex_v8       | 20.5 ms                                                               | 20.9 ms: 1.02x slower                                                 |
| regex_effbot   | 2.63 ms                                                               | 2.73 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.02x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250715-vultr-x86_64-python-5b969fd64502a6e2ba65-3.15.0a0-5b969fd | bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7 |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.18 sec                                                              | 2.17 sec: 1.00x faster                                                |
| json_loads           | 31.0 us                                                               | 31.1 us: 1.00x slower                                                 |
| xml_etree_generate   | 95.0 ms                                                               | 95.3 ms: 1.00x slower                                                 |
| unpickle_pure_python | 230 us                                                                | 231 us: 1.00x slower                                                  |
| xml_etree_parse      | 129 ms                                                                | 130 ms: 1.00x slower                                                  |
| json_dumps           | 12.1 ms                                                               | 12.2 ms: 1.01x slower                                                 |
| xml_etree_iterparse  | 86.8 ms                                                               | 87.8 ms: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                                 | 1.00x slower                                                          |

Benchmark hidden because not significant (2): pickle_pure_python, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250715-vultr-x86_64-python-5b969fd64502a6e2ba65-3.15.0a0-5b969fd | bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7 |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 9.39 ms                                                               | 9.37 ms: 1.00x faster                                                 |
| python_startup         | 15.8 ms                                                               | 15.8 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                 | 1.00x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250715-vultr-x86_64-python-5b969fd64502a6e2ba65-3.15.0a0-5b969fd | bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text    | 26.7 ms                                                               | 27.0 ms: 1.01x slower                                                 |
| genshi_xml     | 57.5 ms                                                               | 58.4 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                          |

Benchmark hidden because not significant (2): django_template, mako

All benchmarks:
===============

| Benchmark                  | bm-20250715-vultr-x86_64-python-5b969fd64502a6e2ba65-3.15.0a0-5b969fd | bm-20250715-vultr-x86_64-kumaraditya303-asyncio_perf-3.15.0a0-89e46c7 |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| logging_silent             | 105 ns                                                                | 100 ns: 1.05x faster                                                  |
| generators                 | 32.1 ms                                                               | 31.0 ms: 1.04x faster                                                 |
| async_tree_io              | 557 ms                                                                | 540 ms: 1.03x faster                                                  |
| create_gc_cycles           | 1.49 ms                                                               | 1.45 ms: 1.03x faster                                                 |
| async_tree_memoization     | 318 ms                                                                | 308 ms: 1.03x faster                                                  |
| async_tree_io_tg           | 530 ms                                                                | 514 ms: 1.03x faster                                                  |
| async_tree_memoization_tg  | 290 ms                                                                | 281 ms: 1.03x faster                                                  |
| async_tree_none_tg         | 230 ms                                                                | 224 ms: 1.02x faster                                                  |
| gc_traversal               | 1.92 ms                                                               | 1.87 ms: 1.02x faster                                                 |
| async_tree_none            | 260 ms                                                                | 254 ms: 1.02x faster                                                  |
| pycparser                  | 1.18 sec                                                              | 1.15 sec: 1.02x faster                                                |
| async_tree_cpu_io_mixed    | 509 ms                                                                | 499 ms: 1.02x faster                                                  |
| deltablue                  | 3.62 ms                                                               | 3.55 ms: 1.02x faster                                                 |
| fannkuch                   | 465 ms                                                                | 457 ms: 1.02x faster                                                  |
| hexiom                     | 6.45 ms                                                               | 6.35 ms: 1.02x faster                                                 |
| pyflate                    | 469 ms                                                                | 462 ms: 1.02x faster                                                  |
| pprint_pformat             | 1.61 sec                                                              | 1.59 sec: 1.01x faster                                                |
| async_tree_cpu_io_mixed_tg | 479 ms                                                                | 473 ms: 1.01x faster                                                  |
| deepcopy                   | 297 us                                                                | 293 us: 1.01x faster                                                  |
| thrift                     | 877 us                                                                | 866 us: 1.01x faster                                                  |
| pprint_safe_repr           | 783 ms                                                                | 774 ms: 1.01x faster                                                  |
| richards                   | 51.2 ms                                                               | 50.8 ms: 1.01x faster                                                 |
| typing_runtime_protocols   | 190 us                                                                | 189 us: 1.01x faster                                                  |
| async_generators           | 366 ms                                                                | 363 ms: 1.01x faster                                                  |
| json                       | 5.34 ms                                                               | 5.30 ms: 1.01x faster                                                 |
| scimark_lu                 | 129 ms                                                                | 128 ms: 1.01x faster                                                  |
| mdp                        | 1.32 sec                                                              | 1.31 sec: 1.01x faster                                                |
| deepcopy_memo              | 34.8 us                                                               | 34.6 us: 1.01x faster                                                 |
| bench_mp_pool              | 109 ms                                                                | 108 ms: 1.01x faster                                                  |
| tomli_loads                | 2.18 sec                                                              | 2.17 sec: 1.00x faster                                                |
| sympy_sum                  | 180 ms                                                                | 179 ms: 1.00x faster                                                  |
| scimark_monte_carlo        | 77.5 ms                                                               | 77.2 ms: 1.00x faster                                                 |
| sympy_integrate            | 22.0 ms                                                               | 21.9 ms: 1.00x faster                                                 |
| k_core                     | 2.24 sec                                                              | 2.23 sec: 1.00x faster                                                |
| 2to3                       | 284 ms                                                                | 283 ms: 1.00x faster                                                  |
| regex_compile              | 143 ms                                                                | 143 ms: 1.00x faster                                                  |
| python_startup_no_site     | 9.39 ms                                                               | 9.37 ms: 1.00x faster                                                 |
| python_startup             | 15.8 ms                                                               | 15.8 ms: 1.00x faster                                                 |
| json_loads                 | 31.0 us                                                               | 31.1 us: 1.00x slower                                                 |
| scimark_sparse_mat_mult    | 5.28 ms                                                               | 5.29 ms: 1.00x slower                                                 |
| crypto_pyaes               | 85.7 ms                                                               | 85.9 ms: 1.00x slower                                                 |
| float                      | 68.6 ms                                                               | 68.9 ms: 1.00x slower                                                 |
| xml_etree_generate         | 95.0 ms                                                               | 95.3 ms: 1.00x slower                                                 |
| nbody                      | 122 ms                                                                | 122 ms: 1.00x slower                                                  |
| scimark_fft                | 362 ms                                                                | 363 ms: 1.00x slower                                                  |
| unpickle_pure_python       | 230 us                                                                | 231 us: 1.00x slower                                                  |
| chaos                      | 62.7 ms                                                               | 63.0 ms: 1.00x slower                                                 |
| xml_etree_parse            | 129 ms                                                                | 130 ms: 1.00x slower                                                  |
| comprehensions             | 17.5 us                                                               | 17.6 us: 1.01x slower                                                 |
| logging_simple             | 6.99 us                                                               | 7.03 us: 1.01x slower                                                 |
| sqlglot_v2_normalize       | 115 ms                                                                | 116 ms: 1.01x slower                                                  |
| telco                      | 176 ms                                                                | 177 ms: 1.01x slower                                                  |
| deepcopy_reduce            | 2.99 us                                                               | 3.01 us: 1.01x slower                                                 |
| json_dumps                 | 12.1 ms                                                               | 12.2 ms: 1.01x slower                                                 |
| nqueens                    | 88.0 ms                                                               | 88.7 ms: 1.01x slower                                                 |
| coroutines                 | 24.6 ms                                                               | 24.8 ms: 1.01x slower                                                 |
| xml_etree_iterparse        | 86.8 ms                                                               | 87.8 ms: 1.01x slower                                                 |
| genshi_text                | 26.7 ms                                                               | 27.0 ms: 1.01x slower                                                 |
| regex_dna                  | 171 ms                                                                | 173 ms: 1.01x slower                                                  |
| meteor_contest             | 119 ms                                                                | 120 ms: 1.01x slower                                                  |
| genshi_xml                 | 57.5 ms                                                               | 58.4 ms: 1.01x slower                                                 |
| regex_v8                   | 20.5 ms                                                               | 20.9 ms: 1.02x slower                                                 |
| regex_effbot               | 2.63 ms                                                               | 2.73 ms: 1.04x slower                                                 |
| pidigits                   | 188 ms                                                                | 204 ms: 1.09x slower                                                  |
| Geometric mean             | (ref)                                                                 | 1.00x faster                                                          |

Benchmark hidden because not significant (30): many_optionals, html5lib, sqlglot_v2_parse, pylint, django_template, richards_super, shortest_path, scimark_sor, spectral_norm, sympy_str, pickle_pure_python, sympy_expand, coverage, mako, go, bpe_tokeniser, xml_etree_process, asyncio_websockets, sqlglot_v2_transpile, bench_thread_pool, sqlglot_v2_optimize, pathlib, dulwich_log, logging_format, subparsers, sphinx, raytrace, sqlite_synth, connected_components, docutils

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 99.19% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x