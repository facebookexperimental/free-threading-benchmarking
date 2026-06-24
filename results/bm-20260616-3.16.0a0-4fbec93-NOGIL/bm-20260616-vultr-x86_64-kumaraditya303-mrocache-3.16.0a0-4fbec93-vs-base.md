# Results vs. base

- fork: kumaraditya303
- ref: mrocache
- machine: linux-x86_64
- commit hash: 4fbec93
- commit date: 2026-06-16
- overall geometric mean: 1.005x slower
- HPT reliability: 99.96%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 296 ms                                                                | 297 ms: 1.01x slower                                              |
| docutils       | 2.95 sec                                                              | 2.93 sec: 1.01x faster                                            |
| html5lib       | 66.9 ms                                                               | 68.6 ms: 1.02x slower                                             |
| sphinx         | 1.11 sec                                                              | 1.11 sec: 1.00x faster                                            |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|-------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_io           | 705 ms                                                                | 709 ms: 1.00x slower                                              |
| async_tree_none         | 341 ms                                                                | 345 ms: 1.01x slower                                              |
| async_tree_cpu_io_mixed | 598 ms                                                                | 605 ms: 1.01x slower                                              |
| Geometric mean          | (ref)                                                                 | 1.00x slower                                                      |

Benchmark hidden because not significant (8): async_tree_io_tg, asyncio_websockets, async_generators, coroutines, async_tree_memoization, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| nbody          | 126 ms                                                                | 125 ms: 1.01x faster                                              |
| float          | 86.5 ms                                                               | 86.9 ms: 1.01x slower                                             |
| pidigits       | 180 ms                                                                | 188 ms: 1.05x slower                                              |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_compile  | 140 ms                                                                | 142 ms: 1.02x slower                                              |
| regex_v8       | 21.1 ms                                                               | 21.6 ms: 1.02x slower                                             |
| regex_dna      | 184 ms                                                                | 188 ms: 1.02x slower                                              |
| regex_effbot   | 3.07 ms                                                               | 3.14 ms: 1.02x slower                                             |
| Geometric mean | (ref)                                                                 | 1.02x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle_pure_python   | 340 us                                                                | 335 us: 1.02x faster                                              |
| json_loads           | 30.1 us                                                               | 29.8 us: 1.01x faster                                             |
| xml_etree_generate   | 102 ms                                                                | 102 ms: 1.01x faster                                              |
| unpickle_pure_python | 238 us                                                                | 239 us: 1.00x slower                                              |
| tomli_loads          | 1.95 sec                                                              | 1.98 sec: 1.02x slower                                            |
| json_dumps           | 10.5 ms                                                               | 10.7 ms: 1.02x slower                                             |
| Geometric mean       | (ref)                                                                 | 1.00x slower                                                      |

Benchmark hidden because not significant (3): xml_etree_iterparse, xml_etree_process, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup_no_site | 9.16 ms                                                               | 9.18 ms: 1.00x slower                                             |
| python_startup         | 15.4 ms                                                               | 15.6 ms: 1.01x slower                                             |
| Geometric mean         | (ref)                                                                 | 1.01x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako            | 16.1 ms                                                               | 15.9 ms: 1.02x faster                                             |
| django_template | 39.9 ms                                                               | 41.8 ms: 1.05x slower                                             |
| Geometric mean  | (ref)                                                                 | 1.02x slower                                                      |

All benchmarks:
===============

