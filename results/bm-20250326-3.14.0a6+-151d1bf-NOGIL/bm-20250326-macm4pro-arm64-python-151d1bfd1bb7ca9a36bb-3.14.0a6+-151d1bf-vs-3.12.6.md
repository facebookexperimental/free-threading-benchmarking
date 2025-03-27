# Results vs. 3.12.6

- fork: python
- ref: 151d1bfd1bb7ca9a36bb
- machine: darwin-arm64
- commit hash: 151d1bf
- commit date: 2025-03-26
- overall geometric mean: 1.065x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 141 ms: 1.24x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.09 sec: 1.07x slower                                                   |
| html5lib       | 23.0 ms                                                  | 26.1 ms: 1.13x slower                                                    |
| sphinx         | 434 ms                                                   | 454 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                    | 1.12x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 240 ms: 2.00x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 250 ms: 1.98x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 234 ms: 1.90x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 259 ms: 1.78x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 143 ms: 1.61x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 156 ms: 1.43x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 125 ms: 1.42x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 252 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 263 ms: 1.27x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 127 ms: 1.04x faster                                                     |
| async_generators                 | 206 ms                                                   | 200 ms: 1.03x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 13.5 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 238 ms: 1.03x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.12x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 60.9 ms: 1.34x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.2 ms: 2.90x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.19x faster                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| float          | 37.9 ms                                                  | 38.6 ms: 1.02x slower                                                    |
| nbody          | 54.2 ms                                                  | 75.3 ms: 1.39x slower                                                    |
| Geometric mean | (ref)                                                    | 1.12x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.16x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 92.6 ms: 1.08x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.72 ms: 1.01x slower                                                    |
| regex_compile  | 54.6 ms                                                  | 65.6 ms: 1.20x slower                                                    |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 41.1 ms: 1.25x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 57.0 ms: 1.19x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.8 us: 1.08x slower                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 43.3 ms: 1.11x slower                                                    |
| tomli_loads          | 957 ms                                                   | 1.14 sec: 1.19x slower                                                   |
| xml_etree_process    | 26.7 ms                                                  | 32.6 ms: 1.22x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 5.26 ms: 1.23x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 183 us: 1.32x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 143 us: 1.39x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.25 ms: 1.15x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.29 ms: 1.28x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 6.36 ms: 1.33x slower                                                    |
| genshi_xml      | 21.8 ms                                                  | 29.2 ms: 1.34x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 14.8 ms: 1.42x slower                                                    |
| django_template | 13.6 ms                                                  | 19.5 ms: 1.43x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.38x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 934 us: 2.15x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 9.93 ms: 2.09x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 240 ms: 2.00x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 250 ms: 1.98x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 234 ms: 1.90x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 259 ms: 1.78x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 505 us: 1.64x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 143 ms: 1.61x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 156 ms: 1.43x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 125 ms: 1.42x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 252 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 263 ms: 1.27x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 41.1 ms: 1.25x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 57.0 ms: 1.19x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.16x faster                                                    |
| deepcopy                         | 161 us                                                   | 146 us: 1.11x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 874 ns: 1.11x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 92.6 ms: 1.08x faster                                                    |
| k_core                           | 1.12 sec                                                 | 1.07 sec: 1.05x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 20.5 ms: 1.04x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 127 ms: 1.04x faster                                                     |
| async_generators                 | 206 ms                                                   | 200 ms: 1.03x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 12.1 ms: 1.02x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 13.5 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.72 ms: 1.01x slower                                                    |
| float                            | 37.9 ms                                                  | 38.6 ms: 1.02x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 40.7 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 238 ms: 1.03x slower                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 19.0 us: 1.04x slower                                                    |
| json                             | 1.93 ms                                                  | 2.01 ms: 1.04x slower                                                    |
| sphinx                           | 434 ms                                                   | 454 ms: 1.05x slower                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.36 sec: 1.05x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.09 sec: 1.07x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.8 us: 1.08x slower                                                    |
| pycparser                        | 497 ms                                                   | 544 ms: 1.09x slower                                                     |
| generators                       | 21.9 ms                                                  | 24.0 ms: 1.10x slower                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.61 us: 1.10x slower                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 43.3 ms: 1.11x slower                                                    |
| comprehensions                   | 9.84 us                                                  | 11.0 us: 1.11x slower                                                    |
| mdp                              | 1.09 sec                                                 | 1.22 sec: 1.12x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 239 ms: 1.12x slower                                                     |
| spectral_norm                    | 54.4 ms                                                  | 61.4 ms: 1.13x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 26.1 ms: 1.13x slower                                                    |
| thrift                           | 322 us                                                   | 365 us: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                     |
| sqlalchemy_declarative           | 46.8 ms                                                  | 53.4 ms: 1.14x slower                                                    |
| scimark_fft                      | 142 ms                                                   | 162 ms: 1.14x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 66.1 ms: 1.15x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.25 ms: 1.15x slower                                                    |
| shortest_path                    | 219 ms                                                   | 253 ms: 1.16x slower                                                     |
| pyflate                          | 216 ms                                                   | 250 ms: 1.16x slower                                                     |
| go                               | 70.0 ms                                                  | 81.2 ms: 1.16x slower                                                    |
| logging_silent                   | 50.9 ns                                                  | 59.3 ns: 1.17x slower                                                    |
| raytrace                         | 145 ms                                                   | 171 ms: 1.18x slower                                                     |
| sqlalchemy_imperative            | 5.17 ms                                                  | 6.10 ms: 1.18x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 1.14 sec: 1.19x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.47 ms: 1.19x slower                                                    |
| connected_components             | 201 ms                                                   | 240 ms: 1.20x slower                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 9.61 ms: 1.20x slower                                                    |
| regex_compile                    | 54.6 ms                                                  | 65.6 ms: 1.20x slower                                                    |
| scimark_sor                      | 61.0 ms                                                  | 73.9 ms: 1.21x slower                                                    |
| sympy_str                        | 104 ms                                                   | 127 ms: 1.22x slower                                                     |
| xml_etree_process                | 26.7 ms                                                  | 32.6 ms: 1.22x slower                                                    |
| logging_format                   | 2.80 us                                                  | 3.42 us: 1.22x slower                                                    |
| nqueens                          | 43.5 ms                                                  | 53.2 ms: 1.22x slower                                                    |
| logging_simple                   | 2.57 us                                                  | 3.17 us: 1.23x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 5.26 ms: 1.23x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 87.9 us: 1.24x slower                                                    |
| 2to3                             | 114 ms                                                   | 141 ms: 1.24x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 60.1 ms: 1.26x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.29 ms: 1.28x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 215 ms: 1.29x slower                                                     |
| chaos                            | 28.9 ms                                                  | 37.6 ms: 1.30x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 66.8 ms: 1.30x slower                                                    |
| richards                         | 22.4 ms                                                  | 29.3 ms: 1.31x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 50.9 ms: 1.31x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 183 us: 1.32x slower                                                     |
| deltablue                        | 1.73 ms                                                  | 2.27 ms: 1.32x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 33.4 ms: 1.32x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 42.6 ms: 1.32x slower                                                    |
| mako                             | 4.77 ms                                                  | 6.36 ms: 1.33x slower                                                    |
| fannkuch                         | 176 ms                                                   | 234 ms: 1.33x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 60.9 ms: 1.34x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 29.2 ms: 1.34x slower                                                    |
| many_optionals                   | 195 us                                                   | 265 us: 1.36x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 143 us: 1.39x slower                                                     |
| nbody                            | 54.2 ms                                                  | 75.3 ms: 1.39x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.66 ms: 1.40x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 4.28 ms: 1.41x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 14.8 ms: 1.42x slower                                                    |
| django_template                  | 13.6 ms                                                  | 19.5 ms: 1.43x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 490 ms: 1.49x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 994 ms: 1.50x slower                                                     |
| coverage                         | 26.9 ms                                                  | 40.6 ms: 1.51x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 635 us: 1.52x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.2 ms: 2.90x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.07x slower                                                             |

Benchmark hidden because not significant (2): asyncio_websockets, pylint
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250326-3.14.0a6+-151d1bf-NOGIL/bm-20250326-macm4pro-arm64-python-151d1bfd1bb7ca9a36bb-3.14.0a6+-151d1bf.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.065x slower

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.22x