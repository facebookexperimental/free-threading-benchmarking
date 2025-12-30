# Results vs. base

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: darwin-arm64
- commit hash: 9f28e87
- commit date: 2025-12-30
- overall geometric mean: 1.021x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-9f28e87 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 110 ms                                                                   | 113 ms: 1.03x slower                                                         |
| docutils       | 1.01 sec                                                                 | 1.03 sec: 1.02x slower                                                       |
| html5lib       | 20.1 ms                                                                  | 20.5 ms: 1.02x slower                                                        |
| sphinx         | 391 ms                                                                   | 407 ms: 1.04x slower                                                         |
| Geometric mean | (ref)                                                                    | 1.03x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-9f28e87 |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_io_tg                 | 224 ms                                                                   | 216 ms: 1.04x faster                                                         |
| async_tree_none_tg               | 98.2 ms                                                                  | 94.9 ms: 1.03x faster                                                        |
| async_tree_memoization_tg        | 136 ms                                                                   | 132 ms: 1.03x faster                                                         |
| coroutines                       | 10.2 ms                                                                  | 10.1 ms: 1.01x faster                                                        |
| asyncio_websockets               | 188 ms                                                                   | 189 ms: 1.01x slower                                                         |
| async_tree_eager                 | 38.5 ms                                                                  | 38.8 ms: 1.01x slower                                                        |
| async_tree_eager_cpu_io_mixed    | 220 ms                                                                   | 223 ms: 1.01x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 240 ms                                                                   | 245 ms: 1.02x slower                                                         |
| Geometric mean                   | (ref)                                                                    | 1.00x faster                                                                 |

Benchmark hidden because not significant (11): async_tree_memoization, async_tree_eager_io, async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_none, async_tree_cpu_io_mixed, async_tree_eager_io_tg, async_generators, async_tree_eager_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-9f28e87 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 39.7 ms                                                                  | 39.9 ms: 1.00x slower                                                        |
| pidigits       | 162 ms                                                                   | 165 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                                    | 1.01x slower                                                                 |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-9f28e87 |
|----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 96.9 ms                                                                  | 96.2 ms: 1.01x faster                                                        |
| regex_compile  | 40.4 ms                                                                  | 46.0 ms: 1.14x slower                                                        |
| Geometric mean | (ref)                                                                    | 1.03x slower                                                                 |

