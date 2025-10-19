# Results vs. base

- fork: Fidget-Spinner
- ref: tracing_jit
- machine: linux-x86_64
- commit hash: 9bb03a8
- commit date: 2025-10-19
- overall geometric mean: 1.007x slower
- HPT reliability: 99.11%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-9bb03a8 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                 | 251 ms: 1.01x slower                                                    |
| html5lib       | 61.0 ms                                                                | 65.7 ms: 1.08x slower                                                   |
| sphinx         | 971 ms                                                                 | 981 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                            |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-9bb03a8 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_generators           | 334 ms                                                                 | 331 ms: 1.01x faster                                                    |
| async_tree_cpu_io_mixed_tg | 471 ms                                                                 | 469 ms: 1.00x faster                                                    |
| asyncio_websockets         | 544 ms                                                                 | 545 ms: 1.00x slower                                                    |
| async_tree_none_tg         | 241 ms                                                                 | 243 ms: 1.01x slower                                                    |
| coroutines                 | 22.5 ms                                                                | 22.7 ms: 1.01x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (6): async_tree_io, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_none, async_tree_memoization_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-9bb03a8 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 67.7 ms                                                                | 62.2 ms: 1.09x faster                                                   |
| pidigits       | 195 ms                                                                 | 192 ms: 1.01x faster                                                    |
| nbody          | 88.3 ms                                                                | 87.3 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.04x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-9bb03a8 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 182 ms                                                                 | 177 ms: 1.03x faster                                                    |
| regex_v8       | 21.4 ms                                                                | 21.6 ms: 1.01x slower                                                   |
| regex_compile  | 122 ms                                                                 | 136 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                            |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-9bb03a8 |
|---------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse | 95.0 ms                                                                | 93.5 ms: 1.02x faster                                                   |
| json_dumps          | 8.99 ms                                                                | 8.87 ms: 1.01x faster                                                   |
| xml_etree_process   | 51.6 ms                                                                | 52.0 ms: 1.01x slower                                                   |
| json_loads          | 25.6 us                                                                | 26.0 us: 1.01x slower                                                   |
| xml_etree_generate  | 74.4 ms                                                                | 76.2 ms: 1.02x slower                                                   |
| tomli_loads         | 1.71 sec                                                               | 1.76 sec: 1.03x slower                                                  |
| Geometric mean      | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (3): unpickle_pure_python, xml_etree_parse, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-9bb03a8 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 12.7 ms                                                                | 12.7 ms: 1.00x faster                                                   |
| python_startup_no_site | 7.41 ms                                                                | 7.39 ms: 1.00x faster                                                   |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-9bb03a8 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 19.3 ms                                                                | 20.0 ms: 1.04x slower                                                   |
| genshi_xml      | 47.5 ms                                                                | 49.4 ms: 1.04x slower                                                   |
| django_template | 32.8 ms                                                                | 35.2 ms: 1.07x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.04x slower                                                            |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20251019-vultr-x86_64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 | bm-20251019-vultr-x86_64-Fidget%2dSpinner-tracing_jit-3.15.0a1+-9bb03a8 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                   | 37.5 ms                                                                | 29.0 ms: 1.29x faster                                                   |
| richards_super             | 43.2 ms                                                                | 33.5 ms: 1.29x faster                                                   |
| deepcopy_memo              | 24.1 us                                                                | 21.9 us: 1.10x faster                                                   |
| float                      | 67.7 ms                                                                | 62.2 ms: 1.09x faster                                                   |
| pprint_safe_repr           | 689 ms                                                                 | 649 ms: 1.06x faster                                                    |
| gc_traversal               | 4.49 ms                                                                | 4.27 ms: 1.05x faster                                                   |
| spectral_norm              | 87.2 ms                                                                | 83.1 ms: 1.05x faster                                                   |
| pprint_pformat             | 1.40 sec                                                               | 1.34 sec: 1.04x faster                                                  |
| crypto_pyaes               | 67.4 ms                                                                | 64.6 ms: 1.04x faster                                                   |
| deltablue                  | 2.89 ms                                                                | 2.78 ms: 1.04x faster                                                   |
| logging_silent             | 80.9 ns                                                                | 78.0 ns: 1.04x faster                                                   |
| scimark_fft                | 250 ms                                                                 | 242 ms: 1.03x faster                                                    |
| scimark_sparse_mat_mult    | 4.06 ms                                                                | 3.95 ms: 1.03x faster                                                   |
| comprehensions             | 15.0 us                                                                | 14.7 us: 1.03x faster                                                   |
| regex_dna                  | 182 ms                                                                 | 177 ms: 1.03x faster                                                    |
| fannkuch                   | 361 ms                                                                 | 355 ms: 1.02x faster                                                    |
| coverage                   | 75.9 ms                                                                | 74.5 ms: 1.02x faster                                                   |
| xml_etree_iterparse        | 95.0 ms                                                                | 93.5 ms: 1.02x faster                                                   |
| scimark_lu                 | 103 ms                                                                 | 101 ms: 1.02x faster                                                    |
| deepcopy_reduce            | 2.41 us                                                                | 2.38 us: 1.01x faster                                                   |
| json_dumps                 | 8.99 ms                                                                | 8.87 ms: 1.01x faster                                                   |
| pidigits                   | 195 ms                                                                 | 192 ms: 1.01x faster                                                    |
| scimark_monte_carlo        | 56.2 ms                                                                | 55.5 ms: 1.01x faster                                                   |
| nbody                      | 88.3 ms                                                                | 87.3 ms: 1.01x faster                                                   |
| scimark_sor                | 99.9 ms                                                                | 98.8 ms: 1.01x faster                                                   |
| async_generators           | 334 ms                                                                 | 331 ms: 1.01x faster                                                    |
| async_tree_cpu_io_mixed_tg | 471 ms                                                                 | 469 ms: 1.00x faster                                                    |
| python_startup             | 12.7 ms                                                                | 12.7 ms: 1.00x faster                                                   |
| python_startup_no_site     | 7.41 ms                                                                | 7.39 ms: 1.00x faster                                                   |
| asyncio_websockets         | 544 ms                                                                 | 545 ms: 1.00x slower                                                    |
| bench_mp_pool              | 12.3 ms                                                                | 12.3 ms: 1.00x slower                                                   |
| pyflate                    | 388 ms                                                                 | 391 ms: 1.01x slower                                                    |
| shortest_path              | 439 ms                                                                 | 442 ms: 1.01x slower                                                    |
| xml_etree_process          | 51.6 ms                                                                | 52.0 ms: 1.01x slower                                                   |
| 2to3                       | 249 ms                                                                 | 251 ms: 1.01x slower                                                    |
| async_tree_none_tg         | 241 ms                                                                 | 243 ms: 1.01x slower                                                    |
| regex_v8                   | 21.4 ms                                                                | 21.6 ms: 1.01x slower                                                   |
| coroutines                 | 22.5 ms                                                                | 22.7 ms: 1.01x slower                                                   |
| sphinx                     | 971 ms                                                                 | 981 ms: 1.01x slower                                                    |
| meteor_contest             | 103 ms                                                                 | 104 ms: 1.01x slower                                                    |
| typing_runtime_protocols   | 146 us                                                                 | 147 us: 1.01x slower                                                    |
| json_loads                 | 25.6 us                                                                | 26.0 us: 1.01x slower                                                   |
| telco                      | 155 ms                                                                 | 158 ms: 1.01x slower                                                    |
| sympy_integrate            | 18.4 ms                                                                | 18.7 ms: 1.02x slower                                                   |
| create_gc_cycles           | 2.00 ms                                                                | 2.03 ms: 1.02x slower                                                   |
| many_optionals             | 1.24 ms                                                                | 1.27 ms: 1.02x slower                                                   |
| sqlglot_v2_optimize        | 49.0 ms                                                                | 50.0 ms: 1.02x slower                                                   |
| sqlglot_v2_parse           | 1.17 ms                                                                | 1.20 ms: 1.02x slower                                                   |
| xml_etree_generate         | 74.4 ms                                                                | 76.2 ms: 1.02x slower                                                   |
| sqlglot_v2_transpile       | 1.46 ms                                                                | 1.50 ms: 1.03x slower                                                   |
| sympy_sum                  | 150 ms                                                                 | 154 ms: 1.03x slower                                                    |
| generators                 | 27.1 ms                                                                | 27.9 ms: 1.03x slower                                                   |
| tomli_loads                | 1.71 sec                                                               | 1.76 sec: 1.03x slower                                                  |
| genshi_text                | 19.3 ms                                                                | 20.0 ms: 1.04x slower                                                   |
| genshi_xml                 | 47.5 ms                                                                | 49.4 ms: 1.04x slower                                                   |
| subparsers                 | 45.1 ms                                                                | 47.0 ms: 1.04x slower                                                   |
| chaos                      | 50.2 ms                                                                | 52.3 ms: 1.04x slower                                                   |
| sympy_expand               | 459 ms                                                                 | 479 ms: 1.04x slower                                                    |
| deepcopy                   | 223 us                                                                 | 233 us: 1.05x slower                                                    |
| sympy_str                  | 267 ms                                                                 | 280 ms: 1.05x slower                                                    |
| thrift                     | 707 us                                                                 | 744 us: 1.05x slower                                                    |
| pycparser                  | 1.07 sec                                                               | 1.13 sec: 1.06x slower                                                  |
| hexiom                     | 5.42 ms                                                                | 5.74 ms: 1.06x slower                                                   |
| logging_format             | 6.21 us                                                                | 6.57 us: 1.06x slower                                                   |
| sqlglot_v2_normalize       | 97.2 ms                                                                | 103 ms: 1.06x slower                                                    |
| mdp                        | 1.10 sec                                                               | 1.18 sec: 1.07x slower                                                  |
| django_template            | 32.8 ms                                                                | 35.2 ms: 1.07x slower                                                   |
| nqueens                    | 74.7 ms                                                                | 80.1 ms: 1.07x slower                                                   |
| logging_simple             | 5.48 us                                                                | 5.88 us: 1.07x slower                                                   |
| html5lib                   | 61.0 ms                                                                | 65.7 ms: 1.08x slower                                                   |
| dulwich_log                | 68.8 ms                                                                | 74.6 ms: 1.08x slower                                                   |
| regex_compile              | 122 ms                                                                 | 136 ms: 1.12x slower                                                    |
| pathlib                    | 16.9 ms                                                                | 19.3 ms: 1.14x slower                                                   |
| raytrace                   | 233 ms                                                                 | 267 ms: 1.14x slower                                                    |
| go                         | 99.8 ms                                                                | 120 ms: 1.21x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (19): unpickle_pure_python, mako, k_core, xml_etree_parse, async_tree_io, bpe_tokeniser, regex_effbot, async_tree_io_tg, bench_thread_pool, docutils, async_tree_cpu_io_mixed, json, connected_components, async_tree_none, async_tree_memoization_tg, pickle_pure_python, sqlite_synth, async_tree_memoization, pylint

- Geometric mean (including insignificant results): 1.007x slower

# HPT report

- Reliability score: 99.11% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x