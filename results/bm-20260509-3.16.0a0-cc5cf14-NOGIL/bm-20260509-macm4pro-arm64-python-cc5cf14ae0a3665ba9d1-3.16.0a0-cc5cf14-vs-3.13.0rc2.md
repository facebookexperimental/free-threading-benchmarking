# Results vs. 3.13.0rc2

- fork: python
- ref: cc5cf14ae0a3665ba9d1
- machine: darwin-arm64
- commit hash: cc5cf14
- commit date: 2026-05-09
- overall geometric mean: 1.003x faster
- HPT reliability: 75.37%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.29x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.05 sec                                                       | 1.06 sec: 1.02x slower                                                  |
| html5lib       | 23.1 ms                                                        | 24.5 ms: 1.06x slower                                                   |
| sphinx         | 409 ms                                                         | 445 ms: 1.09x slower                                                    |
| Geometric mean | (ref)                                                          | 1.05x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io_tg           | 521 ms                                                         | 279 ms: 1.86x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 285 ms: 1.84x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 275 ms: 1.47x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 272 ms: 1.42x faster                                                    |
| async_generators                 | 193 ms                                                         | 153 ms: 1.26x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 172 ms: 1.08x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 134 ms: 1.06x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 286 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 178 ms: 1.04x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 120 ms: 1.01x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.02x slower                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 45.5 ms: 1.05x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 270 ms: 1.30x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 158 ms: 1.54x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 108 ms: 3.73x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.02x faster                                                            |

