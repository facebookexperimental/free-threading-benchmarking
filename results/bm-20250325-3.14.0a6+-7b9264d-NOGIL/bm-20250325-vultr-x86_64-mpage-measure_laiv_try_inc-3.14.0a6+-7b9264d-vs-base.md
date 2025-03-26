# Results vs. base

- fork: mpage
- ref: measure_laiv_try_inc
- machine: linux-x86_64
- commit hash: 7b9264d
- commit date: 2025-03-25
- overall geometric mean: 1.002x slower
- HPT reliability: 91.35%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6+-7bb41ae | bm-20250325-vultr-x86_64-mpage-measure_laiv_try_inc-3.14.0a6+-7b9264d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 298 ms                                                                 | 299 ms: 1.00x slower                                                  |
| html5lib       | 70.5 ms                                                                | 69.5 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6+-7bb41ae | bm-20250325-vultr-x86_64-mpage-measure_laiv_try_inc-3.14.0a6+-7b9264d |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization     | 333 ms                                                                 | 330 ms: 1.01x faster                                                  |
| async_tree_memoization_tg  | 298 ms                                                                 | 300 ms: 1.01x slower                                                  |
| async_tree_io_tg           | 550 ms                                                                 | 554 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed    | 520 ms                                                                 | 539 ms: 1.04x slower                                                  |
| async_tree_cpu_io_mixed_tg | 487 ms                                                                 | 505 ms: 1.04x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (6): async_tree_none, async_generators, async_tree_io, asyncio_websockets, coroutines, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6+-7bb41ae | bm-20250325-vultr-x86_64-mpage-measure_laiv_try_inc-3.14.0a6+-7b9264d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 139 ms                                                                 | 136 ms: 1.02x faster                                                  |
| pidigits       | 196 ms                                                                 | 211 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6+-7bb41ae | bm-20250325-vultr-x86_64-mpage-measure_laiv_try_inc-3.14.0a6+-7b9264d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.85 ms                                                                | 2.68 ms: 1.06x faster                                                 |
| regex_dna      | 175 ms                                                                 | 176 ms: 1.01x slower                                                  |
| regex_compile  | 156 ms                                                                 | 158 ms: 1.01x slower                                                  |
| regex_v8       | 21.5 ms                                                                | 22.0 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6+-7bb41ae | bm-20250325-vultr-x86_64-mpage-measure_laiv_try_inc-3.14.0a6+-7b9264d |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_loads           | 29.6 us                                                                | 29.4 us: 1.01x faster                                                 |
| unpickle_pure_python | 257 us                                                                 | 257 us: 1.00x faster                                                  |
| xml_etree_parse      | 129 ms                                                                 | 130 ms: 1.00x slower                                                  |
| tomli_loads          | 2.34 sec                                                               | 2.35 sec: 1.00x slower                                                |
| pickle_pure_python   | 357 us                                                                 | 360 us: 1.01x slower                                                  |
| xml_etree_iterparse  | 87.7 ms                                                                | 88.6 ms: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (3): xml_etree_generate, json_dumps, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6+-7bb41ae | bm-20250325-vultr-x86_64-mpage-measure_laiv_try_inc-3.14.0a6+-7b9264d |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 15.7 ms                                                                | 15.7 ms: 1.00x slower                                                 |
| python_startup_no_site | 11.1 ms                                                                | 11.1 ms: 1.00x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6+-7bb41ae | bm-20250325-vultr-x86_64-mpage-measure_laiv_try_inc-3.14.0a6+-7b9264d |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 60.4 ms                                                                | 59.9 ms: 1.01x faster                                                 |
| genshi_text     | 28.4 ms                                                                | 28.6 ms: 1.01x slower                                                 |
| django_template | 42.7 ms                                                                | 43.3 ms: 1.01x slower                                                 |
| mako            | 15.7 ms                                                                | 16.0 ms: 1.02x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250326-vultr-x86_64-python-7bb41aef4b7b8f3c3f07-3.14.0a6+-7bb41ae | bm-20250325-vultr-x86_64-mpage-measure_laiv_try_inc-3.14.0a6+-7b9264d |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot               | 2.85 ms                                                                | 2.68 ms: 1.06x faster                                                 |
| pyflate                    | 514 ms                                                                 | 497 ms: 1.03x faster                                                  |
| subparsers                 | 25.8 ms                                                                | 25.2 ms: 1.02x faster                                                 |
| logging_silent             | 114 ns                                                                 | 111 ns: 1.02x faster                                                  |
| nbody                      | 139 ms                                                                 | 136 ms: 1.02x faster                                                  |
| html5lib                   | 70.5 ms                                                                | 69.5 ms: 1.01x faster                                                 |
| telco                      | 9.10 ms                                                                | 8.99 ms: 1.01x faster                                                 |
| scimark_lu                 | 144 ms                                                                 | 142 ms: 1.01x faster                                                  |
| scimark_sor                | 139 ms                                                                 | 138 ms: 1.01x faster                                                  |
| coverage                   | 109 ms                                                                 | 108 ms: 1.01x faster                                                  |
| genshi_xml                 | 60.4 ms                                                                | 59.9 ms: 1.01x faster                                                 |
| async_tree_memoization     | 333 ms                                                                 | 330 ms: 1.01x faster                                                  |
| fannkuch                   | 498 ms                                                                 | 494 ms: 1.01x faster                                                  |
| json_loads                 | 29.6 us                                                                | 29.4 us: 1.01x faster                                                 |
| mdp                        | 2.62 sec                                                               | 2.61 sec: 1.01x faster                                                |
| chaos                      | 69.0 ms                                                                | 68.8 ms: 1.00x faster                                                 |
| scimark_sparse_mat_mult    | 5.72 ms                                                                | 5.70 ms: 1.00x faster                                                 |
| unpickle_pure_python       | 257 us                                                                 | 257 us: 1.00x faster                                                  |
| bench_thread_pool          | 3.16 ms                                                                | 3.16 ms: 1.00x slower                                                 |
| python_startup             | 15.7 ms                                                                | 15.7 ms: 1.00x slower                                                 |
| python_startup_no_site     | 11.1 ms                                                                | 11.1 ms: 1.00x slower                                                 |
| 2to3                       | 298 ms                                                                 | 299 ms: 1.00x slower                                                  |
| xml_etree_parse            | 129 ms                                                                 | 130 ms: 1.00x slower                                                  |
| tomli_loads                | 2.34 sec                                                               | 2.35 sec: 1.00x slower                                                |
| deepcopy                   | 313 us                                                                 | 314 us: 1.00x slower                                                  |
| regex_dna                  | 175 ms                                                                 | 176 ms: 1.01x slower                                                  |
| nqueens                    | 96.8 ms                                                                | 97.3 ms: 1.01x slower                                                 |
| bpe_tokeniser              | 4.85 sec                                                               | 4.88 sec: 1.01x slower                                                |
| pycparser                  | 1.18 sec                                                               | 1.19 sec: 1.01x slower                                                |
| many_optionals             | 1.17 ms                                                                | 1.17 ms: 1.01x slower                                                 |
| pprint_safe_repr           | 837 ms                                                                 | 842 ms: 1.01x slower                                                  |
| hexiom                     | 7.63 ms                                                                | 7.68 ms: 1.01x slower                                                 |
| async_tree_memoization_tg  | 298 ms                                                                 | 300 ms: 1.01x slower                                                  |
| richards_super             | 64.1 ms                                                                | 64.6 ms: 1.01x slower                                                 |
| regex_compile              | 156 ms                                                                 | 158 ms: 1.01x slower                                                  |
| crypto_pyaes               | 88.2 ms                                                                | 88.9 ms: 1.01x slower                                                 |
| genshi_text                | 28.4 ms                                                                | 28.6 ms: 1.01x slower                                                 |
| sqlglot_v2_parse           | 1.59 ms                                                                | 1.60 ms: 1.01x slower                                                 |
| async_tree_io_tg           | 550 ms                                                                 | 554 ms: 1.01x slower                                                  |
| connected_components       | 509 ms                                                                 | 513 ms: 1.01x slower                                                  |
| pprint_pformat             | 1.73 sec                                                               | 1.75 sec: 1.01x slower                                                |
| pickle_pure_python         | 357 us                                                                 | 360 us: 1.01x slower                                                  |
| xml_etree_iterparse        | 87.7 ms                                                                | 88.6 ms: 1.01x slower                                                 |
| gc_traversal               | 1.80 ms                                                                | 1.82 ms: 1.01x slower                                                 |
| shortest_path              | 548 ms                                                                 | 554 ms: 1.01x slower                                                  |
| richards                   | 55.1 ms                                                                | 55.8 ms: 1.01x slower                                                 |
| django_template            | 42.7 ms                                                                | 43.3 ms: 1.01x slower                                                 |
| create_gc_cycles           | 1.36 ms                                                                | 1.38 ms: 1.01x slower                                                 |
| pathlib                    | 19.8 ms                                                                | 20.1 ms: 1.01x slower                                                 |
| comprehensions             | 20.6 us                                                                | 20.9 us: 1.02x slower                                                 |
| spectral_norm              | 112 ms                                                                 | 114 ms: 1.02x slower                                                  |
| regex_v8                   | 21.5 ms                                                                | 22.0 ms: 1.02x slower                                                 |
| mako                       | 15.7 ms                                                                | 16.0 ms: 1.02x slower                                                 |
| sqlite_synth               | 2.01 us                                                                | 2.06 us: 1.02x slower                                                 |
| async_tree_cpu_io_mixed    | 520 ms                                                                 | 539 ms: 1.04x slower                                                  |
| async_tree_cpu_io_mixed_tg | 487 ms                                                                 | 505 ms: 1.04x slower                                                  |
| pidigits                   | 196 ms                                                                 | 211 ms: 1.08x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (39): logging_format, async_tree_none, json, generators, sqlalchemy_imperative, xml_etree_generate, go, sphinx, thrift, meteor_contest, sympy_expand, deepcopy_reduce, async_generators, json_dumps, async_tree_io, sympy_sum, sqlalchemy_declarative, xml_etree_process, k_core, raytrace, deltablue, docutils, typing_runtime_protocols, float, pylint, sympy_integrate, scimark_fft, dulwich_log, sqlglot_v2_normalize, sqlglot_v2_optimize, deepcopy_memo, scimark_monte_carlo, sympy_str, asyncio_websockets, bench_mp_pool, coroutines, logging_simple, async_tree_none_tg, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.002x slower

# HPT report

- Reliability score: 91.35% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x