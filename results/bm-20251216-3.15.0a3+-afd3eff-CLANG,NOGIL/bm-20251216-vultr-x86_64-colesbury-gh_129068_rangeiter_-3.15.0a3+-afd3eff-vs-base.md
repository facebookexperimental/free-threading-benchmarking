# Results vs. base

- fork: colesbury
- ref: gh_129068_rangeiter_
- machine: linux-x86_64
- commit hash: afd3eff
- commit date: 2025-12-16
- overall geometric mean: 1.001x faster
- HPT reliability: 57.74%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251216-vultr-x86_64-python-16a305f15242ed2acac9-3.15.0a3+-16a305f | bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3+-afd3eff |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 270 ms                                                                 | 269 ms: 1.01x faster                                                      |
| docutils       | 2.67 sec                                                               | 2.65 sec: 1.01x faster                                                    |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20251216-vultr-x86_64-python-16a305f15242ed2acac9-3.15.0a3+-16a305f | bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3+-afd3eff |
|-------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| coroutines              | 22.6 ms                                                                | 21.9 ms: 1.03x faster                                                     |
| async_generators        | 335 ms                                                                 | 338 ms: 1.01x slower                                                      |
| async_tree_cpu_io_mixed | 506 ms                                                                 | 514 ms: 1.01x slower                                                      |
| async_tree_io_tg        | 561 ms                                                                 | 573 ms: 1.02x slower                                                      |
| Geometric mean          | (ref)                                                                  | 1.00x slower                                                              |

