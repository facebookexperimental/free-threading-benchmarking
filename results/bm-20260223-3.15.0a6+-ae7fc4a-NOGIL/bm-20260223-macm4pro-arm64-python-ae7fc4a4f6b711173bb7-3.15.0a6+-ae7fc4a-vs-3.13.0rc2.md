# Results vs. 3.13.0rc2

- fork: python
- ref: ae7fc4a4f6b711173bb7
- machine: darwin-arm64
- commit hash: ae7fc4a
- commit date: 2026-02-23
- overall geometric mean: 1.009x faster
- HPT reliability: 67.87%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6+-ae7fc4a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 122 ms: 1.09x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                   |
| html5lib       | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                    |
| sphinx         | 409 ms                                                         | 427 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6+-ae7fc4a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 246 ms: 2.12x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 251 ms: 2.09x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 236 ms: 1.71x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 251 ms: 1.54x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.21x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 268 ms: 1.09x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| async_generators                 | 193 ms                                                         | 187 ms: 1.03x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.1 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.6 ms: 3.24x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6+-ae7fc4a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.7 ms: 1.09x faster                                                    |
| pidigits       | 166 ms                                                         | 169 ms: 1.02x slower                                                     |
| nbody          | 42.5 ms                                                        | 56.6 ms: 1.33x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6+-ae7fc4a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.43 ms: 1.13x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 97.6 ms: 1.03x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 51.0 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6+-ae7fc4a |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.5 ms: 1.20x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.97 ms: 1.17x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 878 ms: 1.14x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 58.9 ms: 1.06x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.4 ms: 1.05x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.1 ms: 1.07x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 108 us: 1.09x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 147 us: 1.13x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6+-ae7fc4a |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.2 ms: 1.18x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.43 ms: 1.25x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.22x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6+-ae7fc4a |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.8 ms: 1.07x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                    |
| django_template | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| mako            | 4.41 ms                                                        | 5.54 ms: 1.26x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.17x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6+-ae7fc4a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 818 us: 2.50x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 246 ms: 2.12x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 251 ms: 2.09x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 517 us: 1.92x faster                                                     |
| mdp                              | 1.06 sec                                                       | 611 ms: 1.73x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 236 ms: 1.71x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 251 ms: 1.54x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.14 ms: 1.51x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.00 sec: 1.46x faster                                                   |
| deepcopy                         | 145 us                                                         | 107 us: 1.35x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.8 us: 1.29x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 145 ms: 1.28x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 104 ms: 1.27x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 115 ms: 1.24x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 153 ms: 1.21x faster                                                     |
| go                               | 72.6 ms                                                        | 60.4 ms: 1.20x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.5 ms: 1.20x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 799 ns: 1.19x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 54.4 ms: 1.18x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.97 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 260 ms: 1.16x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 878 ms: 1.14x faster                                                     |
| pyflate                          | 222 ms                                                         | 196 ms: 1.14x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.43 ms: 1.13x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.18 us: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 268 ms: 1.09x faster                                                     |
| float                            | 31.4 ms                                                        | 28.7 ms: 1.09x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.48 ms: 1.09x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 114 ms: 1.07x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.00 sec: 1.06x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 58.9 ms: 1.06x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.8 ms: 1.05x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.3 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| fannkuch                         | 179 ms                                                         | 172 ms: 1.04x faster                                                     |
| async_generators                 | 193 ms                                                         | 187 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                    |
| docutils                         | 1.05 sec                                                       | 1.02 sec: 1.02x faster                                                   |
| scimark_fft                      | 124 ms                                                         | 125 ms: 1.01x slower                                                     |
| dask                             | 525 ms                                                         | 530 ms: 1.01x slower                                                     |
| json                             | 1.94 ms                                                        | 1.96 ms: 1.01x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                     |
| pidigits                         | 166 ms                                                         | 169 ms: 1.02x slower                                                     |
| html5lib                         | 23.1 ms                                                        | 23.5 ms: 1.02x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 330 ms: 1.03x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 97.6 ms: 1.03x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 672 ms: 1.03x slower                                                     |
| sphinx                           | 409 ms                                                         | 427 ms: 1.04x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.4 ms: 1.05x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.1 ms: 1.05x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.05x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 51.0 ms: 1.06x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.8 ms: 1.07x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.1 ms: 1.07x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.6 ms: 1.08x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 108 us: 1.09x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.1 ms: 1.09x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.44 us: 1.09x slower                                                    |
| 2to3                             | 112 ms                                                         | 122 ms: 1.09x slower                                                     |
| thrift                           | 309 us                                                         | 338 us: 1.10x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 44.5 ns: 1.10x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.27 ms: 1.10x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.0 ms: 1.11x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.72 us: 1.11x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.2 ms: 1.12x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.19 ms: 1.12x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.3 ms: 1.13x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 147 us: 1.13x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 73.3 us: 1.13x slower                                                    |
| shortest_path                    | 225 ms                                                         | 255 ms: 1.14x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 49.8 ms: 1.14x slower                                                    |
| pylint                           | 106 ms                                                         | 120 ms: 1.14x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.66 ms: 1.15x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 42.8 ms: 1.15x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 56.2 ms: 1.17x slower                                                    |
| raytrace                         | 109 ms                                                         | 128 ms: 1.18x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 61.9 ms: 1.18x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 10.2 ms: 1.18x slower                                                    |
| connected_components             | 208 ms                                                         | 246 ms: 1.18x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 189 ms: 1.19x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 249 ms: 1.20x slower                                                     |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.16 ms: 1.21x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.32 us: 1.22x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.6 ms: 1.24x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.43 ms: 1.25x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.6 ms: 1.25x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 129 ms: 1.26x slower                                                     |
| mako                             | 4.41 ms                                                        | 5.54 ms: 1.26x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 47.8 ms: 1.26x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 43.7 ms: 1.30x slower                                                    |
| nbody                            | 42.5 ms                                                        | 56.6 ms: 1.33x slower                                                    |
| many_optionals                   | 200 us                                                         | 270 us: 1.35x slower                                                     |
| generators                       | 15.7 ms                                                        | 21.3 ms: 1.36x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 58.4 ms: 1.37x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 586 us: 1.42x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.6 ms: 3.24x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x faster                                                             |

Benchmark hidden because not significant (2): telco, pycparser
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260223-3.15.0a6+-ae7fc4a-NOGIL/bm-20260223-macm4pro-arm64-python-ae7fc4a4f6b711173bb7-3.15.0a6+-ae7fc4a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.009x faster

# HPT report

- Reliability score: 67.87% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.32x