# Results vs. base

- fork: colesbury
- ref: gh_120321_gen_send
- machine: linux-x86_64
- commit hash: b67dc73
- commit date: 2025-03-13
- overall geometric mean: 1.004x slower
- HPT reliability: 96.27%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (4): 2to3, docutils, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250313-vultr-x86_64-python-c5abded09995f208b21e-3.14.0a5+-c5abded | bm-20250313-vultr-x86_64-colesbury-gh_120321_gen_send-3.14.0a5+-b67dc73 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 498 ms                                                                 | 490 ms: 1.01x faster                                                    |
| async_tree_cpu_io_mixed    | 529 ms                                                                 | 523 ms: 1.01x faster                                                    |
| async_tree_io              | 581 ms                                                                 | 587 ms: 1.01x slower                                                    |
| async_tree_memoization_tg  | 304 ms                                                                 | 307 ms: 1.01x slower                                                    |
| async_generators           | 376 ms                                                                 | 380 ms: 1.01x slower                                                    |
| async_tree_io_tg           | 549 ms                                                                 | 557 ms: 1.01x slower                                                    |
| coroutines                 | 23.8 ms                                                                | 24.3 ms: 1.02x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (4): async_tree_none, async_tree_memoization, asyncio_websockets, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250313-vultr-x86_64-python-c5abded09995f208b21e-3.14.0a5+-c5abded | bm-20250313-vultr-x86_64-colesbury-gh_120321_gen_send-3.14.0a5+-b67dc73 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 77.4 ms                                                                | 77.8 ms: 1.01x slower                                                   |
| nbody          | 135 ms                                                                 | 136 ms: 1.01x slower                                                    |
| pidigits       | 193 ms                                                                 | 199 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250313-vultr-x86_64-python-c5abded09995f208b21e-3.14.0a5+-c5abded | bm-20250313-vultr-x86_64-colesbury-gh_120321_gen_send-3.14.0a5+-b67dc73 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 158 ms                                                                 | 156 ms: 1.01x faster                                                    |
| regex_effbot   | 2.72 ms                                                                | 2.71 ms: 1.01x faster                                                   |
| regex_v8       | 23.2 ms                                                                | 23.7 ms: 1.02x slower                                                   |
| regex_dna      | 171 ms                                                                 | 182 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250313-vultr-x86_64-python-c5abded09995f208b21e-3.14.0a5+-c5abded | bm-20250313-vultr-x86_64-colesbury-gh_120321_gen_send-3.14.0a5+-b67dc73 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_loads           | 29.9 us                                                                | 29.3 us: 1.02x faster                                                   |
| unpickle_pure_python | 257 us                                                                 | 252 us: 1.02x faster                                                    |
| pickle_pure_python   | 363 us                                                                 | 356 us: 1.02x faster                                                    |
| json_dumps           | 12.9 ms                                                                | 12.7 ms: 1.01x faster                                                   |
| xml_etree_generate   | 96.2 ms                                                                | 96.9 ms: 1.01x slower                                                   |
| xml_etree_process    | 70.3 ms                                                                | 70.8 ms: 1.01x slower                                                   |
| xml_etree_parse      | 128 ms                                                                 | 130 ms: 1.01x slower                                                    |
| xml_etree_iterparse  | 88.3 ms                                                                | 89.9 ms: 1.02x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250313-vultr-x86_64-python-c5abded09995f208b21e-3.14.0a5+-c5abded | bm-20250313-vultr-x86_64-colesbury-gh_120321_gen_send-3.14.0a5+-b67dc73 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 15.8 ms                                                                | 15.8 ms: 1.00x faster                                                   |
| python_startup_no_site | 11.2 ms                                                                | 11.1 ms: 1.00x faster                                                   |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250313-vultr-x86_64-python-c5abded09995f208b21e-3.14.0a5+-c5abded | bm-20250313-vultr-x86_64-colesbury-gh_120321_gen_send-3.14.0a5+-b67dc73 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako           | 15.9 ms                                                                | 15.8 ms: 1.01x faster                                                   |
| genshi_xml     | 60.4 ms                                                                | 61.8 ms: 1.02x slower                                                   |
| genshi_text    | 28.1 ms                                                                | 29.3 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20250313-vultr-x86_64-python-c5abded09995f208b21e-3.14.0a5+-c5abded | bm-20250313-vultr-x86_64-colesbury-gh_120321_gen_send-3.14.0a5+-b67dc73 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| telco                      | 9.05 ms                                                                | 8.77 ms: 1.03x faster                                                   |
| json_loads                 | 29.9 us                                                                | 29.3 us: 1.02x faster                                                   |
| unpickle_pure_python       | 257 us                                                                 | 252 us: 1.02x faster                                                    |
| create_gc_cycles           | 1.33 ms                                                                | 1.30 ms: 1.02x faster                                                   |
| deepcopy                   | 312 us                                                                 | 306 us: 1.02x faster                                                    |
| pickle_pure_python         | 363 us                                                                 | 356 us: 1.02x faster                                                    |
| logging_silent             | 115 ns                                                                 | 113 ns: 1.02x faster                                                    |
| deepcopy_reduce            | 3.19 us                                                                | 3.14 us: 1.02x faster                                                   |
| pprint_pformat             | 1.75 sec                                                               | 1.72 sec: 1.02x faster                                                  |
| async_tree_cpu_io_mixed_tg | 498 ms                                                                 | 490 ms: 1.01x faster                                                    |
| json_dumps                 | 12.9 ms                                                                | 12.7 ms: 1.01x faster                                                   |
| go                         | 144 ms                                                                 | 142 ms: 1.01x faster                                                    |
| pprint_safe_repr           | 848 ms                                                                 | 837 ms: 1.01x faster                                                    |
| deltablue                  | 3.93 ms                                                                | 3.88 ms: 1.01x faster                                                   |
| gc_traversal               | 1.74 ms                                                                | 1.72 ms: 1.01x faster                                                   |
| regex_compile              | 158 ms                                                                 | 156 ms: 1.01x faster                                                    |
| async_tree_cpu_io_mixed    | 529 ms                                                                 | 523 ms: 1.01x faster                                                    |
| chaos                      | 69.8 ms                                                                | 69.2 ms: 1.01x faster                                                   |
| raytrace                   | 324 ms                                                                 | 321 ms: 1.01x faster                                                    |
| regex_effbot               | 2.72 ms                                                                | 2.71 ms: 1.01x faster                                                   |
| deepcopy_memo              | 38.9 us                                                                | 38.7 us: 1.01x faster                                                   |
| mako                       | 15.9 ms                                                                | 15.8 ms: 1.01x faster                                                   |
| pycparser                  | 1.20 sec                                                               | 1.20 sec: 1.00x faster                                                  |
| pathlib                    | 19.5 ms                                                                | 19.5 ms: 1.00x faster                                                   |
| python_startup             | 15.8 ms                                                                | 15.8 ms: 1.00x faster                                                   |
| python_startup_no_site     | 11.2 ms                                                                | 11.1 ms: 1.00x faster                                                   |
| crypto_pyaes               | 88.5 ms                                                                | 88.2 ms: 1.00x faster                                                   |
| bpe_tokeniser              | 4.87 sec                                                               | 4.86 sec: 1.00x faster                                                  |
| mdp                        | 2.79 sec                                                               | 2.80 sec: 1.00x slower                                                  |
| k_core                     | 2.31 sec                                                               | 2.32 sec: 1.00x slower                                                  |
| scimark_sor                | 135 ms                                                                 | 136 ms: 1.00x slower                                                    |
| fannkuch                   | 493 ms                                                                 | 495 ms: 1.00x slower                                                    |
| bench_thread_pool          | 3.15 ms                                                                | 3.17 ms: 1.00x slower                                                   |
| float                      | 77.4 ms                                                                | 77.8 ms: 1.01x slower                                                   |
| xml_etree_generate         | 96.2 ms                                                                | 96.9 ms: 1.01x slower                                                   |
| xml_etree_process          | 70.3 ms                                                                | 70.8 ms: 1.01x slower                                                   |
| nbody                      | 135 ms                                                                 | 136 ms: 1.01x slower                                                    |
| sqlglot_parse              | 1.60 ms                                                                | 1.61 ms: 1.01x slower                                                   |
| subparsers                 | 25.3 ms                                                                | 25.5 ms: 1.01x slower                                                   |
| scimark_fft                | 392 ms                                                                 | 395 ms: 1.01x slower                                                    |
| thrift                     | 878 us                                                                 | 886 us: 1.01x slower                                                    |
| async_tree_io              | 581 ms                                                                 | 587 ms: 1.01x slower                                                    |
| async_tree_memoization_tg  | 304 ms                                                                 | 307 ms: 1.01x slower                                                    |
| async_generators           | 376 ms                                                                 | 380 ms: 1.01x slower                                                    |
| sympy_sum                  | 186 ms                                                                 | 188 ms: 1.01x slower                                                    |
| scimark_lu                 | 140 ms                                                                 | 142 ms: 1.01x slower                                                    |
| xml_etree_parse            | 128 ms                                                                 | 130 ms: 1.01x slower                                                    |
| logging_simple             | 7.16 us                                                                | 7.26 us: 1.01x slower                                                   |
| pyflate                    | 501 ms                                                                 | 508 ms: 1.01x slower                                                    |
| async_tree_io_tg           | 549 ms                                                                 | 557 ms: 1.01x slower                                                    |
| nqueens                    | 99.4 ms                                                                | 101 ms: 1.02x slower                                                    |
| xml_etree_iterparse        | 88.3 ms                                                                | 89.9 ms: 1.02x slower                                                   |
| meteor_contest             | 131 ms                                                                 | 134 ms: 1.02x slower                                                    |
| coroutines                 | 23.8 ms                                                                | 24.3 ms: 1.02x slower                                                   |
| scimark_sparse_mat_mult    | 5.68 ms                                                                | 5.79 ms: 1.02x slower                                                   |
| genshi_xml                 | 60.4 ms                                                                | 61.8 ms: 1.02x slower                                                   |
| sqlalchemy_declarative     | 158 ms                                                                 | 162 ms: 1.02x slower                                                    |
| regex_v8                   | 23.2 ms                                                                | 23.7 ms: 1.02x slower                                                   |
| hexiom                     | 7.63 ms                                                                | 7.82 ms: 1.03x slower                                                   |
| pidigits                   | 193 ms                                                                 | 199 ms: 1.03x slower                                                    |
| genshi_text                | 28.1 ms                                                                | 29.3 ms: 1.04x slower                                                   |
| regex_dna                  | 171 ms                                                                 | 182 ms: 1.06x slower                                                    |
| generators                 | 31.4 ms                                                                | 36.2 ms: 1.15x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (33): sqlite_synth, sqlglot_normalize, sympy_expand, html5lib, dulwich_log, bench_mp_pool, async_tree_none, docutils, richards, django_template, logging_format, scimark_monte_carlo, sympy_integrate, richards_super, sympy_str, connected_components, 2to3, spectral_norm, async_tree_memoization, typing_runtime_protocols, sqlglot_optimize, many_optionals, asyncio_websockets, tomli_loads, pylint, sqlalchemy_imperative, shortest_path, comprehensions, coverage, async_tree_none_tg, sphinx, sqlglot_transpile, json

- Geometric mean (including insignificant results): 1.004x slower

# HPT report

- Reliability score: 96.27% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x