Benchmark hidden because not significant (3): async_tree_none_tg, coroutines, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| float          | 31.4 ms                                                        | 33.3 ms: 1.06x slower                                                   |
| nbody          | 42.5 ms                                                        | 56.8 ms: 1.34x slower                                                   |
| Geometric mean | (ref)                                                          | 1.12x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.18 ms: 1.17x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 52.4 ms: 1.09x slower                                                   |
| Geometric mean | (ref)                                                          | 1.04x faster                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.83 ms: 1.21x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 875 ms: 1.14x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 41.9 ms: 1.10x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 61.6 ms: 1.01x faster                                                   |
| json_loads           | 10.8 us                                                        | 11.1 us: 1.02x slower                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 37.9 ms: 1.06x slower                                                   |
| unpickle_pure_python | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| xml_etree_process    | 25.4 ms                                                        | 28.6 ms: 1.13x slower                                                   |
| pickle_pure_python   | 130 us                                                         | 148 us: 1.14x slower                                                    |
| Geometric mean       | (ref)                                                          | 1.00x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 12.5 ms                                                        | 15.8 ms: 1.26x slower                                                   |
| mako            | 4.41 ms                                                        | 5.69 ms: 1.29x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.28x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.04 ms                                                        | 822 us: 2.48x faster                                                    |
| pylint                           | 106 ms                                                         | 53.8 ms: 1.96x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 523 us: 1.90x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 279 ms: 1.86x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 285 ms: 1.84x faster                                                    |
| mdp                              | 1.06 sec                                                       | 596 ms: 1.78x faster                                                    |
| k_core                           | 1.46 sec                                                       | 991 ms: 1.48x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 275 ms: 1.47x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 4.30 ms: 1.46x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 272 ms: 1.42x faster                                                    |
| deepcopy                         | 145 us                                                         | 108 us: 1.35x faster                                                    |
| async_generators                 | 193 ms                                                         | 153 ms: 1.26x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 13.1 us: 1.25x faster                                                   |
| go                               | 72.6 ms                                                        | 59.3 ms: 1.22x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.83 ms: 1.21x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 794 ns: 1.19x faster                                                    |
| regex_v8                         | 10.7 ms                                                        | 9.18 ms: 1.17x faster                                                   |
| pyflate                          | 222 ms                                                         | 192 ms: 1.16x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 875 ms: 1.14x faster                                                    |
| scimark_sor                      | 64.0 ms                                                        | 56.5 ms: 1.13x faster                                                   |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.92 sec: 1.11x faster                                                  |
| xml_etree_iterparse              | 46.1 ms                                                        | 41.9 ms: 1.10x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.20 us: 1.08x faster                                                   |
| regex_effbot                     | 1.61 ms                                                        | 1.49 ms: 1.08x faster                                                   |
| async_tree_memoization_tg        | 186 ms                                                         | 172 ms: 1.08x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 18.7 ms: 1.06x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 134 ms: 1.06x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 286 ms: 1.05x faster                                                    |
| asyncio_websockets               | 194 ms                                                         | 184 ms: 1.05x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 178 ms: 1.04x faster                                                    |
| fannkuch                         | 179 ms                                                         | 173 ms: 1.03x faster                                                    |
| pathlib                          | 11.1 ms                                                        | 10.8 ms: 1.03x faster                                                   |
| pidigits                         | 166 ms                                                         | 163 ms: 1.02x faster                                                    |
| json                             | 1.94 ms                                                        | 1.91 ms: 1.02x faster                                                   |
| async_tree_eager_memoization     | 122 ms                                                         | 120 ms: 1.01x faster                                                    |
| pycparser                        | 470 ms                                                         | 464 ms: 1.01x faster                                                    |
| xml_etree_parse                  | 62.4 ms                                                        | 61.6 ms: 1.01x faster                                                   |
| dask                             | 525 ms                                                         | 527 ms: 1.00x slower                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 228 ms: 1.02x slower                                                    |
| docutils                         | 1.05 sec                                                       | 1.06 sec: 1.02x slower                                                  |
| json_loads                       | 10.8 us                                                        | 11.1 us: 1.02x slower                                                   |
| scimark_fft                      | 124 ms                                                         | 127 ms: 1.03x slower                                                    |
| pprint_safe_repr                 | 322 ms                                                         | 337 ms: 1.05x slower                                                    |
| logging_simple                   | 2.24 us                                                        | 2.35 us: 1.05x slower                                                   |
| async_tree_eager                 | 43.2 ms                                                        | 45.5 ms: 1.05x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 42.9 ns: 1.06x slower                                                   |
| html5lib                         | 23.1 ms                                                        | 24.5 ms: 1.06x slower                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 37.9 ms: 1.06x slower                                                   |
| float                            | 31.4 ms                                                        | 33.3 ms: 1.06x slower                                                   |
| pprint_pformat                   | 650 ms                                                         | 692 ms: 1.07x slower                                                    |
| richards                         | 22.1 ms                                                        | 23.6 ms: 1.07x slower                                                   |
| logging_format                   | 2.45 us                                                        | 2.62 us: 1.07x slower                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 8.12 ms: 1.08x slower                                                   |
| richards_super                   | 24.7 ms                                                        | 26.7 ms: 1.08x slower                                                   |
| sphinx                           | 409 ms                                                         | 445 ms: 1.09x slower                                                    |
| regex_compile                    | 47.9 ms                                                        | 52.4 ms: 1.09x slower                                                   |
| thrift                           | 309 us                                                         | 340 us: 1.10x slower                                                    |
| nqueens                          | 37.2 ms                                                        | 41.0 ms: 1.10x slower                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 110 us: 1.11x slower                                                    |
| scimark_monte_carlo              | 29.9 ms                                                        | 33.2 ms: 1.11x slower                                                   |
| shortest_path                    | 225 ms                                                         | 251 ms: 1.12x slower                                                    |
| hexiom                           | 2.85 ms                                                        | 3.19 ms: 1.12x slower                                                   |
| xml_etree_process                | 25.4 ms                                                        | 28.6 ms: 1.13x slower                                                   |
| meteor_contest                   | 47.9 ms                                                        | 54.4 ms: 1.14x slower                                                   |
| pickle_pure_python               | 130 us                                                         | 148 us: 1.14x slower                                                    |
| chaos                            | 24.3 ms                                                        | 27.8 ms: 1.14x slower                                                   |
| sympy_str                        | 95.5 ms                                                        | 110 ms: 1.15x slower                                                    |
| typing_runtime_protocols         | 64.6 us                                                        | 74.8 us: 1.16x slower                                                   |
| spectral_norm                    | 43.7 ms                                                        | 50.7 ms: 1.16x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 61.1 ms: 1.17x slower                                                   |
| connected_components             | 208 ms                                                         | 243 ms: 1.17x slower                                                    |
| raytrace                         | 109 ms                                                         | 128 ms: 1.18x slower                                                    |
| sympy_expand                     | 159 ms                                                         | 188 ms: 1.18x slower                                                    |
| deltablue                        | 1.45 ms                                                        | 1.74 ms: 1.20x slower                                                   |
| comprehensions                   | 6.80 us                                                        | 8.17 us: 1.20x slower                                                   |
| bench_mp_pool                    | 37.8 ms                                                        | 46.1 ms: 1.22x slower                                                   |
| coverage                         | 31.2 ms                                                        | 38.6 ms: 1.24x slower                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 2.22 ms: 1.25x slower                                                   |
| django_template                  | 12.5 ms                                                        | 15.8 ms: 1.26x slower                                                   |
| mako                             | 4.41 ms                                                        | 5.69 ms: 1.29x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 270 ms: 1.30x slower                                                    |
| many_optionals                   | 200 us                                                         | 261 us: 1.30x slower                                                    |
| crypto_pyaes                     | 33.6 ms                                                        | 44.2 ms: 1.31x slower                                                   |
| nbody                            | 42.5 ms                                                        | 56.8 ms: 1.34x slower                                                   |
| generators                       | 15.7 ms                                                        | 21.2 ms: 1.35x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 570 us: 1.39x slower                                                    |
| scimark_lu                       | 42.8 ms                                                        | 62.1 ms: 1.45x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 158 ms: 1.54x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 108 ms: 3.73x slower                                                    |
| Geometric mean                   | (ref)                                                          | 1.00x slower                                                            |

Benchmark hidden because not significant (5): async_tree_none_tg, regex_dna, coroutines, async_tree_cpu_io_mixed, telco
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (4) of results/bm-20260509-3.16.0a0-cc5cf14-NOGIL/bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json: sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.003x faster

# HPT report

- Reliability score: 75.37% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.29x