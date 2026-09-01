# Results vs. 3.13.0rc2

- fork: python
- ref: b38e073f1be8fe40af99
- machine: darwin-arm64
- commit hash: b38e073
- commit date: 2026-08-31
- overall geometric mean: 1.062x slower
- HPT reliability: 99.82%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.28x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 112 ms                                                         | 137 ms: 1.23x slower                                                    |
| docutils       | 1.05 sec                                                       | 1.09 sec: 1.05x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                   |
| sphinx         | 409 ms                                                         | 461 ms: 1.13x slower                                                    |
| Geometric mean | (ref)                                                          | 1.11x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 309 ms: 1.68x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 312 ms: 1.68x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 314 ms: 1.29x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 319 ms: 1.21x faster                                                    |
| async_generators                 | 193 ms                                                         | 163 ms: 1.18x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 192 ms: 1.04x slower                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 128 ms: 1.05x slower                                                    |
| async_tree_none                  | 142 ms                                                         | 150 ms: 1.05x slower                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 309 ms: 1.05x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 238 ms: 1.06x slower                                                    |
| async_tree_none_tg               | 133 ms                                                         | 148 ms: 1.11x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 51.9 ms: 1.20x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 13.0 ms: 1.21x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 281 ms: 1.35x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 159 ms: 1.55x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 119 ms: 4.13x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x slower                                                            |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| float          | 31.4 ms                                                        | 35.2 ms: 1.12x slower                                                   |
| nbody          | 42.5 ms                                                        | 63.7 ms: 1.50x slower                                                   |
| Geometric mean | (ref)                                                          | 1.19x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.61 ms                                                        | 1.34 ms: 1.20x faster                                                   |
| regex_v8       | 10.7 ms                                                        | 9.19 ms: 1.16x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 92.8 ms: 1.02x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 68.8 ms: 1.44x slower                                                   |
| Geometric mean | (ref)                                                          | 1.00x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.77 ms: 1.23x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 943 ms: 1.06x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 44.0 ms: 1.05x faster                                                   |
| json_loads           | 10.8 us                                                        | 11.0 us: 1.02x slower                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 66.1 ms: 1.06x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 39.3 ms: 1.10x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 118 us: 1.18x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 31.7 ms: 1.25x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 164 us: 1.26x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073 |
|------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.63 ms                                                        | 10.3 ms: 1.19x slower                                                   |
| python_startup_no_site | 5.95 ms                                                        | 7.55 ms: 1.27x slower                                                   |
| Geometric mean         | (ref)                                                          | 1.23x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 5.85 ms: 1.33x slower                                                   |
| django_template | 12.5 ms                                                        | 17.9 ms: 1.44x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.38x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 780 us: 2.62x faster                                                    |
| create_gc_cycles                 | 993 us                                                         | 492 us: 2.02x faster                                                    |
| pylint                           | 106 ms                                                         | 54.3 ms: 1.94x faster                                                   |
| mdp                              | 1.06 sec                                                       | 621 ms: 1.70x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 309 ms: 1.68x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 312 ms: 1.68x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.01 sec: 1.45x faster                                                  |
| subparsers                       | 6.26 ms                                                        | 4.63 ms: 1.35x faster                                                   |
| async_tree_io_tg                 | 405 ms                                                         | 314 ms: 1.29x faster                                                    |
| json_dumps                       | 4.65 ms                                                        | 3.77 ms: 1.23x faster                                                   |
| deepcopy                         | 145 us                                                         | 119 us: 1.22x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 319 ms: 1.21x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.34 ms: 1.20x faster                                                   |
| async_generators                 | 193 ms                                                         | 163 ms: 1.18x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.19 ms: 1.16x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 817 ns: 1.16x faster                                                    |
| go                               | 72.6 ms                                                        | 66.3 ms: 1.09x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.97 sec: 1.08x faster                                                  |
| deepcopy_memo                    | 16.5 us                                                        | 15.4 us: 1.07x faster                                                   |
| tomli_loads                      | 1000 ms                                                        | 943 ms: 1.06x faster                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 61.2 us: 1.06x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 60.8 ms: 1.05x faster                                                   |
| xml_etree_iterparse              | 46.1 ms                                                        | 44.0 ms: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 186 ms: 1.04x faster                                                    |
| pyflate                          | 222 ms                                                         | 214 ms: 1.04x faster                                                    |
| deepcopy_reduce                  | 1.30 us                                                        | 1.25 us: 1.03x faster                                                   |
| regex_dna                        | 94.6 ms                                                        | 92.8 ms: 1.02x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 11.0 ms: 1.01x faster                                                   |
| dulwich_log                      | 19.8 ms                                                        | 19.9 ms: 1.00x slower                                                   |
| telco                            | 3.07 ms                                                        | 3.10 ms: 1.01x slower                                                   |
| pidigits                         | 166 ms                                                         | 168 ms: 1.01x slower                                                    |
| json_loads                       | 10.8 us                                                        | 11.0 us: 1.02x slower                                                   |
| async_tree_memoization           | 184 ms                                                         | 192 ms: 1.04x slower                                                    |
| html5lib                         | 23.1 ms                                                        | 24.1 ms: 1.04x slower                                                   |
| docutils                         | 1.05 sec                                                       | 1.09 sec: 1.05x slower                                                  |
| async_tree_eager_memoization     | 122 ms                                                         | 128 ms: 1.05x slower                                                    |
| async_tree_none                  | 142 ms                                                         | 150 ms: 1.05x slower                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 309 ms: 1.05x slower                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 66.1 ms: 1.06x slower                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 238 ms: 1.06x slower                                                    |
| fannkuch                         | 179 ms                                                         | 189 ms: 1.06x slower                                                    |
| pycparser                        | 470 ms                                                         | 508 ms: 1.08x slower                                                    |
| scimark_fft                      | 124 ms                                                         | 135 ms: 1.09x slower                                                    |
| xml_etree_generate               | 35.8 ms                                                        | 39.3 ms: 1.10x slower                                                   |
| async_tree_none_tg               | 133 ms                                                         | 148 ms: 1.11x slower                                                    |
| float                            | 31.4 ms                                                        | 35.2 ms: 1.12x slower                                                   |
| sphinx                           | 409 ms                                                         | 461 ms: 1.13x slower                                                    |
| sympy_integrate                  | 7.53 ms                                                        | 8.50 ms: 1.13x slower                                                   |
| shortest_path                    | 225 ms                                                         | 254 ms: 1.13x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 368 ms: 1.14x slower                                                    |
| meteor_contest                   | 47.9 ms                                                        | 54.8 ms: 1.14x slower                                                   |
| thrift                           | 309 us                                                         | 354 us: 1.15x slower                                                    |
| pprint_pformat                   | 650 ms                                                         | 757 ms: 1.17x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 44.3 ms: 1.17x slower                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 35.1 ms: 1.18x slower                                                   |
| connected_components             | 208 ms                                                         | 246 ms: 1.18x slower                                                    |
| unpickle_pure_python             | 99.5 us                                                        | 118 us: 1.18x slower                                                    |
| python_startup                   | 8.63 ms                                                        | 10.3 ms: 1.19x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 62.1 ms: 1.19x slower                                                   |
| logging_simple                   | 2.24 us                                                        | 2.66 us: 1.19x slower                                                   |
| nqueens                          | 37.2 ms                                                        | 44.5 ms: 1.19x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.93 us: 1.20x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 115 ms: 1.20x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 51.9 ms: 1.20x slower                                                   |
| coroutines                       | 10.8 ms                                                        | 13.0 ms: 1.21x slower                                                   |
| sympy_expand                     | 159 ms                                                         | 194 ms: 1.22x slower                                                    |
| richards                         | 22.1 ms                                                        | 26.9 ms: 1.22x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 53.3 ms: 1.22x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 49.8 ns: 1.23x slower                                                   |
| 2to3                             | 112 ms                                                         | 137 ms: 1.23x slower                                                    |
| richards_super                   | 24.7 ms                                                        | 30.5 ms: 1.24x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.20 ms: 1.24x slower                                                   |
| hexiom                           | 2.85 ms                                                        | 3.55 ms: 1.25x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 31.7 ms: 1.25x slower                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 42.2 ms: 1.26x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 164 us: 1.26x slower                                                    |
| python_startup_no_site           | 5.95 ms                                                        | 7.55 ms: 1.27x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.82 us: 1.30x slower                                                   |
| coverage                         | 31.2 ms                                                        | 40.5 ms: 1.30x slower                                                   |
| chaos                            | 24.3 ms                                                        | 31.7 ms: 1.30x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.85 ms: 1.33x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 281 ms: 1.35x slower                                                    |
| many_optionals                   | 200 us                                                         | 273 us: 1.36x slower                                                    |
| bench_thread_pool                | 412 us                                                         | 581 us: 1.41x slower                                                    |
| raytrace                         | 109 ms                                                         | 156 ms: 1.43x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 68.8 ms: 1.44x slower                                                   |
| django_template                  | 12.5 ms                                                        | 17.9 ms: 1.44x slower                                                   |
| deltablue                        | 1.45 ms                                                        | 2.12 ms: 1.46x slower                                                   |
| nbody                            | 42.5 ms                                                        | 63.7 ms: 1.50x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 159 ms: 1.55x slower                                                    |
| generators                       | 15.7 ms                                                        | 24.8 ms: 1.58x slower                                                   |
| scimark_lu                       | 42.8 ms                                                        | 69.1 ms: 1.62x slower                                                   |
| async_tree_eager_tg              | 28.9 ms                                                        | 119 ms: 4.13x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.07x slower                                                            |

Benchmark hidden because not significant (3): json, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg
Ignored benchmarks (13) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: chameleon, dask, djangocms, genshi_text, genshi_xml, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260831-3.16.0a0-b38e073-NOGIL/bm-20260831-macm4pro-arm64-python-b38e073f1be8fe40af99-3.16.0a0-b38e073.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.062x slower

# HPT report

- Reliability score: 99.82% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.28x