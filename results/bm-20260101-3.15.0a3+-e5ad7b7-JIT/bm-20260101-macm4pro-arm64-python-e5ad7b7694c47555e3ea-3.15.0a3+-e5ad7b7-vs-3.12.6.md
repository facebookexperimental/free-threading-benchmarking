# Results vs. 3.12.6

- fork: python
- ref: e5ad7b7694c47555e3ea
- machine: darwin-arm64
- commit hash: e5ad7b7
- commit date: 2026-01-01
- overall geometric mean: 1.255x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 110 ms: 1.04x faster                                                     |
| docutils       | 1.02 sec                                                 | 994 ms: 1.03x faster                                                     |
| html5lib       | 23.0 ms                                                  | 19.9 ms: 1.16x faster                                                    |
| sphinx         | 434 ms                                                   | 386 ms: 1.12x faster                                                     |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 219 ms: 2.26x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 222 ms: 2.16x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 217 ms: 2.06x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 229 ms: 2.00x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 98.2 ms: 1.81x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 97.3 ms: 1.77x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.71x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 136 ms: 1.63x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 247 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 252 ms: 1.34x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.25x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 38.2 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.05x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.4 ms: 2.44x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.37x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 23.0 ms: 1.65x faster                                                    |
| nbody          | 54.2 ms                                                  | 39.8 ms: 1.36x faster                                                    |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                    | 1.31x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 39.5 ms: 1.38x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.15x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.2 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.14x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| unpickle_pure_python | 103 us                                                   | 71.8 us: 1.43x faster                                                    |
| xml_etree_iterparse  | 51.6 ms                                                  | 36.2 ms: 1.42x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 30.8 ms: 1.26x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 111 us: 1.25x faster                                                     |
| xml_etree_process    | 26.7 ms                                                  | 21.8 ms: 1.23x faster                                                    |
| tomli_loads          | 957 ms                                                   | 795 ms: 1.20x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.66 ms: 1.16x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 59.2 ms: 1.15x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.01x faster                                                    |
| Geometric mean       | (ref)                                                    | 1.23x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.73 ms: 1.09x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.29 ms: 1.10x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 3.89 ms: 1.23x faster                                                    |
| genshi_text     | 10.5 ms                                                  | 9.09 ms: 1.15x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.4 ms: 1.02x faster                                                    |
| django_template | 13.6 ms                                                  | 13.9 ms: 1.02x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.09x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.87 ms: 5.37x faster                                                    |
| richards                         | 22.4 ms                                                  | 9.59 ms: 2.34x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 219 ms: 2.26x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 11.6 ms: 2.19x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 222 ms: 2.16x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 217 ms: 2.06x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 229 ms: 2.00x faster                                                     |
| mdp                              | 1.09 sec                                                 | 577 ms: 1.89x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 98.2 ms: 1.81x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 97.3 ms: 1.77x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.71x faster                                                     |
| deepcopy                         | 161 us                                                   | 97.1 us: 1.66x faster                                                    |
| float                            | 37.9 ms                                                  | 23.0 ms: 1.65x faster                                                    |
| go                               | 70.0 ms                                                  | 42.7 ms: 1.64x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 136 ms: 1.63x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.4 us: 1.61x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.18 us: 1.59x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.12 ms: 1.54x faster                                                    |
| pyflate                          | 216 ms                                                   | 142 ms: 1.52x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 33.7 ns: 1.51x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 41.7 ms: 1.46x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.00 us: 1.45x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 71.8 us: 1.43x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 22.5 ms: 1.43x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 99.2 ms: 1.43x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 36.2 ms: 1.42x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 36.1 ms: 1.42x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 39.5 ms: 1.38x faster                                                    |
| raytrace                         | 145 ms                                                   | 106 ms: 1.37x faster                                                     |
| nbody                            | 54.2 ms                                                  | 39.8 ms: 1.36x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 247 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 252 ms: 1.34x faster                                                     |
| chaos                            | 28.9 ms                                                  | 21.8 ms: 1.33x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 41.1 ms: 1.32x faster                                                    |
| k_core                           | 1.12 sec                                                 | 862 ms: 1.30x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 516 ms: 1.29x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 257 ms: 1.28x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 30.7 ms: 1.27x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 30.8 ms: 1.26x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.25x faster                                                     |
| pickle_pure_python               | 139 us                                                   | 111 us: 1.25x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.07 us: 1.24x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 21.8 ms: 1.23x faster                                                    |
| mako                             | 4.77 ms                                                  | 3.89 ms: 1.23x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.83 sec: 1.23x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.29 us: 1.22x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 795 ms: 1.20x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.4 ms: 1.19x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 38.2 ms: 1.19x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.60 ms: 1.17x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.66 ms: 1.16x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 19.9 ms: 1.16x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.15x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.09 ms: 1.15x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 61.8 us: 1.15x faster                                                    |
| pycparser                        | 497 ms                                                   | 433 ms: 1.15x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 59.2 ms: 1.15x faster                                                    |
| fannkuch                         | 176 ms                                                   | 153 ms: 1.15x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.7 ms: 1.14x faster                                                    |
| async_generators                 | 206 ms                                                   | 182 ms: 1.13x faster                                                     |
| thrift                           | 322 us                                                   | 285 us: 1.13x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 38.7 ms: 1.12x faster                                                    |
| sphinx                           | 434 ms                                                   | 386 ms: 1.12x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.41 ms: 1.08x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.92 ms: 1.08x faster                                                    |
| meteor_contest                   | 47.7 ms                                                  | 44.8 ms: 1.07x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                     |
| pylint                           | 128 ms                                                   | 121 ms: 1.06x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 94.2 ms: 1.06x faster                                                    |
| json                             | 1.93 ms                                                  | 1.84 ms: 1.05x faster                                                    |
| 2to3                             | 114 ms                                                   | 110 ms: 1.04x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 55.9 ms: 1.03x faster                                                    |
| docutils                         | 1.02 sec                                                 | 994 ms: 1.03x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.4 ms: 1.02x faster                                                    |
| connected_components             | 201 ms                                                   | 197 ms: 1.02x faster                                                     |
| shortest_path                    | 219 ms                                                   | 215 ms: 1.02x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.01x faster                                                    |
| telco                            | 2.61 ms                                                  | 2.58 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| sympy_str                        | 104 ms                                                   | 103 ms: 1.01x faster                                                     |
| django_template                  | 13.6 ms                                                  | 13.9 ms: 1.02x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 428 us: 1.02x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.05 ms: 1.02x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 173 ms: 1.04x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.05x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.73 ms: 1.09x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 913 us: 1.10x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.29 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.13x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 44.8 ms: 1.13x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.8 ms: 1.26x slower                                                    |
| many_optionals                   | 195 us                                                   | 252 us: 1.29x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.4 ms: 2.44x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                             |

Benchmark hidden because not significant (2): sqlite_synth, regex_v8
Ignored benchmarks (12) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: asyncio_websockets, chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260101-3.15.0a3+-e5ad7b7-JIT/bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.255x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.18x
- 95% likely to have a speedup of 1.16x
- 99% likely to have a speedup of 1.14x

# Memory
- memory change: 1.26x