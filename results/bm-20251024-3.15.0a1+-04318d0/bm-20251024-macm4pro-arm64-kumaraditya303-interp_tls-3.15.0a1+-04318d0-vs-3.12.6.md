# Results vs. 3.12.6

- fork: kumaraditya303
- ref: interp_tls
- machine: darwin-arm64
- commit hash: 04318d0
- commit date: 2025-10-24
- overall geometric mean: 1.111x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 114 ms: 1.00x faster                                                   |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                 |
| sphinx         | 434 ms                                                   | 402 ms: 1.08x faster                                                   |
| Geometric mean | (ref)                                                    | 1.02x faster                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 228 ms: 2.17x faster                                                   |
| async_tree_io_tg                 | 480 ms                                                   | 228 ms: 2.11x faster                                                   |
| async_tree_io                    | 459 ms                                                   | 228 ms: 2.01x faster                                                   |
| async_tree_eager_io_tg           | 446 ms                                                   | 227 ms: 1.97x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 100.0 ms: 1.72x faster                                                 |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.65x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 142 ms: 1.57x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 252 ms: 1.32x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                   |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.6 ms: 1.07x faster                                                  |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 126 ms: 1.12x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 82.3 ms: 2.56x slower                                                  |
| Geometric mean                   | (ref)                                                    | 1.31x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.8 ms: 1.32x faster                                                  |
| nbody          | 54.2 ms                                                  | 49.6 ms: 1.09x faster                                                  |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                    | 1.13x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                  |
| regex_compile  | 54.6 ms                                                  | 49.2 ms: 1.11x faster                                                  |
| regex_dna      | 99.6 ms                                                  | 95.5 ms: 1.04x faster                                                  |
| regex_v8       | 9.59 ms                                                  | 9.76 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                    | 1.07x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.7 ms: 1.30x faster                                                  |
| xml_etree_generate   | 38.9 ms                                                  | 35.0 ms: 1.11x faster                                                  |
| xml_etree_parse      | 67.9 ms                                                  | 62.5 ms: 1.09x faster                                                  |
| json_dumps           | 4.26 ms                                                  | 3.96 ms: 1.08x faster                                                  |
| xml_etree_process    | 26.7 ms                                                  | 25.0 ms: 1.07x faster                                                  |
| tomli_loads          | 957 ms                                                   | 899 ms: 1.06x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 101 us: 1.01x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.9 us: 1.01x slower                                                  |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.05x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.25 ms: 1.10x slower                                                  |
| python_startup         | 8.01 ms                                                  | 8.81 ms: 1.10x slower                                                  |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|-----------------|:--------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.90 ms: 1.06x faster                                                  |
| mako            | 4.77 ms                                                  | 4.79 ms: 1.00x slower                                                  |
| genshi_xml      | 21.8 ms                                                  | 22.0 ms: 1.01x slower                                                  |
| django_template | 13.6 ms                                                  | 15.6 ms: 1.14x slower                                                  |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                           |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0 |
|----------------------------------|:--------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 228 ms: 2.17x faster                                                   |
| async_tree_io_tg                 | 480 ms                                                   | 228 ms: 2.11x faster                                                   |
| mdp                              | 1.09 sec                                                 | 540 ms: 2.02x faster                                                   |
| async_tree_io                    | 459 ms                                                   | 228 ms: 2.01x faster                                                   |
| async_tree_eager_io_tg           | 446 ms                                                   | 227 ms: 1.97x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 100.0 ms: 1.72x faster                                                 |
| async_tree_memoization_tg        | 231 ms                                                   | 140 ms: 1.65x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 142 ms: 1.57x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 12.0 us: 1.52x faster                                                  |
| deepcopy                         | 161 us                                                   | 110 us: 1.46x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.44 us: 1.32x faster                                                  |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 252 ms: 1.32x faster                                                   |
| float                            | 37.9 ms                                                  | 28.8 ms: 1.32x faster                                                  |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.7 ms: 1.30x faster                                                  |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.27x faster                                                  |
| spectral_norm                    | 54.4 ms                                                  | 43.7 ms: 1.24x faster                                                  |
| k_core                           | 1.12 sec                                                 | 900 ms: 1.24x faster                                                   |
| go                               | 70.0 ms                                                  | 56.5 ms: 1.24x faster                                                  |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 49.6 ms: 1.23x faster                                                  |
| generators                       | 21.9 ms                                                  | 18.0 ms: 1.22x faster                                                  |
| logging_silent                   | 50.9 ns                                                  | 42.0 ns: 1.21x faster                                                  |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                   |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                  |
| subparsers                       | 20.8 ms                                                  | 18.0 ms: 1.15x faster                                                  |
| deltablue                        | 1.73 ms                                                  | 1.50 ms: 1.15x faster                                                  |
| scimark_fft                      | 142 ms                                                   | 125 ms: 1.14x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                  |
| pyflate                          | 216 ms                                                   | 193 ms: 1.12x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                 |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.86 ms: 1.11x faster                                                  |
| regex_compile                    | 54.6 ms                                                  | 49.2 ms: 1.11x faster                                                  |
| xml_etree_generate               | 38.9 ms                                                  | 35.0 ms: 1.11x faster                                                  |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.2 ms: 1.10x faster                                                  |
| dulwich_log                      | 21.3 ms                                                  | 19.3 ms: 1.10x faster                                                  |
| chaos                            | 28.9 ms                                                  | 26.3 ms: 1.10x faster                                                  |
| nbody                            | 54.2 ms                                                  | 49.6 ms: 1.09x faster                                                  |
| logging_simple                   | 2.57 us                                                  | 2.35 us: 1.09x faster                                                  |
| nqueens                          | 43.5 ms                                                  | 39.8 ms: 1.09x faster                                                  |
| pylint                           | 128 ms                                                   | 117 ms: 1.09x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 62.5 ms: 1.09x faster                                                  |
| logging_format                   | 2.80 us                                                  | 2.58 us: 1.08x faster                                                  |
| sphinx                           | 434 ms                                                   | 402 ms: 1.08x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.82 ms: 1.08x faster                                                  |
| scimark_lu                       | 51.3 ms                                                  | 47.6 ms: 1.08x faster                                                  |
| typing_runtime_protocols         | 71.0 us                                                  | 65.9 us: 1.08x faster                                                  |
| json_dumps                       | 4.26 ms                                                  | 3.96 ms: 1.08x faster                                                  |
| async_tree_eager                 | 45.6 ms                                                  | 42.6 ms: 1.07x faster                                                  |
| xml_etree_process                | 26.7 ms                                                  | 25.0 ms: 1.07x faster                                                  |
| sympy_integrate                  | 8.02 ms                                                  | 7.53 ms: 1.07x faster                                                  |
| tomli_loads                      | 957 ms                                                   | 899 ms: 1.06x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.90 ms: 1.06x faster                                                  |
| richards                         | 22.4 ms                                                  | 21.4 ms: 1.05x faster                                                  |
| richards_super                   | 25.4 ms                                                  | 24.2 ms: 1.05x faster                                                  |
| regex_dna                        | 99.6 ms                                                  | 95.5 ms: 1.04x faster                                                  |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.6 ms: 1.03x faster                                                  |
| pycparser                        | 497 ms                                                   | 484 ms: 1.03x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                   |
| thrift                           | 322 us                                                   | 315 us: 1.02x faster                                                   |
| sympy_str                        | 104 ms                                                   | 102 ms: 1.02x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 101 us: 1.01x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 57.0 ms: 1.01x faster                                                  |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                   |
| bench_thread_pool                | 419 us                                                   | 415 us: 1.01x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 326 ms: 1.01x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 661 ms: 1.00x faster                                                   |
| 2to3                             | 114 ms                                                   | 114 ms: 1.00x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.79 ms: 1.00x slower                                                  |
| genshi_xml                       | 21.8 ms                                                  | 22.0 ms: 1.01x slower                                                  |
| json_loads                       | 10.9 us                                                  | 10.9 us: 1.01x slower                                                  |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                   |
| sqlite_synth                     | 967 ns                                                   | 978 ns: 1.01x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.01x slower                                                 |
| regex_v8                         | 9.59 ms                                                  | 9.76 ms: 1.02x slower                                                  |
| shortest_path                    | 219 ms                                                   | 223 ms: 1.02x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.06 ms: 1.03x slower                                                  |
| connected_components             | 201 ms                                                   | 207 ms: 1.03x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 49.7 ms: 1.04x slower                                                  |
| sympy_expand                     | 167 ms                                                   | 174 ms: 1.04x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 41.4 ms: 1.04x slower                                                  |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.05x slower                                                   |
| fannkuch                         | 176 ms                                                   | 185 ms: 1.05x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.25 ms: 1.10x slower                                                  |
| python_startup                   | 8.01 ms                                                  | 8.81 ms: 1.10x slower                                                  |
| create_gc_cycles                 | 830 us                                                   | 915 us: 1.10x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.91 ms: 1.11x slower                                                  |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 126 ms: 1.12x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 240 ms: 1.13x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.6 ms: 1.14x slower                                                  |
| coverage                         | 26.9 ms                                                  | 32.3 ms: 1.20x slower                                                  |
| many_optionals                   | 195 us                                                   | 368 us: 1.88x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 82.3 ms: 2.56x slower                                                  |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                           |

Benchmark hidden because not significant (2): html5lib, json
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20251024-3.15.0a1+-04318d0/bm-20251024-macm4pro-arm64-kumaraditya303-interp_tls-3.15.0a1+-04318d0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.111x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.20x