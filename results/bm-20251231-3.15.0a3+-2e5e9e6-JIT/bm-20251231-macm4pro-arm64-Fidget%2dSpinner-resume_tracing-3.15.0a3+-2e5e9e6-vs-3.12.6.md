# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: resume_tracing
- machine: darwin-arm64
- commit hash: 2e5e9e6
- commit date: 2025-12-31
- overall geometric mean: 1.226x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-2e5e9e6 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 111 ms: 1.03x faster                                                         |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                       |
| html5lib       | 23.0 ms                                                  | 20.2 ms: 1.14x faster                                                        |
| sphinx         | 434 ms                                                   | 411 ms: 1.06x faster                                                         |
| Geometric mean | (ref)                                                    | 1.05x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-2e5e9e6 |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 217 ms: 2.28x faster                                                         |
| async_tree_io_tg                 | 480 ms                                                   | 214 ms: 2.24x faster                                                         |
| async_tree_eager_io_tg           | 446 ms                                                   | 215 ms: 2.08x faster                                                         |
| async_tree_io                    | 459 ms                                                   | 227 ms: 2.03x faster                                                         |
| async_tree_none                  | 178 ms                                                   | 97.2 ms: 1.83x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 94.9 ms: 1.81x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 132 ms: 1.75x faster                                                         |
| async_tree_memoization           | 223 ms                                                   | 135 ms: 1.65x faster                                                         |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 247 ms: 1.35x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 251 ms: 1.35x faster                                                         |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.23x faster                                                         |
| async_tree_eager                 | 45.6 ms                                                  | 38.8 ms: 1.17x faster                                                        |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                         |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                         |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.05x slower                                                         |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.13x slower                                                         |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.3 ms: 2.47x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.35x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-2e5e9e6 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 24.1 ms: 1.57x faster                                                        |
| nbody          | 54.2 ms                                                  | 39.8 ms: 1.36x faster                                                        |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                    | 1.28x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-2e5e9e6 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 40.3 ms: 1.36x faster                                                        |
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                        |
| regex_dna      | 99.6 ms                                                  | 96.8 ms: 1.03x faster                                                        |
| regex_v8       | 9.59 ms                                                  | 9.81 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                    | 1.11x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-2e5e9e6 |
|----------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| unpickle_pure_python | 103 us                                                   | 72.6 us: 1.42x faster                                                        |
| xml_etree_iterparse  | 51.6 ms                                                  | 37.7 ms: 1.37x faster                                                        |
| pickle_pure_python   | 139 us                                                   | 114 us: 1.22x faster                                                         |
| tomli_loads          | 957 ms                                                   | 798 ms: 1.20x faster                                                         |
| xml_etree_generate   | 38.9 ms                                                  | 32.6 ms: 1.19x faster                                                        |
| xml_etree_process    | 26.7 ms                                                  | 22.4 ms: 1.19x faster                                                        |
| json_dumps           | 4.26 ms                                                  | 3.64 ms: 1.17x faster                                                        |
| xml_etree_parse      | 67.9 ms                                                  | 61.6 ms: 1.10x faster                                                        |
| json_loads           | 10.9 us                                                  | 10.6 us: 1.02x faster                                                        |
| Geometric mean       | (ref)                                                    | 1.20x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-2e5e9e6 |
|------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.95 ms: 1.12x slower                                                        |
| python_startup_no_site | 5.71 ms                                                  | 6.45 ms: 1.13x slower                                                        |
| Geometric mean         | (ref)                                                    | 1.12x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-2e5e9e6 |
|-----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.12 ms: 1.16x faster                                                        |
| genshi_text     | 10.5 ms                                                  | 9.58 ms: 1.09x faster                                                        |
| django_template | 13.6 ms                                                  | 13.1 ms: 1.04x faster                                                        |
| genshi_xml      | 21.8 ms                                                  | 22.8 ms: 1.05x slower                                                        |
| Geometric mean  | (ref)                                                    | 1.06x faster                                                                 |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-2e5e9e6 |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.90 ms: 5.32x faster                                                        |
| async_tree_eager_io              | 496 ms                                                   | 217 ms: 2.28x faster                                                         |
| async_tree_io_tg                 | 480 ms                                                   | 214 ms: 2.24x faster                                                         |
| async_tree_eager_io_tg           | 446 ms                                                   | 215 ms: 2.08x faster                                                         |
| async_tree_io                    | 459 ms                                                   | 227 ms: 2.03x faster                                                         |
| richards                         | 22.4 ms                                                  | 11.6 ms: 1.93x faster                                                        |
| richards_super                   | 25.4 ms                                                  | 13.4 ms: 1.89x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 97.2 ms: 1.83x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 94.9 ms: 1.81x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 132 ms: 1.75x faster                                                         |
| mdp                              | 1.09 sec                                                 | 632 ms: 1.73x faster                                                         |
| async_tree_memoization           | 223 ms                                                   | 135 ms: 1.65x faster                                                         |
| deepcopy                         | 161 us                                                   | 101 us: 1.61x faster                                                         |
| scimark_sor                      | 61.0 ms                                                  | 38.2 ms: 1.60x faster                                                        |
| comprehensions                   | 9.84 us                                                  | 6.19 us: 1.59x faster                                                        |
| float                            | 37.9 ms                                                  | 24.1 ms: 1.57x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 11.9 us: 1.54x faster                                                        |
| go                               | 70.0 ms                                                  | 46.3 ms: 1.51x faster                                                        |
| logging_silent                   | 50.9 ns                                                  | 34.0 ns: 1.50x faster                                                        |
| scimark_lu                       | 51.3 ms                                                  | 34.6 ms: 1.48x faster                                                        |
| deltablue                        | 1.73 ms                                                  | 1.17 ms: 1.47x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.01 us: 1.44x faster                                                        |
| unpickle_pure_python             | 103 us                                                   | 72.6 us: 1.42x faster                                                        |
| logging_simple                   | 2.57 us                                                  | 1.81 us: 1.42x faster                                                        |
| logging_format                   | 2.80 us                                                  | 1.98 us: 1.41x faster                                                        |
| scimark_monte_carlo              | 32.2 ms                                                  | 23.0 ms: 1.40x faster                                                        |
| scimark_fft                      | 142 ms                                                   | 101 ms: 1.40x faster                                                         |
| pyflate                          | 216 ms                                                   | 155 ms: 1.40x faster                                                         |
| raytrace                         | 145 ms                                                   | 104 ms: 1.39x faster                                                         |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.7 ms: 1.37x faster                                                        |
| nbody                            | 54.2 ms                                                  | 39.8 ms: 1.36x faster                                                        |
| chaos                            | 28.9 ms                                                  | 21.3 ms: 1.36x faster                                                        |
| regex_compile                    | 54.6 ms                                                  | 40.3 ms: 1.36x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 247 ms: 1.35x faster                                                         |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 251 ms: 1.35x faster                                                         |
| spectral_norm                    | 54.4 ms                                                  | 41.1 ms: 1.32x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                        |
| k_core                           | 1.12 sec                                                 | 864 ms: 1.29x faster                                                         |
| crypto_pyaes                     | 38.8 ms                                                  | 31.1 ms: 1.25x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.23x faster                                                         |
| pickle_pure_python               | 139 us                                                   | 114 us: 1.22x faster                                                         |
| tomli_loads                      | 957 ms                                                   | 798 ms: 1.20x faster                                                         |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.87 sec: 1.20x faster                                                       |
| xml_etree_generate               | 38.9 ms                                                  | 32.6 ms: 1.19x faster                                                        |
| xml_etree_process                | 26.7 ms                                                  | 22.4 ms: 1.19x faster                                                        |
| pprint_pformat                   | 665 ms                                                   | 559 ms: 1.19x faster                                                         |
| pprint_safe_repr                 | 328 ms                                                   | 278 ms: 1.18x faster                                                         |
| async_tree_eager                 | 45.6 ms                                                  | 38.8 ms: 1.17x faster                                                        |
| json_dumps                       | 4.26 ms                                                  | 3.64 ms: 1.17x faster                                                        |
| generators                       | 21.9 ms                                                  | 18.8 ms: 1.17x faster                                                        |
| mako                             | 4.77 ms                                                  | 4.12 ms: 1.16x faster                                                        |
| fannkuch                         | 176 ms                                                   | 153 ms: 1.14x faster                                                         |
| html5lib                         | 23.0 ms                                                  | 20.2 ms: 1.14x faster                                                        |
| dulwich_log                      | 21.3 ms                                                  | 18.7 ms: 1.14x faster                                                        |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                        |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                        |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                         |
| hexiom                           | 3.04 ms                                                  | 2.71 ms: 1.12x faster                                                        |
| typing_runtime_protocols         | 71.0 us                                                  | 63.5 us: 1.12x faster                                                        |
| nqueens                          | 43.5 ms                                                  | 39.1 ms: 1.11x faster                                                        |
| xml_etree_parse                  | 67.9 ms                                                  | 61.6 ms: 1.10x faster                                                        |
| thrift                           | 322 us                                                   | 294 us: 1.09x faster                                                         |
| genshi_text                      | 10.5 ms                                                  | 9.58 ms: 1.09x faster                                                        |
| pycparser                        | 497 ms                                                   | 462 ms: 1.08x faster                                                         |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.93 ms: 1.07x faster                                                        |
| sphinx                           | 434 ms                                                   | 411 ms: 1.06x faster                                                         |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                         |
| meteor_contest                   | 47.7 ms                                                  | 45.9 ms: 1.04x faster                                                        |
| django_template                  | 13.6 ms                                                  | 13.1 ms: 1.04x faster                                                        |
| json                             | 1.93 ms                                                  | 1.86 ms: 1.04x faster                                                        |
| regex_dna                        | 99.6 ms                                                  | 96.8 ms: 1.03x faster                                                        |
| 2to3                             | 114 ms                                                   | 111 ms: 1.03x faster                                                         |
| json_loads                       | 10.9 us                                                  | 10.6 us: 1.02x faster                                                        |
| connected_components             | 201 ms                                                   | 197 ms: 1.02x faster                                                         |
| telco                            | 2.61 ms                                                  | 2.57 ms: 1.01x faster                                                        |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                         |
| shortest_path                    | 219 ms                                                   | 217 ms: 1.01x faster                                                         |
| regex_v8                         | 9.59 ms                                                  | 9.81 ms: 1.02x slower                                                        |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                         |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                       |
| gc_traversal                     | 2.01 ms                                                  | 2.07 ms: 1.03x slower                                                        |
| bench_thread_pool                | 419 us                                                   | 434 us: 1.04x slower                                                         |
| genshi_xml                       | 21.8 ms                                                  | 22.8 ms: 1.05x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.05x slower                                                         |
| sympy_integrate                  | 8.02 ms                                                  | 8.50 ms: 1.06x slower                                                        |
| sympy_sum                        | 57.6 ms                                                  | 61.7 ms: 1.07x slower                                                        |
| sympy_expand                     | 167 ms                                                   | 184 ms: 1.10x slower                                                         |
| pylint                           | 128 ms                                                   | 141 ms: 1.10x slower                                                         |
| sympy_str                        | 104 ms                                                   | 115 ms: 1.10x slower                                                         |
| python_startup                   | 8.01 ms                                                  | 8.95 ms: 1.12x slower                                                        |
| create_gc_cycles                 | 830 us                                                   | 927 us: 1.12x slower                                                         |
| python_startup_no_site           | 5.71 ms                                                  | 6.45 ms: 1.13x slower                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.13x slower                                                         |
| bench_mp_pool                    | 39.7 ms                                                  | 45.0 ms: 1.13x slower                                                        |
| coverage                         | 26.9 ms                                                  | 32.1 ms: 1.19x slower                                                        |
| many_optionals                   | 195 us                                                   | 258 us: 1.32x slower                                                         |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.3 ms: 2.47x slower                                                        |
| Geometric mean                   | (ref)                                                    | 1.22x faster                                                                 |

Benchmark hidden because not significant (1): sqlite_synth
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251231-3.15.0a3+-2e5e9e6-JIT/bm-20251231-macm4pro-arm64-Fidget%2dSpinner-resume_tracing-3.15.0a3+-2e5e9e6.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.226x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.14x
- 95% likely to have a speedup of 1.13x
- 99% likely to have a speedup of 1.11x

# Memory
- memory change: 1.25x