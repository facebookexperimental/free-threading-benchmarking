# Results vs. base

- fork: DinoV
- ref: lazy_imports
- machine: linux-x86_64
- commit hash: 27836e5
- commit date: 2025-09-22
- overall geometric mean: 1.005x slower
- HPT reliability: 98.52%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250922-vultr-x86_64-python-f0d8583303d28a5312e4-3.15.0a0-f0d8583 | bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| coroutines                 | 24.6 ms                                                               | 24.7 ms: 1.00x slower                                        |
| async_tree_cpu_io_mixed_tg | 504 ms                                                                | 508 ms: 1.01x slower                                         |
| async_generators           | 335 ms                                                                | 342 ms: 1.02x slower                                         |
| Geometric mean             | (ref)                                                                 | 1.00x faster                                                 |

Benchmark hidden because not significant (8): async_tree_io_tg, async_tree_memoization, async_tree_none, async_tree_io, asyncio_websockets, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250922-vultr-x86_64-python-f0d8583303d28a5312e4-3.15.0a0-f0d8583 | bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| pidigits       | 210 ms                                                                | 197 ms: 1.07x faster                                         |
| nbody          | 91.9 ms                                                               | 90.7 ms: 1.01x faster                                        |
| float          | 71.8 ms                                                               | 72.4 ms: 1.01x slower                                        |
| Geometric mean | (ref)                                                                 | 1.02x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250922-vultr-x86_64-python-f0d8583303d28a5312e4-3.15.0a0-f0d8583 | bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_v8       | 21.4 ms                                                               | 21.1 ms: 1.02x faster                                        |
| regex_compile  | 123 ms                                                                | 124 ms: 1.01x slower                                         |
| regex_dna      | 169 ms                                                                | 172 ms: 1.02x slower                                         |
| regex_effbot   | 2.56 ms                                                               | 2.67 ms: 1.04x slower                                        |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250922-vultr-x86_64-python-f0d8583303d28a5312e4-3.15.0a0-f0d8583 | bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5 |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| xml_etree_process    | 58.7 ms                                                               | 58.2 ms: 1.01x faster                                        |
| unpickle_pure_python | 209 us                                                                | 208 us: 1.00x faster                                         |
| xml_etree_iterparse  | 92.6 ms                                                               | 93.2 ms: 1.01x slower                                        |
| json_dumps           | 9.50 ms                                                               | 9.58 ms: 1.01x slower                                        |
| xml_etree_parse      | 132 ms                                                                | 134 ms: 1.01x slower                                         |
| tomli_loads          | 1.90 sec                                                              | 1.93 sec: 1.01x slower                                       |
| json_loads           | 27.7 us                                                               | 28.1 us: 1.01x slower                                        |
| pickle_pure_python   | 303 us                                                                | 307 us: 1.01x slower                                         |
| Geometric mean       | (ref)                                                                 | 1.01x slower                                                 |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250922-vultr-x86_64-python-f0d8583303d28a5312e4-3.15.0a0-f0d8583 | bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5 |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 12.6 ms                                                               | 12.6 ms: 1.00x slower                                        |
| python_startup_no_site | 7.25 ms                                                               | 7.27 ms: 1.00x slower                                        |
| Geometric mean         | (ref)                                                                 | 1.00x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250922-vultr-x86_64-python-f0d8583303d28a5312e4-3.15.0a0-f0d8583 | bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_text    | 20.2 ms                                                               | 20.6 ms: 1.02x slower                                        |
| Geometric mean | (ref)                                                                 | 1.00x slower                                                 |

Benchmark hidden because not significant (2): genshi_xml, django_template

All benchmarks:
===============

