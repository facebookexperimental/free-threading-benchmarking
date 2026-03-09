# Results vs. base

- fork: python
- ref: 5a15a52dd1dee37af4f2
- machine: linux-x86_64
- commit hash: 5a15a52
- commit date: 2026-03-08
- overall geometric mean: 1.004x slower
- HPT reliability: 97.21%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 282 ms                                                                 | 281 ms: 1.00x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (3): docutils, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_generators           | 378 ms                                                                 | 372 ms: 1.02x faster                                                   |
| coroutines                 | 23.1 ms                                                                | 23.4 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed_tg | 514 ms                                                                 | 570 ms: 1.11x slower                                                   |
| async_tree_cpu_io_mixed    | 539 ms                                                                 | 598 ms: 1.11x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                           |

Benchmark hidden because not significant (7): async_tree_none_tg, async_tree_io, async_tree_none, async_tree_io_tg, async_tree_memoization, asyncio_websockets, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 125 ms                                                                 | 123 ms: 1.02x faster                                                   |
| float          | 73.2 ms                                                                | 72.5 ms: 1.01x faster                                                  |
| pidigits       | 187 ms                                                                 | 203 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 178 ms                                                                 | 169 ms: 1.05x faster                                                   |
| regex_compile  | 141 ms                                                                 | 142 ms: 1.01x slower                                                   |
| regex_effbot   | 2.74 ms                                                                | 2.87 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| unpickle_pure_python | 237 us                                                                 | 234 us: 1.01x faster                                                   |
| tomli_loads          | 1.92 sec                                                               | 1.94 sec: 1.01x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (7): xml_etree_parse, pickle_pure_python, json_dumps, xml_etree_generate, xml_etree_process, json_loads, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 16.1 ms                                                                | 16.0 ms: 1.01x faster                                                  |
| python_startup_no_site | 9.86 ms                                                                | 9.79 ms: 1.01x faster                                                  |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 16.0 ms                                                                | 15.8 ms: 1.01x faster                                                  |
| genshi_xml     | 53.8 ms                                                                | 54.2 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (2): genshi_text, django_template

All benchmarks:
===============

