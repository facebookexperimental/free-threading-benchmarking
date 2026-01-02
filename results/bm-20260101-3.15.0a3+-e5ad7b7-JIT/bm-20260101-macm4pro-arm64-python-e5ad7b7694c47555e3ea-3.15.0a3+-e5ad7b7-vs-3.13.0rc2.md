# Results vs. 3.13.0rc2

- fork: python
- ref: e5ad7b7694c47555e3ea
- machine: darwin-arm64
- commit hash: e5ad7b7
- commit date: 2026-01-01
- overall geometric mean: 1.162x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 110 ms: 1.02x faster                                                     |
| docutils       | 1.05 sec                                                       | 994 ms: 1.05x faster                                                     |
| html5lib       | 23.1 ms                                                        | 19.9 ms: 1.17x faster                                                    |
| sphinx         | 409 ms                                                         | 386 ms: 1.06x faster                                                     |
| Geometric mean | (ref)                                                          | 1.07x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 217 ms: 2.40x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 219 ms: 2.39x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 222 ms: 1.83x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 229 ms: 1.69x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 98.2 ms: 1.45x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.37x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 97.3 ms: 1.36x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 252 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 247 ms: 1.19x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 38.2 ms: 1.13x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.4 ms: 2.71x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.23x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 23.0 ms: 1.37x faster                                                    |
| nbody          | 42.5 ms                                                        | 39.8 ms: 1.07x faster                                                    |
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                          | 1.15x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 39.5 ms: 1.21x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.61 ms: 1.11x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 94.2 ms: 1.00x faster                                                    |
| Geometric mean | (ref)                                                          | 1.11x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| unpickle_pure_python | 99.5 us                                                        | 71.8 us: 1.39x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 36.2 ms: 1.27x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.66 ms: 1.27x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 795 ms: 1.26x faster                                                     |
| pickle_pure_python   | 130 us                                                         | 111 us: 1.17x faster                                                     |
| xml_etree_process    | 25.4 ms                                                        | 21.8 ms: 1.17x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 30.8 ms: 1.16x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 59.2 ms: 1.05x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| Geometric mean       | (ref)                                                          | 1.19x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.73 ms: 1.01x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.29 ms: 1.06x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 3.89 ms: 1.13x faster                                                    |
| genshi_text     | 9.97 ms                                                        | 9.09 ms: 1.10x faster                                                    |
| django_template | 12.5 ms                                                        | 13.9 ms: 1.11x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.03x faster                                                             |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 217 ms: 2.40x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 219 ms: 2.39x faster                                                     |
| richards                         | 22.1 ms                                                        | 9.59 ms: 2.30x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 11.6 ms: 2.13x faster                                                    |
| mdp                              | 1.06 sec                                                       | 577 ms: 1.83x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 222 ms: 1.83x faster                                                     |
| go                               | 72.6 ms                                                        | 42.7 ms: 1.70x faster                                                    |
| k_core                           | 1.46 sec                                                       | 862 ms: 1.70x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 229 ms: 1.69x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.87 ms: 1.62x faster                                                    |
| pyflate                          | 222 ms                                                         | 142 ms: 1.56x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 41.7 ms: 1.54x faster                                                    |
| deepcopy                         | 145 us                                                         | 97.1 us: 1.49x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 98.2 ms: 1.45x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.4 us: 1.44x faster                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 71.8 us: 1.39x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 135 ms: 1.37x faster                                                     |
| float                            | 31.4 ms                                                        | 23.0 ms: 1.37x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 97.3 ms: 1.36x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 136 ms: 1.35x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 22.5 ms: 1.33x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.12 ms: 1.30x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.00 us: 1.29x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 36.2 ms: 1.27x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.66 ms: 1.27x faster                                                    |
| pprint_pformat                   | 650 ms                                                         | 516 ms: 1.26x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 795 ms: 1.26x faster                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 257 ms: 1.25x faster                                                     |
| scimark_fft                      | 124 ms                                                         | 99.2 ms: 1.25x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 39.5 ms: 1.21x faster                                                    |
| logging_silent                   | 40.6 ns                                                        | 33.7 ns: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 252 ms: 1.20x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.58 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 247 ms: 1.19x faster                                                     |
| scimark_lu                       | 42.8 ms                                                        | 36.1 ms: 1.18x faster                                                    |
| pickle_pure_python               | 130 us                                                         | 111 us: 1.17x faster                                                     |
| fannkuch                         | 179 ms                                                         | 153 ms: 1.17x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 21.8 ms: 1.17x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 19.9 ms: 1.17x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.83 sec: 1.16x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 30.8 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| mako                             | 4.41 ms                                                        | 3.89 ms: 1.13x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 38.2 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| chaos                            | 24.3 ms                                                        | 21.8 ms: 1.12x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.61 ms: 1.11x faster                                                    |
| comprehensions                   | 6.80 us                                                        | 6.18 us: 1.10x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.09 ms: 1.10x faster                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 30.7 ms: 1.10x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.60 ms: 1.09x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 913 us: 1.09x faster                                                     |
| pycparser                        | 470 ms                                                         | 433 ms: 1.09x faster                                                     |
| thrift                           | 309 us                                                         | 285 us: 1.08x faster                                                     |
| logging_simple                   | 2.24 us                                                        | 2.07 us: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| meteor_contest                   | 47.9 ms                                                        | 44.8 ms: 1.07x faster                                                    |
| nbody                            | 42.5 ms                                                        | 39.8 ms: 1.07x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.29 us: 1.07x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 41.1 ms: 1.06x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                    |
| async_generators                 | 193 ms                                                         | 182 ms: 1.06x faster                                                     |
| sphinx                           | 409 ms                                                         | 386 ms: 1.06x faster                                                     |
| json                             | 1.94 ms                                                        | 1.84 ms: 1.06x faster                                                    |
| connected_components             | 208 ms                                                         | 197 ms: 1.05x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 59.2 ms: 1.05x faster                                                    |
| docutils                         | 1.05 sec                                                       | 994 ms: 1.05x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 61.8 us: 1.05x faster                                                    |
| shortest_path                    | 225 ms                                                         | 215 ms: 1.04x faster                                                     |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 218 ms: 1.03x faster                                                     |
| raytrace                         | 109 ms                                                         | 106 ms: 1.03x faster                                                     |
| 2to3                             | 112 ms                                                         | 110 ms: 1.02x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.41 ms: 1.02x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.7 us: 1.01x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 94.2 ms: 1.00x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.73 ms: 1.01x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 963 ns: 1.02x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 38.7 ms: 1.04x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 428 us: 1.04x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.29 ms: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 55.9 ms: 1.07x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.92 ms: 1.08x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.8 ms: 1.08x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 103 ms: 1.08x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 173 ms: 1.09x slower                                                     |
| django_template                  | 12.5 ms                                                        | 13.9 ms: 1.11x slower                                                    |
| pylint                           | 106 ms                                                         | 121 ms: 1.15x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.4 ms: 1.17x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.8 ms: 1.18x slower                                                    |
| many_optionals                   | 200 us                                                         | 252 us: 1.26x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 78.4 ms: 2.71x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.16x faster                                                             |

Benchmark hidden because not significant (2): genshi_xml, gc_traversal
Ignored benchmarks (12) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: asyncio_websockets, chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260101-3.15.0a3+-e5ad7b7-JIT/bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.162x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.21x