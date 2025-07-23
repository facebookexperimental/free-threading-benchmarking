# Results vs. 3.12.6

- fork: python
- ref: b13a5df52fc854d1097e
- machine: darwin-arm64
- commit hash: b13a5df
- commit date: 2025-07-22
- overall geometric mean: 1.088x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 117 ms: 1.03x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.7 ms: 1.07x slower                                                   |
| sphinx         | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 251 ms: 1.98x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 252 ms: 1.91x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 259 ms: 1.77x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 260 ms: 1.72x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 108 ms: 1.60x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.55x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.99 ms: 1.36x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 266 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 269 ms: 1.24x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.1 ms: 1.08x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 251 ms: 1.18x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.9 ms: 2.77x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 31.1 ms: 1.22x faster                                                   |
| nbody          | 54.2 ms                                                  | 48.6 ms: 1.12x faster                                                   |
| pidigits       | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 49.2 ms: 1.11x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.90 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.9 ms: 1.18x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.4 ms: 1.10x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 63.5 ms: 1.07x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                   |
| tomli_loads          | 957 ms                                                   | 934 ms: 1.03x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 102 us: 1.01x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.9 us: 1.01x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 4.48 ms: 1.05x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 148 us: 1.06x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.74 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.26 ms: 1.10x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.0 ms: 1.05x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.9 ms: 1.00x slower                                                   |
| mako            | 4.77 ms                                                  | 4.91 ms: 1.03x slower                                                   |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.03x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 542 ms: 2.01x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 251 ms: 1.98x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 252 ms: 1.91x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 259 ms: 1.77x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 260 ms: 1.72x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 108 ms: 1.60x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.56x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.55x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.51x faster                                                    |
| deepcopy                         | 161 us                                                   | 112 us: 1.44x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.7 us: 1.44x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 9.99 ms: 1.36x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.53 us: 1.31x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 266 ms: 1.27x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 40.1 ns: 1.27x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.16 us: 1.26x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 269 ms: 1.24x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 43.9 ms: 1.24x faster                                                   |
| go                               | 70.0 ms                                                  | 56.7 ms: 1.23x faster                                                   |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.9 ms: 1.22x faster                                                   |
| float                            | 37.9 ms                                                  | 31.1 ms: 1.22x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 51.0 ms: 1.20x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 17.6 ms: 1.18x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.9 ms: 1.18x faster                                                   |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                    |
| k_core                           | 1.12 sec                                                 | 955 ms: 1.17x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.5 ms: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.53 ms: 1.12x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.8 ms: 1.12x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                  |
| nbody                            | 54.2 ms                                                  | 48.6 ms: 1.12x faster                                                   |
| pylint                           | 128 ms                                                   | 115 ms: 1.11x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 49.2 ms: 1.11x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 64.0 us: 1.11x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.2 ms: 1.11x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.4 ms: 1.10x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.5 ms: 1.09x faster                                                   |
| pyflate                          | 216 ms                                                   | 199 ms: 1.08x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.1 ms: 1.08x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.9 ms: 1.08x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 63.5 ms: 1.07x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.62 us: 1.07x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 133 ms: 1.07x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.52 ms: 1.07x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.42 us: 1.06x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.87 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 410 ms: 1.06x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 24.1 ms: 1.05x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.3 ms: 1.05x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 10.0 ms: 1.05x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.99 ms: 1.05x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 49.2 ms: 1.04x faster                                                   |
| thrift                           | 322 us                                                   | 311 us: 1.03x faster                                                    |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.8 ms: 1.03x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 934 ms: 1.03x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 951 ns: 1.02x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 102 us: 1.01x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 57.0 ms: 1.01x faster                                                   |
| connected_components             | 201 ms                                                   | 199 ms: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 217 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 327 ms: 1.00x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 662 ms: 1.00x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.9 ms: 1.00x slower                                                   |
| json_loads                       | 10.9 us                                                  | 10.9 us: 1.01x slower                                                   |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 170 ms: 1.02x slower                                                    |
| 2to3                             | 114 ms                                                   | 117 ms: 1.03x slower                                                    |
| mako                             | 4.77 ms                                                  | 4.91 ms: 1.03x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.90 ms: 1.03x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 433 us: 1.03x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| pidigits                         | 161 ms                                                   | 168 ms: 1.04x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.9 ms: 1.05x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.10 ms: 1.05x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.48 ms: 1.05x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 148 us: 1.06x slower                                                    |
| fannkuch                         | 176 ms                                                   | 187 ms: 1.06x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.7 ms: 1.07x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.74 ms: 1.09x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.26 ms: 1.10x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.4 ms: 1.12x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 957 us: 1.15x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 132 ms: 1.17x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.05 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 251 ms: 1.18x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.7 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 326 us: 1.67x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 88.9 ms: 2.77x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                            |

Benchmark hidden because not significant (3): regex_dna, json, pycparser
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250722-3.15.0a0-b13a5df/bm-20250722-macm4pro-arm64-python-b13a5df52fc854d1097e-3.15.0a0-b13a5df.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.088x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.14x