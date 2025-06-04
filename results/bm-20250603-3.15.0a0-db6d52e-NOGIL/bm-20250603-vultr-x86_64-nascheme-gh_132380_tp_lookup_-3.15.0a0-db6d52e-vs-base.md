# Results vs. base

- fork: nascheme
- ref: gh_132380_tp_lookup_
- machine: linux-x86_64
- commit hash: db6d52e
- commit date: 2025-06-03
- overall geometric mean: 1.001x slower
- HPT reliability: 62.39%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (4): 2to3, docutils, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_memoization     | 313 ms                                                                | 310 ms: 1.01x faster                                                    |
| async_tree_none            | 258 ms                                                                | 255 ms: 1.01x faster                                                    |
| async_generators           | 370 ms                                                                | 373 ms: 1.01x slower                                                    |
| async_tree_cpu_io_mixed_tg | 469 ms                                                                | 475 ms: 1.01x slower                                                    |
| async_tree_cpu_io_mixed    | 496 ms                                                                | 503 ms: 1.01x slower                                                    |
| Geometric mean             | (ref)                                                                 | 1.00x slower                                                            |

Benchmark hidden because not significant (6): async_tree_io, asyncio_websockets, coroutines, async_tree_none_tg, async_tree_memoization_tg, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 68.8 ms                                                               | 69.6 ms: 1.01x slower                                                   |
| nbody          | 119 ms                                                                | 121 ms: 1.01x slower                                                    |
| pidigits       | 203 ms                                                                | 215 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.03x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 169 ms                                                                | 164 ms: 1.03x faster                                                    |
| regex_effbot   | 2.63 ms                                                               | 2.65 ms: 1.01x slower                                                   |
| regex_v8       | 20.0 ms                                                               | 20.5 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                                 | 1.00x slower                                                            |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e |
|---------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_loads          | 32.0 us                                                               | 30.7 us: 1.04x faster                                                   |
| tomli_loads         | 2.16 sec                                                              | 2.13 sec: 1.01x faster                                                  |
| xml_etree_generate  | 95.7 ms                                                               | 94.6 ms: 1.01x faster                                                   |
| xml_etree_process   | 69.0 ms                                                               | 68.3 ms: 1.01x faster                                                   |
| pickle_pure_python  | 338 us                                                                | 337 us: 1.00x faster                                                    |
| xml_etree_iterparse | 87.1 ms                                                               | 87.9 ms: 1.01x slower                                                   |
| Geometric mean      | (ref)                                                                 | 1.01x faster                                                            |

