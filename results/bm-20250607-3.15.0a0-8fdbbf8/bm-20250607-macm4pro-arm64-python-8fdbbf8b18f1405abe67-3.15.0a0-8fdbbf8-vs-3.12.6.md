# Results vs. 3.12.6

- fork: python
- ref: 8fdbbf8b18f1405abe67
- machine: darwin-arm64
- commit hash: 8fdbbf8
- commit date: 2025-06-07
- overall geometric mean: 1.120x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                  |
| html5lib       | 23.0 ms                                                  | 23.6 ms: 1.02x slower                                                   |
| sphinx         | 434 ms                                                   | 403 ms: 1.08x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 248 ms: 2.00x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 251 ms: 1.91x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 254 ms: 1.81x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 252 ms: 1.77x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.62x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.55x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.53x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.26x faster                                                    |
| async_generators                 | 206 ms                                                   | 172 ms: 1.20x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 42.1 ms: 1.08x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.17x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.7 ms: 2.73x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.7 ms: 1.27x faster                                                   |
| nbody          | 54.2 ms                                                  | 46.9 ms: 1.16x faster                                                   |
| Geometric mean | (ref)                                                    | 1.14x faster                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 47.5 ms: 1.15x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 95.8 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 43.9 ms: 1.18x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 60.6 ms: 1.12x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 35.5 ms: 1.10x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 95.3 us: 1.08x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 25.1 ms: 1.06x faster                                                   |
| tomli_loads          | 957 ms                                                   | 928 ms: 1.03x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.6 us: 1.02x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 143 us: 1.03x slower                                                    |
| json_dumps           | 4.26 ms                                                  | 4.44 ms: 1.04x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.52 ms: 1.06x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.10 ms: 1.07x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.07x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.86 ms: 1.06x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.4 ms: 1.02x faster                                                   |
| mako            | 4.77 ms                                                  | 4.90 ms: 1.03x slower                                                   |
| django_template | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.02x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.57 ms: 2.17x faster                                                   |
| mdp                              | 1.09 sec                                                 | 508 ms: 2.15x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 248 ms: 2.00x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 251 ms: 1.91x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 254 ms: 1.81x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 252 ms: 1.77x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.64x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.62x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.55x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 146 ms: 1.53x faster                                                    |
| deepcopy                         | 161 us                                                   | 108 us: 1.49x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.3 us: 1.49x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.2 ms: 1.34x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.41 us: 1.33x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.28x faster                                                   |
| float                            | 37.9 ms                                                  | 29.7 ms: 1.27x faster                                                   |
| go                               | 70.0 ms                                                  | 55.1 ms: 1.27x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.3 ms: 1.27x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.26x faster                                                    |
| raytrace                         | 145 ms                                                   | 117 ms: 1.24x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 49.8 ms: 1.22x faster                                                   |
| dulwich_log                      | 21.3 ms                                                  | 17.6 ms: 1.21x faster                                                   |
| async_generators                 | 206 ms                                                   | 172 ms: 1.20x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 45.4 ms: 1.20x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                    |
| k_core                           | 1.12 sec                                                 | 950 ms: 1.18x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 43.9 ms: 1.18x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.44 ms: 1.16x faster                                                   |
| nbody                            | 54.2 ms                                                  | 46.9 ms: 1.16x faster                                                   |
| pylint                           | 128 ms                                                   | 111 ms: 1.15x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 47.5 ms: 1.15x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.95 sec: 1.15x faster                                                  |
| typing_runtime_protocols         | 71.0 us                                                  | 61.9 us: 1.15x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.51 ms: 1.14x faster                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.83 ms: 1.13x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.13x faster                                                   |
| pyflate                          | 216 ms                                                   | 192 ms: 1.13x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 38.7 ms: 1.12x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 60.6 ms: 1.12x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.8 ms: 1.12x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.73 ms: 1.11x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.1 ms: 1.11x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 129 ms: 1.10x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.30 ms: 1.10x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 35.5 ms: 1.10x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 47.0 ms: 1.09x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 42.1 ms: 1.08x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 95.3 us: 1.08x faster                                                   |
| sphinx                           | 434 ms                                                   | 403 ms: 1.08x faster                                                    |
| thrift                           | 322 us                                                   | 300 us: 1.07x faster                                                    |
| sympy_str                        | 104 ms                                                   | 97.5 ms: 1.07x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 25.1 ms: 1.06x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.86 ms: 1.06x faster                                                   |
| richards                         | 22.4 ms                                                  | 21.2 ms: 1.06x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 24.2 ms: 1.05x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 54.9 ms: 1.05x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.2 ms: 1.04x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 95.8 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 223 ms: 1.04x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.71 us: 1.03x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 928 ms: 1.03x faster                                                    |
| json                             | 1.93 ms                                                  | 1.88 ms: 1.03x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.50 us: 1.03x faster                                                   |
| pycparser                        | 497 ms                                                   | 485 ms: 1.03x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 944 ns: 1.02x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.6 us: 1.02x faster                                                   |
| genshi_xml                       | 21.8 ms                                                  | 21.4 ms: 1.02x faster                                                   |
| sympy_expand                     | 167 ms                                                   | 165 ms: 1.01x faster                                                    |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 218 ms: 1.00x faster                                                    |
| connected_components             | 201 ms                                                   | 202 ms: 1.01x slower                                                    |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.01x slower                                                  |
| gc_traversal                     | 2.01 ms                                                  | 2.04 ms: 1.02x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 23.6 ms: 1.02x slower                                                   |
| mako                             | 4.77 ms                                                  | 4.90 ms: 1.03x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 143 us: 1.03x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 431 us: 1.03x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.44 ms: 1.04x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.52 ms: 1.06x slower                                                   |
| pprint_pformat                   | 665 ms                                                   | 710 ms: 1.07x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 351 ms: 1.07x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.10 ms: 1.07x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 43.5 ms: 1.10x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 916 us: 1.10x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.4 ms: 1.13x slower                                                   |
| telco                            | 2.61 ms                                                  | 2.99 ms: 1.15x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.17x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.8 ms: 1.22x slower                                                   |
| many_optionals                   | 195 us                                                   | 241 us: 1.24x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.7 ms: 2.73x slower                                                   |
| logging_silent                   | 50.9 ns                                                  | 196 ns: 3.84x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (5): meteor_contest, pidigits, fannkuch, asyncio_websockets, regex_v8
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250607-3.15.0a0-8fdbbf8/bm-20250607-macm4pro-arm64-python-8fdbbf8b18f1405abe67-3.15.0a0-8fdbbf8.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.120x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.15x