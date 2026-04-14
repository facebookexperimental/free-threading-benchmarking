# Results vs. 3.13.0rc2

- fork: python
- ref: eb4c78df07c87237f97e
- machine: darwin-arm64
- commit hash: eb4c78d
- commit date: 2026-04-13
- overall geometric mean: 1.012x faster
- HPT reliability: 52.96%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8+-eb4c78d |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 123 ms: 1.10x slower                                                     |
| docutils       | 1.05 sec                                                       | 997 ms: 1.05x faster                                                     |
| sphinx         | 409 ms                                                         | 425 ms: 1.04x slower                                                     |
| Geometric mean | (ref)                                                          | 1.02x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8+-eb4c78d |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 242 ms: 2.17x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 241 ms: 2.16x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 240 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 245 ms: 1.58x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 108 ms: 1.22x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.22x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 257 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                     |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.00x faster                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 47.7 ms: 1.10x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.6 ms: 3.24x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.12x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8+-eb4c78d |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.7 ms: 1.09x faster                                                    |
| pidigits       | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| nbody          | 42.5 ms                                                        | 57.0 ms: 1.34x slower                                                    |
| Geometric mean | (ref)                                                          | 1.07x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8+-eb4c78d |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.28 ms: 1.15x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 96.5 ms: 1.02x slower                                                    |
| regex_compile  | 47.9 ms                                                        | 51.3 ms: 1.07x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8+-eb4c78d |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 37.9 ms: 1.22x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.85 ms: 1.21x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 890 ms: 1.12x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 56.8 ms: 1.10x faster                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.8 ms: 1.06x slower                                                    |
| json_loads           | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.0 ms: 1.07x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 112 us: 1.12x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 149 us: 1.14x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8+-eb4c78d |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.86 ms: 1.14x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.15 ms: 1.20x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.17x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8+-eb4c78d |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 22.9 ms: 1.07x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                    |
| django_template | 12.5 ms                                                        | 15.8 ms: 1.26x slower                                                    |
| mako            | 4.41 ms                                                        | 5.80 ms: 1.31x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.19x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8+-eb4c78d |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 814 us: 2.51x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 242 ms: 2.17x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 241 ms: 2.16x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 519 us: 1.91x faster                                                     |
| mdp                              | 1.06 sec                                                       | 614 ms: 1.72x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 240 ms: 1.69x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 245 ms: 1.58x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.14 ms: 1.51x faster                                                    |
| k_core                           | 1.46 sec                                                       | 998 ms: 1.47x faster                                                     |
| deepcopy                         | 145 us                                                         | 109 us: 1.33x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 144 ms: 1.29x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 13.2 us: 1.25x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 108 ms: 1.22x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 117 ms: 1.22x faster                                                     |
| xml_etree_iterparse              | 46.1 ms                                                        | 37.9 ms: 1.22x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.85 ms: 1.21x faster                                                    |
| go                               | 72.6 ms                                                        | 60.1 ms: 1.21x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 787 ns: 1.20x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 257 ms: 1.17x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.28 ms: 1.15x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 55.6 ms: 1.15x faster                                                    |
| pyflate                          | 222 ms                                                         | 193 ms: 1.15x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 890 ms: 1.12x faster                                                     |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 266 ms: 1.10x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.18 us: 1.10x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 56.8 ms: 1.10x faster                                                    |
| float                            | 31.4 ms                                                        | 28.7 ms: 1.09x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 113 ms: 1.08x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                     |
| docutils                         | 1.05 sec                                                       | 997 ms: 1.05x faster                                                     |
| async_generators                 | 193 ms                                                         | 186 ms: 1.04x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.5 ms: 1.03x faster                                                    |
| fannkuch                         | 179 ms                                                         | 174 ms: 1.03x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                    |
| pycparser                        | 470 ms                                                         | 462 ms: 1.02x faster                                                     |
| telco                            | 3.07 ms                                                        | 3.03 ms: 1.01x faster                                                    |
| pidigits                         | 166 ms                                                         | 164 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 224 ms: 1.00x faster                                                     |
| dask                             | 525 ms                                                         | 529 ms: 1.01x slower                                                     |
| json                             | 1.94 ms                                                        | 1.96 ms: 1.01x slower                                                    |
| regex_dna                        | 94.6 ms                                                        | 96.5 ms: 1.02x slower                                                    |
| sphinx                           | 409 ms                                                         | 425 ms: 1.04x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 129 ms: 1.04x slower                                                     |
| pprint_safe_repr                 | 322 ms                                                         | 336 ms: 1.04x slower                                                     |
| pprint_pformat                   | 650 ms                                                         | 682 ms: 1.05x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.8 ms: 1.06x slower                                                    |
| logging_silent                   | 40.6 ns                                                        | 43.0 ns: 1.06x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.5 us: 1.06x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.38 us: 1.06x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.0 ms: 1.07x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.6 ms: 1.07x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 51.3 ms: 1.07x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 22.9 ms: 1.07x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.62 us: 1.07x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.20 ms: 1.09x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 27.0 ms: 1.09x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 47.7 ms: 1.10x slower                                                    |
| 2to3                             | 112 ms                                                         | 123 ms: 1.10x slower                                                     |
| nqueens                          | 37.2 ms                                                        | 41.1 ms: 1.10x slower                                                    |
| pylint                           | 106 ms                                                         | 118 ms: 1.12x slower                                                     |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.4 ms: 1.12x slower                                                    |
| shortest_path                    | 225 ms                                                         | 252 ms: 1.12x slower                                                     |
| unpickle_pure_python             | 99.5 us                                                        | 112 us: 1.12x slower                                                     |
| thrift                           | 309 us                                                         | 347 us: 1.12x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.22 ms: 1.13x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.65 ms: 1.14x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.86 ms: 1.14x slower                                                    |
| pickle_pure_python               | 130 us                                                         | 149 us: 1.14x slower                                                     |
| typing_runtime_protocols         | 64.6 us                                                        | 73.9 us: 1.14x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.8 ms: 1.14x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 111 ms: 1.16x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 243 ms: 1.17x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 51.2 ms: 1.17x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 61.3 ms: 1.17x slower                                                    |
| connected_components             | 208 ms                                                         | 244 ms: 1.17x slower                                                     |
| raytrace                         | 109 ms                                                         | 129 ms: 1.18x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                     |
| meteor_contest                   | 47.9 ms                                                        | 56.8 ms: 1.19x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.15 ms: 1.20x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.18 us: 1.20x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.5 ms: 1.24x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.22 ms: 1.25x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.8 ms: 1.26x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 130 ms: 1.27x slower                                                     |
| bench_mp_pool                    | 37.8 ms                                                        | 48.1 ms: 1.27x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 55.0 ms: 1.28x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.80 ms: 1.31x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 44.3 ms: 1.32x slower                                                    |
| many_optionals                   | 200 us                                                         | 267 us: 1.33x slower                                                     |
| nbody                            | 42.5 ms                                                        | 57.0 ms: 1.34x slower                                                    |
| generators                       | 15.7 ms                                                        | 21.2 ms: 1.35x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 564 us: 1.37x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 93.6 ms: 3.24x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.01x faster                                                             |

Benchmark hidden because not significant (1): html5lib
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260413-3.15.0a8+-eb4c78d-NOGIL/bm-20260413-macm4pro-arm64-python-eb4c78df07c87237f97e-3.15.0a8+-eb4c78d.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.012x faster

# HPT report

- Reliability score: 52.96% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.32x