# Results vs. 3.13.0rc2

- fork: python
- ref: 151d1bfd1bb7ca9a36bb
- machine: darwin-arm64
- commit hash: 151d1bf
- commit date: 2025-03-26
- overall geometric mean: 1.058x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 120 ms: 1.07x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.11 sec: 1.06x slower                                                   |
| html5lib       | 23.1 ms                                                        | 24.2 ms: 1.04x slower                                                    |
| sphinx         | 409 ms                                                         | 432 ms: 1.06x slower                                                     |
| Geometric mean | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 275 ms: 1.91x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 275 ms: 1.90x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 277 ms: 1.46x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 279 ms: 1.38x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 158 ms: 1.18x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 121 ms: 1.18x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 115 ms: 1.15x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 161 ms: 1.15x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 274 ms: 1.10x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 273 ms: 1.08x faster                                                     |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 118 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                     |
| asyncio_websockets               | 194 ms                                                         | 196 ms: 1.01x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.2 ms: 1.07x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 11.8 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 252 ms: 1.21x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 140 ms: 1.36x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.9 ms: 3.28x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 166 ms: 1.00x slower                                                     |
| float          | 31.4 ms                                                        | 34.9 ms: 1.11x slower                                                    |
| nbody          | 42.5 ms                                                        | 57.3 ms: 1.35x slower                                                    |
| Geometric mean | (ref)                                                          | 1.14x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 94.1 ms: 1.01x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 52.8 ms: 1.10x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 976 ms: 1.02x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 63.7 ms: 1.02x slower                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 49.2 ms: 1.07x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.7 us: 1.08x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 39.3 ms: 1.10x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 28.8 ms: 1.13x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 113 us: 1.14x slower                                                     |
| json_dumps           | 4.65 ms                                                        | 5.28 ms: 1.14x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 154 us: 1.18x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.09x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.82 ms: 1.02x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.53 ms: 1.10x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.06x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.8 ms: 1.11x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.7 ms: 1.18x slower                                                    |
| mako            | 4.41 ms                                                        | 5.27 ms: 1.19x slower                                                    |
| django_template | 12.5 ms                                                        | 17.2 ms: 1.38x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.21x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 275 ms: 1.91x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 275 ms: 1.90x faster                                                     |
| k_core                           | 1.46 sec                                                       | 996 ms: 1.47x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 277 ms: 1.46x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 279 ms: 1.38x faster                                                     |
| deepcopy                         | 145 us                                                         | 118 us: 1.23x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 13.9 us: 1.18x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 158 ms: 1.18x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 121 ms: 1.18x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 115 ms: 1.15x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 161 ms: 1.15x faster                                                     |
| go                               | 72.6 ms                                                        | 65.0 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.47 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 274 ms: 1.10x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 273 ms: 1.08x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 927 us: 1.07x faster                                                     |
| async_generators                 | 193 ms                                                         | 183 ms: 1.06x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.24 us: 1.05x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 10.3 ms: 1.04x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 118 ms: 1.03x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 62.1 ms: 1.03x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 976 ms: 1.02x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 94.1 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                     |
| pidigits                         | 166 ms                                                         | 166 ms: 1.00x slower                                                     |
| shortest_path                    | 225 ms                                                         | 226 ms: 1.00x slower                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 226 ms: 1.01x slower                                                     |
| connected_components             | 208 ms                                                         | 210 ms: 1.01x slower                                                     |
| asyncio_websockets               | 194 ms                                                         | 196 ms: 1.01x slower                                                     |
| pyflate                          | 222 ms                                                         | 225 ms: 1.01x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.82 ms: 1.02x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 63.7 ms: 1.02x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 972 ns: 1.03x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 39.1 ms: 1.03x slower                                                    |
| thrift                           | 309 us                                                         | 322 us: 1.04x slower                                                     |
| html5lib                         | 23.1 ms                                                        | 24.2 ms: 1.04x slower                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.22 sec: 1.04x slower                                                   |
| json                             | 1.94 ms                                                        | 2.05 ms: 1.05x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.15 ms: 1.06x slower                                                    |
| sphinx                           | 409 ms                                                         | 432 ms: 1.06x slower                                                     |
| docutils                         | 1.05 sec                                                       | 1.11 sec: 1.06x slower                                                   |
| pathlib                          | 11.1 ms                                                        | 11.8 ms: 1.06x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 47.2 ms: 1.06x slower                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 49.2 ms: 1.07x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 440 us: 1.07x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.2 ms: 1.07x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.28 ms: 1.07x slower                                                    |
| mdp                              | 1.06 sec                                                       | 1.13 sec: 1.07x slower                                                   |
| coverage                         | 31.2 ms                                                        | 33.4 ms: 1.07x slower                                                    |
| 2to3                             | 112 ms                                                         | 120 ms: 1.07x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.91 ms: 1.08x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.7 us: 1.08x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 52.5 ms: 1.10x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.53 ms: 1.10x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 11.8 ms: 1.10x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 39.3 ms: 1.10x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 52.8 ms: 1.10x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 71.4 us: 1.10x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.54 ms: 1.11x slower                                                    |
| float                            | 31.4 ms                                                        | 34.9 ms: 1.11x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.8 ms: 1.11x slower                                                    |
| pycparser                        | 470 ms                                                         | 524 ms: 1.11x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 8.45 ms: 1.12x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 58.7 ms: 1.12x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 107 ms: 1.13x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 180 ms: 1.13x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.9 ms: 1.13x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 28.8 ms: 1.13x slower                                                    |
| richards                         | 22.1 ms                                                        | 25.0 ms: 1.13x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 28.0 ms: 1.14x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 113 us: 1.14x slower                                                     |
| json_dumps                       | 4.65 ms                                                        | 5.28 ms: 1.14x slower                                                    |
| pylint                           | 106 ms                                                         | 122 ms: 1.15x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.29 ms: 1.16x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 143 ms: 1.16x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.61 us: 1.17x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.85 us: 1.17x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 376 ms: 1.17x slower                                                     |
| fannkuch                         | 179 ms                                                         | 209 ms: 1.17x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 51.2 ms: 1.17x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.7 ms: 1.18x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 764 ms: 1.18x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 154 us: 1.18x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 48.5 ns: 1.19x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.27 ms: 1.19x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.8 ms: 1.20x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 252 ms: 1.21x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.77 ms: 1.22x slower                                                    |
| chaos                            | 24.3 ms                                                        | 29.8 ms: 1.23x slower                                                    |
| raytrace                         | 109 ms                                                         | 134 ms: 1.23x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 45.8 ms: 1.23x slower                                                    |
| many_optionals                   | 200 us                                                         | 252 us: 1.26x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 8.56 us: 1.26x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.7 ms: 1.27x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 55.9 ms: 1.31x slower                                                    |
| nbody                            | 42.5 ms                                                        | 57.3 ms: 1.35x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 140 ms: 1.36x slower                                                     |
| django_template                  | 12.5 ms                                                        | 17.2 ms: 1.38x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.33 ms: 1.49x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 94.9 ms: 3.28x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.06x slower                                                             |
Ignored benchmarks (8) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250326-3.14.0a6+-151d1bf/bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.058x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.07x