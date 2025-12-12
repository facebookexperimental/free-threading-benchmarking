# Results vs. base

- fork: colesbury
- ref: gh_120321_gen_atomic
- machine: linux-x86_64
- commit hash: bc054db
- commit date: 2025-12-11
- overall geometric mean: 1.002x faster
- HPT reliability: 94.82%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251211-vultr-x86_64-python-dac4589726952be873df-3.15.0a2+-dac4589 | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 248 ms                                                                 | 246 ms: 1.01x faster                                                      |
| html5lib       | 59.3 ms                                                                | 60.4 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                              |

Benchmark hidden because not significant (2): docutils, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20251211-vultr-x86_64-python-dac4589726952be873df-3.15.0a2+-dac4589 | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| coroutines       | 24.4 ms                                                                | 23.3 ms: 1.05x faster                                                     |
| async_tree_io_tg | 587 ms                                                                 | 582 ms: 1.01x faster                                                      |
| Geometric mean   | (ref)                                                                  | 1.01x faster                                                              |

Benchmark hidden because not significant (9): async_tree_io, async_tree_memoization, async_tree_cpu_io_mixed, async_generators, asyncio_websockets, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_none_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251211-vultr-x86_64-python-dac4589726952be873df-3.15.0a2+-dac4589 | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 70.9 ms                                                                | 68.1 ms: 1.04x faster                                                     |
| pidigits       | 204 ms                                                                 | 198 ms: 1.03x faster                                                      |
| nbody          | 89.4 ms                                                                | 88.1 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251211-vultr-x86_64-python-dac4589726952be873df-3.15.0a2+-dac4589 | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 123 ms                                                                 | 123 ms: 1.00x slower                                                      |
| regex_effbot   | 2.78 ms                                                                | 3.05 ms: 1.10x slower                                                     |
| regex_dna      | 173 ms                                                                 | 190 ms: 1.10x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.05x slower                                                              |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20251211-vultr-x86_64-python-dac4589726952be873df-3.15.0a2+-dac4589 | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|---------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps          | 9.92 ms                                                                | 9.79 ms: 1.01x faster                                                     |
| json_loads          | 28.0 us                                                                | 27.8 us: 1.01x faster                                                     |
| xml_etree_process   | 57.9 ms                                                                | 57.6 ms: 1.01x faster                                                     |
| xml_etree_iterparse | 84.8 ms                                                                | 84.4 ms: 1.00x faster                                                     |
| tomli_loads         | 2.15 sec                                                               | 2.18 sec: 1.01x slower                                                    |
| Geometric mean      | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (4): xml_etree_generate, xml_etree_parse, pickle_pure_python, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251211-vultr-x86_64-python-dac4589726952be873df-3.15.0a2+-dac4589 | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 12.5 ms                                                                | 12.4 ms: 1.01x faster                                                     |
| python_startup_no_site | 7.30 ms                                                                | 7.25 ms: 1.01x faster                                                     |
| Geometric mean         | (ref)                                                                  | 1.01x faster                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20251211-vultr-x86_64-python-dac4589726952be873df-3.15.0a2+-dac4589 | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako           | 12.0 ms                                                                | 11.8 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (3): django_template, genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20251211-vultr-x86_64-python-dac4589726952be873df-3.15.0a2+-dac4589 | bm-20251211-vultr-x86_64-colesbury-gh_120321_gen_atomic-3.15.0a2+-bc054db |
|--------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| coroutines               | 24.4 ms                                                                | 23.3 ms: 1.05x faster                                                     |
| float                    | 70.9 ms                                                                | 68.1 ms: 1.04x faster                                                     |
| create_gc_cycles         | 1.88 ms                                                                | 1.82 ms: 1.03x faster                                                     |
| pidigits                 | 204 ms                                                                 | 198 ms: 1.03x faster                                                      |
| scimark_sparse_mat_mult  | 4.37 ms                                                                | 4.24 ms: 1.03x faster                                                     |
| gc_traversal             | 4.29 ms                                                                | 4.18 ms: 1.03x faster                                                     |
| comprehensions           | 16.0 us                                                                | 15.6 us: 1.02x faster                                                     |
| scimark_lu               | 111 ms                                                                 | 109 ms: 1.02x faster                                                      |
| logging_simple           | 5.90 us                                                                | 5.79 us: 1.02x faster                                                     |
| pyflate                  | 428 ms                                                                 | 421 ms: 1.01x faster                                                      |
| sympy_integrate          | 19.0 ms                                                                | 18.7 ms: 1.01x faster                                                     |
| nbody                    | 89.4 ms                                                                | 88.1 ms: 1.01x faster                                                     |
| json_dumps               | 9.92 ms                                                                | 9.79 ms: 1.01x faster                                                     |
| typing_runtime_protocols | 155 us                                                                 | 153 us: 1.01x faster                                                      |
| spectral_norm            | 96.5 ms                                                                | 95.4 ms: 1.01x faster                                                     |
| sympy_sum                | 155 ms                                                                 | 153 ms: 1.01x faster                                                      |
| richards_super           | 48.6 ms                                                                | 48.1 ms: 1.01x faster                                                     |
| sqlglot_v2_transpile     | 1.50 ms                                                                | 1.48 ms: 1.01x faster                                                     |
| sympy_str                | 276 ms                                                                 | 272 ms: 1.01x faster                                                      |
| deepcopy_reduce          | 2.63 us                                                                | 2.60 us: 1.01x faster                                                     |
| pprint_safe_repr         | 700 ms                                                                 | 692 ms: 1.01x faster                                                      |
| mako                     | 12.0 ms                                                                | 11.8 ms: 1.01x faster                                                     |
| json                     | 5.05 ms                                                                | 5.00 ms: 1.01x faster                                                     |
| generators               | 27.7 ms                                                                | 27.4 ms: 1.01x faster                                                     |
| k_core                   | 1.89 sec                                                               | 1.87 sec: 1.01x faster                                                    |
| python_startup           | 12.5 ms                                                                | 12.4 ms: 1.01x faster                                                     |
| sqlglot_v2_parse         | 1.20 ms                                                                | 1.19 ms: 1.01x faster                                                     |
| json_loads               | 28.0 us                                                                | 27.8 us: 1.01x faster                                                     |
| 2to3                     | 248 ms                                                                 | 246 ms: 1.01x faster                                                      |
| crypto_pyaes             | 69.7 ms                                                                | 69.1 ms: 1.01x faster                                                     |
| telco                    | 157 ms                                                                 | 156 ms: 1.01x faster                                                      |
| async_tree_io_tg         | 587 ms                                                                 | 582 ms: 1.01x faster                                                      |
| python_startup_no_site   | 7.30 ms                                                                | 7.25 ms: 1.01x faster                                                     |
| go                       | 107 ms                                                                 | 106 ms: 1.01x faster                                                      |
| xml_etree_process        | 57.9 ms                                                                | 57.6 ms: 1.01x faster                                                     |
| connected_components     | 388 ms                                                                 | 386 ms: 1.01x faster                                                      |
| deepcopy_memo            | 27.0 us                                                                | 26.9 us: 1.00x faster                                                     |
| xml_etree_iterparse      | 84.8 ms                                                                | 84.4 ms: 1.00x faster                                                     |
| deltablue                | 3.34 ms                                                                | 3.33 ms: 1.00x faster                                                     |
| richards                 | 42.4 ms                                                                | 42.3 ms: 1.00x faster                                                     |
| raytrace                 | 251 ms                                                                 | 250 ms: 1.00x faster                                                      |
| regex_compile            | 123 ms                                                                 | 123 ms: 1.00x slower                                                      |
| deepcopy                 | 244 us                                                                 | 244 us: 1.00x slower                                                      |
| mdp                      | 1.15 sec                                                               | 1.15 sec: 1.00x slower                                                    |
| bpe_tokeniser            | 4.17 sec                                                               | 4.20 sec: 1.01x slower                                                    |
| hexiom                   | 5.72 ms                                                                | 5.77 ms: 1.01x slower                                                     |
| subparsers               | 9.09 ms                                                                | 9.19 ms: 1.01x slower                                                     |
| coverage                 | 81.1 ms                                                                | 82.2 ms: 1.01x slower                                                     |
| tomli_loads              | 2.15 sec                                                               | 2.18 sec: 1.01x slower                                                    |
| many_optionals           | 933 us                                                                 | 946 us: 1.01x slower                                                      |
| html5lib                 | 59.3 ms                                                                | 60.4 ms: 1.02x slower                                                     |
| scimark_monte_carlo      | 62.4 ms                                                                | 63.7 ms: 1.02x slower                                                     |
| pycparser                | 1.09 sec                                                               | 1.11 sec: 1.02x slower                                                    |
| scimark_fft              | 298 ms                                                                 | 305 ms: 1.02x slower                                                      |
| regex_effbot             | 2.78 ms                                                                | 3.05 ms: 1.10x slower                                                     |
| regex_dna                | 173 ms                                                                 | 190 ms: 1.10x slower                                                      |
| bench_mp_pool            | 278 ms                                                                 | 329 ms: 1.18x slower                                                      |
| Geometric mean           | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (37): async_tree_io, thrift, pylint, regex_v8, async_tree_memoization, dulwich_log, async_tree_cpu_io_mixed, xml_etree_generate, xml_etree_parse, pathlib, sqlglot_v2_optimize, async_generators, sympy_expand, scimark_sor, django_template, pprint_pformat, asyncio_websockets, bench_thread_pool, genshi_text, async_tree_cpu_io_mixed_tg, shortest_path, pickle_pure_python, fannkuch, chaos, nqueens, docutils, genshi_xml, logging_silent, async_tree_memoization_tg, meteor_contest, unpickle_pure_python, sphinx, sqlglot_v2_normalize, async_tree_none_tg, logging_format, async_tree_none, sqlite_synth

- Geometric mean (including insignificant results): 1.002x faster

# HPT report

- Reliability score: 94.82% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x