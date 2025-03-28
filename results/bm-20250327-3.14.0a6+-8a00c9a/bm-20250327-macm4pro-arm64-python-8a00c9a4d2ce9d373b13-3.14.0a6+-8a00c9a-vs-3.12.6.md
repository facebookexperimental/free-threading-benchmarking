# Results vs. 3.12.6

- fork: python
- ref: 8a00c9a4d2ce9d373b13
- machine: darwin-arm64
- commit hash: 8a00c9a
- commit date: 2025-03-27
- overall geometric mean: 1.035x faster
- HPT reliability: 52.52%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 116 ms: 1.02x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.08 sec: 1.06x slower                                                   |
| html5lib       | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                    |
| sphinx         | 434 ms                                                   | 426 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 267 ms: 1.86x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 271 ms: 1.77x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 272 ms: 1.69x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 269 ms: 1.66x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 113 ms: 1.52x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 118 ms: 1.51x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 156 ms: 1.48x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 158 ms: 1.41x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 267 ms: 1.27x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 11.6 ms: 1.17x faster                                                    |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 116 ms: 1.13x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 137 ms: 1.22x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.1 ms: 2.90x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.19x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 34.7 ms: 1.09x faster                                                    |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| nbody          | 54.2 ms                                                  | 58.1 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                    | 1.00x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.54 ms: 1.08x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 93.6 ms: 1.06x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 52.1 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 10.2 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 67.9 ms                                                  | 59.8 ms: 1.14x faster                                                    |
| xml_etree_iterparse  | 51.6 ms                                                  | 47.0 ms: 1.10x faster                                                    |
| tomli_loads          | 957 ms                                                   | 979 ms: 1.02x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| xml_etree_process    | 26.7 ms                                                  | 28.6 ms: 1.07x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.09x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 152 us: 1.09x slower                                                     |
| json_dumps           | 4.26 ms                                                  | 5.18 ms: 1.22x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.03x slower                                                             |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.70 ms: 1.09x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.46 ms: 1.13x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.3 ms: 1.07x slower                                                    |
| mako            | 4.77 ms                                                  | 5.17 ms: 1.08x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                    |
| django_template | 13.6 ms                                                  | 17.0 ms: 1.25x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.12x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.05 ms: 2.30x faster                                                    |
| mdp                              | 1.09 sec                                                 | 577 ms: 1.89x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 267 ms: 1.86x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 271 ms: 1.77x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 272 ms: 1.69x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 269 ms: 1.66x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 113 ms: 1.52x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 118 ms: 1.51x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 156 ms: 1.48x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 158 ms: 1.41x faster                                                     |
| deepcopy                         | 161 us                                                   | 117 us: 1.38x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 13.8 us: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 267 ms: 1.27x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.21 us: 1.21x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.0 ms: 1.18x faster                                                    |
| generators                       | 21.9 ms                                                  | 18.7 ms: 1.17x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 11.6 ms: 1.17x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.42 us: 1.17x faster                                                    |
| async_generators                 | 206 ms                                                   | 180 ms: 1.15x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 59.8 ms: 1.14x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 116 ms: 1.13x faster                                                     |
| k_core                           | 1.12 sec                                                 | 993 ms: 1.13x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 47.0 ms: 1.10x faster                                                    |
| raytrace                         | 145 ms                                                   | 132 ms: 1.09x faster                                                     |
| float                            | 37.9 ms                                                  | 34.7 ms: 1.09x faster                                                    |
| go                               | 70.0 ms                                                  | 64.4 ms: 1.09x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.54 ms: 1.08x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.92 ms: 1.08x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 93.6 ms: 1.06x faster                                                    |
| pylint                           | 128 ms                                                   | 121 ms: 1.06x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 11.7 ms: 1.06x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 48.1 ns: 1.06x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.9 ms: 1.05x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 52.1 ms: 1.05x faster                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 38.0 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.18 sec: 1.03x faster                                                   |
| sphinx                           | 434 ms                                                   | 426 ms: 1.02x faster                                                     |
| sqlalchemy_declarative           | 46.8 ms                                                  | 46.4 ms: 1.01x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.73 ms: 1.00x slower                                                    |
| logging_format                   | 2.80 us                                                  | 2.81 us: 1.00x slower                                                    |
| scimark_fft                      | 142 ms                                                   | 143 ms: 1.01x slower                                                     |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                     |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| logging_simple                   | 2.57 us                                                  | 2.60 us: 1.01x slower                                                    |
| chaos                            | 28.9 ms                                                  | 29.4 ms: 1.02x slower                                                    |
| 2to3                             | 114 ms                                                   | 116 ms: 1.02x slower                                                     |
| scimark_sor                      | 61.0 ms                                                  | 62.1 ms: 1.02x slower                                                    |
| tomli_loads                      | 957 ms                                                   | 979 ms: 1.02x slower                                                     |
| json                             | 1.93 ms                                                  | 1.98 ms: 1.03x slower                                                    |
| sympy_str                        | 104 ms                                                   | 107 ms: 1.03x slower                                                     |
| html5lib                         | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                    |
| shortest_path                    | 219 ms                                                   | 225 ms: 1.03x slower                                                     |
| pyflate                          | 216 ms                                                   | 224 ms: 1.04x slower                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 8.34 ms: 1.04x slower                                                    |
| connected_components             | 201 ms                                                   | 209 ms: 1.04x slower                                                     |
| nqueens                          | 43.5 ms                                                  | 45.3 ms: 1.04x slower                                                    |
| pycparser                        | 497 ms                                                   | 519 ms: 1.04x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.6 ms: 1.04x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 438 us: 1.05x slower                                                     |
| docutils                         | 1.02 sec                                                 | 1.08 sec: 1.06x slower                                                   |
| regex_v8                         | 9.59 ms                                                  | 10.2 ms: 1.06x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.52 ms: 1.07x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.3 ms: 1.07x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 28.6 ms: 1.07x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.1 ms: 1.07x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 179 ms: 1.07x slower                                                     |
| nbody                            | 54.2 ms                                                  | 58.1 ms: 1.07x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.27 ms: 1.08x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 41.8 ms: 1.08x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 51.5 ms: 1.08x slower                                                    |
| richards                         | 22.4 ms                                                  | 24.2 ms: 1.08x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.17 ms: 1.08x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.70 ms: 1.09x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.09x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 55.8 ms: 1.09x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 152 us: 1.09x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 910 us: 1.10x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 748 ms: 1.13x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.46 ms: 1.13x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 373 ms: 1.14x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.31 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.17x slower                                                     |
| fannkuch                         | 176 ms                                                   | 207 ms: 1.18x slower                                                     |
| json_dumps                       | 4.26 ms                                                  | 5.18 ms: 1.22x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 137 ms: 1.22x slower                                                     |
| coverage                         | 26.9 ms                                                  | 33.1 ms: 1.23x slower                                                    |
| many_optionals                   | 195 us                                                   | 242 us: 1.24x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.24 ms: 1.24x slower                                                    |
| django_template                  | 13.6 ms                                                  | 17.0 ms: 1.25x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.1 ms: 2.90x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.04x faster                                                             |

Benchmark hidden because not significant (5): sqlite_synth, async_tree_eager, xml_etree_generate, sympy_sum, typing_runtime_protocols
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250327-3.14.0a6+-8a00c9a/bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.035x faster

# HPT report

- Reliability score: 52.52% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.12x