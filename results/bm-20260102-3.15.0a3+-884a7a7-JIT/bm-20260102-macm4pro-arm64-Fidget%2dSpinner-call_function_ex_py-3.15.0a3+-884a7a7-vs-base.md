# Results vs. base

- fork: Fidget-Spinner
- ref: call_function_ex_py
- machine: darwin-arm64
- commit hash: 884a7a7
- commit date: 2026-01-02
- overall geometric mean: 1.016x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 110 ms                                                                   | 107 ms: 1.03x faster                                                              |
| docutils       | 994 ms                                                                   | 973 ms: 1.02x faster                                                              |
| html5lib       | 19.9 ms                                                                  | 19.4 ms: 1.02x faster                                                             |
| sphinx         | 386 ms                                                                   | 379 ms: 1.02x faster                                                              |
| Geometric mean | (ref)                                                                    | 1.02x faster                                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_eager                 | 38.2 ms                                                                  | 35.9 ms: 1.06x faster                                                             |
| async_tree_none                  | 98.2 ms                                                                  | 94.5 ms: 1.04x faster                                                             |
| async_tree_eager_io              | 219 ms                                                                   | 212 ms: 1.03x faster                                                              |
| async_tree_cpu_io_mixed          | 247 ms                                                                   | 239 ms: 1.03x faster                                                              |
| async_tree_io_tg                 | 222 ms                                                                   | 215 ms: 1.03x faster                                                              |
| async_tree_io                    | 229 ms                                                                   | 222 ms: 1.03x faster                                                              |
| async_tree_eager_tg              | 78.4 ms                                                                  | 76.2 ms: 1.03x faster                                                             |
| async_tree_cpu_io_mixed_tg       | 252 ms                                                                   | 245 ms: 1.03x faster                                                              |
| async_tree_none_tg               | 97.3 ms                                                                  | 94.7 ms: 1.03x faster                                                             |
| async_generators                 | 182 ms                                                                   | 178 ms: 1.02x faster                                                              |
| async_tree_memoization           | 136 ms                                                                   | 133 ms: 1.02x faster                                                              |
| async_tree_memoization_tg        | 135 ms                                                                   | 132 ms: 1.02x faster                                                              |
| async_tree_eager_cpu_io_mixed_tg | 239 ms                                                                   | 235 ms: 1.02x faster                                                              |
| async_tree_eager_cpu_io_mixed    | 218 ms                                                                   | 214 ms: 1.02x faster                                                              |
| coroutines                       | 10.0 ms                                                                  | 10.1 ms: 1.01x slower                                                             |
| Geometric mean                   | (ref)                                                                    | 1.02x faster                                                                      |

Benchmark hidden because not significant (3): async_tree_eager_io_tg, async_tree_eager_memoization_tg, async_tree_eager_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| pidigits       | 160 ms                                                                   | 155 ms: 1.03x faster                                                              |
| nbody          | 39.8 ms                                                                  | 39.0 ms: 1.02x faster                                                             |
| float          | 23.0 ms                                                                  | 22.8 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                                    | 1.02x faster                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_dna      | 94.2 ms                                                                  | 91.6 ms: 1.03x faster                                                             |
| regex_effbot   | 1.44 ms                                                                  | 1.41 ms: 1.03x faster                                                             |
| regex_v8       | 9.61 ms                                                                  | 9.51 ms: 1.01x faster                                                             |
| regex_compile  | 39.5 ms                                                                  | 39.1 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                                    | 1.02x faster                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| json_dumps           | 3.66 ms                                                                  | 3.57 ms: 1.03x faster                                                             |
| json_loads           | 10.7 us                                                                  | 10.5 us: 1.02x faster                                                             |
| xml_etree_generate   | 30.8 ms                                                                  | 30.2 ms: 1.02x faster                                                             |
| unpickle_pure_python | 71.8 us                                                                  | 70.5 us: 1.02x faster                                                             |
| xml_etree_process    | 21.8 ms                                                                  | 21.4 ms: 1.02x faster                                                             |
| tomli_loads          | 795 ms                                                                   | 785 ms: 1.01x faster                                                              |
| pickle_pure_python   | 111 us                                                                   | 110 us: 1.01x faster                                                              |
| xml_etree_iterparse  | 36.2 ms                                                                  | 37.8 ms: 1.04x slower                                                             |
| Geometric mean       | (ref)                                                                    | 1.01x faster                                                                      |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|-----------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| django_template | 13.9 ms                                                                  | 13.5 ms: 1.02x faster                                                             |
| genshi_text     | 9.09 ms                                                                  | 8.90 ms: 1.02x faster                                                             |
| mako            | 3.89 ms                                                                  | 3.86 ms: 1.01x faster                                                             |
| genshi_xml      | 21.4 ms                                                                  | 21.2 ms: 1.01x faster                                                             |
| Geometric mean  | (ref)                                                                    | 1.02x faster                                                                      |

All benchmarks:
===============

