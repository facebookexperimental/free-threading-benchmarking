# Results vs. 3.12.6

- fork: python
- ref: 246be21de1e2a51d757c
- machine: darwin-arm64
- commit hash: 246be21
- commit date: 2025-07-20
- overall geometric mean: 1.085x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 117 ms: 1.02x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.4 ms: 1.06x slower                                                   |
| sphinx         | 434 ms                                                   | 412 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 255 ms: 1.95x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 253 ms: 1.90x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 259 ms: 1.77x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 257 ms: 1.73x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 109 ms: 1.58x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 149 ms: 1.55x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 267 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 270 ms: 1.24x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.8 ms: 1.06x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 227 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.02x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 253 ms: 1.19x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.0 ms: 2.77x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.23x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 32.0 ms: 1.18x faster                                                   |
| nbody          | 54.2 ms                                                  | 48.7 ms: 1.11x faster                                                   |
| pidigits       | 161 ms                                                   | 169 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 49.2 ms: 1.11x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 99.1 ms: 1.01x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.70 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 45.5 ms: 1.13x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.0 ms: 1.08x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.3 ms: 1.06x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 65.6 ms: 1.04x faster                                                   |
| tomli_loads          | 957 ms                                                   | 926 ms: 1.03x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 101 us: 1.02x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.0 us: 1.01x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 4.46 ms: 1.05x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 149 us: 1.07x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.73 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.23 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.1 ms: 1.04x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 22.0 ms: 1.01x slower                                                   |
| mako            | 4.77 ms                                                  | 5.00 ms: 1.05x slower                                                   |
| django_template | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.04x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 516 ms: 2.12x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 255 ms: 1.95x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 253 ms: 1.90x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 259 ms: 1.77x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 257 ms: 1.73x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 109 ms: 1.58x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 149 ms: 1.55x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.50x faster                                                    |
| deepcopy                         | 161 us                                                   | 113 us: 1.43x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.0 us: 1.41x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.48 us: 1.32x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.30x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 267 ms: 1.27x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.18 us: 1.24x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 270 ms: 1.24x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 44.1 ms: 1.23x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 41.4 ns: 1.23x faster                                                   |
| generators                       | 21.9 ms                                                  | 18.0 ms: 1.22x faster                                                   |
| raytrace                         | 145 ms                                                   | 120 ms: 1.21x faster                                                    |
| go                               | 70.0 ms                                                  | 58.0 ms: 1.21x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 50.7 ms: 1.20x faster                                                   |
| float                            | 37.9 ms                                                  | 32.0 ms: 1.18x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 17.6 ms: 1.18x faster                                                   |
| k_core                           | 1.12 sec                                                 | 948 ms: 1.18x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.2 ms: 1.17x faster                                                   |
| async_generators                 | 206 ms                                                   | 178 ms: 1.16x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 38.1 ms: 1.14x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 45.5 ms: 1.13x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.13x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                  |
| typing_runtime_protocols         | 71.0 us                                                  | 62.7 us: 1.13x faster                                                   |
| pylint                           | 128 ms                                                   | 114 ms: 1.12x faster                                                    |
| nbody                            | 54.2 ms                                                  | 48.7 ms: 1.11x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.55 ms: 1.11x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 49.2 ms: 1.11x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.87 ms: 1.11x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.11x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.0 ms: 1.08x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.8 ms: 1.08x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.81 ms: 1.08x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.60 us: 1.08x faster                                                   |
| pyflate                          | 216 ms                                                   | 201 ms: 1.08x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.0 ms: 1.07x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.41 us: 1.07x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.53 ms: 1.06x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.8 ms: 1.06x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.3 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 412 ms: 1.05x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 48.7 ms: 1.05x faster                                                   |
| thrift                           | 322 us                                                   | 307 us: 1.05x faster                                                    |
| sympy_str                        | 104 ms                                                   | 99.7 ms: 1.05x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 10.1 ms: 1.04x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 65.6 ms: 1.04x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 926 ms: 1.03x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.8 ms: 1.03x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 138 ms: 1.03x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 101 us: 1.02x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 24.9 ms: 1.02x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 56.4 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 227 ms: 1.02x faster                                                    |
| richards                         | 22.4 ms                                                  | 22.0 ms: 1.02x faster                                                   |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 218 ms: 1.01x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 99.1 ms: 1.01x faster                                                   |
| connected_components             | 201 ms                                                   | 200 ms: 1.00x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.01x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.0 ms: 1.01x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.70 ms: 1.01x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.0 us: 1.01x slower                                                   |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.02x slower                                                    |
| pycparser                        | 497 ms                                                   | 505 ms: 1.02x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.6 ms: 1.02x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 334 ms: 1.02x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 679 ms: 1.02x slower                                                    |
| 2to3                             | 114 ms                                                   | 117 ms: 1.02x slower                                                    |
| fannkuch                         | 176 ms                                                   | 182 ms: 1.04x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 435 us: 1.04x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| pidigits                         | 161 ms                                                   | 169 ms: 1.05x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.00 ms: 1.05x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.46 ms: 1.05x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.13 ms: 1.06x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.4 ms: 1.06x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 149 us: 1.07x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.73 ms: 1.09x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.23 ms: 1.09x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.0 ms: 1.13x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.05 ms: 1.17x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.17x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 974 us: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 253 ms: 1.19x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.9 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 327 us: 1.68x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.0 ms: 2.77x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (2): json, sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250720-3.15.0a0-246be21/bm-20250720-macm4pro-arm64-python-246be21de1e2a51d757c-3.15.0a0-246be21.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.085x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.15x