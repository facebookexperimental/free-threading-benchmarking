# Results vs. 3.13.0rc2

- fork: python
- ref: 8a00c9a4d2ce9d373b13
- machine: darwin-arm64
- commit hash: 8a00c9a
- commit date: 2025-03-27
- overall geometric mean: 1.040x slower
- HPT reliability: 99.23%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 116 ms: 1.04x slower                                                     |
| docutils       | 1.05 sec                                                       | 1.08 sec: 1.03x slower                                                   |
| html5lib       | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                    |
| sphinx         | 409 ms                                                         | 426 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 267 ms: 1.97x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 269 ms: 1.93x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 271 ms: 1.49x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 272 ms: 1.42x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 118 ms: 1.21x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 156 ms: 1.19x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 113 ms: 1.17x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 158 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 267 ms: 1.13x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                     |
| async_generators                 | 193 ms                                                         | 180 ms: 1.08x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 116 ms: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 45.5 ms: 1.05x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 11.6 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 137 ms: 1.34x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.1 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| float          | 31.4 ms                                                        | 34.7 ms: 1.10x slower                                                    |
| nbody          | 42.5 ms                                                        | 58.1 ms: 1.37x slower                                                    |
| Geometric mean | (ref)                                                          | 1.14x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.54 ms: 1.05x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 93.6 ms: 1.01x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 52.1 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                          | 1.01x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 62.4 ms                                                        | 59.8 ms: 1.04x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 979 ms: 1.02x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 47.0 ms: 1.02x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 38.9 ms: 1.09x slower                                                    |
| json_dumps           | 4.65 ms                                                        | 5.18 ms: 1.11x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.13x slower                                                     |
| xml_etree_process    | 25.4 ms                                                        | 28.6 ms: 1.13x slower                                                    |
| pickle_pure_python   | 130 us                                                         | 152 us: 1.17x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.70 ms: 1.01x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.46 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.05x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.3 ms: 1.09x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.5 ms: 1.15x slower                                                    |
| mako            | 4.41 ms                                                        | 5.17 ms: 1.17x slower                                                    |
| django_template | 12.5 ms                                                        | 17.0 ms: 1.36x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.19x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 267 ms: 1.97x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 269 ms: 1.93x faster                                                     |
| mdp                              | 1.06 sec                                                       | 577 ms: 1.83x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 271 ms: 1.49x faster                                                     |
| k_core                           | 1.46 sec                                                       | 993 ms: 1.47x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 272 ms: 1.42x faster                                                     |
| deepcopy                         | 145 us                                                         | 117 us: 1.24x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 118 ms: 1.21x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 156 ms: 1.19x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 13.8 us: 1.19x faster                                                    |
| async_tree_none_tg               | 133 ms                                                         | 113 ms: 1.17x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 158 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 267 ms: 1.13x faster                                                     |
| go                               | 72.6 ms                                                        | 64.4 ms: 1.13x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.0 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 910 us: 1.09x faster                                                     |
| async_generators                 | 193 ms                                                         | 180 ms: 1.08x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.21 us: 1.07x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 10.2 ms: 1.05x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.54 ms: 1.05x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 116 ms: 1.05x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 59.8 ms: 1.04x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 62.1 ms: 1.03x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 979 ms: 1.02x faster                                                     |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 93.6 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 223 ms: 1.01x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 192 ms: 1.01x faster                                                     |
| shortest_path                    | 225 ms                                                         | 225 ms: 1.00x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 38.0 ms: 1.00x slower                                                    |
| connected_components             | 208 ms                                                         | 209 ms: 1.00x slower                                                     |
| python_startup                   | 8.63 ms                                                        | 8.70 ms: 1.01x slower                                                    |
| pyflate                          | 222 ms                                                         | 224 ms: 1.01x slower                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 47.0 ms: 1.02x slower                                                    |
| sqlite_synth                     | 948 ns                                                         | 966 ns: 1.02x slower                                                     |
| json                             | 1.94 ms                                                        | 1.98 ms: 1.02x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 23.7 ms: 1.02x slower                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 2.18 sec: 1.02x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.08 sec: 1.03x slower                                                   |
| 2to3                             | 112 ms                                                         | 116 ms: 1.04x slower                                                     |
| sphinx                           | 409 ms                                                         | 426 ms: 1.04x slower                                                     |
| sqlalchemy_declarative           | 44.4 ms                                                        | 46.4 ms: 1.05x slower                                                    |
| pathlib                          | 11.1 ms                                                        | 11.7 ms: 1.05x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 45.5 ms: 1.05x slower                                                    |
| telco                            | 3.07 ms                                                        | 3.24 ms: 1.06x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.1 ms: 1.06x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 438 us: 1.06x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 51.5 ms: 1.08x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.92 ms: 1.08x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 11.6 ms: 1.08x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 6.46 ms: 1.09x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 38.9 ms: 1.09x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 52.1 ms: 1.09x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.3 ms: 1.09x slower                                                    |
| richards                         | 22.1 ms                                                        | 24.2 ms: 1.10x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.1 ms: 1.10x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 71.1 us: 1.10x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 57.7 ms: 1.10x slower                                                    |
| sqlalchemy_imperative            | 5.00 ms                                                        | 5.52 ms: 1.10x slower                                                    |
| pycparser                        | 470 ms                                                         | 519 ms: 1.10x slower                                                     |
| float                            | 31.4 ms                                                        | 34.7 ms: 1.10x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.34 ms: 1.11x slower                                                    |
| json_dumps                       | 4.65 ms                                                        | 5.18 ms: 1.11x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 107 ms: 1.12x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 179 ms: 1.12x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.6 ms: 1.12x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.13x slower                                                     |
| xml_etree_process                | 25.4 ms                                                        | 28.6 ms: 1.13x slower                                                    |
| gc_traversal                     | 2.04 ms                                                        | 2.31 ms: 1.13x slower                                                    |
| pylint                           | 106 ms                                                         | 121 ms: 1.14x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.27 ms: 1.15x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.81 us: 1.15x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 748 ms: 1.15x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.5 ms: 1.15x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 143 ms: 1.15x slower                                                     |
| fannkuch                         | 179 ms                                                         | 207 ms: 1.16x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 373 ms: 1.16x slower                                                     |
| logging_simple                   | 2.24 us                                                        | 2.60 us: 1.16x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 152 us: 1.17x slower                                                     |
| mako                             | 4.41 ms                                                        | 5.17 ms: 1.17x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 48.1 ns: 1.18x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 51.9 ms: 1.19x slower                                                    |
| generators                       | 15.7 ms                                                        | 18.7 ms: 1.19x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 248 ms: 1.19x slower                                                     |
| deltablue                        | 1.45 ms                                                        | 1.73 ms: 1.19x slower                                                    |
| many_optionals                   | 200 us                                                         | 242 us: 1.21x slower                                                     |
| chaos                            | 24.3 ms                                                        | 29.4 ms: 1.21x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 45.3 ms: 1.22x slower                                                    |
| raytrace                         | 109 ms                                                         | 132 ms: 1.22x slower                                                     |
| comprehensions                   | 6.80 us                                                        | 8.42 us: 1.24x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 41.8 ms: 1.24x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 55.8 ms: 1.31x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 137 ms: 1.34x slower                                                     |
| django_template                  | 12.5 ms                                                        | 17.0 ms: 1.36x slower                                                    |
| nbody                            | 42.5 ms                                                        | 58.1 ms: 1.37x slower                                                    |
| subparsers                       | 6.26 ms                                                        | 9.05 ms: 1.44x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.1 ms: 3.22x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.04x slower                                                             |
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, gevent_hub, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http
Ignored benchmarks (4) of results/bm-20250327-3.14.0a6+-8a00c9a/bm-20250327-macm4pro-arm64-python-8a00c9a4d2ce9d373b13-3.14.0a6+-8a00c9a.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.040x slower

# HPT report

- Reliability score: 99.23% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.08x