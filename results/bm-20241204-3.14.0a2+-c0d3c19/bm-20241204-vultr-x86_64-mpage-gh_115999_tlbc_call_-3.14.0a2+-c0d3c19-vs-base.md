# Results vs. base

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: c0d3c19
- commit date: 2024-12-04
- overall geometric mean: 1.002x faster
- HPT reliability: 98.04%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

Benchmark hidden because not significant (3): 2to3, docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|--------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_generators   | 369 ms                                                                 | 362 ms: 1.02x faster                                                  |
| async_tree_none_tg | 263 ms                                                                 | 261 ms: 1.01x faster                                                  |
| coroutines         | 22.1 ms                                                                | 21.9 ms: 1.01x faster                                                 |
| Geometric mean     | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (8): async_tree_io, async_tree_none, async_tree_io_tg, async_tree_memoization_tg, async_tree_memoization, asyncio_websockets, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 94.9 ms                                                                | 93.8 ms: 1.01x faster                                                 |
| float          | 78.1 ms                                                                | 77.4 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 173 ms                                                                 | 169 ms: 1.03x faster                                                  |
| regex_effbot   | 2.79 ms                                                                | 2.77 ms: 1.00x faster                                                 |
| regex_compile  | 129 ms                                                                 | 128 ms: 1.00x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|--------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python | 317 us                                                                 | 314 us: 1.01x faster                                                  |
| xml_etree_parse    | 129 ms                                                                 | 130 ms: 1.01x slower                                                  |
| xml_etree_generate | 84.9 ms                                                                | 86.0 ms: 1.01x slower                                                 |
| json_dumps         | 11.4 ms                                                                | 11.6 ms: 1.02x slower                                                 |
| xml_etree_process  | 59.3 ms                                                                | 60.5 ms: 1.02x slower                                                 |
| Geometric mean     | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (4): xml_etree_iterparse, unpickle_pure_python, tomli_loads, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.47 ms                                                                | 7.47 ms: 1.00x faster                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako           | 11.8 ms                                                                | 11.6 ms: 1.01x faster                                                 |
| genshi_text    | 22.3 ms                                                                | 22.0 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (2): genshi_xml, django_template

All benchmarks:
===============

