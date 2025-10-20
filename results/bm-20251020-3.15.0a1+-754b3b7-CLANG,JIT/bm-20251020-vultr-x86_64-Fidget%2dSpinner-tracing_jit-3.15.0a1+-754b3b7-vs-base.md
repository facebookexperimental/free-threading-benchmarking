# Results vs. base

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: 754b3b7
- commit date: 2025-10-20
- overall geometric mean: 1.010x slower
- HPT reliability: 99.63%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-754b3b7 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 250 ms                                                                 | 253 ms: 1.01x slower                                                    |
| docutils       | 2.56 sec                                                               | 2.58 sec: 1.01x slower                                                  |
| html5lib       | 59.0 ms                                                                | 66.0 ms: 1.12x slower                                                   |
| sphinx         | 970 ms                                                                 | 988 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-754b3b7 |
|------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| coroutines       | 22.8 ms                                                                | 22.4 ms: 1.02x faster                                                   |
| async_generators | 339 ms                                                                 | 334 ms: 1.02x faster                                                    |
| async_tree_io    | 587 ms                                                                 | 593 ms: 1.01x slower                                                    |
| Geometric mean   | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (8): asyncio_websockets, async_tree_cpu_io_mixed_tg, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_memoization_tg, async_tree_none, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-754b3b7 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 67.0 ms                                                                | 62.3 ms: 1.08x faster                                                   |
| pidigits       | 193 ms                                                                 | 194 ms: 1.01x slower                                                    |
| nbody          | 86.3 ms                                                                | 98.8 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-754b3b7 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.11 ms                                                                | 2.95 ms: 1.05x faster                                                   |
| regex_dna      | 187 ms                                                                 | 180 ms: 1.04x faster                                                    |
| regex_compile  | 121 ms                                                                 | 137 ms: 1.13x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-754b3b7 |
|---------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_parse     | 148 ms                                                                 | 143 ms: 1.04x faster                                                    |
| xml_etree_iterparse | 96.8 ms                                                                | 93.7 ms: 1.03x faster                                                   |
| json_dumps          | 9.00 ms                                                                | 8.84 ms: 1.02x faster                                                   |
| json_loads          | 25.9 us                                                                | 25.7 us: 1.01x faster                                                   |
| xml_etree_process   | 51.8 ms                                                                | 52.4 ms: 1.01x slower                                                   |
| xml_etree_generate  | 75.1 ms                                                                | 76.2 ms: 1.01x slower                                                   |
| pickle_pure_python  | 297 us                                                                 | 304 us: 1.02x slower                                                    |
| tomli_loads         | 1.73 sec                                                               | 2.00 sec: 1.16x slower                                                  |
| Geometric mean      | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-754b3b7 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 12.7 ms                                                                | 12.7 ms: 1.00x faster                                                   |
| python_startup_no_site | 7.41 ms                                                                | 7.40 ms: 1.00x faster                                                   |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-754b3b7 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 11.2 ms                                                                | 11.2 ms: 1.00x slower                                                   |
| genshi_text     | 19.4 ms                                                                | 19.8 ms: 1.02x slower                                                   |
| django_template | 33.4 ms                                                                | 34.5 ms: 1.03x slower                                                   |
| genshi_xml      | 47.2 ms                                                                | 49.6 ms: 1.05x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.03x slower                                                            |

All benchmarks:
===============

