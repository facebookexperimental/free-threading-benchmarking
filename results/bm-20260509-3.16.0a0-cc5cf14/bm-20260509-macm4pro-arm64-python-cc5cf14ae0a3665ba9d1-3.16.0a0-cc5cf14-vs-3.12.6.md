# Results vs. 3.12.6

- fork: python
- ref: cc5cf14ae0a3665ba9d1
- machine: darwin-arm64
- commit hash: cc5cf14
- commit date: 2026-05-09
- overall geometric mean: 1.111x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 983 ms: 1.04x faster                                                    |
| sphinx         | 434 ms                                                   | 413 ms: 1.05x faster                                                    |
| Geometric mean | (ref)                                                    | 1.03x faster                                                            |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 310 ms: 1.60x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 122 ms: 1.46x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 315 ms: 1.46x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 333 ms: 1.44x faster                                                    |
| async_generators                 | 206 ms                                                   | 149 ms: 1.39x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 127 ms: 1.35x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 334 ms: 1.34x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 173 ms: 1.33x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 177 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 281 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 291 ms: 1.16x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.14x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.1 ms: 1.11x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 261 ms: 1.23x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 152 ms: 1.35x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 103 ms: 3.21x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.12x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 30.5 ms: 1.24x faster                                                   |
| nbody          | 54.2 ms                                                  | 45.5 ms: 1.19x faster                                                   |
| Geometric mean | (ref)                                                    | 1.14x faster                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.43 ms: 1.16x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 47.4 ms: 1.15x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 94.7 ms: 1.05x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.76 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 42.1 ms: 1.23x faster                                                   |
| tomli_loads          | 957 ms                                                   | 842 ms: 1.14x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.78 ms: 1.13x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.6 us: 1.02x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.2 ms: 1.02x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 66.6 ms: 1.02x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 104 us: 1.01x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 144 us: 1.04x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.88 ms: 1.02x slower                                                   |
| django_template | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.08x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.22 ms: 4.92x faster                                                   |
| pylint                           | 128 ms                                                   | 57.2 ms: 2.24x faster                                                   |
| mdp                              | 1.09 sec                                                 | 522 ms: 2.09x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 310 ms: 1.60x faster                                                    |
| deepcopy                         | 161 us                                                   | 103 us: 1.57x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 122 ms: 1.46x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.5 us: 1.46x faster                                                   |
| async_tree_io                    | 459 ms                                                   | 315 ms: 1.46x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 333 ms: 1.44x faster                                                    |
| async_generators                 | 206 ms                                                   | 149 ms: 1.39x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.27 us: 1.35x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 127 ms: 1.35x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 334 ms: 1.34x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 173 ms: 1.33x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.11 us: 1.31x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.6 ms: 1.28x faster                                                   |
| go                               | 70.0 ms                                                  | 54.8 ms: 1.28x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 177 ms: 1.25x faster                                                    |
| float                            | 37.9 ms                                                  | 30.5 ms: 1.24x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 42.1 ms: 1.23x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 44.4 ms: 1.22x faster                                                   |
| raytrace                         | 145 ms                                                   | 119 ms: 1.22x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 42.5 ns: 1.20x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 51.0 ms: 1.20x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 119 ms: 1.19x faster                                                    |
| nbody                            | 54.2 ms                                                  | 45.5 ms: 1.19x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 281 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 291 ms: 1.16x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.43 ms: 1.16x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 47.4 ms: 1.15x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 115 ms: 1.14x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 842 ms: 1.14x faster                                                    |
| pyflate                          | 216 ms                                                   | 190 ms: 1.14x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.6 ms: 1.13x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.78 ms: 1.13x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.53 ms: 1.13x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.12x faster                                                  |
| logging_simple                   | 2.57 us                                                  | 2.30 us: 1.12x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.51 us: 1.12x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 19.1 ms: 1.11x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 41.1 ms: 1.11x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.3 ms: 1.10x faster                                                   |
| k_core                           | 1.12 sec                                                 | 1.02 sec: 1.10x faster                                                  |
| generators                       | 21.9 ms                                                  | 20.1 ms: 1.09x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 65.7 us: 1.08x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.83 ms: 1.07x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.56 ms: 1.06x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.96 ms: 1.06x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 94.7 ms: 1.05x faster                                                   |
| sphinx                           | 434 ms                                                   | 413 ms: 1.05x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.1 ms: 1.05x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.5 ms: 1.04x faster                                                   |
| docutils                         | 1.02 sec                                                 | 983 ms: 1.04x faster                                                    |
| fannkuch                         | 176 ms                                                   | 169 ms: 1.04x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 24.6 ms: 1.03x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 646 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 225 ms: 1.03x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 1.96 ms: 1.03x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 943 ns: 1.03x faster                                                    |
| json                             | 1.93 ms                                                  | 1.89 ms: 1.03x faster                                                   |
| sympy_str                        | 104 ms                                                   | 102 ms: 1.02x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 321 ms: 1.02x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.6 us: 1.02x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 26.2 ms: 1.02x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 56.5 ms: 1.02x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 66.6 ms: 1.02x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                    |
| pycparser                        | 497 ms                                                   | 491 ms: 1.01x faster                                                    |
| thrift                           | 322 us                                                   | 318 us: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 51.7 ms: 1.01x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 104 us: 1.01x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.76 ms: 1.02x slower                                                   |
| mako                             | 4.77 ms                                                  | 4.88 ms: 1.02x slower                                                   |
| shortest_path                    | 219 ms                                                   | 225 ms: 1.03x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 173 ms: 1.03x slower                                                    |
| connected_components             | 201 ms                                                   | 208 ms: 1.04x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 144 us: 1.04x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 434 us: 1.04x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 40.5 ms: 1.04x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 50.0 ms: 1.05x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 870 us: 1.05x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.85 ms: 1.09x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 47.5 ms: 1.20x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 261 ms: 1.23x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.2 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 248 us: 1.27x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 152 ms: 1.35x slower                                                    |
| nqueens                          | 43.5 ms                                                  | 58.8 ms: 1.35x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 103 ms: 3.21x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                            |

Benchmark hidden because not significant (2): html5lib, pidigits
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260509-3.16.0a0-cc5cf14/bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.111x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.21x