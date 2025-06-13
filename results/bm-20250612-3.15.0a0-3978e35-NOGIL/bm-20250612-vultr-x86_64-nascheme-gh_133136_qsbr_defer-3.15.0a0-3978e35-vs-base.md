# Results vs. base

- fork: nascheme
- ref: gh_133136_qsbr_defer
- machine: linux-x86_64
- commit hash: 3978e35
- commit date: 2025-06-12
- overall geometric mean: 1.000x slower
- HPT reliability: 56.16%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (4): 2to3, docutils, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| asyncio_websockets         | 515 ms                                                                | 511 ms: 1.01x faster                                                    |
| async_generators           | 370 ms                                                                | 368 ms: 1.01x faster                                                    |
| coroutines                 | 23.5 ms                                                               | 23.4 ms: 1.00x faster                                                   |
| async_tree_cpu_io_mixed_tg | 469 ms                                                                | 472 ms: 1.01x slower                                                    |
| async_tree_none_tg         | 226 ms                                                                | 237 ms: 1.05x slower                                                    |
| Geometric mean             | (ref)                                                                 | 1.00x slower                                                            |

Benchmark hidden because not significant (6): async_tree_memoization, async_tree_io, async_tree_none, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 203 ms                                                                | 184 ms: 1.10x faster                                                    |
| float          | 68.8 ms                                                               | 69.4 ms: 1.01x slower                                                   |
| nbody          | 119 ms                                                                | 121 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.03x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 169 ms                                                                | 167 ms: 1.01x faster                                                    |
| regex_v8       | 20.0 ms                                                               | 20.6 ms: 1.03x slower                                                   |
| regex_effbot   | 2.63 ms                                                               | 2.73 ms: 1.04x slower                                                   |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                            |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35 |
|---------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_generate  | 95.7 ms                                                               | 94.5 ms: 1.01x faster                                                   |
| xml_etree_iterparse | 87.1 ms                                                               | 86.3 ms: 1.01x faster                                                   |
| xml_etree_process   | 69.0 ms                                                               | 68.4 ms: 1.01x faster                                                   |
| pickle_pure_python  | 338 us                                                                | 335 us: 1.01x faster                                                    |
| json_dumps          | 12.0 ms                                                               | 11.9 ms: 1.00x faster                                                   |
| json_loads          | 32.0 us                                                               | 31.8 us: 1.00x faster                                                   |
| Geometric mean      | (ref)                                                                 | 1.01x faster                                                            |

Benchmark hidden because not significant (3): tomli_loads, xml_etree_parse, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 9.59 ms                                                               | 9.61 ms: 1.00x slower                                                   |
| Geometric mean         | (ref)                                                                 | 1.00x slower                                                            |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 39.4 ms                                                               | 39.0 ms: 1.01x faster                                                   |
| genshi_xml      | 56.2 ms                                                               | 55.6 ms: 1.01x faster                                                   |
| Geometric mean  | (ref)                                                                 | 1.01x faster                                                            |

