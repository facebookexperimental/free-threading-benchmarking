# Results vs. 3.13.0rc2

- fork: python
- ref: ee521e8ac19ad012ebc4
- machine: darwin-arm64
- commit hash: ee521e8
- commit date: 2026-08-24
- overall geometric mean: 1.059x slower
- HPT reliability: 99.57%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.28x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 136 ms: 1.22x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.09 sec: 1.04x slower                                                  |
| html5lib       | 23.1 ms                                                        | 23.9 ms: 1.03x slower                                                   |
| sphinx         | 409 ms                                                         | 459 ms: 1.12x slower                                                    |
| Geometric mean | (ref)                                                          | 1.10x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 310 ms: 1.68x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 314 ms: 1.67x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 313 ms: 1.29x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 320 ms: 1.21x faster                                                    |
| async_generators                 | 193 ms                                                         | 166 ms: 1.16x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 192 ms: 1.04x slower                                                    |
| async_tree_none                  | 142 ms                                                         | 149 ms: 1.05x slower                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 308 ms: 1.05x slower                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 128 ms: 1.05x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 239 ms: 1.06x slower                                                    |
| async_tree_none_tg               | 133 ms                                                         | 146 ms: 1.10x slower                                                    |
| coroutines                       | 10.8 ms                                                        | 12.9 ms: 1.20x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 52.7 ms: 1.22x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 280 ms: 1.35x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 159 ms: 1.55x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 119 ms: 4.12x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x slower                                                            |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| float          | 31.4 ms                                                        | 35.1 ms: 1.12x slower                                                   |
| nbody          | 42.5 ms                                                        | 63.4 ms: 1.49x slower                                                   |
| Geometric mean | (ref)                                                          | 1.18x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.05 ms: 1.18x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.39 ms: 1.16x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 91.5 ms: 1.03x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 68.8 ms: 1.44x slower                                                   |
| Geometric mean | (ref)                                                          | 1.00x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.76 ms: 1.24x faster                                                   |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.6 ms: 1.11x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 57.6 ms: 1.08x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 961 ms: 1.04x faster                                                    |
| json_loads           | 10.8 us                                                        | 11.0 us: 1.01x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 39.4 ms: 1.10x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 120 us: 1.20x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 31.5 ms: 1.24x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 164 us: 1.26x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.03x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.1 ms: 1.17x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.46 ms: 1.25x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 6.00 ms: 1.36x slower                                                   |
| django_template | 12.5 ms                                                        | 17.8 ms: 1.43x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.39x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 771 us: 2.65x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 483 us: 2.05x faster                                                    |
| pylint                           | 106 ms                                                         | 54.2 ms: 1.95x faster                                                   |
| mdp                              | 1.06 sec                                                       | 625 ms: 1.69x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 310 ms: 1.68x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 314 ms: 1.67x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.00 sec: 1.46x faster                                                  |
| subparsers                       | 6.26 ms                                                        | 4.61 ms: 1.36x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 313 ms: 1.29x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.76 ms: 1.24x faster                                                   |
| deepcopy                         | 145 us                                                         | 120 us: 1.21x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 320 ms: 1.21x faster                                                    |
| sqlite_synth                     | 948 ns                                                         | 798 ns: 1.19x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.05 ms: 1.18x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.39 ms: 1.16x faster                                                   |
| async_generators                 | 193 ms                                                         | 166 ms: 1.16x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.6 ms: 1.11x faster                                                   |
| go                               | 72.6 ms                                                        | 66.3 ms: 1.09x faster                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 57.6 ms: 1.08x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.98 sec: 1.08x faster                                                  |
| typing_runtime_protocols         | 64.6 us                                                        | 60.3 us: 1.07x faster                                                   |
| deepcopy_memo                    | 16.5 us                                                        | 15.5 us: 1.06x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| pyflate                          | 222 ms                                                         | 213 ms: 1.04x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 961 ms: 1.04x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 61.8 ms: 1.04x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 91.5 ms: 1.03x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.9 ms: 1.02x faster                                                   |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.27 us: 1.02x faster                                                   |
| telco                            | 3.07 ms                                                        | 3.10 ms: 1.01x slower                                                   |
| json_loads                       | 10.8 us                                                        | 11.0 us: 1.01x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 23.9 ms: 1.03x slower                                                   |
| async_tree_memoization           | 184 ms                                                         | 192 ms: 1.04x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.09 sec: 1.04x slower                                                  |
| async_tree_none                  | 142 ms                                                         | 149 ms: 1.05x slower                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 308 ms: 1.05x slower                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 128 ms: 1.05x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 239 ms: 1.06x slower                                                    |
| pycparser                        | 470 ms                                                         | 506 ms: 1.08x slower                                                    |
| fannkuch                         | 179 ms                                                         | 193 ms: 1.08x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 135 ms: 1.09x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 39.4 ms: 1.10x slower                                                   |
| async_tree_none_tg               | 133 ms                                                         | 146 ms: 1.10x slower                                                    |
| float                            | 31.4 ms                                                        | 35.1 ms: 1.12x slower                                                   |
| sphinx                           | 409 ms                                                         | 459 ms: 1.12x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.47 ms: 1.12x slower                                                   |
| shortest_path                    | 225 ms                                                         | 253 ms: 1.13x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 54.0 ms: 1.13x slower                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 370 ms: 1.15x slower                                                    |
| thrift                           | 309 us                                                         | 356 us: 1.15x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 43.8 ms: 1.16x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 759 ms: 1.17x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 10.1 ms: 1.17x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.62 us: 1.17x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 43.7 ms: 1.17x slower                                                   |
| connected_components             | 208 ms                                                         | 246 ms: 1.18x slower                                                    |
| logging_format                   | 2.45 us                                                        | 2.89 us: 1.18x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 51.9 ms: 1.19x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 62.2 ms: 1.19x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 35.8 ms: 1.20x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 12.9 ms: 1.20x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 115 ms: 1.20x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 120 us: 1.20x slower                                                    |
| richards                         | 22.1 ms                                                        | 26.6 ms: 1.21x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 52.7 ms: 1.22x slower                                                   |
| 2to3                             | 112 ms                                                         | 136 ms: 1.22x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 30.2 ms: 1.22x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 196 ms: 1.23x slower                                                    |
| xml_etree_process                | 25.4 ms                                                        | 31.5 ms: 1.24x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.22 ms: 1.25x slower                                                   |
| python_startup_no_site           | 5.95 ms                                                        | 7.46 ms: 1.25x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 51.0 ns: 1.26x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 164 us: 1.26x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.59 ms: 1.26x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.5 ms: 1.26x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.80 us: 1.29x slower                                                   |
| chaos                            | 24.3 ms                                                        | 31.9 ms: 1.31x slower                                                   |
| coverage                         | 31.2 ms                                                        | 41.8 ms: 1.34x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 280 ms: 1.35x slower                                                    |
| many_optionals                   | 200 us                                                         | 272 us: 1.36x slower                                                    |
| mako                             | 4.41 ms                                                        | 6.00 ms: 1.36x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 570 us: 1.38x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 2.06 ms: 1.42x slower                                                   |
| django_template                  | 12.5 ms                                                        | 17.8 ms: 1.43x slower                                                   |
| raytrace                         | 109 ms                                                         | 156 ms: 1.43x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 68.8 ms: 1.44x slower                                                   |
| nbody                            | 42.5 ms                                                        | 63.4 ms: 1.49x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 159 ms: 1.55x slower                                                    |
| generators                       | 15.7 ms                                                        | 24.5 ms: 1.56x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 70.1 ms: 1.64x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 119 ms: 4.12x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x slower                                                            |

Benchmark hidden because not significant (4): dulwich_log, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, json
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260824-3.16.0a0-ee521e8-NOGIL/bm-20260824-macm4pro-arm64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.059x slower

# HPT report

- Reliability score: 99.57% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.28x