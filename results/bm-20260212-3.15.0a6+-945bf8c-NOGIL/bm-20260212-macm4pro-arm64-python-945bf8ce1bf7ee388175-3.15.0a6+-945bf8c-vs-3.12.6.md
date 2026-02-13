# Results vs. 3.12.6

- fork: python
- ref: 945bf8ce1bf7ee388175
- machine: darwin-arm64
- commit hash: 945bf8c
- commit date: 2026-02-12
- overall geometric mean: 1.091x faster
- HPT reliability: 99.72%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260212-macm4pro-arm64-python-945bf8ce1bf7ee388175-3.15.0a6+-945bf8c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 120 ms: 1.06x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| html5lib       | 23.0 ms                                                  | 23.2 ms: 1.01x slower                                                    |
| sphinx         | 434 ms                                                   | 424 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260212-macm4pro-arm64-python-945bf8ce1bf7ee388175-3.15.0a6+-945bf8c |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 245 ms: 2.03x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 239 ms: 2.01x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 247 ms: 1.86x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 242 ms: 1.85x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.62x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 143 ms: 1.61x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 150 ms: 1.49x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 256 ms: 1.32x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                     |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.8 ms: 1.03x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.15x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.5 ms: 2.88x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260212-macm4pro-arm64-python-945bf8ce1bf7ee388175-3.15.0a6+-945bf8c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.6 ms: 1.32x faster                                                    |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                     |
| nbody          | 54.2 ms                                                  | 56.6 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260212-macm4pro-arm64-python-945bf8ce1bf7ee388175-3.15.0a6+-945bf8c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.9 ms: 1.07x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.0 ms: 1.04x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.27 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260212-macm4pro-arm64-python-945bf8ce1bf7ee388175-3.15.0a6+-945bf8c |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.8 ms: 1.30x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 60.6 ms: 1.12x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.93 ms: 1.08x faster                                                    |
| tomli_loads          | 957 ms                                                   | 883 ms: 1.08x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 108 us: 1.05x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260212-macm4pro-arm64-python-945bf8ce1bf7ee388175-3.15.0a6+-945bf8c |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.89 ms: 1.23x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.17 ms: 1.26x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.25x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260212-macm4pro-arm64-python-945bf8ce1bf7ee388175-3.15.0a6+-945bf8c |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.8 ms: 1.05x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                    |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                    |
| mako            | 4.77 ms                                                  | 5.52 ms: 1.16x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.10x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260212-macm4pro-arm64-python-945bf8ce1bf7ee388175-3.15.0a6+-945bf8c |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.13 ms: 5.03x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 813 us: 2.47x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 245 ms: 2.03x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 239 ms: 2.01x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 247 ms: 1.86x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 242 ms: 1.85x faster                                                     |
| mdp                              | 1.09 sec                                                 | 609 ms: 1.79x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 511 us: 1.62x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.62x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 143 ms: 1.61x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                     |
| deepcopy                         | 161 us                                                   | 106 us: 1.53x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 150 ms: 1.49x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.4 us: 1.47x faster                                                    |
| float                            | 37.9 ms                                                  | 28.6 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 256 ms: 1.32x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.8 ms: 1.30x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.8 ms: 1.26x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.16 us: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 790 ns: 1.22x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.28 us: 1.19x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 112 ms: 1.18x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 43.6 ns: 1.17x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                    |
| go                               | 70.0 ms                                                  | 60.5 ms: 1.16x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.7 ms: 1.14x faster                                                    |
| k_core                           | 1.12 sec                                                 | 993 ms: 1.13x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 126 ms: 1.13x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 60.6 ms: 1.12x faster                                                    |
| raytrace                         | 145 ms                                                   | 130 ms: 1.12x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 54.6 ms: 1.12x faster                                                    |
| async_generators                 | 206 ms                                                   | 186 ms: 1.11x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.03 sec: 1.10x faster                                                   |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.93 ms: 1.08x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 883 ms: 1.08x faster                                                     |
| pylint                           | 128 ms                                                   | 119 ms: 1.07x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 50.9 ms: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 466 ms: 1.07x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.63 ms: 1.06x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.4 ms: 1.06x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.45 us: 1.05x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.0 ms: 1.04x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.71 us: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.27 ms: 1.03x faster                                                    |
| chaos                            | 28.9 ms                                                  | 28.0 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                     |
| generators                       | 21.9 ms                                                  | 21.4 ms: 1.03x faster                                                    |
| sphinx                           | 434 ms                                                   | 424 ms: 1.02x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 42.6 ms: 1.02x faster                                                    |
| fannkuch                         | 176 ms                                                   | 173 ms: 1.02x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 327 ms: 1.00x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 23.2 ms: 1.01x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.8 ms: 1.02x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.19 ms: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.98 ms: 1.02x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 46.8 ms: 1.03x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 73.2 us: 1.03x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.3 ms: 1.04x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.4 ms: 1.04x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.6 ms: 1.04x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.8 ms: 1.05x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.18 ms: 1.05x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.18 ms: 1.05x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 108 us: 1.05x slower                                                     |
| thrift                           | 322 us                                                   | 339 us: 1.05x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.05x slower                                                     |
| 2to3                             | 114 ms                                                   | 120 ms: 1.06x slower                                                     |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.07x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 61.6 ms: 1.07x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.2 ms: 1.07x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 55.6 ms: 1.08x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 43.5 ms: 1.12x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 191 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.15x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.00 ms: 1.15x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.52 ms: 1.16x slower                                                    |
| shortest_path                    | 219 ms                                                   | 254 ms: 1.16x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 55.6 ms: 1.16x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 47.2 ms: 1.19x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.89 ms: 1.23x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.17 ms: 1.26x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 554 us: 1.32x slower                                                     |
| many_optionals                   | 195 us                                                   | 267 us: 1.37x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.9 ms: 1.45x slower                                                    |
| connected_components             | 201 ms                                                   | 302 ms: 1.50x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.5 ms: 2.88x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (2): pprint_pformat, dask
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260212-3.15.0a6+-945bf8c-NOGIL/bm-20260212-macm4pro-arm64-python-945bf8ce1bf7ee388175-3.15.0a6+-945bf8c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.091x faster

# HPT report

- Reliability score: 99.72% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.36x