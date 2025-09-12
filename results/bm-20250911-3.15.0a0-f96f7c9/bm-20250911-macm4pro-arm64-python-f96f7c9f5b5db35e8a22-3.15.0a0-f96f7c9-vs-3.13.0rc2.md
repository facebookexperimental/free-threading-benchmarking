# Results vs. 3.13.0rc2

- fork: python
- ref: f96f7c9f5b5db35e8a22
- machine: darwin-arm64
- commit hash: f96f7c9
- commit date: 2025-09-11
- overall geometric mean: 1.025x faster
- HPT reliability: 90.05%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.2 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 252 ms: 2.08x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.07x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 253 ms: 1.60x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 253 ms: 1.53x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 264 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 9.89 ms: 1.09x faster                                                   |
| async_generators                 | 193 ms                                                         | 179 ms: 1.08x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 42.2 ms: 1.02x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.0 ms: 3.04x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 29.8 ms: 1.05x faster                                                   |
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| nbody          | 42.5 ms                                                        | 47.6 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                          | 1.02x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.85 ms: 1.09x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 48.2 ms: 1.01x slower                                                   |
| regex_dna      | 94.6 ms                                                        | 97.6 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.80 ms: 1.22x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 890 ms: 1.12x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.6 ms: 1.03x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 61.3 ms: 1.02x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                   |
| unpickle_pure_python | 99.5 us                                                        | 98.9 us: 1.01x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 143 us: 1.10x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.69 ms: 1.01x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 6.23 ms: 1.05x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.80 ms: 1.02x faster                                                   |
| genshi_xml      | 21.4 ms                                                        | 21.4 ms: 1.00x slower                                                   |
| mako            | 4.41 ms                                                        | 4.91 ms: 1.11x slower                                                   |
| django_template | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.08x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 252 ms: 2.08x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 252 ms: 2.07x faster                                                    |
| mdp                              | 1.06 sec                                                       | 539 ms: 1.96x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 253 ms: 1.60x faster                                                    |
| k_core                           | 1.46 sec                                                       | 954 ms: 1.53x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 253 ms: 1.53x faster                                                    |
| deepcopy                         | 145 us                                                         | 105 us: 1.39x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 12.1 us: 1.36x faster                                                   |
| go                               | 72.6 ms                                                        | 55.6 ms: 1.30x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 50.0 ms: 1.28x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 148 ms: 1.25x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 149 ms: 1.23x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.80 ms: 1.22x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.11 us: 1.17x faster                                                   |
| pyflate                          | 222 ms                                                         | 195 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 264 ms: 1.14x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 890 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 111 ms: 1.10x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.0 ms: 1.10x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.80 ms: 1.10x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 9.89 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                  |
| regex_v8                         | 10.7 ms                                                        | 9.85 ms: 1.09x faster                                                   |
| async_generators                 | 193 ms                                                         | 179 ms: 1.08x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 935 us: 1.06x faster                                                    |
| float                            | 31.4 ms                                                        | 29.8 ms: 1.05x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                   |
| richards                         | 22.1 ms                                                        | 21.2 ms: 1.04x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 62.4 us: 1.04x faster                                                   |
| connected_components             | 208 ms                                                         | 201 ms: 1.03x faster                                                    |
| shortest_path                    | 225 ms                                                         | 217 ms: 1.03x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.6 ms: 1.03x faster                                                   |
| logging_silent                   | 40.6 ns                                                        | 39.5 ns: 1.03x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 24.0 ms: 1.03x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 42.2 ms: 1.02x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 35.1 ms: 1.02x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.79 ms: 1.02x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 61.3 ms: 1.02x faster                                                   |
| genshi_text                      | 9.97 ms                                                        | 9.80 ms: 1.02x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 29.4 ms: 1.02x faster                                                   |
| xml_etree_process                | 25.4 ms                                                        | 25.1 ms: 1.01x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.47 ms: 1.01x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 98.9 us: 1.01x faster                                                   |
| spectral_norm                    | 43.7 ms                                                        | 43.5 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 522 ms: 1.01x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 21.4 ms: 1.00x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 653 ms: 1.01x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 48.2 ms: 1.01x slower                                                   |
| python_startup                   | 8.63 ms                                                        | 8.69 ms: 1.01x slower                                                   |
| json_loads                       | 10.8 us                                                        | 10.9 us: 1.01x slower                                                   |
| thrift                           | 309 us                                                         | 312 us: 1.01x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 958 ns: 1.01x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.01x slower                                                  |
| gc_traversal                     | 2.04 ms                                                        | 2.07 ms: 1.01x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.50 us: 1.02x slower                                                   |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 97.6 ms: 1.03x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.31 us: 1.03x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 38.6 ms: 1.04x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 427 us: 1.04x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.51 ms: 1.04x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.2 ms: 1.05x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 6.23 ms: 1.05x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 100 ms: 1.05x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.8 ms: 1.05x slower                                                   |
| pycparser                        | 470 ms                                                         | 495 ms: 1.05x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 131 ms: 1.06x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 50.7 ms: 1.06x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 169 ms: 1.06x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.90 ms: 1.07x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 56.0 ms: 1.07x slower                                                   |
| chaos                            | 24.3 ms                                                        | 26.1 ms: 1.07x slower                                                   |
| pylint                           | 106 ms                                                         | 114 ms: 1.08x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 7.38 us: 1.08x slower                                                   |
| raytrace                         | 109 ms                                                         | 118 ms: 1.09x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 143 us: 1.10x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.91 ms: 1.11x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 42.3 ms: 1.12x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.6 ms: 1.12x slower                                                   |
| nbody                            | 42.5 ms                                                        | 47.6 ms: 1.12x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 37.9 ms: 1.13x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 48.2 ms: 1.13x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.5 ms: 1.24x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 131 ms: 1.28x slower                                                    |
| many_optionals                   | 200 us                                                         | 323 us: 1.61x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 17.4 ms: 2.79x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 88.0 ms: 3.04x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (5): json, sphinx, async_tree_eager_cpu_io_mixed, pprint_safe_repr, fannkuch
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250911-3.15.0a0-f96f7c9/bm-20250911-macm4pro-arm64-python-f96f7c9f5b5db35e8a22-3.15.0a0-f96f7c9.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.025x faster

# HPT report

- Reliability score: 90.05% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x