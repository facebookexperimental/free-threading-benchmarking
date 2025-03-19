# Results vs. base

- fork: colesbury
- ref: experiment_interp_ti
- machine: linux-x86_64
- commit hash: 62b231d
- commit date: 2025-03-19
- overall geometric mean: 1.002x slower
- HPT reliability: 99.21%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250319-vultr-x86_64-python-f5e4c2955ba5977f468e-3.14.0a6+-f5e4c29 | bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6+-62b231d |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 275 ms                                                                 | 276 ms: 1.00x slower                                                      |
| docutils       | 2.62 sec                                                               | 2.65 sec: 1.01x slower                                                    |
| html5lib       | 64.9 ms                                                                | 63.3 ms: 1.03x faster                                                     |
| sphinx         | 1.03 sec                                                               | 1.04 sec: 1.00x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20250319-vultr-x86_64-python-f5e4c2955ba5977f468e-3.14.0a6+-f5e4c29 | bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6+-62b231d |
|------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| coroutines       | 20.4 ms                                                                | 19.5 ms: 1.04x faster                                                     |
| async_generators | 321 ms                                                                 | 326 ms: 1.02x slower                                                      |
| Geometric mean   | (ref)                                                                  | 1.00x faster                                                              |

Benchmark hidden because not significant (9): async_tree_none_tg, async_tree_none, async_tree_io, async_tree_io_tg, async_tree_memoization_tg, asyncio_websockets, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250319-vultr-x86_64-python-f5e4c2955ba5977f468e-3.14.0a6+-f5e4c29 | bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6+-62b231d |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| nbody          | 119 ms                                                                 | 120 ms: 1.01x slower                                                      |
| float          | 67.7 ms                                                                | 69.1 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                              |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250319-vultr-x86_64-python-f5e4c2955ba5977f468e-3.14.0a6+-f5e4c29 | bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6+-62b231d |
|----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_dna      | 208 ms                                                                 | 188 ms: 1.11x faster                                                      |
| regex_effbot   | 3.34 ms                                                                | 3.19 ms: 1.05x faster                                                     |
| regex_v8       | 22.3 ms                                                                | 21.9 ms: 1.02x faster                                                     |
| regex_compile  | 139 ms                                                                 | 140 ms: 1.01x slower                                                      |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250319-vultr-x86_64-python-f5e4c2955ba5977f468e-3.14.0a6+-f5e4c29 | bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6+-62b231d |
|----------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_parse      | 145 ms                                                                 | 143 ms: 1.02x faster                                                      |
| pickle_pure_python   | 325 us                                                                 | 321 us: 1.01x faster                                                      |
| tomli_loads          | 2.13 sec                                                               | 2.11 sec: 1.01x faster                                                    |
| unpickle_pure_python | 226 us                                                                 | 227 us: 1.01x slower                                                      |
| xml_etree_generate   | 84.9 ms                                                                | 85.6 ms: 1.01x slower                                                     |
| xml_etree_process    | 60.1 ms                                                                | 60.9 ms: 1.01x slower                                                     |
| json_loads           | 29.1 us                                                                | 30.2 us: 1.04x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                              |

Benchmark hidden because not significant (2): xml_etree_iterparse, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250319-vultr-x86_64-python-f5e4c2955ba5977f468e-3.14.0a6+-f5e4c29 | bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6+-62b231d |
|------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 11.0 ms                                                                | 11.0 ms: 1.00x slower                                                     |
| python_startup         | 15.5 ms                                                                | 15.5 ms: 1.00x slower                                                     |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250319-vultr-x86_64-python-f5e4c2955ba5977f468e-3.14.0a6+-f5e4c29 | bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6+-62b231d |
|-----------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 51.6 ms                                                                | 52.1 ms: 1.01x slower                                                     |
| django_template | 36.8 ms                                                                | 37.2 ms: 1.01x slower                                                     |
| mako            | 14.8 ms                                                                | 14.9 ms: 1.01x slower                                                     |
| genshi_text     | 24.2 ms                                                                | 24.4 ms: 1.01x slower                                                     |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                              |

