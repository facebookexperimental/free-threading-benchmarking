# Results vs. 3.12.6

- fork: python
- ref: 151d1bfd1bb7ca9a36bb
- machine: darwin-arm64
- commit hash: 151d1bf
- commit date: 2025-03-26
- overall geometric mean: 1.014x faster
- HPT reliability: 82.48%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 120 ms: 1.05x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.11 sec: 1.08x slower                                                   |
| html5lib       | 23.0 ms                                                  | 24.2 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.04x slower                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 275 ms: 1.80x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 277 ms: 1.73x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 279 ms: 1.65x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 275 ms: 1.62x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 115 ms: 1.49x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 121 ms: 1.47x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 158 ms: 1.46x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 161 ms: 1.39x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 274 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 273 ms: 1.22x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 11.8 ms: 1.15x faster                                                    |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 118 ms: 1.12x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.2 ms: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 196 ms: 1.03x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 252 ms: 1.19x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 140 ms: 1.24x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.9 ms: 2.95x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.17x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 34.9 ms: 1.09x faster                                                    |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                     |
| nbody          | 54.2 ms                                                  | 57.3 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.00x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.1 ms: 1.06x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 52.8 ms: 1.03x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 10.3 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 67.9 ms                                                  | 63.7 ms: 1.07x faster                                                    |
| xml_etree_iterparse  | 51.6 ms                                                  | 49.2 ms: 1.05x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 39.3 ms: 1.01x slower                                                    |
| tomli_loads          | 957 ms                                                   | 976 ms: 1.02x slower                                                     |
| xml_etree_process    | 26.7 ms                                                  | 28.8 ms: 1.08x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.7 us: 1.08x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 113 us: 1.10x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 154 us: 1.11x slower                                                     |
| json_dumps           | 4.26 ms                                                  | 5.28 ms: 1.24x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.05x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.82 ms: 1.10x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.53 ms: 1.14x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.12x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.8 ms: 1.09x slower                                                    |
| mako            | 4.77 ms                                                  | 5.27 ms: 1.10x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.7 ms: 1.12x slower                                                    |
| django_template | 13.6 ms                                                  | 17.2 ms: 1.26x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.14x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.33 ms: 2.22x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 275 ms: 1.80x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 277 ms: 1.73x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 279 ms: 1.65x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 275 ms: 1.62x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 115 ms: 1.49x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 121 ms: 1.47x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 158 ms: 1.46x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 161 ms: 1.39x faster                                                     |
| deepcopy                         | 161 us                                                   | 118 us: 1.37x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 13.9 us: 1.31x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 274 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 273 ms: 1.22x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.24 us: 1.18x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.8 ms: 1.17x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.16x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.56 us: 1.15x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 11.8 ms: 1.15x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                     |
| k_core                           | 1.12 sec                                                 | 996 ms: 1.12x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 118 ms: 1.12x faster                                                     |
| float                            | 37.9 ms                                                  | 34.9 ms: 1.09x faster                                                    |
| raytrace                         | 145 ms                                                   | 134 ms: 1.09x faster                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.91 ms: 1.08x faster                                                    |
| go                               | 70.0 ms                                                  | 65.0 ms: 1.08x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 63.7 ms: 1.07x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.2 ms: 1.06x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.1 ms: 1.06x faster                                                    |
| pylint                           | 128 ms                                                   | 122 ms: 1.05x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 48.5 ns: 1.05x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 49.2 ms: 1.05x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 11.8 ms: 1.05x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 52.8 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 39.1 ms: 1.02x faster                                                    |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.22 sec: 1.01x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 143 ms: 1.01x slower                                                     |
| sqlalchemy_declarative           | 46.8 ms                                                  | 47.2 ms: 1.01x slower                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 39.3 ms: 1.01x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 46.2 ms: 1.01x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 2.61 us: 1.01x slower                                                    |
| logging_format                   | 2.80 us                                                  | 2.85 us: 1.02x slower                                                    |
| scimark_sor                      | 61.0 ms                                                  | 62.1 ms: 1.02x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 976 ms: 1.02x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 58.7 ms: 1.02x slower                                                    |
| deltablue                        | 1.73 ms                                                  | 1.77 ms: 1.02x slower                                                    |
| chaos                            | 28.9 ms                                                  | 29.8 ms: 1.03x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 196 ms: 1.03x slower                                                     |
| shortest_path                    | 219 ms                                                   | 226 ms: 1.03x slower                                                     |
| sympy_str                        | 104 ms                                                   | 107 ms: 1.03x slower                                                     |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                     |
| mdp                              | 1.09 sec                                                 | 1.13 sec: 1.04x slower                                                   |
| pyflate                          | 216 ms                                                   | 225 ms: 1.04x slower                                                     |
| connected_components             | 201 ms                                                   | 210 ms: 1.04x slower                                                     |
| html5lib                         | 23.0 ms                                                  | 24.2 ms: 1.05x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 440 us: 1.05x slower                                                     |
| 2to3                             | 114 ms                                                   | 120 ms: 1.05x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.9 ms: 1.05x slower                                                    |
| nqueens                          | 43.5 ms                                                  | 45.8 ms: 1.05x slower                                                    |
| pycparser                        | 497 ms                                                   | 524 ms: 1.05x slower                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 8.45 ms: 1.05x slower                                                    |
| nbody                            | 54.2 ms                                                  | 57.3 ms: 1.06x slower                                                    |
| json                             | 1.93 ms                                                  | 2.05 ms: 1.06x slower                                                    |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.54 ms: 1.07x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.15 ms: 1.07x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 10.3 ms: 1.07x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 180 ms: 1.08x slower                                                     |
| xml_etree_process                | 26.7 ms                                                  | 28.8 ms: 1.08x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.7 us: 1.08x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.29 ms: 1.08x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.11 sec: 1.08x slower                                                   |
| genshi_xml                       | 21.8 ms                                                  | 23.8 ms: 1.09x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 55.9 ms: 1.09x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 113 us: 1.10x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 42.7 ms: 1.10x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 52.5 ms: 1.10x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.82 ms: 1.10x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.27 ms: 1.10x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 28.0 ms: 1.10x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 154 us: 1.11x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 927 us: 1.12x slower                                                     |
| richards                         | 22.4 ms                                                  | 25.0 ms: 1.12x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.7 ms: 1.12x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.53 ms: 1.14x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 376 ms: 1.15x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 764 ms: 1.15x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 252 ms: 1.19x slower                                                     |
| fannkuch                         | 176 ms                                                   | 209 ms: 1.19x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 140 ms: 1.24x slower                                                     |
| json_dumps                       | 4.26 ms                                                  | 5.28 ms: 1.24x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.4 ms: 1.24x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.28 ms: 1.26x slower                                                    |
| django_template                  | 13.6 ms                                                  | 17.2 ms: 1.26x slower                                                    |
| many_optionals                   | 195 us                                                   | 252 us: 1.29x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 94.9 ms: 2.95x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.02x faster                                                             |

Benchmark hidden because not significant (4): sphinx, thrift, sqlite_synth, typing_runtime_protocols
Ignored benchmarks (8) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250326-3.14.0a6+-151d1bf/bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.014x faster

# HPT report

- Reliability score: 82.48% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.12x