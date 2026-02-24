# Results vs. 3.12.6

- fork: python
- ref: ae7fc4a4f6b711173bb7
- machine: darwin-arm64
- commit hash: ae7fc4a
- commit date: 2026-02-23
- overall geometric mean: 1.088x faster
- HPT reliability: 98.72%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6+-ae7fc4a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| html5lib       | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                    |
| sphinx         | 434 ms                                                   | 427 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x slower                                                             |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6+-ae7fc4a |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 236 ms: 2.03x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 251 ms: 1.98x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 251 ms: 1.83x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 246 ms: 1.81x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.65x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.56x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.46x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 260 ms: 1.30x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 268 ms: 1.24x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.15x faster                                                     |
| async_generators                 | 206 ms                                                   | 187 ms: 1.10x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.1 ms: 1.03x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.6 ms: 2.91x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6+-ae7fc4a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                    |
| nbody          | 54.2 ms                                                  | 56.6 ms: 1.04x slower                                                    |
| pidigits       | 161 ms                                                   | 169 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6+-ae7fc4a |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 51.0 ms: 1.07x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 97.6 ms: 1.02x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.43 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6+-ae7fc4a |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.5 ms: 1.34x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 58.9 ms: 1.15x faster                                                    |
| tomli_loads          | 957 ms                                                   | 878 ms: 1.09x faster                                                     |
| json_dumps           | 4.26 ms                                                  | 3.97 ms: 1.07x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.1 ms: 1.01x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 108 us: 1.05x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 147 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6+-ae7fc4a |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 10.2 ms: 1.28x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.43 ms: 1.30x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.29x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6+-ae7fc4a |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 22.8 ms: 1.05x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.3 ms: 1.07x slower                                                    |
| django_template | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                    |
| mako            | 4.77 ms                                                  | 5.54 ms: 1.16x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.11x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6+-ae7fc4a |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.14 ms: 5.01x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 818 us: 2.46x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 236 ms: 2.03x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 251 ms: 1.98x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 251 ms: 1.83x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 246 ms: 1.81x faster                                                     |
| mdp                              | 1.09 sec                                                 | 611 ms: 1.79x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.65x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 517 us: 1.61x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 145 ms: 1.59x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.56x faster                                                     |
| deepcopy                         | 161 us                                                   | 107 us: 1.50x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 153 ms: 1.46x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.8 us: 1.43x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.5 ms: 1.34x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                    |
| float                            | 37.9 ms                                                  | 28.7 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 260 ms: 1.30x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 268 ms: 1.24x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.18 us: 1.24x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 799 ns: 1.21x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.32 us: 1.18x faster                                                    |
| go                               | 70.0 ms                                                  | 60.4 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.15x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 58.9 ms: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 44.5 ns: 1.14x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 125 ms: 1.14x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                    |
| raytrace                         | 145 ms                                                   | 128 ms: 1.13x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.48 ms: 1.13x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 54.4 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                   |
| k_core                           | 1.12 sec                                                 | 1.00 sec: 1.12x faster                                                   |
| pyflate                          | 216 ms                                                   | 196 ms: 1.10x faster                                                     |
| async_generators                 | 206 ms                                                   | 187 ms: 1.10x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 49.8 ms: 1.09x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 878 ms: 1.09x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.97 ms: 1.07x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 51.0 ms: 1.07x faster                                                    |
| chaos                            | 28.9 ms                                                  | 27.2 ms: 1.06x faster                                                    |
| pylint                           | 128 ms                                                   | 120 ms: 1.06x faster                                                     |
| pycparser                        | 497 ms                                                   | 471 ms: 1.06x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.44 us: 1.05x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.66 ms: 1.04x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.72 us: 1.03x faster                                                    |
| generators                       | 21.9 ms                                                  | 21.3 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 97.6 ms: 1.02x faster                                                    |
| fannkuch                         | 176 ms                                                   | 172 ms: 1.02x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 42.8 ms: 1.02x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.43 ms: 1.02x faster                                                    |
| sphinx                           | 434 ms                                                   | 427 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 228 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 530 ms: 1.00x slower                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 330 ms: 1.01x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 672 ms: 1.01x slower                                                     |
| xml_etree_process                | 26.7 ms                                                  | 27.1 ms: 1.01x slower                                                    |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.02x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.5 ms: 1.02x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.0 ms: 1.03x slower                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 8.27 ms: 1.03x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.1 ms: 1.03x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 73.3 us: 1.03x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 47.1 ms: 1.03x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.16 ms: 1.04x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.6 ms: 1.04x slower                                                    |
| pidigits                         | 161 ms                                                   | 169 ms: 1.05x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 26.6 ms: 1.05x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 22.8 ms: 1.05x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 108 us: 1.05x slower                                                     |
| hexiom                           | 3.04 ms                                                  | 3.19 ms: 1.05x slower                                                    |
| thrift                           | 322 us                                                   | 338 us: 1.05x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 147 us: 1.06x slower                                                     |
| sympy_str                        | 104 ms                                                   | 111 ms: 1.06x slower                                                     |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| genshi_text                      | 10.5 ms                                                  | 11.3 ms: 1.07x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 61.9 ms: 1.07x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 43.7 ms: 1.13x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 189 ms: 1.13x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 58.4 ms: 1.14x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.6 ms: 1.15x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.54 ms: 1.16x slower                                                    |
| shortest_path                    | 219 ms                                                   | 255 ms: 1.17x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.07 ms: 1.18x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 56.2 ms: 1.18x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 47.8 ms: 1.20x slower                                                    |
| connected_components             | 201 ms                                                   | 246 ms: 1.23x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 10.2 ms: 1.28x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.43 ms: 1.30x slower                                                    |
| many_optionals                   | 195 us                                                   | 270 us: 1.38x slower                                                     |
| bench_thread_pool                | 419 us                                                   | 586 us: 1.40x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.6 ms: 1.44x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.6 ms: 2.91x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                             |

Benchmark hidden because not significant (1): docutils
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260223-3.15.0a6+-ae7fc4a-NOGIL/bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6+-ae7fc4a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.088x faster

# HPT report

- Reliability score: 98.72% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.38x