# Results vs. 3.12.6

- fork: python
- ref: b13a5df52fc854d1097e
- machine: darwin-arm64
- commit hash: b13a5df
- commit date: 2025-07-22
- overall geometric mean: 1.088x faster
- HPT reliability: 97.20%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| docutils       | 1.02 sec                                                 | 998 ms: 1.02x faster                                                    |
| html5lib       | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                   |
| sphinx         | 434 ms                                                   | 415 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.00x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 202 ms: 2.45x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.44x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 193 ms: 2.31x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 85.6 ms: 2.01x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 99.9 ms: 1.79x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.72x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 235 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.5 ms: 1.07x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.1 ms: 2.40x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.2 ms: 1.34x faster                                                   |
| nbody          | 54.2 ms                                                  | 55.3 ms: 1.02x slower                                                   |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 52.3 ms: 1.04x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.21 ms: 1.04x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.4 ms: 1.02x faster                                                   |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.8 ms: 1.33x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 60.0 ms: 1.13x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.5 ms: 1.06x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.5 ms: 1.01x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 150 us: 1.07x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.61 ms: 1.08x slower                                                   |
| json_loads           | 10.9 us                                                  | 11.8 us: 1.08x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.08x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                            |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.70 ms: 1.21x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.05 ms: 1.24x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.22x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.6 ms: 1.08x slower                                                   |
| genshi_text     | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                   |
| mako            | 4.77 ms                                                  | 5.62 ms: 1.18x slower                                                   |
| django_template | 13.6 ms                                                  | 16.4 ms: 1.20x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.14x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 782 us: 2.57x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 202 ms: 2.45x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.44x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 193 ms: 2.31x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.20x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 85.6 ms: 2.01x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.87x faster                                                    |
| mdp                              | 1.09 sec                                                 | 604 ms: 1.81x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 99.9 ms: 1.79x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.72x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 487 us: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 235 ms: 1.44x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 243 ms: 1.37x faster                                                    |
| deepcopy                         | 161 us                                                   | 118 us: 1.37x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.6 us: 1.35x faster                                                   |
| float                            | 37.9 ms                                                  | 28.2 ms: 1.34x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.8 ms: 1.33x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.26 us: 1.19x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 814 ns: 1.19x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.24 us: 1.17x faster                                                   |
| go                               | 70.0 ms                                                  | 60.0 ms: 1.17x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 44.3 ns: 1.15x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 18.2 ms: 1.14x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.3 ms: 1.14x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 60.0 ms: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 988 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.13x faster                                                  |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.12x faster                                                   |
| raytrace                         | 145 ms                                                   | 129 ms: 1.12x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.11x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 49.5 ms: 1.10x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.8 ms: 1.09x faster                                                   |
| pyflate                          | 216 ms                                                   | 199 ms: 1.09x faster                                                    |
| pylint                           | 128 ms                                                   | 119 ms: 1.08x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.5 ms: 1.06x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.62 ms: 1.06x faster                                                   |
| pycparser                        | 497 ms                                                   | 473 ms: 1.05x faster                                                    |
| sphinx                           | 434 ms                                                   | 415 ms: 1.04x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 52.3 ms: 1.04x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.21 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| docutils                         | 1.02 sec                                                 | 998 ms: 1.02x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 97.4 ms: 1.02x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.02x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.54 us: 1.01x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 26.5 ms: 1.01x faster                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 112 ms: 1.01x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 141 ms: 1.01x faster                                                    |
| chaos                            | 28.9 ms                                                  | 29.1 ms: 1.01x slower                                                   |
| dask                             | 528 ms                                                   | 531 ms: 1.01x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.10 ms: 1.01x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                   |
| nbody                            | 54.2 ms                                                  | 55.3 ms: 1.02x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.12 ms: 1.03x slower                                                   |
| thrift                           | 322 us                                                   | 331 us: 1.03x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.1 ms: 1.03x slower                                                   |
| fannkuch                         | 176 ms                                                   | 181 ms: 1.03x slower                                                    |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.4 ms: 1.04x slower                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 73.8 us: 1.04x slower                                                   |
| json                             | 1.93 ms                                                  | 2.01 ms: 1.04x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.8 ms: 1.05x slower                                                   |
| shortest_path                    | 219 ms                                                   | 232 ms: 1.06x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 48.5 ms: 1.07x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 350 ms: 1.07x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 227 ms: 1.07x slower                                                    |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 712 ms: 1.07x slower                                                    |
| sympy_str                        | 104 ms                                                   | 112 ms: 1.07x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 61.8 ms: 1.07x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 150 us: 1.07x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.61 ms: 1.08x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 23.6 ms: 1.08x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.8 us: 1.08x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.08x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 42.4 ms: 1.09x slower                                                   |
| connected_components             | 201 ms                                                   | 219 ms: 1.09x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 56.2 ms: 1.10x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.28 ms: 1.10x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 190 ms: 1.14x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 45.5 ms: 1.15x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 56.0 ms: 1.17x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.62 ms: 1.18x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.4 ms: 1.20x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.70 ms: 1.21x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.05 ms: 1.24x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.23 ms: 1.24x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 583 us: 1.39x slower                                                    |
| coverage                         | 26.9 ms                                                  | 39.7 ms: 1.48x slower                                                   |
| many_optionals                   | 195 us                                                   | 330 us: 1.69x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 77.1 ms: 2.40x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (3): nqueens, logging_format, tomli_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250722-3.15.0a0-b13a5df-NOGIL/bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.088x faster

# HPT report

- Reliability score: 97.20% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.26x