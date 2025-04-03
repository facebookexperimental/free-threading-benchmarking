# Results vs. base

- fork: Fidget-Spinner
- ref: tail_call_force_on
- machine: darwin-arm64
- commit hash: 0227a6d
- commit date: 2025-04-03
- overall geometric mean: 1.071x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250402-macm4pro-arm64-python-06822bfbf625e9777813-3.14.0a6+-06822bf | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 123 ms                                                                   | 113 ms: 1.08x faster                                                             |
| docutils       | 1.03 sec                                                                 | 984 ms: 1.04x faster                                                             |
| html5lib       | 23.9 ms                                                                  | 21.7 ms: 1.10x faster                                                            |
| sphinx         | 426 ms                                                                   | 404 ms: 1.06x faster                                                             |
| Geometric mean | (ref)                                                                    | 1.07x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20250402-macm4pro-arm64-python-06822bfbf625e9777813-3.14.0a6+-06822bf | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| coroutines                       | 10.6 ms                                                                  | 8.94 ms: 1.19x faster                                                            |
| async_tree_eager                 | 51.7 ms                                                                  | 46.1 ms: 1.12x faster                                                            |
| async_tree_eager_io_tg           | 202 ms                                                                   | 185 ms: 1.09x faster                                                             |
| async_tree_eager_io              | 214 ms                                                                   | 197 ms: 1.09x faster                                                             |
| async_tree_eager_tg              | 79.9 ms                                                                  | 73.7 ms: 1.08x faster                                                            |
| async_tree_io_tg                 | 204 ms                                                                   | 188 ms: 1.08x faster                                                             |
| async_tree_none_tg               | 88.8 ms                                                                  | 82.0 ms: 1.08x faster                                                            |
| async_tree_io                    | 216 ms                                                                   | 201 ms: 1.08x faster                                                             |
| async_tree_none                  | 104 ms                                                                   | 97.6 ms: 1.06x faster                                                            |
| async_tree_eager_memoization     | 113 ms                                                                   | 107 ms: 1.06x faster                                                             |
| async_tree_eager_memoization_tg  | 114 ms                                                                   | 109 ms: 1.05x faster                                                             |
| async_tree_memoization_tg        | 126 ms                                                                   | 120 ms: 1.05x faster                                                             |
| async_tree_memoization           | 133 ms                                                                   | 127 ms: 1.05x faster                                                             |
| async_generators                 | 180 ms                                                                   | 172 ms: 1.05x faster                                                             |
| async_tree_eager_cpu_io_mixed    | 224 ms                                                                   | 218 ms: 1.03x faster                                                             |
| async_tree_cpu_io_mixed_tg       | 236 ms                                                                   | 229 ms: 1.03x faster                                                             |
| async_tree_cpu_io_mixed          | 244 ms                                                                   | 239 ms: 1.02x faster                                                             |
| async_tree_eager_cpu_io_mixed_tg | 226 ms                                                                   | 221 ms: 1.02x faster                                                             |
| Geometric mean                   | (ref)                                                                    | 1.06x faster                                                                     |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250402-macm4pro-arm64-python-06822bfbf625e9777813-3.14.0a6+-06822bf | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 28.1 ms                                                                  | 25.7 ms: 1.09x faster                                                            |
| nbody          | 54.3 ms                                                                  | 51.1 ms: 1.06x faster                                                            |
| pidigits       | 166 ms                                                                   | 165 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                                    | 1.05x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250402-macm4pro-arm64-python-06822bfbf625e9777813-3.14.0a6+-06822bf | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 54.0 ms                                                                  | 48.0 ms: 1.12x faster                                                            |
| regex_v8       | 9.98 ms                                                                  | 9.71 ms: 1.03x faster                                                            |
| regex_effbot   | 1.51 ms                                                                  | 1.50 ms: 1.01x faster                                                            |
| regex_dna      | 101 ms                                                                   | 102 ms: 1.01x slower                                                             |
| Geometric mean | (ref)                                                                    | 1.04x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250402-macm4pro-arm64-python-06822bfbf625e9777813-3.14.0a6+-06822bf | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| tomli_loads          | 967 ms                                                                   | 849 ms: 1.14x faster                                                             |
| unpickle_pure_python | 109 us                                                                   | 97.7 us: 1.11x faster                                                            |
| pickle_pure_python   | 154 us                                                                   | 139 us: 1.11x faster                                                             |
| xml_etree_process    | 26.8 ms                                                                  | 24.8 ms: 1.08x faster                                                            |
| xml_etree_generate   | 36.9 ms                                                                  | 34.3 ms: 1.08x faster                                                            |
| json_dumps           | 5.06 ms                                                                  | 4.97 ms: 1.02x faster                                                            |
| json_loads           | 12.1 us                                                                  | 11.9 us: 1.02x faster                                                            |
| xml_etree_parse      | 55.6 ms                                                                  | 56.5 ms: 1.02x slower                                                            |
| xml_etree_iterparse  | 35.6 ms                                                                  | 36.9 ms: 1.04x slower                                                            |
| Geometric mean       | (ref)                                                                    | 1.05x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250402-macm4pro-arm64-python-06822bfbf625e9777813-3.14.0a6+-06822bf | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 7.65 ms                                                                  | 7.55 ms: 1.01x faster                                                            |
| python_startup         | 9.62 ms                                                                  | 9.51 ms: 1.01x faster                                                            |
| Geometric mean         | (ref)                                                                    | 1.01x faster                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250402-macm4pro-arm64-python-06822bfbf625e9777813-3.14.0a6+-06822bf | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|-----------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml      | 24.0 ms                                                                  | 20.8 ms: 1.15x faster                                                            |
| django_template | 16.8 ms                                                                  | 15.1 ms: 1.11x faster                                                            |
| genshi_text     | 11.5 ms                                                                  | 10.5 ms: 1.10x faster                                                            |
| mako            | 5.56 ms                                                                  | 5.27 ms: 1.06x faster                                                            |
| Geometric mean  | (ref)                                                                    | 1.10x faster                                                                     |