| Benchmark                  | bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6+-149c465 | bm-20260308-vultr-x86_64-python-5a15a52dd1dee37af4f2-3.15.0a6+-5a15a52 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna                  | 178 ms                                                                 | 169 ms: 1.05x faster                                                   |
| logging_silent             | 104 ns                                                                 | 98.9 ns: 1.05x faster                                                  |
| create_gc_cycles           | 1.50 ms                                                                | 1.47 ms: 1.02x faster                                                  |
| async_generators           | 378 ms                                                                 | 372 ms: 1.02x faster                                                   |
| nbody                      | 125 ms                                                                 | 123 ms: 1.02x faster                                                   |
| mako                       | 16.0 ms                                                                | 15.8 ms: 1.01x faster                                                  |
| gc_traversal               | 1.95 ms                                                                | 1.93 ms: 1.01x faster                                                  |
| richards                   | 52.7 ms                                                                | 52.0 ms: 1.01x faster                                                  |
| sqlite_synth               | 1.93 us                                                                | 1.91 us: 1.01x faster                                                  |
| unpickle_pure_python       | 237 us                                                                 | 234 us: 1.01x faster                                                   |
| float                      | 73.2 ms                                                                | 72.5 ms: 1.01x faster                                                  |
| sympy_str                  | 316 ms                                                                 | 313 ms: 1.01x faster                                                   |
| fannkuch                   | 456 ms                                                                 | 452 ms: 1.01x faster                                                   |
| python_startup             | 16.1 ms                                                                | 16.0 ms: 1.01x faster                                                  |
| python_startup_no_site     | 9.86 ms                                                                | 9.79 ms: 1.01x faster                                                  |
| comprehensions             | 18.4 us                                                                | 18.3 us: 1.01x faster                                                  |
| json                       | 5.33 ms                                                                | 5.29 ms: 1.01x faster                                                  |
| deepcopy                   | 268 us                                                                 | 267 us: 1.01x faster                                                   |
| pprint_pformat             | 1.64 sec                                                               | 1.63 sec: 1.01x faster                                                 |
| 2to3                       | 282 ms                                                                 | 281 ms: 1.00x faster                                                   |
| raytrace                   | 296 ms                                                                 | 296 ms: 1.00x faster                                                   |
| shortest_path              | 532 ms                                                                 | 532 ms: 1.00x slower                                                   |
| scimark_sor                | 121 ms                                                                 | 121 ms: 1.00x slower                                                   |
| mdp                        | 1.31 sec                                                               | 1.32 sec: 1.00x slower                                                 |
| sqlglot_v2_normalize       | 115 ms                                                                 | 115 ms: 1.00x slower                                                   |
| bpe_tokeniser              | 4.31 sec                                                               | 4.33 sec: 1.00x slower                                                 |
| regex_compile              | 141 ms                                                                 | 142 ms: 1.01x slower                                                   |
| bench_mp_pool              | 7.04 ms                                                                | 7.08 ms: 1.01x slower                                                  |
| genshi_xml                 | 53.8 ms                                                                | 54.2 ms: 1.01x slower                                                  |
| crypto_pyaes               | 86.8 ms                                                                | 87.5 ms: 1.01x slower                                                  |
| scimark_monte_carlo        | 77.2 ms                                                                | 77.9 ms: 1.01x slower                                                  |
| thrift                     | 909 us                                                                 | 918 us: 1.01x slower                                                   |
| tomli_loads                | 1.92 sec                                                               | 1.94 sec: 1.01x slower                                                 |
| typing_runtime_protocols   | 196 us                                                                 | 198 us: 1.01x slower                                                   |
| telco                      | 172 ms                                                                 | 174 ms: 1.01x slower                                                   |
| scimark_sparse_mat_mult    | 5.23 ms                                                                | 5.30 ms: 1.01x slower                                                  |
| deepcopy_memo              | 31.1 us                                                                | 31.5 us: 1.01x slower                                                  |
| connected_components       | 483 ms                                                                 | 490 ms: 1.01x slower                                                   |
| coroutines                 | 23.1 ms                                                                | 23.4 ms: 1.01x slower                                                  |
| deepcopy_reduce            | 2.94 us                                                                | 2.98 us: 1.01x slower                                                  |
| pyflate                    | 456 ms                                                                 | 463 ms: 1.02x slower                                                   |
| scimark_lu                 | 125 ms                                                                 | 127 ms: 1.02x slower                                                   |
| pathlib                    | 17.3 ms                                                                | 17.7 ms: 1.02x slower                                                  |
| generators                 | 31.6 ms                                                                | 32.6 ms: 1.03x slower                                                  |
| spectral_norm              | 108 ms                                                                 | 112 ms: 1.03x slower                                                   |
| regex_effbot               | 2.74 ms                                                                | 2.87 ms: 1.05x slower                                                  |
| pidigits                   | 187 ms                                                                 | 203 ms: 1.08x slower                                                   |
| async_tree_cpu_io_mixed_tg | 514 ms                                                                 | 570 ms: 1.11x slower                                                   |
| async_tree_cpu_io_mixed    | 539 ms                                                                 | 598 ms: 1.11x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (45): sphinx, xml_etree_parse, async_tree_none_tg, async_tree_io, async_tree_none, logging_simple, regex_v8, dulwich_log, pickle_pure_python, pylint, genshi_text, async_tree_io_tg, django_template, richards_super, json_dumps, scimark_fft, sympy_sum, subparsers, async_tree_memoization, xml_etree_generate, xml_etree_process, sympy_expand, sqlglot_v2_optimize, html5lib, asyncio_websockets, meteor_contest, pprint_safe_repr, many_optionals, docutils, bench_thread_pool, k_core, chaos, deltablue, coverage, go, sympy_integrate, json_loads, logging_format, nqueens, xml_etree_iterparse, hexiom, sqlglot_v2_transpile, pycparser, async_tree_memoization_tg, sqlglot_v2_parse
Ignored benchmarks (8) of results/bm-20260307-3.15.0a6+-149c465-NOGIL/bm-20260307-vultr-x86_64-python-149c4657507d17f78dd0-3.15.0a6+-149c465.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.004x slower

# HPT report

- Reliability score: 97.21% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x