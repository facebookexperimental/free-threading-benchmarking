# Results vs. 3.12.6

- fork: python
- ref: 406dc714f6b4dbc18d4e
- machine: darwin-arm64
- commit hash: 406dc71
- commit date: 2025-08-03
- overall geometric mean: 1.087x faster
- HPT reliability: 97.08%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 124 ms: 1.09x slower                                                    |
| docutils       | 1.02 sec                                                 | 999 ms: 1.02x faster                                                    |
| html5lib       | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                   |
| sphinx         | 434 ms                                                   | 409 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.43x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 196 ms: 2.28x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.1 ms: 2.00x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 100.0 ms: 1.78x faster                                                  |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.72x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 244 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.26x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.3 ms: 1.06x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.9 ms: 2.43x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.0 ms: 1.35x faster                                                   |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                    |
| nbody          | 54.2 ms                                                  | 58.9 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.16 ms: 1.05x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 52.3 ms: 1.04x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 96.4 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.7 ms: 1.33x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 59.9 ms: 1.13x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.4 ms: 1.07x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.5 ms: 1.01x faster                                                   |
| tomli_loads          | 957 ms                                                   | 972 ms: 1.01x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.05x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 109 us: 1.06x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.55 ms: 1.07x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 149 us: 1.07x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.59 ms: 1.20x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.98 ms: 1.22x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.5 ms: 1.09x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 23.8 ms: 1.09x slower                                                   |
| mako            | 4.77 ms                                                  | 5.62 ms: 1.18x slower                                                   |
| django_template | 13.6 ms                                                  | 16.4 ms: 1.21x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.14x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 778 us: 2.58x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 198 ms: 2.43x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 205 ms: 2.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 196 ms: 2.28x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 86.1 ms: 2.00x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| mdp                              | 1.09 sec                                                 | 606 ms: 1.80x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 100.0 ms: 1.78x faster                                                  |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.72x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 494 us: 1.68x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 237 ms: 1.43x faster                                                    |
| deepcopy                         | 161 us                                                   | 117 us: 1.38x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 244 ms: 1.37x faster                                                    |
| float                            | 37.9 ms                                                  | 28.0 ms: 1.35x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.7 ms: 1.33x faster                                                   |
| deepcopy_memo                    | 18.3 us                                                  | 13.8 us: 1.33x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.26x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.18 us: 1.20x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 819 ns: 1.18x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.26 us: 1.16x faster                                                   |
| go                               | 70.0 ms                                                  | 60.3 ms: 1.16x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 44.4 ns: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.3 ms: 1.14x faster                                                   |
| k_core                           | 1.12 sec                                                 | 985 ms: 1.14x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 59.9 ms: 1.13x faster                                                   |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.98 sec: 1.13x faster                                                  |
| subparsers                       | 20.8 ms                                                  | 18.4 ms: 1.13x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.12x faster                                                   |
| raytrace                         | 145 ms                                                   | 131 ms: 1.11x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.8 ms: 1.09x faster                                                   |
| pyflate                          | 216 ms                                                   | 198 ms: 1.09x faster                                                    |
| pylint                           | 128 ms                                                   | 118 ms: 1.09x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.4 ms: 1.07x faster                                                   |
| pycparser                        | 497 ms                                                   | 467 ms: 1.07x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.62 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 409 ms: 1.06x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.5 ms: 1.06x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.16 ms: 1.05x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 52.3 ms: 1.04x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 96.4 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| docutils                         | 1.02 sec                                                 | 999 ms: 1.02x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.52 us: 1.02x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 42.9 ms: 1.01x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 26.5 ms: 1.01x faster                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 143 ms: 1.01x slower                                                    |
| dask                             | 528 ms                                                   | 531 ms: 1.01x slower                                                    |
| chaos                            | 28.9 ms                                                  | 29.2 ms: 1.01x slower                                                   |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                    |
| json                             | 1.93 ms                                                  | 1.95 ms: 1.01x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 972 ms: 1.01x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.11 ms: 1.02x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                   |
| fannkuch                         | 176 ms                                                   | 180 ms: 1.03x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 73.1 us: 1.03x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.5 ms: 1.04x slower                                                   |
| thrift                           | 322 us                                                   | 336 us: 1.04x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.4 ms: 1.04x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.05x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 109 us: 1.06x slower                                                    |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.06x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.3 ms: 1.06x slower                                                   |
| shortest_path                    | 219 ms                                                   | 232 ms: 1.06x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 348 ms: 1.06x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 61.3 ms: 1.07x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 27.1 ms: 1.07x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 710 ms: 1.07x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.55 ms: 1.07x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 149 us: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 228 ms: 1.07x slower                                                    |
| nbody                            | 54.2 ms                                                  | 58.9 ms: 1.09x slower                                                   |
| 2to3                             | 114 ms                                                   | 124 ms: 1.09x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.5 ms: 1.09x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 23.8 ms: 1.09x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.27 ms: 1.10x slower                                                   |
| connected_components             | 201 ms                                                   | 220 ms: 1.10x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.7 ms: 1.10x slower                                                   |
| scimark_lu                       | 51.3 ms                                                  | 57.5 ms: 1.12x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 45.4 ms: 1.14x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 55.8 ms: 1.17x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.62 ms: 1.18x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.59 ms: 1.20x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.4 ms: 1.21x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.19 ms: 1.22x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.98 ms: 1.22x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 599 us: 1.43x slower                                                    |
| coverage                         | 26.9 ms                                                  | 39.4 ms: 1.47x slower                                                   |
| many_optionals                   | 195 us                                                   | 334 us: 1.71x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.9 ms: 2.43x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (2): sympy_integrate, logging_format
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250803-3.15.0a0-406dc71-NOGIL/bm-20250803-macm4pro-arm64-python-406dc714f6b4dbc18d4e-3.15.0a0-406dc71.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.087x faster

# HPT report

- Reliability score: 97.08% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.25x