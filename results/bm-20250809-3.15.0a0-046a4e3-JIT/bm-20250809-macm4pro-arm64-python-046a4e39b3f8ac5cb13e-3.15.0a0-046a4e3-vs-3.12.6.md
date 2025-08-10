# Results vs. 3.12.6

- fork: python
- ref: 046a4e39b3f8ac5cb13e
- machine: darwin-arm64
- commit hash: 046a4e3
- commit date: 2025-08-09
- overall geometric mean: 1.101x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 117 ms: 1.03x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                   |
| sphinx         | 434 ms                                                   | 407 ms: 1.07x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 244 ms: 2.03x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 248 ms: 1.93x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 253 ms: 1.81x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 254 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 109 ms: 1.63x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.52x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.90 ms: 1.37x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 265 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.6 ms: 1.09x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.8 ms: 2.70x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 31.1 ms: 1.22x faster                                                   |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                    |
| nbody          | 54.2 ms                                                  | 56.8 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 47.9 ms: 1.14x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 96.4 ms: 1.03x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.66 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.2 ms: 1.17x faster                                                   |
| tomli_loads          | 957 ms                                                   | 822 ms: 1.16x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 33.8 ms: 1.15x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 23.6 ms: 1.13x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.78 ms: 1.13x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 92.4 us: 1.11x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 62.1 ms: 1.09x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 141 us: 1.01x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.1 us: 1.03x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.72 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.24 ms: 1.09x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.44 ms: 1.08x faster                                                   |
| genshi_text     | 10.5 ms                                                  | 9.89 ms: 1.06x faster                                                   |
| django_template | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.00x faster                                                            |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 244 ms: 2.03x faster                                                    |
| mdp                              | 1.09 sec                                                 | 542 ms: 2.02x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 248 ms: 1.93x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 253 ms: 1.81x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 254 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 109 ms: 1.63x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.52x faster                                                    |
| deepcopy                         | 161 us                                                   | 111 us: 1.46x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.9 us: 1.42x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 9.90 ms: 1.37x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.38 us: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 265 ms: 1.28x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.27x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 40.5 ns: 1.26x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.6 ms: 1.25x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 44.3 ms: 1.23x faster                                                   |
| go                               | 70.0 ms                                                  | 57.3 ms: 1.22x faster                                                   |
| raytrace                         | 145 ms                                                   | 119 ms: 1.22x faster                                                    |
| float                            | 37.9 ms                                                  | 31.1 ms: 1.22x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 17.2 ms: 1.21x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 50.9 ms: 1.20x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.1 ms: 1.18x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.2 ms: 1.17x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 822 ms: 1.16x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 33.8 ms: 1.15x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 47.9 ms: 1.14x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.14x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 23.6 ms: 1.13x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.78 ms: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 992 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.13x faster                                                  |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                    |
| pylint                           | 128 ms                                                   | 114 ms: 1.12x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 293 ms: 1.12x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 595 ms: 1.12x faster                                                    |
| pyflate                          | 216 ms                                                   | 194 ms: 1.12x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 92.4 us: 1.11x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 63.7 us: 1.11x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 39.4 ms: 1.10x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 129 ms: 1.10x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.6 ms: 1.09x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 62.1 ms: 1.09x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.7 ms: 1.09x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 47.3 ms: 1.08x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.38 us: 1.08x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.60 us: 1.08x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.44 ms: 1.08x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.83 ms: 1.07x faster                                                   |
| sphinx                           | 434 ms                                                   | 407 ms: 1.07x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.9 ms: 1.06x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.56 ms: 1.06x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.1 ms: 1.06x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.89 ms: 1.06x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 30.6 ms: 1.05x faster                                                   |
| thrift                           | 322 us                                                   | 307 us: 1.05x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.66 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.4 ms: 1.03x faster                                                   |
| fannkuch                         | 176 ms                                                   | 170 ms: 1.03x faster                                                    |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 56.1 ms: 1.03x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.8 ms: 1.03x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 949 ns: 1.02x faster                                                    |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.66 ms: 1.01x slower                                                   |
| asyncio_websockets               | 190 ms                                                   | 192 ms: 1.01x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 141 us: 1.01x slower                                                    |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                    |
| 2to3                             | 114 ms                                                   | 117 ms: 1.03x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 172 ms: 1.03x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.1 us: 1.03x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.03x slower                                                  |
| meteor_contest                   | 47.7 ms                                                  | 49.4 ms: 1.04x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 436 us: 1.04x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.09 ms: 1.04x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.16 ms: 1.04x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                   |
| nbody                            | 54.2 ms                                                  | 56.8 ms: 1.05x slower                                                   |
| shortest_path                    | 219 ms                                                   | 234 ms: 1.07x slower                                                    |
| connected_components             | 201 ms                                                   | 218 ms: 1.09x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.72 ms: 1.09x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.24 ms: 1.09x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.92 ms: 1.12x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.5 ms: 1.12x slower                                                   |
| django_template                  | 13.6 ms                                                  | 15.3 ms: 1.12x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 944 us: 1.14x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.1 ms: 1.23x slower                                                   |
| many_optionals                   | 195 us                                                   | 323 us: 1.65x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.8 ms: 2.70x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (3): genshi_xml, pycparser, json
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250809-3.15.0a0-046a4e3-JIT/bm-20250809-macm4pro-arm64-python-046a4e39b3f8ac5cb13e-3.15.0a0-046a4e3.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.101x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.17x