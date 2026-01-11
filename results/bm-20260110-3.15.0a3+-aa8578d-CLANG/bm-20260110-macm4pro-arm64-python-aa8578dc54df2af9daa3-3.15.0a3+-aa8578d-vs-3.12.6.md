# Results vs. 3.12.6

- fork: python
- ref: aa8578dc54df2af9daa3
- machine: darwin-arm64
- commit hash: aa8578d
- commit date: 2026-01-10
- overall geometric mean: 1.187x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x faster
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 111 ms: 1.03x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                   |
| html5lib       | 23.0 ms                                                  | 21.0 ms: 1.10x faster                                                    |
| sphinx         | 434 ms                                                   | 380 ms: 1.14x faster                                                     |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 220 ms: 2.26x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 219 ms: 2.19x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 218 ms: 2.05x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 228 ms: 2.02x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.1 ms: 1.80x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 97.7 ms: 1.76x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 134 ms: 1.72x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 136 ms: 1.63x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 251 ms: 1.35x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.26x faster                                                     |
| async_generators                 | 206 ms                                                   | 173 ms: 1.20x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 39.4 ms: 1.16x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 217 ms: 1.06x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.05x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 237 ms: 1.12x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.4 ms: 2.47x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.35x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.2 ms: 1.34x faster                                                    |
| nbody          | 54.2 ms                                                  | 44.8 ms: 1.21x faster                                                    |
| pidigits       | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                    | 1.18x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 43.1 ms: 1.27x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 97.6 ms: 1.02x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.69 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                    | 1.10x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.7 ms: 1.37x faster                                                    |
| tomli_loads          | 957 ms                                                   | 771 ms: 1.24x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 32.1 ms: 1.21x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.68 ms: 1.16x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 23.3 ms: 1.15x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 61.3 ms: 1.11x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 92.9 us: 1.11x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.5 us: 1.03x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 136 us: 1.03x faster                                                     |
| Geometric mean       | (ref)                                                    | 1.15x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.57 ms: 1.07x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.18 ms: 1.08x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.19 ms: 1.14x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 19.6 ms: 1.11x faster                                                    |
| mako            | 4.77 ms                                                  | 4.73 ms: 1.01x faster                                                    |
| django_template | 13.6 ms                                                  | 13.7 ms: 1.01x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.06x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.91 ms: 5.31x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 220 ms: 2.26x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 219 ms: 2.19x faster                                                     |
| mdp                              | 1.09 sec                                                 | 524 ms: 2.08x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 218 ms: 2.05x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 228 ms: 2.02x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 99.1 ms: 1.80x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 97.7 ms: 1.76x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 134 ms: 1.72x faster                                                     |
| deepcopy                         | 161 us                                                   | 94.0 us: 1.72x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 136 ms: 1.63x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.3 us: 1.62x faster                                                    |
| generators                       | 21.9 ms                                                  | 14.7 ms: 1.49x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.92 us: 1.42x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.04 us: 1.41x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.7 ms: 1.37x faster                                                    |
| go                               | 70.0 ms                                                  | 51.2 ms: 1.37x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 251 ms: 1.35x faster                                                     |
| float                            | 37.9 ms                                                  | 28.2 ms: 1.34x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.3 ms: 1.32x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 39.1 ns: 1.30x faster                                                    |
| raytrace                         | 145 ms                                                   | 113 ms: 1.28x faster                                                     |
| regex_compile                    | 54.6 ms                                                  | 43.1 ms: 1.27x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 105 ms: 1.26x faster                                                     |
| k_core                           | 1.12 sec                                                 | 894 ms: 1.25x faster                                                     |
| tomli_loads                      | 957 ms                                                   | 771 ms: 1.24x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 49.3 ms: 1.24x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 44.8 ms: 1.21x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 32.1 ms: 1.21x faster                                                    |
| nbody                            | 54.2 ms                                                  | 44.8 ms: 1.21x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.44 ms: 1.20x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 42.8 ms: 1.20x faster                                                    |
| async_generators                 | 206 ms                                                   | 173 ms: 1.20x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.15 us: 1.19x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.36 us: 1.19x faster                                                    |
| pyflate                          | 216 ms                                                   | 185 ms: 1.17x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.6 ms: 1.17x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.61 ms: 1.16x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.4 ms: 1.16x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.68 ms: 1.16x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 39.4 ms: 1.16x faster                                                    |
| pylint                           | 128 ms                                                   | 111 ms: 1.16x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 124 ms: 1.15x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 22.1 ms: 1.15x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 23.3 ms: 1.15x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 62.0 us: 1.14x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                    |
| richards                         | 22.4 ms                                                  | 19.6 ms: 1.14x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.3 ms: 1.14x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 9.19 ms: 1.14x faster                                                    |
| sphinx                           | 434 ms                                                   | 380 ms: 1.14x faster                                                     |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.4 ms: 1.13x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.14 ms: 1.12x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.85 ms: 1.12x faster                                                    |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.9 ms: 1.12x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 19.6 ms: 1.11x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 61.3 ms: 1.11x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 92.9 us: 1.11x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 21.0 ms: 1.10x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 52.7 ms: 1.09x faster                                                    |
| sympy_str                        | 104 ms                                                   | 96.0 ms: 1.08x faster                                                    |
| thrift                           | 322 us                                                   | 298 us: 1.08x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 616 ms: 1.08x faster                                                     |
| pycparser                        | 497 ms                                                   | 461 ms: 1.08x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 305 ms: 1.08x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 217 ms: 1.06x faster                                                     |
| json                             | 1.93 ms                                                  | 1.85 ms: 1.04x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.3 ms: 1.04x faster                                                    |
| 2to3                             | 114 ms                                                   | 111 ms: 1.03x faster                                                     |
| json_loads                       | 10.9 us                                                  | 10.5 us: 1.03x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 162 ms: 1.03x faster                                                     |
| pickle_pure_python               | 139 us                                                   | 136 us: 1.03x faster                                                     |
| regex_dna                        | 99.6 ms                                                  | 97.6 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 187 ms: 1.02x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.00 sec: 1.02x faster                                                   |
| bench_thread_pool                | 419 us                                                   | 415 us: 1.01x faster                                                     |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                     |
| mako                             | 4.77 ms                                                  | 4.73 ms: 1.01x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 958 ns: 1.01x faster                                                     |
| pidigits                         | 161 ms                                                   | 160 ms: 1.01x faster                                                     |
| django_template                  | 13.6 ms                                                  | 13.7 ms: 1.01x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.69 ms: 1.01x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.03 ms: 1.01x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.3 ms: 1.01x slower                                                    |
| fannkuch                         | 176 ms                                                   | 179 ms: 1.02x slower                                                     |
| shortest_path                    | 219 ms                                                   | 225 ms: 1.03x slower                                                     |
| connected_components             | 201 ms                                                   | 210 ms: 1.05x slower                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 119 ms: 1.05x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.57 ms: 1.07x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.81 ms: 1.08x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.18 ms: 1.08x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 908 us: 1.09x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 44.0 ms: 1.11x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 237 ms: 1.12x slower                                                     |
| coverage                         | 26.9 ms                                                  | 31.4 ms: 1.17x slower                                                    |
| many_optionals                   | 195 us                                                   | 247 us: 1.27x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 79.4 ms: 2.47x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.18x faster                                                             |
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260110-3.15.0a3+-aa8578d-CLANG/bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.187x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.11x
- 95% likely to have a speedup of 1.11x
- 99% likely to have a speedup of 1.09x

# Memory
- memory change: 1.21x