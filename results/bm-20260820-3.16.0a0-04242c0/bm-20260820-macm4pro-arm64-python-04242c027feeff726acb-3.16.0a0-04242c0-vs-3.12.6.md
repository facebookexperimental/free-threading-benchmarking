# Results vs. 3.12.6

- fork: python
- ref: 04242c027feeff726acb
- machine: darwin-arm64
- commit hash: 04242c0
- commit date: 2026-08-20
- overall geometric mean: 1.132x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 121 ms: 1.06x slower                                                    |
| docutils       | 1.02 sec                                                 | 964 ms: 1.06x faster                                                    |
| html5lib       | 23.0 ms                                                  | 21.5 ms: 1.07x faster                                                   |
| sphinx         | 434 ms                                                   | 408 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 318 ms: 1.56x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 321 ms: 1.43x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 336 ms: 1.43x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 125 ms: 1.42x faster                                                    |
| async_generators                 | 206 ms                                                   | 146 ms: 1.42x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 129 ms: 1.34x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 176 ms: 1.31x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 343 ms: 1.30x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 181 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 289 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 297 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 118 ms: 1.11x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.2 ms: 1.08x faster                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 269 ms: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 157 ms: 1.39x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 106 ms: 3.30x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (2): async_tree_eager_cpu_io_mixed, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.2 ms: 1.30x faster                                                   |
| nbody          | 54.2 ms                                                  | 42.4 ms: 1.28x faster                                                   |
| pidigits       | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.17x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.40 ms: 1.19x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 92.4 ms: 1.08x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.15 ms: 1.05x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 54.8 ms: 1.00x slower                                                   |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.26 ms                                                  | 3.55 ms: 1.20x faster                                                   |
| tomli_loads          | 957 ms                                                   | 804 ms: 1.19x faster                                                    |
| xml_etree_iterparse  | 51.6 ms                                                  | 43.6 ms: 1.18x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 99.3 us: 1.04x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.9 ms: 1.03x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.9 us: 1.01x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 141 us: 1.01x slower                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 69.0 ms: 1.02x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.33 ms: 1.11x slower                                                   |
| python_startup         | 8.01 ms                                                  | 9.10 ms: 1.14x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.12x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.67 ms: 1.02x faster                                                   |
| django_template | 13.6 ms                                                  | 15.0 ms: 1.10x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.04x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.15 ms: 5.01x faster                                                   |
| pylint                           | 128 ms                                                   | 57.2 ms: 2.24x faster                                                   |
| mdp                              | 1.09 sec                                                 | 525 ms: 2.08x faster                                                    |
| deepcopy                         | 161 us                                                   | 98.6 us: 1.64x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 318 ms: 1.56x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.8 us: 1.56x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 6.79 us: 1.45x faster                                                   |
| async_tree_io                    | 459 ms                                                   | 321 ms: 1.43x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 49.7 us: 1.43x faster                                                   |
| async_tree_io_tg                 | 480 ms                                                   | 336 ms: 1.43x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 125 ms: 1.42x faster                                                    |
| async_generators                 | 206 ms                                                   | 146 ms: 1.42x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.08 us: 1.36x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.35x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 129 ms: 1.34x faster                                                    |
| go                               | 70.0 ms                                                  | 52.9 ms: 1.32x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 176 ms: 1.31x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 343 ms: 1.30x faster                                                    |
| float                            | 37.9 ms                                                  | 29.2 ms: 1.30x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 42.1 ms: 1.29x faster                                                   |
| nbody                            | 54.2 ms                                                  | 42.4 ms: 1.28x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 49.2 ms: 1.24x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 181 ms: 1.23x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 35.4 ms: 1.23x faster                                                   |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 116 ms: 1.22x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 42.1 ns: 1.21x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.55 ms: 1.20x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.40 ms: 1.19x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 804 ms: 1.19x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.6 ms: 1.18x faster                                                   |
| pyflate                          | 216 ms                                                   | 186 ms: 1.16x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.22 us: 1.16x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.16x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 289 ms: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.15x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.0 ms: 1.15x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.43 us: 1.15x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.80 ms: 1.15x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.51 ms: 1.15x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.1 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                  |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 297 ms: 1.14x faster                                                    |
| k_core                           | 1.12 sec                                                 | 991 ms: 1.13x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.7 ms: 1.13x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.71 ms: 1.12x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 118 ms: 1.11x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.3 ms: 1.10x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 23.2 ms: 1.10x faster                                                   |
| fannkuch                         | 176 ms                                                   | 160 ms: 1.09x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.2 ms: 1.08x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 92.4 ms: 1.08x faster                                                   |
| html5lib                         | 23.0 ms                                                  | 21.5 ms: 1.07x faster                                                   |
| sphinx                           | 434 ms                                                   | 408 ms: 1.06x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.56 ms: 1.06x faster                                                   |
| docutils                         | 1.02 sec                                                 | 964 ms: 1.06x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 312 ms: 1.05x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.15 ms: 1.05x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 923 ns: 1.05x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 639 ms: 1.04x faster                                                    |
| sympy_str                        | 104 ms                                                   | 100 ms: 1.04x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.5 ms: 1.04x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 99.3 us: 1.04x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.9 ms: 1.03x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 56.0 ms: 1.03x faster                                                   |
| thrift                           | 322 us                                                   | 314 us: 1.03x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 1.96 ms: 1.02x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.67 ms: 1.02x faster                                                   |
| pycparser                        | 497 ms                                                   | 493 ms: 1.01x faster                                                    |
| json                             | 1.93 ms                                                  | 1.92 ms: 1.01x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 54.8 ms: 1.00x slower                                                   |
| json_loads                       | 10.9 us                                                  | 10.9 us: 1.01x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 423 us: 1.01x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 141 us: 1.01x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 842 us: 1.02x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 52.1 ms: 1.02x slower                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 69.0 ms: 1.02x slower                                                   |
| shortest_path                    | 219 ms                                                   | 223 ms: 1.02x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 170 ms: 1.02x slower                                                    |
| connected_components             | 201 ms                                                   | 207 ms: 1.03x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.6 ms: 1.04x slower                                                   |
| pidigits                         | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| 2to3                             | 114 ms                                                   | 121 ms: 1.06x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.87 ms: 1.10x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.0 ms: 1.10x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.33 ms: 1.11x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.10 ms: 1.14x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.5 ms: 1.14x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 269 ms: 1.26x slower                                                    |
| many_optionals                   | 195 us                                                   | 247 us: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 157 ms: 1.39x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 106 ms: 3.30x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                            |

Benchmark hidden because not significant (2): async_tree_eager_cpu_io_mixed, asyncio_websockets
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260820-3.16.0a0-04242c0/bm-20260820-macm4pro-arm64-python-04242c027feeff726acb-3.16.0a0-04242c0.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.132x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.19x