| Benchmark               | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|-------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna               | 173 ms                                                                 | 169 ms: 1.03x faster                                                  |
| spectral_norm           | 113 ms                                                                 | 110 ms: 1.03x faster                                                  |
| deepcopy_reduce         | 2.65 us                                                                | 2.60 us: 1.02x faster                                                 |
| richards                | 46.6 ms                                                                | 45.7 ms: 1.02x faster                                                 |
| crypto_pyaes            | 68.3 ms                                                                | 67.0 ms: 1.02x faster                                                 |
| async_generators        | 369 ms                                                                 | 362 ms: 1.02x faster                                                  |
| logging_silent          | 106 ns                                                                 | 104 ns: 1.02x faster                                                  |
| mako                    | 11.8 ms                                                                | 11.6 ms: 1.01x faster                                                 |
| create_gc_cycles        | 1.86 ms                                                                | 1.84 ms: 1.01x faster                                                 |
| fannkuch                | 379 ms                                                                 | 375 ms: 1.01x faster                                                  |
| nbody                   | 94.9 ms                                                                | 93.8 ms: 1.01x faster                                                 |
| go                      | 120 ms                                                                 | 119 ms: 1.01x faster                                                  |
| genshi_text             | 22.3 ms                                                                | 22.0 ms: 1.01x faster                                                 |
| generators              | 28.7 ms                                                                | 28.4 ms: 1.01x faster                                                 |
| async_tree_none_tg      | 263 ms                                                                 | 261 ms: 1.01x faster                                                  |
| richards_super          | 52.4 ms                                                                | 51.9 ms: 1.01x faster                                                 |
| float                   | 78.1 ms                                                                | 77.4 ms: 1.01x faster                                                 |
| telco                   | 7.27 ms                                                                | 7.21 ms: 1.01x faster                                                 |
| pickle_pure_python      | 317 us                                                                 | 314 us: 1.01x faster                                                  |
| sqlglot_optimize        | 53.9 ms                                                                | 53.4 ms: 1.01x faster                                                 |
| scimark_sor             | 134 ms                                                                 | 132 ms: 1.01x faster                                                  |
| sqlite_synth            | 2.24 us                                                                | 2.22 us: 1.01x faster                                                 |
| hexiom                  | 5.87 ms                                                                | 5.82 ms: 1.01x faster                                                 |
| coroutines              | 22.1 ms                                                                | 21.9 ms: 1.01x faster                                                 |
| pathlib                 | 18.2 ms                                                                | 18.1 ms: 1.01x faster                                                 |
| scimark_monte_carlo     | 65.2 ms                                                                | 64.8 ms: 1.01x faster                                                 |
| sqlglot_parse           | 1.29 ms                                                                | 1.28 ms: 1.01x faster                                                 |
| sqlglot_transpile       | 1.61 ms                                                                | 1.60 ms: 1.01x faster                                                 |
| comprehensions          | 17.6 us                                                                | 17.5 us: 1.00x faster                                                 |
| regex_effbot            | 2.79 ms                                                                | 2.77 ms: 1.00x faster                                                 |
| raytrace                | 264 ms                                                                 | 262 ms: 1.00x faster                                                  |
| chaos                   | 58.9 ms                                                                | 58.6 ms: 1.00x faster                                                 |
| regex_compile           | 129 ms                                                                 | 128 ms: 1.00x faster                                                  |
| python_startup_no_site  | 7.47 ms                                                                | 7.47 ms: 1.00x faster                                                 |
| bench_thread_pool       | 1.01 ms                                                                | 1.02 ms: 1.00x slower                                                 |
| gc_traversal            | 4.26 ms                                                                | 4.28 ms: 1.00x slower                                                 |
| sqlalchemy_imperative   | 18.9 ms                                                                | 19.1 ms: 1.01x slower                                                 |
| xml_etree_parse         | 129 ms                                                                 | 130 ms: 1.01x slower                                                  |
| mdp                     | 2.47 sec                                                               | 2.49 sec: 1.01x slower                                                |
| pprint_pformat          | 1.46 sec                                                               | 1.48 sec: 1.01x slower                                                |
| thrift                  | 734 us                                                                 | 744 us: 1.01x slower                                                  |
| xml_etree_generate      | 84.9 ms                                                                | 86.0 ms: 1.01x slower                                                 |
| json_dumps              | 11.4 ms                                                                | 11.6 ms: 1.02x slower                                                 |
| xml_etree_process       | 59.3 ms                                                                | 60.5 ms: 1.02x slower                                                 |
| scimark_sparse_mat_mult | 4.39 ms                                                                | 4.50 ms: 1.02x slower                                                 |
| coverage                | 78.8 ms                                                                | 81.0 ms: 1.03x slower                                                 |
| Geometric mean          | (ref)                                                                  | 1.00x faster                                                          |

Benchmark hidden because not significant (49): async_tree_io, async_tree_none, async_tree_io_tg, sympy_expand, shortest_path, pylint, logging_format, genshi_xml, async_tree_memoization_tg, bench_mp_pool, k_core, deltablue, pyflate, docutils, sqlglot_normalize, subparsers, sqlalchemy_declarative, deepcopy_memo, meteor_contest, async_tree_memoization, sphinx, bpe_tokeniser, asyncio_websockets, sympy_sum, python_startup, 2to3, xml_etree_iterparse, regex_v8, unpickle_pure_python, deepcopy, connected_components, pycparser, sympy_integrate, dulwich_log, typing_runtime_protocols, async_tree_cpu_io_mixed_tg, logging_simple, scimark_fft, pidigits, scimark_lu, sympy_str, django_template, many_optionals, async_tree_cpu_io_mixed, pprint_safe_repr, nqueens, tomli_loads, json_loads, json

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 98.04% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x