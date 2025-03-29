# Results vs. 3.13.0rc2

- fork: python
- ref: 9c1e85fd64cf6a85f7c9
- machine: darwin-arm64
- commit hash: 9c1e85f
- commit date: 2025-03-29
- overall geometric mean: 1.037x slower
- HPT reliability: 98.89%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 116 ms: 1.04x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.08 sec: 1.03x slower                                                   |
| html5lib       | 23.1 ms                                                        | 23.6 ms: 1.02x slower                                                    |
| sphinx         | 409 ms                                                         | 423 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 268 ms: 1.96x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 271 ms: 1.92x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 271 ms: 1.50x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 270 ms: 1.43x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 118 ms: 1.21x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 155 ms: 1.20x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 113 ms: 1.17x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 157 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 266 ms: 1.13x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                     |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 116 ms: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.3 ms: 1.07x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 11.7 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 137 ms: 1.34x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.2 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| float          | 31.4 ms                                                        | 34.6 ms: 1.10x slower                                                    |
| nbody          | 42.5 ms                                                        | 58.3 ms: 1.37x slower                                                    |
| Geometric mean | (ref)                                                          | 1.14x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 92.4 ms: 1.02x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 52.3 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 62.4 ms                                                        | 60.5 ms: 1.03x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 970 ms: 1.03x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 47.1 ms: 1.02x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.4 us: 1.06x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 38.9 ms: 1.09x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.17 ms: 1.11x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 111 us: 1.11x slower                                                     |
| xml_etree_process    | 25.4 ms                                                        | 28.4 ms: 1.12x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 152 us: 1.17x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.68 ms: 1.01x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.44 ms: 1.08x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.3 ms: 1.09x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                    |
| mako            | 4.41 ms                                                        | 5.21 ms: 1.18x slower                                                    |
| django_template | 12.5 ms                                                        | 17.0 ms: 1.36x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.19x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 268 ms: 1.96x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 271 ms: 1.92x faster                                                     |
| mdp                              | 1.06 sec                                                       | 578 ms: 1.83x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 271 ms: 1.50x faster                                                     |
| k_core                           | 1.46 sec                                                       | 991 ms: 1.48x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 270 ms: 1.43x faster                                                     |
| deepcopy                         | 145 us                                                         | 117 us: 1.24x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 118 ms: 1.21x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 13.7 us: 1.20x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 155 ms: 1.20x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 113 ms: 1.17x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 157 ms: 1.17x faster                                                     |
| go                               | 72.6 ms                                                        | 63.9 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 266 ms: 1.13x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.43 ms: 1.13x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.0 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 903 us: 1.10x faster                                                     |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 61.1 ms: 1.05x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 116 ms: 1.05x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 60.5 ms: 1.03x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 970 ms: 1.03x faster                                                     |
| pidigits                         | 166 ms                                                         | 162 ms: 1.03x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 92.4 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 221 ms: 1.02x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.28 us: 1.01x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 37.7 ms: 1.00x faster                                                    |
| pyflate                          | 222 ms                                                         | 223 ms: 1.00x slower                                                     |
| connected_components             | 208 ms                                                         | 209 ms: 1.00x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.68 ms: 1.01x slower                                                    |
| shortest_path                    | 225 ms                                                         | 228 ms: 1.02x slower                                                     |
| sqlite_synth                     | 948 ns                                                         | 964 ns: 1.02x slower                                                     |
| html5lib                         | 23.1 ms                                                        | 23.6 ms: 1.02x slower                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 47.1 ms: 1.02x slower                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.18 sec: 1.02x slower                                                   |
| json                             | 1.94 ms                                                        | 1.99 ms: 1.03x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.10 ms: 1.03x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.08 sec: 1.03x slower                                                   |
| sphinx                           | 409 ms                                                         | 423 ms: 1.04x slower                                                     |
| 2to3                             | 112 ms                                                         | 116 ms: 1.04x slower                                                     |
| pathlib                          | 11.1 ms                                                        | 11.6 ms: 1.04x slower                                                    |
| sqlalchemy_declarative           | 44.4 ms                                                        | 46.1 ms: 1.04x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.23 ms: 1.05x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.4 us: 1.06x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.0 ms: 1.06x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 51.3 ms: 1.07x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 441 us: 1.07x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 46.3 ms: 1.07x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.91 ms: 1.08x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.44 ms: 1.08x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 11.7 ms: 1.08x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 38.9 ms: 1.09x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.44 ms: 1.09x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.3 ms: 1.09x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 52.3 ms: 1.09x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 70.7 us: 1.09x slower                                                    |
| pycparser                        | 470 ms                                                         | 514 ms: 1.09x slower                                                     |
| richards_super                   | 24.7 ms                                                        | 27.0 ms: 1.10x slower                                                    |
| richards                         | 22.1 ms                                                        | 24.2 ms: 1.10x slower                                                    |
| float                            | 31.4 ms                                                        | 34.6 ms: 1.10x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.33 ms: 1.11x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 58.0 ms: 1.11x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 5.17 ms: 1.11x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 111 us: 1.11x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.4 ms: 1.12x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 28.4 ms: 1.12x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 179 ms: 1.12x slower                                                     |
| sympy_str                        | 95.5 ms                                                        | 107 ms: 1.12x slower                                                     |
| pylint                           | 106 ms                                                         | 120 ms: 1.14x slower                                                     |
| fannkuch                         | 179 ms                                                         | 204 ms: 1.14x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.4 ms: 1.14x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.27 ms: 1.15x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 747 ms: 1.15x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.81 us: 1.15x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 371 ms: 1.15x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.58 us: 1.15x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 144 ms: 1.16x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 152 us: 1.17x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 51.6 ms: 1.18x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.21 ms: 1.18x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 48.1 ns: 1.19x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 247 ms: 1.19x slower                                                     |
| generators                       | 15.7 ms                                                        | 18.6 ms: 1.19x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.73 ms: 1.19x slower                                                    |
| many_optionals                   | 200 us                                                         | 241 us: 1.20x slower                                                     |
| raytrace                         | 109 ms                                                         | 132 ms: 1.21x slower                                                     |
| chaos                            | 24.3 ms                                                        | 29.5 ms: 1.22x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 45.4 ms: 1.22x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.46 us: 1.24x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 41.9 ms: 1.25x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 55.4 ms: 1.30x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 137 ms: 1.34x slower                                                     |
| django_template                  | 12.5 ms                                                        | 17.0 ms: 1.36x slower                                                    |
| nbody                            | 42.5 ms                                                        | 58.3 ms: 1.37x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.02 ms: 1.44x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.2 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x slower                                                             |
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250329-3.14.0a6+-9c1e85f/bm-20250329-macm4pro-arm64-python-9c1e85fd64cf6a85f7c9-3.14.0a6+-9c1e85f.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.037x slower

# HPT report

- Reliability score: 98.89% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.08x