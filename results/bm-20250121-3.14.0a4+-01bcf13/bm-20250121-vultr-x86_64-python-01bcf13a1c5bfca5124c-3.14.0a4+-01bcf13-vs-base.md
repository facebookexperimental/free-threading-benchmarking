# Results vs. base

- fork: python
- ref: 01bcf13a1c5bfca5124c
- machine: linux-x86_64
- commit hash: 01bcf13
- commit date: 2025-01-21
- overall geometric mean: 1.002x slower
- HPT reliability: 83.49%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4+-29caec6 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 254 ms                                                                 | 253 ms: 1.00x faster                                                   |
| docutils       | 2.55 sec                                                               | 2.56 sec: 1.00x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4+-29caec6 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| coroutines                 | 22.4 ms                                                                | 21.6 ms: 1.04x faster                                                  |
| async_generators           | 319 ms                                                                 | 320 ms: 1.00x slower                                                   |
| asyncio_websockets         | 517 ms                                                                 | 523 ms: 1.01x slower                                                   |
| async_tree_cpu_io_mixed    | 488 ms                                                                 | 496 ms: 1.02x slower                                                   |
| async_tree_cpu_io_mixed_tg | 476 ms                                                                 | 484 ms: 1.02x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (6): async_tree_none, async_tree_memoization, async_tree_io, async_tree_memoization_tg, async_tree_none_tg, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4+-29caec6 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| nbody          | 91.6 ms                                                                | 90.7 ms: 1.01x faster                                                  |
| pidigits       | 196 ms                                                                 | 198 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4+-29caec6 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 168 ms                                                                 | 172 ms: 1.02x slower                                                   |
| regex_v8       | 23.5 ms                                                                | 24.2 ms: 1.03x slower                                                  |
| regex_effbot   | 2.57 ms                                                                | 2.87 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                           |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4+-29caec6 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 129 ms                                                                 | 127 ms: 1.02x faster                                                   |
| unpickle_pure_python | 224 us                                                                 | 221 us: 1.01x faster                                                   |
| xml_etree_iterparse  | 90.8 ms                                                                | 90.0 ms: 1.01x faster                                                  |
| tomli_loads          | 1.95 sec                                                               | 1.94 sec: 1.01x faster                                                 |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (5): xml_etree_generate, xml_etree_process, pickle_pure_python, json_loads, json_dumps

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4+-29caec6 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako           | 11.7 ms                                                                | 11.6 ms: 1.01x faster                                                  |
| genshi_text    | 21.3 ms                                                                | 21.5 ms: 1.01x slower                                                  |
| genshi_xml     | 48.9 ms                                                                | 49.7 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4+-29caec6 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| spectral_norm              | 93.5 ms                                                                | 90.1 ms: 1.04x faster                                                  |
| coroutines                 | 22.4 ms                                                                | 21.6 ms: 1.04x faster                                                  |
| logging_silent             | 103 ns                                                                 | 101 ns: 1.03x faster                                                   |
| chaos                      | 55.9 ms                                                                | 54.9 ms: 1.02x faster                                                  |
| pyflate                    | 421 ms                                                                 | 414 ms: 1.02x faster                                                   |
| xml_etree_parse            | 129 ms                                                                 | 127 ms: 1.02x faster                                                   |
| sqlite_synth               | 2.22 us                                                                | 2.19 us: 1.01x faster                                                  |
| richards_super             | 47.9 ms                                                                | 47.3 ms: 1.01x faster                                                  |
| raytrace                   | 261 ms                                                                 | 258 ms: 1.01x faster                                                   |
| unpickle_pure_python       | 224 us                                                                 | 221 us: 1.01x faster                                                   |
| nbody                      | 91.6 ms                                                                | 90.7 ms: 1.01x faster                                                  |
| mako                       | 11.7 ms                                                                | 11.6 ms: 1.01x faster                                                  |
| xml_etree_iterparse        | 90.8 ms                                                                | 90.0 ms: 1.01x faster                                                  |
| pprint_pformat             | 1.42 sec                                                               | 1.41 sec: 1.01x faster                                                 |
| thrift                     | 740 us                                                                 | 734 us: 1.01x faster                                                   |
| sqlalchemy_imperative      | 19.6 ms                                                                | 19.4 ms: 1.01x faster                                                  |
| tomli_loads                | 1.95 sec                                                               | 1.94 sec: 1.01x faster                                                 |
| pathlib                    | 18.3 ms                                                                | 18.1 ms: 1.01x faster                                                  |
| generators                 | 27.7 ms                                                                | 27.5 ms: 1.01x faster                                                  |
| go                         | 113 ms                                                                 | 113 ms: 1.01x faster                                                   |
| pprint_safe_repr           | 700 ms                                                                 | 697 ms: 1.00x faster                                                   |
| sqlalchemy_declarative     | 129 ms                                                                 | 129 ms: 1.00x faster                                                   |
| 2to3                       | 254 ms                                                                 | 253 ms: 1.00x faster                                                   |
| scimark_fft                | 313 ms                                                                 | 313 ms: 1.00x faster                                                   |
| docutils                   | 2.55 sec                                                               | 2.56 sec: 1.00x slower                                                 |
| bpe_tokeniser              | 4.23 sec                                                               | 4.25 sec: 1.00x slower                                                 |
| async_generators           | 319 ms                                                                 | 320 ms: 1.00x slower                                                   |
| bench_thread_pool          | 1.03 ms                                                                | 1.03 ms: 1.01x slower                                                  |
| logging_simple             | 6.34 us                                                                | 6.39 us: 1.01x slower                                                  |
| telco                      | 7.15 ms                                                                | 7.21 ms: 1.01x slower                                                  |
| pycparser                  | 1.12 sec                                                               | 1.13 sec: 1.01x slower                                                 |
| genshi_text                | 21.3 ms                                                                | 21.5 ms: 1.01x slower                                                  |
| asyncio_websockets         | 517 ms                                                                 | 523 ms: 1.01x slower                                                   |
| scimark_sparse_mat_mult    | 4.33 ms                                                                | 4.38 ms: 1.01x slower                                                  |
| nqueens                    | 77.2 ms                                                                | 78.1 ms: 1.01x slower                                                  |
| hexiom                     | 5.74 ms                                                                | 5.80 ms: 1.01x slower                                                  |
| pidigits                   | 196 ms                                                                 | 198 ms: 1.01x slower                                                   |
| scimark_lu                 | 111 ms                                                                 | 113 ms: 1.01x slower                                                   |
| async_tree_cpu_io_mixed    | 488 ms                                                                 | 496 ms: 1.02x slower                                                   |
| async_tree_cpu_io_mixed_tg | 476 ms                                                                 | 484 ms: 1.02x slower                                                   |
| genshi_xml                 | 48.9 ms                                                                | 49.7 ms: 1.02x slower                                                  |
| regex_dna                  | 168 ms                                                                 | 172 ms: 1.02x slower                                                   |
| gc_traversal               | 4.19 ms                                                                | 4.29 ms: 1.02x slower                                                  |
| meteor_contest             | 98.3 ms                                                                | 101 ms: 1.03x slower                                                   |
| regex_v8                   | 23.5 ms                                                                | 24.2 ms: 1.03x slower                                                  |
| mdp                        | 2.29 sec                                                               | 2.44 sec: 1.07x slower                                                 |
| regex_effbot               | 2.57 ms                                                                | 2.87 ms: 1.12x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (48): async_tree_none, connected_components, comprehensions, subparsers, sympy_expand, float, coverage, xml_etree_generate, async_tree_memoization, async_tree_io, xml_etree_process, typing_runtime_protocols, sympy_sum, async_tree_memoization_tg, fannkuch, python_startup_no_site, richards, deltablue, pickle_pure_python, python_startup, sqlglot_normalize, deepcopy_memo, shortest_path, many_optionals, sympy_integrate, crypto_pyaes, django_template, deepcopy, dulwich_log, sympy_str, sqlglot_optimize, pylint, json, sphinx, scimark_sor, sqlglot_parse, sqlglot_transpile, logging_format, regex_compile, deepcopy_reduce, scimark_monte_carlo, json_loads, bench_mp_pool, json_dumps, k_core, create_gc_cycles, async_tree_none_tg, async_tree_io_tg

- Geometric mean (including insignificant results): 1.002x slower

# HPT report

- Reliability score: 83.49% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x