# Results vs. 3.12.6

- fork: python
- ref: 04ace41fe2cf648be433
- machine: darwin-arm64
- commit hash: 04ace41
- commit date: 2026-01-05
- overall geometric mean: 1.083x faster
- HPT reliability: 98.74%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260105-macm4pro-arm64-python-04ace41fe2cf648be433-3.15.0a3+-04ace41 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 124 ms: 1.08x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.02 sec: 1.00x faster                                                   |
| html5lib       | 23.0 ms                                                  | 23.6 ms: 1.02x slower                                                    |
| sphinx         | 434 ms                                                   | 428 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260105-macm4pro-arm64-python-04ace41fe2cf648be433-3.15.0a3+-04ace41 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 240 ms: 2.00x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 253 ms: 1.96x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 253 ms: 1.82x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 250 ms: 1.79x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 154 ms: 1.45x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 271 ms: 1.23x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.15x faster                                                     |
| async_generators                 | 206 ms                                                   | 188 ms: 1.10x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 229 ms: 1.01x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.4 ms: 1.04x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.15x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.8 ms: 2.95x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.22x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260105-macm4pro-arm64-python-04ace41fe2cf648be433-3.15.0a3+-04ace41 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.9 ms: 1.31x faster                                                    |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                     |
| nbody          | 54.2 ms                                                  | 56.7 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260105-macm4pro-arm64-python-04ace41fe2cf648be433-3.15.0a3+-04ace41 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 51.3 ms: 1.06x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.5 ms: 1.03x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.41 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260105-macm4pro-arm64-python-04ace41fe2cf648be433-3.15.0a3+-04ace41 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.0 ms: 1.29x faster                                                    |
| tomli_loads          | 957 ms                                                   | 882 ms: 1.09x faster                                                     |
| xml_etree_parse      | 67.9 ms                                                  | 62.7 ms: 1.08x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 4.01 ms: 1.06x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.2 ms: 1.05x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.2 ms: 1.02x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 149 us: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260105-macm4pro-arm64-python-04ace41fe2cf648be433-3.15.0a3+-04ace41 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.89 ms: 1.23x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.18 ms: 1.26x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.25x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260105-macm4pro-arm64-python-04ace41fe2cf648be433-3.15.0a3+-04ace41 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.4 ms: 1.08x slower                                                    |
| genshi_xml      | 21.8 ms                                                  | 23.6 ms: 1.08x slower                                                    |
| mako            | 4.77 ms                                                  | 5.51 ms: 1.15x slower                                                    |
| django_template | 13.6 ms                                                  | 15.8 ms: 1.16x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.12x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260105-macm4pro-arm64-python-04ace41fe2cf648be433-3.15.0a3+-04ace41 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.24 ms: 4.90x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 818 us: 2.46x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 240 ms: 2.00x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 253 ms: 1.96x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 253 ms: 1.82x faster                                                     |
| mdp                              | 1.09 sec                                                 | 611 ms: 1.79x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 250 ms: 1.79x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 516 us: 1.61x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.54x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.5 us: 1.46x faster                                                    |
| deepcopy                         | 161 us                                                   | 111 us: 1.45x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 154 ms: 1.45x faster                                                     |
| float                            | 37.9 ms                                                  | 28.9 ms: 1.31x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.0 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 271 ms: 1.23x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.20 us: 1.21x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 43.0 ns: 1.18x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.41 us: 1.17x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 828 ns: 1.17x faster                                                     |
| go                               | 70.0 ms                                                  | 60.4 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.15x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 125 ms: 1.14x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.14x faster                                                    |
| raytrace                         | 145 ms                                                   | 128 ms: 1.14x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                   |
| k_core                           | 1.12 sec                                                 | 998 ms: 1.12x faster                                                     |
| pyflate                          | 216 ms                                                   | 194 ms: 1.12x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 54.7 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                    |
| async_generators                 | 206 ms                                                   | 188 ms: 1.10x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 882 ms: 1.09x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 62.7 ms: 1.08x faster                                                    |
| pylint                           | 128 ms                                                   | 119 ms: 1.07x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 50.9 ms: 1.07x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 51.3 ms: 1.06x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.01 ms: 1.06x faster                                                    |
| pycparser                        | 497 ms                                                   | 470 ms: 1.06x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 37.2 ms: 1.05x faster                                                    |
| generators                       | 21.9 ms                                                  | 21.0 ms: 1.04x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.65 ms: 1.04x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.48 us: 1.04x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.5 ms: 1.03x faster                                                    |
| chaos                            | 28.9 ms                                                  | 28.3 ms: 1.02x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.75 us: 1.02x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.41 ms: 1.02x faster                                                    |
| sphinx                           | 434 ms                                                   | 428 ms: 1.01x faster                                                     |
| fannkuch                         | 176 ms                                                   | 174 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 229 ms: 1.01x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.02 sec: 1.00x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.4 ms: 1.01x slower                                                    |
| nqueens                          | 43.5 ms                                                  | 43.9 ms: 1.01x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 71.6 us: 1.01x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.2 ms: 1.02x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.15 ms: 1.02x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.6 ms: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 338 ms: 1.03x slower                                                     |
| hexiom                           | 3.04 ms                                                  | 3.14 ms: 1.03x slower                                                    |
| json                             | 1.93 ms                                                  | 2.00 ms: 1.03x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.2 ms: 1.04x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 47.4 ms: 1.04x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 693 ms: 1.04x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 26.6 ms: 1.05x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.7 ms: 1.05x slower                                                    |
| thrift                           | 322 us                                                   | 338 us: 1.05x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 61.1 ms: 1.06x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 149 us: 1.07x slower                                                     |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.07x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.4 ms: 1.08x slower                                                    |
| 2to3                             | 114 ms                                                   | 124 ms: 1.08x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 23.6 ms: 1.08x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.2 ms: 1.09x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 190 ms: 1.14x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 58.7 ms: 1.14x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.15x slower                                                     |
| shortest_path                    | 219 ms                                                   | 251 ms: 1.15x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.00 ms: 1.15x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.51 ms: 1.15x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.8 ms: 1.16x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 56.0 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 46.9 ms: 1.18x slower                                                    |
| connected_components             | 201 ms                                                   | 245 ms: 1.22x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.89 ms: 1.23x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.18 ms: 1.26x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 551 us: 1.32x slower                                                     |
| many_optionals                   | 195 us                                                   | 277 us: 1.42x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.5 ms: 1.43x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.8 ms: 2.95x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (3): dask, scimark_sparse_mat_mult, asyncio_websockets
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260105-3.15.0a3+-04ace41-NOGIL/bm-20260105-macm4pro-arm64-python-04ace41fe2cf648be433-3.15.0a3+-04ace41.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.083x faster

# HPT report

- Reliability score: 98.74% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.34x