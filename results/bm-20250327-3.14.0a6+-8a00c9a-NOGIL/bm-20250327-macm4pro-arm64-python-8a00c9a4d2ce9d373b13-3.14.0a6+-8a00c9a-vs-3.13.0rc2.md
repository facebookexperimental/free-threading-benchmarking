# Results vs. 3.13.0rc2

- fork: python
- ref: 8a00c9a4d2ce9d373b13
- machine: darwin-arm64
- commit hash: 8a00c9a
- commit date: 2025-03-27
- overall geometric mean: 1.072x slower
- HPT reliability: 99.95%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 131 ms: 1.17x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.05 sec: 1.01x slower                                                   |
| html5lib       | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                    |
| sphinx         | 409 ms                                                         | 440 ms: 1.08x slower                                                     |
| Geometric mean | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 220 ms: 2.37x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 230 ms: 2.28x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 222 ms: 1.82x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 237 ms: 1.63x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.37x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 98.7 ms: 1.34x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 144 ms: 1.28x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 245 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 254 ms: 1.15x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 119 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 230 ms: 1.02x slower                                                     |
| coroutines                       | 10.8 ms                                                        | 11.1 ms: 1.03x slower                                                    |
| async_generators                 | 193 ms                                                         | 201 ms: 1.04x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 233 ms: 1.12x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 122 ms: 1.19x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 55.1 ms: 1.28x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.2 ms: 3.01x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| float          | 31.4 ms                                                        | 35.2 ms: 1.12x slower                                                    |
| nbody          | 42.5 ms                                                        | 73.8 ms: 1.74x slower                                                    |
| Geometric mean | (ref)                                                          | 1.24x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.64 ms: 1.11x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 93.6 ms: 1.01x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 58.7 ms: 1.23x slower                                                    |
| Geometric mean | (ref)                                                          | 1.00x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 40.2 ms: 1.15x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 56.2 ms: 1.11x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 1.06 sec: 1.06x slower                                                   |
| json_loads           | 10.8 us                                                        | 11.8 us: 1.09x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.21 ms: 1.12x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 40.9 ms: 1.14x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 30.4 ms: 1.20x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 126 us: 1.26x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 169 us: 1.30x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.10x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.24 ms: 1.07x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.27 ms: 1.22x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.14x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 26.1 ms: 1.22x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 12.9 ms: 1.29x slower                                                    |
| mako            | 4.41 ms                                                        | 6.10 ms: 1.38x slower                                                    |
| django_template | 12.5 ms                                                        | 18.2 ms: 1.46x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.33x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 220 ms: 2.37x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 230 ms: 2.28x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 925 us: 2.21x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 502 us: 1.98x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 222 ms: 1.82x faster                                                     |
| mdp                              | 1.06 sec                                                       | 636 ms: 1.66x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 237 ms: 1.63x faster                                                     |
| k_core                           | 1.46 sec                                                       | 1.05 sec: 1.40x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 136 ms: 1.37x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 98.7 ms: 1.34x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 144 ms: 1.28x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 114 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 245 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 254 ms: 1.15x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.2 ms: 1.15x faster                                                    |
| deepcopy                         | 145 us                                                         | 127 us: 1.14x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 841 ns: 1.13x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 56.2 ms: 1.11x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.64 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| pidigits                         | 166 ms                                                         | 161 ms: 1.03x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 119 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.02x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 19.5 ms: 1.02x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 93.6 ms: 1.01x faster                                                    |
| go                               | 72.6 ms                                                        | 72.2 ms: 1.01x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.05 sec: 1.01x slower                                                   |
| pyflate                          | 222 ms                                                         | 226 ms: 1.02x slower                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 230 ms: 1.02x slower                                                     |
| json                             | 1.94 ms                                                        | 1.99 ms: 1.03x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 11.1 ms: 1.03x slower                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.19 sec: 1.03x slower                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 17.0 us: 1.03x slower                                                    |
| async_generators                 | 193 ms                                                         | 201 ms: 1.04x slower                                                     |
| html5lib                         | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                    |
| pathlib                          | 11.1 ms                                                        | 11.7 ms: 1.05x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 39.8 ms: 1.05x slower                                                    |
| tomli_loads                      | 1000 ms                                                        | 1.06 sec: 1.06x slower                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.38 us: 1.06x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.24 ms: 1.07x slower                                                    |
| scimark_sor                      | 64.0 ms                                                        | 68.5 ms: 1.07x slower                                                    |
| pycparser                        | 470 ms                                                         | 503 ms: 1.07x slower                                                     |
| sphinx                           | 409 ms                                                         | 440 ms: 1.08x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.8 us: 1.09x slower                                                    |
| shortest_path                    | 225 ms                                                         | 246 ms: 1.10x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 233 ms: 1.12x slower                                                     |
| float                            | 31.4 ms                                                        | 35.2 ms: 1.12x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 5.21 ms: 1.12x slower                                                    |
| connected_components             | 208 ms                                                         | 234 ms: 1.12x slower                                                     |
| sqlalchemy_declarative           | 44.4 ms                                                        | 50.7 ms: 1.14x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 40.9 ms: 1.14x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.56 ms: 1.16x slower                                                    |
| 2to3                             | 112 ms                                                         | 131 ms: 1.17x slower                                                     |
| pylint                           | 106 ms                                                         | 124 ms: 1.18x slower                                                     |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.89 ms: 1.18x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 122 ms: 1.19x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 8.96 ms: 1.19x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 30.4 ms: 1.20x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 63.3 ms: 1.21x slower                                                    |
| fannkuch                         | 179 ms                                                         | 217 ms: 1.22x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.27 ms: 1.22x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 26.1 ms: 1.22x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 58.7 ms: 1.23x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 59.1 ms: 1.23x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 79.9 us: 1.24x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 119 ms: 1.25x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 31.1 ms: 1.26x slower                                                    |
| many_optionals                   | 200 us                                                         | 253 us: 1.26x slower                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 126 us: 1.26x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 202 ms: 1.27x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.84 us: 1.27x slower                                                    |
| richards                         | 22.1 ms                                                        | 28.1 ms: 1.28x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 411 ms: 1.28x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 55.1 ms: 1.28x slower                                                    |
| logging_format                   | 2.45 us                                                        | 3.13 us: 1.28x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 47.7 ms: 1.28x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 837 ms: 1.29x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 12.9 ms: 1.29x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 169 us: 1.30x slower                                                     |
| coverage                         | 31.2 ms                                                        | 40.7 ms: 1.30x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 162 ms: 1.31x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 39.7 ms: 1.33x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.37 ms: 1.33x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 58.7 ms: 1.34x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.86 ms: 1.35x slower                                                    |
| chaos                            | 24.3 ms                                                        | 32.9 ms: 1.36x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 55.9 ns: 1.38x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 46.4 ms: 1.38x slower                                                    |
| mako                             | 4.41 ms                                                        | 6.10 ms: 1.38x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 2.01 ms: 1.38x slower                                                    |
| generators                       | 15.7 ms                                                        | 22.2 ms: 1.42x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 590 us: 1.43x slower                                                     |
| raytrace                         | 109 ms                                                         | 157 ms: 1.45x slower                                                     |
| django_template                  | 12.5 ms                                                        | 18.2 ms: 1.46x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 10.0 us: 1.47x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.35 ms: 1.49x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 64.1 ms: 1.50x slower                                                    |
| nbody                            | 42.5 ms                                                        | 73.8 ms: 1.74x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 87.2 ms: 3.01x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.08x slower                                                             |
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250327-3.14.0a6+-8a00c9a-NOGIL/bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.072x slower

# HPT report

- Reliability score: 99.95% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.18x