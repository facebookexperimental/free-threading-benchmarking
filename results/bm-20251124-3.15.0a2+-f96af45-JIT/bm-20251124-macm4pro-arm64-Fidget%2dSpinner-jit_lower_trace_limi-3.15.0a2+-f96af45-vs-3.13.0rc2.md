# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: jit_lower_trace_limi
- machine: darwin-arm64
- commit hash: f96af45
- commit date: 2025-11-24
- overall geometric mean: 1.070x faster
- HPT reliability: 94.85%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-macm4pro-arm64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 116 ms: 1.04x slower                                                               |
| sphinx         | 409 ms                                                         | 8.71 ms: 46.91x faster                                                             |
| Geometric mean | (ref)                                                          | 3.56x faster                                                                       |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-macm4pro-arm64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 224 ms: 2.34x faster                                                               |
| async_tree_eager_io_tg           | 521 ms                                                         | 225 ms: 2.31x faster                                                               |
| async_tree_io_tg                 | 405 ms                                                         | 229 ms: 1.77x faster                                                               |
| async_tree_io                    | 386 ms                                                         | 232 ms: 1.67x faster                                                               |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.40x faster                                                               |
| async_tree_none_tg               | 133 ms                                                         | 97.3 ms: 1.36x faster                                                              |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.35x faster                                                               |
| async_tree_memoization_tg        | 186 ms                                                         | 139 ms: 1.33x faster                                                               |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                               |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 251 ms: 1.17x faster                                                               |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                               |
| coroutines                       | 10.8 ms                                                        | 9.92 ms: 1.08x faster                                                              |
| async_generators                 | 193 ms                                                         | 185 ms: 1.05x faster                                                               |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                               |
| async_tree_eager                 | 43.2 ms                                                        | 42.3 ms: 1.02x faster                                                              |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                               |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 125 ms: 1.22x slower                                                               |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.0 ms: 2.83x slower                                                              |
| Geometric mean                   | (ref)                                                          | 1.18x faster                                                                       |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-macm4pro-arm64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.6 ms: 1.06x faster                                                              |
| pidigits       | 166 ms                                                         | 167 ms: 1.01x slower                                                               |
| nbody          | 42.5 ms                                                        | 55.4 ms: 1.30x slower                                                              |
| Geometric mean | (ref)                                                          | 1.07x slower                                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-macm4pro-arm64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                              |
| regex_v8       | 10.7 ms                                                        | 9.61 ms: 1.11x faster                                                              |
| regex_compile  | 47.9 ms                                                        | 45.2 ms: 1.06x faster                                                              |
| regex_dna      | 94.6 ms                                                        | 96.4 ms: 1.02x slower                                                              |
| Geometric mean | (ref)                                                          | 1.07x faster                                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-macm4pro-arm64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 822 ms: 1.22x faster                                                               |
| json_dumps           | 4.65 ms                                                        | 3.83 ms: 1.22x faster                                                              |
| xml_etree_iterparse  | 46.1 ms                                                        | 39.7 ms: 1.16x faster                                                              |
| xml_etree_process    | 25.4 ms                                                        | 23.6 ms: 1.07x faster                                                              |
| xml_etree_generate   | 35.8 ms                                                        | 34.1 ms: 1.05x faster                                                              |
| unpickle_pure_python | 99.5 us                                                        | 95.0 us: 1.05x faster                                                              |
| xml_etree_parse      | 62.4 ms                                                        | 61.2 ms: 1.02x faster                                                              |
| json_loads           | 10.8 us                                                        | 10.9 us: 1.01x slower                                                              |
| pickle_pure_python   | 130 us                                                         | 133 us: 1.02x slower                                                               |
| Geometric mean       | (ref)                                                          | 1.08x faster                                                                       |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-macm4pro-arm64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.09 ms: 1.05x slower                                                              |
| python_startup_no_site | 5.95 ms                                                        | 6.53 ms: 1.10x slower                                                              |
| Geometric mean         | (ref)                                                          | 1.07x slower                                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-macm4pro-arm64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|-----------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 10.5 ms: 1.05x slower                                                              |
| genshi_xml      | 21.4 ms                                                        | 24.0 ms: 1.12x slower                                                              |
| django_template | 12.5 ms                                                        | 14.7 ms: 1.17x slower                                                              |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                                       |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251124-macm4pro-arm64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45 |
|----------------------------------|:--------------------------------------------------------------:|:----------------------------------------------------------------------------------:|
| sphinx                           | 409 ms                                                         | 8.71 ms: 46.91x faster                                                             |
| async_tree_eager_io              | 525 ms                                                         | 224 ms: 2.34x faster                                                               |
| async_tree_eager_io_tg           | 521 ms                                                         | 225 ms: 2.31x faster                                                               |
| async_tree_io_tg                 | 405 ms                                                         | 229 ms: 1.77x faster                                                               |
| mdp                              | 1.06 sec                                                       | 621 ms: 1.70x faster                                                               |
| async_tree_io                    | 386 ms                                                         | 232 ms: 1.67x faster                                                               |
| deepcopy_memo                    | 16.5 us                                                        | 11.0 us: 1.50x faster                                                              |
| deepcopy                         | 145 us                                                         | 100 us: 1.44x faster                                                               |
| richards_super                   | 24.7 ms                                                        | 17.3 ms: 1.43x faster                                                              |
| richards                         | 22.1 ms                                                        | 15.5 ms: 1.42x faster                                                              |
| async_tree_none                  | 142 ms                                                         | 101 ms: 1.40x faster                                                               |
| async_tree_none_tg               | 133 ms                                                         | 97.3 ms: 1.36x faster                                                              |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.35x faster                                                               |
| async_tree_memoization_tg        | 186 ms                                                         | 139 ms: 1.33x faster                                                               |
| deepcopy_reduce                  | 1.30 us                                                        | 1.03 us: 1.26x faster                                                              |
| go                               | 72.6 ms                                                        | 58.2 ms: 1.25x faster                                                              |
| tomli_loads                      | 1000 ms                                                        | 822 ms: 1.22x faster                                                               |
| json_dumps                       | 4.65 ms                                                        | 3.83 ms: 1.22x faster                                                              |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                               |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 251 ms: 1.17x faster                                                               |
| pyflate                          | 222 ms                                                         | 190 ms: 1.17x faster                                                               |
| xml_etree_iterparse              | 46.1 ms                                                        | 39.7 ms: 1.16x faster                                                              |
| scimark_sor                      | 64.0 ms                                                        | 56.3 ms: 1.14x faster                                                              |
| async_tree_eager_memoization     | 122 ms                                                         | 108 ms: 1.13x faster                                                               |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                              |
| telco                            | 3.07 ms                                                        | 2.74 ms: 1.12x faster                                                              |
| regex_v8                         | 10.7 ms                                                        | 9.61 ms: 1.11x faster                                                              |
| pprint_safe_repr                 | 322 ms                                                         | 294 ms: 1.09x faster                                                               |
| pprint_pformat                   | 650 ms                                                         | 595 ms: 1.09x faster                                                               |
| coroutines                       | 10.8 ms                                                        | 9.92 ms: 1.08x faster                                                              |
| xml_etree_process                | 25.4 ms                                                        | 23.6 ms: 1.07x faster                                                              |
| create_gc_cycles                 | 993 us                                                         | 933 us: 1.07x faster                                                               |
| float                            | 31.4 ms                                                        | 29.6 ms: 1.06x faster                                                              |
| scimark_monte_carlo              | 29.9 ms                                                        | 28.1 ms: 1.06x faster                                                              |
| regex_compile                    | 47.9 ms                                                        | 45.2 ms: 1.06x faster                                                              |
| xml_etree_generate               | 35.8 ms                                                        | 34.1 ms: 1.05x faster                                                              |
| unpickle_pure_python             | 99.5 us                                                        | 95.0 us: 1.05x faster                                                              |
| async_generators                 | 193 ms                                                         | 185 ms: 1.05x faster                                                               |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.05 sec: 1.04x faster                                                             |
| scimark_fft                      | 124 ms                                                         | 120 ms: 1.03x faster                                                               |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                               |
| async_tree_eager                 | 43.2 ms                                                        | 42.3 ms: 1.02x faster                                                              |
| xml_etree_parse                  | 62.4 ms                                                        | 61.2 ms: 1.02x faster                                                              |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                              |
| thrift                           | 309 us                                                         | 305 us: 1.01x faster                                                               |
| logging_simple                   | 2.24 us                                                        | 2.21 us: 1.01x faster                                                              |
| pidigits                         | 166 ms                                                         | 167 ms: 1.01x slower                                                               |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                              |
| fannkuch                         | 179 ms                                                         | 181 ms: 1.01x slower                                                               |
| pycparser                        | 470 ms                                                         | 477 ms: 1.01x slower                                                               |
| sqlite_synth                     | 948 ns                                                         | 963 ns: 1.02x slower                                                               |
| regex_dna                        | 94.6 ms                                                        | 96.4 ms: 1.02x slower                                                              |
| pickle_pure_python               | 130 us                                                         | 133 us: 1.02x slower                                                               |
| gc_traversal                     | 2.04 ms                                                        | 2.09 ms: 1.02x slower                                                              |
| dask                             | 525 ms                                                         | 546 ms: 1.04x slower                                                               |
| 2to3                             | 112 ms                                                         | 116 ms: 1.04x slower                                                               |
| bench_thread_pool                | 412 us                                                         | 430 us: 1.04x slower                                                               |
| genshi_text                      | 9.97 ms                                                        | 10.5 ms: 1.05x slower                                                              |
| python_startup                   | 8.63 ms                                                        | 9.09 ms: 1.05x slower                                                              |
| meteor_contest                   | 47.9 ms                                                        | 50.7 ms: 1.06x slower                                                              |
| deltablue                        | 1.45 ms                                                        | 1.55 ms: 1.07x slower                                                              |
| comprehensions                   | 6.80 us                                                        | 7.36 us: 1.08x slower                                                              |
| coverage                         | 31.2 ms                                                        | 33.8 ms: 1.08x slower                                                              |
| python_startup_no_site           | 5.95 ms                                                        | 6.53 ms: 1.10x slower                                                              |
| spectral_norm                    | 43.7 ms                                                        | 48.7 ms: 1.11x slower                                                              |
| sympy_integrate                  | 7.53 ms                                                        | 8.43 ms: 1.12x slower                                                              |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.00 ms: 1.12x slower                                                              |
| genshi_xml                       | 21.4 ms                                                        | 24.0 ms: 1.12x slower                                                              |
| crypto_pyaes                     | 33.6 ms                                                        | 38.0 ms: 1.13x slower                                                              |
| hexiom                           | 2.85 ms                                                        | 3.22 ms: 1.13x slower                                                              |
| chaos                            | 24.3 ms                                                        | 27.6 ms: 1.14x slower                                                              |
| nqueens                          | 37.2 ms                                                        | 42.8 ms: 1.15x slower                                                              |
| sympy_expand                     | 159 ms                                                         | 183 ms: 1.15x slower                                                               |
| sympy_sum                        | 52.3 ms                                                        | 60.8 ms: 1.16x slower                                                              |
| django_template                  | 12.5 ms                                                        | 14.7 ms: 1.17x slower                                                              |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 246 ms: 1.18x slower                                                               |
| scimark_lu                       | 42.8 ms                                                        | 51.5 ms: 1.20x slower                                                              |
| sympy_str                        | 95.5 ms                                                        | 115 ms: 1.21x slower                                                               |
| bench_mp_pool                    | 37.8 ms                                                        | 45.6 ms: 1.21x slower                                                              |
| raytrace                         | 109 ms                                                         | 132 ms: 1.21x slower                                                               |
| pylint                           | 106 ms                                                         | 128 ms: 1.21x slower                                                               |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 125 ms: 1.22x slower                                                               |
| generators                       | 15.7 ms                                                        | 19.4 ms: 1.23x slower                                                              |
| logging_silent                   | 40.6 ns                                                        | 51.4 ns: 1.27x slower                                                              |
| nbody                            | 42.5 ms                                                        | 55.4 ms: 1.30x slower                                                              |
| many_optionals                   | 200 us                                                         | 374 us: 1.86x slower                                                               |
| async_tree_eager_tg              | 28.9 ms                                                        | 82.0 ms: 2.83x slower                                                              |
| subparsers                       | 6.26 ms                                                        | 18.3 ms: 2.93x slower                                                              |
| Geometric mean                   | (ref)                                                          | 1.06x faster                                                                       |

Benchmark hidden because not significant (7): json, mako, logging_format, html5lib, dulwich_log, async_tree_eager_cpu_io_mixed, typing_runtime_protocols
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, connected_components, djangocms, docutils, gevent_hub, k_core, shortest_path, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251124-3.15.0a2+-f96af45-JIT/bm-20251124-macm4pro-arm64-Fidget%2dSpinner-jit_lower_trace_limi-3.15.0a2+-f96af45.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.070x faster

# HPT report

- Reliability score: 94.85% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.20x