Benchmark hidden because not significant (3): xml_etree_parse, json_dumps, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 9.59 ms                                                               | 9.61 ms: 1.00x slower                                                   |
| python_startup         | 16.0 ms                                                               | 16.1 ms: 1.00x slower                                                   |
| Geometric mean         | (ref)                                                                 | 1.00x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako           | 16.0 ms                                                               | 15.7 ms: 1.02x faster                                                   |
| genshi_text    | 25.7 ms                                                               | 26.2 ms: 1.02x slower                                                   |
| genshi_xml     | 56.2 ms                                                               | 57.4 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                                 | 1.00x slower                                                            |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250603-vultr-x86_64-nascheme-gh_132380_tp_lookup_-3.15.0a0-db6d52e |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_loads                 | 32.0 us                                                               | 30.7 us: 1.04x faster                                                   |
| hexiom                     | 6.50 ms                                                               | 6.30 ms: 1.03x faster                                                   |
| regex_dna                  | 169 ms                                                                | 164 ms: 1.03x faster                                                    |
| coverage                   | 114 ms                                                                | 112 ms: 1.02x faster                                                    |
| mako                       | 16.0 ms                                                               | 15.7 ms: 1.02x faster                                                   |
| json                       | 5.40 ms                                                               | 5.33 ms: 1.01x faster                                                   |
| tomli_loads                | 2.16 sec                                                              | 2.13 sec: 1.01x faster                                                  |
| comprehensions             | 17.8 us                                                               | 17.6 us: 1.01x faster                                                   |
| xml_etree_generate         | 95.7 ms                                                               | 94.6 ms: 1.01x faster                                                   |
| async_tree_memoization     | 313 ms                                                                | 310 ms: 1.01x faster                                                    |
| xml_etree_process          | 69.0 ms                                                               | 68.3 ms: 1.01x faster                                                   |
| telco                      | 8.71 ms                                                               | 8.63 ms: 1.01x faster                                                   |
| generators                 | 30.2 ms                                                               | 29.9 ms: 1.01x faster                                                   |
| async_tree_none            | 258 ms                                                                | 255 ms: 1.01x faster                                                    |
| logging_format             | 8.74 us                                                               | 8.68 us: 1.01x faster                                                   |
| go                         | 122 ms                                                                | 121 ms: 1.01x faster                                                    |
| chaos                      | 63.3 ms                                                               | 62.9 ms: 1.01x faster                                                   |
| raytrace                   | 297 ms                                                                | 296 ms: 1.01x faster                                                    |
| spectral_norm              | 114 ms                                                                | 113 ms: 1.01x faster                                                    |
| sympy_sum                  | 178 ms                                                                | 177 ms: 1.01x faster                                                    |
| mdp                        | 1.31 sec                                                              | 1.31 sec: 1.00x faster                                                  |
| scimark_fft                | 361 ms                                                                | 360 ms: 1.00x faster                                                    |
| pickle_pure_python         | 338 us                                                                | 337 us: 1.00x faster                                                    |
| python_startup_no_site     | 9.59 ms                                                               | 9.61 ms: 1.00x slower                                                   |
| deepcopy_reduce            | 2.96 us                                                               | 2.97 us: 1.00x slower                                                   |
| python_startup             | 16.0 ms                                                               | 16.1 ms: 1.00x slower                                                   |
| bpe_tokeniser              | 4.36 sec                                                              | 4.38 sec: 1.00x slower                                                  |
| richards_super             | 58.4 ms                                                               | 58.7 ms: 1.00x slower                                                   |
| async_generators           | 370 ms                                                                | 373 ms: 1.01x slower                                                    |
| pprint_safe_repr           | 874 ms                                                                | 880 ms: 1.01x slower                                                    |
| regex_effbot               | 2.63 ms                                                               | 2.65 ms: 1.01x slower                                                   |
| gc_traversal               | 1.91 ms                                                               | 1.92 ms: 1.01x slower                                                   |
| scimark_lu                 | 127 ms                                                                | 128 ms: 1.01x slower                                                    |
| deepcopy                   | 287 us                                                                | 289 us: 1.01x slower                                                    |
| meteor_contest             | 119 ms                                                                | 120 ms: 1.01x slower                                                    |
| xml_etree_iterparse        | 87.1 ms                                                               | 87.9 ms: 1.01x slower                                                   |
| richards                   | 50.7 ms                                                               | 51.2 ms: 1.01x slower                                                   |
| float                      | 68.8 ms                                                               | 69.6 ms: 1.01x slower                                                   |
| pathlib                    | 19.4 ms                                                               | 19.6 ms: 1.01x slower                                                   |
| async_tree_cpu_io_mixed_tg | 469 ms                                                                | 475 ms: 1.01x slower                                                    |
| typing_runtime_protocols   | 185 us                                                                | 188 us: 1.01x slower                                                    |
| async_tree_cpu_io_mixed    | 496 ms                                                                | 503 ms: 1.01x slower                                                    |
| nbody                      | 119 ms                                                                | 121 ms: 1.01x slower                                                    |
| deepcopy_memo              | 34.4 us                                                               | 35.0 us: 1.02x slower                                                   |
| genshi_text                | 25.7 ms                                                               | 26.2 ms: 1.02x slower                                                   |
| fannkuch                   | 458 ms                                                                | 466 ms: 1.02x slower                                                    |
| scimark_sparse_mat_mult    | 5.16 ms                                                               | 5.26 ms: 1.02x slower                                                   |
| scimark_sor                | 122 ms                                                                | 124 ms: 1.02x slower                                                    |
| pyflate                    | 468 ms                                                                | 477 ms: 1.02x slower                                                    |
| genshi_xml                 | 56.2 ms                                                               | 57.4 ms: 1.02x slower                                                   |
| regex_v8                   | 20.0 ms                                                               | 20.5 ms: 1.03x slower                                                   |
| pidigits                   | 203 ms                                                                | 215 ms: 1.06x slower                                                    |
| Geometric mean             | (ref)                                                                 | 1.00x slower                                                            |

Benchmark hidden because not significant (42): html5lib, deltablue, connected_components, sqlglot_v2_parse, sphinx, django_template, async_tree_io, k_core, sqlglot_v2_transpile, pycparser, sympy_expand, subparsers, pprint_pformat, sqlglot_v2_optimize, sympy_integrate, sqlglot_v2_normalize, xml_etree_parse, asyncio_websockets, 2to3, logging_simple, json_dumps, coroutines, scimark_monte_carlo, bench_thread_pool, unpickle_pure_python, thrift, crypto_pyaes, logging_silent, sqlite_synth, sympy_str, regex_compile, async_tree_none_tg, docutils, nqueens, async_tree_memoization_tg, dulwich_log, bench_mp_pool, async_tree_io_tg, many_optionals, shortest_path, create_gc_cycles, pylint

- Geometric mean (including insignificant results): 1.001x slower

# HPT report

- Reliability score: 62.39% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x