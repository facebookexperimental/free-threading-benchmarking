# Results vs. 3.12.6

- fork: python
- ref: be9c7cb4b50f8007b610
- machine: darwin-arm64
- commit hash: be9c7cb
- commit date: 2026-05-01
- overall geometric mean: 1.103x faster
- HPT reliability: 99.48%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.37x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 123 ms: 1.08x slower                                                     |
| docutils       | 1.02 sec                                                 | 996 ms: 1.03x faster                                                     |
| sphinx         | 434 ms                                                   | 422 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 245 ms: 2.02x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 239 ms: 2.01x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 239 ms: 1.86x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 251 ms: 1.83x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.53x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 151 ms: 1.48x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 256 ms: 1.32x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 263 ms: 1.27x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                     |
| async_generators                 | 206 ms                                                   | 188 ms: 1.10x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.03x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.2 ms: 1.04x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.14x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.9 ms: 2.89x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                    |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| nbody          | 54.2 ms                                                  | 58.0 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 51.5 ms: 1.06x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.5 ms: 1.04x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.22 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.5 ms: 1.30x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 58.3 ms: 1.16x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.85 ms: 1.11x faster                                                    |
| tomli_loads          | 957 ms                                                   | 888 ms: 1.08x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.2 ms: 1.02x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 111 us: 1.08x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 151 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.77 ms: 1.19x slower                                                    |
| python_startup         | 8.01 ms                                                  | 9.67 ms: 1.21x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.20x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 13.6 ms                                                  | 15.8 ms: 1.16x slower                                                    |
| mako            | 4.77 ms                                                  | 5.70 ms: 1.19x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.18x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.11 ms: 5.05x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 785 us: 2.56x faster                                                     |
| pylint                           | 128 ms                                                   | 51.8 ms: 2.47x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 245 ms: 2.02x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 239 ms: 2.01x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 239 ms: 1.86x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 251 ms: 1.83x faster                                                     |
| mdp                              | 1.09 sec                                                 | 612 ms: 1.78x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 504 us: 1.65x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 107 ms: 1.61x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 116 ms: 1.53x faster                                                     |
| deepcopy                         | 161 us                                                   | 109 us: 1.49x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 151 ms: 1.48x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 13.1 us: 1.39x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 256 ms: 1.32x faster                                                     |
| float                            | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.5 ms: 1.30x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 263 ms: 1.27x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.18 us: 1.24x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.13 us: 1.21x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 812 ns: 1.19x faster                                                     |
| go                               | 70.0 ms                                                  | 59.9 ms: 1.17x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 43.6 ns: 1.17x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 58.3 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.45 ms: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                    |
| raytrace                         | 145 ms                                                   | 129 ms: 1.13x faster                                                     |
| k_core                           | 1.12 sec                                                 | 992 ms: 1.13x faster                                                     |
| pyflate                          | 216 ms                                                   | 193 ms: 1.12x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.85 ms: 1.11x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 55.6 ms: 1.10x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 129 ms: 1.10x faster                                                     |
| async_generators                 | 206 ms                                                   | 188 ms: 1.10x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 888 ms: 1.08x faster                                                     |
| pycparser                        | 497 ms                                                   | 464 ms: 1.07x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.40 us: 1.07x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.63 us: 1.07x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 51.5 ms: 1.06x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.4 ms: 1.06x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 41.3 ms: 1.05x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.6 ms: 1.05x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.65 ms: 1.05x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 95.5 ms: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.22 ms: 1.04x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 184 ms: 1.03x faster                                                     |
| generators                       | 21.9 ms                                                  | 21.2 ms: 1.03x faster                                                    |
| sphinx                           | 434 ms                                                   | 422 ms: 1.03x faster                                                     |
| docutils                         | 1.02 sec                                                 | 996 ms: 1.03x faster                                                     |
| fannkuch                         | 176 ms                                                   | 176 ms: 1.00x slower                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 8.10 ms: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| xml_etree_process                | 26.7 ms                                                  | 27.2 ms: 1.02x slower                                                    |
| json                             | 1.93 ms                                                  | 1.98 ms: 1.03x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 337 ms: 1.03x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.3 ms: 1.03x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 689 ms: 1.04x slower                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 73.6 us: 1.04x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 47.2 ms: 1.04x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.4 ms: 1.04x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.6 ms: 1.05x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 60.8 ms: 1.06x slower                                                    |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.06x slower                                                     |
| hexiom                           | 3.04 ms                                                  | 3.23 ms: 1.06x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.21 ms: 1.06x slower                                                    |
| thrift                           | 322 us                                                   | 344 us: 1.07x slower                                                     |
| nbody                            | 54.2 ms                                                  | 58.0 ms: 1.07x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 111 us: 1.08x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 151 us: 1.08x slower                                                     |
| 2to3                             | 114 ms                                                   | 123 ms: 1.08x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                     |
| shortest_path                    | 219 ms                                                   | 249 ms: 1.14x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.14x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 44.7 ms: 1.15x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.8 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 56.0 ms: 1.17x slower                                                    |
| telco                            | 2.61 ms                                                  | 3.09 ms: 1.18x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 47.0 ms: 1.18x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.77 ms: 1.19x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 61.1 ms: 1.19x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.70 ms: 1.19x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.67 ms: 1.21x slower                                                    |
| connected_components             | 201 ms                                                   | 244 ms: 1.22x slower                                                     |
| many_optionals                   | 195 us                                                   | 261 us: 1.34x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 567 us: 1.35x slower                                                     |
| coverage                         | 26.9 ms                                                  | 39.8 ms: 1.48x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 92.9 ms: 2.89x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                             |

Benchmark hidden because not significant (2): dask, html5lib
Ignored benchmarks (12) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260501-3.15.0a8+-be9c7cb-NOGIL/bm-20260501-macm4pro-arm64-python-be9c7cb4b50f8007b610-3.15.0a8+-be9c7cb.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.103x faster

# HPT report

- Reliability score: 99.48% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.37x