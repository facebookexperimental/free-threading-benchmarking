# Results vs. base

- fork: Fidget-Spinner
- ref: loop_peeling
- machine: darwin-arm64
- commit hash: e650bf3
- commit date: 2026-01-03
- overall geometric mean: 1.009x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3+-b538c28 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-loop_peeling-3.15.0a3+-e650bf3 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| 2to3           | 110 ms                                                                   | 107 ms: 1.02x faster                                                       |
| docutils       | 1.01 sec                                                                 | 1000 ms: 1.01x faster                                                      |
| html5lib       | 20.2 ms                                                                  | 19.7 ms: 1.02x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.01x faster                                                               |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3+-b538c28 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-loop_peeling-3.15.0a3+-e650bf3 |
|----------------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| async_tree_io_tg                 | 222 ms                                                                   | 217 ms: 1.02x faster                                                       |
| async_tree_cpu_io_mixed_tg       | 252 ms                                                                   | 247 ms: 1.02x faster                                                       |
| async_tree_none                  | 98.4 ms                                                                  | 96.3 ms: 1.02x faster                                                      |
| async_tree_cpu_io_mixed          | 247 ms                                                                   | 242 ms: 1.02x faster                                                       |
| async_tree_eager                 | 38.0 ms                                                                  | 37.2 ms: 1.02x faster                                                      |
| async_tree_eager_cpu_io_mixed    | 218 ms                                                                   | 213 ms: 1.02x faster                                                       |
| coroutines                       | 10.4 ms                                                                  | 10.2 ms: 1.02x faster                                                      |
| async_tree_io                    | 230 ms                                                                   | 225 ms: 1.02x faster                                                       |
| async_generators                 | 181 ms                                                                   | 178 ms: 1.02x faster                                                       |
| async_tree_none_tg               | 97.7 ms                                                                  | 96.1 ms: 1.02x faster                                                      |
| async_tree_eager_cpu_io_mixed_tg | 240 ms                                                                   | 237 ms: 1.01x faster                                                       |
| async_tree_eager_tg              | 78.3 ms                                                                  | 77.4 ms: 1.01x faster                                                      |
| async_tree_eager_memoization     | 105 ms                                                                   | 104 ms: 1.01x faster                                                       |
| Geometric mean                   | (ref)                                                                    | 1.02x faster                                                               |

Benchmark hidden because not significant (5): async_tree_eager_io_tg, async_tree_eager_io, async_tree_memoization_tg, async_tree_eager_memoization_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3+-b538c28 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-loop_peeling-3.15.0a3+-e650bf3 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| float          | 22.7 ms                                                                  | 22.2 ms: 1.03x faster                                                      |
| pidigits       | 161 ms                                                                   | 159 ms: 1.01x faster                                                       |
| nbody          | 40.2 ms                                                                  | 39.9 ms: 1.01x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.02x faster                                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3+-b538c28 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-loop_peeling-3.15.0a3+-e650bf3 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| regex_compile  | 41.1 ms                                                                  | 40.4 ms: 1.02x faster                                                      |
| regex_v8       | 9.66 ms                                                                  | 9.83 ms: 1.02x slower                                                      |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                               |

Benchmark hidden because not significant (2): regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3+-b538c28 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-loop_peeling-3.15.0a3+-e650bf3 |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| xml_etree_iterparse  | 38.8 ms                                                                  | 36.4 ms: 1.07x faster                                                      |
| xml_etree_parse      | 62.4 ms                                                                  | 60.0 ms: 1.04x faster                                                      |
| json_dumps           | 3.64 ms                                                                  | 3.58 ms: 1.02x faster                                                      |
| json_loads           | 10.6 us                                                                  | 10.4 us: 1.02x faster                                                      |
| tomli_loads          | 772 ms                                                                   | 764 ms: 1.01x faster                                                       |
| xml_etree_process    | 22.1 ms                                                                  | 21.9 ms: 1.01x faster                                                      |
| pickle_pure_python   | 110 us                                                                   | 109 us: 1.01x faster                                                       |
| unpickle_pure_python | 72.0 us                                                                  | 72.4 us: 1.01x slower                                                      |
| Geometric mean       | (ref)                                                                    | 1.02x faster                                                               |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3+-b538c28 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-loop_peeling-3.15.0a3+-e650bf3 |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| python_startup | 8.78 ms                                                                  | 8.76 ms: 1.00x faster                                                      |
| Geometric mean | (ref)                                                                    | 1.00x faster                                                               |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3+-b538c28 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-loop_peeling-3.15.0a3+-e650bf3 |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| genshi_xml      | 21.7 ms                                                                  | 21.2 ms: 1.02x faster                                                      |
| genshi_text     | 9.07 ms                                                                  | 8.95 ms: 1.01x faster                                                      |
| mako            | 3.91 ms                                                                  | 3.87 ms: 1.01x faster                                                      |
| django_template | 13.9 ms                                                                  | 13.8 ms: 1.01x faster                                                      |
| Geometric mean  | (ref)                                                                    | 1.01x faster                                                               |