| Benchmark                        | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 | bm-20260102-macm4pro-arm64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7 |
|----------------------------------|:------------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| coverage                         | 33.8 ms                                                                  | 31.4 ms: 1.08x faster                                                             |
| async_tree_eager                 | 38.2 ms                                                                  | 35.9 ms: 1.06x faster                                                             |
| async_tree_none                  | 98.2 ms                                                                  | 94.5 ms: 1.04x faster                                                             |
| many_optionals                   | 252 us                                                                   | 243 us: 1.04x faster                                                              |
| async_tree_eager_io              | 219 ms                                                                   | 212 ms: 1.03x faster                                                              |
| gc_traversal                     | 2.05 ms                                                                  | 1.98 ms: 1.03x faster                                                             |
| async_tree_cpu_io_mixed          | 247 ms                                                                   | 239 ms: 1.03x faster                                                              |
| async_tree_io_tg                 | 222 ms                                                                   | 215 ms: 1.03x faster                                                              |
| async_tree_io                    | 229 ms                                                                   | 222 ms: 1.03x faster                                                              |
| go                               | 42.7 ms                                                                  | 41.4 ms: 1.03x faster                                                             |
| pidigits                         | 160 ms                                                                   | 155 ms: 1.03x faster                                                              |
| json                             | 1.84 ms                                                                  | 1.79 ms: 1.03x faster                                                             |
| dulwich_log                      | 18.7 ms                                                                  | 18.2 ms: 1.03x faster                                                             |
| 2to3                             | 110 ms                                                                   | 107 ms: 1.03x faster                                                              |
| regex_dna                        | 94.2 ms                                                                  | 91.6 ms: 1.03x faster                                                             |
| async_tree_eager_tg              | 78.4 ms                                                                  | 76.2 ms: 1.03x faster                                                             |
| async_tree_cpu_io_mixed_tg       | 252 ms                                                                   | 245 ms: 1.03x faster                                                              |
| pathlib                          | 10.8 ms                                                                  | 10.5 ms: 1.03x faster                                                             |
| async_tree_none_tg               | 97.3 ms                                                                  | 94.7 ms: 1.03x faster                                                             |
| json_dumps                       | 3.66 ms                                                                  | 3.57 ms: 1.03x faster                                                             |
| meteor_contest                   | 44.8 ms                                                                  | 43.7 ms: 1.03x faster                                                             |
| bench_mp_pool                    | 44.8 ms                                                                  | 43.7 ms: 1.03x faster                                                             |
| regex_effbot                     | 1.44 ms                                                                  | 1.41 ms: 1.03x faster                                                             |
| create_gc_cycles                 | 913 us                                                                   | 890 us: 1.03x faster                                                              |
| async_generators                 | 182 ms                                                                   | 178 ms: 1.02x faster                                                              |
| django_template                  | 13.9 ms                                                                  | 13.5 ms: 1.02x faster                                                             |
| pylint                           | 121 ms                                                                   | 118 ms: 1.02x faster                                                              |
| async_tree_memoization           | 136 ms                                                                   | 133 ms: 1.02x faster                                                              |
| json_loads                       | 10.7 us                                                                  | 10.5 us: 1.02x faster                                                             |
| sympy_expand                     | 173 ms                                                                   | 169 ms: 1.02x faster                                                              |
| typing_runtime_protocols         | 61.8 us                                                                  | 60.4 us: 1.02x faster                                                             |
| async_tree_memoization_tg        | 135 ms                                                                   | 132 ms: 1.02x faster                                                              |
| docutils                         | 994 ms                                                                   | 973 ms: 1.02x faster                                                              |
| genshi_text                      | 9.09 ms                                                                  | 8.90 ms: 1.02x faster                                                             |
| html5lib                         | 19.9 ms                                                                  | 19.4 ms: 1.02x faster                                                             |
| subparsers                       | 3.87 ms                                                                  | 3.79 ms: 1.02x faster                                                             |
| nbody                            | 39.8 ms                                                                  | 39.0 ms: 1.02x faster                                                             |
| sqlite_synth                     | 963 ns                                                                   | 944 ns: 1.02x faster                                                              |
| fannkuch                         | 153 ms                                                                   | 150 ms: 1.02x faster                                                              |
| comprehensions                   | 6.18 us                                                                  | 6.06 us: 1.02x faster                                                             |
| async_tree_eager_cpu_io_mixed_tg | 239 ms                                                                   | 235 ms: 1.02x faster                                                              |
| sqlglot_v2_normalize             | 47.5 ms                                                                  | 46.6 ms: 1.02x faster                                                             |
| async_tree_eager_cpu_io_mixed    | 218 ms                                                                   | 214 ms: 1.02x faster                                                              |
| sphinx                           | 386 ms                                                                   | 379 ms: 1.02x faster                                                              |
| deepcopy                         | 97.1 us                                                                  | 95.3 us: 1.02x faster                                                             |
| xml_etree_generate               | 30.8 ms                                                                  | 30.2 ms: 1.02x faster                                                             |
| unpickle_pure_python             | 71.8 us                                                                  | 70.5 us: 1.02x faster                                                             |
| xml_etree_process                | 21.8 ms                                                                  | 21.4 ms: 1.02x faster                                                             |
| mdp                              | 577 ms                                                                   | 567 ms: 1.02x faster                                                              |
| scimark_monte_carlo              | 22.5 ms                                                                  | 22.1 ms: 1.02x faster                                                             |
| sympy_sum                        | 55.9 ms                                                                  | 54.9 ms: 1.02x faster                                                             |
| deepcopy_memo                    | 11.4 us                                                                  | 11.2 us: 1.02x faster                                                             |
| logging_simple                   | 2.07 us                                                                  | 2.04 us: 1.02x faster                                                             |
| richards_super                   | 11.6 ms                                                                  | 11.4 ms: 1.02x faster                                                             |
| deltablue                        | 1.12 ms                                                                  | 1.10 ms: 1.02x faster                                                             |
| generators                       | 18.4 ms                                                                  | 18.1 ms: 1.02x faster                                                             |
| thrift                           | 285 us                                                                   | 281 us: 1.02x faster                                                              |
| nqueens                          | 38.7 ms                                                                  | 38.1 ms: 1.01x faster                                                             |
| raytrace                         | 106 ms                                                                   | 104 ms: 1.01x faster                                                              |
| bpe_tokeniser                    | 1.83 sec                                                                 | 1.80 sec: 1.01x faster                                                            |
| crypto_pyaes                     | 30.7 ms                                                                  | 30.2 ms: 1.01x faster                                                             |
| deepcopy_reduce                  | 1.00 us                                                                  | 991 ns: 1.01x faster                                                              |
| pycparser                        | 433 ms                                                                   | 428 ms: 1.01x faster                                                              |
| scimark_sparse_mat_mult          | 1.92 ms                                                                  | 1.90 ms: 1.01x faster                                                             |
| hexiom                           | 2.60 ms                                                                  | 2.57 ms: 1.01x faster                                                             |
| sqlglot_v2_optimize              | 23.8 ms                                                                  | 23.5 ms: 1.01x faster                                                             |
| tomli_loads                      | 795 ms                                                                   | 785 ms: 1.01x faster                                                              |
| chaos                            | 21.8 ms                                                                  | 21.5 ms: 1.01x faster                                                             |
| logging_format                   | 2.29 us                                                                  | 2.26 us: 1.01x faster                                                             |
| pickle_pure_python               | 111 us                                                                   | 110 us: 1.01x faster                                                              |
| regex_v8                         | 9.61 ms                                                                  | 9.51 ms: 1.01x faster                                                             |
| regex_compile                    | 39.5 ms                                                                  | 39.1 ms: 1.01x faster                                                             |
| sympy_integrate                  | 7.41 ms                                                                  | 7.34 ms: 1.01x faster                                                             |
| mako                             | 3.89 ms                                                                  | 3.86 ms: 1.01x faster                                                             |
| genshi_xml                       | 21.4 ms                                                                  | 21.2 ms: 1.01x faster                                                             |
| float                            | 23.0 ms                                                                  | 22.8 ms: 1.01x faster                                                             |
| sqlglot_v2_transpile             | 570 us                                                                   | 567 us: 1.01x faster                                                              |
| pprint_safe_repr                 | 257 ms                                                                   | 256 ms: 1.01x faster                                                              |
| scimark_lu                       | 36.1 ms                                                                  | 36.0 ms: 1.00x faster                                                             |
| shortest_path                    | 215 ms                                                                   | 216 ms: 1.00x slower                                                              |
| connected_components             | 197 ms                                                                   | 198 ms: 1.01x slower                                                              |
| coroutines                       | 10.0 ms                                                                  | 10.1 ms: 1.01x slower                                                             |
| logging_silent                   | 33.7 ns                                                                  | 34.3 ns: 1.02x slower                                                             |
| pprint_pformat                   | 516 ms                                                                   | 525 ms: 1.02x slower                                                              |
| xml_etree_iterparse              | 36.2 ms                                                                  | 37.8 ms: 1.04x slower                                                             |
| Geometric mean                   | (ref)                                                                    | 1.02x faster                                                                      |

Benchmark hidden because not significant (16): async_tree_eager_io_tg, async_tree_eager_memoization_tg, sympy_str, xml_etree_parse, telco, k_core, pyflate, async_tree_eager_memoization, sqlglot_v2_parse, python_startup_no_site, scimark_sor, bench_thread_pool, scimark_fft, python_startup, spectral_norm, richards
Ignored benchmarks (1) of results/bm-20260102-3.15.0a3+-884a7a7-JIT/bm-20260102-macm4pro-arm64-Fidget%2dSpinner-call_function_ex_py-3.15.0a3+-884a7a7.json: asyncio_websockets

- Geometric mean (including insignificant results): 1.016x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.00x