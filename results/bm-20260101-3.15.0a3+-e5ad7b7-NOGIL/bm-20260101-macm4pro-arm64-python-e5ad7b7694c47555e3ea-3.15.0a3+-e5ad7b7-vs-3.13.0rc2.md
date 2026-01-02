# Results vs. 3.13.0rc2

- fork: python
- ref: e5ad7b7694c47555e3ea
- machine: darwin-arm64
- commit hash: e5ad7b7
- commit date: 2026-01-01
- overall geometric mean: 1.005x faster
- HPT reliability: 73.50%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.29x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.09x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.7 ms: 1.03x slower                                                    |
| sphinx         | 409 ms                                                         | 429 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 247 ms: 2.10x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 251 ms: 2.09x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 239 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 252 ms: 1.53x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| async_generators                 | 193 ms                                                         | 185 ms: 1.04x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.0 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.25x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.3 ms: 3.26x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                    |
| nbody          | 42.5 ms                                                        | 56.8 ms: 1.34x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x slower                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.30 ms: 1.15x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 95.1 ms: 1.01x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 51.2 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 4.00 ms: 1.16x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.8 ms: 1.13x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 61.1 ms: 1.02x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 1.01 sec: 1.02x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.1 ms: 1.07x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 109 us: 1.09x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 148 us: 1.14x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.90 ms: 1.15x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.18 ms: 1.21x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.18x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.8 ms: 1.11x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                    |
| mako            | 4.41 ms                                                        | 5.61 ms: 1.27x slower                                                    |
| django_template | 12.5 ms                                                        | 15.9 ms: 1.28x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.20x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 817 us: 2.50x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 247 ms: 2.10x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 251 ms: 2.09x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 513 us: 1.94x faster                                                     |
| mdp                              | 1.06 sec                                                       | 614 ms: 1.72x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 239 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 252 ms: 1.53x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.19 ms: 1.50x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.00 sec: 1.46x faster                                                   |
| deepcopy                         | 145 us                                                         | 111 us: 1.31x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.6 us: 1.30x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 105 ms: 1.26x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.21x faster                                                     |
| go                               | 72.6 ms                                                        | 60.7 ms: 1.19x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 53.8 ms: 1.19x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.00 ms: 1.16x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 259 ms: 1.16x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 822 ns: 1.15x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.30 ms: 1.15x faster                                                    |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.8 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                    |
| float                            | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.20 us: 1.08x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.07x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 18.9 ms: 1.05x faster                                                    |
| async_generators                 | 193 ms                                                         | 185 ms: 1.04x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.03x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 61.1 ms: 1.02x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| fannkuch                         | 179 ms                                                         | 175 ms: 1.02x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.04 ms: 1.01x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 95.1 ms: 1.01x slower                                                    |
| tomli_loads                      | 1000 ms                                                        | 1.01 sec: 1.02x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.7 ms: 1.03x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 127 ms: 1.03x slower                                                     |
| json                             | 1.94 ms                                                        | 2.01 ms: 1.03x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.1 ms: 1.04x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 335 ms: 1.04x slower                                                     |
| sphinx                           | 409 ms                                                         | 429 ms: 1.05x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 42.9 ns: 1.06x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 689 ms: 1.06x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 51.2 ms: 1.07x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.1 ms: 1.07x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.8 ms: 1.08x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.16 ms: 1.08x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 47.0 ms: 1.09x slower                                                    |
| 2to3                             | 112 ms                                                         | 122 ms: 1.09x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.7 ms: 1.09x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 109 us: 1.09x slower                                                     |
| thrift                           | 309 us                                                         | 339 us: 1.10x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 27.1 ms: 1.10x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.46 us: 1.10x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 71.5 us: 1.11x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.8 ms: 1.11x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.19 ms: 1.12x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.75 us: 1.12x slower                                                    |
| shortest_path                    | 225 ms                                                         | 253 ms: 1.13x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.64 ms: 1.13x slower                                                    |
| pylint                           | 106 ms                                                         | 120 ms: 1.14x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 148 us: 1.14x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.90 ms: 1.15x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.2 ms: 1.15x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 61.0 ms: 1.17x slower                                                    |
| chaos                            | 24.3 ms                                                        | 28.4 ms: 1.17x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 56.1 ms: 1.17x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 43.8 ms: 1.17x slower                                                    |
| raytrace                         | 109 ms                                                         | 128 ms: 1.18x slower                                                     |
| connected_components             | 208 ms                                                         | 246 ms: 1.18x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.19x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.13 ms: 1.20x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.18 ms: 1.21x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.34 us: 1.23x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.9 ms: 1.24x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.7 ms: 1.24x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 41.9 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.25x slower                                                     |
| mako                             | 4.41 ms                                                        | 5.61 ms: 1.27x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.9 ms: 1.28x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 550 us: 1.34x slower                                                     |
| nbody                            | 42.5 ms                                                        | 56.8 ms: 1.34x slower                                                    |
| generators                       | 15.7 ms                                                        | 21.1 ms: 1.34x slower                                                    |
| many_optionals                   | 200 us                                                         | 271 us: 1.35x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 59.0 ms: 1.38x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.3 ms: 3.26x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                             |

Benchmark hidden because not significant (3): pidigits, async_tree_eager_cpu_io_mixed, pycparser
Ignored benchmarks (11) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260101-3.15.0a3+-e5ad7b7-NOGIL/bm-20260101-macm4pro-arm64-python-e5ad7b7694c47555e3ea-3.15.0a3+-e5ad7b7.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.005x faster

# HPT report

- Reliability score: 73.50% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.29x