| Benchmark                  | bm-20250922-vultr-x86_64-python-f0d8583303d28a5312e4-3.15.0a0-f0d8583 | bm-20250922-vultr-x86_64-DinoV-lazy_imports-3.15.0a0-27836e5 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| pidigits                   | 210 ms                                                                | 197 ms: 1.07x faster                                         |
| regex_v8                   | 21.4 ms                                                               | 21.1 ms: 1.02x faster                                        |
| scimark_lu                 | 111 ms                                                                | 110 ms: 1.01x faster                                         |
| nbody                      | 91.9 ms                                                               | 90.7 ms: 1.01x faster                                        |
| logging_format             | 6.64 us                                                               | 6.56 us: 1.01x faster                                        |
| sqlite_synth               | 2.28 us                                                               | 2.26 us: 1.01x faster                                        |
| pathlib                    | 18.2 ms                                                               | 18.0 ms: 1.01x faster                                        |
| xml_etree_process          | 58.7 ms                                                               | 58.2 ms: 1.01x faster                                        |
| pprint_safe_repr           | 700 ms                                                                | 694 ms: 1.01x faster                                         |
| deepcopy_memo              | 26.5 us                                                               | 26.3 us: 1.01x faster                                        |
| dulwich_log                | 66.7 ms                                                               | 66.2 ms: 1.01x faster                                        |
| spectral_norm              | 95.4 ms                                                               | 94.7 ms: 1.01x faster                                        |
| deepcopy_reduce            | 2.60 us                                                               | 2.58 us: 1.01x faster                                        |
| unpickle_pure_python       | 209 us                                                                | 208 us: 1.00x faster                                         |
| coverage                   | 82.2 ms                                                               | 81.8 ms: 1.00x faster                                        |
| telco                      | 158 ms                                                                | 158 ms: 1.00x faster                                         |
| python_startup             | 12.6 ms                                                               | 12.6 ms: 1.00x slower                                        |
| coroutines                 | 24.6 ms                                                               | 24.7 ms: 1.00x slower                                        |
| raytrace                   | 252 ms                                                                | 253 ms: 1.00x slower                                         |
| python_startup_no_site     | 7.25 ms                                                               | 7.27 ms: 1.00x slower                                        |
| bench_thread_pool          | 1.01 ms                                                               | 1.01 ms: 1.00x slower                                        |
| sympy_integrate            | 18.7 ms                                                               | 18.8 ms: 1.00x slower                                        |
| scimark_sor                | 109 ms                                                                | 110 ms: 1.01x slower                                         |
| sqlglot_v2_normalize       | 99.2 ms                                                               | 99.7 ms: 1.01x slower                                        |
| xml_etree_iterparse        | 92.6 ms                                                               | 93.2 ms: 1.01x slower                                        |
| scimark_fft                | 335 ms                                                                | 337 ms: 1.01x slower                                         |
| bench_mp_pool              | 12.4 ms                                                               | 12.5 ms: 1.01x slower                                        |
| go                         | 105 ms                                                                | 105 ms: 1.01x slower                                         |
| hexiom                     | 5.62 ms                                                               | 5.66 ms: 1.01x slower                                        |
| fannkuch                   | 376 ms                                                                | 378 ms: 1.01x slower                                         |
| typing_runtime_protocols   | 149 us                                                                | 151 us: 1.01x slower                                         |
| sqlglot_v2_optimize        | 49.8 ms                                                               | 50.2 ms: 1.01x slower                                        |
| sympy_str                  | 268 ms                                                                | 270 ms: 1.01x slower                                         |
| generators                 | 27.7 ms                                                               | 27.9 ms: 1.01x slower                                        |
| async_tree_cpu_io_mixed_tg | 504 ms                                                                | 508 ms: 1.01x slower                                         |
| float                      | 71.8 ms                                                               | 72.4 ms: 1.01x slower                                        |
| bpe_tokeniser              | 4.17 sec                                                              | 4.21 sec: 1.01x slower                                       |
| json_dumps                 | 9.50 ms                                                               | 9.58 ms: 1.01x slower                                        |
| chaos                      | 56.2 ms                                                               | 56.7 ms: 1.01x slower                                        |
| regex_compile              | 123 ms                                                                | 124 ms: 1.01x slower                                         |
| subparsers                 | 43.8 ms                                                               | 44.3 ms: 1.01x slower                                        |
| sympy_sum                  | 153 ms                                                                | 154 ms: 1.01x slower                                         |
| xml_etree_parse            | 132 ms                                                                | 134 ms: 1.01x slower                                         |
| sqlglot_v2_parse           | 1.21 ms                                                               | 1.22 ms: 1.01x slower                                        |
| sqlglot_v2_transpile       | 1.51 ms                                                               | 1.53 ms: 1.01x slower                                        |
| tomli_loads                | 1.90 sec                                                              | 1.93 sec: 1.01x slower                                       |
| json_loads                 | 27.7 us                                                               | 28.1 us: 1.01x slower                                        |
| nqueens                    | 76.7 ms                                                               | 77.8 ms: 1.01x slower                                        |
| pickle_pure_python         | 303 us                                                                | 307 us: 1.01x slower                                         |
| richards                   | 40.8 ms                                                               | 41.5 ms: 1.02x slower                                        |
| comprehensions             | 15.5 us                                                               | 15.8 us: 1.02x slower                                        |
| json                       | 4.93 ms                                                               | 5.02 ms: 1.02x slower                                        |
| pyflate                    | 402 ms                                                                | 410 ms: 1.02x slower                                         |
| thrift                     | 754 us                                                                | 768 us: 1.02x slower                                         |
| richards_super             | 46.7 ms                                                               | 47.5 ms: 1.02x slower                                        |
| regex_dna                  | 169 ms                                                                | 172 ms: 1.02x slower                                         |
| async_generators           | 335 ms                                                                | 342 ms: 1.02x slower                                         |
| many_optionals             | 1.21 ms                                                               | 1.23 ms: 1.02x slower                                        |
| genshi_text                | 20.2 ms                                                               | 20.6 ms: 1.02x slower                                        |
| deltablue                  | 3.28 ms                                                               | 3.36 ms: 1.03x slower                                        |
| sympy_expand               | 451 ms                                                                | 466 ms: 1.03x slower                                         |
| regex_effbot               | 2.56 ms                                                               | 2.67 ms: 1.04x slower                                        |
| logging_silent             | 96.7 ns                                                               | 101 ns: 1.04x slower                                         |
| gc_traversal               | 4.45 ms                                                               | 4.75 ms: 1.07x slower                                        |
| Geometric mean             | (ref)                                                                 | 1.00x slower                                                 |

Benchmark hidden because not significant (27): async_tree_io_tg, async_tree_memoization, async_tree_none, async_tree_io, genshi_xml, logging_simple, shortest_path, xml_etree_generate, django_template, k_core, connected_components, pprint_pformat, docutils, asyncio_websockets, async_tree_memoization_tg, meteor_contest, mdp, async_tree_none_tg, deepcopy, scimark_monte_carlo, crypto_pyaes, async_tree_cpu_io_mixed, pycparser, pylint, html5lib, create_gc_cycles, scimark_sparse_mat_mult
Ignored benchmarks (3) of results/bm-20250922-3.15.0a0-f0d8583/bm-20250922-vultr-x86_64-python-f0d8583303d28a5312e4-3.15.0a0-f0d8583.json: 2to3, mako, sphinx

- Geometric mean (including insignificant results): 1.005x slower

# HPT report

- Reliability score: 98.52% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x