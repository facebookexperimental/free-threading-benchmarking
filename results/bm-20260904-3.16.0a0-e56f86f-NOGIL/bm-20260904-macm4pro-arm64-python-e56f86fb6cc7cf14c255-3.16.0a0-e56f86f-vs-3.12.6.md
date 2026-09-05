# Results vs. 3.12.6

- fork: python
- ref: e56f86fb6cc7cf14c255
- machine: darwin-arm64
- commit hash: e56f86f
- commit date: 2026-09-04
- overall geometric mean: 1.056x faster
- HPT reliability: 87.63%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 131 ms: 1.15x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.07 sec: 1.05x slower                                                  |
| html5lib       | 23.0 ms                                                  | 23.4 ms: 1.02x slower                                                   |
| sphinx         | 434 ms                                                   | 446 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.06x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 296 ms: 1.68x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 295 ms: 1.63x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 294 ms: 1.52x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 306 ms: 1.50x faster                                                    |
| async_generators                 | 206 ms                                                   | 157 ms: 1.31x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 180 ms: 1.28x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 142 ms: 1.26x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 139 ms: 1.23x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 185 ms: 1.20x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 11.5 ms: 1.18x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 297 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 303 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 125 ms: 1.06x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 237 ms: 1.03x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.4 ms: 1.08x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 277 ms: 1.30x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 163 ms: 1.44x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 114 ms: 3.53x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 33.0 ms: 1.15x faster                                                   |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| nbody          | 54.2 ms                                                  | 56.0 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.39 ms: 1.20x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 94.1 ms: 1.06x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 63.4 ms: 1.16x slower                                                   |
| Geometric mean | (ref)                                                    | 1.02x faster                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.3 ms: 1.25x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.72 ms: 1.14x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 59.4 ms: 1.14x faster                                                   |
| tomli_loads          | 957 ms                                                   | 916 ms: 1.05x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.9 ms: 1.03x faster                                                   |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.04x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 110 us: 1.07x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 29.4 ms: 1.10x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 154 us: 1.11x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 10.3 ms: 1.28x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.56 ms: 1.33x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.30x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 5.70 ms: 1.19x slower                                                   |
| django_template | 13.6 ms                                                  | 16.9 ms: 1.24x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.22x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.34 ms: 4.79x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 786 us: 2.56x faster                                                    |
| pylint                           | 128 ms                                                   | 54.5 ms: 2.35x faster                                                   |
| mdp                              | 1.09 sec                                                 | 607 ms: 1.80x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 493 us: 1.68x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 296 ms: 1.68x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 295 ms: 1.63x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 294 ms: 1.52x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 306 ms: 1.50x faster                                                    |
| deepcopy                         | 161 us                                                   | 113 us: 1.43x faster                                                    |
| async_generators                 | 206 ms                                                   | 157 ms: 1.31x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 14.1 us: 1.29x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 180 ms: 1.28x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 142 ms: 1.26x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 56.6 us: 1.25x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.3 ms: 1.25x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 139 ms: 1.23x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 798 ns: 1.21x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 185 ms: 1.20x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.21 us: 1.20x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.39 ms: 1.20x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.23 us: 1.19x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 11.5 ms: 1.18x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.90 sec: 1.18x faster                                                  |
| go                               | 70.0 ms                                                  | 60.8 ms: 1.15x faster                                                   |
| float                            | 37.9 ms                                                  | 33.0 ms: 1.15x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.72 ms: 1.14x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 59.4 ms: 1.14x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 297 ms: 1.14x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 125 ms: 1.14x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 999 ms: 1.12x faster                                                    |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 49.1 ms: 1.11x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 303 ms: 1.10x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.4 ms: 1.09x faster                                                   |
| raytrace                         | 145 ms                                                   | 136 ms: 1.06x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.1 ms: 1.06x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 125 ms: 1.06x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 58.0 ms: 1.05x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 916 ms: 1.05x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.48 us: 1.04x faster                                                   |
| pycparser                        | 497 ms                                                   | 481 ms: 1.03x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 49.4 ns: 1.03x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.9 ms: 1.03x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 42.6 ms: 1.02x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.75 us: 1.02x faster                                                   |
| chaos                            | 28.9 ms                                                  | 28.5 ms: 1.02x faster                                                   |
| fannkuch                         | 176 ms                                                   | 174 ms: 1.01x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 23.4 ms: 1.02x slower                                                   |
| json                             | 1.93 ms                                                  | 1.97 ms: 1.02x slower                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 8.19 ms: 1.02x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 237 ms: 1.03x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.1 ms: 1.03x slower                                                   |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| sphinx                           | 434 ms                                                   | 446 ms: 1.03x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.0 ms: 1.03x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.04x slower                                                   |
| hexiom                           | 3.04 ms                                                  | 3.17 ms: 1.04x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.17 ms: 1.04x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.07 sec: 1.05x slower                                                  |
| crypto_pyaes                     | 38.8 ms                                                  | 41.4 ms: 1.07x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 110 us: 1.07x slower                                                    |
| sympy_str                        | 104 ms                                                   | 112 ms: 1.07x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 61.7 ms: 1.07x slower                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 353 ms: 1.08x slower                                                    |
| deltablue                        | 1.73 ms                                                  | 1.86 ms: 1.08x slower                                                   |
| generators                       | 21.9 ms                                                  | 23.7 ms: 1.08x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 49.4 ms: 1.08x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 721 ms: 1.09x slower                                                    |
| thrift                           | 322 us                                                   | 351 us: 1.09x slower                                                    |
| richards                         | 22.4 ms                                                  | 24.5 ms: 1.09x slower                                                   |
| xml_etree_process                | 26.7 ms                                                  | 29.4 ms: 1.10x slower                                                   |
| richards_super                   | 25.4 ms                                                  | 28.1 ms: 1.11x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 52.9 ms: 1.11x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 154 us: 1.11x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 44.2 ms: 1.11x slower                                                   |
| sympy_expand                     | 167 ms                                                   | 190 ms: 1.13x slower                                                    |
| shortest_path                    | 219 ms                                                   | 251 ms: 1.15x slower                                                    |
| 2to3                             | 114 ms                                                   | 131 ms: 1.15x slower                                                    |
| regex_compile                    | 54.6 ms                                                  | 63.4 ms: 1.16x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.11 ms: 1.19x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.70 ms: 1.19x slower                                                   |
| connected_components             | 201 ms                                                   | 242 ms: 1.21x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 63.2 ms: 1.23x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.9 ms: 1.24x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 10.3 ms: 1.28x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 277 ms: 1.30x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.56 ms: 1.33x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 556 us: 1.33x slower                                                    |
| many_optionals                   | 195 us                                                   | 269 us: 1.38x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 163 ms: 1.44x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.9 ms: 1.52x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 114 ms: 3.53x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.05x faster                                                            |

Benchmark hidden because not significant (1): regex_v8
Ignored benchmarks (13) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260904-3.16.0a0-e56f86f-NOGIL/bm-20260904-macm4pro-arm64-python-e56f86fb6cc7cf14c255-3.16.0a0-e56f86f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.056x faster

# HPT report

- Reliability score: 87.63% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.33x