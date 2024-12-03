# Results vs. base

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: e517ccb
- commit date: 2024-12-02
- overall geometric mean: 1.001x slower
- HPT reliability: 55.67%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2+-15d6506 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 258 ms                                                                 | 259 ms: 1.00x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2+-15d6506 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 670 ms                                                                 | 635 ms: 1.06x faster                                                     |
| async_tree_cpu_io_mixed_tg | 667 ms                                                                 | 632 ms: 1.05x faster                                                     |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (9): async_tree_io, async_tree_memoization, async_tree_none_tg, async_tree_none, async_generators, async_tree_memoization_tg, asyncio_websockets, coroutines, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2+-15d6506 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 222 ms                                                                 | 216 ms: 1.03x faster                                                     |
| float          | 81.3 ms                                                                | 82.1 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2+-15d6506 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 175 ms                                                                 | 177 ms: 1.01x slower                                                     |
| regex_v8       | 24.5 ms                                                                | 24.9 ms: 1.02x slower                                                    |
| regex_effbot   | 2.62 ms                                                                | 2.82 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                             |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2+-15d6506 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|--------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps         | 11.4 ms                                                                | 11.4 ms: 1.01x slower                                                    |
| xml_etree_generate | 86.2 ms                                                                | 86.7 ms: 1.01x slower                                                    |
| pickle_pure_python | 321 us                                                                 | 323 us: 1.01x slower                                                     |
| tomli_loads        | 2.11 sec                                                               | 2.13 sec: 1.01x slower                                                   |
| Geometric mean     | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (5): json_loads, unpickle_pure_python, xml_etree_parse, xml_etree_process, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2+-15d6506 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.40 ms                                                                | 7.36 ms: 1.01x faster                                                    |
| python_startup         | 14.6 ms                                                                | 14.5 ms: 1.00x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2+-15d6506 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text    | 22.7 ms                                                                | 22.3 ms: 1.01x faster                                                    |
| genshi_xml     | 50.8 ms                                                                | 50.2 ms: 1.01x faster                                                    |
| mako           | 11.6 ms                                                                | 12.1 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20241129-vultr-x86_64-python-15d6506d175780bb29e5-3.14.0a2+-15d6506 | bm-20241202-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-e517ccb |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 670 ms                                                                 | 635 ms: 1.06x faster                                                     |
| async_tree_cpu_io_mixed_tg | 667 ms                                                                 | 632 ms: 1.05x faster                                                     |
| pidigits                   | 222 ms                                                                 | 216 ms: 1.03x faster                                                     |
| logging_silent             | 112 ns                                                                 | 110 ns: 1.02x faster                                                     |
| nqueens                    | 80.9 ms                                                                | 79.6 ms: 1.02x faster                                                    |
| create_gc_cycles           | 1.96 ms                                                                | 1.93 ms: 1.02x faster                                                    |
| scimark_lu                 | 114 ms                                                                 | 113 ms: 1.01x faster                                                     |
| genshi_text                | 22.7 ms                                                                | 22.3 ms: 1.01x faster                                                    |
| comprehensions             | 17.8 us                                                                | 17.6 us: 1.01x faster                                                    |
| pathlib                    | 18.4 ms                                                                | 18.2 ms: 1.01x faster                                                    |
| genshi_xml                 | 50.8 ms                                                                | 50.2 ms: 1.01x faster                                                    |
| scimark_sor                | 137 ms                                                                 | 135 ms: 1.01x faster                                                     |
| sympy_expand               | 466 ms                                                                 | 462 ms: 1.01x faster                                                     |
| deepcopy                   | 265 us                                                                 | 263 us: 1.01x faster                                                     |
| pycparser                  | 1.14 sec                                                               | 1.13 sec: 1.01x faster                                                   |
| bench_mp_pool              | 86.3 ms                                                                | 85.8 ms: 1.01x faster                                                    |
| richards                   | 47.4 ms                                                                | 47.1 ms: 1.01x faster                                                    |
| python_startup_no_site     | 7.40 ms                                                                | 7.36 ms: 1.01x faster                                                    |
| scimark_sparse_mat_mult    | 4.55 ms                                                                | 4.53 ms: 1.01x faster                                                    |
| python_startup             | 14.6 ms                                                                | 14.5 ms: 1.00x faster                                                    |
| sqlalchemy_declarative     | 127 ms                                                                 | 127 ms: 1.00x faster                                                     |
| raytrace                   | 269 ms                                                                 | 268 ms: 1.00x faster                                                     |
| pylint                     | 270 ms                                                                 | 271 ms: 1.00x slower                                                     |
| hexiom                     | 6.03 ms                                                                | 6.04 ms: 1.00x slower                                                    |
| 2to3                       | 258 ms                                                                 | 259 ms: 1.00x slower                                                     |
| chaos                      | 58.9 ms                                                                | 59.1 ms: 1.00x slower                                                    |
| sympy_integrate            | 20.0 ms                                                                | 20.1 ms: 1.00x slower                                                    |
| go                         | 121 ms                                                                 | 122 ms: 1.00x slower                                                     |
| pyflate                    | 450 ms                                                                 | 453 ms: 1.01x slower                                                     |
| json_dumps                 | 11.4 ms                                                                | 11.4 ms: 1.01x slower                                                    |
| subparsers                 | 22.0 ms                                                                | 22.2 ms: 1.01x slower                                                    |
| xml_etree_generate         | 86.2 ms                                                                | 86.7 ms: 1.01x slower                                                    |
| many_optionals             | 1.02 ms                                                                | 1.02 ms: 1.01x slower                                                    |
| mdp                        | 2.48 sec                                                               | 2.50 sec: 1.01x slower                                                   |
| pickle_pure_python         | 321 us                                                                 | 323 us: 1.01x slower                                                     |
| scimark_fft                | 339 ms                                                                 | 342 ms: 1.01x slower                                                     |
| float                      | 81.3 ms                                                                | 82.1 ms: 1.01x slower                                                    |
| deltablue                  | 3.29 ms                                                                | 3.32 ms: 1.01x slower                                                    |
| regex_dna                  | 175 ms                                                                 | 177 ms: 1.01x slower                                                     |
| scimark_monte_carlo        | 65.3 ms                                                                | 66.0 ms: 1.01x slower                                                    |
| meteor_contest             | 100.0 ms                                                               | 101 ms: 1.01x slower                                                     |
| fannkuch                   | 381 ms                                                                 | 385 ms: 1.01x slower                                                     |
| typing_runtime_protocols   | 158 us                                                                 | 159 us: 1.01x slower                                                     |
| tomli_loads                | 2.11 sec                                                               | 2.13 sec: 1.01x slower                                                   |
| logging_simple             | 6.20 us                                                                | 6.28 us: 1.01x slower                                                    |
| regex_v8                   | 24.5 ms                                                                | 24.9 ms: 1.02x slower                                                    |
| spectral_norm              | 115 ms                                                                 | 117 ms: 1.02x slower                                                     |
| deepcopy_memo              | 30.5 us                                                                | 31.2 us: 1.02x slower                                                    |
| crypto_pyaes               | 67.4 ms                                                                | 69.4 ms: 1.03x slower                                                    |
| mako                       | 11.6 ms                                                                | 12.1 ms: 1.04x slower                                                    |
| regex_effbot               | 2.62 ms                                                                | 2.82 ms: 1.08x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (44): async_tree_io, sqlalchemy_imperative, json, async_tree_memoization, pprint_safe_repr, async_tree_none_tg, async_tree_none, django_template, bench_thread_pool, gc_traversal, richards_super, dulwich_log, sympy_sum, async_generators, json_loads, sympy_str, sqlglot_parse, regex_compile, k_core, coverage, async_tree_memoization_tg, asyncio_websockets, deepcopy_reduce, bpe_tokeniser, pprint_pformat, logging_format, sqlglot_optimize, sqlglot_transpile, connected_components, generators, telco, thrift, unpickle_pure_python, sqlite_synth, xml_etree_parse, coroutines, xml_etree_process, docutils, sqlglot_normalize, sphinx, shortest_path, xml_etree_iterparse, nbody, async_tree_io_tg

- Geometric mean (including insignificant results): 1.001x slower

# HPT report

- Reliability score: 55.67% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x