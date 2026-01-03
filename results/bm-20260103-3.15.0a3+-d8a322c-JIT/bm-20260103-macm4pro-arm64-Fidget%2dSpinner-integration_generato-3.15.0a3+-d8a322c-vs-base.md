# Results vs. base

- fork: Fidget-Spinner
- ref: integration_generato
- machine: darwin-arm64
- commit hash: d8a322c
- commit date: 2026-01-03
- overall geometric mean: 1.001x slower
- HPT reliability: 86.98%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3+-b538c28 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-integration_generato-3.15.0a3+-d8a322c |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| 2to3           | 110 ms                                                                   | 110 ms: 1.01x slower                                                               |
| docutils       | 1.01 sec                                                                 | 1.01 sec: 1.01x slower                                                             |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                                       |

Benchmark hidden because not significant (2): html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                     | bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3+-b538c28 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-integration_generato-3.15.0a3+-d8a322c |
|-------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| async_tree_eager              | 38.0 ms                                                                  | 36.9 ms: 1.03x faster                                                              |
| async_tree_none               | 98.4 ms                                                                  | 96.2 ms: 1.02x faster                                                              |
| async_tree_cpu_io_mixed       | 247 ms                                                                   | 242 ms: 1.02x faster                                                               |
| async_tree_cpu_io_mixed_tg    | 252 ms                                                                   | 247 ms: 1.02x faster                                                               |
| async_tree_io                 | 230 ms                                                                   | 226 ms: 1.02x faster                                                               |
| async_tree_none_tg            | 97.7 ms                                                                  | 96.4 ms: 1.01x faster                                                              |
| async_tree_eager_cpu_io_mixed | 218 ms                                                                   | 215 ms: 1.01x faster                                                               |
| async_generators              | 181 ms                                                                   | 192 ms: 1.06x slower                                                               |
| Geometric mean                | (ref)                                                                    | 1.01x faster                                                                       |

Benchmark hidden because not significant (9): async_tree_io_tg, async_tree_memoization_tg, async_tree_memoization, async_tree_eager_io, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io_tg, async_tree_eager_memoization_tg, async_tree_eager_tg, coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3+-b538c28 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-integration_generato-3.15.0a3+-d8a322c |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| nbody          | 40.2 ms                                                                  | 40.1 ms: 1.00x faster                                                              |
| pidigits       | 161 ms                                                                   | 163 ms: 1.01x slower                                                               |
| float          | 22.7 ms                                                                  | 23.0 ms: 1.01x slower                                                              |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3+-b538c28 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-integration_generato-3.15.0a3+-d8a322c |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| regex_compile  | 41.1 ms                                                                  | 40.8 ms: 1.01x faster                                                              |
| regex_v8       | 9.66 ms                                                                  | 9.81 ms: 1.01x slower                                                              |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                                       |

Benchmark hidden because not significant (2): regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3+-b538c28 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-integration_generato-3.15.0a3+-d8a322c |
|---------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| xml_etree_parse     | 62.4 ms                                                                  | 61.0 ms: 1.02x faster                                                              |
| xml_etree_iterparse | 38.8 ms                                                                  | 37.9 ms: 1.02x faster                                                              |
| xml_etree_process   | 22.1 ms                                                                  | 22.0 ms: 1.00x faster                                                              |
| json_dumps          | 3.64 ms                                                                  | 3.66 ms: 1.01x slower                                                              |
| tomli_loads         | 772 ms                                                                   | 780 ms: 1.01x slower                                                               |
| pickle_pure_python  | 110 us                                                                   | 112 us: 1.01x slower                                                               |
| Geometric mean      | (ref)                                                                    | 1.00x faster                                                                       |

