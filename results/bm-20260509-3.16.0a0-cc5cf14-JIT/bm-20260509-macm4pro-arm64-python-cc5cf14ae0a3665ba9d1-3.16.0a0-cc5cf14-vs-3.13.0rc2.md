# Results vs. 3.13.0rc2

- fork: python
- ref: cc5cf14ae0a3665ba9d1
- machine: darwin-arm64
- commit hash: cc5cf14
- commit date: 2026-05-09
- overall geometric mean: 1.161x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.05 sec                                                       | 933 ms: 1.12x faster                                                    |
| html5lib       | 23.1 ms                                                        | 22.2 ms: 1.04x faster                                                   |
| sphinx         | 409 ms                                                         | 399 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                          | 1.06x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 525 ms                                                         | 286 ms: 1.84x faster                                                    |
| async_tree_eager_io_tg           | 521 ms                                                         | 317 ms: 1.64x faster                                                    |
| async_tree_io                    | 386 ms                                                         | 286 ms: 1.35x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 301 ms: 1.35x faster                                                    |
| async_tree_none                  | 142 ms                                                         | 108 ms: 1.32x faster                                                    |
| async_generators                 | 193 ms                                                         | 151 ms: 1.28x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 35.9 ms: 1.20x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 114 ms: 1.16x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 162 ms: 1.14x faster                                                    |
| async_tree_memoization           | 184 ms                                                         | 165 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 279 ms: 1.08x faster                                                    |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 254 ms: 1.22x slower                                                    |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 147 ms: 1.44x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 95.7 ms: 3.31x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.08x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 31.4 ms                                                        | 23.7 ms: 1.33x faster                                                   |
| nbody          | 42.5 ms                                                        | 33.8 ms: 1.26x faster                                                   |
| pidigits       | 166 ms                                                         | 160 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                          | 1.20x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 10.7 ms                                                        | 9.47 ms: 1.13x faster                                                   |
| regex_effbot   | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                   |
| regex_compile  | 47.9 ms                                                        | 46.6 ms: 1.03x faster                                                   |
| regex_dna      | 94.6 ms                                                        | 93.7 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                          | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 4.65 ms                                                        | 3.44 ms: 1.35x faster                                                   |
| tomli_loads          | 1000 ms                                                        | 748 ms: 1.34x faster                                                    |
| unpickle_pure_python | 99.5 us                                                        | 84.2 us: 1.18x faster                                                   |
| pickle_pure_python   | 130 us                                                         | 114 us: 1.15x faster                                                    |
| xml_etree_iterparse  | 46.1 ms                                                        | 40.4 ms: 1.14x faster                                                   |
| xml_etree_process    | 25.4 ms                                                        | 22.7 ms: 1.12x faster                                                   |
| xml_etree_generate   | 35.8 ms                                                        | 33.4 ms: 1.07x faster                                                   |
| json_loads           | 10.8 us                                                        | 10.2 us: 1.06x faster                                                   |
| xml_etree_parse      | 62.4 ms                                                        | 66.6 ms: 1.07x slower                                                   |
| Geometric mean       | (ref)                                                          | 1.14x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|-----------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.41 ms                                                        | 3.89 ms: 1.13x faster                                                   |
| django_template | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                   |
| Geometric mean  | (ref)                                                          | 1.01x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------------|:--------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| richards                         | 22.1 ms                                                        | 9.99 ms: 2.21x faster                                                   |
| richards_super                   | 24.7 ms                                                        | 11.5 ms: 2.15x faster                                                   |
| scimark_sor                      | 64.0 ms                                                        | 32.9 ms: 1.94x faster                                                   |
| pylint                           | 106 ms                                                         | 55.9 ms: 1.89x faster                                                   |
| mdp                              | 1.06 sec                                                       | 566 ms: 1.87x faster                                                    |
| async_tree_eager_io              | 525 ms                                                         | 286 ms: 1.84x faster                                                    |
| subparsers                       | 6.26 ms                                                        | 3.67 ms: 1.71x faster                                                   |
| async_tree_eager_io_tg           | 521 ms                                                         | 317 ms: 1.64x faster                                                    |
| deepcopy_memo                    | 16.5 us                                                        | 10.7 us: 1.53x faster                                                   |
| go                               | 72.6 ms                                                        | 47.9 ms: 1.51x faster                                                   |
| pyflate                          | 222 ms                                                         | 148 ms: 1.50x faster                                                    |
| deepcopy                         | 145 us                                                         | 98.6 us: 1.47x faster                                                   |
| scimark_lu                       | 42.8 ms                                                        | 29.4 ms: 1.45x faster                                                   |
| json_dumps                       | 4.65 ms                                                        | 3.44 ms: 1.35x faster                                                   |
| async_tree_io                    | 386 ms                                                         | 286 ms: 1.35x faster                                                    |
| async_tree_io_tg                 | 405 ms                                                         | 301 ms: 1.35x faster                                                    |
| tomli_loads                      | 1000 ms                                                        | 748 ms: 1.34x faster                                                    |
| float                            | 31.4 ms                                                        | 23.7 ms: 1.33x faster                                                   |
| spectral_norm                    | 43.7 ms                                                        | 33.0 ms: 1.32x faster                                                   |
| async_tree_none                  | 142 ms                                                         | 108 ms: 1.32x faster                                                    |
| scimark_fft                      | 124 ms                                                         | 96.2 ms: 1.29x faster                                                   |
| scimark_monte_carlo              | 29.9 ms                                                        | 23.3 ms: 1.28x faster                                                   |
| async_generators                 | 193 ms                                                         | 151 ms: 1.28x faster                                                    |
| k_core                           | 1.46 sec                                                       | 1.15 sec: 1.27x faster                                                  |
| nbody                            | 42.5 ms                                                        | 33.8 ms: 1.26x faster                                                   |
| deltablue                        | 1.45 ms                                                        | 1.16 ms: 1.25x faster                                                   |
| logging_format                   | 2.45 us                                                        | 1.96 us: 1.25x faster                                                   |
| logging_simple                   | 2.24 us                                                        | 1.80 us: 1.24x faster                                                   |
| deepcopy_reduce                  | 1.30 us                                                        | 1.05 us: 1.23x faster                                                   |
| nqueens                          | 37.2 ms                                                        | 30.3 ms: 1.23x faster                                                   |
| pprint_safe_repr                 | 322 ms                                                         | 265 ms: 1.21x faster                                                    |
| fannkuch                         | 179 ms                                                         | 148 ms: 1.21x faster                                                    |
| async_tree_eager                 | 43.2 ms                                                        | 35.9 ms: 1.20x faster                                                   |
| pprint_pformat                   | 650 ms                                                         | 542 ms: 1.20x faster                                                    |
| chaos                            | 24.3 ms                                                        | 20.4 ms: 1.19x faster                                                   |
| unpickle_pure_python             | 99.5 us                                                        | 84.2 us: 1.18x faster                                                   |
| telco                            | 3.07 ms                                                        | 2.60 ms: 1.18x faster                                                   |
| hexiom                           | 2.85 ms                                                        | 2.44 ms: 1.17x faster                                                   |
| async_tree_none_tg               | 133 ms                                                         | 114 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.13 sec                                                       | 1.84 sec: 1.15x faster                                                  |
| pickle_pure_python               | 130 us                                                         | 114 us: 1.15x faster                                                    |
| async_tree_memoization_tg        | 186 ms                                                         | 162 ms: 1.14x faster                                                    |
| xml_etree_iterparse              | 46.1 ms                                                        | 40.4 ms: 1.14x faster                                                   |
| create_gc_cycles                 | 993 us                                                         | 871 us: 1.14x faster                                                    |
| dulwich_log                      | 19.8 ms                                                        | 17.5 ms: 1.14x faster                                                   |
| mako                             | 4.41 ms                                                        | 3.89 ms: 1.13x faster                                                   |
| regex_v8                         | 10.7 ms                                                        | 9.47 ms: 1.13x faster                                                   |
| comprehensions                   | 6.80 us                                                        | 6.05 us: 1.12x faster                                                   |
| docutils                         | 1.05 sec                                                       | 933 ms: 1.12x faster                                                    |
| xml_etree_process                | 25.4 ms                                                        | 22.7 ms: 1.12x faster                                                   |
| async_tree_memoization           | 184 ms                                                         | 165 ms: 1.12x faster                                                    |
| async_tree_eager_memoization     | 122 ms                                                         | 110 ms: 1.11x faster                                                    |
| regex_effbot                     | 1.61 ms                                                        | 1.46 ms: 1.11x faster                                                   |
| async_tree_cpu_io_mixed          | 294 ms                                                         | 267 ms: 1.10x faster                                                    |
| raytrace                         | 109 ms                                                         | 100.0 ms: 1.09x faster                                                  |
| async_tree_cpu_io_mixed_tg       | 301 ms                                                         | 279 ms: 1.08x faster                                                    |
| meteor_contest                   | 47.9 ms                                                        | 44.5 ms: 1.08x faster                                                   |
| json                             | 1.94 ms                                                        | 1.81 ms: 1.08x faster                                                   |
| xml_etree_generate               | 35.8 ms                                                        | 33.4 ms: 1.07x faster                                                   |
| json_loads                       | 10.8 us                                                        | 10.2 us: 1.06x faster                                                   |
| coroutines                       | 10.8 ms                                                        | 10.2 ms: 1.06x faster                                                   |
| pathlib                          | 11.1 ms                                                        | 10.6 ms: 1.05x faster                                                   |
| typing_runtime_protocols         | 64.6 us                                                        | 61.4 us: 1.05x faster                                                   |
| gc_traversal                     | 2.04 ms                                                        | 1.94 ms: 1.05x faster                                                   |
| crypto_pyaes                     | 33.6 ms                                                        | 32.0 ms: 1.05x faster                                                   |
| asyncio_websockets               | 194 ms                                                         | 185 ms: 1.05x faster                                                    |
| html5lib                         | 23.1 ms                                                        | 22.2 ms: 1.04x faster                                                   |
| scimark_sparse_mat_mult          | 1.78 ms                                                        | 1.71 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 225 ms                                                         | 217 ms: 1.04x faster                                                    |
| pidigits                         | 166 ms                                                         | 160 ms: 1.04x faster                                                    |
| connected_components             | 208 ms                                                         | 202 ms: 1.03x faster                                                    |
| regex_compile                    | 47.9 ms                                                        | 46.6 ms: 1.03x faster                                                   |
| sqlite_synth                     | 948 ns                                                         | 922 ns: 1.03x faster                                                    |
| sphinx                           | 409 ms                                                         | 399 ms: 1.02x faster                                                    |
| shortest_path                    | 225 ms                                                         | 221 ms: 1.01x faster                                                    |
| thrift                           | 309 us                                                         | 306 us: 1.01x faster                                                    |
| regex_dna                        | 94.6 ms                                                        | 93.7 ms: 1.01x faster                                                   |
| sympy_integrate                  | 7.53 ms                                                        | 7.46 ms: 1.01x faster                                                   |
| sympy_expand                     | 159 ms                                                         | 158 ms: 1.01x faster                                                    |
| pycparser                        | 470 ms                                                         | 474 ms: 1.01x slower                                                    |
| sympy_str                        | 95.5 ms                                                        | 96.5 ms: 1.01x slower                                                   |
| sympy_sum                        | 52.3 ms                                                        | 52.9 ms: 1.01x slower                                                   |
| logging_silent                   | 40.6 ns                                                        | 41.4 ns: 1.02x slower                                                   |
| bench_thread_pool                | 412 us                                                         | 429 us: 1.04x slower                                                    |
| coverage                         | 31.2 ms                                                        | 33.1 ms: 1.06x slower                                                   |
| xml_etree_parse                  | 62.4 ms                                                        | 66.6 ms: 1.07x slower                                                   |
| generators                       | 15.7 ms                                                        | 17.3 ms: 1.10x slower                                                   |
| many_optionals                   | 200 us                                                         | 222 us: 1.11x slower                                                    |
| django_template                  | 12.5 ms                                                        | 14.6 ms: 1.17x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 208 ms                                                         | 254 ms: 1.22x slower                                                    |
| bench_mp_pool                    | 37.8 ms                                                        | 46.7 ms: 1.23x slower                                                   |
| async_tree_eager_memoization_tg  | 103 ms                                                         | 147 ms: 1.44x slower                                                    |
| async_tree_eager_tg              | 28.9 ms                                                        | 95.7 ms: 3.31x slower                                                   |
| Geometric mean                   | (ref)                                                          | 1.15x faster                                                            |

Benchmark hidden because not significant (1): dask
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-macm4pro-arm64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260509-3.16.0a0-cc5cf14-JIT/bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json: pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.161x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.21x