# Results vs. 3.13.0rc2

- fork: python
- ref: 9c1e85fd64cf6a85f7c9
- machine: darwin-arm64
- commit hash: 9c1e85f
- commit date: 2025-03-29
- overall geometric mean: 1.003x faster
- HPT reliability: 65.57%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 121 ms: 1.08x slower                                                     |
| docutils       | 1.05 sec                                                       | 997 ms: 1.05x faster                                                     |
| html5lib       | 23.1 ms                                                        | 21.9 ms: 1.06x faster                                                    |
| sphinx         | 409 ms                                                         | 416 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                          | 1.00x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 203 ms: 2.56x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 213 ms: 2.46x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 207 ms: 1.96x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 220 ms: 1.76x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 90.9 ms: 1.46x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 127 ms: 1.46x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 135 ms: 1.37x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 105 ms: 1.36x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.28x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 245 ms: 1.20x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.08x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| async_generators                 | 193 ms                                                         | 189 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.09x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 115 ms: 1.13x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 49.5 ms: 1.15x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.0 ms: 2.80x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.22x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 158 ms: 1.05x faster                                                     |
| float          | 31.4 ms                                                        | 30.7 ms: 1.02x faster                                                    |
| nbody          | 42.5 ms                                                        | 66.1 ms: 1.55x slower                                                    |
| Geometric mean | (ref)                                                          | 1.13x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.40 ms: 1.15x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.42 ms: 1.14x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 91.9 ms: 1.03x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 52.9 ms: 1.10x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 37.0 ms: 1.25x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 54.7 ms: 1.14x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 913 ms: 1.09x faster                                                     |
| xml_etree_generate   | 35.8 ms                                                        | 37.8 ms: 1.05x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.6 us: 1.07x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.00 ms: 1.07x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.5 ms: 1.08x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 111 us: 1.11x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 152 us: 1.17x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.01x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.16 ms: 1.06x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.23 ms: 1.21x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.13x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.9 ms: 1.07x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.5 ms: 1.16x slower                                                    |
| mako            | 4.41 ms                                                        | 5.63 ms: 1.28x slower                                                    |
| django_template | 12.5 ms                                                        | 16.2 ms: 1.30x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.20x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 203 ms: 2.56x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 213 ms: 2.46x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 930 us: 2.19x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 207 ms: 1.96x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 508 us: 1.95x faster                                                     |
| mdp                              | 1.06 sec                                                       | 600 ms: 1.76x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 220 ms: 1.76x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 90.9 ms: 1.46x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 127 ms: 1.46x faster                                                     |
| k_core                           | 1.46 sec                                                       | 1.03 sec: 1.43x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 135 ms: 1.37x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 105 ms: 1.36x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 236 ms: 1.28x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.0 ms: 1.25x faster                                                    |
| deepcopy                         | 145 us                                                         | 117 us: 1.24x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 245 ms: 1.20x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 822 ns: 1.15x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.40 ms: 1.15x faster                                                    |
| go                               | 72.6 ms                                                        | 63.3 ms: 1.15x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 54.7 ms: 1.14x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.42 ms: 1.14x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 913 ms: 1.09x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.08x faster                                                     |
| pyflate                          | 222 ms                                                         | 206 ms: 1.08x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.4 ms: 1.08x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 59.3 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 15.3 us: 1.07x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 21.9 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 997 ms: 1.05x faster                                                     |
| pidigits                         | 166 ms                                                         | 158 ms: 1.05x faster                                                     |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.04 sec: 1.04x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 91.9 ms: 1.03x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 188 ms: 1.03x faster                                                     |
| float                            | 31.4 ms                                                        | 30.7 ms: 1.02x faster                                                    |
| pycparser                        | 470 ms                                                         | 460 ms: 1.02x faster                                                     |
| async_generators                 | 193 ms                                                         | 189 ms: 1.02x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.27 us: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 222 ms: 1.01x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 11.3 ms: 1.02x slower                                                    |
| sphinx                           | 409 ms                                                         | 416 ms: 1.02x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 39.2 ms: 1.04x slower                                                    |
| shortest_path                    | 225 ms                                                         | 235 ms: 1.04x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.8 ms: 1.05x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.16 ms: 1.06x slower                                                    |
| connected_components             | 208 ms                                                         | 221 ms: 1.06x slower                                                     |
| genshi_xml                       | 21.4 ms                                                        | 22.9 ms: 1.07x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.6 us: 1.07x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 5.00 ms: 1.07x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 47.9 ms: 1.08x slower                                                    |
| 2to3                             | 112 ms                                                         | 121 ms: 1.08x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 27.5 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 226 ms: 1.09x slower                                                     |
| richards                         | 22.1 ms                                                        | 24.0 ms: 1.09x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.48 ms: 1.10x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.37 ms: 1.10x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 52.9 ms: 1.10x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.3 ms: 1.10x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.34 ms: 1.11x slower                                                    |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 111 us: 1.11x slower                                                     |
| fannkuch                         | 179 ms                                                         | 200 ms: 1.12x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 115 ms: 1.13x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.21 ms: 1.13x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.54 us: 1.13x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 365 ms: 1.13x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 743 ms: 1.14x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 74.0 us: 1.14x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 59.9 ms: 1.15x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 49.5 ms: 1.15x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.81 us: 1.15x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 55.0 ms: 1.15x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 42.9 ms: 1.15x slower                                                    |
| genshi_text                      | 9.97 ms                                                        | 11.5 ms: 1.16x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 152 us: 1.17x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.3 ms: 1.17x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 112 ms: 1.17x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 47.7 ns: 1.17x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.71 ms: 1.18x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 35.4 ms: 1.19x slower                                                    |
| many_optionals                   | 200 us                                                         | 238 us: 1.19x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 190 ms: 1.19x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 147 ms: 1.19x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.23 ms: 1.21x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 53.1 ms: 1.22x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.18 ms: 1.22x slower                                                    |
| chaos                            | 24.3 ms                                                        | 30.1 ms: 1.24x slower                                                    |
| coverage                         | 31.2 ms                                                        | 39.3 ms: 1.26x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.61 us: 1.27x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 42.7 ms: 1.27x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.63 ms: 1.28x slower                                                    |
| raytrace                         | 109 ms                                                         | 140 ms: 1.29x slower                                                     |
| django_template                  | 12.5 ms                                                        | 16.2 ms: 1.30x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 56.6 ms: 1.32x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 8.69 ms: 1.39x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 578 us: 1.40x slower                                                     |
| nbody                            | 42.5 ms                                                        | 66.1 ms: 1.55x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 81.0 ms: 2.80x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                             |

Benchmark hidden because not significant (1): json
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250329-3.14.0a6+-9c1e85f-NOGIL/bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.003x faster

# HPT report

- Reliability score: 65.57% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.17x