# Results vs. 3.13.0rc2

- fork: python
- ref: 151d1bfd1bb7ca9a36bb
- machine: darwin-arm64
- commit hash: 151d1bf
- commit date: 2025-03-26
- overall geometric mean: 1.132x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 141 ms: 1.27x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.09 sec: 1.05x slower                                                   |
| html5lib       | 23.1 ms                                                        | 26.1 ms: 1.13x slower                                                    |
| sphinx         | 409 ms                                                         | 454 ms: 1.11x slower                                                     |
| Geometric mean | (ref)                                                          | 1.13x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 234 ms: 2.22x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 250 ms: 2.10x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 240 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 259 ms: 1.49x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 143 ms: 1.30x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 252 ms: 1.20x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 156 ms: 1.18x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 125 ms: 1.14x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 263 ms: 1.12x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| async_generators                 | 193 ms                                                         | 200 ms: 1.03x slower                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 127 ms: 1.04x slower                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 238 ms: 1.06x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| coroutines                       | 10.8 ms                                                        | 13.5 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.25x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 60.9 ms: 1.41x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.2 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| float          | 31.4 ms                                                        | 38.6 ms: 1.23x slower                                                    |
| nbody          | 42.5 ms                                                        | 75.3 ms: 1.77x slower                                                    |
| Geometric mean | (ref)                                                          | 1.28x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.72 ms: 1.10x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 92.6 ms: 1.02x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 65.6 ms: 1.37x slower                                                    |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 41.1 ms: 1.12x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 57.0 ms: 1.09x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.8 us: 1.09x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.26 ms: 1.13x slower                                                    |
| tomli_loads          | 1000 ms                                                        | 1.14 sec: 1.14x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 43.3 ms: 1.21x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 32.6 ms: 1.29x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 183 us: 1.41x slower                                                     |
| unpickle_pure_python | 99.5 us                                                        | 143 us: 1.44x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.15x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.25 ms: 1.07x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.29 ms: 1.23x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 29.2 ms: 1.37x slower                                                    |
| mako            | 4.41 ms                                                        | 6.36 ms: 1.44x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 14.8 ms: 1.49x slower                                                    |
| django_template | 12.5 ms                                                        | 19.5 ms: 1.56x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.46x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 234 ms: 2.22x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 934 us: 2.19x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 250 ms: 2.10x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 505 us: 1.97x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 240 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 259 ms: 1.49x faster                                                     |
| k_core                           | 1.46 sec                                                       | 1.07 sec: 1.37x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 143 ms: 1.30x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 106 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 252 ms: 1.20x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 156 ms: 1.18x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 125 ms: 1.14x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.1 ms: 1.12x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 263 ms: 1.12x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.72 ms: 1.10x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 57.0 ms: 1.09x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 874 ns: 1.08x faster                                                     |
| pidigits                         | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 92.6 ms: 1.02x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 190 ms: 1.02x faster                                                     |
| deepcopy                         | 145 us                                                         | 146 us: 1.00x slower                                                     |
| async_generators                 | 193 ms                                                         | 200 ms: 1.03x slower                                                     |
| dulwich_log                      | 19.8 ms                                                        | 20.5 ms: 1.03x slower                                                    |
| json                             | 1.94 ms                                                        | 2.01 ms: 1.04x slower                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 127 ms: 1.04x slower                                                     |
| docutils                         | 1.05 sec                                                       | 1.09 sec: 1.05x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 238 ms: 1.06x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 9.25 ms: 1.07x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 40.7 ms: 1.08x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.8 us: 1.09x slower                                                    |
| pathlib                          | 11.1 ms                                                        | 12.1 ms: 1.09x slower                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.36 sec: 1.11x slower                                                   |
| sphinx                           | 409 ms                                                         | 454 ms: 1.11x slower                                                     |
| go                               | 72.6 ms                                                        | 81.2 ms: 1.12x slower                                                    |
| pyflate                          | 222 ms                                                         | 250 ms: 1.13x slower                                                     |
| shortest_path                    | 225 ms                                                         | 253 ms: 1.13x slower                                                     |
| html5lib                         | 23.1 ms                                                        | 26.1 ms: 1.13x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 5.26 ms: 1.13x slower                                                    |
| tomli_loads                      | 1000 ms                                                        | 1.14 sec: 1.14x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 239 ms: 1.15x slower                                                     |
| connected_components             | 208 ms                                                         | 240 ms: 1.15x slower                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 19.0 us: 1.15x slower                                                    |
| scimark_sor                      | 64.0 ms                                                        | 73.9 ms: 1.16x slower                                                    |
| pycparser                        | 470 ms                                                         | 544 ms: 1.16x slower                                                     |
| mdp                              | 1.06 sec                                                       | 1.22 sec: 1.16x slower                                                   |
| thrift                           | 309 us                                                         | 365 us: 1.18x slower                                                     |
| telco                            | 3.07 ms                                                        | 3.66 ms: 1.19x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 53.4 ms: 1.20x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 43.3 ms: 1.21x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 6.10 ms: 1.22x slower                                                    |
| pylint                           | 106 ms                                                         | 129 ms: 1.22x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.29 ms: 1.23x slower                                                    |
| float                            | 31.4 ms                                                        | 38.6 ms: 1.23x slower                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.61 us: 1.24x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 13.5 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.25x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 60.1 ms: 1.26x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 66.1 ms: 1.26x slower                                                    |
| 2to3                             | 112 ms                                                         | 141 ms: 1.27x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 9.61 ms: 1.28x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 32.6 ms: 1.29x slower                                                    |
| coverage                         | 31.2 ms                                                        | 40.6 ms: 1.30x slower                                                    |
| fannkuch                         | 179 ms                                                         | 234 ms: 1.31x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 162 ms: 1.31x slower                                                     |
| many_optionals                   | 200 us                                                         | 265 us: 1.32x slower                                                     |
| richards                         | 22.1 ms                                                        | 29.3 ms: 1.33x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 127 ms: 1.33x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 215 ms: 1.35x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 33.4 ms: 1.35x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 87.9 us: 1.36x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 29.2 ms: 1.37x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 65.6 ms: 1.37x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.47 ms: 1.39x slower                                                    |
| logging_format                   | 2.45 us                                                        | 3.42 us: 1.40x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 61.4 ms: 1.40x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 183 us: 1.41x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 60.9 ms: 1.41x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 3.17 us: 1.42x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 42.6 ms: 1.43x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 53.2 ms: 1.43x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 143 us: 1.44x slower                                                     |
| mako                             | 4.41 ms                                                        | 6.36 ms: 1.44x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 59.3 ns: 1.46x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 14.8 ms: 1.49x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 4.28 ms: 1.50x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 50.9 ms: 1.51x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 490 ms: 1.52x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 994 ms: 1.53x slower                                                     |
| generators                       | 15.7 ms                                                        | 24.0 ms: 1.53x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 635 us: 1.54x slower                                                     |
| chaos                            | 24.3 ms                                                        | 37.6 ms: 1.55x slower                                                    |
| django_template                  | 12.5 ms                                                        | 19.5 ms: 1.56x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 66.8 ms: 1.56x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 2.27 ms: 1.57x slower                                                    |
| raytrace                         | 109 ms                                                         | 171 ms: 1.57x slower                                                     |
| subparsers                       | 6.26 ms                                                        | 9.93 ms: 1.59x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 11.0 us: 1.61x slower                                                    |
| nbody                            | 42.5 ms                                                        | 75.3 ms: 1.77x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.2 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.16x slower                                                             |
Ignored benchmarks (9) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250326-3.14.0a6+-151d1bf-NOGIL/bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.132x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.09x

# Memory
- memory change: 1.18x