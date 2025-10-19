# Results vs. 3.12.6

- fork: python
- ref: bedaea05987738c4c6b9
- machine: darwin-arm64
- commit hash: bedaea0
- commit date: 2025-10-19
- overall geometric mean: 1.095x faster
- HPT reliability: 99.17%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| docutils       | 1.02 sec                                                 | 989 ms: 1.03x faster                                                     |
| html5lib       | 23.0 ms                                                  | 23.2 ms: 1.01x slower                                                    |
| sphinx         | 434 ms                                                   | 406 ms: 1.07x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 202 ms: 2.46x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.43x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 192 ms: 2.32x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.19x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 85.9 ms: 2.01x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.88x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.8 ms: 1.79x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.72x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 241 ms: 1.38x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.9 ms: 1.24x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                     |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 225 ms: 1.06x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 48.7 ms: 1.07x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.9 ms: 2.39x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.38x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.3 ms: 1.29x faster                                                    |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| nbody          | 54.2 ms                                                  | 56.2 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 93.2 ms: 1.07x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 52.6 ms: 1.04x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.25 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 36.4 ms: 1.42x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 55.9 ms: 1.22x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 36.4 ms: 1.07x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 4.00 ms: 1.06x faster                                                    |
| json_loads           | 10.9 us                                                  | 11.6 us: 1.07x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 150 us: 1.08x slower                                                     |
| unpickle_pure_python | 103 us                                                   | 111 us: 1.08x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.05x faster                                                             |

Benchmark hidden because not significant (2): xml_etree_process, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.61 ms: 1.20x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.00 ms: 1.23x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.21x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                    |
| genshi_xml      | 21.8 ms                                                  | 23.9 ms: 1.10x slower                                                    |
| mako            | 4.77 ms                                                  | 5.73 ms: 1.20x slower                                                    |
| django_template | 13.6 ms                                                  | 16.6 ms: 1.22x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.15x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 757 us: 2.65x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 202 ms: 2.46x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 197 ms: 2.43x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 192 ms: 2.32x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 209 ms: 2.19x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 85.9 ms: 2.01x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 123 ms: 1.88x faster                                                     |
| mdp                              | 1.09 sec                                                 | 597 ms: 1.83x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.8 ms: 1.79x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 467 us: 1.78x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 129 ms: 1.72x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 234 ms: 1.45x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 36.4 ms: 1.42x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 13.0 us: 1.40x faster                                                    |
| deepcopy                         | 161 us                                                   | 116 us: 1.39x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 241 ms: 1.38x faster                                                     |
| float                            | 37.9 ms                                                  | 29.3 ms: 1.29x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.9 ms: 1.24x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 55.9 ms: 1.22x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 109 ms: 1.21x faster                                                     |
| comprehensions                   | 9.84 us                                                  | 8.28 us: 1.19x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 816 ns: 1.19x faster                                                     |
| regex_effbot                     | 1.67 ms                                                  | 1.42 ms: 1.17x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.26 us: 1.16x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.16x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 44.0 ns: 1.16x faster                                                    |
| generators                       | 21.9 ms                                                  | 19.1 ms: 1.15x faster                                                    |
| go                               | 70.0 ms                                                  | 61.0 ms: 1.15x faster                                                    |
| async_generators                 | 206 ms                                                   | 181 ms: 1.14x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.8 ms: 1.13x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.99 sec: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 995 ms: 1.12x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 55.1 ms: 1.11x faster                                                    |
| pylint                           | 128 ms                                                   | 116 ms: 1.11x faster                                                     |
| raytrace                         | 145 ms                                                   | 131 ms: 1.10x faster                                                     |
| subparsers                       | 20.8 ms                                                  | 18.9 ms: 1.10x faster                                                    |
| pyflate                          | 216 ms                                                   | 197 ms: 1.10x faster                                                     |
| pycparser                        | 497 ms                                                   | 464 ms: 1.07x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 50.7 ms: 1.07x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 93.2 ms: 1.07x faster                                                    |
| sphinx                           | 434 ms                                                   | 406 ms: 1.07x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 36.4 ms: 1.07x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.62 ms: 1.07x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.00 ms: 1.06x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 134 ms: 1.06x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.04x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.47 us: 1.04x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 52.6 ms: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.25 ms: 1.04x faster                                                    |
| docutils                         | 1.02 sec                                                 | 989 ms: 1.03x faster                                                     |
| logging_format                   | 2.80 us                                                  | 2.74 us: 1.02x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 111 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 188 ms: 1.01x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.97 ms: 1.01x faster                                                    |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 531 ms: 1.01x slower                                                     |
| html5lib                         | 23.0 ms                                                  | 23.2 ms: 1.01x slower                                                    |
| chaos                            | 28.9 ms                                                  | 29.1 ms: 1.01x slower                                                    |
| json                             | 1.93 ms                                                  | 1.99 ms: 1.03x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.13 ms: 1.03x slower                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.3 ms: 1.03x slower                                                    |
| nbody                            | 54.2 ms                                                  | 56.2 ms: 1.04x slower                                                    |
| richards                         | 22.4 ms                                                  | 23.3 ms: 1.04x slower                                                    |
| thrift                           | 322 us                                                   | 334 us: 1.04x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 59.9 ms: 1.04x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 73.9 us: 1.04x slower                                                    |
| fannkuch                         | 176 ms                                                   | 184 ms: 1.05x slower                                                     |
| sympy_str                        | 104 ms                                                   | 109 ms: 1.05x slower                                                     |
| richards_super                   | 25.4 ms                                                  | 26.7 ms: 1.05x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 225 ms: 1.06x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 42.3 ms: 1.07x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 350 ms: 1.07x slower                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 48.7 ms: 1.07x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.6 us: 1.07x slower                                                    |
| 2to3                             | 114 ms                                                   | 122 ms: 1.07x slower                                                     |
| shortest_path                    | 219 ms                                                   | 235 ms: 1.07x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 150 us: 1.08x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 111 us: 1.08x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 716 ms: 1.08x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 42.2 ms: 1.09x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.9 ms: 1.10x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 56.4 ms: 1.10x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.29 ms: 1.10x slower                                                    |
| connected_components             | 201 ms                                                   | 223 ms: 1.11x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 187 ms: 1.12x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.02 ms: 1.16x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 56.8 ms: 1.19x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.61 ms: 1.20x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.73 ms: 1.20x slower                                                    |
| django_template                  | 13.6 ms                                                  | 16.6 ms: 1.22x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 7.00 ms: 1.23x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 542 us: 1.29x slower                                                     |
| coverage                         | 26.9 ms                                                  | 40.3 ms: 1.50x slower                                                    |
| many_optionals                   | 195 us                                                   | 384 us: 1.97x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 76.9 ms: 2.39x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (3): xml_etree_process, nqueens, tomli_loads
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20251019-3.15.0a1+-bedaea0-NOGIL/bm-20251019-macm4pro-arm64-python-bedaea05987738c4c6b9-3.15.0a1+-bedaea0.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.095x faster

# HPT report

- Reliability score: 99.17% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.33x