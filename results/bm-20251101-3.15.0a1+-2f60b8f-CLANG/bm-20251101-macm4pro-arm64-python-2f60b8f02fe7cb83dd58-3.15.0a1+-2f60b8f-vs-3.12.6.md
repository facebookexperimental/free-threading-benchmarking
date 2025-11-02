# Results vs. 3.12.6

- fork: python
- ref: 2f60b8f02fe7cb83dd58
- machine: darwin-arm64
- commit hash: 2f60b8f
- commit date: 2025-11-01
- overall geometric mean: 1.148x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 110 ms: 1.03x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| html5lib       | 23.0 ms                                                  | 21.0 ms: 1.09x faster                                                    |
| sphinx         | 434 ms                                                   | 397 ms: 1.09x faster                                                     |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 221 ms: 2.24x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 219 ms: 2.19x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 225 ms: 2.04x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 221 ms: 2.02x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 98.4 ms: 1.81x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 96.6 ms: 1.78x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.67x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 139 ms: 1.60x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.30x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 40.1 ms: 1.14x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 125 ms: 1.11x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.7 ms: 2.48x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.33x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 27.8 ms: 1.36x faster                                                    |
| nbody          | 54.2 ms                                                  | 47.9 ms: 1.13x faster                                                    |
| pidigits       | 161 ms                                                   | 164 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                    | 1.15x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 43.8 ms: 1.25x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 105 ms: 1.05x slower                                                     |
| regex_effbot   | 1.67 ms                                                  | 1.76 ms: 1.06x slower                                                    |
| regex_v8       | 9.59 ms                                                  | 11.2 ms: 1.17x slower                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 39.3 ms: 1.31x faster                                                    |
| tomli_loads          | 957 ms                                                   | 786 ms: 1.22x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 32.7 ms: 1.19x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 23.2 ms: 1.15x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 89.9 us: 1.14x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.84 ms: 1.11x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 63.4 ms: 1.07x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 137 us: 1.02x faster                                                     |
| json_loads           | 10.9 us                                                  | 10.6 us: 1.02x faster                                                    |
| Geometric mean       | (ref)                                                    | 1.13x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 5.71 ms                                                  | 6.20 ms: 1.09x slower                                                    |
| python_startup         | 8.01 ms                                                  | 8.72 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.32 ms: 1.12x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 20.4 ms: 1.07x faster                                                    |
| mako            | 4.77 ms                                                  | 4.58 ms: 1.04x faster                                                    |
| django_template | 13.6 ms                                                  | 14.1 ms: 1.03x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.05x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 221 ms: 2.24x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 219 ms: 2.19x faster                                                     |
| mdp                              | 1.09 sec                                                 | 524 ms: 2.08x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 225 ms: 2.04x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 221 ms: 2.02x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 98.4 ms: 1.81x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 96.6 ms: 1.78x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 138 ms: 1.67x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.1 us: 1.65x faster                                                    |
| deepcopy                         | 161 us                                                   | 98.2 us: 1.64x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 139 ms: 1.60x faster                                                     |
| generators                       | 21.9 ms                                                  | 14.2 ms: 1.54x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.90 us: 1.43x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.04 us: 1.40x faster                                                    |
| go                               | 70.0 ms                                                  | 51.2 ms: 1.37x faster                                                    |
| float                            | 37.9 ms                                                  | 27.8 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 253 ms: 1.32x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 39.3 ms: 1.31x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.5 ms: 1.30x faster                                                    |
| raytrace                         | 145 ms                                                   | 114 ms: 1.27x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 43.8 ms: 1.25x faster                                                    |
| k_core                           | 1.12 sec                                                 | 897 ms: 1.25x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 49.0 ms: 1.25x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 41.5 ns: 1.23x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 786 ms: 1.22x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 45.2 ms: 1.20x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.44 ms: 1.20x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 17.4 ms: 1.19x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 32.7 ms: 1.19x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.18 us: 1.18x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 121 ms: 1.18x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.39 us: 1.17x faster                                                    |
| pyflate                          | 216 ms                                                   | 185 ms: 1.17x faster                                                     |
| hexiom                           | 3.04 ms                                                  | 2.60 ms: 1.17x faster                                                    |
| richards                         | 22.4 ms                                                  | 19.2 ms: 1.17x faster                                                    |
| async_generators                 | 206 ms                                                   | 177 ms: 1.17x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 44.3 ms: 1.16x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 21.9 ms: 1.16x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 23.2 ms: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.7 ms: 1.15x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.5 ms: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.15x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 89.9 us: 1.14x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 40.1 ms: 1.14x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.5 ms: 1.13x faster                                                    |
| nbody                            | 54.2 ms                                                  | 47.9 ms: 1.13x faster                                                    |
| pylint                           | 128 ms                                                   | 113 ms: 1.13x faster                                                     |
| genshi_text                      | 10.5 ms                                                  | 9.32 ms: 1.12x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 63.1 us: 1.12x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.85 ms: 1.12x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 38.8 ms: 1.12x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.7 ms: 1.12x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.84 ms: 1.11x faster                                                    |
| thrift                           | 322 us                                                   | 293 us: 1.10x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 21.0 ms: 1.09x faster                                                    |
| sphinx                           | 434 ms                                                   | 397 ms: 1.09x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.36 ms: 1.09x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 616 ms: 1.08x faster                                                     |
| pycparser                        | 497 ms                                                   | 461 ms: 1.08x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 305 ms: 1.08x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 63.4 ms: 1.07x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 20.4 ms: 1.07x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 54.1 ms: 1.06x faster                                                    |
| sympy_str                        | 104 ms                                                   | 98.0 ms: 1.06x faster                                                    |
| bench_thread_pool                | 419 us                                                   | 399 us: 1.05x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.58 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                     |
| 2to3                             | 114 ms                                                   | 110 ms: 1.03x faster                                                     |
| sympy_expand                     | 167 ms                                                   | 163 ms: 1.03x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 37.9 ms: 1.03x faster                                                    |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 137 us: 1.02x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.6 us: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 524 ms: 1.01x faster                                                     |
| fannkuch                         | 176 ms                                                   | 178 ms: 1.02x slower                                                     |
| pidigits                         | 161 ms                                                   | 164 ms: 1.02x slower                                                     |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| shortest_path                    | 219 ms                                                   | 224 ms: 1.02x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 49.1 ms: 1.03x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.1 ms: 1.03x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.08 ms: 1.04x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 41.3 ms: 1.04x slower                                                    |
| connected_components             | 201 ms                                                   | 210 ms: 1.05x slower                                                     |
| regex_dna                        | 99.6 ms                                                  | 105 ms: 1.05x slower                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.76 ms: 1.06x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.20 ms: 1.09x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.72 ms: 1.09x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.86 ms: 1.10x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 125 ms: 1.11x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 934 us: 1.13x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 242 ms: 1.14x slower                                                     |
| regex_v8                         | 9.59 ms                                                  | 11.2 ms: 1.17x slower                                                    |
| coverage                         | 26.9 ms                                                  | 31.9 ms: 1.19x slower                                                    |
| many_optionals                   | 195 us                                                   | 348 us: 1.78x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.7 ms: 2.48x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.15x faster                                                             |

Benchmark hidden because not significant (1): sqlite_synth
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251101-3.15.0a1+-2f60b8f-CLANG/bm-20251101-macm4pro-arm64-python-2f60b8f02fe7cb83dd58-3.15.0a1+-2f60b8f.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.148x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.19x