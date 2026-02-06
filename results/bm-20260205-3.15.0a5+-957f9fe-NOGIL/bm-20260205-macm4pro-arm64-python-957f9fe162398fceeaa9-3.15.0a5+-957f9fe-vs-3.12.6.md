# Results vs. 3.12.6

- fork: python
- ref: 957f9fe162398fceeaa9
- machine: darwin-arm64
- commit hash: 957f9fe
- commit date: 2026-02-05
- overall geometric mean: 1.121x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5+-957f9fe |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| docutils       | 1.02 sec                                                 | 967 ms: 1.06x faster                                                     |
| html5lib       | 23.0 ms                                                  | 22.4 ms: 1.03x faster                                                    |
| sphinx         | 434 ms                                                   | 409 ms: 1.06x faster                                                     |
| Geometric mean | (ref)                                                    | 1.03x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5+-957f9fe |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 239 ms: 2.08x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 236 ms: 2.03x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 238 ms: 1.93x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 237 ms: 1.88x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 141 ms: 1.64x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.60x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.51x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 248 ms: 1.36x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 255 ms: 1.31x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| async_generators                 | 206 ms                                                   | 177 ms: 1.16x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 183 ms: 1.04x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 45.3 ms: 1.01x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 125 ms: 1.11x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 237 ms: 1.11x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.9 ms: 2.80x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.28x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5+-957f9fe |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.2 ms: 1.34x faster                                                    |
| pidigits       | 161 ms                                                   | 156 ms: 1.03x faster                                                     |
| nbody          | 54.2 ms                                                  | 55.8 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.11x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5+-957f9fe |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.41 ms: 1.18x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 49.5 ms: 1.10x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 90.6 ms: 1.10x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 8.96 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                    | 1.11x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5+-957f9fe |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.8 ms: 1.33x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 59.1 ms: 1.15x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.80 ms: 1.12x faster                                                    |
| tomli_loads          | 957 ms                                                   | 874 ms: 1.10x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 36.7 ms: 1.06x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 26.4 ms: 1.01x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.9 us: 1.01x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 144 us: 1.03x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 107 us: 1.04x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5+-957f9fe |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.62 ms: 1.20x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.00 ms: 1.23x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5+-957f9fe |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.0 ms: 1.01x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                    |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                    |
| mako            | 4.77 ms                                                  | 5.52 ms: 1.16x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.09x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5+-957f9fe |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.02 ms: 5.17x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 759 us: 2.65x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 239 ms: 2.08x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 236 ms: 2.03x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 238 ms: 1.93x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 237 ms: 1.88x faster                                                     |
| mdp                              | 1.09 sec                                                 | 586 ms: 1.86x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 491 us: 1.69x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 141 ms: 1.64x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.60x faster                                                     |
| deepcopy                         | 161 us                                                   | 103 us: 1.57x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.51x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.2 us: 1.50x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 248 ms: 1.36x faster                                                     |
| float                            | 37.9 ms                                                  | 28.2 ms: 1.34x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.8 ms: 1.33x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 255 ms: 1.31x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.12 us: 1.30x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 777 ns: 1.24x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.19 us: 1.20x faster                                                    |
| go                               | 70.0 ms                                                  | 58.6 ms: 1.20x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.0 ms: 1.18x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.41 ms: 1.18x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.18x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.16x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 44.1 ns: 1.15x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 59.1 ms: 1.15x faster                                                    |
| raytrace                         | 145 ms                                                   | 126 ms: 1.15x faster                                                     |
| k_core                           | 1.12 sec                                                 | 986 ms: 1.13x faster                                                     |
| pyflate                          | 216 ms                                                   | 191 ms: 1.13x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 54.1 ms: 1.13x faster                                                    |
| pylint                           | 128 ms                                                   | 114 ms: 1.12x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.80 ms: 1.12x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 127 ms: 1.12x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 49.5 ms: 1.10x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 90.6 ms: 1.10x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 874 ms: 1.10x faster                                                     |
| pycparser                        | 497 ms                                                   | 454 ms: 1.10x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.58 ms: 1.09x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.2 ms: 1.09x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.37 us: 1.08x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.61 us: 1.07x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 8.96 ms: 1.07x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 50.8 ms: 1.07x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 36.7 ms: 1.06x faster                                                    |
| sphinx                           | 434 ms                                                   | 409 ms: 1.06x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 41.1 ms: 1.06x faster                                                    |
| docutils                         | 1.02 sec                                                 | 967 ms: 1.06x faster                                                     |
| chaos                            | 28.9 ms                                                  | 27.6 ms: 1.05x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 183 ms: 1.04x faster                                                     |
| pidigits                         | 161 ms                                                   | 156 ms: 1.03x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.4 ms: 1.03x faster                                                    |
| fannkuch                         | 176 ms                                                   | 171 ms: 1.03x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.90 ms: 1.01x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.4 ms: 1.01x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 70.1 us: 1.01x faster                                                    |
| json                             | 1.93 ms                                                  | 1.91 ms: 1.01x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 45.3 ms: 1.01x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.0 ms: 1.01x slower                                                    |
| json_loads                       | 10.9 us                                                  | 10.9 us: 1.01x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.5 ms: 1.01x slower                                                    |
| 2to3                             | 114 ms                                                   | 115 ms: 1.01x slower                                                     |
| hexiom                           | 3.04 ms                                                  | 3.07 ms: 1.01x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 333 ms: 1.02x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 25.8 ms: 1.02x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 676 ms: 1.02x slower                                                     |
| thrift                           | 322 us                                                   | 328 us: 1.02x slower                                                     |
| nbody                            | 54.2 ms                                                  | 55.8 ms: 1.03x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.14 ms: 1.03x slower                                                    |
| sympy_str                        | 104 ms                                                   | 107 ms: 1.03x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 59.4 ms: 1.03x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 144 us: 1.03x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 107 us: 1.04x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 54.7 ms: 1.07x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.2 ms: 1.09x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.5 ms: 1.10x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 183 ms: 1.10x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 125 ms: 1.11x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 53.0 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 237 ms: 1.11x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 44.5 ms: 1.12x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                    |
| shortest_path                    | 219 ms                                                   | 251 ms: 1.15x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.01 ms: 1.15x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.52 ms: 1.16x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.62 ms: 1.20x slower                                                    |
| connected_components             | 201 ms                                                   | 245 ms: 1.22x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 7.00 ms: 1.23x slower                                                    |
| many_optionals                   | 195 us                                                   | 251 us: 1.29x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 547 us: 1.31x slower                                                     |
| coverage                         | 26.9 ms                                                  | 37.6 ms: 1.40x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 89.9 ms: 2.80x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                             |

Benchmark hidden because not significant (2): richards, dask
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260205-3.15.0a5+-957f9fe-NOGIL/bm-20260205-macm4pro-arm64-python-957f9fe162398fceeaa9-3.15.0a5+-957f9fe.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.121x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.36x