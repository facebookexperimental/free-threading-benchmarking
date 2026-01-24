# Results vs. 3.13.0rc2

- fork: python
- ref: 58ccf21cbb92e0e99cbe
- machine: darwin-arm64
- commit hash: 58ccf21
- commit date: 2026-01-23
- overall geometric mean: 1.028x faster
- HPT reliability: 70.22%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.30x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 118 ms: 1.06x slower                                                     |
| docutils       | 1.05 sec                                                       | 992 ms: 1.05x faster                                                     |
| sphinx         | 409 ms                                                         | 415 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                          | 1.00x slower                                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 241 ms: 2.16x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 244 ms: 2.15x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 234 ms: 1.73x faster                                                     |
| async_tree_io                    | 386 ms                                                         | 253 ms: 1.53x faster                                                     |
| async_tree_memoization_tg        | 186 ms                                                         | 143 ms: 1.30x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 260 ms: 1.13x faster                                                     |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                     |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 45.9 ms: 1.06x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.24x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.0 ms: 3.18x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.14x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                    |
| pidigits       | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| nbody          | 42.5 ms                                                        | 55.1 ms: 1.30x slower                                                    |
| Geometric mean | (ref)                                                          | 1.04x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.20 ms: 1.16x faster                                                    |
| regex_effbot   | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| regex_dna      | 94.6 ms                                                        | 92.7 ms: 1.02x faster                                                    |
| regex_compile  | 47.9 ms                                                        | 50.4 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 46.1 ms                                                        | 38.3 ms: 1.20x faster                                                    |
| json_dumps           | 4.65 ms                                                        | 3.92 ms: 1.19x faster                                                    |
| tomli_loads          | 1000 ms                                                        | 874 ms: 1.14x faster                                                     |
| xml_etree_parse      | 62.4 ms                                                        | 58.6 ms: 1.06x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.1 us: 1.02x slower                                                    |
| xml_etree_generate   | 35.8 ms                                                        | 37.4 ms: 1.04x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 27.1 ms: 1.07x slower                                                    |
| unpickle_pure_python | 99.5 us                                                        | 108 us: 1.09x slower                                                     |
| pickle_pure_python   | 130 us                                                         | 145 us: 1.11x slower                                                     |
| Geometric mean       | (ref)                                                          | 1.03x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 9.66 ms: 1.12x slower                                                    |
| python_startup_no_site | 5.95 ms                                                        | 7.02 ms: 1.18x slower                                                    |
| Geometric mean         | (ref)                                                          | 1.15x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|-----------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.4 ms                                                        | 23.0 ms: 1.08x slower                                                    |
| genshi_text     | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                    |
| django_template | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                    |
| mako            | 4.41 ms                                                        | 5.42 ms: 1.23x slower                                                    |
| Geometric mean  | (ref)                                                          | 1.16x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21 |
|----------------------------------|:--------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 785 us: 2.60x faster                                                     |
| async_tree_eager_io_tg           | 521 ms                                                         | 241 ms: 2.16x faster                                                     |
| async_tree_eager_io              | 525 ms                                                         | 244 ms: 2.15x faster                                                     |
| create_gc_cycles                 | 993 us                                                         | 513 us: 1.94x faster                                                     |
| mdp                              | 1.06 sec                                                       | 598 ms: 1.77x faster                                                     |
| async_tree_io_tg                 | 405 ms                                                         | 234 ms: 1.73x faster                                                     |
| subparsers                       | 6.26 ms                                                        | 4.02 ms: 1.56x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 253 ms: 1.53x faster                                                     |
| k_core                           | 1.46 sec                                                       | 985 ms: 1.49x faster                                                     |
| deepcopy                         | 145 us                                                         | 106 us: 1.37x faster                                                     |
| deepcopy_memo                    | 16.5 us                                                        | 12.4 us: 1.33x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 143 ms: 1.30x faster                                                     |
| async_tree_none_tg               | 133 ms                                                         | 103 ms: 1.29x faster                                                     |
| async_tree_none                  | 142 ms                                                         | 112 ms: 1.27x faster                                                     |
| async_tree_memoization           | 184 ms                                                         | 150 ms: 1.23x faster                                                     |
| go                               | 72.6 ms                                                        | 59.4 ms: 1.22x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 38.3 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 253 ms: 1.19x faster                                                     |
| json_dumps                       | 4.65 ms                                                        | 3.92 ms: 1.19x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 54.7 ms: 1.17x faster                                                    |
| pyflate                          | 222 ms                                                         | 190 ms: 1.17x faster                                                     |
| regex_v8                         | 10.7 ms                                                        | 9.20 ms: 1.16x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 817 ns: 1.16x faster                                                     |
| tomli_loads                      | 1000 ms                                                        | 874 ms: 1.14x faster                                                     |
| deepcopy_reduce                  | 1.30 us                                                        | 1.14 us: 1.14x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.42 ms: 1.13x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 260 ms: 1.13x faster                                                     |
| float                            | 31.4 ms                                                        | 28.5 ms: 1.10x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.96 sec: 1.09x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 112 ms: 1.09x faster                                                     |
| dulwich_log                      | 19.8 ms                                                        | 18.2 ms: 1.09x faster                                                    |
| async_generators                 | 193 ms                                                         | 180 ms: 1.07x faster                                                     |
| xml_etree_parse                  | 62.4 ms                                                        | 58.6 ms: 1.06x faster                                                    |
| docutils                         | 1.05 sec                                                       | 992 ms: 1.05x faster                                                     |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                     |
| fannkuch                         | 179 ms                                                         | 171 ms: 1.05x faster                                                     |
| pathlib                          | 11.1 ms                                                        | 10.7 ms: 1.04x faster                                                    |
| pidigits                         | 166 ms                                                         | 159 ms: 1.04x faster                                                     |
| telco                            | 3.07 ms                                                        | 2.98 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 220 ms: 1.02x faster                                                     |
| pycparser                        | 470 ms                                                         | 459 ms: 1.02x faster                                                     |
| regex_dna                        | 94.6 ms                                                        | 92.7 ms: 1.02x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.6 ms: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.92 ms: 1.01x faster                                                    |
| dask                             | 525 ms                                                         | 528 ms: 1.01x slower                                                     |
| sphinx                           | 409 ms                                                         | 415 ms: 1.01x slower                                                     |
| json_loads                       | 10.8 us                                                        | 11.1 us: 1.02x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 330 ms: 1.03x slower                                                     |
| scimark_fft                      | 124 ms                                                         | 128 ms: 1.04x slower                                                     |
| richards                         | 22.1 ms                                                        | 22.9 ms: 1.04x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 677 ms: 1.04x slower                                                     |
| xml_etree_generate               | 35.8 ms                                                        | 37.4 ms: 1.04x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 50.4 ms: 1.05x slower                                                    |
| 2to3                             | 112 ms                                                         | 118 ms: 1.06x slower                                                     |
| async_tree_eager                 | 43.2 ms                                                        | 45.9 ms: 1.06x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 26.3 ms: 1.07x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 27.1 ms: 1.07x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.04 ms: 1.07x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.40 us: 1.07x slower                                                    |
| genshi_xml                       | 21.4 ms                                                        | 23.0 ms: 1.08x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 32.2 ms: 1.08x slower                                                    |
| thrift                           | 309 us                                                         | 334 us: 1.08x slower                                                     |
| logging_format                   | 2.45 us                                                        | 2.65 us: 1.09x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 108 us: 1.09x slower                                                     |
| hexiom                           | 2.85 ms                                                        | 3.10 ms: 1.09x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 71.2 us: 1.10x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.61 ms: 1.11x slower                                                    |
| pylint                           | 106 ms                                                         | 117 ms: 1.11x slower                                                     |
| pickle_pure_python               | 130 us                                                         | 145 us: 1.11x slower                                                     |
| logging_silent                   | 40.6 ns                                                        | 45.1 ns: 1.11x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 9.66 ms: 1.12x slower                                                    |
| shortest_path                    | 225 ms                                                         | 252 ms: 1.12x slower                                                     |
| genshi_text                      | 9.97 ms                                                        | 11.2 ms: 1.12x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 42.0 ms: 1.13x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 54.3 ms: 1.13x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.7 ms: 1.14x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 109 ms: 1.14x slower                                                     |
| spectral_norm                    | 43.7 ms                                                        | 50.1 ms: 1.14x slower                                                    |
| sympy_sum                        | 52.3 ms                                                        | 60.0 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 241 ms: 1.16x slower                                                     |
| sympy_expand                     | 159 ms                                                         | 185 ms: 1.16x slower                                                     |
| raytrace                         | 109 ms                                                         | 127 ms: 1.17x slower                                                     |
| connected_components             | 208 ms                                                         | 245 ms: 1.18x slower                                                     |
| python_startup_no_site           | 5.95 ms                                                        | 7.02 ms: 1.18x slower                                                    |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.11 ms: 1.18x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 45.3 ms: 1.20x slower                                                    |
| comprehensions                   | 6.80 us                                                        | 8.16 us: 1.20x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 41.2 ms: 1.23x slower                                                    |
| django_template                  | 12.5 ms                                                        | 15.3 ms: 1.23x slower                                                    |
| mako                             | 4.41 ms                                                        | 5.42 ms: 1.23x slower                                                    |
| coverage                         | 31.2 ms                                                        | 38.5 ms: 1.23x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 127 ms: 1.24x slower                                                     |
| many_optionals                   | 200 us                                                         | 258 us: 1.29x slower                                                     |
| scimark_lu                       | 42.8 ms                                                        | 55.4 ms: 1.30x slower                                                    |
| nbody                            | 42.5 ms                                                        | 55.1 ms: 1.30x slower                                                    |
| generators                       | 15.7 ms                                                        | 20.4 ms: 1.30x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 562 us: 1.37x slower                                                     |
| async_tree_eager_tg              | 28.9 ms                                                        | 92.0 ms: 3.18x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                             |

Benchmark hidden because not significant (1): html5lib
Ignored benchmarks (10) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260123-3.15.0a5+-58ccf21-NOGIL/bm-20260123-macm4pro-arm64-python-58ccf21cbb92e0e99cbe-3.15.0a5+-58ccf21.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.028x faster

# HPT report

- Reliability score: 70.22% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.30x