# Results vs. 3.12.6

- fork: python
- ref: d3d94e0ed715829d9bf9
- machine: darwin-arm64
- commit hash: d3d94e0
- commit date: 2025-08-30
- overall geometric mean: 1.097x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 118 ms: 1.04x slower                                                    |
| docutils       | 1.02 sec                                                 | 1.06 sec: 1.03x slower                                                  |
| html5lib       | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                   |
| sphinx         | 434 ms                                                   | 409 ms: 1.06x faster                                                    |
| Geometric mean | (ref)                                                    | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 251 ms: 1.98x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 251 ms: 1.92x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 252 ms: 1.82x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 254 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.65x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.9 ms: 1.09x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.0 ms: 2.71x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.25x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 31.5 ms: 1.20x faster                                                   |
| pidigits       | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| nbody          | 54.2 ms                                                  | 56.8 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                    | 1.04x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 48.1 ms: 1.14x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 97.1 ms: 1.03x faster                                                   |
| Geometric mean | (ref)                                                    | 1.07x faster                                                            |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 957 ms                                                   | 823 ms: 1.16x faster                                                    |
| xml_etree_iterparse  | 51.6 ms                                                  | 44.5 ms: 1.16x faster                                                   |
| xml_etree_generate   | 38.9 ms                                                  | 34.2 ms: 1.14x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 23.7 ms: 1.13x faster                                                   |
| json_dumps           | 4.26 ms                                                  | 3.80 ms: 1.12x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 93.5 us: 1.10x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 64.2 ms: 1.06x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 141 us: 1.02x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.1 us: 1.03x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.09x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.74 ms: 1.09x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.28 ms: 1.10x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 4.51 ms: 1.06x faster                                                   |
| genshi_text     | 10.5 ms                                                  | 9.93 ms: 1.06x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 21.7 ms: 1.00x faster                                                   |
| django_template | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.00x slower                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0 |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mdp                              | 1.09 sec                                                 | 548 ms: 1.99x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 251 ms: 1.98x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 251 ms: 1.92x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 252 ms: 1.82x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 254 ms: 1.76x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 105 ms: 1.65x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 113 ms: 1.58x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 148 ms: 1.56x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 149 ms: 1.49x faster                                                    |
| deepcopy                         | 161 us                                                   | 111 us: 1.45x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 12.9 us: 1.41x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 10.0 ms: 1.35x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 7.32 us: 1.34x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 262 ms: 1.29x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.15 us: 1.27x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 266 ms: 1.25x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 40.7 ns: 1.25x faster                                                   |
| generators                       | 21.9 ms                                                  | 17.7 ms: 1.24x faster                                                   |
| raytrace                         | 145 ms                                                   | 118 ms: 1.23x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 44.6 ms: 1.22x faster                                                   |
| go                               | 70.0 ms                                                  | 57.9 ms: 1.21x faster                                                   |
| float                            | 37.9 ms                                                  | 31.5 ms: 1.20x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 50.9 ms: 1.20x faster                                                   |
| subparsers                       | 20.8 ms                                                  | 17.3 ms: 1.20x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 111 ms: 1.19x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 18.2 ms: 1.17x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 823 ms: 1.16x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.5 ms: 1.16x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 34.2 ms: 1.14x faster                                                   |
| regex_compile                    | 54.6 ms                                                  | 48.1 ms: 1.14x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 10.9 ms: 1.13x faster                                                   |
| k_core                           | 1.12 sec                                                 | 991 ms: 1.13x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 23.7 ms: 1.13x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.29 us: 1.12x faster                                                   |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.80 ms: 1.12x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.50 us: 1.12x faster                                                   |
| typing_runtime_protocols         | 71.0 us                                                  | 63.3 us: 1.12x faster                                                   |
| pyflate                          | 216 ms                                                   | 193 ms: 1.12x faster                                                    |
| pprint_pformat                   | 665 ms                                                   | 594 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                  |
| pylint                           | 128 ms                                                   | 115 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.50 ms: 1.11x faster                                                   |
| pprint_safe_repr                 | 328 ms                                                   | 296 ms: 1.11x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 39.4 ms: 1.10x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 93.5 us: 1.10x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 129 ms: 1.10x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 41.9 ms: 1.09x faster                                                   |
| chaos                            | 28.9 ms                                                  | 26.8 ms: 1.08x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 30.3 ms: 1.06x faster                                                   |
| sphinx                           | 434 ms                                                   | 409 ms: 1.06x faster                                                    |
| sympy_integrate                  | 8.02 ms                                                  | 7.57 ms: 1.06x faster                                                   |
| xml_etree_parse                  | 67.9 ms                                                  | 64.2 ms: 1.06x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.51 ms: 1.06x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.93 ms: 1.06x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.66 ms: 1.04x faster                                                   |
| thrift                           | 322 us                                                   | 310 us: 1.04x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 24.5 ms: 1.04x faster                                                   |
| sympy_sum                        | 57.6 ms                                                  | 55.8 ms: 1.03x faster                                                   |
| sympy_str                        | 104 ms                                                   | 101 ms: 1.03x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| richards                         | 22.4 ms                                                  | 21.8 ms: 1.03x faster                                                   |
| regex_dna                        | 99.6 ms                                                  | 97.1 ms: 1.03x faster                                                   |
| crypto_pyaes                     | 38.8 ms                                                  | 38.0 ms: 1.02x faster                                                   |
| sqlite_synth                     | 967 ns                                                   | 947 ns: 1.02x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.98 ms: 1.02x faster                                                   |
| fannkuch                         | 176 ms                                                   | 172 ms: 1.02x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 50.7 ms: 1.01x faster                                                   |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| genshi_xml                       | 21.8 ms                                                  | 21.7 ms: 1.00x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 193 ms: 1.01x slower                                                    |
| json                             | 1.93 ms                                                  | 1.96 ms: 1.01x slower                                                   |
| pickle_pure_python               | 139 us                                                   | 141 us: 1.02x slower                                                    |
| pycparser                        | 497 ms                                                   | 505 ms: 1.02x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 428 us: 1.02x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.1 us: 1.03x slower                                                   |
| pidigits                         | 161 ms                                                   | 166 ms: 1.03x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 172 ms: 1.03x slower                                                    |
| telco                            | 2.61 ms                                                  | 2.69 ms: 1.03x slower                                                   |
| gc_traversal                     | 2.01 ms                                                  | 2.07 ms: 1.03x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.06 sec: 1.03x slower                                                  |
| 2to3                             | 114 ms                                                   | 118 ms: 1.04x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 49.5 ms: 1.04x slower                                                   |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.16 ms: 1.04x slower                                                   |
| nbody                            | 54.2 ms                                                  | 56.8 ms: 1.05x slower                                                   |
| html5lib                         | 23.0 ms                                                  | 24.1 ms: 1.05x slower                                                   |
| shortest_path                    | 219 ms                                                   | 235 ms: 1.07x slower                                                    |
| connected_components             | 201 ms                                                   | 218 ms: 1.09x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 8.74 ms: 1.09x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.28 ms: 1.10x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.7 ms: 1.12x slower                                                   |
| create_gc_cycles                 | 830 us                                                   | 944 us: 1.14x slower                                                    |
| django_template                  | 13.6 ms                                                  | 15.5 ms: 1.14x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 249 ms: 1.17x slower                                                    |
| coverage                         | 26.9 ms                                                  | 33.3 ms: 1.24x slower                                                   |
| many_optionals                   | 195 us                                                   | 324 us: 1.66x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.0 ms: 2.71x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (1): regex_v8
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250830-3.15.0a0-d3d94e0-JIT/bm-20250830-macm4pro-arm64-python-d3d94e0ed715829d9bf9-3.15.0a0-d3d94e0.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.097x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.17x