# Results vs. 3.12.6

- fork: python
- ref: 5637f4e38a68cd015daa
- machine: darwin-arm64
- commit hash: 5637f4e
- commit date: 2026-09-27
- overall geometric mean: 1.048x faster
- HPT reliability: 80.63%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 130 ms: 1.14x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.07 sec: 1.04x slower                                                  |
| html5lib       | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                   |
| sphinx         | 434 ms                                                   | 445 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.05x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 303 ms: 1.64x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 294 ms: 1.63x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 293 ms: 1.52x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 304 ms: 1.51x faster                                                    |
| async_generators                 | 206 ms                                                   | 159 ms: 1.30x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 179 ms: 1.29x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 139 ms: 1.24x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 193 ms: 1.15x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 11.8 ms: 1.15x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 155 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 296 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 305 ms: 1.09x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 147 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 263 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 279 ms: 1.31x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 163 ms: 1.45x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 68.1 ms: 1.49x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 114 ms: 3.54x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 32.9 ms: 1.15x faster                                                   |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| nbody          | 54.2 ms                                                  | 57.2 ms: 1.06x slower                                                   |
| Geometric mean | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.37 ms: 1.22x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 93.4 ms: 1.07x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.30 ms: 1.03x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 63.0 ms: 1.15x slower                                                   |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.9 ms: 1.26x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 59.7 ms: 1.14x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.78 ms: 1.13x faster                                                   |
| tomli_loads          | 957 ms                                                   | 888 ms: 1.08x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 38.1 ms: 1.02x faster                                                   |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.04x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 29.4 ms: 1.10x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 156 us: 1.12x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 10.2 ms: 1.28x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.46 ms: 1.31x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.29x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 5.67 ms: 1.19x slower                                                   |
| django_template | 13.6 ms                                                  | 17.0 ms: 1.25x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.22x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.31 ms: 4.82x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 777 us: 2.59x faster                                                    |
| pylint                           | 128 ms                                                   | 53.9 ms: 2.38x faster                                                   |
| mdp                              | 1.09 sec                                                 | 598 ms: 1.82x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 491 us: 1.69x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 303 ms: 1.64x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 294 ms: 1.63x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 293 ms: 1.52x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 304 ms: 1.51x faster                                                    |
| deepcopy                         | 161 us                                                   | 109 us: 1.48x faster                                                    |
| async_generators                 | 206 ms                                                   | 159 ms: 1.30x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 14.2 us: 1.29x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 179 ms: 1.29x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.9 ms: 1.26x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 57.0 us: 1.24x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 139 ms: 1.24x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.20 us: 1.22x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.37 ms: 1.22x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 808 ns: 1.20x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.29 us: 1.19x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.92 sec: 1.17x faster                                                  |
| float                            | 37.9 ms                                                  | 32.9 ms: 1.15x faster                                                   |
| go                               | 70.0 ms                                                  | 60.8 ms: 1.15x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 193 ms: 1.15x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 11.8 ms: 1.15x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 155 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 296 ms: 1.14x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 59.7 ms: 1.14x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.78 ms: 1.13x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 126 ms: 1.12x faster                                                    |
| k_core                           | 1.12 sec                                                 | 997 ms: 1.12x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 49.0 ms: 1.11x faster                                                   |
| pyflate                          | 216 ms                                                   | 196 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 305 ms: 1.09x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.6 ms: 1.09x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 888 ms: 1.08x faster                                                    |
| raytrace                         | 145 ms                                                   | 136 ms: 1.07x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 93.4 ms: 1.07x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 57.7 ms: 1.06x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 48.5 ns: 1.05x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.46 us: 1.05x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.30 ms: 1.03x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.72 us: 1.03x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| pycparser                        | 497 ms                                                   | 484 ms: 1.03x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 38.1 ms: 1.02x faster                                                   |
| fannkuch                         | 176 ms                                                   | 172 ms: 1.02x faster                                                    |
| chaos                            | 28.9 ms                                                  | 28.5 ms: 1.02x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 43.1 ms: 1.01x faster                                                   |
| html5lib                         | 23.0 ms                                                  | 23.3 ms: 1.01x slower                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 8.15 ms: 1.02x slower                                                   |
| sphinx                           | 434 ms                                                   | 445 ms: 1.03x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.2 ms: 1.03x slower                                                   |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.04x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.07 sec: 1.04x slower                                                  |
| json                             | 1.93 ms                                                  | 2.02 ms: 1.04x slower                                                   |
| nbody                            | 54.2 ms                                                  | 57.2 ms: 1.06x slower                                                   |
| deltablue                        | 1.73 ms                                                  | 1.82 ms: 1.06x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.21 ms: 1.06x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 61.0 ms: 1.06x slower                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 41.3 ms: 1.06x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 349 ms: 1.07x slower                                                    |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.07x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.23 ms: 1.07x slower                                                   |
| generators                       | 21.9 ms                                                  | 23.7 ms: 1.08x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 726 ms: 1.09x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 29.4 ms: 1.10x slower                                                   |
| thrift                           | 322 us                                                   | 354 us: 1.10x slower                                                    |
| richards                         | 22.4 ms                                                  | 24.7 ms: 1.10x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 28.2 ms: 1.11x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.2 ms: 1.11x slower                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 147 ms: 1.12x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 53.4 ms: 1.12x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 156 us: 1.12x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                    |
| shortest_path                    | 219 ms                                                   | 249 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 263 ms: 1.14x slower                                                    |
| 2to3                             | 114 ms                                                   | 130 ms: 1.14x slower                                                    |
| regex_compile                    | 54.6 ms                                                  | 63.0 ms: 1.15x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.07 ms: 1.18x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.67 ms: 1.19x slower                                                   |
| connected_components             | 201 ms                                                   | 241 ms: 1.20x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 63.9 ms: 1.25x slower                                                   |
| django_template                  | 13.6 ms                                                  | 17.0 ms: 1.25x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 10.2 ms: 1.28x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.46 ms: 1.31x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 279 ms: 1.31x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 565 us: 1.35x slower                                                    |
| many_optionals                   | 195 us                                                   | 269 us: 1.38x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 163 ms: 1.45x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 68.1 ms: 1.49x slower                                                   |
| coverage                         | 26.9 ms                                                  | 41.4 ms: 1.54x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 114 ms: 3.54x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.04x faster                                                            |
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260927-3.16.0a0-5637f4e-NOGIL/bm-20260927-macm4pro-arm64-python-5637f4e38a68cd015daa-3.16.0a0-5637f4e.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.048x faster

# HPT report

- Reliability score: 80.63% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.33x