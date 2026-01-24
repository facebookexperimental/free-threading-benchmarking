# Results vs. 3.13.0rc2

- fork: python
- ref: 012c498035a9adfe9fd2
- machine: darwin-arm64
- commit hash: 012c498
- commit date: 2026-01-24
- overall geometric mean: 1.164x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| docutils       | 1.05 sec                                                       | 992 ms: 1.06x faster                                                     |
| html5lib       | 23.1 ms                                                        | 19.2 ms: 1.21x faster                                                    |
| sphinx         | 409 ms                                                         | 384 ms: 1.06x faster                                                     |
| Geometric mean | (ref)                                                          | 1.08x faster                                                             |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 217 ms: 2.42x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 217 ms: 2.40x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 217 ms: 1.87x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 226 ms: 1.71x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 96.4 ms: 1.48x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.38x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 96.0 ms: 1.38x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 135 ms: 1.36x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 251 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 245 ms: 1.20x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 37.3 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| async_generators                 | 193 ms                                                         | 183 ms: 1.05x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 238 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.4 ms: 2.67x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.22x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 22.9 ms: 1.37x faster                                                    |
| nbody          | 42.5 ms                                                        | 39.8 ms: 1.07x faster                                                    |
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                          | 1.15x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 47.9 ms                                                        | 40.8 ms: 1.17x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.50 ms: 1.13x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 93.6 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                          | 1.11x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 666 ms: 1.50x faster                                                     |
| unpickle_pure_python | 99.5 us                                                        | 74.0 us: 1.34x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.63 ms: 1.28x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.8 ms: 1.19x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 113 us: 1.15x faster                                                     |
| xml_etree_process    | 25.4 ms                                                        | 22.1 ms: 1.15x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 31.3 ms: 1.14x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 60.5 ms: 1.03x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.5 us: 1.03x faster                                                    |
| Geometric mean       | (ref)                                                          | 1.19x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.77 ms: 1.02x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.32 ms: 1.06x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 3.89 ms: 1.13x faster                                                    |
| genshi_text     | 9.97 ms                                                        | 8.81 ms: 1.13x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 20.7 ms: 1.04x faster                                                    |
| django_template | 12.5 ms                                                        | 13.8 ms: 1.10x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.05x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 217 ms: 2.42x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 217 ms: 2.40x faster                                                     |
| richards                         | 22.1 ms                                                        | 9.33 ms: 2.36x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 11.2 ms: 2.21x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 217 ms: 1.87x faster                                                     |
| mdp                              | 1.06 sec                                                       | 615 ms: 1.72x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 226 ms: 1.71x faster                                                     |
| k_core                           | 1.46 sec                                                       | 859 ms: 1.70x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 38.2 ms: 1.67x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 3.92 ms: 1.60x faster                                                    |
| go                               | 72.6 ms                                                        | 45.7 ms: 1.59x faster                                                    |
| deepcopy                         | 145 us                                                         | 92.8 us: 1.56x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 10.6 us: 1.55x faster                                                    |
| scimark_lu                       | 42.8 ms                                                        | 27.7 ms: 1.54x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 666 ms: 1.50x faster                                                     |
| pyflate                          | 222 ms                                                         | 150 ms: 1.48x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 96.4 ms: 1.48x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 134 ms: 1.38x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 96.0 ms: 1.38x faster                                                    |
| float                            | 31.4 ms                                                        | 22.9 ms: 1.37x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 135 ms: 1.36x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 74.0 us: 1.34x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 983 ns: 1.32x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 22.9 ms: 1.31x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.63 ms: 1.28x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.14 ms: 1.27x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 97.5 ms: 1.27x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 262 ms: 1.23x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 532 ms: 1.22x faster                                                     |
| html5lib                         | 23.1 ms                                                        | 19.2 ms: 1.21x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 251 ms: 1.20x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 245 ms: 1.20x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.8 ms: 1.19x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 40.8 ms: 1.17x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.64 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.84 sec: 1.16x faster                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 37.3 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 105 ms: 1.16x faster                                                     |
| logging_silent                   | 40.6 ns                                                        | 35.3 ns: 1.15x faster                                                    |
| pickle_pure_python               | 130 us                                                         | 113 us: 1.15x faster                                                     |
| xml_etree_process                | 25.4 ms                                                        | 22.1 ms: 1.15x faster                                                    |
| fannkuch                         | 179 ms                                                         | 156 ms: 1.14x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 31.3 ms: 1.14x faster                                                    |
| mako                             | 4.41 ms                                                        | 3.89 ms: 1.13x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 8.81 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.50 ms: 1.13x faster                                                    |
| spectral_norm                    | 43.7 ms                                                        | 39.4 ms: 1.11x faster                                                    |
| chaos                            | 24.3 ms                                                        | 21.9 ms: 1.11x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 910 us: 1.09x faster                                                     |
| pycparser                        | 470 ms                                                         | 433 ms: 1.08x faster                                                     |
| comprehensions                   | 6.80 us                                                        | 6.32 us: 1.08x faster                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 31.4 ms: 1.07x faster                                                    |
| nbody                            | 42.5 ms                                                        | 39.8 ms: 1.07x faster                                                    |
| logging_simple                   | 2.24 us                                                        | 2.09 us: 1.07x faster                                                    |
| sphinx                           | 409 ms                                                         | 384 ms: 1.06x faster                                                     |
| logging_format                   | 2.45 us                                                        | 2.30 us: 1.06x faster                                                    |
| connected_components             | 208 ms                                                         | 197 ms: 1.06x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 992 ms: 1.06x faster                                                     |
| json                             | 1.94 ms                                                        | 1.84 ms: 1.05x faster                                                    |
| async_generators                 | 193 ms                                                         | 183 ms: 1.05x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| hexiom                           | 2.85 ms                                                        | 2.70 ms: 1.05x faster                                                    |
| meteor_contest                   | 47.9 ms                                                        | 45.7 ms: 1.05x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                    |
| nqueens                          | 37.2 ms                                                        | 35.6 ms: 1.05x faster                                                    |
| shortest_path                    | 225 ms                                                         | 216 ms: 1.04x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                     |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 62.2 us: 1.04x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 20.7 ms: 1.04x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 60.5 ms: 1.03x faster                                                    |
| thrift                           | 309 us                                                         | 300 us: 1.03x faster                                                     |
| json_loads                       | 10.8 us                                                        | 10.5 us: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 219 ms: 1.03x faster                                                     |
| raytrace                         | 109 ms                                                         | 106 ms: 1.03x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 93.6 ms: 1.01x faster                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.02 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 521 ms: 1.01x faster                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 7.58 ms: 1.01x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 8.77 ms: 1.02x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 963 ns: 1.02x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 429 us: 1.04x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.86 ms: 1.05x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.8 ms: 1.05x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.32 ms: 1.06x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 56.9 ms: 1.09x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 174 ms: 1.09x slower                                                     |
| django_template                  | 12.5 ms                                                        | 13.8 ms: 1.10x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 106 ms: 1.11x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 238 ms: 1.14x slower                                                     |
| pylint                           | 106 ms                                                         | 121 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 120 ms: 1.17x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.5 ms: 1.18x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.9 ms: 1.19x slower                                                    |
| many_optionals                   | 200 us                                                         | 252 us: 1.26x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.4 ms: 2.67x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.16x faster                                                             |

Benchmark hidden because not significant (1): 2to3
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260124-3.15.0a5+-012c498-JIT/bm-20260124-macm4pro-arm64-python-012c498035a9adfe9fd2-3.15.0a5+-012c498.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.164x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.21x