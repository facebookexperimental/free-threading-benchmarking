# Results vs. 3.12.6

- fork: python
- ref: bedaea05987738c4c6b9
- machine: darwin-arm64
- commit hash: bedaea0
- commit date: 2025-10-19
- overall geometric mean: 1.153x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x faster
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 108 ms: 1.05x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| html5lib       | 23.0 ms                                                  | 22.2 ms: 1.04x faster                                                    |
| sphinx         | 434 ms                                                   | 391 ms: 1.11x faster                                                     |
| Geometric mean | (ref)                                                    | 1.05x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 237 ms: 2.10x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 242 ms: 1.98x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 246 ms: 1.87x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 242 ms: 1.84x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.70x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 107 ms: 1.67x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.54x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.95 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 256 ms: 1.32x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 258 ms: 1.29x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| async_generators                 | 206 ms                                                   | 171 ms: 1.21x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 39.0 ms: 1.17x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.14x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 83.9 ms: 2.61x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.29x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.0 ms: 1.31x faster                                                    |
| nbody          | 54.2 ms                                                  | 48.1 ms: 1.13x faster                                                    |
| Geometric mean | (ref)                                                    | 1.14x faster                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 43.8 ms: 1.25x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.53 ms: 1.09x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.8 ms: 1.03x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 10.2 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 775 ms: 1.24x faster                                                     |
| xml_etree_iterparse  | 51.6 ms                                                  | 42.5 ms: 1.21x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 32.7 ms: 1.19x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.70 ms: 1.15x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 89.5 us: 1.15x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 23.4 ms: 1.14x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 61.0 ms: 1.11x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.4 us: 1.04x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 134 us: 1.04x faster                                                     |
| Geometric mean       | (ref)                                                    | 1.14x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.67 ms: 1.08x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.23 ms: 1.09x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.01 ms: 1.16x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 19.4 ms: 1.12x faster                                                    |
| mako            | 4.77 ms                                                  | 4.62 ms: 1.03x faster                                                    |
| django_template | 13.6 ms                                                  | 14.0 ms: 1.02x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.07x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 521 ms: 2.10x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 237 ms: 2.10x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 242 ms: 1.98x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 246 ms: 1.87x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 242 ms: 1.84x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 101 ms: 1.70x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 107 ms: 1.67x faster                                                     |
| deepcopy                         | 161 us                                                   | 96.8 us: 1.67x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.0 us: 1.66x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                     |
| generators                       | 21.9 ms                                                  | 14.0 ms: 1.57x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.54x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.03 us: 1.42x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.98 us: 1.41x faster                                                    |
| go                               | 70.0 ms                                                  | 50.2 ms: 1.40x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.95 ms: 1.36x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 256 ms: 1.32x faster                                                     |
| float                            | 37.9 ms                                                  | 29.0 ms: 1.31x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 39.1 ns: 1.30x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 258 ms: 1.29x faster                                                     |
| raytrace                         | 145 ms                                                   | 115 ms: 1.27x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 43.8 ms: 1.25x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 775 ms: 1.24x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.23x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.42 ms: 1.21x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 17.1 ms: 1.21x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 42.5 ms: 1.21x faster                                                    |
| async_generators                 | 206 ms                                                   | 171 ms: 1.21x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.15 us: 1.20x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.35 us: 1.19x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 51.2 ms: 1.19x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.56 ms: 1.19x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 32.7 ms: 1.19x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 45.8 ms: 1.19x faster                                                    |
| pyflate                          | 216 ms                                                   | 182 ms: 1.19x faster                                                     |
| pylint                           | 128 ms                                                   | 109 ms: 1.18x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.5 ms: 1.18x faster                                                    |
| richards                         | 22.4 ms                                                  | 19.1 ms: 1.18x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 37.0 ms: 1.18x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 21.6 ms: 1.17x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 39.0 ms: 1.17x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.2 ms: 1.17x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 60.9 us: 1.16x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 122 ms: 1.16x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 44.1 ms: 1.16x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.01 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.94 sec: 1.16x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.70 ms: 1.15x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 89.5 us: 1.15x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 23.4 ms: 1.14x faster                                                    |
| k_core                           | 1.12 sec                                                 | 983 ms: 1.14x faster                                                     |
| chaos                            | 28.9 ms                                                  | 25.5 ms: 1.13x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.12 ms: 1.13x faster                                                    |
| nbody                            | 54.2 ms                                                  | 48.1 ms: 1.13x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 19.4 ms: 1.12x faster                                                    |
| thrift                           | 322 us                                                   | 289 us: 1.11x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 61.0 ms: 1.11x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.0 ms: 1.11x faster                                                    |
| sympy_str                        | 104 ms                                                   | 93.9 ms: 1.11x faster                                                    |
| sphinx                           | 434 ms                                                   | 391 ms: 1.11x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 52.3 ms: 1.10x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.53 ms: 1.09x faster                                                    |
| pycparser                        | 497 ms                                                   | 457 ms: 1.09x faster                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.91 ms: 1.09x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 618 ms: 1.08x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 305 ms: 1.07x faster                                                     |
| sympy_expand                     | 167 ms                                                   | 156 ms: 1.07x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 218 ms: 1.06x faster                                                     |
| 2to3                             | 114 ms                                                   | 108 ms: 1.05x faster                                                     |
| json                             | 1.93 ms                                                  | 1.84 ms: 1.05x faster                                                    |
| bench_thread_pool                | 419 us                                                   | 398 us: 1.05x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 37.3 ms: 1.04x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.4 us: 1.04x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 134 us: 1.04x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 932 ns: 1.04x faster                                                     |
| html5lib                         | 23.0 ms                                                  | 22.2 ms: 1.04x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.62 ms: 1.03x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 96.8 ms: 1.03x faster                                                    |
| fannkuch                         | 176 ms                                                   | 172 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.03 ms: 1.01x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.0 ms: 1.02x slower                                                    |
| shortest_path                    | 219 ms                                                   | 225 ms: 1.03x slower                                                     |
| connected_components             | 201 ms                                                   | 209 ms: 1.04x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 41.3 ms: 1.04x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 10.2 ms: 1.06x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.78 ms: 1.07x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.67 ms: 1.08x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 904 us: 1.09x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.23 ms: 1.09x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 128 ms: 1.14x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 244 ms: 1.15x slower                                                     |
| coverage                         | 26.9 ms                                                  | 31.9 ms: 1.19x slower                                                    |
| many_optionals                   | 195 us                                                   | 354 us: 1.81x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 83.9 ms: 2.61x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.15x faster                                                             |

Benchmark hidden because not significant (2): pidigits, meteor_contest
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251019-3.15.0a1+-bedaea0-CLANG/bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.153x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.09x

# Memory
- memory change: 1.19x