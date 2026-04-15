# Results vs. 3.12.6

- fork: python
- ref: d0e7c6acc936a171d05b
- machine: darwin-arm64
- commit hash: d0e7c6a
- commit date: 2026-04-14
- overall geometric mean: 1.100x faster
- HPT reliability: 99.52%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8+-d0e7c6a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 125 ms: 1.10x slower                                                     |
| docutils       | 1.02 sec                                                 | 998 ms: 1.02x faster                                                     |
| sphinx         | 434 ms                                                   | 422 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8+-d0e7c6a |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 243 ms: 2.04x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 240 ms: 2.00x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 246 ms: 1.87x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 242 ms: 1.84x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 108 ms: 1.59x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 117 ms: 1.52x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 150 ms: 1.48x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.17x faster                                                     |
| async_generators                 | 206 ms                                                   | 188 ms: 1.10x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.02x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.6 ms: 1.05x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.7 ms: 2.91x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8+-d0e7c6a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                    |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| nbody          | 54.2 ms                                                  | 57.6 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8+-d0e7c6a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 51.3 ms: 1.07x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.7 ms: 1.04x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.30 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8+-d0e7c6a |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 40.0 ms: 1.29x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.84 ms: 1.11x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 61.5 ms: 1.10x faster                                                    |
| tomli_loads          | 957 ms                                                   | 891 ms: 1.07x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 37.5 ms: 1.04x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.9 ms: 1.00x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 148 us: 1.06x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 111 us: 1.07x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.04x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8+-d0e7c6a |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.71 ms: 1.18x slower                                                    |
| python_startup         | 8.01 ms                                                  | 9.62 ms: 1.20x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.19x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8+-d0e7c6a |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.0 ms: 1.06x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.3 ms: 1.08x slower                                                    |
| django_template | 13.6 ms                                                  | 15.8 ms: 1.16x slower                                                    |
| mako            | 4.77 ms                                                  | 5.63 ms: 1.18x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.12x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8+-d0e7c6a |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.13 ms: 5.03x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 807 us: 2.49x faster                                                     |
| pylint                           | 128 ms                                                   | 51.8 ms: 2.47x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 243 ms: 2.04x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 240 ms: 2.00x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 246 ms: 1.87x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 242 ms: 1.84x faster                                                     |
| mdp                              | 1.09 sec                                                 | 617 ms: 1.77x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 513 us: 1.62x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 108 ms: 1.59x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 117 ms: 1.52x faster                                                     |
| deepcopy                         | 161 us                                                   | 109 us: 1.48x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 150 ms: 1.48x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 13.2 us: 1.39x faster                                                    |
| float                            | 37.9 ms                                                  | 28.5 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.0 ms: 1.29x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.18 us: 1.24x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 792 ns: 1.22x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.16 us: 1.21x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 113 ms: 1.17x faster                                                     |
| go                               | 70.0 ms                                                  | 60.1 ms: 1.17x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.94 sec: 1.15x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 44.2 ns: 1.15x faster                                                    |
| raytrace                         | 145 ms                                                   | 127 ms: 1.14x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.7 ms: 1.13x faster                                                    |
| k_core                           | 1.12 sec                                                 | 987 ms: 1.13x faster                                                     |
| pyflate                          | 216 ms                                                   | 194 ms: 1.11x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.84 ms: 1.11x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 61.5 ms: 1.10x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.5 ms: 1.10x faster                                                    |
| async_generators                 | 206 ms                                                   | 188 ms: 1.10x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 131 ms: 1.08x faster                                                     |
| pycparser                        | 497 ms                                                   | 461 ms: 1.08x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.38 us: 1.08x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 891 ms: 1.07x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 50.6 ms: 1.07x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 51.3 ms: 1.07x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.64 us: 1.06x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 41.1 ms: 1.06x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.4 ms: 1.05x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.65 ms: 1.05x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 95.7 ms: 1.04x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.5 ms: 1.04x faster                                                    |
| generators                       | 21.9 ms                                                  | 21.2 ms: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.30 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| sphinx                           | 434 ms                                                   | 422 ms: 1.03x faster                                                     |
| docutils                         | 1.02 sec                                                 | 998 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.02x faster                                                     |
| fannkuch                         | 176 ms                                                   | 174 ms: 1.01x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 26.9 ms: 1.00x slower                                                    |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 8.14 ms: 1.01x slower                                                    |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 334 ms: 1.02x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 684 ms: 1.03x slower                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 73.2 us: 1.03x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.3 ms: 1.03x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.4 ms: 1.04x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 47.6 ms: 1.05x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.18 ms: 1.05x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.0 ms: 1.06x slower                                                    |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.06x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 60.9 ms: 1.06x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.9 ms: 1.06x slower                                                    |
| nbody                            | 54.2 ms                                                  | 57.6 ms: 1.06x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 148 us: 1.06x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 111 us: 1.07x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 55.2 ms: 1.08x slower                                                    |
| thrift                           | 322 us                                                   | 347 us: 1.08x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.3 ms: 1.08x slower                                                    |
| 2to3                             | 114 ms                                                   | 125 ms: 1.10x slower                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.30 ms: 1.11x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.13x slower                                                     |
| shortest_path                    | 219 ms                                                   | 250 ms: 1.14x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 44.5 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 245 ms: 1.15x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.02 ms: 1.16x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.8 ms: 1.16x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 55.8 ms: 1.17x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.71 ms: 1.18x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.63 ms: 1.18x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.62 ms: 1.20x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 48.1 ms: 1.21x slower                                                    |
| connected_components             | 201 ms                                                   | 244 ms: 1.22x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 567 us: 1.35x slower                                                     |
| many_optionals                   | 195 us                                                   | 272 us: 1.39x slower                                                     |
| coverage                         | 26.9 ms                                                  | 39.1 ms: 1.46x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.7 ms: 2.91x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (2): html5lib, dask
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260414-3.15.0a8+-d0e7c6a-NOGIL/bm-20260414-macm4pro-arm64-python-d0e7c6acc936a171d05b-3.15.0a8+-d0e7c6a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.100x faster

# HPT report

- Reliability score: 99.52% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.38x