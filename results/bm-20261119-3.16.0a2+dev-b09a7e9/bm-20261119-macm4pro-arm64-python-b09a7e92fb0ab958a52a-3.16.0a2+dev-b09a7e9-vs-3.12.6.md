# Results vs. 3.12.6

- fork: python
- ref: b09a7e92fb0ab958a52a
- machine: darwin-arm64
- commit hash: b09a7e9
- commit date: 2026-11-19
- overall geometric mean: 1.190x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2+dev-b09a7e9 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.00x slower                                                        |
| docutils       | 1.02 sec                                                 | 916 ms: 1.12x faster                                                        |
| html5lib       | 23.0 ms                                                  | 20.8 ms: 1.11x faster                                                       |
| sphinx         | 434 ms                                                   | 393 ms: 1.10x faster                                                        |
| Geometric mean | (ref)                                                    | 1.08x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2+dev-b09a7e9 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_generators                 | 206 ms                                                   | 96.7 ms: 2.13x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 268 ms: 1.85x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 279 ms: 1.72x faster                                                        |
| async_tree_io                    | 459 ms                                                   | 273 ms: 1.68x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 281 ms: 1.58x faster                                                        |
| async_tree_none_tg               | 172 ms                                                   | 112 ms: 1.53x faster                                                        |
| async_tree_memoization_tg        | 231 ms                                                   | 158 ms: 1.46x faster                                                        |
| coroutines                       | 13.6 ms                                                  | 9.69 ms: 1.40x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 163 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 268 ms: 1.25x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 272 ms: 1.24x faster                                                        |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                        |
| async_tree_eager                 | 45.6 ms                                                  | 40.6 ms: 1.12x faster                                                       |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                        |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                        |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 142 ms: 1.26x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.8 ms: 2.92x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                                |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2+dev-b09a7e9 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.5 ms: 1.38x faster                                                       |
| nbody          | 54.2 ms                                                  | 42.0 ms: 1.29x faster                                                       |
| pidigits       | 161 ms                                                   | 152 ms: 1.06x faster                                                        |
| Geometric mean | (ref)                                                    | 1.24x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2+dev-b09a7e9 |
|----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                       |
| regex_dna      | 99.6 ms                                                  | 92.7 ms: 1.07x faster                                                       |
| regex_v8       | 9.59 ms                                                  | 9.20 ms: 1.04x faster                                                       |
| regex_compile  | 54.6 ms                                                  | 53.6 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                    | 1.10x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2+dev-b09a7e9 |
|----------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.9 ms: 1.23x faster                                                       |
| tomli_loads          | 957 ms                                                   | 805 ms: 1.19x faster                                                        |
| json_dumps           | 4.26 ms                                                  | 3.64 ms: 1.17x faster                                                       |
| xml_etree_generate   | 38.9 ms                                                  | 34.4 ms: 1.13x faster                                                       |
| unpickle_pure_python | 103 us                                                   | 94.1 us: 1.09x faster                                                       |
| xml_etree_process    | 26.7 ms                                                  | 25.0 ms: 1.07x faster                                                       |
| xml_etree_parse      | 67.9 ms                                                  | 65.4 ms: 1.04x faster                                                       |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.02x faster                                                       |
| pickle_pure_python   | 139 us                                                   | 140 us: 1.00x slower                                                        |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2+dev-b09a7e9 |
|------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.70 ms: 1.09x slower                                                       |
| python_startup_no_site | 5.71 ms                                                  | 6.74 ms: 1.18x slower                                                       |
| Geometric mean         | (ref)                                                    | 1.13x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2+dev-b09a7e9 |
|-----------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.37 ms: 1.09x faster                                                       |
| django_template | 13.6 ms                                                  | 14.8 ms: 1.08x slower                                                       |
| Geometric mean  | (ref)                                                    | 1.00x faster                                                                |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2+dev-b09a7e9 |
|----------------------------------|:--------------------------------------------------------:|:---------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.97 ms: 5.23x faster                                                       |
| pylint                           | 128 ms                                                   | 52.4 ms: 2.44x faster                                                       |
| mdp                              | 1.09 sec                                                 | 504 ms: 2.17x faster                                                        |
| async_generators                 | 206 ms                                                   | 96.7 ms: 2.13x faster                                                       |
| async_tree_eager_io              | 496 ms                                                   | 268 ms: 1.85x faster                                                        |
| async_tree_io_tg                 | 480 ms                                                   | 279 ms: 1.72x faster                                                        |
| deepcopy                         | 161 us                                                   | 95.9 us: 1.68x faster                                                       |
| async_tree_io                    | 459 ms                                                   | 273 ms: 1.68x faster                                                        |
| async_tree_none                  | 178 ms                                                   | 112 ms: 1.59x faster                                                        |
| async_tree_eager_io_tg           | 446 ms                                                   | 281 ms: 1.58x faster                                                        |
| deepcopy_memo                    | 18.3 us                                                  | 11.6 us: 1.57x faster                                                       |
| typing_runtime_protocols         | 71.0 us                                                  | 45.2 us: 1.57x faster                                                       |
| async_tree_none_tg               | 172 ms                                                   | 112 ms: 1.53x faster                                                        |
| comprehensions                   | 9.84 us                                                  | 6.66 us: 1.48x faster                                                       |
| async_tree_memoization_tg        | 231 ms                                                   | 158 ms: 1.46x faster                                                        |
| deepcopy_reduce                  | 1.46 us                                                  | 1.03 us: 1.42x faster                                                       |
| coroutines                       | 13.6 ms                                                  | 9.69 ms: 1.40x faster                                                       |
| float                            | 37.9 ms                                                  | 27.5 ms: 1.38x faster                                                       |
| async_tree_memoization           | 223 ms                                                   | 163 ms: 1.37x faster                                                        |
| go                               | 70.0 ms                                                  | 52.1 ms: 1.34x faster                                                       |
| spectral_norm                    | 54.4 ms                                                  | 40.9 ms: 1.33x faster                                                       |
| create_gc_cycles                 | 830 us                                                   | 642 us: 1.29x faster                                                        |
| nbody                            | 54.2 ms                                                  | 42.0 ms: 1.29x faster                                                       |
| scimark_fft                      | 142 ms                                                   | 110 ms: 1.29x faster                                                        |
| raytrace                         | 145 ms                                                   | 113 ms: 1.28x faster                                                        |
| generators                       | 21.9 ms                                                  | 17.2 ms: 1.28x faster                                                       |
| nqueens                          | 43.5 ms                                                  | 34.3 ms: 1.27x faster                                                       |
| regex_effbot                     | 1.67 ms                                                  | 1.32 ms: 1.26x faster                                                       |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 268 ms: 1.25x faster                                                        |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 272 ms: 1.24x faster                                                        |
| scimark_sor                      | 61.0 ms                                                  | 49.5 ms: 1.23x faster                                                       |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.9 ms: 1.23x faster                                                       |
| logging_silent                   | 50.9 ns                                                  | 41.7 ns: 1.22x faster                                                       |
| scimark_monte_carlo              | 32.2 ms                                                  | 26.4 ms: 1.22x faster                                                       |
| deltablue                        | 1.73 ms                                                  | 1.44 ms: 1.20x faster                                                       |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.87 sec: 1.19x faster                                                      |
| tomli_loads                      | 957 ms                                                   | 805 ms: 1.19x faster                                                        |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.75 ms: 1.18x faster                                                       |
| logging_simple                   | 2.57 us                                                  | 2.18 us: 1.18x faster                                                       |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.18x faster                                                       |
| chaos                            | 28.9 ms                                                  | 24.6 ms: 1.18x faster                                                       |
| json_dumps                       | 4.26 ms                                                  | 3.64 ms: 1.17x faster                                                       |
| logging_format                   | 2.80 us                                                  | 2.40 us: 1.17x faster                                                       |
| pyflate                          | 216 ms                                                   | 186 ms: 1.16x faster                                                        |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.16x faster                                                       |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                        |
| hexiom                           | 3.04 ms                                                  | 2.63 ms: 1.16x faster                                                       |
| k_core                           | 1.12 sec                                                 | 982 ms: 1.14x faster                                                        |
| xml_etree_generate               | 38.9 ms                                                  | 34.4 ms: 1.13x faster                                                       |
| async_tree_eager                 | 45.6 ms                                                  | 40.6 ms: 1.12x faster                                                       |
| docutils                         | 1.02 sec                                                 | 916 ms: 1.12x faster                                                        |
| gc_traversal                     | 2.01 ms                                                  | 1.81 ms: 1.11x faster                                                       |
| html5lib                         | 23.0 ms                                                  | 20.8 ms: 1.11x faster                                                       |
| sphinx                           | 434 ms                                                   | 393 ms: 1.10x faster                                                        |
| fannkuch                         | 176 ms                                                   | 160 ms: 1.10x faster                                                        |
| richards                         | 22.4 ms                                                  | 20.4 ms: 1.10x faster                                                       |
| richards_super                   | 25.4 ms                                                  | 23.2 ms: 1.10x faster                                                       |
| unpickle_pure_python             | 103 us                                                   | 94.1 us: 1.09x faster                                                       |
| mako                             | 4.77 ms                                                  | 4.37 ms: 1.09x faster                                                       |
| scimark_lu                       | 51.3 ms                                                  | 47.0 ms: 1.09x faster                                                       |
| sympy_integrate                  | 8.02 ms                                                  | 7.36 ms: 1.09x faster                                                       |
| regex_dna                        | 99.6 ms                                                  | 92.7 ms: 1.07x faster                                                       |
| xml_etree_process                | 26.7 ms                                                  | 25.0 ms: 1.07x faster                                                       |
| crypto_pyaes                     | 38.8 ms                                                  | 36.4 ms: 1.07x faster                                                       |
| thrift                           | 322 us                                                   | 302 us: 1.07x faster                                                        |
| pprint_safe_repr                 | 328 ms                                                   | 308 ms: 1.06x faster                                                        |
| pidigits                         | 161 ms                                                   | 152 ms: 1.06x faster                                                        |
| sympy_str                        | 104 ms                                                   | 99.1 ms: 1.05x faster                                                       |
| pycparser                        | 497 ms                                                   | 473 ms: 1.05x faster                                                        |
| pprint_pformat                   | 665 ms                                                   | 634 ms: 1.05x faster                                                        |
| sqlite_synth                     | 967 ns                                                   | 926 ns: 1.04x faster                                                        |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                        |
| regex_v8                         | 9.59 ms                                                  | 9.20 ms: 1.04x faster                                                       |
| sympy_sum                        | 57.6 ms                                                  | 55.2 ms: 1.04x faster                                                       |
| xml_etree_parse                  | 67.9 ms                                                  | 65.4 ms: 1.04x faster                                                       |
| bench_thread_pool                | 419 us                                                   | 408 us: 1.03x faster                                                        |
| json                             | 1.93 ms                                                  | 1.89 ms: 1.02x faster                                                       |
| regex_compile                    | 54.6 ms                                                  | 53.6 ms: 1.02x faster                                                       |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.02x faster                                                       |
| pickle_pure_python               | 139 us                                                   | 140 us: 1.00x slower                                                        |
| 2to3                             | 114 ms                                                   | 115 ms: 1.00x slower                                                        |
| sympy_expand                     | 167 ms                                                   | 168 ms: 1.01x slower                                                        |
| shortest_path                    | 219 ms                                                   | 225 ms: 1.03x slower                                                        |
| connected_components             | 201 ms                                                   | 208 ms: 1.04x slower                                                        |
| meteor_contest                   | 47.7 ms                                                  | 49.6 ms: 1.04x slower                                                       |
| bench_mp_pool                    | 39.7 ms                                                  | 42.8 ms: 1.08x slower                                                       |
| django_template                  | 13.6 ms                                                  | 14.8 ms: 1.08x slower                                                       |
| python_startup                   | 8.01 ms                                                  | 8.70 ms: 1.09x slower                                                       |
| telco                            | 2.61 ms                                                  | 2.89 ms: 1.11x slower                                                       |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 250 ms: 1.18x slower                                                        |
| many_optionals                   | 195 us                                                   | 231 us: 1.18x slower                                                        |
| python_startup_no_site           | 5.71 ms                                                  | 6.74 ms: 1.18x slower                                                       |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 142 ms: 1.26x slower                                                        |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.8 ms: 2.92x slower                                                       |
| Geometric mean                   | (ref)                                                    | 1.19x faster                                                                |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (14) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, coverage, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20261119-3.16.0a2+dev-b09a7e9/bm-20261119-macm4pro-arm64-python-b09a7e92fb0ab958a52a-3.16.0a2+dev-b09a7e9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.190x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.09x

# Memory
- memory change: 1.15x