# Results vs. 3.12.6

- fork: python
- ref: e5ad7b7694c47555e3ea
- machine: darwin-arm64
- commit hash: e5ad7b7
- commit date: 2026-01-01
- overall geometric mean: 1.084x faster
- HPT reliability: 95.20%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| html5lib       | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                    |
| sphinx         | 434 ms                                                   | 429 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x slower                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 239 ms: 2.01x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 251 ms: 1.97x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 252 ms: 1.82x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 247 ms: 1.80x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.63x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.46x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.31x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.15x faster                                                     |
| async_generators                 | 206 ms                                                   | 185 ms: 1.12x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.02x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.0 ms: 1.03x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.3 ms: 2.93x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.23x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                    |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                     |
| nbody          | 54.2 ms                                                  | 56.8 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 51.2 ms: 1.07x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.1 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.30 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.8 ms: 1.26x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 61.1 ms: 1.11x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 4.00 ms: 1.07x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.1 ms: 1.01x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 109 us: 1.06x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| tomli_loads          | 957 ms                                                   | 1.01 sec: 1.06x slower                                                   |
| pickle_pure_python   | 139 us                                                   | 148 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.90 ms: 1.24x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.18 ms: 1.26x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.25x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                    |
| genshi_xml      | 21.8 ms                                                  | 23.8 ms: 1.09x slower                                                    |
| django_template | 13.6 ms                                                  | 15.9 ms: 1.17x slower                                                    |
| mako            | 4.77 ms                                                  | 5.61 ms: 1.17x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.13x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.19 ms: 4.96x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 817 us: 2.46x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 239 ms: 2.01x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 251 ms: 1.97x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 252 ms: 1.82x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 247 ms: 1.80x faster                                                     |
| mdp                              | 1.09 sec                                                 | 614 ms: 1.78x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.63x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 513 us: 1.62x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.46x faster                                                     |
| deepcopy                         | 161 us                                                   | 111 us: 1.45x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.6 us: 1.45x faster                                                    |
| float                            | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 259 ms: 1.31x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.30x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.8 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.20 us: 1.22x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 42.9 ns: 1.19x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.34 us: 1.18x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 822 ns: 1.18x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.15x faster                                                     |
| go                               | 70.0 ms                                                  | 60.7 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 53.8 ms: 1.13x faster                                                    |
| raytrace                         | 145 ms                                                   | 128 ms: 1.13x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.9 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                   |
| async_generators                 | 206 ms                                                   | 185 ms: 1.12x faster                                                     |
| k_core                           | 1.12 sec                                                 | 1.00 sec: 1.12x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 127 ms: 1.12x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 61.1 ms: 1.11x faster                                                    |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 50.2 ms: 1.08x faster                                                    |
| pylint                           | 128 ms                                                   | 120 ms: 1.07x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 51.2 ms: 1.07x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.00 ms: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 471 ms: 1.06x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.64 ms: 1.05x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 95.1 ms: 1.05x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.46 us: 1.04x faster                                                    |
| generators                       | 21.9 ms                                                  | 21.1 ms: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.30 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.02x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.75 us: 1.02x faster                                                    |
| chaos                            | 28.9 ms                                                  | 28.4 ms: 1.02x faster                                                    |
| sphinx                           | 434 ms                                                   | 429 ms: 1.01x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 43.8 ms: 1.01x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 71.5 us: 1.01x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.1 ms: 1.01x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.7 ms: 1.02x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.16 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 335 ms: 1.02x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.13 ms: 1.02x slower                                                    |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.0 ms: 1.03x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 689 ms: 1.04x slower                                                     |
| json                             | 1.93 ms                                                  | 2.01 ms: 1.04x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.8 ms: 1.05x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.19 ms: 1.05x slower                                                    |
| thrift                           | 322 us                                                   | 339 us: 1.05x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 109 us: 1.06x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 1.01 sec: 1.06x slower                                                   |
| sympy_sum                        | 57.6 ms                                                  | 61.0 ms: 1.06x slower                                                    |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.06x slower                                                     |
| richards                         | 22.4 ms                                                  | 23.8 ms: 1.06x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 148 us: 1.06x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 27.1 ms: 1.07x slower                                                    |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 41.9 ms: 1.08x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.8 ms: 1.09x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 59.0 ms: 1.15x slower                                                    |
| shortest_path                    | 219 ms                                                   | 253 ms: 1.16x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.04 ms: 1.17x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.9 ms: 1.17x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.61 ms: 1.17x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 56.1 ms: 1.18x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 46.9 ms: 1.18x slower                                                    |
| connected_components             | 201 ms                                                   | 246 ms: 1.23x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.90 ms: 1.24x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.18 ms: 1.26x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 550 us: 1.31x slower                                                     |
| many_optionals                   | 195 us                                                   | 271 us: 1.39x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.7 ms: 1.44x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.3 ms: 2.93x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (3): fannkuch, asyncio_websockets, docutils
Ignored benchmarks (11) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260101-3.15.0a3+-e5ad7b7-NOGIL/bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.084x faster

# HPT report

- Reliability score: 95.20% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.34x