| Benchmark                | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251020-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-754b3b7 |
|--------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                 | 37.3 ms                                                                | 29.0 ms: 1.29x faster                                                   |
| richards_super           | 42.8 ms                                                                | 33.7 ms: 1.27x faster                                                   |
| deepcopy_memo            | 24.5 us                                                                | 22.3 us: 1.10x faster                                                   |
| float                    | 67.0 ms                                                                | 62.3 ms: 1.08x faster                                                   |
| pprint_safe_repr         | 695 ms                                                                 | 651 ms: 1.07x faster                                                    |
| deltablue                | 2.96 ms                                                                | 2.78 ms: 1.06x faster                                                   |
| regex_effbot             | 3.11 ms                                                                | 2.95 ms: 1.05x faster                                                   |
| gc_traversal             | 4.48 ms                                                                | 4.27 ms: 1.05x faster                                                   |
| scimark_lu               | 100 ms                                                                 | 96.1 ms: 1.04x faster                                                   |
| pprint_pformat           | 1.40 sec                                                               | 1.35 sec: 1.04x faster                                                  |
| regex_dna                | 187 ms                                                                 | 180 ms: 1.04x faster                                                    |
| xml_etree_parse          | 148 ms                                                                 | 143 ms: 1.04x faster                                                    |
| xml_etree_iterparse      | 96.8 ms                                                                | 93.7 ms: 1.03x faster                                                   |
| scimark_sor              | 101 ms                                                                 | 98.3 ms: 1.03x faster                                                   |
| comprehensions           | 15.1 us                                                                | 14.8 us: 1.02x faster                                                   |
| logging_silent           | 80.2 ns                                                                | 78.6 ns: 1.02x faster                                                   |
| coroutines               | 22.8 ms                                                                | 22.4 ms: 1.02x faster                                                   |
| spectral_norm            | 86.7 ms                                                                | 85.1 ms: 1.02x faster                                                   |
| json_dumps               | 9.00 ms                                                                | 8.84 ms: 1.02x faster                                                   |
| async_generators         | 339 ms                                                                 | 334 ms: 1.02x faster                                                    |
| scimark_sparse_mat_mult  | 3.99 ms                                                                | 3.93 ms: 1.02x faster                                                   |
| deepcopy_reduce          | 2.39 us                                                                | 2.37 us: 1.01x faster                                                   |
| fannkuch                 | 358 ms                                                                 | 355 ms: 1.01x faster                                                    |
| json_loads               | 25.9 us                                                                | 25.7 us: 1.01x faster                                                   |
| bench_mp_pool            | 12.4 ms                                                                | 12.3 ms: 1.01x faster                                                   |
| python_startup           | 12.7 ms                                                                | 12.7 ms: 1.00x faster                                                   |
| python_startup_no_site   | 7.41 ms                                                                | 7.40 ms: 1.00x faster                                                   |
| mako                     | 11.2 ms                                                                | 11.2 ms: 1.00x slower                                                   |
| coverage                 | 74.5 ms                                                                | 75.0 ms: 1.01x slower                                                   |
| typing_runtime_protocols | 145 us                                                                 | 146 us: 1.01x slower                                                    |
| pidigits                 | 193 ms                                                                 | 194 ms: 1.01x slower                                                    |
| docutils                 | 2.56 sec                                                               | 2.58 sec: 1.01x slower                                                  |
| create_gc_cycles         | 2.01 ms                                                                | 2.03 ms: 1.01x slower                                                   |
| connected_components     | 403 ms                                                                 | 407 ms: 1.01x slower                                                    |
| async_tree_io            | 587 ms                                                                 | 593 ms: 1.01x slower                                                    |
| 2to3                     | 250 ms                                                                 | 253 ms: 1.01x slower                                                    |
| xml_etree_process        | 51.8 ms                                                                | 52.4 ms: 1.01x slower                                                   |
| xml_etree_generate       | 75.1 ms                                                                | 76.2 ms: 1.01x slower                                                   |
| shortest_path            | 440 ms                                                                 | 447 ms: 1.02x slower                                                    |
| pyflate                  | 386 ms                                                                 | 392 ms: 1.02x slower                                                    |
| sphinx                   | 970 ms                                                                 | 988 ms: 1.02x slower                                                    |
| sympy_integrate          | 18.4 ms                                                                | 18.7 ms: 1.02x slower                                                   |
| genshi_text              | 19.4 ms                                                                | 19.8 ms: 1.02x slower                                                   |
| pycparser                | 1.12 sec                                                               | 1.14 sec: 1.02x slower                                                  |
| sympy_sum                | 150 ms                                                                 | 154 ms: 1.02x slower                                                    |
| pickle_pure_python       | 297 us                                                                 | 304 us: 1.02x slower                                                    |
| sqlglot_v2_transpile     | 1.46 ms                                                                | 1.50 ms: 1.03x slower                                                   |
| django_template          | 33.4 ms                                                                | 34.5 ms: 1.03x slower                                                   |
| sqlglot_v2_parse         | 1.17 ms                                                                | 1.21 ms: 1.03x slower                                                   |
| chaos                    | 50.2 ms                                                                | 52.1 ms: 1.04x slower                                                   |
| many_optionals           | 1.24 ms                                                                | 1.29 ms: 1.04x slower                                                   |
| meteor_contest           | 103 ms                                                                 | 107 ms: 1.04x slower                                                    |
| sympy_str                | 267 ms                                                                 | 279 ms: 1.04x slower                                                    |
| sympy_expand             | 459 ms                                                                 | 479 ms: 1.04x slower                                                    |
| sqlglot_v2_optimize      | 48.5 ms                                                                | 50.7 ms: 1.05x slower                                                   |
| deepcopy                 | 225 us                                                                 | 236 us: 1.05x slower                                                    |
| genshi_xml               | 47.2 ms                                                                | 49.6 ms: 1.05x slower                                                   |
| logging_format           | 6.28 us                                                                | 6.61 us: 1.05x slower                                                   |
| logging_simple           | 5.58 us                                                                | 5.89 us: 1.05x slower                                                   |
| sqlglot_v2_normalize     | 97.2 ms                                                                | 103 ms: 1.06x slower                                                    |
| subparsers               | 44.9 ms                                                                | 47.4 ms: 1.06x slower                                                   |
| mdp                      | 1.11 sec                                                               | 1.18 sec: 1.06x slower                                                  |
| thrift                   | 711 us                                                                 | 759 us: 1.07x slower                                                    |
| nqueens                  | 74.7 ms                                                                | 80.1 ms: 1.07x slower                                                   |
| dulwich_log              | 68.7 ms                                                                | 73.8 ms: 1.07x slower                                                   |
| hexiom                   | 5.47 ms                                                                | 5.94 ms: 1.09x slower                                                   |
| html5lib                 | 59.0 ms                                                                | 66.0 ms: 1.12x slower                                                   |
| regex_compile            | 121 ms                                                                 | 137 ms: 1.13x slower                                                    |
| raytrace                 | 236 ms                                                                 | 267 ms: 1.13x slower                                                    |
| pathlib                  | 16.9 ms                                                                | 19.2 ms: 1.14x slower                                                   |
| nbody                    | 86.3 ms                                                                | 98.8 ms: 1.14x slower                                                   |
| tomli_loads              | 1.73 sec                                                               | 2.00 sec: 1.16x slower                                                  |
| go                       | 99.5 ms                                                                | 121 ms: 1.21x slower                                                    |
| Geometric mean           | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (21): k_core, scimark_fft, unpickle_pure_python, sqlite_synth, json, regex_v8, bpe_tokeniser, asyncio_websockets, telco, async_tree_cpu_io_mixed_tg, generators, async_tree_io_tg, bench_thread_pool, async_tree_cpu_io_mixed, scimark_monte_carlo, async_tree_none_tg, async_tree_memoization_tg, async_tree_none, crypto_pyaes, async_tree_memoization, pylint

- Geometric mean (including insignificant results): 1.010x slower

# HPT report

- Reliability score: 99.63% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x