All benchmarks:
===============

| Benchmark                | bm-20250319-vultr-x86_64-python-f5e4c2955ba5977f468e-3.14.0a6+-f5e4c29 | bm-20250319-vultr-x86_64-colesbury-experiment_interp_ti-3.14.0a6+-62b231d |
|--------------------------|:----------------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_dna                | 208 ms                                                                 | 188 ms: 1.11x faster                                                      |
| gc_traversal             | 2.18 ms                                                                | 2.07 ms: 1.05x faster                                                     |
| regex_effbot             | 3.34 ms                                                                | 3.19 ms: 1.05x faster                                                     |
| coroutines               | 20.4 ms                                                                | 19.5 ms: 1.04x faster                                                     |
| meteor_contest           | 125 ms                                                                 | 120 ms: 1.04x faster                                                      |
| pyflate                  | 464 ms                                                                 | 450 ms: 1.03x faster                                                      |
| html5lib                 | 64.9 ms                                                                | 63.3 ms: 1.03x faster                                                     |
| hexiom                   | 6.69 ms                                                                | 6.58 ms: 1.02x faster                                                     |
| regex_v8                 | 22.3 ms                                                                | 21.9 ms: 1.02x faster                                                     |
| xml_etree_parse          | 145 ms                                                                 | 143 ms: 1.02x faster                                                      |
| logging_silent           | 90.7 ns                                                                | 89.3 ns: 1.02x faster                                                     |
| pickle_pure_python       | 325 us                                                                 | 321 us: 1.01x faster                                                      |
| k_core                   | 2.25 sec                                                               | 2.23 sec: 1.01x faster                                                    |
| shortest_path            | 538 ms                                                                 | 532 ms: 1.01x faster                                                      |
| bpe_tokeniser            | 4.43 sec                                                               | 4.39 sec: 1.01x faster                                                    |
| connected_components     | 506 ms                                                                 | 502 ms: 1.01x faster                                                      |
| tomli_loads              | 2.13 sec                                                               | 2.11 sec: 1.01x faster                                                    |
| scimark_sparse_mat_mult  | 4.99 ms                                                                | 4.96 ms: 1.01x faster                                                     |
| spectral_norm            | 94.9 ms                                                                | 95.2 ms: 1.00x slower                                                     |
| comprehensions           | 17.6 us                                                                | 17.6 us: 1.00x slower                                                     |
| bench_thread_pool        | 3.11 ms                                                                | 3.12 ms: 1.00x slower                                                     |
| python_startup_no_site   | 11.0 ms                                                                | 11.0 ms: 1.00x slower                                                     |
| nqueens                  | 84.5 ms                                                                | 84.9 ms: 1.00x slower                                                     |
| deepcopy                 | 267 us                                                                 | 268 us: 1.00x slower                                                      |
| 2to3                     | 275 ms                                                                 | 276 ms: 1.00x slower                                                      |
| python_startup           | 15.5 ms                                                                | 15.5 ms: 1.00x slower                                                     |
| sympy_sum                | 171 ms                                                                 | 172 ms: 1.00x slower                                                      |
| sphinx                   | 1.03 sec                                                               | 1.04 sec: 1.00x slower                                                    |
| deepcopy_memo            | 34.2 us                                                                | 34.4 us: 1.01x slower                                                     |
| bench_mp_pool            | 94.8 ms                                                                | 95.4 ms: 1.01x slower                                                     |
| chaos                    | 60.9 ms                                                                | 61.2 ms: 1.01x slower                                                     |
| deltablue                | 3.53 ms                                                                | 3.55 ms: 1.01x slower                                                     |
| fannkuch                 | 430 ms                                                                 | 433 ms: 1.01x slower                                                      |
| scimark_sor              | 113 ms                                                                 | 113 ms: 1.01x slower                                                      |
| sqlalchemy_declarative   | 148 ms                                                                 | 149 ms: 1.01x slower                                                      |
| go                       | 123 ms                                                                 | 124 ms: 1.01x slower                                                      |
| nbody                    | 119 ms                                                                 | 120 ms: 1.01x slower                                                      |
| unpickle_pure_python     | 226 us                                                                 | 227 us: 1.01x slower                                                      |
| scimark_fft              | 342 ms                                                                 | 345 ms: 1.01x slower                                                      |
| sympy_integrate          | 21.9 ms                                                                | 22.1 ms: 1.01x slower                                                     |
| many_optionals           | 1.09 ms                                                                | 1.10 ms: 1.01x slower                                                     |
| genshi_xml               | 51.6 ms                                                                | 52.1 ms: 1.01x slower                                                     |
| xml_etree_generate       | 84.9 ms                                                                | 85.6 ms: 1.01x slower                                                     |
| django_template          | 36.8 ms                                                                | 37.2 ms: 1.01x slower                                                     |
| richards                 | 46.1 ms                                                                | 46.6 ms: 1.01x slower                                                     |
| mako                     | 14.8 ms                                                                | 14.9 ms: 1.01x slower                                                     |
| genshi_text              | 24.2 ms                                                                | 24.4 ms: 1.01x slower                                                     |
| regex_compile            | 139 ms                                                                 | 140 ms: 1.01x slower                                                      |
| telco                    | 7.98 ms                                                                | 8.08 ms: 1.01x slower                                                     |
| sqlglot_v2_normalize     | 106 ms                                                                 | 107 ms: 1.01x slower                                                      |
| crypto_pyaes             | 79.9 ms                                                                | 80.9 ms: 1.01x slower                                                     |
| docutils                 | 2.62 sec                                                               | 2.65 sec: 1.01x slower                                                    |
| xml_etree_process        | 60.1 ms                                                                | 60.9 ms: 1.01x slower                                                     |
| pprint_pformat           | 1.58 sec                                                               | 1.60 sec: 1.01x slower                                                    |
| typing_runtime_protocols | 172 us                                                                 | 174 us: 1.01x slower                                                      |
| async_generators         | 321 ms                                                                 | 326 ms: 1.02x slower                                                      |
| richards_super           | 54.8 ms                                                                | 55.6 ms: 1.02x slower                                                     |
| scimark_monte_carlo      | 69.7 ms                                                                | 70.8 ms: 1.02x slower                                                     |
| pprint_safe_repr         | 769 ms                                                                 | 781 ms: 1.02x slower                                                      |
| mdp                      | 2.75 sec                                                               | 2.80 sec: 1.02x slower                                                    |
| float                    | 67.7 ms                                                                | 69.1 ms: 1.02x slower                                                     |
| raytrace                 | 282 ms                                                                 | 288 ms: 1.02x slower                                                      |
| subparsers               | 24.0 ms                                                                | 24.6 ms: 1.02x slower                                                     |
| scimark_lu               | 113 ms                                                                 | 117 ms: 1.03x slower                                                      |
| json_loads               | 29.1 us                                                                | 30.2 us: 1.04x slower                                                     |
| pycparser                | 1.11 sec                                                               | 1.15 sec: 1.04x slower                                                    |
| coverage                 | 86.3 ms                                                                | 90.4 ms: 1.05x slower                                                     |
| Geometric mean           | (ref)                                                                  | 1.00x slower                                                              |

Benchmark hidden because not significant (29): async_tree_none_tg, async_tree_none, async_tree_io, sympy_expand, async_tree_io_tg, async_tree_memoization_tg, xml_etree_iterparse, create_gc_cycles, asyncio_websockets, async_tree_cpu_io_mixed, json_dumps, dulwich_log, thrift, sympy_str, sqlglot_v2_parse, deepcopy_reduce, generators, sqlglot_v2_transpile, async_tree_memoization, pidigits, logging_simple, json, pathlib, async_tree_cpu_io_mixed_tg, logging_format, sqlite_synth, sqlglot_v2_optimize, pylint, sqlalchemy_imperative

- Geometric mean (including insignificant results): 1.002x slower

# HPT report

- Reliability score: 99.21% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x