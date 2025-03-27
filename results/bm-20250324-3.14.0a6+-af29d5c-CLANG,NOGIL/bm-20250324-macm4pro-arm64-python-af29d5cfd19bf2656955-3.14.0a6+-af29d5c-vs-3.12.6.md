# Results vs. 3.12.6

- fork: python
- ref: af29d5cfd19bf2656955
- machine: darwin-arm64
- commit hash: af29d5c
- commit date: 2025-03-24
- overall geometric mean: 1.126x faster
- HPT reliability: 99.82%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| docutils       | 1.02 sec                                                 | 978 ms: 1.04x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.5 ms: 1.02x faster                                                    |
| sphinx         | 434 ms                                                   | 403 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 190 ms: 2.53x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 199 ms: 2.50x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 186 ms: 2.40x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 205 ms: 2.24x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 83.2 ms: 2.07x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 121 ms: 1.91x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.9 ms: 1.78x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.72x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.11 ms: 1.49x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 231 ms: 1.47x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 240 ms: 1.39x faster                                                     |
| async_generators                 | 206 ms                                                   | 169 ms: 1.22x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 110 ms: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.01x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 46.7 ms: 1.02x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 222 ms: 1.04x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 74.9 ms: 2.33x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.42x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.9 ms: 1.31x faster                                                    |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                     |
| nbody          | 54.2 ms                                                  | 60.1 ms: 1.11x slower                                                    |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 49.4 ms: 1.11x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 103 ms: 1.03x slower                                                     |
| regex_v8       | 9.59 ms                                                  | 10.1 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 35.4 ms: 1.46x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 57.1 ms: 1.19x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 34.8 ms: 1.12x faster                                                    |
| tomli_loads          | 957 ms                                                   | 882 ms: 1.09x faster                                                     |
| xml_etree_process    | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 98.8 us: 1.04x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 140 us: 1.00x slower                                                     |
| json_loads           | 10.9 us                                                  | 11.8 us: 1.08x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 5.09 ms: 1.19x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.31 ms: 1.16x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.35 ms: 1.29x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.22x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 20.9 ms: 1.04x faster                                                    |
| genshi_text     | 10.5 ms                                                  | 10.6 ms: 1.01x slower                                                    |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                    |
| mako            | 4.77 ms                                                  | 5.47 ms: 1.14x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.06x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 771 us: 2.61x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 190 ms: 2.53x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 199 ms: 2.50x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 8.44 ms: 2.46x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 186 ms: 2.40x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 205 ms: 2.24x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 83.2 ms: 2.07x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 121 ms: 1.91x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 464 us: 1.79x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.9 ms: 1.78x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.72x faster                                                     |
| generators                       | 21.9 ms                                                  | 14.0 ms: 1.57x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.11 ms: 1.49x faster                                                    |
| deepcopy                         | 161 us                                                   | 110 us: 1.47x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 231 ms: 1.47x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 35.4 ms: 1.46x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 240 ms: 1.39x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 13.3 us: 1.38x faster                                                    |
| float                            | 37.9 ms                                                  | 28.9 ms: 1.31x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.12 us: 1.31x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.89 us: 1.25x faster                                                    |
| async_generators                 | 206 ms                                                   | 169 ms: 1.22x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| go                               | 70.0 ms                                                  | 58.6 ms: 1.19x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 810 ns: 1.19x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 57.1 ms: 1.19x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.0 ms: 1.18x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 43.3 ns: 1.17x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.94 sec: 1.16x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 54.0 ms: 1.13x faster                                                    |
| raytrace                         | 145 ms                                                   | 129 ms: 1.12x faster                                                     |
| pylint                           | 128 ms                                                   | 114 ms: 1.12x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.54 ms: 1.12x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.8 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                    |
| pyflate                          | 216 ms                                                   | 195 ms: 1.11x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.11x faster                                                    |
| k_core                           | 1.12 sec                                                 | 1.01 sec: 1.11x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 49.4 ms: 1.11x faster                                                    |
| pycparser                        | 497 ms                                                   | 452 ms: 1.10x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 39.5 ms: 1.10x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 49.8 ms: 1.09x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 882 ms: 1.09x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.38 us: 1.08x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.61 us: 1.08x faster                                                    |
| sphinx                           | 434 ms                                                   | 403 ms: 1.07x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 25.2 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 220 ms: 1.05x faster                                                     |
| docutils                         | 1.02 sec                                                 | 978 ms: 1.04x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 20.9 ms: 1.04x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 98.8 us: 1.04x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.8 ms: 1.04x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.93 ms: 1.04x faster                                                    |
| thrift                           | 322 us                                                   | 311 us: 1.03x faster                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 69.0 us: 1.03x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 110 ms: 1.03x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.5 ms: 1.02x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 139 ms: 1.02x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.88 ms: 1.02x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 57.2 ms: 1.01x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 140 us: 1.00x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 39.9 ms: 1.00x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 191 ms: 1.01x slower                                                     |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 10.6 ms: 1.01x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 25.8 ms: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.02x slower                                                    |
| mdp                              | 1.09 sec                                                 | 1.11 sec: 1.02x slower                                                   |
| richards                         | 22.4 ms                                                  | 22.9 ms: 1.02x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 46.7 ms: 1.02x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 39.9 ms: 1.03x slower                                                    |
| sqlalchemy_declarative           | 46.8 ms                                                  | 48.1 ms: 1.03x slower                                                    |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                     |
| regex_dna                        | 99.6 ms                                                  | 103 ms: 1.03x slower                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 340 ms: 1.04x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 691 ms: 1.04x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.5 ms: 1.04x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 222 ms: 1.04x slower                                                     |
| sqlalchemy_imperative            | 5.17 ms                                                  | 5.42 ms: 1.05x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 175 ms: 1.05x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 10.1 ms: 1.05x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.19 ms: 1.05x slower                                                    |
| fannkuch                         | 176 ms                                                   | 189 ms: 1.08x slower                                                     |
| json_loads                       | 10.9 us                                                  | 11.8 us: 1.08x slower                                                    |
| shortest_path                    | 219 ms                                                   | 239 ms: 1.09x slower                                                     |
| nbody                            | 54.2 ms                                                  | 60.1 ms: 1.11x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 53.7 ms: 1.13x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.47 ms: 1.14x slower                                                    |
| connected_components             | 201 ms                                                   | 230 ms: 1.15x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 9.31 ms: 1.16x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 5.09 ms: 1.19x slower                                                    |
| many_optionals                   | 195 us                                                   | 235 us: 1.20x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.30 ms: 1.27x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.35 ms: 1.29x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 590 us: 1.41x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.6 ms: 1.44x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 74.9 ms: 2.33x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                             |

Benchmark hidden because not significant (2): sympy_str, scimark_lu
Ignored benchmarks (9) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250324-3.14.0a6+-af29d5c-CLANG,NOGIL/bm-20250324-macm4pro-arm64-python-af29d5cfd19bf2656955-3.14.0a6+-af29d5c.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.126x faster

# HPT report

- Reliability score: 99.82% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.22x