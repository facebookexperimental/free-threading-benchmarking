# Results vs. 3.12.6

- fork: python
- ref: d3d94e0ed715829d9bf9
- machine: darwin-arm64
- commit hash: d3d94e0
- commit date: 2025-08-30
- overall geometric mean: 1.132x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 110 ms: 1.03x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| html5lib       | 23.0 ms                                                  | 22.4 ms: 1.03x faster                                                   |
| sphinx         | 434 ms                                                   | 407 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 240 ms: 2.07x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 247 ms: 1.94x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 251 ms: 1.83x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 251 ms: 1.78x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.66x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.63x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.52x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 263 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.26x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                    |
| async_generators                 | 206 ms                                                   | 174 ms: 1.18x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 39.3 ms: 1.16x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.17x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 85.3 ms: 2.65x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.27x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.3 ms: 1.29x faster                                                   |
| nbody          | 54.2 ms                                                  | 48.1 ms: 1.13x faster                                                   |
| pidigits       | 161 ms                                                   | 167 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                    | 1.12x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 44.0 ms: 1.24x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.74 ms: 1.05x slower                                                   |
| regex_dna      | 99.6 ms                                                  | 106 ms: 1.07x slower                                                    |
| regex_v8       | 9.59 ms                                                  | 11.3 ms: 1.18x slower                                                   |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 786 ms: 1.22x faster                                                    |
| xml_etree_generate   | 38.9 ms                                                  | 32.8 ms: 1.19x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.69 ms: 1.15x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 23.2 ms: 1.15x faster                                                   |
| xml_etree_iterparse  | 51.6 ms                                                  | 45.2 ms: 1.14x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 92.5 us: 1.11x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 134 us: 1.04x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 66.4 ms: 1.02x faster                                                   |
| json_loads           | 10.9 us                                                  | 11.2 us: 1.03x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.11x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.63 ms: 1.08x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.18 ms: 1.08x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.02 ms: 1.16x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 19.5 ms: 1.12x faster                                                   |
| mako            | 4.77 ms                                                  | 4.56 ms: 1.05x faster                                                   |
| django_template | 13.6 ms                                                  | 14.1 ms: 1.04x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.07x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 523 ms: 2.09x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 240 ms: 2.07x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 247 ms: 1.94x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 251 ms: 1.83x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 251 ms: 1.78x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 104 ms: 1.66x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 110 ms: 1.63x faster                                                    |
| deepcopy                         | 161 us                                                   | 101 us: 1.60x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.6 us: 1.58x faster                                                   |
| async_tree_memoization_tg        | 231 ms                                                   | 146 ms: 1.58x faster                                                    |
| generators                       | 21.9 ms                                                  | 14.3 ms: 1.54x faster                                                   |
| async_tree_memoization           | 223 ms                                                   | 147 ms: 1.52x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 7.04 us: 1.40x faster                                                   |
| go                               | 70.0 ms                                                  | 50.9 ms: 1.38x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.08 us: 1.35x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.1 ms: 1.34x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 38.8 ns: 1.31x faster                                                   |
| float                            | 37.9 ms                                                  | 29.3 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 263 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 264 ms: 1.26x faster                                                    |
| raytrace                         | 145 ms                                                   | 115 ms: 1.26x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 44.0 ms: 1.24x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 16.7 ms: 1.24x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 786 ms: 1.22x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.5 ms: 1.21x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.33 us: 1.20x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.14 us: 1.20x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 51.1 ms: 1.19x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 32.8 ms: 1.19x faster                                                   |
| async_generators                 | 206 ms                                                   | 174 ms: 1.18x faster                                                    |
| deltablue                        | 1.73 ms                                                  | 1.46 ms: 1.18x faster                                                   |
| hexiom                           | 3.04 ms                                                  | 2.58 ms: 1.18x faster                                                   |
| spectral_norm                    | 54.4 ms                                                  | 46.2 ms: 1.18x faster                                                   |
| richards                         | 22.4 ms                                                  | 19.1 ms: 1.17x faster                                                   |
| k_core                           | 1.12 sec                                                 | 954 ms: 1.17x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                  |
| genshi_text                      | 10.5 ms                                                  | 9.02 ms: 1.16x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 39.3 ms: 1.16x faster                                                   |
| richards_super                   | 25.4 ms                                                  | 21.9 ms: 1.16x faster                                                   |
| pylint                           | 128 ms                                                   | 111 ms: 1.16x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.69 ms: 1.15x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 23.2 ms: 1.15x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 61.7 us: 1.15x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 45.2 ms: 1.14x faster                                                   |
| scimark_lu                       | 51.3 ms                                                  | 45.0 ms: 1.14x faster                                                   |
| pyflate                          | 216 ms                                                   | 191 ms: 1.13x faster                                                    |
| chaos                            | 28.9 ms                                                  | 25.6 ms: 1.13x faster                                                   |
| nbody                            | 54.2 ms                                                  | 48.1 ms: 1.13x faster                                                   |
| nqueens                          | 43.5 ms                                                  | 38.6 ms: 1.13x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                   |
| genshi_xml                       | 21.8 ms                                                  | 19.5 ms: 1.12x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 92.5 us: 1.11x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 29.1 ms: 1.11x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.28 ms: 1.10x faster                                                   |
| thrift                           | 322 us                                                   | 292 us: 1.10x faster                                                    |
| sympy_str                        | 104 ms                                                   | 95.2 ms: 1.09x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 131 ms: 1.08x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 53.6 ms: 1.07x faster                                                   |
| sphinx                           | 434 ms                                                   | 407 ms: 1.06x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 309 ms: 1.06x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 627 ms: 1.06x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 159 ms: 1.05x faster                                                    |
| mako                             | 4.77 ms                                                  | 4.56 ms: 1.05x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 37.2 ms: 1.04x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 222 ms: 1.04x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 134 us: 1.04x faster                                                    |
| 2to3                             | 114 ms                                                   | 110 ms: 1.03x faster                                                    |
| pycparser                        | 497 ms                                                   | 482 ms: 1.03x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.02 ms: 1.03x faster                                                   |
| html5lib                         | 23.0 ms                                                  | 22.4 ms: 1.03x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 66.4 ms: 1.02x faster                                                   |
| bench_thread_pool                | 419 us                                                   | 410 us: 1.02x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 948 ns: 1.02x faster                                                    |
| fannkuch                         | 176 ms                                                   | 174 ms: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 524 ms: 1.01x faster                                                    |
| shortest_path                    | 219 ms                                                   | 221 ms: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.5 ms: 1.02x slower                                                   |
| json_loads                       | 10.9 us                                                  | 11.2 us: 1.03x slower                                                   |
| connected_components             | 201 ms                                                   | 207 ms: 1.03x slower                                                    |
| pidigits                         | 161 ms                                                   | 167 ms: 1.03x slower                                                    |
| django_template                  | 13.6 ms                                                  | 14.1 ms: 1.04x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.04x slower                                                  |
| gc_traversal                     | 2.01 ms                                                  | 2.08 ms: 1.04x slower                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.74 ms: 1.05x slower                                                   |
| regex_dna                        | 99.6 ms                                                  | 106 ms: 1.07x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.79 ms: 1.07x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.63 ms: 1.08x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.18 ms: 1.08x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.0 ms: 1.11x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 946 us: 1.14x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 129 ms: 1.14x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 248 ms: 1.17x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 11.3 ms: 1.18x slower                                                   |
| coverage                         | 26.9 ms                                                  | 32.0 ms: 1.19x slower                                                   |
| many_optionals                   | 195 us                                                   | 309 us: 1.58x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 85.3 ms: 2.65x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.13x faster                                                            |

Benchmark hidden because not significant (1): json
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250830-3.15.0a0-d3d94e0-CLANG/bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.132x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.13x