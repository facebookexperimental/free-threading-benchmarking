# Results vs. 3.13.0rc2

- fork: python
- ref: 45a3ab5a81769eadd94d
- machine: darwin-arm64
- commit hash: 45a3ab5
- commit date: 2025-03-31
- overall geometric mean: 1.030x slower
- HPT reliability: 98.40%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.07 sec: 1.02x slower                                                   |
| html5lib       | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                    |
| sphinx         | 409 ms                                                         | 420 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 265 ms: 1.99x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 269 ms: 1.93x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 267 ms: 1.51x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 267 ms: 1.45x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 152 ms: 1.22x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.22x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 155 ms: 1.19x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 112 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 264 ms: 1.14x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                     |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 116 ms: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.2 ms: 1.07x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 11.6 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 134 ms: 1.31x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.4 ms: 3.19x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.08x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| float          | 31.4 ms                                                        | 34.5 ms: 1.10x slower                                                    |
| nbody          | 42.5 ms                                                        | 57.6 ms: 1.36x slower                                                    |
| Geometric mean | (ref)                                                          | 1.13x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.98 ms: 1.07x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 92.5 ms: 1.02x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 51.6 ms: 1.08x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 1000 ms                                                        | 970 ms: 1.03x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 63.4 ms: 1.02x slower                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 47.4 ms: 1.03x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.3 us: 1.04x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 38.5 ms: 1.08x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.08 ms: 1.09x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.10x slower                                                     |
| xml_etree_process    | 25.4 ms                                                        | 28.4 ms: 1.12x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 151 us: 1.16x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.66 ms: 1.00x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.43 ms: 1.08x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.1 ms: 1.08x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.3 ms: 1.14x slower                                                    |
| mako            | 4.41 ms                                                        | 5.17 ms: 1.17x slower                                                    |
| django_template | 12.5 ms                                                        | 16.9 ms: 1.36x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.18x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 265 ms: 1.99x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 269 ms: 1.93x faster                                                     |
| mdp                              | 1.06 sec                                                       | 576 ms: 1.83x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 267 ms: 1.51x faster                                                     |
| k_core                           | 1.46 sec                                                       | 989 ms: 1.48x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 267 ms: 1.45x faster                                                     |
| deepcopy                         | 145 us                                                         | 116 us: 1.25x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 152 ms: 1.22x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.22x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 13.7 us: 1.20x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 155 ms: 1.19x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 112 ms: 1.18x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 264 ms: 1.14x faster                                                     |
| go                               | 72.6 ms                                                        | 63.6 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.44 ms: 1.12x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 891 us: 1.11x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 264 ms: 1.11x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 17.8 ms: 1.11x faster                                                    |
| async_generators                 | 193 ms                                                         | 178 ms: 1.09x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.98 ms: 1.07x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 116 ms: 1.05x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 61.6 ms: 1.04x faster                                                    |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 970 ms: 1.03x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 92.5 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 191 ms: 1.02x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.28 us: 1.01x faster                                                    |
| pyflate                          | 222 ms                                                         | 220 ms: 1.01x faster                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 37.5 ms: 1.01x faster                                                    |
| python_startup                   | 8.63 ms                                                        | 8.66 ms: 1.00x slower                                                    |
| connected_components             | 208 ms                                                         | 209 ms: 1.00x slower                                                     |
| html5lib                         | 23.1 ms                                                        | 23.4 ms: 1.01x slower                                                    |
| shortest_path                    | 225 ms                                                         | 228 ms: 1.01x slower                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.16 sec: 1.02x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 63.4 ms: 1.02x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.08 ms: 1.02x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.07 sec: 1.02x slower                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 47.4 ms: 1.03x slower                                                    |
| sphinx                           | 409 ms                                                         | 420 ms: 1.03x slower                                                     |
| 2to3                             | 112 ms                                                         | 115 ms: 1.03x slower                                                     |
| sqlalchemy_declarative           | 44.4 ms                                                        | 45.9 ms: 1.03x slower                                                    |
| pathlib                          | 11.1 ms                                                        | 11.6 ms: 1.04x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.3 us: 1.04x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.21 ms: 1.05x slower                                                    |
| coverage                         | 31.2 ms                                                        | 32.8 ms: 1.05x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 50.7 ms: 1.06x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.90 ms: 1.07x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 46.2 ms: 1.07x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 441 us: 1.07x slower                                                     |
| sympy_integrate                  | 7.53 ms                                                        | 8.09 ms: 1.07x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 38.5 ms: 1.08x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 51.6 ms: 1.08x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 11.6 ms: 1.08x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.43 ms: 1.08x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.1 ms: 1.08x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.43 ms: 1.09x slower                                                    |
| pycparser                        | 470 ms                                                         | 510 ms: 1.09x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 26.9 ms: 1.09x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 70.5 us: 1.09x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 5.08 ms: 1.09x slower                                                    |
| richards                         | 22.1 ms                                                        | 24.2 ms: 1.10x slower                                                    |
| float                            | 31.4 ms                                                        | 34.5 ms: 1.10x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.10x slower                                                     |
| sympy_sum                        | 52.3 ms                                                        | 57.6 ms: 1.10x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.2 ms: 1.11x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 106 ms: 1.11x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 178 ms: 1.11x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 28.4 ms: 1.12x slower                                                    |
| pylint                           | 106 ms                                                         | 119 ms: 1.13x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.23 ms: 1.13x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.3 ms: 1.14x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.79 us: 1.14x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 142 ms: 1.14x slower                                                     |
| fannkuch                         | 179 ms                                                         | 205 ms: 1.15x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.57 us: 1.15x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 749 ms: 1.15x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 151 us: 1.16x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 373 ms: 1.16x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 50.9 ms: 1.16x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 47.6 ns: 1.17x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.17 ms: 1.17x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.4 ms: 1.17x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| chaos                            | 24.3 ms                                                        | 28.8 ms: 1.19x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.73 ms: 1.19x slower                                                    |
| many_optionals                   | 200 us                                                         | 239 us: 1.19x slower                                                     |
| raytrace                         | 109 ms                                                         | 131 ms: 1.21x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 45.1 ms: 1.21x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 41.3 ms: 1.23x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.41 us: 1.24x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 53.9 ms: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 134 ms: 1.31x slower                                                     |
| django_template                  | 12.5 ms                                                        | 16.9 ms: 1.36x slower                                                    |
| nbody                            | 42.5 ms                                                        | 57.6 ms: 1.36x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 8.96 ms: 1.43x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.4 ms: 3.19x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.03x slower                                                             |

Benchmark hidden because not significant (2): sqlite_synth, json
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250331-3.14.0a6+-45a3ab5/bm-20250331-macm4pro-arm64-python-45a3ab5a81769eadd94d-3.14.0a6+-45a3ab5.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.030x slower

# HPT report

- Reliability score: 98.40% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.07x