Benchmark hidden because not significant (3): json_loads, xml_etree_generate, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3+-b538c28 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-integration_generato-3.15.0a3+-d8a322c |
|------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| python_startup         | 8.78 ms                                                                  | 8.84 ms: 1.01x slower                                                              |
| python_startup_no_site | 6.32 ms                                                                  | 6.37 ms: 1.01x slower                                                              |
| Geometric mean         | (ref)                                                                    | 1.01x slower                                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3+-b538c28 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-integration_generato-3.15.0a3+-d8a322c |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| genshi_xml     | 21.7 ms                                                                  | 20.3 ms: 1.07x faster                                                              |
| genshi_text    | 9.07 ms                                                                  | 8.75 ms: 1.04x faster                                                              |
| mako           | 3.91 ms                                                                  | 3.93 ms: 1.01x slower                                                              |
| Geometric mean | (ref)                                                                    | 1.03x faster                                                                       |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                     | bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3+-b538c28 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-integration_generato-3.15.0a3+-d8a322c |
|-------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| genshi_xml                    | 21.7 ms                                                                  | 20.3 ms: 1.07x faster                                                              |
| genshi_text                   | 9.07 ms                                                                  | 8.75 ms: 1.04x faster                                                              |
| deepcopy_reduce               | 1.00 us                                                                  | 965 ns: 1.04x faster                                                               |
| async_tree_eager              | 38.0 ms                                                                  | 36.9 ms: 1.03x faster                                                              |
| xml_etree_parse               | 62.4 ms                                                                  | 61.0 ms: 1.02x faster                                                              |
| async_tree_none               | 98.4 ms                                                                  | 96.2 ms: 1.02x faster                                                              |
| xml_etree_iterparse           | 38.8 ms                                                                  | 37.9 ms: 1.02x faster                                                              |
| async_tree_cpu_io_mixed       | 247 ms                                                                   | 242 ms: 1.02x faster                                                               |
| async_tree_cpu_io_mixed_tg    | 252 ms                                                                   | 247 ms: 1.02x faster                                                               |
| telco                         | 2.63 ms                                                                  | 2.58 ms: 1.02x faster                                                              |
| async_tree_io                 | 230 ms                                                                   | 226 ms: 1.02x faster                                                               |
| nqueens                       | 38.9 ms                                                                  | 38.4 ms: 1.01x faster                                                              |
| async_tree_none_tg            | 97.7 ms                                                                  | 96.4 ms: 1.01x faster                                                              |
| typing_runtime_protocols      | 62.6 us                                                                  | 61.8 us: 1.01x faster                                                              |
| deepcopy                      | 97.8 us                                                                  | 96.7 us: 1.01x faster                                                              |
| async_tree_eager_cpu_io_mixed | 218 ms                                                                   | 215 ms: 1.01x faster                                                               |
| regex_compile                 | 41.1 ms                                                                  | 40.8 ms: 1.01x faster                                                              |
| coverage                      | 33.3 ms                                                                  | 33.1 ms: 1.01x faster                                                              |
| pathlib                       | 10.8 ms                                                                  | 10.8 ms: 1.01x faster                                                              |
| xml_etree_process             | 22.1 ms                                                                  | 22.0 ms: 1.00x faster                                                              |
| shortest_path                 | 216 ms                                                                   | 215 ms: 1.00x faster                                                               |
| many_optionals                | 250 us                                                                   | 250 us: 1.00x faster                                                               |
| scimark_sor                   | 42.2 ms                                                                  | 42.1 ms: 1.00x faster                                                              |
| nbody                         | 40.2 ms                                                                  | 40.1 ms: 1.00x faster                                                              |
| bpe_tokeniser                 | 1.84 sec                                                                 | 1.84 sec: 1.00x faster                                                             |
| spectral_norm                 | 40.9 ms                                                                  | 41.0 ms: 1.00x slower                                                              |
| dulwich_log                   | 18.7 ms                                                                  | 18.8 ms: 1.00x slower                                                              |
| sympy_sum                     | 56.2 ms                                                                  | 56.5 ms: 1.00x slower                                                              |
| generators                    | 18.5 ms                                                                  | 18.6 ms: 1.00x slower                                                              |
| subparsers                    | 3.90 ms                                                                  | 3.92 ms: 1.01x slower                                                              |
| sqlglot_v2_transpile          | 578 us                                                                   | 581 us: 1.01x slower                                                               |
| mako                          | 3.91 ms                                                                  | 3.93 ms: 1.01x slower                                                              |
| hexiom                        | 2.63 ms                                                                  | 2.65 ms: 1.01x slower                                                              |
| json_dumps                    | 3.64 ms                                                                  | 3.66 ms: 1.01x slower                                                              |
| docutils                      | 1.01 sec                                                                 | 1.01 sec: 1.01x slower                                                             |
| mdp                           | 583 ms                                                                   | 587 ms: 1.01x slower                                                               |
| scimark_fft                   | 101 ms                                                                   | 101 ms: 1.01x slower                                                               |
| python_startup                | 8.78 ms                                                                  | 8.84 ms: 1.01x slower                                                              |
| crypto_pyaes                  | 30.7 ms                                                                  | 30.9 ms: 1.01x slower                                                              |
| python_startup_no_site        | 6.32 ms                                                                  | 6.37 ms: 1.01x slower                                                              |
| logging_format                | 2.31 us                                                                  | 2.33 us: 1.01x slower                                                              |
| scimark_lu                    | 36.7 ms                                                                  | 37.0 ms: 1.01x slower                                                              |
| raytrace                      | 106 ms                                                                   | 107 ms: 1.01x slower                                                               |
| pidigits                      | 161 ms                                                                   | 163 ms: 1.01x slower                                                               |
| 2to3                          | 110 ms                                                                   | 110 ms: 1.01x slower                                                               |
| sqlglot_v2_parse              | 452 us                                                                   | 456 us: 1.01x slower                                                               |
| tomli_loads                   | 772 ms                                                                   | 780 ms: 1.01x slower                                                               |
| pyflate                       | 142 ms                                                                   | 144 ms: 1.01x slower                                                               |
| deepcopy_memo                 | 11.2 us                                                                  | 11.3 us: 1.01x slower                                                              |
| logging_simple                | 2.09 us                                                                  | 2.11 us: 1.01x slower                                                              |
| float                         | 22.7 ms                                                                  | 23.0 ms: 1.01x slower                                                              |
| gc_traversal                  | 2.05 ms                                                                  | 2.07 ms: 1.01x slower                                                              |
| pprint_pformat                | 515 ms                                                                   | 521 ms: 1.01x slower                                                               |
| meteor_contest                | 45.6 ms                                                                  | 46.2 ms: 1.01x slower                                                              |
| thrift                        | 302 us                                                                   | 305 us: 1.01x slower                                                               |
| logging_silent                | 33.9 ns                                                                  | 34.4 ns: 1.01x slower                                                              |
| create_gc_cycles              | 919 us                                                                   | 931 us: 1.01x slower                                                               |
| go                            | 42.6 ms                                                                  | 43.2 ms: 1.01x slower                                                              |
| sqlite_synth                  | 962 ns                                                                   | 974 ns: 1.01x slower                                                               |
| sympy_integrate               | 7.53 ms                                                                  | 7.63 ms: 1.01x slower                                                              |
| pickle_pure_python            | 110 us                                                                   | 112 us: 1.01x slower                                                               |
| regex_v8                      | 9.66 ms                                                                  | 9.81 ms: 1.01x slower                                                              |
| richards_super                | 11.4 ms                                                                  | 11.6 ms: 1.02x slower                                                              |
| chaos                         | 21.9 ms                                                                  | 22.2 ms: 1.02x slower                                                              |
| sympy_str                     | 104 ms                                                                   | 106 ms: 1.02x slower                                                               |
| fannkuch                      | 150 ms                                                                   | 153 ms: 1.02x slower                                                               |
| richards                      | 9.52 ms                                                                  | 9.85 ms: 1.04x slower                                                              |
| async_generators              | 181 ms                                                                   | 192 ms: 1.06x slower                                                               |
| Geometric mean                | (ref)                                                                    | 1.00x slower                                                                       |

Benchmark hidden because not significant (32): async_tree_io_tg, async_tree_memoization_tg, async_tree_memoization, async_tree_eager_io, async_tree_eager_cpu_io_mixed_tg, async_tree_eager_io_tg, async_tree_eager_memoization_tg, async_tree_eager_tg, bench_thread_pool, sqlglot_v2_normalize, json_loads, regex_dna, scimark_monte_carlo, xml_etree_generate, django_template, connected_components, k_core, json, comprehensions, bench_mp_pool, scimark_sparse_mat_mult, deltablue, pylint, sqlglot_v2_optimize, html5lib, pprint_safe_repr, sympy_expand, unpickle_pure_python, regex_effbot, pycparser, sphinx, coroutines
Ignored benchmarks (2) of results/bm-20260102-3.15.0a3+-b538c28-JIT/bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3+-b538c28.json: async_tree_eager_memoization, asyncio_websockets

- Geometric mean (including insignificant results): 1.001x slower

# HPT report

- Reliability score: 86.98% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x