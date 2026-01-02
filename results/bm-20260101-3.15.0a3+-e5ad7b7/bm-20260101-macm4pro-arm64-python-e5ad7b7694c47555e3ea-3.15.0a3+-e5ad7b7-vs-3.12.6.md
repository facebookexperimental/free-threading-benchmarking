# Results vs. 3.12.6

- fork: python
- ref: e5ad7b7694c47555e3ea
- machine: darwin-arm64
- commit hash: e5ad7b7
- commit date: 2026-01-01
- overall geometric mean: 1.160x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                    |
| sphinx         | 434 ms                                                   | 393 ms: 1.10x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 227 ms: 2.18x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 225 ms: 2.13x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 222 ms: 2.01x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 235 ms: 1.96x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.74x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 100 ms: 1.72x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.69x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 139 ms: 1.60x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 252 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 248 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                     |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.8 ms: 1.12x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.12x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.2 ms: 2.49x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.34x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.2 ms: 1.39x faster                                                    |
| nbody          | 54.2 ms                                                  | 45.1 ms: 1.20x faster                                                    |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                    | 1.18x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 45.4 ms: 1.20x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 98.0 ms: 1.02x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.84 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.5 ms: 1.27x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.7 ms: 1.12x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.89 ms: 1.10x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 62.7 ms: 1.08x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 24.7 ms: 1.08x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 98.6 us: 1.04x faster                                                    |
| tomli_loads          | 957 ms                                                   | 933 ms: 1.03x faster                                                     |
| pickle_pure_python   | 139 us                                                   | 140 us: 1.01x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.82 ms: 1.10x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.35 ms: 1.11x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.75 ms: 1.08x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.1 ms: 1.03x faster                                                    |
| mako            | 4.77 ms                                                  | 4.63 ms: 1.03x faster                                                    |
| django_template | 13.6 ms                                                  | 14.9 ms: 1.10x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.04 ms: 5.15x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 227 ms: 2.18x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 225 ms: 2.13x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 222 ms: 2.01x faster                                                     |
| mdp                              | 1.09 sec                                                 | 547 ms: 2.00x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 235 ms: 1.96x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.74x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 100 ms: 1.72x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 136 ms: 1.69x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.3 us: 1.62x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 139 ms: 1.60x faster                                                     |
| deepcopy                         | 161 us                                                   | 102 us: 1.59x faster                                                     |
| float                            | 37.9 ms                                                  | 27.2 ms: 1.39x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.08 us: 1.39x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.06 us: 1.37x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 252 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 248 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                    |
| go                               | 70.0 ms                                                  | 53.0 ms: 1.32x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.5 ms: 1.27x faster                                                    |
| raytrace                         | 145 ms                                                   | 114 ms: 1.27x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                     |
| k_core                           | 1.12 sec                                                 | 903 ms: 1.24x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 44.0 ms: 1.23x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 41.4 ns: 1.23x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 50.1 ms: 1.22x faster                                                    |
| nbody                            | 54.2 ms                                                  | 45.1 ms: 1.20x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 45.4 ms: 1.20x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.45 ms: 1.19x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 120 ms: 1.18x faster                                                     |
| generators                       | 21.9 ms                                                  | 18.6 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 176 ms: 1.17x faster                                                     |
| pyflate                          | 216 ms                                                   | 184 ms: 1.17x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 27.6 ms: 1.17x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.23 us: 1.15x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 44.5 ms: 1.15x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.1 ms: 1.15x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.81 ms: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.14x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 62.5 us: 1.14x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.47 us: 1.14x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.13x faster                                                   |
| pylint                           | 128 ms                                                   | 114 ms: 1.13x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 22.6 ms: 1.12x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.12x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.7 ms: 1.12x faster                                                    |
| richards                         | 22.4 ms                                                  | 20.0 ms: 1.12x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.8 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                    |
| sphinx                           | 434 ms                                                   | 393 ms: 1.10x faster                                                     |
| hexiom                           | 3.04 ms                                                  | 2.77 ms: 1.10x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.89 ms: 1.10x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 39.8 ms: 1.09x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.40 ms: 1.08x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 62.7 ms: 1.08x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 24.7 ms: 1.08x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 615 ms: 1.08x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 305 ms: 1.08x faster                                                     |
| genshi_text                      | 10.5 ms                                                  | 9.75 ms: 1.08x faster                                                    |
| pycparser                        | 497 ms                                                   | 465 ms: 1.07x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 36.6 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                     |
| thrift                           | 322 us                                                   | 308 us: 1.05x faster                                                     |
| unpickle_pure_python             | 103 us                                                   | 98.6 us: 1.04x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.2 ms: 1.04x faster                                                    |
| sympy_str                        | 104 ms                                                   | 100 ms: 1.04x faster                                                     |
| fannkuch                         | 176 ms                                                   | 170 ms: 1.04x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.1 ms: 1.03x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.63 ms: 1.03x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 933 ms: 1.03x faster                                                     |
| json                             | 1.93 ms                                                  | 1.89 ms: 1.02x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 98.0 ms: 1.02x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 22.8 ms: 1.01x faster                                                    |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                     |
| pickle_pure_python               | 139 us                                                   | 140 us: 1.01x slower                                                     |
| sqlite_synth                     | 967 ns                                                   | 978 ns: 1.01x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 170 ms: 1.02x slower                                                     |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                     |
| shortest_path                    | 219 ms                                                   | 223 ms: 1.02x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 428 us: 1.02x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.84 ms: 1.03x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.07 ms: 1.03x slower                                                    |
| connected_components             | 201 ms                                                   | 207 ms: 1.03x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 49.7 ms: 1.04x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 120 ms: 1.06x slower                                                     |
| telco                            | 2.61 ms                                                  | 2.80 ms: 1.07x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.9 ms: 1.10x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.82 ms: 1.10x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.35 ms: 1.11x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 924 us: 1.11x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.12x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.4 ms: 1.14x slower                                                    |
| coverage                         | 26.9 ms                                                  | 31.9 ms: 1.19x slower                                                    |
| many_optionals                   | 195 us                                                   | 256 us: 1.31x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 80.2 ms: 2.49x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.16x faster                                                             |

Benchmark hidden because not significant (2): json_loads, docutils
Ignored benchmarks (12) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: asyncio_websockets, chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260101-3.15.0a3+-e5ad7b7/bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.160x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.23x