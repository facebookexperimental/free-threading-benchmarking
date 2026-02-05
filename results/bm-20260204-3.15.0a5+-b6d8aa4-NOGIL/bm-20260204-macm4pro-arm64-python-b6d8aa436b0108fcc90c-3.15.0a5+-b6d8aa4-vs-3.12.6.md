# Results vs. 3.12.6

- fork: python
- ref: b6d8aa436b0108fcc90c
- machine: darwin-arm64
- commit hash: b6d8aa4
- commit date: 2026-02-04
- overall geometric mean: 1.120x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 118 ms: 1.03x slower                                                     |
| docutils       | 1.02 sec                                                 | 979 ms: 1.04x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.3 ms: 1.03x faster                                                    |
| sphinx         | 434 ms                                                   | 410 ms: 1.06x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 236 ms: 2.10x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 235 ms: 2.04x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 243 ms: 1.89x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 238 ms: 1.87x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 142 ms: 1.63x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.57x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.51x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 263 ms: 1.27x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| async_generators                 | 206 ms                                                   | 182 ms: 1.14x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 45.8 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.14x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.4 ms: 2.84x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.2 ms: 1.34x faster                                                    |
| pidigits       | 161 ms                                                   | 157 ms: 1.03x faster                                                     |
| nbody          | 54.2 ms                                                  | 55.3 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.11x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.41 ms: 1.18x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 49.3 ms: 1.11x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 91.8 ms: 1.09x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 8.95 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                    | 1.11x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|---------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse | 51.6 ms                                                  | 37.9 ms: 1.36x faster                                                    |
| xml_etree_parse     | 67.9 ms                                                  | 56.3 ms: 1.21x faster                                                    |
| tomli_loads         | 957 ms                                                   | 846 ms: 1.13x faster                                                     |
| json_dumps          | 4.26 ms                                                  | 3.89 ms: 1.09x faster                                                    |
| xml_etree_generate  | 38.9 ms                                                  | 36.5 ms: 1.07x faster                                                    |
| xml_etree_process   | 26.7 ms                                                  | 26.4 ms: 1.01x faster                                                    |
| json_loads          | 10.9 us                                                  | 11.0 us: 1.01x slower                                                    |
| pickle_pure_python  | 139 us                                                   | 143 us: 1.02x slower                                                     |
| Geometric mean      | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.63 ms: 1.20x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.00 ms: 1.23x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 10.8 ms: 1.03x slower                                                    |
| django_template | 13.6 ms                                                  | 15.2 ms: 1.11x slower                                                    |
| mako            | 4.77 ms                                                  | 5.44 ms: 1.14x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.07x slower                                                             |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.09 ms: 5.08x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 768 us: 2.61x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 236 ms: 2.10x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 235 ms: 2.04x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 243 ms: 1.89x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 238 ms: 1.87x faster                                                     |
| mdp                              | 1.09 sec                                                 | 592 ms: 1.84x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 501 us: 1.66x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 142 ms: 1.63x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 114 ms: 1.57x faster                                                     |
| deepcopy                         | 161 us                                                   | 104 us: 1.56x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.51x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.3 us: 1.48x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.9 ms: 1.36x faster                                                    |
| float                            | 37.9 ms                                                  | 28.2 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.13 us: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 263 ms: 1.27x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 781 ns: 1.24x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.07 us: 1.22x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 56.3 ms: 1.21x faster                                                    |
| go                               | 70.0 ms                                                  | 58.5 ms: 1.20x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 42.9 ns: 1.19x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.18x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.41 ms: 1.18x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.17x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                   |
| raytrace                         | 145 ms                                                   | 126 ms: 1.15x faster                                                     |
| pyflate                          | 216 ms                                                   | 189 ms: 1.14x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 125 ms: 1.14x faster                                                     |
| async_generators                 | 206 ms                                                   | 182 ms: 1.14x faster                                                     |
| k_core                           | 1.12 sec                                                 | 984 ms: 1.14x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 846 ms: 1.13x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 54.0 ms: 1.13x faster                                                    |
| pylint                           | 128 ms                                                   | 115 ms: 1.11x faster                                                     |
| pycparser                        | 497 ms                                                   | 448 ms: 1.11x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 49.3 ms: 1.11x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.89 ms: 1.09x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.59 ms: 1.09x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 91.8 ms: 1.09x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.3 ms: 1.08x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.38 us: 1.08x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.3 ms: 1.08x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 8.95 ms: 1.07x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.62 us: 1.07x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 36.5 ms: 1.07x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.2 ms: 1.07x faster                                                    |
| fannkuch                         | 176 ms                                                   | 165 ms: 1.06x faster                                                     |
| sphinx                           | 434 ms                                                   | 410 ms: 1.06x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                     |
| docutils                         | 1.02 sec                                                 | 979 ms: 1.04x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 41.7 ms: 1.04x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 22.3 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| pidigits                         | 161 ms                                                   | 157 ms: 1.03x faster                                                     |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 70.1 us: 1.01x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.4 ms: 1.01x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 325 ms: 1.01x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.95 ms: 1.01x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.0 ms: 1.01x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 667 ms: 1.00x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 45.8 ms: 1.01x slower                                                    |
| thrift                           | 322 us                                                   | 325 us: 1.01x slower                                                     |
| hexiom                           | 3.04 ms                                                  | 3.07 ms: 1.01x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.0 us: 1.01x slower                                                    |
| nbody                            | 54.2 ms                                                  | 55.3 ms: 1.02x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.12 ms: 1.02x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 143 us: 1.02x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 10.8 ms: 1.03x slower                                                    |
| 2to3                             | 114 ms                                                   | 118 ms: 1.03x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 59.5 ms: 1.03x slower                                                    |
| sympy_str                        | 104 ms                                                   | 108 ms: 1.04x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 42.4 ms: 1.09x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 183 ms: 1.10x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.2 ms: 1.11x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 53.3 ms: 1.12x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 45.2 ms: 1.14x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.14x slower                                                     |
| mako                             | 4.77 ms                                                  | 5.44 ms: 1.14x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 58.6 ms: 1.14x slower                                                    |
| shortest_path                    | 219 ms                                                   | 251 ms: 1.15x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.02 ms: 1.16x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.63 ms: 1.20x slower                                                    |
| connected_components             | 201 ms                                                   | 246 ms: 1.22x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 7.00 ms: 1.23x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 551 us: 1.31x slower                                                     |
| many_optionals                   | 195 us                                                   | 259 us: 1.33x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.5 ms: 1.43x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 91.4 ms: 2.84x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                             |

Benchmark hidden because not significant (5): richards, genshi_xml, richards_super, dask, unpickle_pure_python
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260204-3.15.0a5+-b6d8aa4-NOGIL/bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.120x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.36x