All benchmarks:
===============

| Benchmark                        | bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3+-b538c28 | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-loop_peeling-3.15.0a3+-e650bf3 |
|----------------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------:|
| xml_etree_iterparse              | 38.8 ms                                                                  | 36.4 ms: 1.07x faster                                                      |
| scimark_sparse_mat_mult          | 1.87 ms                                                                  | 1.79 ms: 1.05x faster                                                      |
| spectral_norm                    | 40.9 ms                                                                  | 39.1 ms: 1.05x faster                                                      |
| xml_etree_parse                  | 62.4 ms                                                                  | 60.0 ms: 1.04x faster                                                      |
| telco                            | 2.63 ms                                                                  | 2.55 ms: 1.03x faster                                                      |
| scimark_fft                      | 101 ms                                                                   | 97.8 ms: 1.03x faster                                                      |
| coverage                         | 33.3 ms                                                                  | 32.4 ms: 1.03x faster                                                      |
| float                            | 22.7 ms                                                                  | 22.2 ms: 1.03x faster                                                      |
| many_optionals                   | 250 us                                                                   | 244 us: 1.02x faster                                                       |
| genshi_xml                       | 21.7 ms                                                                  | 21.2 ms: 1.02x faster                                                      |
| async_tree_io_tg                 | 222 ms                                                                   | 217 ms: 1.02x faster                                                       |
| 2to3                             | 110 ms                                                                   | 107 ms: 1.02x faster                                                       |
| scimark_lu                       | 36.7 ms                                                                  | 35.9 ms: 1.02x faster                                                      |
| html5lib                         | 20.2 ms                                                                  | 19.7 ms: 1.02x faster                                                      |
| subparsers                       | 3.90 ms                                                                  | 3.81 ms: 1.02x faster                                                      |
| async_tree_cpu_io_mixed_tg       | 252 ms                                                                   | 247 ms: 1.02x faster                                                       |
| async_tree_none                  | 98.4 ms                                                                  | 96.3 ms: 1.02x faster                                                      |
| async_tree_cpu_io_mixed          | 247 ms                                                                   | 242 ms: 1.02x faster                                                       |
| async_tree_eager                 | 38.0 ms                                                                  | 37.2 ms: 1.02x faster                                                      |
| async_tree_eager_cpu_io_mixed    | 218 ms                                                                   | 213 ms: 1.02x faster                                                       |
| create_gc_cycles                 | 919 us                                                                   | 901 us: 1.02x faster                                                       |
| coroutines                       | 10.4 ms                                                                  | 10.2 ms: 1.02x faster                                                      |
| async_tree_io                    | 230 ms                                                                   | 225 ms: 1.02x faster                                                       |
| json_dumps                       | 3.64 ms                                                                  | 3.58 ms: 1.02x faster                                                      |
| bench_mp_pool                    | 45.0 ms                                                                  | 44.2 ms: 1.02x faster                                                      |
| bpe_tokeniser                    | 1.84 sec                                                                 | 1.81 sec: 1.02x faster                                                     |
| regex_compile                    | 41.1 ms                                                                  | 40.4 ms: 1.02x faster                                                      |
| json                             | 1.84 ms                                                                  | 1.81 ms: 1.02x faster                                                      |
| async_generators                 | 181 ms                                                                   | 178 ms: 1.02x faster                                                       |
| json_loads                       | 10.6 us                                                                  | 10.4 us: 1.02x faster                                                      |
| async_tree_none_tg               | 97.7 ms                                                                  | 96.1 ms: 1.02x faster                                                      |
| pycparser                        | 443 ms                                                                   | 436 ms: 1.02x faster                                                       |
| nqueens                          | 38.9 ms                                                                  | 38.4 ms: 1.01x faster                                                      |
| pprint_safe_repr                 | 255 ms                                                                   | 251 ms: 1.01x faster                                                       |
| generators                       | 18.5 ms                                                                  | 18.3 ms: 1.01x faster                                                      |
| pprint_pformat                   | 515 ms                                                                   | 509 ms: 1.01x faster                                                       |
| genshi_text                      | 9.07 ms                                                                  | 8.95 ms: 1.01x faster                                                      |
| pidigits                         | 161 ms                                                                   | 159 ms: 1.01x faster                                                       |
| deltablue                        | 1.13 ms                                                                  | 1.11 ms: 1.01x faster                                                      |
| async_tree_eager_cpu_io_mixed_tg | 240 ms                                                                   | 237 ms: 1.01x faster                                                       |
| dulwich_log                      | 18.7 ms                                                                  | 18.4 ms: 1.01x faster                                                      |
| async_tree_eager_tg              | 78.3 ms                                                                  | 77.4 ms: 1.01x faster                                                      |
| chaos                            | 21.9 ms                                                                  | 21.6 ms: 1.01x faster                                                      |
| mdp                              | 583 ms                                                                   | 577 ms: 1.01x faster                                                       |
| tomli_loads                      | 772 ms                                                                   | 764 ms: 1.01x faster                                                       |
| crypto_pyaes                     | 30.7 ms                                                                  | 30.4 ms: 1.01x faster                                                      |
| xml_etree_process                | 22.1 ms                                                                  | 21.9 ms: 1.01x faster                                                      |
| nbody                            | 40.2 ms                                                                  | 39.9 ms: 1.01x faster                                                      |
| mako                             | 3.91 ms                                                                  | 3.87 ms: 1.01x faster                                                      |
| async_tree_eager_memoization     | 105 ms                                                                   | 104 ms: 1.01x faster                                                       |
| meteor_contest                   | 45.6 ms                                                                  | 45.3 ms: 1.01x faster                                                      |
| pickle_pure_python               | 110 us                                                                   | 109 us: 1.01x faster                                                       |
| docutils                         | 1.01 sec                                                                 | 1000 ms: 1.01x faster                                                      |
| sqlite_synth                     | 962 ns                                                                   | 955 ns: 1.01x faster                                                       |
| django_template                  | 13.9 ms                                                                  | 13.8 ms: 1.01x faster                                                      |
| scimark_monte_carlo              | 22.1 ms                                                                  | 21.9 ms: 1.01x faster                                                      |
| logging_silent                   | 33.9 ns                                                                  | 33.7 ns: 1.01x faster                                                      |
| hexiom                           | 2.63 ms                                                                  | 2.62 ms: 1.01x faster                                                      |
| comprehensions                   | 6.16 us                                                                  | 6.13 us: 1.00x faster                                                      |
| python_startup                   | 8.78 ms                                                                  | 8.76 ms: 1.00x faster                                                      |
| scimark_sor                      | 42.2 ms                                                                  | 42.2 ms: 1.00x faster                                                      |
| sqlglot_v2_normalize             | 47.4 ms                                                                  | 47.7 ms: 1.00x slower                                                      |
| connected_components             | 198 ms                                                                   | 199 ms: 1.01x slower                                                       |
| unpickle_pure_python             | 72.0 us                                                                  | 72.4 us: 1.01x slower                                                      |
| shortest_path                    | 216 ms                                                                   | 217 ms: 1.01x slower                                                       |
| deepcopy                         | 97.8 us                                                                  | 98.6 us: 1.01x slower                                                      |
| logging_format                   | 2.31 us                                                                  | 2.33 us: 1.01x slower                                                      |
| thrift                           | 302 us                                                                   | 304 us: 1.01x slower                                                       |
| logging_simple                   | 2.09 us                                                                  | 2.12 us: 1.01x slower                                                      |
| sympy_expand                     | 174 ms                                                                   | 176 ms: 1.01x slower                                                       |
| sqlglot_v2_parse                 | 452 us                                                                   | 458 us: 1.01x slower                                                       |
| sympy_integrate                  | 7.53 ms                                                                  | 7.65 ms: 1.02x slower                                                      |
| regex_v8                         | 9.66 ms                                                                  | 9.83 ms: 1.02x slower                                                      |
| sqlglot_v2_optimize              | 24.1 ms                                                                  | 24.6 ms: 1.02x slower                                                      |
| sympy_sum                        | 56.2 ms                                                                  | 57.7 ms: 1.03x slower                                                      |
| sympy_str                        | 104 ms                                                                   | 107 ms: 1.03x slower                                                       |
| Geometric mean                   | (ref)                                                                    | 1.01x faster                                                               |

Benchmark hidden because not significant (25): async_tree_eager_io_tg, async_tree_eager_io, async_tree_memoization_tg, async_tree_eager_memoization_tg, async_tree_memoization, typing_runtime_protocols, pyflate, richards_super, sphinx, regex_dna, pathlib, gc_traversal, raytrace, xml_etree_generate, python_startup_no_site, k_core, deepcopy_memo, richards, fannkuch, deepcopy_reduce, bench_thread_pool, sqlglot_v2_transpile, pylint, go, regex_effbot
Ignored benchmarks (1) of results/bm-20260102-3.15.0a3+-b538c28-JIT/bm-20260102-macm4pro-arm64-python-b538c2832d582a428a6f-3.15.0a3+-b538c28.json: asyncio_websockets

- Geometric mean (including insignificant results): 1.009x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x