| Benchmark                | bm-20260615-vultr-x86_64-python-11f032f904c8019b332a-3.16.0a0-11f032f | bm-20260616-vultr-x86_64-kumaraditya303-mrocache-3.16.0a0-4fbec93 |
|--------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| scimark_sparse_mat_mult  | 5.48 ms                                                               | 5.30 ms: 1.03x faster                                             |
| scimark_fft              | 357 ms                                                                | 348 ms: 1.03x faster                                              |
| generators               | 33.7 ms                                                               | 33.1 ms: 1.02x faster                                             |
| fannkuch                 | 466 ms                                                                | 458 ms: 1.02x faster                                              |
| spectral_norm            | 112 ms                                                                | 110 ms: 1.02x faster                                              |
| pickle_pure_python       | 340 us                                                                | 335 us: 1.02x faster                                              |
| mako                     | 16.1 ms                                                               | 15.9 ms: 1.02x faster                                             |
| comprehensions           | 17.8 us                                                               | 17.6 us: 1.01x faster                                             |
| dulwich_log              | 71.1 ms                                                               | 70.4 ms: 1.01x faster                                             |
| bench_mp_pool            | 6.83 ms                                                               | 6.76 ms: 1.01x faster                                             |
| subparsers               | 10.5 ms                                                               | 10.4 ms: 1.01x faster                                             |
| telco                    | 177 ms                                                                | 175 ms: 1.01x faster                                              |
| json_loads               | 30.1 us                                                               | 29.8 us: 1.01x faster                                             |
| nbody                    | 126 ms                                                                | 125 ms: 1.01x faster                                              |
| xml_etree_generate       | 102 ms                                                                | 102 ms: 1.01x faster                                              |
| docutils                 | 2.95 sec                                                              | 2.93 sec: 1.01x faster                                            |
| sphinx                   | 1.11 sec                                                              | 1.11 sec: 1.00x faster                                            |
| raytrace                 | 308 ms                                                                | 307 ms: 1.00x faster                                              |
| gc_traversal             | 1.78 ms                                                               | 1.78 ms: 1.00x faster                                             |
| nqueens                  | 88.2 ms                                                               | 88.0 ms: 1.00x faster                                             |
| deepcopy                 | 268 us                                                                | 267 us: 1.00x faster                                              |
| unpickle_pure_python     | 238 us                                                                | 239 us: 1.00x slower                                              |
| python_startup_no_site   | 9.16 ms                                                               | 9.18 ms: 1.00x slower                                             |
| connected_components     | 488 ms                                                                | 489 ms: 1.00x slower                                              |
| bpe_tokeniser            | 4.41 sec                                                              | 4.42 sec: 1.00x slower                                            |
| mdp                      | 1.31 sec                                                              | 1.32 sec: 1.00x slower                                            |
| async_tree_io            | 705 ms                                                                | 709 ms: 1.00x slower                                              |
| float                    | 86.5 ms                                                               | 86.9 ms: 1.01x slower                                             |
| sympy_integrate          | 21.8 ms                                                               | 21.9 ms: 1.01x slower                                             |
| go                       | 121 ms                                                                | 122 ms: 1.01x slower                                              |
| 2to3                     | 296 ms                                                                | 297 ms: 1.01x slower                                              |
| bench_thread_pool        | 1.47 ms                                                               | 1.48 ms: 1.01x slower                                             |
| sympy_sum                | 180 ms                                                                | 181 ms: 1.01x slower                                              |
| pyflate                  | 459 ms                                                                | 463 ms: 1.01x slower                                              |
| richards_super           | 60.0 ms                                                               | 60.7 ms: 1.01x slower                                             |
| many_optionals           | 1.00 ms                                                               | 1.01 ms: 1.01x slower                                             |
| async_tree_none          | 341 ms                                                                | 345 ms: 1.01x slower                                              |
| scimark_monte_carlo      | 79.1 ms                                                               | 80.0 ms: 1.01x slower                                             |
| python_startup           | 15.4 ms                                                               | 15.6 ms: 1.01x slower                                             |
| async_tree_cpu_io_mixed  | 598 ms                                                                | 605 ms: 1.01x slower                                              |
| richards                 | 52.5 ms                                                               | 53.1 ms: 1.01x slower                                             |
| logging_silent           | 107 ns                                                                | 108 ns: 1.01x slower                                              |
| create_gc_cycles         | 1.35 ms                                                               | 1.37 ms: 1.01x slower                                             |
| deepcopy_memo            | 31.0 us                                                               | 31.4 us: 1.01x slower                                             |
| pprint_safe_repr         | 796 ms                                                                | 807 ms: 1.01x slower                                              |
| shortest_path            | 534 ms                                                                | 541 ms: 1.01x slower                                              |
| typing_runtime_protocols | 145 us                                                                | 147 us: 1.01x slower                                              |
| pprint_pformat           | 1.65 sec                                                              | 1.68 sec: 1.01x slower                                            |
| k_core                   | 2.24 sec                                                              | 2.28 sec: 1.02x slower                                            |
| regex_compile            | 140 ms                                                                | 142 ms: 1.02x slower                                              |
| deltablue                | 3.67 ms                                                               | 3.73 ms: 1.02x slower                                             |
| tomli_loads              | 1.95 sec                                                              | 1.98 sec: 1.02x slower                                            |
| sympy_expand             | 522 ms                                                                | 531 ms: 1.02x slower                                              |
| json_dumps               | 10.5 ms                                                               | 10.7 ms: 1.02x slower                                             |
| logging_format           | 7.90 us                                                               | 8.05 us: 1.02x slower                                             |
| coverage                 | 113 ms                                                                | 115 ms: 1.02x slower                                              |
| sympy_str                | 312 ms                                                                | 318 ms: 1.02x slower                                              |
| regex_v8                 | 21.1 ms                                                               | 21.6 ms: 1.02x slower                                             |
| thrift                   | 899 us                                                                | 919 us: 1.02x slower                                              |
| pycparser                | 1.18 sec                                                              | 1.20 sec: 1.02x slower                                            |
| regex_dna                | 184 ms                                                                | 188 ms: 1.02x slower                                              |
| regex_effbot             | 3.07 ms                                                               | 3.14 ms: 1.02x slower                                             |
| html5lib                 | 66.9 ms                                                               | 68.6 ms: 1.02x slower                                             |
| meteor_contest           | 124 ms                                                                | 129 ms: 1.04x slower                                              |
| logging_simple           | 6.89 us                                                               | 7.16 us: 1.04x slower                                             |
| pidigits                 | 180 ms                                                                | 188 ms: 1.05x slower                                              |
| django_template          | 39.9 ms                                                               | 41.8 ms: 1.05x slower                                             |
| Geometric mean           | (ref)                                                                 | 1.01x slower                                                      |

Benchmark hidden because not significant (25): async_tree_io_tg, pathlib, asyncio_websockets, xml_etree_iterparse, scimark_lu, sqlglot_v2_normalize, xml_etree_process, chaos, sqlite_synth, async_generators, hexiom, coroutines, crypto_pyaes, xml_etree_parse, sqlglot_v2_parse, scimark_sor, async_tree_memoization, async_tree_cpu_io_mixed_tg, deepcopy_reduce, sqlglot_v2_optimize, json, sqlglot_v2_transpile, async_tree_memoization_tg, async_tree_none_tg, pylint

- Geometric mean (including insignificant results): 1.005x slower

# HPT report

- Reliability score: 99.96% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x