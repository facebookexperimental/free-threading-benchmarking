# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: tail_call_force_on
- machine: darwin-arm64
- commit hash: 0227a6d
- commit date: 2025-04-03
- overall geometric mean: 1.156x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                             |
| docutils       | 1.02 sec                                                 | 984 ms: 1.04x faster                                                             |
| html5lib       | 23.0 ms                                                  | 21.7 ms: 1.06x faster                                                            |
| sphinx         | 434 ms                                                   | 404 ms: 1.07x faster                                                             |
| Geometric mean | (ref)                                                    | 1.04x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------------------------|:--------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 188 ms: 2.56x faster                                                             |
| async_tree_eager_io              | 496 ms                                                   | 197 ms: 2.52x faster                                                             |
| async_tree_eager_io_tg           | 446 ms                                                   | 185 ms: 2.41x faster                                                             |
| async_tree_io                    | 459 ms                                                   | 201 ms: 2.29x faster                                                             |
| async_tree_none_tg               | 172 ms                                                   | 82.0 ms: 2.10x faster                                                            |
| async_tree_memoization_tg        | 231 ms                                                   | 120 ms: 1.93x faster                                                             |
| async_tree_none                  | 178 ms                                                   | 97.6 ms: 1.83x faster                                                            |
| async_tree_memoization           | 223 ms                                                   | 127 ms: 1.75x faster                                                             |
| coroutines                       | 13.6 ms                                                  | 8.94 ms: 1.52x faster                                                            |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 229 ms: 1.47x faster                                                             |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 239 ms: 1.40x faster                                                             |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                             |
| async_generators                 | 206 ms                                                   | 172 ms: 1.20x faster                                                             |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                             |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 109 ms: 1.04x faster                                                             |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                             |
| async_tree_eager                 | 45.6 ms                                                  | 46.1 ms: 1.01x slower                                                            |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 221 ms: 1.04x slower                                                             |
| async_tree_eager_tg              | 32.1 ms                                                  | 73.7 ms: 2.29x slower                                                            |
| Geometric mean                   | (ref)                                                    | 1.44x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 25.7 ms: 1.47x faster                                                            |
| nbody          | 54.2 ms                                                  | 51.1 ms: 1.06x faster                                                            |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                             |
| Geometric mean | (ref)                                                    | 1.15x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 48.0 ms: 1.14x faster                                                            |
| regex_effbot   | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                            |
| regex_v8       | 9.59 ms                                                  | 9.71 ms: 1.01x slower                                                            |
| regex_dna      | 99.6 ms                                                  | 102 ms: 1.02x slower                                                             |
| Geometric mean | (ref)                                                    | 1.05x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------------|:--------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 36.9 ms: 1.40x faster                                                            |
| xml_etree_parse      | 67.9 ms                                                  | 56.5 ms: 1.20x faster                                                            |
| xml_etree_generate   | 38.9 ms                                                  | 34.3 ms: 1.13x faster                                                            |
| tomli_loads          | 957 ms                                                   | 849 ms: 1.13x faster                                                             |
| xml_etree_process    | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                            |
| unpickle_pure_python | 103 us                                                   | 97.7 us: 1.05x faster                                                            |
| json_loads           | 10.9 us                                                  | 11.9 us: 1.09x slower                                                            |
| json_dumps           | 4.26 ms                                                  | 4.97 ms: 1.17x slower                                                            |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                                     |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|------------------------|:--------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.51 ms: 1.19x slower                                                            |
| python_startup_no_site | 5.71 ms                                                  | 7.55 ms: 1.32x slower                                                            |
| Geometric mean         | (ref)                                                    | 1.25x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|-----------------|:--------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 20.8 ms: 1.05x faster                                                            |
| mako            | 4.77 ms                                                  | 5.27 ms: 1.10x slower                                                            |
| django_template | 13.6 ms                                                  | 15.1 ms: 1.11x slower                                                            |
| Geometric mean  | (ref)                                                    | 1.04x slower                                                                     |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------------------------|:--------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 761 us: 2.64x faster                                                             |
| async_tree_io_tg                 | 480 ms                                                   | 188 ms: 2.56x faster                                                             |
| async_tree_eager_io              | 496 ms                                                   | 197 ms: 2.52x faster                                                             |
| subparsers                       | 20.8 ms                                                  | 8.27 ms: 2.51x faster                                                            |
| async_tree_eager_io_tg           | 446 ms                                                   | 185 ms: 2.41x faster                                                             |
| async_tree_io                    | 459 ms                                                   | 201 ms: 2.29x faster                                                             |
| async_tree_none_tg               | 172 ms                                                   | 82.0 ms: 2.10x faster                                                            |
| mdp                              | 1.09 sec                                                 | 543 ms: 2.01x faster                                                             |
| async_tree_memoization_tg        | 231 ms                                                   | 120 ms: 1.93x faster                                                             |
| async_tree_none                  | 178 ms                                                   | 97.6 ms: 1.83x faster                                                            |
| create_gc_cycles                 | 830 us                                                   | 459 us: 1.81x faster                                                             |
| async_tree_memoization           | 223 ms                                                   | 127 ms: 1.75x faster                                                             |
| deepcopy                         | 161 us                                                   | 106 us: 1.52x faster                                                             |
| generators                       | 21.9 ms                                                  | 14.4 ms: 1.52x faster                                                            |
| coroutines                       | 13.6 ms                                                  | 8.94 ms: 1.52x faster                                                            |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 229 ms: 1.47x faster                                                             |
| float                            | 37.9 ms                                                  | 25.7 ms: 1.47x faster                                                            |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 239 ms: 1.40x faster                                                             |
| xml_etree_iterparse              | 51.6 ms                                                  | 36.9 ms: 1.40x faster                                                            |
| deepcopy_memo                    | 18.3 us                                                  | 13.1 us: 1.39x faster                                                            |
| deepcopy_reduce                  | 1.46 us                                                  | 1.14 us: 1.28x faster                                                            |
| go                               | 70.0 ms                                                  | 56.3 ms: 1.24x faster                                                            |
| comprehensions                   | 9.84 us                                                  | 7.93 us: 1.24x faster                                                            |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                             |
| sqlite_synth                     | 967 ns                                                   | 803 ns: 1.20x faster                                                             |
| xml_etree_parse                  | 67.9 ms                                                  | 56.5 ms: 1.20x faster                                                            |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.87 sec: 1.20x faster                                                           |
| async_generators                 | 206 ms                                                   | 172 ms: 1.20x faster                                                             |
| dulwich_log                      | 21.3 ms                                                  | 18.0 ms: 1.18x faster                                                            |
| raytrace                         | 145 ms                                                   | 124 ms: 1.17x faster                                                             |
| logging_silent                   | 50.9 ns                                                  | 44.5 ns: 1.14x faster                                                            |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                            |
| k_core                           | 1.12 sec                                                 | 980 ms: 1.14x faster                                                             |
| pycparser                        | 497 ms                                                   | 437 ms: 1.14x faster                                                             |
| regex_compile                    | 54.6 ms                                                  | 48.0 ms: 1.14x faster                                                            |
| pyflate                          | 216 ms                                                   | 190 ms: 1.13x faster                                                             |
| xml_etree_generate               | 38.9 ms                                                  | 34.3 ms: 1.13x faster                                                            |
| tomli_loads                      | 957 ms                                                   | 849 ms: 1.13x faster                                                             |
| scimark_sor                      | 61.0 ms                                                  | 54.1 ms: 1.13x faster                                                            |
| pylint                           | 128 ms                                                   | 114 ms: 1.12x faster                                                             |
| regex_effbot                     | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                            |
| deltablue                        | 1.73 ms                                                  | 1.55 ms: 1.11x faster                                                            |
| spectral_norm                    | 54.4 ms                                                  | 49.2 ms: 1.11x faster                                                            |
| scimark_fft                      | 142 ms                                                   | 128 ms: 1.11x faster                                                             |
| logging_simple                   | 2.57 us                                                  | 2.34 us: 1.10x faster                                                            |
| nqueens                          | 43.5 ms                                                  | 39.7 ms: 1.10x faster                                                            |
| logging_format                   | 2.80 us                                                  | 2.59 us: 1.08x faster                                                            |
| xml_etree_process                | 26.7 ms                                                  | 24.8 ms: 1.08x faster                                                            |
| sphinx                           | 434 ms                                                   | 404 ms: 1.07x faster                                                             |
| hexiom                           | 3.04 ms                                                  | 2.84 ms: 1.07x faster                                                            |
| nbody                            | 54.2 ms                                                  | 51.1 ms: 1.06x faster                                                            |
| chaos                            | 28.9 ms                                                  | 27.3 ms: 1.06x faster                                                            |
| html5lib                         | 23.0 ms                                                  | 21.7 ms: 1.06x faster                                                            |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                             |
| unpickle_pure_python             | 103 us                                                   | 97.7 us: 1.05x faster                                                            |
| genshi_xml                       | 21.8 ms                                                  | 20.8 ms: 1.05x faster                                                            |
| typing_runtime_protocols         | 71.0 us                                                  | 68.1 us: 1.04x faster                                                            |
| docutils                         | 1.02 sec                                                 | 984 ms: 1.04x faster                                                             |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 109 ms: 1.04x faster                                                             |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.01 ms: 1.03x faster                                                            |
| scimark_lu                       | 51.3 ms                                                  | 49.8 ms: 1.03x faster                                                            |
| sympy_integrate                  | 8.02 ms                                                  | 7.80 ms: 1.03x faster                                                            |
| scimark_monte_carlo              | 32.2 ms                                                  | 31.4 ms: 1.03x faster                                                            |
| richards                         | 22.4 ms                                                  | 22.0 ms: 1.02x faster                                                            |
| sympy_str                        | 104 ms                                                   | 103 ms: 1.02x faster                                                             |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                             |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                             |
| richards_super                   | 25.4 ms                                                  | 25.2 ms: 1.01x faster                                                            |
| pprint_safe_repr                 | 328 ms                                                   | 327 ms: 1.00x faster                                                             |
| async_tree_eager                 | 45.6 ms                                                  | 46.1 ms: 1.01x slower                                                            |
| sqlalchemy_declarative           | 46.8 ms                                                  | 47.4 ms: 1.01x slower                                                            |
| regex_v8                         | 9.59 ms                                                  | 9.71 ms: 1.01x slower                                                            |
| crypto_pyaes                     | 38.8 ms                                                  | 39.3 ms: 1.01x slower                                                            |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                            |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                             |
| regex_dna                        | 99.6 ms                                                  | 102 ms: 1.02x slower                                                             |
| fannkuch                         | 176 ms                                                   | 181 ms: 1.03x slower                                                             |
| sympy_expand                     | 167 ms                                                   | 173 ms: 1.04x slower                                                             |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 221 ms: 1.04x slower                                                             |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.38 ms: 1.04x slower                                                            |
| shortest_path                    | 219 ms                                                   | 230 ms: 1.05x slower                                                             |
| bench_mp_pool                    | 39.7 ms                                                  | 41.9 ms: 1.05x slower                                                            |
| connected_components             | 201 ms                                                   | 219 ms: 1.09x slower                                                             |
| json_loads                       | 10.9 us                                                  | 11.9 us: 1.09x slower                                                            |
| mako                             | 4.77 ms                                                  | 5.27 ms: 1.10x slower                                                            |
| django_template                  | 13.6 ms                                                  | 15.1 ms: 1.11x slower                                                            |
| meteor_contest                   | 47.7 ms                                                  | 53.7 ms: 1.12x slower                                                            |
| json_dumps                       | 4.26 ms                                                  | 4.97 ms: 1.17x slower                                                            |
| python_startup                   | 8.01 ms                                                  | 9.51 ms: 1.19x slower                                                            |
| many_optionals                   | 195 us                                                   | 233 us: 1.19x slower                                                             |
| telco                            | 2.61 ms                                                  | 3.14 ms: 1.20x slower                                                            |
| python_startup_no_site           | 5.71 ms                                                  | 7.55 ms: 1.32x slower                                                            |
| bench_thread_pool                | 419 us                                                   | 572 us: 1.37x slower                                                             |
| coverage                         | 26.9 ms                                                  | 38.4 ms: 1.43x slower                                                            |
| async_tree_eager_tg              | 32.1 ms                                                  | 73.7 ms: 2.29x slower                                                            |
| Geometric mean                   | (ref)                                                    | 1.15x faster                                                                     |

Benchmark hidden because not significant (4): pickle_pure_python, pprint_pformat, sympy_sum, genshi_text
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250403-3.14.0a6+-0227a6d-NOGIL/bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.156x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.23x