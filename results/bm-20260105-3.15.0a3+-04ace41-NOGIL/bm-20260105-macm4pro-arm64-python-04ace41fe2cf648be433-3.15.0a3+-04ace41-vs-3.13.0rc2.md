# Results vs. 3.13.0rc2

- fork: python
- ref: 04ace41fe2cf648be433
- machine: darwin-arm64
- commit hash: 04ace41
- commit date: 2026-01-05
- overall geometric mean: 1.005x faster
- HPT reliability: 73.60%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260105-macm4pro-arm64-python-04ace41fe2cf648be433-3.15.0a3+-04ace41 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 124 ms: 1.11x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.6 ms: 1.02x slower                                                    |
| sphinx         | 409 ms                                                         | 428 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260105-macm4pro-arm64-python-04ace41fe2cf648be433-3.15.0a3+-04ace41 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 250 ms: 2.08x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 253 ms: 2.07x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 240 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 253 ms: 1.53x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.28x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.23x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 154 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 262 ms: 1.15x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 271 ms: 1.09x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.04x faster                                                    |
| async_generators                 | 193 ms                                                         | 188 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 229 ms: 1.02x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.4 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.8 ms: 3.28x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260105-macm4pro-arm64-python-04ace41fe2cf648be433-3.15.0a3+-04ace41 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                    |
| nbody          | 42.5 ms                                                        | 56.7 ms: 1.33x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x slower                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260105-macm4pro-arm64-python-04ace41fe2cf648be433-3.15.0a3+-04ace41 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.41 ms: 1.14x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.50 ms: 1.07x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.5 ms: 1.02x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 51.3 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260105-macm4pro-arm64-python-04ace41fe2cf648be433-3.15.0a3+-04ace41 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 4.01 ms: 1.16x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.0 ms: 1.15x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 882 ms: 1.13x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 62.7 ms: 1.01x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.2 ms: 1.04x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.06x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.2 ms: 1.07x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.10x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 149 us: 1.14x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.00x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260105-macm4pro-arm64-python-04ace41fe2cf648be433-3.15.0a3+-04ace41 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.89 ms: 1.15x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.18 ms: 1.21x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.18x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260105-macm4pro-arm64-python-04ace41fe2cf648be433-3.15.0a3+-04ace41 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.6 ms: 1.11x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                    |
| mako            | 4.41 ms                                                        | 5.51 ms: 1.25x slower                                                    |
| django_template | 12.5 ms                                                        | 15.8 ms: 1.27x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.19x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260105-macm4pro-arm64-python-04ace41fe2cf648be433-3.15.0a3+-04ace41 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 818 us: 2.50x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 250 ms: 2.08x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 253 ms: 2.07x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 516 us: 1.92x faster                                                     |
| mdp                              | 1.06 sec                                                       | 611 ms: 1.73x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 240 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 253 ms: 1.53x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.24 ms: 1.48x faster                                                    |
| k_core                           | 1.46 sec                                                       | 998 ms: 1.47x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.5 us: 1.31x faster                                                    |
| deepcopy                         | 145 us                                                         | 111 us: 1.31x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 146 ms: 1.28x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.25x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 116 ms: 1.23x faster                                                     |
| go                               | 72.6 ms                                                        | 60.4 ms: 1.20x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 154 ms: 1.20x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 54.7 ms: 1.17x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 4.01 ms: 1.16x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.0 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 262 ms: 1.15x faster                                                     |
| pyflate                          | 222 ms                                                         | 194 ms: 1.15x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 828 ns: 1.14x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.41 ms: 1.14x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 882 ms: 1.13x faster                                                     |
| float                            | 31.4 ms                                                        | 28.9 ms: 1.09x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 271 ms: 1.09x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.20 us: 1.08x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.50 ms: 1.07x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.07x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 115 ms: 1.06x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 19.0 ms: 1.05x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.4 ms: 1.04x faster                                                    |
| fannkuch                         | 179 ms                                                         | 174 ms: 1.03x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.03x faster                                                   |
| async_generators                 | 193 ms                                                         | 188 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| telco                            | 3.07 ms                                                        | 3.00 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 62.7 ms: 1.01x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 125 ms: 1.01x slower                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 229 ms: 1.02x slower                                                     |
| html5lib                         | 23.1 ms                                                        | 23.6 ms: 1.02x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.5 ms: 1.02x slower                                                    |
| json                             | 1.94 ms                                                        | 2.00 ms: 1.03x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 37.2 ms: 1.04x slower                                                    |
| sphinx                           | 409 ms                                                         | 428 ms: 1.05x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 338 ms: 1.05x slower                                                     |
| richards                         | 22.1 ms                                                        | 23.2 ms: 1.05x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.06x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.0 ns: 1.06x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 693 ms: 1.07x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 51.3 ms: 1.07x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.2 ms: 1.07x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.6 ms: 1.08x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.15 ms: 1.08x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.4 ms: 1.08x slower                                                    |
| thrift                           | 309 us                                                         | 338 us: 1.09x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.4 ms: 1.10x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.14 ms: 1.10x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.10x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 23.6 ms: 1.11x slower                                                    |
| 2to3                             | 112 ms                                                         | 124 ms: 1.11x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 71.6 us: 1.11x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.48 us: 1.11x slower                                                    |
| shortest_path                    | 225 ms                                                         | 251 ms: 1.12x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.75 us: 1.12x slower                                                    |
| pylint                           | 106 ms                                                         | 119 ms: 1.13x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.65 ms: 1.14x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 149 us: 1.14x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 9.89 ms: 1.15x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 50.9 ms: 1.16x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.17x slower                                                     |
| chaos                            | 24.3 ms                                                        | 28.3 ms: 1.17x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.08 ms: 1.17x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.1 ms: 1.17x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 56.0 ms: 1.17x slower                                                    |
| raytrace                         | 109 ms                                                         | 128 ms: 1.17x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 43.9 ms: 1.18x slower                                                    |
| connected_components             | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 190 ms: 1.19x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 250 ms: 1.20x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.18 ms: 1.21x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.5 ms: 1.23x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.41 us: 1.24x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.9 ms: 1.24x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.51 ms: 1.25x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.2 ms: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                     |
| django_template                  | 12.5 ms                                                        | 15.8 ms: 1.27x slower                                                    |
| nbody                            | 42.5 ms                                                        | 56.7 ms: 1.33x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 551 us: 1.34x slower                                                     |
| generators                       | 15.7 ms                                                        | 21.0 ms: 1.34x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 58.7 ms: 1.37x slower                                                    |
| many_optionals                   | 200 us                                                         | 277 us: 1.38x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.8 ms: 3.28x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                             |

Benchmark hidden because not significant (3): pycparser, pidigits, dask
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260105-3.15.0a3+-04ace41-NOGIL/bm-20260105-macm4pro-arm64-python-04ace41fe2cf648be433-3.15.0a3+-04ace41.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.005x faster

# HPT report

- Reliability score: 73.60% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.30x