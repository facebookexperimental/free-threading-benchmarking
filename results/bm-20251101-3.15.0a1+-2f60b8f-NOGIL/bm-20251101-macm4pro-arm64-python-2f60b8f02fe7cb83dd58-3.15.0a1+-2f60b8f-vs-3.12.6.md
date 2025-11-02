# Results vs. 3.12.6

- fork: python
- ref: 2f60b8f02fe7cb83dd58
- machine: darwin-arm64
- commit hash: 2f60b8f
- commit date: 2025-11-01
- overall geometric mean: 1.072x faster
- HPT reliability: 92.03%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 125 ms: 1.10x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| html5lib       | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                    |
| sphinx         | 434 ms                                                   | 419 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                    | 1.02x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 206 ms: 2.40x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 200 ms: 2.40x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 196 ms: 2.27x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 212 ms: 2.17x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 87.6 ms: 1.96x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.85x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 239 ms: 1.42x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 247 ms: 1.35x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 11.0 ms: 1.23x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                     |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 230 ms: 1.08x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 49.6 ms: 1.09x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.8 ms: 2.45x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.36x faster                                                             |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.7 ms: 1.27x faster                                                    |
| pidigits       | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| nbody          | 54.2 ms                                                  | 57.3 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.0 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.43 ms: 1.02x faster                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.9 ms: 1.29x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 59.3 ms: 1.15x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 4.11 ms: 1.04x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 37.9 ms: 1.03x faster                                                    |
| tomli_loads          | 957 ms                                                   | 979 ms: 1.02x slower                                                     |
| xml_etree_process    | 26.7 ms                                                  | 27.7 ms: 1.04x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 112 us: 1.09x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 154 us: 1.11x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.02x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.66 ms: 1.21x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.03 ms: 1.23x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.22x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 24.9 ms: 1.14x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 12.0 ms: 1.15x slower                                                    |
| mako            | 4.77 ms                                                  | 5.92 ms: 1.24x slower                                                    |
| django_template | 13.6 ms                                                  | 17.0 ms: 1.25x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.19x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 764 us: 2.63x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 206 ms: 2.40x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 200 ms: 2.40x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 196 ms: 2.27x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 212 ms: 2.17x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 87.6 ms: 1.96x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.85x faster                                                     |
| mdp                              | 1.09 sec                                                 | 614 ms: 1.78x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 101 ms: 1.76x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 478 us: 1.74x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 131 ms: 1.70x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 239 ms: 1.42x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 13.2 us: 1.39x faster                                                    |
| deepcopy                         | 161 us                                                   | 118 us: 1.37x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 247 ms: 1.35x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.9 ms: 1.29x faster                                                    |
| float                            | 37.9 ms                                                  | 29.7 ms: 1.27x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 11.0 ms: 1.23x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.20x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 837 ns: 1.15x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 59.3 ms: 1.15x faster                                                    |
| generators                       | 21.9 ms                                                  | 19.1 ms: 1.15x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.59 us: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.14x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.28 us: 1.14x faster                                                    |
| async_generators                 | 206 ms                                                   | 183 ms: 1.13x faster                                                     |
| k_core                           | 1.12 sec                                                 | 993 ms: 1.13x faster                                                     |
| go                               | 70.0 ms                                                  | 62.4 ms: 1.12x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 45.6 ns: 1.12x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.1 ms: 1.11x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.04 sec: 1.10x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 55.9 ms: 1.09x faster                                                    |
| raytrace                         | 145 ms                                                   | 133 ms: 1.09x faster                                                     |
| pyflate                          | 216 ms                                                   | 199 ms: 1.09x faster                                                     |
| pylint                           | 128 ms                                                   | 118 ms: 1.08x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 50.3 ms: 1.08x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 19.2 ms: 1.08x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.63 ms: 1.06x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 135 ms: 1.05x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 95.0 ms: 1.05x faster                                                    |
| pycparser                        | 497 ms                                                   | 478 ms: 1.04x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 4.11 ms: 1.04x faster                                                    |
| sphinx                           | 434 ms                                                   | 419 ms: 1.04x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 37.9 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| regex_v8                         | 9.59 ms                                                  | 9.43 ms: 1.02x faster                                                    |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.55 us: 1.01x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 8.10 ms: 1.01x slower                                                    |
| dask                             | 528 ms                                                   | 533 ms: 1.01x slower                                                     |
| pidigits                         | 161 ms                                                   | 163 ms: 1.01x slower                                                     |
| tomli_loads                      | 957 ms                                                   | 979 ms: 1.02x slower                                                     |
| chaos                            | 28.9 ms                                                  | 29.6 ms: 1.02x slower                                                    |
| nqueens                          | 43.5 ms                                                  | 44.6 ms: 1.03x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.7 ms: 1.03x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.7 ms: 1.04x slower                                                    |
| json                             | 1.93 ms                                                  | 2.01 ms: 1.04x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.20 ms: 1.05x slower                                                    |
| nbody                            | 54.2 ms                                                  | 57.3 ms: 1.06x slower                                                    |
| thrift                           | 322 us                                                   | 340 us: 1.06x slower                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 75.0 us: 1.06x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.5 us: 1.06x slower                                                    |
| fannkuch                         | 176 ms                                                   | 185 ms: 1.06x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 34.2 ms: 1.06x slower                                                    |
| shortest_path                    | 219 ms                                                   | 233 ms: 1.06x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 61.3 ms: 1.07x slower                                                    |
| richards                         | 22.4 ms                                                  | 24.0 ms: 1.07x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.23 ms: 1.08x slower                                                    |
| sympy_str                        | 104 ms                                                   | 112 ms: 1.08x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 27.4 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 230 ms: 1.08x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 43.0 ms: 1.08x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.6 ms: 1.09x slower                                                    |
| unpickle_pure_python             | 103 us                                                   | 112 us: 1.09x slower                                                     |
| 2to3                             | 114 ms                                                   | 125 ms: 1.10x slower                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 360 ms: 1.10x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 730 ms: 1.10x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 42.8 ms: 1.10x slower                                                    |
| connected_components             | 201 ms                                                   | 222 ms: 1.10x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 154 us: 1.11x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 24.9 ms: 1.14x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 12.0 ms: 1.15x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 192 ms: 1.15x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.10 ms: 1.19x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 56.7 ms: 1.19x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.66 ms: 1.21x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.03 ms: 1.23x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.92 ms: 1.24x slower                                                    |
| django_template                  | 13.6 ms                                                  | 17.0 ms: 1.25x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 534 us: 1.28x slower                                                     |
| scimark_lu                       | 51.3 ms                                                  | 67.1 ms: 1.31x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.1 ms: 1.49x slower                                                    |
| many_optionals                   | 195 us                                                   | 389 us: 1.99x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.8 ms: 2.45x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.07x faster                                                             |

Benchmark hidden because not significant (3): async_tree_eager_memoization_tg, regex_compile, logging_format
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251101-3.15.0a1+-2f60b8f-NOGIL/bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.072x faster

# HPT report

- Reliability score: 92.03% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.34x