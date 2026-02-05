# Results vs. 3.13.0rc2

- fork: python
- ref: b6d8aa436b0108fcc90c
- machine: darwin-arm64
- commit hash: b6d8aa4
- commit date: 2026-02-04
- overall geometric mean: 1.110x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 107 ms: 1.04x faster                                                     |
| docutils       | 1.05 sec                                                       | 975 ms: 1.07x faster                                                     |
| html5lib       | 23.1 ms                                                        | 20.7 ms: 1.12x faster                                                    |
| sphinx         | 409 ms                                                         | 378 ms: 1.08x faster                                                     |
| Geometric mean | (ref)                                                          | 1.08x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 213 ms: 2.47x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 214 ms: 2.43x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 222 ms: 1.82x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 220 ms: 1.76x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 98.9 ms: 1.44x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 133 ms: 1.39x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 95.4 ms: 1.39x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 135 ms: 1.37x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 243 ms: 1.24x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 247 ms: 1.19x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 104 ms: 1.17x faster                                                     |
| async_generators                 | 193 ms                                                         | 169 ms: 1.14x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 38.8 ms: 1.11x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 181 ms: 1.07x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 211 ms: 1.06x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 116 ms: 1.13x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.2 ms: 2.67x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.24x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 27.6 ms: 1.14x faster                                                    |
| pidigits       | 166 ms                                                         | 156 ms: 1.07x faster                                                     |
| nbody          | 42.5 ms                                                        | 43.3 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.41 ms: 1.14x faster                                                    |
| regex_v8       | 10.7 ms                                                        | 9.53 ms: 1.12x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 43.8 ms: 1.09x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 91.2 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                          | 1.10x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.71 ms: 1.25x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 814 ms: 1.23x faster                                                     |
| xml_etree_iterparse  | 46.1 ms                                                        | 38.6 ms: 1.19x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 33.8 ms: 1.06x faster                                                    |
| xml_etree_process    | 25.4 ms                                                        | 24.0 ms: 1.06x faster                                                    |
| json_loads           | 10.8 us                                                        | 10.3 us: 1.05x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 95.3 us: 1.04x faster                                                    |
| xml_etree_parse      | 62.4 ms                                                        | 60.7 ms: 1.03x faster                                                    |
| pickle_pure_python   | 130 us                                                         | 137 us: 1.05x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.09x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 8.65 ms: 1.00x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 6.25 ms: 1.05x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.03x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 9.97 ms                                                        | 9.45 ms: 1.06x faster                                                    |
| genshi_xml      | 21.4 ms                                                        | 20.4 ms: 1.05x faster                                                    |
| mako            | 4.41 ms                                                        | 4.57 ms: 1.04x slower                                                    |
| django_template | 12.5 ms                                                        | 14.3 ms: 1.15x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.02x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 213 ms: 2.47x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 214 ms: 2.43x faster                                                     |
| mdp                              | 1.06 sec                                                       | 521 ms: 2.03x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 222 ms: 1.82x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 220 ms: 1.76x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 3.81 ms: 1.64x faster                                                    |
| k_core                           | 1.46 sec                                                       | 892 ms: 1.64x faster                                                     |
| deepcopy                         | 145 us                                                         | 94.7 us: 1.53x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 11.1 us: 1.49x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 98.9 ms: 1.44x faster                                                    |
| go                               | 72.6 ms                                                        | 50.9 ms: 1.43x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 133 ms: 1.39x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 95.4 ms: 1.39x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 135 ms: 1.37x faster                                                     |
| scimark_sor                      | 64.0 ms                                                        | 49.3 ms: 1.30x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.71 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 243 ms: 1.24x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.05 us: 1.24x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 814 ms: 1.23x faster                                                     |
| pyflate                          | 222 ms                                                         | 185 ms: 1.20x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.6 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 247 ms: 1.19x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 104 ms: 1.17x faster                                                     |
| richards                         | 22.1 ms                                                        | 19.3 ms: 1.14x faster                                                    |
| async_generators                 | 193 ms                                                         | 169 ms: 1.14x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.41 ms: 1.14x faster                                                    |
| richards_super                   | 24.7 ms                                                        | 21.7 ms: 1.14x faster                                                    |
| float                            | 31.4 ms                                                        | 27.6 ms: 1.14x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 878 us: 1.13x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.53 ms: 1.12x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 20.7 ms: 1.12x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.8 ms: 1.11x faster                                                    |
| telco                            | 3.07 ms                                                        | 2.75 ms: 1.11x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 38.8 ms: 1.11x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                                   |
| regex_compile                    | 47.9 ms                                                        | 43.8 ms: 1.09x faster                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 297 ms: 1.08x faster                                                     |
| fannkuch                         | 179 ms                                                         | 165 ms: 1.08x faster                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 27.7 ms: 1.08x faster                                                    |
| sphinx                           | 409 ms                                                         | 378 ms: 1.08x faster                                                     |
| pprint_pformat                   | 650 ms                                                         | 603 ms: 1.08x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.0 ms: 1.07x faster                                                    |
| docutils                         | 1.05 sec                                                       | 975 ms: 1.07x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 181 ms: 1.07x faster                                                     |
| hexiom                           | 2.85 ms                                                        | 2.67 ms: 1.07x faster                                                    |
| pidigits                         | 166 ms                                                         | 156 ms: 1.07x faster                                                     |
| json                             | 1.94 ms                                                        | 1.82 ms: 1.06x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 211 ms: 1.06x faster                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 33.8 ms: 1.06x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 24.0 ms: 1.06x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.5 ms: 1.06x faster                                                    |
| genshi_text                      | 9.97 ms                                                        | 9.45 ms: 1.06x faster                                                    |
| json_loads                       | 10.8 us                                                        | 10.3 us: 1.05x faster                                                    |
| pycparser                        | 470 ms                                                         | 448 ms: 1.05x faster                                                     |
| logging_simple                   | 2.24 us                                                        | 2.13 us: 1.05x faster                                                    |
| logging_format                   | 2.45 us                                                        | 2.33 us: 1.05x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 61.7 us: 1.05x faster                                                    |
| genshi_xml                       | 21.4 ms                                                        | 20.4 ms: 1.05x faster                                                    |
| 2to3                             | 112 ms                                                         | 107 ms: 1.04x faster                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 95.3 us: 1.04x faster                                                    |
| deltablue                        | 1.45 ms                                                        | 1.39 ms: 1.04x faster                                                    |
| thrift                           | 309 us                                                         | 297 us: 1.04x faster                                                     |
| gc_traversal                     | 2.04 ms                                                        | 1.97 ms: 1.04x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 91.2 ms: 1.04x faster                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 7.26 ms: 1.04x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 120 ms: 1.03x faster                                                     |
| sqlite_synth                     | 948 ns                                                         | 920 ns: 1.03x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 60.7 ms: 1.03x faster                                                    |
| coverage                         | 31.2 ms                                                        | 30.6 ms: 1.02x faster                                                    |
| meteor_contest                   | 47.9 ms                                                        | 47.4 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 523 ms: 1.00x faster                                                     |
| shortest_path                    | 225 ms                                                         | 224 ms: 1.00x faster                                                     |
| python_startup                   | 8.63 ms                                                        | 8.65 ms: 1.00x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 43.0 ms: 1.01x slower                                                    |
| spectral_norm                    | 43.7 ms                                                        | 44.4 ms: 1.02x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 37.9 ms: 1.02x slower                                                    |
| nbody                            | 42.5 ms                                                        | 43.3 ms: 1.02x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 97.5 ms: 1.02x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 53.5 ms: 1.02x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 6.98 us: 1.03x slower                                                    |
| chaos                            | 24.3 ms                                                        | 25.1 ms: 1.03x slower                                                    |
| mako                             | 4.41 ms                                                        | 4.57 ms: 1.04x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 166 ms: 1.04x slower                                                     |
| raytrace                         | 109 ms                                                         | 114 ms: 1.04x slower                                                     |
| bench_thread_pool                | 412 us                                                         | 430 us: 1.04x slower                                                     |
| pylint                           | 106 ms                                                         | 110 ms: 1.05x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 137 us: 1.05x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 6.25 ms: 1.05x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.87 ms: 1.05x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 36.7 ms: 1.09x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 227 ms: 1.09x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 116 ms: 1.13x slower                                                     |
| generators                       | 15.7 ms                                                        | 17.8 ms: 1.13x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 43.3 ms: 1.15x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.3 ms: 1.15x slower                                                    |
| many_optionals                   | 200 us                                                         | 235 us: 1.17x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 77.2 ms: 2.67x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.11x faster                                                             |

Benchmark hidden because not significant (2): logging_silent, connected_components
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260204-3.15.0a5+-b6d8aa4/bm-20260204-macm4pro-arm64-python-b6d8aa436b0108fcc90c-3.15.0a5+-b6d8aa4.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.110x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.18x