Benchmark hidden because not significant (2): mako, genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20250603-vultr-x86_64-python-1ffe913c2017b44804ac-3.15.0a0-1ffe913 | bm-20250612-vultr-x86_64-nascheme-gh_133136_qsbr_defer-3.15.0a0-3978e35 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits                   | 203 ms                                                                | 184 ms: 1.10x faster                                                    |
| coverage                   | 114 ms                                                                | 109 ms: 1.05x faster                                                    |
| generators                 | 30.2 ms                                                               | 29.4 ms: 1.03x faster                                                   |
| hexiom                     | 6.50 ms                                                               | 6.34 ms: 1.03x faster                                                   |
| nqueens                    | 86.6 ms                                                               | 85.1 ms: 1.02x faster                                                   |
| sqlglot_v2_normalize       | 113 ms                                                                | 112 ms: 1.02x faster                                                    |
| xml_etree_generate         | 95.7 ms                                                               | 94.5 ms: 1.01x faster                                                   |
| regex_dna                  | 169 ms                                                                | 167 ms: 1.01x faster                                                    |
| django_template            | 39.4 ms                                                               | 39.0 ms: 1.01x faster                                                   |
| genshi_xml                 | 56.2 ms                                                               | 55.6 ms: 1.01x faster                                                   |
| comprehensions             | 17.8 us                                                               | 17.6 us: 1.01x faster                                                   |
| xml_etree_iterparse        | 87.1 ms                                                               | 86.3 ms: 1.01x faster                                                   |
| asyncio_websockets         | 515 ms                                                                | 511 ms: 1.01x faster                                                    |
| xml_etree_process          | 69.0 ms                                                               | 68.4 ms: 1.01x faster                                                   |
| scimark_monte_carlo        | 77.3 ms                                                               | 76.7 ms: 1.01x faster                                                   |
| pickle_pure_python         | 338 us                                                                | 335 us: 1.01x faster                                                    |
| async_generators           | 370 ms                                                                | 368 ms: 1.01x faster                                                    |
| pycparser                  | 1.13 sec                                                              | 1.13 sec: 1.01x faster                                                  |
| chaos                      | 63.3 ms                                                               | 63.0 ms: 1.01x faster                                                   |
| sqlglot_v2_optimize        | 56.5 ms                                                               | 56.2 ms: 1.01x faster                                                   |
| json_dumps                 | 12.0 ms                                                               | 11.9 ms: 1.00x faster                                                   |
| mdp                        | 1.31 sec                                                              | 1.31 sec: 1.00x faster                                                  |
| json_loads                 | 32.0 us                                                               | 31.8 us: 1.00x faster                                                   |
| deepcopy                   | 287 us                                                                | 286 us: 1.00x faster                                                    |
| logging_silent             | 526 ns                                                                | 524 ns: 1.00x faster                                                    |
| raytrace                   | 297 ms                                                                | 296 ms: 1.00x faster                                                    |
| coroutines                 | 23.5 ms                                                               | 23.4 ms: 1.00x faster                                                   |
| crypto_pyaes               | 85.8 ms                                                               | 85.9 ms: 1.00x slower                                                   |
| python_startup_no_site     | 9.59 ms                                                               | 9.61 ms: 1.00x slower                                                   |
| richards_super             | 58.4 ms                                                               | 58.6 ms: 1.00x slower                                                   |
| pprint_pformat             | 1.82 sec                                                              | 1.82 sec: 1.00x slower                                                  |
| richards                   | 50.7 ms                                                               | 50.9 ms: 1.00x slower                                                   |
| bench_mp_pool              | 103 ms                                                                | 103 ms: 1.01x slower                                                    |
| async_tree_cpu_io_mixed_tg | 469 ms                                                                | 472 ms: 1.01x slower                                                    |
| float                      | 68.8 ms                                                               | 69.4 ms: 1.01x slower                                                   |
| create_gc_cycles           | 1.48 ms                                                               | 1.49 ms: 1.01x slower                                                   |
| pyflate                    | 468 ms                                                                | 472 ms: 1.01x slower                                                    |
| pprint_safe_repr           | 874 ms                                                                | 883 ms: 1.01x slower                                                    |
| deepcopy_memo              | 34.4 us                                                               | 34.7 us: 1.01x slower                                                   |
| gc_traversal               | 1.91 ms                                                               | 1.93 ms: 1.01x slower                                                   |
| nbody                      | 119 ms                                                                | 121 ms: 1.01x slower                                                    |
| scimark_fft                | 361 ms                                                                | 366 ms: 1.02x slower                                                    |
| sqlite_synth               | 2.03 us                                                               | 2.06 us: 1.02x slower                                                   |
| fannkuch                   | 458 ms                                                                | 466 ms: 1.02x slower                                                    |
| spectral_norm              | 114 ms                                                                | 116 ms: 1.02x slower                                                    |
| scimark_sor                | 122 ms                                                                | 125 ms: 1.03x slower                                                    |
| regex_v8                   | 20.0 ms                                                               | 20.6 ms: 1.03x slower                                                   |
| typing_runtime_protocols   | 185 us                                                                | 191 us: 1.03x slower                                                    |
| regex_effbot               | 2.63 ms                                                               | 2.73 ms: 1.04x slower                                                   |
| async_tree_none_tg         | 226 ms                                                                | 237 ms: 1.05x slower                                                    |
| scimark_sparse_mat_mult    | 5.16 ms                                                               | 5.44 ms: 1.05x slower                                                   |
| bench_thread_pool          | 3.11 ms                                                               | 3.43 ms: 1.10x slower                                                   |
| Geometric mean             | (ref)                                                                 | 1.00x slower                                                            |

Benchmark hidden because not significant (42): subparsers, sqlglot_v2_parse, meteor_contest, async_tree_memoization, telco, thrift, async_tree_io, mako, tomli_loads, deltablue, async_tree_none, xml_etree_parse, docutils, html5lib, regex_compile, logging_simple, async_tree_io_tg, k_core, go, deepcopy_reduce, python_startup, bpe_tokeniser, sympy_sum, sympy_expand, pathlib, many_optionals, sympy_integrate, 2to3, sympy_str, dulwich_log, sphinx, json, connected_components, logging_format, unpickle_pure_python, async_tree_cpu_io_mixed, shortest_path, genshi_text, async_tree_memoization_tg, scimark_lu, sqlglot_v2_transpile, pylint

- Geometric mean (including insignificant results): 1.000x slower

# HPT report

- Reliability score: 56.16% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.99x