Benchmark hidden because not significant (7): async_tree_none, asyncio_websockets, async_tree_memoization, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251216-vultr-x86_64-python-16a305f15242ed2acac9-3.15.0a3+-16a305f | bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3+-afd3eff |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 190 ms                                                                 | 192 ms: 1.01x slower                                                      |
| nbody          | 116 ms                                                                 | 117 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                              |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251216-vultr-x86_64-python-16a305f15242ed2acac9-3.15.0a3+-16a305f | bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3+-afd3eff |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.44 ms                                                                | 3.39 ms: 1.01x faster                                                     |
| regex_dna      | 207 ms                                                                 | 206 ms: 1.00x faster                                                      |
| regex_v8       | 24.2 ms                                                                | 24.1 ms: 1.00x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                              |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251216-vultr-x86_64-python-16a305f15242ed2acac9-3.15.0a3+-16a305f | bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3+-afd3eff |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_parse      | 148 ms                                                                 | 143 ms: 1.04x faster                                                      |
| xml_etree_iterparse  | 86.8 ms                                                                | 84.1 ms: 1.03x faster                                                     |
| pickle_pure_python   | 319 us                                                                 | 313 us: 1.02x faster                                                      |
| json_loads           | 28.6 us                                                                | 28.4 us: 1.01x faster                                                     |
| unpickle_pure_python | 222 us                                                                 | 221 us: 1.01x faster                                                      |
| xml_etree_process    | 61.0 ms                                                                | 62.2 ms: 1.02x slower                                                     |
| tomli_loads          | 2.09 sec                                                               | 2.16 sec: 1.03x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (2): json_dumps, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251216-vultr-x86_64-python-16a305f15242ed2acac9-3.15.0a3+-16a305f | bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3+-afd3eff |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 9.59 ms                                                                | 9.59 ms: 1.00x faster                                                     |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20251216-vultr-x86_64-python-16a305f15242ed2acac9-3.15.0a3+-16a305f | bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3+-afd3eff |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_text    | 23.4 ms                                                                | 22.9 ms: 1.02x faster                                                     |
| mako           | 15.1 ms                                                                | 15.1 ms: 1.01x faster                                                     |
| genshi_xml     | 50.7 ms                                                                | 50.4 ms: 1.00x faster                                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                              |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                | bm-20251216-vultr-x86_64-python-16a305f15242ed2acac9-3.15.0a3+-16a305f | bm-20251216-vultr-x86_64-colesbury-gh_129068_rangeiter_-3.15.0a3+-afd3eff |
|--------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_parse          | 148 ms                                                                 | 143 ms: 1.04x faster                                                      |
| coroutines               | 22.6 ms                                                                | 21.9 ms: 1.03x faster                                                     |
| xml_etree_iterparse      | 86.8 ms                                                                | 84.1 ms: 1.03x faster                                                     |
| subparsers               | 10.1 ms                                                                | 9.80 ms: 1.03x faster                                                     |
| genshi_text              | 23.4 ms                                                                | 22.9 ms: 1.02x faster                                                     |
| pathlib                  | 17.4 ms                                                                | 17.1 ms: 1.02x faster                                                     |
| pickle_pure_python       | 319 us                                                                 | 313 us: 1.02x faster                                                      |
| richards                 | 46.8 ms                                                                | 45.9 ms: 1.02x faster                                                     |
| regex_effbot             | 3.44 ms                                                                | 3.39 ms: 1.01x faster                                                     |
| pprint_pformat           | 1.51 sec                                                               | 1.49 sec: 1.01x faster                                                    |
| pprint_safe_repr         | 729 ms                                                                 | 720 ms: 1.01x faster                                                      |
| pyflate                  | 430 ms                                                                 | 425 ms: 1.01x faster                                                      |
| sympy_sum                | 168 ms                                                                 | 166 ms: 1.01x faster                                                      |
| scimark_lu               | 109 ms                                                                 | 108 ms: 1.01x faster                                                      |
| richards_super           | 53.9 ms                                                                | 53.4 ms: 1.01x faster                                                     |
| json_loads               | 28.6 us                                                                | 28.4 us: 1.01x faster                                                     |
| nqueens                  | 83.9 ms                                                                | 83.2 ms: 1.01x faster                                                     |
| sqlglot_v2_optimize      | 51.6 ms                                                                | 51.2 ms: 1.01x faster                                                     |
| docutils                 | 2.67 sec                                                               | 2.65 sec: 1.01x faster                                                    |
| generators               | 28.3 ms                                                                | 28.1 ms: 1.01x faster                                                     |
| mako                     | 15.1 ms                                                                | 15.1 ms: 1.01x faster                                                     |
| mdp                      | 1.26 sec                                                               | 1.26 sec: 1.01x faster                                                    |
| unpickle_pure_python     | 222 us                                                                 | 221 us: 1.01x faster                                                      |
| 2to3                     | 270 ms                                                                 | 269 ms: 1.01x faster                                                      |
| genshi_xml               | 50.7 ms                                                                | 50.4 ms: 1.00x faster                                                     |
| sympy_integrate          | 20.7 ms                                                                | 20.6 ms: 1.00x faster                                                     |
| shortest_path            | 532 ms                                                                 | 530 ms: 1.00x faster                                                      |
| regex_dna                | 207 ms                                                                 | 206 ms: 1.00x faster                                                      |
| scimark_monte_carlo      | 69.6 ms                                                                | 69.4 ms: 1.00x faster                                                     |
| regex_v8                 | 24.2 ms                                                                | 24.1 ms: 1.00x faster                                                     |
| k_core                   | 2.16 sec                                                               | 2.16 sec: 1.00x faster                                                    |
| deepcopy_memo            | 28.6 us                                                                | 28.5 us: 1.00x faster                                                     |
| logging_silent           | 86.7 ns                                                                | 86.5 ns: 1.00x faster                                                     |
| python_startup_no_site   | 9.59 ms                                                                | 9.59 ms: 1.00x faster                                                     |
| fannkuch                 | 412 ms                                                                 | 412 ms: 1.00x slower                                                      |
| comprehensions           | 16.3 us                                                                | 16.3 us: 1.00x slower                                                     |
| telco                    | 167 ms                                                                 | 168 ms: 1.00x slower                                                      |
| bpe_tokeniser            | 4.21 sec                                                               | 4.23 sec: 1.00x slower                                                    |
| hexiom                   | 6.04 ms                                                                | 6.07 ms: 1.01x slower                                                     |
| sympy_expand             | 501 ms                                                                 | 505 ms: 1.01x slower                                                      |
| connected_components     | 491 ms                                                                 | 494 ms: 1.01x slower                                                      |
| thrift                   | 853 us                                                                 | 860 us: 1.01x slower                                                      |
| pidigits                 | 190 ms                                                                 | 192 ms: 1.01x slower                                                      |
| deepcopy                 | 245 us                                                                 | 247 us: 1.01x slower                                                      |
| async_generators         | 335 ms                                                                 | 338 ms: 1.01x slower                                                      |
| logging_simple           | 6.40 us                                                                | 6.48 us: 1.01x slower                                                     |
| typing_runtime_protocols | 170 us                                                                 | 172 us: 1.01x slower                                                      |
| chaos                    | 57.4 ms                                                                | 58.2 ms: 1.01x slower                                                     |
| async_tree_cpu_io_mixed  | 506 ms                                                                 | 514 ms: 1.01x slower                                                      |
| nbody                    | 116 ms                                                                 | 117 ms: 1.01x slower                                                      |
| xml_etree_process        | 61.0 ms                                                                | 62.2 ms: 1.02x slower                                                     |
| async_tree_io_tg         | 561 ms                                                                 | 573 ms: 1.02x slower                                                      |
| logging_format           | 7.31 us                                                                | 7.46 us: 1.02x slower                                                     |
| meteor_contest           | 118 ms                                                                 | 121 ms: 1.02x slower                                                      |
| tomli_loads              | 2.09 sec                                                               | 2.16 sec: 1.03x slower                                                    |
| dulwich_log              | 71.3 ms                                                                | 73.6 ms: 1.03x slower                                                     |
| Geometric mean           | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (38): sympy_str, async_tree_none, deepcopy_reduce, django_template, go, bench_mp_pool, many_optionals, sqlglot_v2_normalize, float, create_gc_cycles, pylint, gc_traversal, asyncio_websockets, sphinx, python_startup, deltablue, spectral_norm, json_dumps, json, regex_compile, raytrace, pycparser, sqlglot_v2_parse, crypto_pyaes, scimark_sor, bench_thread_pool, coverage, xml_etree_generate, scimark_fft, sqlglot_v2_transpile, html5lib, async_tree_memoization, sqlite_synth, scimark_sparse_mat_mult, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_io

- Geometric mean (including insignificant results): 1.001x faster

# HPT report

- Reliability score: 57.74% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x