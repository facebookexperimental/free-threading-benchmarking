# Results vs. 3.13.0rc2

- fork: python
- ref: ca1bedc9a4da523f4d1f
- machine: darwin-arm64
- commit hash: ca1bedc
- commit date: 2025-03-14
- overall geometric mean: 1.029x slower
- HPT reliability: 98.33%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250314-macm4pro-arm64-python-ca1bedc9a4da523f4d1f-3.14.0a5+-ca1bedc |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 126 ms: 1.13x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| html5lib       | 23.1 ms                                                        | 24.5 ms: 1.06x slower                                                    |
| sphinx         | 409 ms                                                         | 426 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250314-macm4pro-arm64-python-ca1bedc9a4da523f4d1f-3.14.0a5+-ca1bedc |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 204 ms: 2.55x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 216 ms: 2.43x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 205 ms: 1.98x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 220 ms: 1.75x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 90.8 ms: 1.46x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 131 ms: 1.42x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 139 ms: 1.33x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 107 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 239 ms: 1.26x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 248 ms: 1.18x faster                                                     |
| async_generators                 | 193 ms                                                         | 181 ms: 1.07x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 118 ms: 1.03x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 230 ms: 1.11x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 52.8 ms: 1.22x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.5 ms: 2.82x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.20x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250314-macm4pro-arm64-python-ca1bedc9a4da523f4d1f-3.14.0a5+-ca1bedc |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| float          | 31.4 ms                                                        | 32.4 ms: 1.03x slower                                                    |
| nbody          | 42.5 ms                                                        | 63.3 ms: 1.49x slower                                                    |
| Geometric mean | (ref)                                                          | 1.15x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250314-macm4pro-arm64-python-ca1bedc9a4da523f4d1f-3.14.0a5+-ca1bedc |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.51 ms: 1.07x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 102 ms: 1.08x slower                                                     |
| regex_compile  | 47.9 ms                                                        | 56.0 ms: 1.17x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250314-macm4pro-arm64-python-ca1bedc9a4da523f4d1f-3.14.0a5+-ca1bedc |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 37.2 ms: 1.24x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 59.0 ms: 1.06x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 38.3 ms: 1.07x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.8 ms: 1.10x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.9 us: 1.10x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.13 ms: 1.10x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 114 us: 1.15x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 163 us: 1.25x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.05x slower                                                             |

