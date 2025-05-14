# Results vs. 3.13.0rc2

- fork: python
- ref: 9ad0c7b0f14c5fcda6bf
- machine: darwin-arm64
- commit hash: 9ad0c7b
- commit date: 2025-05-13
- overall geometric mean: 1.009x faster
- HPT reliability: 65.30%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| html5lib       | 23.1 ms                                                        | 25.8 ms: 1.12x slower                                                   |
| sphinx         | 409 ms                                                         | 419 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 250 ms: 2.10x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 255 ms: 2.04x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 254 ms: 1.60x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 258 ms: 1.50x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.26x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 263 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.09x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.8 ms: 1.01x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.9 ms: 3.04x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 30.5 ms: 1.03x faster                                                   |
| pidigits       | 166 ms                                                         | 165 ms: 1.00x faster                                                    |
| nbody          | 42.5 ms                                                        | 50.9 ms: 1.20x slower                                                   |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.58 ms: 1.02x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 49.6 ms: 1.04x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 102 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 44.4 ms: 1.04x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 970 ms: 1.03x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 62.7 ms: 1.01x slower                                                   |
| json_dumps           | 4.65 ms                                                        | 4.68 ms: 1.01x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 101 us: 1.01x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 36.6 ms: 1.02x slower                                                   |
| xml_etree_process    | 25.4 ms                                                        | 26.0 ms: 1.02x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.7 us: 1.08x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.70 ms: 1.01x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.21 ms: 1.04x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.0 ms: 1.03x slower                                                   |
| genshi_text     | 9.97 ms                                                        | 10.3 ms: 1.03x slower                                                   |
| mako            | 4.41 ms                                                        | 4.86 ms: 1.10x slower                                                   |
| django_template | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.10x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 250 ms: 2.10x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 255 ms: 2.04x faster                                                    |
| mdp                              | 1.06 sec                                                       | 535 ms: 1.98x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 254 ms: 1.60x faster                                                    |
| k_core                           | 1.46 sec                                                       | 962 ms: 1.52x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 258 ms: 1.50x faster                                                    |
| deepcopy                         | 145 us                                                         | 112 us: 1.29x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.7 us: 1.29x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.26x faster                                                    |
| go                               | 72.6 ms                                                        | 57.9 ms: 1.25x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 149 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 52.2 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 263 ms: 1.15x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.16 us: 1.11x faster                                                   |
| pyflate                          | 222 ms                                                         | 201 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.09x faster                                                    |
| async_generators                 | 193 ms                                                         | 177 ms: 1.09x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.2 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| create_gc_cycles                 | 993 us                                                         | 933 us: 1.06x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 10.1 ms: 1.06x faster                                                   |
| connected_components             | 208 ms                                                         | 200 ms: 1.04x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.4 ms: 1.04x faster                                                   |
| shortest_path                    | 225 ms                                                         | 217 ms: 1.03x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 970 ms: 1.03x faster                                                    |
| float                            | 31.4 ms                                                        | 30.5 ms: 1.03x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.58 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.01x faster                                                    |
| thrift                           | 309 us                                                         | 305 us: 1.01x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.7 ms: 1.01x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.8 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 165 ms: 1.00x faster                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 30.0 ms: 1.00x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 2.86 ms: 1.00x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 62.7 ms: 1.01x slower                                                   |
| json_dumps                       | 4.65 ms                                                        | 4.68 ms: 1.01x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 8.70 ms: 1.01x slower                                                   |
| richards                         | 22.1 ms                                                        | 22.3 ms: 1.01x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| sympy_integrate                  | 7.53 ms                                                        | 7.63 ms: 1.01x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 101 us: 1.01x slower                                                    |
| pathlib                          | 11.1 ms                                                        | 11.3 ms: 1.02x slower                                                   |
| json                             | 1.94 ms                                                        | 1.97 ms: 1.02x slower                                                   |
| gc_traversal                     | 2.04 ms                                                        | 2.08 ms: 1.02x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 25.2 ms: 1.02x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 36.6 ms: 1.02x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 26.0 ms: 1.02x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 666 ms: 1.02x slower                                                    |
| sphinx                           | 409 ms                                                         | 419 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 331 ms: 1.03x slower                                                    |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.0 ms: 1.03x slower                                                   |
| genshi_text                      | 9.97 ms                                                        | 10.3 ms: 1.03x slower                                                   |
| regex_compile                    | 47.9 ms                                                        | 49.6 ms: 1.04x slower                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 67.1 us: 1.04x slower                                                   |
| fannkuch                         | 179 ms                                                         | 186 ms: 1.04x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.51 ms: 1.04x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.21 ms: 1.04x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.9 ms: 1.04x slower                                                   |
| coverage                         | 31.2 ms                                                        | 33.0 ms: 1.06x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 101 ms: 1.06x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 438 us: 1.06x slower                                                    |
| pycparser                        | 470 ms                                                         | 503 ms: 1.07x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 51.5 ms: 1.08x slower                                                   |
| regex_dna                        | 94.6 ms                                                        | 102 ms: 1.08x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.7 us: 1.08x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 56.9 ms: 1.09x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 48.1 ms: 1.10x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.96 ms: 1.10x slower                                                   |
| mako                             | 4.41 ms                                                        | 4.86 ms: 1.10x slower                                                   |
| raytrace                         | 109 ms                                                         | 120 ms: 1.11x slower                                                    |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.0 ms: 1.11x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 25.8 ms: 1.12x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.6 ms: 1.12x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 48.0 ms: 1.12x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 38.0 ms: 1.13x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 7.82 us: 1.15x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 44.0 ms: 1.16x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.86 us: 1.17x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.63 us: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                    |
| nbody                            | 42.5 ms                                                        | 50.9 ms: 1.20x slower                                                   |
| many_optionals                   | 200 us                                                         | 249 us: 1.24x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.7 ms: 1.26x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.80 ms: 1.56x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.9 ms: 3.04x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 196 ns: 4.82x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x slower                                                            |

Benchmark hidden because not significant (2): telco, sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250513-3.15.0a0-9ad0c7b/bm-20250513-macm4pro-arm64-python-9ad0c7b0f14c5fcda6bf-3.15.0a0-9ad0c7b.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.009x faster

# HPT report

- Reliability score: 65.30% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.09x