Benchmark hidden because not significant (2): regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-9f28e87 |
|----------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| xml_etree_parse      | 63.9 ms                                                                  | 62.6 ms: 1.02x faster                                                        |
| json_loads           | 10.6 us                                                                  | 10.5 us: 1.01x faster                                                        |
| json_dumps           | 3.68 ms                                                                  | 3.70 ms: 1.01x slower                                                        |
| tomli_loads          | 796 ms                                                                   | 801 ms: 1.01x slower                                                         |
| unpickle_pure_python | 72.5 us                                                                  | 73.2 us: 1.01x slower                                                        |
| pickle_pure_python   | 112 us                                                                   | 114 us: 1.02x slower                                                         |
| xml_etree_generate   | 31.4 ms                                                                  | 32.0 ms: 1.02x slower                                                        |
| xml_etree_process    | 21.9 ms                                                                  | 22.4 ms: 1.02x slower                                                        |
| Geometric mean       | (ref)                                                                    | 1.01x slower                                                                 |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-9f28e87 |
|------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 6.35 ms                                                                  | 6.43 ms: 1.01x slower                                                        |
| python_startup         | 8.81 ms                                                                  | 8.93 ms: 1.01x slower                                                        |
| Geometric mean         | (ref)                                                                    | 1.01x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-9f28e87 |
|-----------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 13.9 ms                                                                  | 13.6 ms: 1.02x faster                                                        |
| mako            | 4.14 ms                                                                  | 4.19 ms: 1.01x slower                                                        |
| genshi_text     | 8.99 ms                                                                  | 9.89 ms: 1.10x slower                                                        |
| genshi_xml      | 21.1 ms                                                                  | 23.4 ms: 1.11x slower                                                        |
| Geometric mean  | (ref)                                                                    | 1.05x slower                                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d | bm-20251230-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-9f28e87 |
|----------------------------------|:------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| logging_simple                   | 2.14 us                                                                  | 1.87 us: 1.14x faster                                                        |
| logging_format                   | 2.34 us                                                                  | 2.05 us: 1.14x faster                                                        |
| scimark_sor                      | 42.3 ms                                                                  | 38.1 ms: 1.11x faster                                                        |
| coverage                         | 33.8 ms                                                                  | 31.9 ms: 1.06x faster                                                        |
| async_tree_io_tg                 | 224 ms                                                                   | 216 ms: 1.04x faster                                                         |
| async_tree_none_tg               | 98.2 ms                                                                  | 94.9 ms: 1.03x faster                                                        |
| async_tree_memoization_tg        | 136 ms                                                                   | 132 ms: 1.03x faster                                                         |
| xml_etree_parse                  | 63.9 ms                                                                  | 62.6 ms: 1.02x faster                                                        |
| django_template                  | 13.9 ms                                                                  | 13.6 ms: 1.02x faster                                                        |
| telco                            | 2.61 ms                                                                  | 2.57 ms: 1.02x faster                                                        |
| coroutines                       | 10.2 ms                                                                  | 10.1 ms: 1.01x faster                                                        |
| json_loads                       | 10.6 us                                                                  | 10.5 us: 1.01x faster                                                        |
| sqlite_synth                     | 974 ns                                                                   | 966 ns: 1.01x faster                                                         |
| regex_dna                        | 96.9 ms                                                                  | 96.2 ms: 1.01x faster                                                        |
| raytrace                         | 106 ms                                                                   | 106 ms: 1.00x faster                                                         |
| k_core                           | 864 ms                                                                   | 867 ms: 1.00x slower                                                         |
| nbody                            | 39.7 ms                                                                  | 39.9 ms: 1.00x slower                                                        |
| crypto_pyaes                     | 31.1 ms                                                                  | 31.3 ms: 1.00x slower                                                        |
| dulwich_log                      | 18.7 ms                                                                  | 18.8 ms: 1.00x slower                                                        |
| shortest_path                    | 215 ms                                                                   | 216 ms: 1.00x slower                                                         |
| subparsers                       | 3.92 ms                                                                  | 3.94 ms: 1.00x slower                                                        |
| json_dumps                       | 3.68 ms                                                                  | 3.70 ms: 1.01x slower                                                        |
| tomli_loads                      | 796 ms                                                                   | 801 ms: 1.01x slower                                                         |
| asyncio_websockets               | 188 ms                                                                   | 189 ms: 1.01x slower                                                         |
| json                             | 1.85 ms                                                                  | 1.87 ms: 1.01x slower                                                        |
| async_tree_eager                 | 38.5 ms                                                                  | 38.8 ms: 1.01x slower                                                        |
| bench_thread_pool                | 429 us                                                                   | 432 us: 1.01x slower                                                         |
| unpickle_pure_python             | 72.5 us                                                                  | 73.2 us: 1.01x slower                                                        |
| typing_runtime_protocols         | 62.9 us                                                                  | 63.6 us: 1.01x slower                                                        |
| mako                             | 4.14 ms                                                                  | 4.19 ms: 1.01x slower                                                        |
| meteor_contest                   | 44.9 ms                                                                  | 45.4 ms: 1.01x slower                                                        |
| python_startup_no_site           | 6.35 ms                                                                  | 6.43 ms: 1.01x slower                                                        |
| scimark_monte_carlo              | 22.7 ms                                                                  | 23.0 ms: 1.01x slower                                                        |
| bpe_tokeniser                    | 1.85 sec                                                                 | 1.87 sec: 1.01x slower                                                       |
| deepcopy_reduce                  | 1.03 us                                                                  | 1.04 us: 1.01x slower                                                        |
| python_startup                   | 8.81 ms                                                                  | 8.93 ms: 1.01x slower                                                        |
| async_tree_eager_cpu_io_mixed    | 220 ms                                                                   | 223 ms: 1.01x slower                                                         |
| docutils                         | 1.01 sec                                                                 | 1.03 sec: 1.02x slower                                                       |
| bench_mp_pool                    | 44.7 ms                                                                  | 45.4 ms: 1.02x slower                                                        |
| fannkuch                         | 154 ms                                                                   | 157 ms: 1.02x slower                                                         |
| scimark_sparse_mat_mult          | 1.92 ms                                                                  | 1.95 ms: 1.02x slower                                                        |
| pidigits                         | 162 ms                                                                   | 165 ms: 1.02x slower                                                         |
| logging_silent                   | 33.2 ns                                                                  | 33.8 ns: 1.02x slower                                                        |
| thrift                           | 290 us                                                                   | 295 us: 1.02x slower                                                         |
| nqueens                          | 38.8 ms                                                                  | 39.5 ms: 1.02x slower                                                        |
| many_optionals                   | 254 us                                                                   | 259 us: 1.02x slower                                                         |
| pickle_pure_python               | 112 us                                                                   | 114 us: 1.02x slower                                                         |
| pathlib                          | 10.8 ms                                                                  | 11.0 ms: 1.02x slower                                                        |
| xml_etree_generate               | 31.4 ms                                                                  | 32.0 ms: 1.02x slower                                                        |
| html5lib                         | 20.1 ms                                                                  | 20.5 ms: 1.02x slower                                                        |
| create_gc_cycles                 | 919 us                                                                   | 937 us: 1.02x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 240 ms                                                                   | 245 ms: 1.02x slower                                                         |
| sqlglot_v2_normalize             | 48.6 ms                                                                  | 49.6 ms: 1.02x slower                                                        |
| xml_etree_process                | 21.9 ms                                                                  | 22.4 ms: 1.02x slower                                                        |
| 2to3                             | 110 ms                                                                   | 113 ms: 1.03x slower                                                         |
| gc_traversal                     | 2.06 ms                                                                  | 2.12 ms: 1.03x slower                                                        |
| sphinx                           | 391 ms                                                                   | 407 ms: 1.04x slower                                                         |
| deepcopy                         | 99.1 us                                                                  | 103 us: 1.04x slower                                                         |
| deltablue                        | 1.13 ms                                                                  | 1.20 ms: 1.06x slower                                                        |
| sympy_expand                     | 176 ms                                                                   | 187 ms: 1.06x slower                                                         |
| pprint_pformat                   | 529 ms                                                                   | 568 ms: 1.08x slower                                                         |
| go                               | 42.7 ms                                                                  | 46.0 ms: 1.08x slower                                                        |
| pyflate                          | 143 ms                                                                   | 154 ms: 1.08x slower                                                         |
| pprint_safe_repr                 | 259 ms                                                                   | 280 ms: 1.08x slower                                                         |
| hexiom                           | 2.61 ms                                                                  | 2.83 ms: 1.09x slower                                                        |
| sympy_integrate                  | 7.63 ms                                                                  | 8.34 ms: 1.09x slower                                                        |
| genshi_text                      | 8.99 ms                                                                  | 9.89 ms: 1.10x slower                                                        |
| genshi_xml                       | 21.1 ms                                                                  | 23.4 ms: 1.11x slower                                                        |
| mdp                              | 578 ms                                                                   | 645 ms: 1.12x slower                                                         |
| sympy_sum                        | 56.8 ms                                                                  | 63.5 ms: 1.12x slower                                                        |
| sqlglot_v2_optimize              | 24.6 ms                                                                  | 27.7 ms: 1.12x slower                                                        |
| scimark_lu                       | 36.7 ms                                                                  | 41.5 ms: 1.13x slower                                                        |
| generators                       | 18.9 ms                                                                  | 21.4 ms: 1.13x slower                                                        |
| regex_compile                    | 40.4 ms                                                                  | 46.0 ms: 1.14x slower                                                        |
| sympy_str                        | 106 ms                                                                   | 122 ms: 1.15x slower                                                         |
| richards_super                   | 11.5 ms                                                                  | 13.2 ms: 1.15x slower                                                        |
| richards                         | 9.75 ms                                                                  | 11.4 ms: 1.17x slower                                                        |
| comprehensions                   | 6.18 us                                                                  | 7.70 us: 1.25x slower                                                        |
| Geometric mean                   | (ref)                                                                    | 1.02x slower                                                                 |

Benchmark hidden because not significant (21): async_tree_memoization, async_tree_eager_io, async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_none, async_tree_cpu_io_mixed, regex_v8, chaos, async_tree_eager_io_tg, float, xml_etree_iterparse, connected_components, spectral_norm, async_generators, deepcopy_memo, regex_effbot, scimark_fft, async_tree_eager_tg, async_tree_eager_memoization, async_tree_eager_memoization_tg, pylint
Ignored benchmarks (3) of results/bm-20251229-3.15.0a3+-6cb245d-JIT/bm-20251229-macm4pro-arm64-python-6cb245d26086369bb075-3.15.0a3+-6cb245d.json: pycparser, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.021x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x