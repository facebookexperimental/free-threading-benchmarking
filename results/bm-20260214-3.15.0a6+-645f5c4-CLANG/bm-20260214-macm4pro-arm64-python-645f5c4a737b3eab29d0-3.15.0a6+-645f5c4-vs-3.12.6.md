# Results vs. 3.12.6

- fork: python
- ref: 645f5c4a737b3eab29d0
- machine: darwin-arm64
- commit hash: 645f5c4
- commit date: 2026-02-14
- overall geometric mean: 1.184x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 109 ms: 1.05x faster                                                     |
| docutils       | 1.02 sec                                                 | 994 ms: 1.03x faster                                                     |
| html5lib       | 23.0 ms                                                  | 20.8 ms: 1.11x faster                                                    |
| sphinx         | 434 ms                                                   | 383 ms: 1.13x faster                                                     |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 213 ms: 2.33x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 219 ms: 2.19x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 211 ms: 2.11x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 218 ms: 2.11x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 97.0 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 94.4 ms: 1.82x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 132 ms: 1.75x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 134 ms: 1.66x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 245 ms: 1.38x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.33x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.30x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                     |
| async_generators                 | 206 ms                                                   | 172 ms: 1.20x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 39.3 ms: 1.16x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 117 ms: 1.04x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 231 ms: 1.09x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.6 ms: 2.44x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.36x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.9 ms: 1.31x faster                                                    |
| nbody          | 54.2 ms                                                  | 46.4 ms: 1.17x faster                                                    |
| Geometric mean | (ref)                                                    | 1.15x faster                                                             |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 43.3 ms: 1.26x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 96.8 ms: 1.03x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.80 ms: 1.02x slower                                                    |
| Geometric mean | (ref)                                                    | 1.09x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.3 ms: 1.35x faster                                                    |
| tomli_loads          | 957 ms                                                   | 783 ms: 1.22x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 32.4 ms: 1.20x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.73 ms: 1.14x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 23.4 ms: 1.14x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 60.8 ms: 1.12x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 92.6 us: 1.11x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.5 us: 1.04x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 136 us: 1.03x faster                                                     |
| Geometric mean       | (ref)                                                    | 1.15x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.66 ms: 1.08x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.27 ms: 1.10x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.09x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.08 ms: 1.16x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 19.8 ms: 1.10x faster                                                    |
| mako            | 4.77 ms                                                  | 4.73 ms: 1.01x faster                                                    |
| django_template | 13.6 ms                                                  | 13.9 ms: 1.02x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.06x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4 |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.82 ms: 5.44x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 213 ms: 2.33x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 219 ms: 2.19x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 211 ms: 2.11x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 218 ms: 2.11x faster                                                     |
| mdp                              | 1.09 sec                                                 | 519 ms: 2.10x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 97.0 ms: 1.84x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 94.4 ms: 1.82x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 132 ms: 1.75x faster                                                     |
| deepcopy                         | 161 us                                                   | 93.8 us: 1.72x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 134 ms: 1.66x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.3 us: 1.62x faster                                                    |
| generators                       | 21.9 ms                                                  | 14.8 ms: 1.48x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.00 us: 1.46x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.88 us: 1.43x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 245 ms: 1.38x faster                                                     |
| go                               | 70.0 ms                                                  | 51.7 ms: 1.35x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.3 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 250 ms: 1.33x faster                                                     |
| logging_silent                   | 50.9 ns                                                  | 38.7 ns: 1.31x faster                                                    |
| float                            | 37.9 ms                                                  | 28.9 ms: 1.31x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.30x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 43.3 ms: 1.26x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 48.4 ms: 1.26x faster                                                    |
| raytrace                         | 145 ms                                                   | 115 ms: 1.26x faster                                                     |
| k_core                           | 1.12 sec                                                 | 891 ms: 1.25x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 106 ms: 1.24x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 43.9 ms: 1.24x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 783 ms: 1.22x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.42 ms: 1.21x faster                                                    |
| async_generators                 | 206 ms                                                   | 172 ms: 1.20x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 32.4 ms: 1.20x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.18 us: 1.18x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.37 us: 1.18x faster                                                    |
| nbody                            | 54.2 ms                                                  | 46.4 ms: 1.17x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.16x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 39.3 ms: 1.16x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 122 ms: 1.16x faster                                                     |
| hexiom                           | 3.04 ms                                                  | 2.63 ms: 1.16x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.08 ms: 1.16x faster                                                    |
| pylint                           | 128 ms                                                   | 112 ms: 1.15x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.5 ms: 1.15x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.96 sec: 1.14x faster                                                   |
| json_dumps                       | 4.26 ms                                                  | 3.73 ms: 1.14x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 23.4 ms: 1.14x faster                                                    |
| richards                         | 22.4 ms                                                  | 19.6 ms: 1.14x faster                                                    |
| pyflate                          | 216 ms                                                   | 189 ms: 1.14x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 22.3 ms: 1.14x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 38.3 ms: 1.14x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.5 ms: 1.13x faster                                                    |
| sphinx                           | 434 ms                                                   | 383 ms: 1.13x faster                                                     |
| scimark_lu                       | 51.3 ms                                                  | 45.4 ms: 1.13x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 63.5 us: 1.12x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.8 ms: 1.12x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 92.6 us: 1.11x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 20.8 ms: 1.11x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.28 ms: 1.10x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 19.8 ms: 1.10x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.3 ms: 1.10x faster                                                    |
| pycparser                        | 497 ms                                                   | 458 ms: 1.09x faster                                                     |
| sympy_str                        | 104 ms                                                   | 97.2 ms: 1.07x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 216 ms: 1.07x faster                                                     |
| sympy_sum                        | 57.6 ms                                                  | 53.9 ms: 1.07x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 307 ms: 1.07x faster                                                     |
| thrift                           | 322 us                                                   | 303 us: 1.06x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 628 ms: 1.06x faster                                                     |
| 2to3                             | 114 ms                                                   | 109 ms: 1.05x faster                                                     |
| json                             | 1.93 ms                                                  | 1.85 ms: 1.04x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.5 us: 1.04x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 936 ns: 1.03x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 96.8 ms: 1.03x faster                                                    |
| docutils                         | 1.02 sec                                                 | 994 ms: 1.03x faster                                                     |
| pickle_pure_python               | 139 us                                                   | 136 us: 1.03x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 186 ms: 1.02x faster                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.03 ms: 1.02x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 164 ms: 1.02x faster                                                     |
| bench_thread_pool                | 419 us                                                   | 413 us: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 522 ms: 1.01x faster                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 38.5 ms: 1.01x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.73 ms: 1.01x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.02 ms: 1.01x slower                                                    |
| fannkuch                         | 176 ms                                                   | 177 ms: 1.01x slower                                                     |
| meteor_contest                   | 47.7 ms                                                  | 48.5 ms: 1.02x slower                                                    |
| django_template                  | 13.6 ms                                                  | 13.9 ms: 1.02x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.80 ms: 1.02x slower                                                    |
| shortest_path                    | 219 ms                                                   | 226 ms: 1.03x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 117 ms: 1.04x slower                                                     |
| connected_components             | 201 ms                                                   | 210 ms: 1.05x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.66 ms: 1.08x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 231 ms: 1.09x slower                                                     |
| create_gc_cycles                 | 830 us                                                   | 905 us: 1.09x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 6.27 ms: 1.10x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.87 ms: 1.10x slower                                                    |
| bench_mp_pool                    | 39.7 ms                                                  | 44.2 ms: 1.11x slower                                                    |
| coverage                         | 26.9 ms                                                  | 30.9 ms: 1.15x slower                                                    |
| many_optionals                   | 195 us                                                   | 241 us: 1.23x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.6 ms: 2.44x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.18x faster                                                             |

Benchmark hidden because not significant (1): pidigits
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260214-3.15.0a6+-645f5c4-CLANG/bm-20260214-macm4pro-arm64-python-645f5c4a737b3eab29d0-3.15.0a6+-645f5c4.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.184x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.10x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: 1.21x