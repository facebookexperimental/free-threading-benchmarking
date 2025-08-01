# Results vs. 3.12.6

- fork: python
- ref: 47b01da4ccedd9c00fad
- machine: darwin-arm64
- commit hash: 47b01da
- commit date: 2025-07-12
- overall geometric mean: 1.090x faster
- HPT reliability: 96.07%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.26x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 124 ms: 1.09x slower                                                    |
| html5lib       | 23.0 ms                                                  | 24.0 ms: 1.04x slower                                                   |
| sphinx         | 434 ms                                                   | 418 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x slower                                                            |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 200 ms: 2.40x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 207 ms: 2.40x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 196 ms: 2.27x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 211 ms: 2.17x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 87.7 ms: 1.96x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 239 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.35x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.00x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 49.4 ms: 1.08x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 231 ms: 1.09x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.7 ms: 2.45x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.36x faster                                                            |

Benchmark hidden because not significant (1): async_tree_eager_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.5 ms: 1.28x faster                                                   |
| nbody          | 54.2 ms                                                  | 55.2 ms: 1.02x slower                                                   |
| pidigits       | 161 ms                                                   | 169 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.06x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_v8       | 9.59 ms                                                  | 9.27 ms: 1.03x faster                                                   |
| regex_compile  | 54.6 ms                                                  | 52.8 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                    | 1.05x faster                                                            |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 38.4 ms: 1.34x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 59.2 ms: 1.15x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 26.9 ms: 1.01x slower                                                   |
| tomli_loads          | 957 ms                                                   | 991 ms: 1.03x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.4 us: 1.05x slower                                                   |
| json_dumps           | 4.26 ms                                                  | 4.63 ms: 1.09x slower                                                   |
| unpickle_pure_python | 103 us                                                   | 113 us: 1.09x slower                                                    |
| pickle_pure_python   | 139 us                                                   | 155 us: 1.11x slower                                                    |
| Geometric mean       | (ref)                                                    | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.73 ms: 1.21x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 7.05 ms: 1.23x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.22x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                   |
| genshi_xml      | 21.8 ms                                                  | 23.7 ms: 1.09x slower                                                   |
| mako            | 4.77 ms                                                  | 5.72 ms: 1.20x slower                                                   |
| django_template | 13.6 ms                                                  | 16.4 ms: 1.20x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.14x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| gc_traversal                     | 2.01 ms                                                  | 791 us: 2.54x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 200 ms: 2.40x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 207 ms: 2.40x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 196 ms: 2.27x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 211 ms: 2.17x faster                                                    |
| subparsers                       | 20.8 ms                                                  | 10.0 ms: 2.07x faster                                                   |
| async_tree_none_tg               | 172 ms                                                   | 87.7 ms: 1.96x faster                                                   |
| mdp                              | 1.09 sec                                                 | 575 ms: 1.90x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 124 ms: 1.86x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 102 ms: 1.75x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 130 ms: 1.71x faster                                                    |
| create_gc_cycles                 | 830 us                                                   | 491 us: 1.69x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 239 ms: 1.42x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 246 ms: 1.35x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 38.4 ms: 1.34x faster                                                   |
| deepcopy                         | 161 us                                                   | 121 us: 1.34x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 14.0 us: 1.31x faster                                                   |
| float                            | 37.9 ms                                                  | 29.5 ms: 1.28x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.27x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.97 us: 1.23x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 110 ms: 1.19x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 818 ns: 1.18x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.26 us: 1.16x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 59.2 ms: 1.15x faster                                                   |
| go                               | 70.0 ms                                                  | 61.2 ms: 1.14x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| generators                       | 21.9 ms                                                  | 19.2 ms: 1.14x faster                                                   |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.97 sec: 1.14x faster                                                  |
| logging_silent                   | 50.9 ns                                                  | 44.9 ns: 1.13x faster                                                   |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                    |
| k_core                           | 1.12 sec                                                 | 996 ms: 1.12x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.1 ms: 1.12x faster                                                   |
| raytrace                         | 145 ms                                                   | 132 ms: 1.10x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 56.8 ms: 1.07x faster                                                   |
| pylint                           | 128 ms                                                   | 119 ms: 1.07x faster                                                    |
| pyflate                          | 216 ms                                                   | 202 ms: 1.07x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 51.4 ms: 1.06x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 36.9 ms: 1.05x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.64 ms: 1.05x faster                                                   |
| pycparser                        | 497 ms                                                   | 474 ms: 1.05x faster                                                    |
| sphinx                           | 434 ms                                                   | 418 ms: 1.04x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 41.9 ms: 1.04x faster                                                   |
| regex_v8                         | 9.59 ms                                                  | 9.27 ms: 1.03x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 52.8 ms: 1.03x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 140 ms: 1.01x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 3.01 ms: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.00x faster                                                    |
| dask                             | 528 ms                                                   | 530 ms: 1.01x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 26.9 ms: 1.01x slower                                                   |
| nbody                            | 54.2 ms                                                  | 55.2 ms: 1.02x slower                                                   |
| logging_simple                   | 2.57 us                                                  | 2.62 us: 1.02x slower                                                   |
| chaos                            | 28.9 ms                                                  | 29.5 ms: 1.02x slower                                                   |
| fannkuch                         | 176 ms                                                   | 180 ms: 1.03x slower                                                    |
| thrift                           | 322 us                                                   | 332 us: 1.03x slower                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 73.2 us: 1.03x slower                                                   |
| tomli_loads                      | 957 ms                                                   | 991 ms: 1.03x slower                                                    |
| logging_format                   | 2.80 us                                                  | 2.90 us: 1.04x slower                                                   |
| json                             | 1.93 ms                                                  | 2.00 ms: 1.04x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.0 ms: 1.04x slower                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 33.6 ms: 1.04x slower                                                   |
| pidigits                         | 161 ms                                                   | 169 ms: 1.05x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.4 us: 1.05x slower                                                   |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.05x slower                                                    |
| sympy_sum                        | 57.6 ms                                                  | 61.2 ms: 1.06x slower                                                   |
| richards                         | 22.4 ms                                                  | 23.9 ms: 1.07x slower                                                   |
| shortest_path                    | 219 ms                                                   | 234 ms: 1.07x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 350 ms: 1.07x slower                                                    |
| pprint_pformat                   | 665 ms                                                   | 714 ms: 1.07x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 27.3 ms: 1.08x slower                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 49.4 ms: 1.08x slower                                                   |
| genshi_text                      | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                   |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 231 ms: 1.09x slower                                                    |
| genshi_xml                       | 21.8 ms                                                  | 23.7 ms: 1.09x slower                                                   |
| json_dumps                       | 4.26 ms                                                  | 4.63 ms: 1.09x slower                                                   |
| 2to3                             | 114 ms                                                   | 124 ms: 1.09x slower                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 42.5 ms: 1.09x slower                                                   |
| unpickle_pure_python             | 103 us                                                   | 113 us: 1.09x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.29 ms: 1.10x slower                                                   |
| connected_components             | 201 ms                                                   | 222 ms: 1.11x slower                                                    |
| pickle_pure_python               | 139 us                                                   | 155 us: 1.11x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.12x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 58.1 ms: 1.13x slower                                                   |
| meteor_contest                   | 47.7 ms                                                  | 54.5 ms: 1.14x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 45.6 ms: 1.15x slower                                                   |
| mako                             | 4.77 ms                                                  | 5.72 ms: 1.20x slower                                                   |
| django_template                  | 13.6 ms                                                  | 16.4 ms: 1.20x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 9.73 ms: 1.21x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 7.05 ms: 1.23x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.25 ms: 1.24x slower                                                   |
| many_optionals                   | 195 us                                                   | 254 us: 1.30x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 581 us: 1.39x slower                                                    |
| coverage                         | 26.9 ms                                                  | 40.1 ms: 1.49x slower                                                   |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.7 ms: 2.45x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.08x faster                                                            |

Benchmark hidden because not significant (4): regex_dna, docutils, sympy_integrate, async_tree_eager_memoization_tg
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250712-3.15.0a0-47b01da-NOGIL/bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.090x faster

# HPT report

- Reliability score: 96.07% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.26x