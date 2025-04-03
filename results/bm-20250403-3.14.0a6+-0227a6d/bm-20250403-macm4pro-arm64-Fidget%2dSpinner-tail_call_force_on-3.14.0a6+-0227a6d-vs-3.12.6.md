# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: tail_call_force_on
- machine: darwin-arm64
- commit hash: 0227a6d
- commit date: 2025-04-03
- overall geometric mean: 1.150x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 106 ms: 1.08x faster                                                             |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                           |
| html5lib       | 23.0 ms                                                  | 23.2 ms: 1.01x slower                                                            |
| sphinx         | 434 ms                                                   | 401 ms: 1.08x faster                                                             |
| Geometric mean | (ref)                                                    | 1.03x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------------------------|:--------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 235 ms: 2.11x faster                                                             |
| async_tree_io_tg                 | 480 ms                                                   | 242 ms: 1.98x faster                                                             |
| async_tree_io                    | 459 ms                                                   | 241 ms: 1.91x faster                                                             |
| async_tree_eager_io_tg           | 446 ms                                                   | 248 ms: 1.80x faster                                                             |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.68x faster                                                             |
| async_tree_none                  | 178 ms                                                   | 109 ms: 1.64x faster                                                             |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                             |
| async_tree_memoization           | 223 ms                                                   | 144 ms: 1.54x faster                                                             |
| coroutines                       | 13.6 ms                                                  | 9.29 ms: 1.46x faster                                                            |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                             |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 258 ms: 1.29x faster                                                             |
| async_generators                 | 206 ms                                                   | 166 ms: 1.25x faster                                                             |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                             |
| async_tree_eager                 | 45.6 ms                                                  | 39.1 ms: 1.16x faster                                                            |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 217 ms: 1.06x faster                                                             |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                             |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                             |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                             |
| async_tree_eager_tg              | 32.1 ms                                                  | 85.5 ms: 2.66x slower                                                            |
| Geometric mean                   | (ref)                                                    | 1.29x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.0 ms: 1.35x faster                                                            |
| nbody          | 54.2 ms                                                  | 46.8 ms: 1.16x faster                                                            |
| pidigits       | 161 ms                                                   | 167 ms: 1.03x slower                                                             |
| Geometric mean | (ref)                                                    | 1.15x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------|:--------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 43.3 ms: 1.26x faster                                                            |
| regex_effbot   | 1.67 ms                                                  | 1.51 ms: 1.10x faster                                                            |
| regex_dna      | 99.6 ms                                                  | 104 ms: 1.04x slower                                                             |
| regex_v8       | 9.59 ms                                                  | 10.3 ms: 1.07x slower                                                            |
| Geometric mean | (ref)                                                    | 1.06x faster                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------------|:--------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 801 ms: 1.19x faster                                                             |
| xml_etree_iterparse  | 51.6 ms                                                  | 43.3 ms: 1.19x faster                                                            |
| xml_etree_generate   | 38.9 ms                                                  | 33.0 ms: 1.18x faster                                                            |
| xml_etree_parse      | 67.9 ms                                                  | 60.5 ms: 1.12x faster                                                            |
| xml_etree_process    | 26.7 ms                                                  | 24.0 ms: 1.11x faster                                                            |
| unpickle_pure_python | 103 us                                                   | 92.7 us: 1.11x faster                                                            |
| pickle_pure_python   | 139 us                                                   | 134 us: 1.04x faster                                                             |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                            |
| json_dumps           | 4.26 ms                                                  | 4.95 ms: 1.16x slower                                                            |
| Geometric mean       | (ref)                                                    | 1.08x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|------------------------|:--------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.05 ms: 1.13x slower                                                            |
| python_startup_no_site | 5.71 ms                                                  | 6.72 ms: 1.18x slower                                                            |
| Geometric mean         | (ref)                                                    | 1.15x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|-----------------|:--------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.23 ms: 1.14x faster                                                            |
| genshi_xml      | 21.8 ms                                                  | 19.3 ms: 1.13x faster                                                            |
| mako            | 4.77 ms                                                  | 4.65 ms: 1.03x faster                                                            |
| django_template | 13.6 ms                                                  | 14.2 ms: 1.04x slower                                                            |
| Geometric mean  | (ref)                                                    | 1.06x faster                                                                     |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d |
|----------------------------------|:--------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 8.28 ms: 2.51x faster                                                            |
| mdp                              | 1.09 sec                                                 | 505 ms: 2.16x faster                                                             |
| async_tree_eager_io              | 496 ms                                                   | 235 ms: 2.11x faster                                                             |
| async_tree_io_tg                 | 480 ms                                                   | 242 ms: 1.98x faster                                                             |
| async_tree_io                    | 459 ms                                                   | 241 ms: 1.91x faster                                                             |
| async_tree_eager_io_tg           | 446 ms                                                   | 248 ms: 1.80x faster                                                             |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.68x faster                                                             |
| deepcopy                         | 161 us                                                   | 98.1 us: 1.65x faster                                                            |
| async_tree_none                  | 178 ms                                                   | 109 ms: 1.64x faster                                                             |
| deepcopy_memo                    | 18.3 us                                                  | 11.2 us: 1.63x faster                                                            |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                             |
| generators                       | 21.9 ms                                                  | 14.0 ms: 1.57x faster                                                            |
| async_tree_memoization           | 223 ms                                                   | 144 ms: 1.54x faster                                                             |
| coroutines                       | 13.6 ms                                                  | 9.29 ms: 1.46x faster                                                            |
| deepcopy_reduce                  | 1.46 us                                                  | 1.02 us: 1.43x faster                                                            |
| comprehensions                   | 9.84 us                                                  | 7.04 us: 1.40x faster                                                            |
| go                               | 70.0 ms                                                  | 51.3 ms: 1.36x faster                                                            |
| float                            | 37.9 ms                                                  | 28.0 ms: 1.35x faster                                                            |
| logging_silent                   | 50.9 ns                                                  | 37.8 ns: 1.35x faster                                                            |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                             |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 258 ms: 1.29x faster                                                             |
| raytrace                         | 145 ms                                                   | 114 ms: 1.27x faster                                                             |
| regex_compile                    | 54.6 ms                                                  | 43.3 ms: 1.26x faster                                                            |
| dulwich_log                      | 21.3 ms                                                  | 17.0 ms: 1.25x faster                                                            |
| async_generators                 | 206 ms                                                   | 166 ms: 1.25x faster                                                             |
| deltablue                        | 1.73 ms                                                  | 1.41 ms: 1.22x faster                                                            |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                             |
| scimark_sor                      | 61.0 ms                                                  | 50.4 ms: 1.21x faster                                                            |
| tomli_loads                      | 957 ms                                                   | 801 ms: 1.19x faster                                                             |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.3 ms: 1.19x faster                                                            |
| k_core                           | 1.12 sec                                                 | 945 ms: 1.18x faster                                                             |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.89 sec: 1.18x faster                                                           |
| xml_etree_generate               | 38.9 ms                                                  | 33.0 ms: 1.18x faster                                                            |
| hexiom                           | 3.04 ms                                                  | 2.59 ms: 1.17x faster                                                            |
| typing_runtime_protocols         | 71.0 us                                                  | 60.7 us: 1.17x faster                                                            |
| async_tree_eager                 | 45.6 ms                                                  | 39.1 ms: 1.16x faster                                                            |
| logging_simple                   | 2.57 us                                                  | 2.22 us: 1.16x faster                                                            |
| nbody                            | 54.2 ms                                                  | 46.8 ms: 1.16x faster                                                            |
| pylint                           | 128 ms                                                   | 111 ms: 1.15x faster                                                             |
| scimark_lu                       | 51.3 ms                                                  | 44.5 ms: 1.15x faster                                                            |
| logging_format                   | 2.80 us                                                  | 2.44 us: 1.15x faster                                                            |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                            |
| genshi_text                      | 10.5 ms                                                  | 9.23 ms: 1.14x faster                                                            |
| pyflate                          | 216 ms                                                   | 191 ms: 1.13x faster                                                             |
| genshi_xml                       | 21.8 ms                                                  | 19.3 ms: 1.13x faster                                                            |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.6 ms: 1.12x faster                                                            |
| xml_etree_parse                  | 67.9 ms                                                  | 60.5 ms: 1.12x faster                                                            |
| xml_etree_process                | 26.7 ms                                                  | 24.0 ms: 1.11x faster                                                            |
| scimark_fft                      | 142 ms                                                   | 127 ms: 1.11x faster                                                             |
| unpickle_pure_python             | 103 us                                                   | 92.7 us: 1.11x faster                                                            |
| chaos                            | 28.9 ms                                                  | 26.2 ms: 1.11x faster                                                            |
| regex_effbot                     | 1.67 ms                                                  | 1.51 ms: 1.10x faster                                                            |
| richards                         | 22.4 ms                                                  | 20.4 ms: 1.10x faster                                                            |
| sympy_str                        | 104 ms                                                   | 94.9 ms: 1.10x faster                                                            |
| spectral_norm                    | 54.4 ms                                                  | 49.6 ms: 1.10x faster                                                            |
| richards_super                   | 25.4 ms                                                  | 23.2 ms: 1.10x faster                                                            |
| nqueens                          | 43.5 ms                                                  | 39.9 ms: 1.09x faster                                                            |
| pprint_pformat                   | 665 ms                                                   | 610 ms: 1.09x faster                                                             |
| sympy_integrate                  | 8.02 ms                                                  | 7.37 ms: 1.09x faster                                                            |
| sqlalchemy_declarative           | 46.8 ms                                                  | 43.1 ms: 1.08x faster                                                            |
| sphinx                           | 434 ms                                                   | 401 ms: 1.08x faster                                                             |
| pprint_safe_repr                 | 328 ms                                                   | 304 ms: 1.08x faster                                                             |
| 2to3                             | 114 ms                                                   | 106 ms: 1.08x faster                                                             |
| sympy_sum                        | 57.6 ms                                                  | 53.9 ms: 1.07x faster                                                            |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 217 ms: 1.06x faster                                                             |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.96 ms: 1.06x faster                                                            |
| pycparser                        | 497 ms                                                   | 471 ms: 1.06x faster                                                             |
| sympy_expand                     | 167 ms                                                   | 159 ms: 1.05x faster                                                             |
| sqlite_synth                     | 967 ns                                                   | 923 ns: 1.05x faster                                                             |
| pickle_pure_python               | 139 us                                                   | 134 us: 1.04x faster                                                             |
| crypto_pyaes                     | 38.8 ms                                                  | 37.6 ms: 1.03x faster                                                            |
| mako                             | 4.77 ms                                                  | 4.65 ms: 1.03x faster                                                            |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.08 ms: 1.02x faster                                                            |
| shortest_path                    | 219 ms                                                   | 216 ms: 1.01x faster                                                             |
| fannkuch                         | 176 ms                                                   | 173 ms: 1.01x faster                                                             |
| bench_thread_pool                | 419 us                                                   | 414 us: 1.01x faster                                                             |
| meteor_contest                   | 47.7 ms                                                  | 47.6 ms: 1.00x faster                                                            |
| connected_components             | 201 ms                                                   | 200 ms: 1.00x faster                                                             |
| json                             | 1.93 ms                                                  | 1.95 ms: 1.01x slower                                                            |
| html5lib                         | 23.0 ms                                                  | 23.2 ms: 1.01x slower                                                            |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                             |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                           |
| bench_mp_pool                    | 39.7 ms                                                  | 40.5 ms: 1.02x slower                                                            |
| gc_traversal                     | 2.01 ms                                                  | 2.08 ms: 1.03x slower                                                            |
| pidigits                         | 161 ms                                                   | 167 ms: 1.03x slower                                                             |
| regex_dna                        | 99.6 ms                                                  | 104 ms: 1.04x slower                                                             |
| django_template                  | 13.6 ms                                                  | 14.2 ms: 1.04x slower                                                            |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                            |
| regex_v8                         | 9.59 ms                                                  | 10.3 ms: 1.07x slower                                                            |
| create_gc_cycles                 | 830 us                                                   | 898 us: 1.08x slower                                                             |
| python_startup                   | 8.01 ms                                                  | 9.05 ms: 1.13x slower                                                            |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                             |
| many_optionals                   | 195 us                                                   | 225 us: 1.15x slower                                                             |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                             |
| telco                            | 2.61 ms                                                  | 3.02 ms: 1.16x slower                                                            |
| json_dumps                       | 4.26 ms                                                  | 4.95 ms: 1.16x slower                                                            |
| python_startup_no_site           | 5.71 ms                                                  | 6.72 ms: 1.18x slower                                                            |
| coverage                         | 26.9 ms                                                  | 32.5 ms: 1.21x slower                                                            |
| async_tree_eager_tg              | 32.1 ms                                                  | 85.5 ms: 2.66x slower                                                            |
| Geometric mean                   | (ref)                                                    | 1.15x faster                                                                     |
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250403-3.14.0a6+-0227a6d/bm-20250403-macm4pro-arm64-Fidget%2dSpinner-tail_call_force_on-3.14.0a6+-0227a6d.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.150x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.11x