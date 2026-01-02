# Results vs. 3.13.0rc2

- fork: python
- ref: e5ad7b7694c47555e3ea
- machine: darwin-arm64
- commit hash: e5ad7b7
- commit date: 2026-01-01
- overall geometric mean: 1.075x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 113 ms: 1.01x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                   |
| html5lib       | 23.1 ms                                                        | 22.8 ms: 1.02x faster                                                    |
| sphinx         | 409 ms                                                         | 393 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 222 ms: 2.34x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 227 ms: 2.31x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 225 ms: 1.80x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 235 ms: 1.64x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.36x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.32x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 139 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 252 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 248 ms: 1.18x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.8 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.2 ms: 2.77x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.21x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.2 ms: 1.15x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 45.1 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.84 ms: 1.09x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 45.4 ms: 1.06x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 98.0 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.89 ms: 1.20x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.5 ms: 1.14x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 933 ms: 1.07x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 34.7 ms: 1.03x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.7 ms: 1.03x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 98.6 us: 1.01x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 62.7 ms: 1.00x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 140 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.04x faster                                                             |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.82 ms: 1.02x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.35 ms: 1.07x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.75 ms: 1.02x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 21.1 ms: 1.01x faster                                                    |
| mako            | 4.41 ms                                                        | 4.63 ms: 1.05x slower                                                    |
| django_template | 12.5 ms                                                        | 14.9 ms: 1.20x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.05x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 222 ms: 2.34x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 227 ms: 2.31x faster                                                     |
| mdp                              | 1.06 sec                                                       | 547 ms: 1.93x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 225 ms: 1.80x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 235 ms: 1.64x faster                                                     |
| k_core                           | 1.46 sec                                                       | 903 ms: 1.62x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.04 ms: 1.55x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.3 us: 1.46x faster                                                    |
| deepcopy                         | 145 us                                                         | 102 us: 1.43x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 102 ms: 1.39x faster                                                     |
| go                               | 72.6 ms                                                        | 53.0 ms: 1.37x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.36x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 100 ms: 1.32x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 139 ms: 1.32x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 50.1 ms: 1.28x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.06 us: 1.22x faster                                                    |
| pyflate                          | 222 ms                                                         | 184 ms: 1.20x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.89 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 252 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 248 ms: 1.18x faster                                                     |
| float                            | 31.4 ms                                                        | 27.2 ms: 1.15x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 106 ms: 1.15x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.5 ms: 1.14x faster                                                    |
| richards                         | 22.1 ms                                                        | 20.0 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 176 ms: 1.10x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.80 ms: 1.10x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 22.6 ms: 1.09x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.84 ms: 1.09x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.6 ms: 1.08x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 924 us: 1.08x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.99 sec: 1.07x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 933 ms: 1.07x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.1 ms: 1.06x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 40.8 ms: 1.06x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 615 ms: 1.06x faster                                                     |
| regex_compile                    | 47.9 ms                                                        | 45.4 ms: 1.06x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 305 ms: 1.06x faster                                                     |
| fannkuch                         | 179 ms                                                         | 170 ms: 1.05x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                    |
| sphinx                           | 409 ms                                                         | 393 ms: 1.04x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 62.5 us: 1.03x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 120 ms: 1.03x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 34.7 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.77 ms: 1.03x faster                                                    |
| json                             | 1.94 ms                                                        | 1.89 ms: 1.03x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.7 ms: 1.03x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.75 ms: 1.02x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.40 ms: 1.02x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.8 ms: 1.02x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.1 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| pycparser                        | 470 ms                                                         | 465 ms: 1.01x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 98.6 us: 1.01x faster                                                    |
| shortest_path                    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| connected_components             | 208 ms                                                         | 207 ms: 1.01x faster                                                     |
| logging_simple                   | 2.24 us                                                        | 2.23 us: 1.00x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 62.7 ms: 1.00x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 44.0 ms: 1.01x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.47 us: 1.01x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.07 ms: 1.01x slower                                                    |
| 2to3                             | 112 ms                                                         | 113 ms: 1.01x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.81 ms: 1.02x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 41.4 ns: 1.02x slower                                                    |
| coverage                         | 31.2 ms                                                        | 31.9 ms: 1.02x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.82 ms: 1.02x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 978 ns: 1.03x slower                                                     |
| chaos                            | 24.3 ms                                                        | 25.1 ms: 1.03x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 98.0 ms: 1.04x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 49.7 ms: 1.04x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 44.5 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 428 us: 1.04x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 7.08 us: 1.04x slower                                                    |
| raytrace                         | 109 ms                                                         | 114 ms: 1.05x slower                                                     |
| mako                             | 4.41 ms                                                        | 4.63 ms: 1.05x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 100 ms: 1.05x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 55.2 ms: 1.06x slower                                                    |
| nbody                            | 42.5 ms                                                        | 45.1 ms: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 170 ms: 1.07x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.35 ms: 1.07x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 39.8 ms: 1.07x slower                                                    |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 140 us: 1.08x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 36.6 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.6 ms: 1.18x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.9 ms: 1.20x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.4 ms: 1.20x slower                                                    |
| many_optionals                   | 200 us                                                         | 256 us: 1.27x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 80.2 ms: 2.77x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmark hidden because not significant (3): thrift, json_loads, deltablue
Ignored benchmarks (12) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: asyncio_websockets, chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260101-3.15.0a3+-e5ad7b7/bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.075x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.19x