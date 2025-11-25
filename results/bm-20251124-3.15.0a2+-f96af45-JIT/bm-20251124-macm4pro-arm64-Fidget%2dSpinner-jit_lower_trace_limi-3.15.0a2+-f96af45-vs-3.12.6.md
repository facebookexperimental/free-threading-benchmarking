# Results vs. 3.12.6

- fork: Fidget-Spinner
- ref: jit_lower_trace_limi
- machine: darwin-arm64
- commit hash: f96af45
- commit date: 2025-11-24
- overall geometric mean: 1.162x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-macm4pro-arm64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 116 ms: 1.02x slower                                                               |
| sphinx         | 434 ms                                                   | 8.71 ms: 49.76x faster                                                             |
| Geometric mean | (ref)                                                    | 3.65x faster                                                                       |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-macm4pro-arm64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 224 ms: 2.21x faster                                                               |
| async_tree_io_tg                 | 480 ms                                                   | 229 ms: 2.10x faster                                                               |
| async_tree_io                    | 459 ms                                                   | 232 ms: 1.98x faster                                                               |
| async_tree_eager_io_tg           | 446 ms                                                   | 225 ms: 1.98x faster                                                               |
| async_tree_none_tg               | 172 ms                                                   | 97.3 ms: 1.77x faster                                                              |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                               |
| async_tree_memoization_tg        | 231 ms                                                   | 139 ms: 1.66x faster                                                               |
| async_tree_memoization           | 223 ms                                                   | 136 ms: 1.63x faster                                                               |
| coroutines                       | 13.6 ms                                                  | 9.92 ms: 1.37x faster                                                              |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                               |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 251 ms: 1.33x faster                                                               |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                               |
| async_generators                 | 206 ms                                                   | 185 ms: 1.12x faster                                                               |
| async_tree_eager                 | 45.6 ms                                                  | 42.3 ms: 1.08x faster                                                              |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                               |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                               |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 125 ms: 1.11x slower                                                               |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                               |
| async_tree_eager_tg              | 32.1 ms                                                  | 82.0 ms: 2.55x slower                                                              |
| Geometric mean                   | (ref)                                                    | 1.31x faster                                                                       |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-macm4pro-arm64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.6 ms: 1.28x faster                                                              |
| nbody          | 54.2 ms                                                  | 55.4 ms: 1.02x slower                                                              |
| pidigits       | 161 ms                                                   | 167 ms: 1.04x slower                                                               |
| Geometric mean | (ref)                                                    | 1.07x faster                                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-macm4pro-arm64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 45.2 ms: 1.21x faster                                                              |
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                              |
| regex_dna      | 99.6 ms                                                  | 96.4 ms: 1.03x faster                                                              |
| Geometric mean | (ref)                                                    | 1.10x faster                                                                       |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-macm4pro-arm64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.7 ms: 1.30x faster                                                              |
| tomli_loads          | 957 ms                                                   | 822 ms: 1.16x faster                                                               |
| xml_etree_generate   | 38.9 ms                                                  | 34.1 ms: 1.14x faster                                                              |
| xml_etree_process    | 26.7 ms                                                  | 23.6 ms: 1.13x faster                                                              |
| json_dumps           | 4.26 ms                                                  | 3.83 ms: 1.11x faster                                                              |
| xml_etree_parse      | 67.9 ms                                                  | 61.2 ms: 1.11x faster                                                              |
| unpickle_pure_python | 103 us                                                   | 95.0 us: 1.08x faster                                                              |
| pickle_pure_python   | 139 us                                                   | 133 us: 1.05x faster                                                               |
| json_loads           | 10.9 us                                                  | 10.9 us: 1.01x slower                                                              |
| Geometric mean       | (ref)                                                    | 1.12x faster                                                                       |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-macm4pro-arm64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.09 ms: 1.13x slower                                                              |
| python_startup_no_site | 5.71 ms                                                  | 6.53 ms: 1.14x slower                                                              |
| Geometric mean         | (ref)                                                    | 1.14x slower                                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-macm4pro-arm64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|-----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.40 ms: 1.09x faster                                                              |
| django_template | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                              |
| genshi_xml      | 21.8 ms                                                  | 24.0 ms: 1.10x slower                                                              |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                                       |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251124-macm4pro-arm64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| sphinx                           | 434 ms                                                   | 8.71 ms: 49.76x faster                                                             |
| async_tree_eager_io              | 496 ms                                                   | 224 ms: 2.21x faster                                                               |
| async_tree_io_tg                 | 480 ms                                                   | 229 ms: 2.10x faster                                                               |
| async_tree_io                    | 459 ms                                                   | 232 ms: 1.98x faster                                                               |
| async_tree_eager_io_tg           | 446 ms                                                   | 225 ms: 1.98x faster                                                               |
| async_tree_none_tg               | 172 ms                                                   | 97.3 ms: 1.77x faster                                                              |
| mdp                              | 1.09 sec                                                 | 621 ms: 1.76x faster                                                               |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                               |
| deepcopy_memo                    | 18.3 us                                                  | 11.0 us: 1.67x faster                                                              |
| async_tree_memoization_tg        | 231 ms                                                   | 139 ms: 1.66x faster                                                               |
| async_tree_memoization           | 223 ms                                                   | 136 ms: 1.63x faster                                                               |
| deepcopy                         | 161 us                                                   | 100 us: 1.61x faster                                                               |
| richards_super                   | 25.4 ms                                                  | 17.3 ms: 1.47x faster                                                              |
| richards                         | 22.4 ms                                                  | 15.5 ms: 1.45x faster                                                              |
| deepcopy_reduce                  | 1.46 us                                                  | 1.03 us: 1.42x faster                                                              |
| coroutines                       | 13.6 ms                                                  | 9.92 ms: 1.37x faster                                                              |
| comprehensions                   | 9.84 us                                                  | 7.36 us: 1.34x faster                                                              |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                               |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 251 ms: 1.33x faster                                                               |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.7 ms: 1.30x faster                                                              |
| float                            | 37.9 ms                                                  | 29.6 ms: 1.28x faster                                                              |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                               |
| regex_compile                    | 54.6 ms                                                  | 45.2 ms: 1.21x faster                                                              |
| go                               | 70.0 ms                                                  | 58.2 ms: 1.20x faster                                                              |
| scimark_fft                      | 142 ms                                                   | 120 ms: 1.18x faster                                                               |
| tomli_loads                      | 957 ms                                                   | 822 ms: 1.16x faster                                                               |
| logging_simple                   | 2.57 us                                                  | 2.21 us: 1.16x faster                                                              |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                              |
| logging_format                   | 2.80 us                                                  | 2.44 us: 1.15x faster                                                              |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.1 ms: 1.14x faster                                                              |
| xml_etree_generate               | 38.9 ms                                                  | 34.1 ms: 1.14x faster                                                              |
| pyflate                          | 216 ms                                                   | 190 ms: 1.13x faster                                                               |
| subparsers                       | 20.8 ms                                                  | 18.3 ms: 1.13x faster                                                              |
| generators                       | 21.9 ms                                                  | 19.4 ms: 1.13x faster                                                              |
| xml_etree_process                | 26.7 ms                                                  | 23.6 ms: 1.13x faster                                                              |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                              |
| async_generators                 | 206 ms                                                   | 185 ms: 1.12x faster                                                               |
| pprint_pformat                   | 665 ms                                                   | 595 ms: 1.12x faster                                                               |
| spectral_norm                    | 54.4 ms                                                  | 48.7 ms: 1.12x faster                                                              |
| pprint_safe_repr                 | 328 ms                                                   | 294 ms: 1.11x faster                                                               |
| json_dumps                       | 4.26 ms                                                  | 3.83 ms: 1.11x faster                                                              |
| deltablue                        | 1.73 ms                                                  | 1.55 ms: 1.11x faster                                                              |
| xml_etree_parse                  | 67.9 ms                                                  | 61.2 ms: 1.11x faster                                                              |
| raytrace                         | 145 ms                                                   | 132 ms: 1.10x faster                                                               |
| typing_runtime_protocols         | 71.0 us                                                  | 65.0 us: 1.09x faster                                                              |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.05 sec: 1.09x faster                                                             |
| mako                             | 4.77 ms                                                  | 4.40 ms: 1.09x faster                                                              |
| scimark_sor                      | 61.0 ms                                                  | 56.3 ms: 1.08x faster                                                              |
| unpickle_pure_python             | 103 us                                                   | 95.0 us: 1.08x faster                                                              |
| async_tree_eager                 | 45.6 ms                                                  | 42.3 ms: 1.08x faster                                                              |
| dulwich_log                      | 21.3 ms                                                  | 19.8 ms: 1.07x faster                                                              |
| thrift                           | 322 us                                                   | 305 us: 1.05x faster                                                               |
| pickle_pure_python               | 139 us                                                   | 133 us: 1.05x faster                                                               |
| chaos                            | 28.9 ms                                                  | 27.6 ms: 1.05x faster                                                              |
| pycparser                        | 497 ms                                                   | 477 ms: 1.04x faster                                                               |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.00 ms: 1.04x faster                                                              |
| regex_dna                        | 99.6 ms                                                  | 96.4 ms: 1.03x faster                                                              |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                               |
| crypto_pyaes                     | 38.8 ms                                                  | 38.0 ms: 1.02x faster                                                              |
| nqueens                          | 43.5 ms                                                  | 42.8 ms: 1.02x faster                                                              |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                               |
| scimark_lu                       | 51.3 ms                                                  | 51.5 ms: 1.00x slower                                                              |
| json_loads                       | 10.9 us                                                  | 10.9 us: 1.01x slower                                                              |
| 2to3                             | 114 ms                                                   | 116 ms: 1.02x slower                                                               |
| nbody                            | 54.2 ms                                                  | 55.4 ms: 1.02x slower                                                              |
| bench_thread_pool                | 419 us                                                   | 430 us: 1.03x slower                                                               |
| fannkuch                         | 176 ms                                                   | 181 ms: 1.03x slower                                                               |
| dask                             | 528 ms                                                   | 546 ms: 1.04x slower                                                               |
| pidigits                         | 161 ms                                                   | 167 ms: 1.04x slower                                                               |
| gc_traversal                     | 2.01 ms                                                  | 2.09 ms: 1.04x slower                                                              |
| sympy_integrate                  | 8.02 ms                                                  | 8.43 ms: 1.05x slower                                                              |
| telco                            | 2.61 ms                                                  | 2.74 ms: 1.05x slower                                                              |
| sympy_sum                        | 57.6 ms                                                  | 60.8 ms: 1.06x slower                                                              |
| meteor_contest                   | 47.7 ms                                                  | 50.7 ms: 1.06x slower                                                              |
| hexiom                           | 3.04 ms                                                  | 3.22 ms: 1.06x slower                                                              |
| django_template                  | 13.6 ms                                                  | 14.7 ms: 1.08x slower                                                              |
| sympy_expand                     | 167 ms                                                   | 183 ms: 1.10x slower                                                               |
| genshi_xml                       | 21.8 ms                                                  | 24.0 ms: 1.10x slower                                                              |
| sympy_str                        | 104 ms                                                   | 115 ms: 1.10x slower                                                               |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 125 ms: 1.11x slower                                                               |
| create_gc_cycles                 | 830 us                                                   | 933 us: 1.12x slower                                                               |
| python_startup                   | 8.01 ms                                                  | 9.09 ms: 1.13x slower                                                              |
| python_startup_no_site           | 5.71 ms                                                  | 6.53 ms: 1.14x slower                                                              |
| bench_mp_pool                    | 39.7 ms                                                  | 45.6 ms: 1.15x slower                                                              |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 246 ms: 1.16x slower                                                               |
| coverage                         | 26.9 ms                                                  | 33.8 ms: 1.26x slower                                                              |
| many_optionals                   | 195 us                                                   | 374 us: 1.91x slower                                                               |
| async_tree_eager_tg              | 32.1 ms                                                  | 82.0 ms: 2.55x slower                                                              |
| Geometric mean                   | (ref)                                                    | 1.16x faster                                                                       |

Benchmark hidden because not significant (7): sqlite_synth, genshi_text, json, pylint, regex_v8, html5lib, logging_silent
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, connected_components, djangocms, docutils, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251124-3.15.0a2+-f96af45-JIT/bm-20251124-macm4pro-arm64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.162x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.25x