# Results vs. 3.12.6

- fork: python
- ref: bedaea05987738c4c6b9
- machine: darwin-arm64
- commit hash: bedaea0
- commit date: 2025-10-19
- overall geometric mean: 1.109x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 116 ms: 1.02x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| html5lib       | 23.0 ms                                                  | 24.0 ms: 1.04x slower                                                    |
| sphinx         | 434 ms                                                   | 403 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                    | 1.00x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 245 ms: 2.03x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 247 ms: 1.95x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 248 ms: 1.85x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 251 ms: 1.78x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.60x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.92 ms: 1.37x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 261 ms: 1.30x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 263 ms: 1.27x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                     |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 41.6 ms: 1.10x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.1 ms: 2.68x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.6 ms: 1.28x faster                                                    |
| nbody          | 54.2 ms                                                  | 56.7 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.41 ms: 1.18x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 47.6 ms: 1.15x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.0 ms: 1.06x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.66 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 44.1 ms: 1.17x faster                                                    |
| tomli_loads          | 957 ms                                                   | 829 ms: 1.15x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 34.1 ms: 1.14x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.78 ms: 1.13x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 23.9 ms: 1.12x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 92.1 us: 1.12x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 63.3 ms: 1.07x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 138 us: 1.01x faster                                                     |
| json_loads           | 10.9 us                                                  | 11.1 us: 1.02x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.86 ms: 1.11x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.35 ms: 1.11x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.11x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.38 ms: 1.09x faster                                                    |
| genshi_text     | 10.5 ms                                                  | 9.87 ms: 1.06x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.9 ms: 1.00x slower                                                    |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.00x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 245 ms: 2.03x faster                                                     |
| mdp                              | 1.09 sec                                                 | 546 ms: 2.00x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 247 ms: 1.95x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 248 ms: 1.85x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 251 ms: 1.78x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 103 ms: 1.67x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.60x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.0 us: 1.52x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 148 ms: 1.50x faster                                                     |
| deepcopy                         | 161 us                                                   | 109 us: 1.48x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 9.92 ms: 1.37x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.43 us: 1.32x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 261 ms: 1.30x faster                                                     |
| float                            | 37.9 ms                                                  | 29.6 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 263 ms: 1.27x faster                                                     |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.27x faster                                                    |
| generators                       | 21.9 ms                                                  | 17.3 ms: 1.27x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 40.3 ns: 1.26x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 43.4 ms: 1.25x faster                                                    |
| raytrace                         | 145 ms                                                   | 116 ms: 1.25x faster                                                     |
| go                               | 70.0 ms                                                  | 56.1 ms: 1.25x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.3 ms: 1.24x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.41 ms: 1.18x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 17.8 ms: 1.17x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.1 ms: 1.17x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 122 ms: 1.17x faster                                                     |
| pyflate                          | 216 ms                                                   | 187 ms: 1.16x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 829 ms: 1.15x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 578 ms: 1.15x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 47.6 ms: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 34.1 ms: 1.14x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.52 ms: 1.14x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 288 ms: 1.14x faster                                                     |
| pylint                           | 128 ms                                                   | 113 ms: 1.13x faster                                                     |
| json_dumps                       | 4.26 ms                                                  | 3.78 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.12x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.8 ms: 1.12x faster                                                    |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                     |
| xml_etree_process                | 26.7 ms                                                  | 23.9 ms: 1.12x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 92.1 us: 1.12x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 39.0 ms: 1.12x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.31 us: 1.11x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.1 ms: 1.11x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.53 us: 1.11x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.1 ms: 1.10x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 64.6 us: 1.10x faster                                                    |
| k_core                           | 1.12 sec                                                 | 1.02 sec: 1.10x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 41.6 ms: 1.10x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.38 ms: 1.09x faster                                                    |
| sphinx                           | 434 ms                                                   | 403 ms: 1.07x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 47.8 ms: 1.07x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 63.3 ms: 1.07x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.84 ms: 1.07x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.51 ms: 1.07x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 23.8 ms: 1.07x faster                                                    |
| richards                         | 22.4 ms                                                  | 21.0 ms: 1.06x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.87 ms: 1.06x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.0 ms: 1.06x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 55.2 ms: 1.04x faster                                                    |
| sympy_str                        | 104 ms                                                   | 100 ms: 1.04x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                     |
| sqlite_synth                     | 967 ns                                                   | 932 ns: 1.04x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 37.7 ms: 1.03x faster                                                    |
| thrift                           | 322 us                                                   | 313 us: 1.03x faster                                                     |
| pycparser                        | 497 ms                                                   | 486 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| fannkuch                         | 176 ms                                                   | 173 ms: 1.01x faster                                                     |
| bench_thread_pool                | 419 us                                                   | 414 us: 1.01x faster                                                     |
| pickle_pure_python               | 139 us                                                   | 138 us: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.9 ms: 1.00x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.66 ms: 1.01x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.04 ms: 1.01x slower                                                    |
| 2to3                             | 114 ms                                                   | 116 ms: 1.02x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 170 ms: 1.02x slower                                                     |
| docutils                         | 1.02 sec                                                 | 1.04 sec: 1.02x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.1 us: 1.02x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.0 ms: 1.03x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.70 ms: 1.04x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 24.0 ms: 1.04x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.7 ms: 1.05x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 42.6 ms: 1.07x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 912 us: 1.10x slower                                                     |
| shortest_path                    | 219 ms                                                   | 241 ms: 1.10x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.86 ms: 1.11x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.35 ms: 1.11x slower                                                    |
| connected_components             | 201 ms                                                   | 225 ms: 1.12x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                     |
| coverage                         | 26.9 ms                                                  | 32.9 ms: 1.22x slower                                                    |
| many_optionals                   | 195 us                                                   | 378 us: 1.93x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 86.1 ms: 2.68x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.11x faster                                                             |

Benchmark hidden because not significant (3): json, pidigits, scimark_sparse_mat_mult
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251019-3.15.0a1+-bedaea0-JIT/bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.109x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.21x