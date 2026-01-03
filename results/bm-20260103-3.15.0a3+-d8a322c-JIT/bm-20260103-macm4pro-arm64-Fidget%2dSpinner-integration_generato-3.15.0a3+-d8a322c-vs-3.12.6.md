# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: integration_generato
- machine: darwin-arm64
- commit hash: d8a322c
- commit date: 2026-01-03
- overall geometric mean: 1.247x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x faster
- Memory change: 1.27x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-integration_generato-3.15.0a3+-d8a322c |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 110 ms: 1.03x faster                                                               |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                             |
| html5lib       | 23.0 ms                                                  | 20.2 ms: 1.14x faster                                                              |
| sphinx         | 434 ms                                                   | 394 ms: 1.10x faster                                                               |
| Geometric mean | (ref)                                                    | 1.07x faster                                                                       |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-integration_generato-3.15.0a3+-d8a322c |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 220 ms: 2.26x faster                                                               |
| async_tree_io_tg                 | 480 ms                                                   | 219 ms: 2.19x faster                                                               |
| async_tree_eager_io_tg           | 446 ms                                                   | 219 ms: 2.04x faster                                                               |
| async_tree_io                    | 459 ms                                                   | 226 ms: 2.03x faster                                                               |
| async_tree_none                  | 178 ms                                                   | 96.2 ms: 1.85x faster                                                              |
| async_tree_none_tg               | 172 ms                                                   | 96.4 ms: 1.79x faster                                                              |
| async_tree_memoization_tg        | 231 ms                                                   | 134 ms: 1.72x faster                                                               |
| async_tree_memoization           | 223 ms                                                   | 136 ms: 1.64x faster                                                               |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 242 ms: 1.38x faster                                                               |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 247 ms: 1.37x faster                                                               |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.30x faster                                                              |
| async_tree_eager                 | 45.6 ms                                                  | 36.9 ms: 1.23x faster                                                              |
| async_generators                 | 206 ms                                                   | 192 ms: 1.07x faster                                                               |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 215 ms: 1.07x faster                                                               |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                               |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 238 ms: 1.12x slower                                                               |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.9 ms: 2.42x slower                                                              |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                                       |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-integration_generato-3.15.0a3+-d8a322c |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 23.0 ms: 1.65x faster                                                              |
| nbody          | 54.2 ms                                                  | 40.1 ms: 1.35x faster                                                              |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                               |
| Geometric mean | (ref)                                                    | 1.30x faster                                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-integration_generato-3.15.0a3+-d8a322c |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 40.8 ms: 1.34x faster                                                              |
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                              |
| regex_dna      | 99.6 ms                                                  | 94.7 ms: 1.05x faster                                                              |
| regex_v8       | 9.59 ms                                                  | 9.81 ms: 1.02x slower                                                              |
| Geometric mean | (ref)                                                    | 1.12x faster                                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-integration_generato-3.15.0a3+-d8a322c |
|----------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| unpickle_pure_python | 103 us                                                   | 72.3 us: 1.42x faster                                                              |
| xml_etree_iterparse  | 51.6 ms                                                  | 37.9 ms: 1.36x faster                                                              |
| xml_etree_generate   | 38.9 ms                                                  | 31.0 ms: 1.25x faster                                                              |
| pickle_pure_python   | 139 us                                                   | 112 us: 1.25x faster                                                               |
| tomli_loads          | 957 ms                                                   | 780 ms: 1.23x faster                                                               |
| xml_etree_process    | 26.7 ms                                                  | 22.0 ms: 1.22x faster                                                              |
| json_dumps           | 4.26 ms                                                  | 3.66 ms: 1.16x faster                                                              |
| xml_etree_parse      | 67.9 ms                                                  | 61.0 ms: 1.11x faster                                                              |
| json_loads           | 10.9 us                                                  | 10.6 us: 1.02x faster                                                              |
| Geometric mean       | (ref)                                                    | 1.22x faster                                                                       |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-integration_generato-3.15.0a3+-d8a322c |
|------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.84 ms: 1.10x slower                                                              |
| python_startup_no_site | 5.71 ms                                                  | 6.37 ms: 1.12x slower                                                              |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-integration_generato-3.15.0a3+-d8a322c |
|-----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 3.93 ms: 1.22x faster                                                              |
| genshi_text     | 10.5 ms                                                  | 8.75 ms: 1.20x faster                                                              |
| genshi_xml      | 21.8 ms                                                  | 20.3 ms: 1.07x faster                                                              |
| django_template | 13.6 ms                                                  | 13.9 ms: 1.02x slower                                                              |
| Geometric mean  | (ref)                                                    | 1.11x faster                                                                       |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260103-macm4pro-arm64-Fidget%2dSpinner-integration_generato-3.15.0a3+-d8a322c |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.92 ms: 5.30x faster                                                              |
| richards                         | 22.4 ms                                                  | 9.85 ms: 2.27x faster                                                              |
| async_tree_eager_io              | 496 ms                                                   | 220 ms: 2.26x faster                                                               |
| richards_super                   | 25.4 ms                                                  | 11.6 ms: 2.20x faster                                                              |
| async_tree_io_tg                 | 480 ms                                                   | 219 ms: 2.19x faster                                                               |
| async_tree_eager_io_tg           | 446 ms                                                   | 219 ms: 2.04x faster                                                               |
| async_tree_io                    | 459 ms                                                   | 226 ms: 2.03x faster                                                               |
| mdp                              | 1.09 sec                                                 | 587 ms: 1.86x faster                                                               |
| async_tree_none                  | 178 ms                                                   | 96.2 ms: 1.85x faster                                                              |
| async_tree_none_tg               | 172 ms                                                   | 96.4 ms: 1.79x faster                                                              |
| async_tree_memoization_tg        | 231 ms                                                   | 134 ms: 1.72x faster                                                               |
| deepcopy                         | 161 us                                                   | 96.7 us: 1.67x faster                                                              |
| float                            | 37.9 ms                                                  | 23.0 ms: 1.65x faster                                                              |
| async_tree_memoization           | 223 ms                                                   | 136 ms: 1.64x faster                                                               |
| go                               | 70.0 ms                                                  | 43.2 ms: 1.62x faster                                                              |
| deepcopy_memo                    | 18.3 us                                                  | 11.3 us: 1.62x faster                                                              |
| comprehensions                   | 9.84 us                                                  | 6.17 us: 1.59x faster                                                              |
| deltablue                        | 1.73 ms                                                  | 1.13 ms: 1.52x faster                                                              |
| deepcopy_reduce                  | 1.46 us                                                  | 965 ns: 1.51x faster                                                               |
| pyflate                          | 216 ms                                                   | 144 ms: 1.50x faster                                                               |
| logging_silent                   | 50.9 ns                                                  | 34.4 ns: 1.48x faster                                                              |
| scimark_monte_carlo              | 32.2 ms                                                  | 22.0 ms: 1.46x faster                                                              |
| scimark_sor                      | 61.0 ms                                                  | 42.1 ms: 1.45x faster                                                              |
| unpickle_pure_python             | 103 us                                                   | 72.3 us: 1.42x faster                                                              |
| scimark_fft                      | 142 ms                                                   | 101 ms: 1.40x faster                                                               |
| scimark_lu                       | 51.3 ms                                                  | 37.0 ms: 1.39x faster                                                              |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 242 ms: 1.38x faster                                                               |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 247 ms: 1.37x faster                                                               |
| raytrace                         | 145 ms                                                   | 107 ms: 1.36x faster                                                               |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.9 ms: 1.36x faster                                                              |
| nbody                            | 54.2 ms                                                  | 40.1 ms: 1.35x faster                                                              |
| regex_compile                    | 54.6 ms                                                  | 40.8 ms: 1.34x faster                                                              |
| spectral_norm                    | 54.4 ms                                                  | 41.0 ms: 1.33x faster                                                              |
| chaos                            | 28.9 ms                                                  | 22.2 ms: 1.30x faster                                                              |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.30x faster                                                              |
| k_core                           | 1.12 sec                                                 | 865 ms: 1.29x faster                                                               |
| pprint_safe_repr                 | 328 ms                                                   | 256 ms: 1.28x faster                                                               |
| pprint_pformat                   | 665 ms                                                   | 521 ms: 1.27x faster                                                               |
| crypto_pyaes                     | 38.8 ms                                                  | 30.9 ms: 1.26x faster                                                              |
| xml_etree_generate               | 38.9 ms                                                  | 31.0 ms: 1.25x faster                                                              |
| pickle_pure_python               | 139 us                                                   | 112 us: 1.25x faster                                                               |
| async_tree_eager                 | 45.6 ms                                                  | 36.9 ms: 1.23x faster                                                              |
| tomli_loads                      | 957 ms                                                   | 780 ms: 1.23x faster                                                               |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.84 sec: 1.22x faster                                                             |
| logging_simple                   | 2.57 us                                                  | 2.11 us: 1.22x faster                                                              |
| xml_etree_process                | 26.7 ms                                                  | 22.0 ms: 1.22x faster                                                              |
| mako                             | 4.77 ms                                                  | 3.93 ms: 1.22x faster                                                              |
| logging_format                   | 2.80 us                                                  | 2.33 us: 1.20x faster                                                              |
| genshi_text                      | 10.5 ms                                                  | 8.75 ms: 1.20x faster                                                              |
| generators                       | 21.9 ms                                                  | 18.6 ms: 1.18x faster                                                              |
| json_dumps                       | 4.26 ms                                                  | 3.66 ms: 1.16x faster                                                              |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                              |
| typing_runtime_protocols         | 71.0 us                                                  | 61.8 us: 1.15x faster                                                              |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                              |
| hexiom                           | 3.04 ms                                                  | 2.65 ms: 1.15x faster                                                              |
| fannkuch                         | 176 ms                                                   | 153 ms: 1.14x faster                                                               |
| html5lib                         | 23.0 ms                                                  | 20.2 ms: 1.14x faster                                                              |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                              |
| nqueens                          | 43.5 ms                                                  | 38.4 ms: 1.13x faster                                                              |
| pycparser                        | 497 ms                                                   | 445 ms: 1.12x faster                                                               |
| xml_etree_parse                  | 67.9 ms                                                  | 61.0 ms: 1.11x faster                                                              |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.87 ms: 1.11x faster                                                              |
| sphinx                           | 434 ms                                                   | 394 ms: 1.10x faster                                                               |
| genshi_xml                       | 21.8 ms                                                  | 20.3 ms: 1.07x faster                                                              |
| async_generators                 | 206 ms                                                   | 192 ms: 1.07x faster                                                               |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 215 ms: 1.07x faster                                                               |
| thrift                           | 322 us                                                   | 305 us: 1.05x faster                                                               |
| sympy_integrate                  | 8.02 ms                                                  | 7.63 ms: 1.05x faster                                                              |
| regex_dna                        | 99.6 ms                                                  | 94.7 ms: 1.05x faster                                                              |
| pylint                           | 128 ms                                                   | 122 ms: 1.05x faster                                                               |
| json                             | 1.93 ms                                                  | 1.84 ms: 1.05x faster                                                              |
| meteor_contest                   | 47.7 ms                                                  | 46.2 ms: 1.03x faster                                                              |
| 2to3                             | 114 ms                                                   | 110 ms: 1.03x faster                                                               |
| json_loads                       | 10.9 us                                                  | 10.6 us: 1.02x faster                                                              |
| sympy_sum                        | 57.6 ms                                                  | 56.5 ms: 1.02x faster                                                              |
| shortest_path                    | 219 ms                                                   | 215 ms: 1.02x faster                                                               |
| connected_components             | 201 ms                                                   | 198 ms: 1.02x faster                                                               |
| telco                            | 2.61 ms                                                  | 2.58 ms: 1.01x faster                                                              |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                             |
| sqlite_synth                     | 967 ns                                                   | 974 ns: 1.01x slower                                                               |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                               |
| sympy_str                        | 104 ms                                                   | 106 ms: 1.02x slower                                                               |
| django_template                  | 13.6 ms                                                  | 13.9 ms: 1.02x slower                                                              |
| bench_thread_pool                | 419 us                                                   | 426 us: 1.02x slower                                                               |
| regex_v8                         | 9.59 ms                                                  | 9.81 ms: 1.02x slower                                                              |
| gc_traversal                     | 2.01 ms                                                  | 2.07 ms: 1.03x slower                                                              |
| sympy_expand                     | 167 ms                                                   | 175 ms: 1.05x slower                                                               |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                               |
| python_startup                   | 8.01 ms                                                  | 8.84 ms: 1.10x slower                                                              |
| python_startup_no_site           | 5.71 ms                                                  | 6.37 ms: 1.12x slower                                                              |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 238 ms: 1.12x slower                                                               |
| create_gc_cycles                 | 830 us                                                   | 931 us: 1.12x slower                                                               |
| bench_mp_pool                    | 39.7 ms                                                  | 45.1 ms: 1.13x slower                                                              |
| coverage                         | 26.9 ms                                                  | 33.1 ms: 1.23x slower                                                              |
| many_optionals                   | 195 us                                                   | 250 us: 1.28x slower                                                               |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.9 ms: 2.42x slower                                                              |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                                       |
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: async_tree_eager_memoization, asyncio_websockets, chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260103-3.15.0a3+-d8a322c-JIT/bm-20260103-macm4pro-arm64-Fidget%2dSpinner-integration_generato-3.15.0a3+-d8a322c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.247x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.17x
- 95% likely to have a speedup of 1.15x
- 99% likely to have a speedup of 1.13x

# Memory
- memory change: 1.27x