Benchmark hidden because not significant (1): tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250314-macm4pro-arm64-python-ca1bedc9a4da523f4d1f-3.14.0a5+-ca1bedc |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.55 ms: 1.11x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.58 ms: 1.27x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.19x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250314-macm4pro-arm64-python-ca1bedc9a4da523f4d1f-3.14.0a5+-ca1bedc |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 24.6 ms: 1.15x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 12.0 ms: 1.20x slower                                                    |
| mako            | 4.41 ms                                                        | 5.77 ms: 1.31x slower                                                    |
| django_template | 12.5 ms                                                        | 16.9 ms: 1.35x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.25x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250314-macm4pro-arm64-python-ca1bedc9a4da523f4d1f-3.14.0a5+-ca1bedc |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 758 us: 2.69x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 204 ms: 2.55x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 216 ms: 2.43x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 459 us: 2.16x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 205 ms: 1.98x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 220 ms: 1.75x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 90.8 ms: 1.46x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.02 sec: 1.44x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 131 ms: 1.42x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 139 ms: 1.33x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 107 ms: 1.33x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 239 ms: 1.26x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.2 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 248 ms: 1.18x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 824 ns: 1.15x faster                                                     |
| deepcopy                         | 145 us                                                         | 130 us: 1.12x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 57.9 ms: 1.10x faster                                                    |
| async_generators                 | 193 ms                                                         | 181 ms: 1.07x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.51 ms: 1.07x faster                                                    |
| go                               | 72.6 ms                                                        | 68.2 ms: 1.06x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 59.0 ms: 1.06x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 15.6 us: 1.05x faster                                                    |
| pyflate                          | 222 ms                                                         | 214 ms: 1.04x faster                                                     |
| docutils                         | 1.05 sec                                                       | 1.01 sec: 1.04x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 118 ms: 1.03x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 19.2 ms: 1.03x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.07 sec: 1.03x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 189 ms: 1.03x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.02x faster                                                    |
| pidigits                         | 166 ms                                                         | 165 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.01x slower                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.32 us: 1.02x slower                                                    |
| float                            | 31.4 ms                                                        | 32.4 ms: 1.03x slower                                                    |
| json                             | 1.94 ms                                                        | 2.00 ms: 1.03x slower                                                    |
| pycparser                        | 470 ms                                                         | 488 ms: 1.04x slower                                                     |
| sphinx                           | 409 ms                                                         | 426 ms: 1.04x slower                                                     |
| shortest_path                    | 225 ms                                                         | 234 ms: 1.04x slower                                                     |
| html5lib                         | 23.1 ms                                                        | 24.5 ms: 1.06x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 38.3 ms: 1.07x slower                                                    |
| connected_components             | 208 ms                                                         | 223 ms: 1.07x slower                                                     |
| regex_dna                        | 94.6 ms                                                        | 102 ms: 1.08x slower                                                     |
| mdp                              | 1.06 sec                                                       | 1.15 sec: 1.09x slower                                                   |
| thrift                           | 309 us                                                         | 336 us: 1.09x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 27.8 ms: 1.10x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.9 us: 1.10x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 5.13 ms: 1.10x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.55 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 230 ms: 1.11x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 41.9 ms: 1.11x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.44 ms: 1.12x slower                                                    |
| 2to3                             | 112 ms                                                         | 126 ms: 1.13x slower                                                     |
| pylint                           | 106 ms                                                         | 120 ms: 1.13x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 8.62 ms: 1.15x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 114 us: 1.15x slower                                                     |
| fannkuch                         | 179 ms                                                         | 205 ms: 1.15x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 42.8 ms: 1.15x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 24.6 ms: 1.15x slower                                                    |
| richards                         | 22.1 ms                                                        | 25.4 ms: 1.15x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 51.3 ms: 1.16x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.80 ms: 1.16x slower                                                    |
| coverage                         | 31.2 ms                                                        | 36.2 ms: 1.16x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 75.0 us: 1.16x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 119 ms: 1.16x slower                                                     |
| regex_compile                    | 47.9 ms                                                        | 56.0 ms: 1.17x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 28.9 ms: 1.17x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.6 ms: 1.18x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.36 ms: 1.18x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.5 ms: 1.18x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 113 ms: 1.19x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 35.6 ms: 1.19x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.67 us: 1.19x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.92 us: 1.19x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 12.0 ms: 1.20x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.8 ms: 1.20x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.74 ms: 1.20x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 192 ms: 1.20x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 48.8 ns: 1.20x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 57.7 ms: 1.20x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 388 ms: 1.20x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 52.8 ms: 1.22x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 152 ms: 1.23x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 798 ms: 1.23x slower                                                     |
| crypto_pyaes                     | 33.6 ms                                                        | 42.0 ms: 1.25x slower                                                    |
| many_optionals                   | 200 us                                                         | 250 us: 1.25x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 163 us: 1.25x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.58 ms: 1.27x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.27 ms: 1.28x slower                                                    |
| chaos                            | 24.3 ms                                                        | 31.5 ms: 1.30x slower                                                    |
| raytrace                         | 109 ms                                                         | 142 ms: 1.30x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 8.86 us: 1.30x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.77 ms: 1.31x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 56.2 ms: 1.31x slower                                                    |
| django_template                  | 12.5 ms                                                        | 16.9 ms: 1.35x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.10 ms: 1.45x slower                                                    |
| nbody                            | 42.5 ms                                                        | 63.3 ms: 1.49x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 614 us: 1.49x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.5 ms: 2.82x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x slower                                                             |

Benchmark hidden because not significant (2): pathlib, tomli_loads
Ignored benchmarks (9) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20250314-3.14.0a5+-ca1bedc-NOGIL/bm-20250314-macm4pro-arm64-python-ca1bedc9a4da523f4d1f-3.14.0a5+-ca1bedc.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.029x slower

# HPT report

- Reliability score: 98.33% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.18x