All benchmarks:
===============

| Benchmark                        | bm-20250402-macm4pro-arm64-python-06822bfbf625e9777813-3.14.0a6+-06822bf | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------------------------|:------------------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| generators                       | 19.0 ms                                                                  | 14.4 ms: 1.32x faster                                                            |
| coroutines                       | 10.6 ms                                                                  | 8.94 ms: 1.19x faster                                                            |
| deepcopy                         | 126 us                                                                   | 106 us: 1.19x faster                                                             |
| genshi_xml                       | 24.0 ms                                                                  | 20.8 ms: 1.15x faster                                                            |
| hexiom                           | 3.24 ms                                                                  | 2.84 ms: 1.14x faster                                                            |
| sqlglot_v2_parse                 | 606 us                                                                   | 531 us: 1.14x faster                                                             |
| tomli_loads                      | 967 ms                                                                   | 849 ms: 1.14x faster                                                             |
| go                               | 64.0 ms                                                                  | 56.3 ms: 1.14x faster                                                            |
| deepcopy_reduce                  | 1.30 us                                                                  | 1.14 us: 1.14x faster                                                            |
| sqlglot_v2_transpile             | 731 us                                                                   | 648 us: 1.13x faster                                                             |
| pprint_safe_repr                 | 368 ms                                                                   | 327 ms: 1.13x faster                                                             |
| richards                         | 24.8 ms                                                                  | 22.0 ms: 1.13x faster                                                            |
| richards_super                   | 28.3 ms                                                                  | 25.2 ms: 1.12x faster                                                            |
| regex_compile                    | 54.0 ms                                                                  | 48.0 ms: 1.12x faster                                                            |
| async_tree_eager                 | 51.7 ms                                                                  | 46.1 ms: 1.12x faster                                                            |
| pprint_pformat                   | 744 ms                                                                   | 664 ms: 1.12x faster                                                             |
| sympy_expand                     | 194 ms                                                                   | 173 ms: 1.12x faster                                                             |
| deepcopy_memo                    | 14.7 us                                                                  | 13.1 us: 1.12x faster                                                            |
| unpickle_pure_python             | 109 us                                                                   | 97.7 us: 1.11x faster                                                            |
| django_template                  | 16.8 ms                                                                  | 15.1 ms: 1.11x faster                                                            |
| pickle_pure_python               | 154 us                                                                   | 139 us: 1.11x faster                                                             |
| comprehensions                   | 8.76 us                                                                  | 7.93 us: 1.10x faster                                                            |
| logging_simple                   | 2.59 us                                                                  | 2.34 us: 1.10x faster                                                            |
| sympy_str                        | 113 ms                                                                   | 103 ms: 1.10x faster                                                             |
| logging_format                   | 2.85 us                                                                  | 2.59 us: 1.10x faster                                                            |
| html5lib                         | 23.9 ms                                                                  | 21.7 ms: 1.10x faster                                                            |
| scimark_fft                      | 141 ms                                                                   | 128 ms: 1.10x faster                                                             |
| sqlglot_v2_optimize              | 24.5 ms                                                                  | 22.4 ms: 1.10x faster                                                            |
| genshi_text                      | 11.5 ms                                                                  | 10.5 ms: 1.10x faster                                                            |
| sqlglot_v2_normalize             | 49.7 ms                                                                  | 45.4 ms: 1.09x faster                                                            |
| async_tree_eager_io_tg           | 202 ms                                                                   | 185 ms: 1.09x faster                                                             |
| float                            | 28.1 ms                                                                  | 25.7 ms: 1.09x faster                                                            |
| scimark_lu                       | 54.2 ms                                                                  | 49.8 ms: 1.09x faster                                                            |
| sqlalchemy_imperative            | 5.85 ms                                                                  | 5.38 ms: 1.09x faster                                                            |
| async_tree_eager_io              | 214 ms                                                                   | 197 ms: 1.09x faster                                                             |
| sympy_sum                        | 62.5 ms                                                                  | 57.5 ms: 1.09x faster                                                            |
| pycparser                        | 475 ms                                                                   | 437 ms: 1.09x faster                                                             |
| chaos                            | 29.6 ms                                                                  | 27.3 ms: 1.09x faster                                                            |
| 2to3                             | 123 ms                                                                   | 113 ms: 1.08x faster                                                             |
| async_tree_eager_tg              | 79.9 ms                                                                  | 73.7 ms: 1.08x faster                                                            |
| subparsers                       | 8.97 ms                                                                  | 8.27 ms: 1.08x faster                                                            |
| async_tree_io_tg                 | 204 ms                                                                   | 188 ms: 1.08x faster                                                             |
| async_tree_none_tg               | 88.8 ms                                                                  | 82.0 ms: 1.08x faster                                                            |
| xml_etree_process                | 26.8 ms                                                                  | 24.8 ms: 1.08x faster                                                            |
| scimark_monte_carlo              | 33.9 ms                                                                  | 31.4 ms: 1.08x faster                                                            |
| async_tree_io                    | 216 ms                                                                   | 201 ms: 1.08x faster                                                             |
| typing_runtime_protocols         | 73.4 us                                                                  | 68.1 us: 1.08x faster                                                            |
| xml_etree_generate               | 36.9 ms                                                                  | 34.3 ms: 1.08x faster                                                            |
| sqlalchemy_declarative           | 51.0 ms                                                                  | 47.4 ms: 1.08x faster                                                            |
| fannkuch                         | 195 ms                                                                   | 181 ms: 1.08x faster                                                             |
| meteor_contest                   | 57.6 ms                                                                  | 53.7 ms: 1.07x faster                                                            |
| nqueens                          | 42.5 ms                                                                  | 39.7 ms: 1.07x faster                                                            |
| bpe_tokeniser                    | 1.99 sec                                                                 | 1.87 sec: 1.07x faster                                                           |
| deltablue                        | 1.66 ms                                                                  | 1.55 ms: 1.07x faster                                                            |
| mdp                              | 579 ms                                                                   | 543 ms: 1.07x faster                                                             |
| logging_silent                   | 47.4 ns                                                                  | 44.5 ns: 1.07x faster                                                            |
| raytrace                         | 132 ms                                                                   | 124 ms: 1.07x faster                                                             |
| pyflate                          | 203 ms                                                                   | 190 ms: 1.07x faster                                                             |
| async_tree_none                  | 104 ms                                                                   | 97.6 ms: 1.06x faster                                                            |
| nbody                            | 54.3 ms                                                                  | 51.1 ms: 1.06x faster                                                            |
| async_tree_eager_memoization     | 113 ms                                                                   | 107 ms: 1.06x faster                                                             |
| sympy_integrate                  | 8.26 ms                                                                  | 7.80 ms: 1.06x faster                                                            |
| dulwich_log                      | 19.0 ms                                                                  | 18.0 ms: 1.06x faster                                                            |
| scimark_sparse_mat_mult          | 2.13 ms                                                                  | 2.01 ms: 1.06x faster                                                            |
| many_optionals                   | 246 us                                                                   | 233 us: 1.06x faster                                                             |
| sphinx                           | 426 ms                                                                   | 404 ms: 1.06x faster                                                             |
| mako                             | 5.56 ms                                                                  | 5.27 ms: 1.06x faster                                                            |
| pylint                           | 121 ms                                                                   | 114 ms: 1.05x faster                                                             |
| telco                            | 3.31 ms                                                                  | 3.14 ms: 1.05x faster                                                            |
| async_tree_eager_memoization_tg  | 114 ms                                                                   | 109 ms: 1.05x faster                                                             |
| async_tree_memoization_tg        | 126 ms                                                                   | 120 ms: 1.05x faster                                                             |
| async_tree_memoization           | 133 ms                                                                   | 127 ms: 1.05x faster                                                             |
| async_generators                 | 180 ms                                                                   | 172 ms: 1.05x faster                                                             |
| crypto_pyaes                     | 41.2 ms                                                                  | 39.3 ms: 1.05x faster                                                            |
| docutils                         | 1.03 sec                                                                 | 984 ms: 1.04x faster                                                             |
| spectral_norm                    | 51.1 ms                                                                  | 49.2 ms: 1.04x faster                                                            |
| regex_v8                         | 9.98 ms                                                                  | 9.71 ms: 1.03x faster                                                            |
| async_tree_eager_cpu_io_mixed    | 224 ms                                                                   | 218 ms: 1.03x faster                                                             |
| async_tree_cpu_io_mixed_tg       | 236 ms                                                                   | 229 ms: 1.03x faster                                                             |
| async_tree_cpu_io_mixed          | 244 ms                                                                   | 239 ms: 1.02x faster                                                             |
| async_tree_eager_cpu_io_mixed_tg | 226 ms                                                                   | 221 ms: 1.02x faster                                                             |
| json                             | 2.01 ms                                                                  | 1.97 ms: 1.02x faster                                                            |
| json_dumps                       | 5.06 ms                                                                  | 4.97 ms: 1.02x faster                                                            |
| json_loads                       | 12.1 us                                                                  | 11.9 us: 1.02x faster                                                            |
| pathlib                          | 11.0 ms                                                                  | 10.8 ms: 1.02x faster                                                            |
| sqlite_synth                     | 816 ns                                                                   | 803 ns: 1.02x faster                                                             |
| coverage                         | 38.9 ms                                                                  | 38.4 ms: 1.01x faster                                                            |
| python_startup_no_site           | 7.65 ms                                                                  | 7.55 ms: 1.01x faster                                                            |
| python_startup                   | 9.62 ms                                                                  | 9.51 ms: 1.01x faster                                                            |
| bench_mp_pool                    | 42.4 ms                                                                  | 41.9 ms: 1.01x faster                                                            |
| bench_thread_pool                | 579 us                                                                   | 572 us: 1.01x faster                                                             |
| create_gc_cycles                 | 463 us                                                                   | 459 us: 1.01x faster                                                             |
| k_core                           | 990 ms                                                                   | 980 ms: 1.01x faster                                                             |
| regex_effbot                     | 1.51 ms                                                                  | 1.50 ms: 1.01x faster                                                            |
| pidigits                         | 166 ms                                                                   | 165 ms: 1.01x faster                                                             |
| scimark_sor                      | 54.5 ms                                                                  | 54.1 ms: 1.01x faster                                                            |
| shortest_path                    | 231 ms                                                                   | 230 ms: 1.00x faster                                                             |
| regex_dna                        | 101 ms                                                                   | 102 ms: 1.01x slower                                                             |
| xml_etree_parse                  | 55.6 ms                                                                  | 56.5 ms: 1.02x slower                                                            |
| xml_etree_iterparse              | 35.6 ms                                                                  | 36.9 ms: 1.04x slower                                                            |
| Geometric mean                   | (ref)                                                                    | 1.07x faster                                                                     |

Benchmark hidden because not significant (3): gc_traversal, asyncio_websockets, connected_components

- Geometric mean (including insignificant results): 1.071x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.01x