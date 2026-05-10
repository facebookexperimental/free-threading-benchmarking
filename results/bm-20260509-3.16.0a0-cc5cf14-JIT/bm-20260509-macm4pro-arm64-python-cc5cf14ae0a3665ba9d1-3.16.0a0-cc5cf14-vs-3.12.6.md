# Results vs. 3.12.6

- fork: python
- ref: cc5cf14ae0a3665ba9d1
- machine: darwin-arm64
- commit hash: cc5cf14
- commit date: 2026-05-09
- overall geometric mean: 1.257x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.15x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| docutils       | 1.02 sec                                                 | 933 ms: 1.09x faster                                                    |
| html5lib       | 23.0 ms                                                  | 22.2 ms: 1.04x faster                                                   |
| sphinx         | 434 ms                                                   | 399 ms: 1.09x faster                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 286 ms: 1.73x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 108 ms: 1.65x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 286 ms: 1.61x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 301 ms: 1.59x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 114 ms: 1.51x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 162 ms: 1.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 317 ms: 1.41x faster                                                    |
| async_generators                 | 206 ms                                                   | 151 ms: 1.37x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 165 ms: 1.35x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 35.9 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 279 ms: 1.21x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 217 ms: 1.06x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 254 ms: 1.19x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 147 ms: 1.31x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 95.7 ms: 2.98x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.20x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 54.2 ms                                                  | 33.8 ms: 1.61x faster                                                   |
| float          | 37.9 ms                                                  | 23.7 ms: 1.60x faster                                                   |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                    |
| Geometric mean | (ref)                                                    | 1.37x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 46.6 ms: 1.17x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 93.7 ms: 1.06x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.47 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                    | 1.10x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 748 ms: 1.28x faster                                                    |
| xml_etree_iterparse  | 51.6 ms                                                  | 40.4 ms: 1.28x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.44 ms: 1.24x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 114 us: 1.23x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 84.2 us: 1.22x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 22.7 ms: 1.18x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 33.4 ms: 1.16x faster                                                   |
| json_loads           | 10.9 us                                                  | 10.2 us: 1.06x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 66.6 ms: 1.02x faster                                                   |
| Geometric mean       | (ref)                                                    | 1.18x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 3.89 ms: 1.23x faster                                                   |
| django_template | 13.6 ms                                                  | 14.6 ms: 1.07x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.07x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.67 ms: 5.66x faster                                                   |
| pylint                           | 128 ms                                                   | 55.9 ms: 2.29x faster                                                   |
| richards                         | 22.4 ms                                                  | 9.99 ms: 2.24x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 11.5 ms: 2.21x faster                                                   |
| mdp                              | 1.09 sec                                                 | 566 ms: 1.93x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 32.9 ms: 1.85x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 29.4 ms: 1.74x faster                                                   |
| async_tree_eager_io              | 496 ms                                                   | 286 ms: 1.73x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 10.7 us: 1.70x faster                                                   |
| async_tree_none                  | 178 ms                                                   | 108 ms: 1.65x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 33.0 ms: 1.65x faster                                                   |
| deepcopy                         | 161 us                                                   | 98.6 us: 1.64x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 6.05 us: 1.63x faster                                                   |
| async_tree_io                    | 459 ms                                                   | 286 ms: 1.61x faster                                                    |
| nbody                            | 54.2 ms                                                  | 33.8 ms: 1.61x faster                                                   |
| float                            | 37.9 ms                                                  | 23.7 ms: 1.60x faster                                                   |
| async_tree_io_tg                 | 480 ms                                                   | 301 ms: 1.59x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 114 ms: 1.51x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.16 ms: 1.48x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 96.2 ms: 1.47x faster                                                   |
| go                               | 70.0 ms                                                  | 47.9 ms: 1.46x faster                                                   |
| pyflate                          | 216 ms                                                   | 148 ms: 1.46x faster                                                    |
| raytrace                         | 145 ms                                                   | 100.0 ms: 1.45x faster                                                  |
| nqueens                          | 43.5 ms                                                  | 30.3 ms: 1.43x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 1.80 us: 1.43x faster                                                   |
| logging_format                   | 2.80 us                                                  | 1.96 us: 1.43x faster                                                   |
| chaos                            | 28.9 ms                                                  | 20.4 ms: 1.42x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 162 ms: 1.42x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 317 ms: 1.41x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.05 us: 1.39x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 23.3 ms: 1.38x faster                                                   |
| async_generators                 | 206 ms                                                   | 151 ms: 1.37x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 165 ms: 1.35x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.33x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 748 ms: 1.28x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 40.4 ms: 1.28x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 35.9 ms: 1.27x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.3 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.44 ms: 1.25x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.44 ms: 1.24x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 265 ms: 1.24x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 41.4 ns: 1.23x faster                                                   |
| mako                             | 4.77 ms                                                  | 3.89 ms: 1.23x faster                                                   |
| pickle_pure_python               | 139 us                                                   | 114 us: 1.23x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 542 ms: 1.23x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 84.2 us: 1.22x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 17.5 ms: 1.22x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.84 sec: 1.22x faster                                                  |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 279 ms: 1.21x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 32.0 ms: 1.21x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.71 ms: 1.21x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                    |
| fannkuch                         | 176 ms                                                   | 148 ms: 1.19x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 22.7 ms: 1.18x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 46.6 ms: 1.17x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.17x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 33.4 ms: 1.16x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 61.4 us: 1.16x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| docutils                         | 1.02 sec                                                 | 933 ms: 1.09x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 52.9 ms: 1.09x faster                                                   |
| sphinx                           | 434 ms                                                   | 399 ms: 1.09x faster                                                    |
| sympy_str                        | 104 ms                                                   | 96.5 ms: 1.08x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.46 ms: 1.08x faster                                                   |
| meteor_contest                   | 47.7 ms                                                  | 44.5 ms: 1.07x faster                                                   |
| json                             | 1.93 ms                                                  | 1.81 ms: 1.07x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 217 ms: 1.06x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 93.7 ms: 1.06x faster                                                   |
| json_loads                       | 10.9 us                                                  | 10.2 us: 1.06x faster                                                   |
| sympy_expand                     | 167 ms                                                   | 158 ms: 1.05x faster                                                    |
| thrift                           | 322 us                                                   | 306 us: 1.05x faster                                                    |
| pycparser                        | 497 ms                                                   | 474 ms: 1.05x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 922 ns: 1.05x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 22.2 ms: 1.04x faster                                                   |
| gc_traversal                     | 2.01 ms                                                  | 1.94 ms: 1.04x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 185 ms: 1.03x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 66.6 ms: 1.02x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.47 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                    |
| connected_components             | 201 ms                                                   | 202 ms: 1.01x slower                                                    |
| shortest_path                    | 219 ms                                                   | 221 ms: 1.01x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 429 us: 1.02x slower                                                    |
| k_core                           | 1.12 sec                                                 | 1.15 sec: 1.03x slower                                                  |
| create_gc_cycles                 | 830 us                                                   | 871 us: 1.05x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.6 ms: 1.07x slower                                                   |
| many_optionals                   | 195 us                                                   | 222 us: 1.13x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 46.7 ms: 1.18x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 254 ms: 1.19x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.1 ms: 1.23x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 147 ms: 1.31x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 95.7 ms: 2.98x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                            |

Benchmark hidden because not significant (1): telco
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: 2to3, chameleon, djangocms, genshi_text, genshi_xml, gevent_hub, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260509-3.16.0a0-cc5cf14-JIT/bm-20260509-macm4pro-arm64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json: pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.257x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.17x
- 99% likely to have a speedup of 1.15x

# Memory
- memory change: 1.25x