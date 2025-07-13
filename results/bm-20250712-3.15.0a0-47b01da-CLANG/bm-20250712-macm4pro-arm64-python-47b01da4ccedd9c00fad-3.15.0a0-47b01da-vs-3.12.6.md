# Results vs. 3.12.6

- fork: python
- ref: 47b01da4ccedd9c00fad
- machine: darwin-arm64
- commit hash: 47b01da
- commit date: 2025-07-12
- overall geometric mean: 1.143x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 110 ms: 1.03x faster                                                    |
| docutils       | 1.02 sec                                                 | 1.05 sec: 1.02x slower                                                  |
| sphinx         | 434 ms                                                   | 401 ms: 1.08x faster                                                    |
| Geometric mean | (ref)                                                    | 1.02x faster                                                            |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 243 ms: 2.04x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 248 ms: 1.94x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 249 ms: 1.85x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 254 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.61x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.54x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 9.84 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 267 ms: 1.27x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 268 ms: 1.24x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                    |
| async_generators                 | 206 ms                                                   | 173 ms: 1.20x faster                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 39.4 ms: 1.16x faster                                                   |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| asyncio_websockets               | 190 ms                                                   | 194 ms: 1.02x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 251 ms: 1.18x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.5 ms: 2.72x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.26x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 29.3 ms: 1.29x faster                                                   |
| nbody          | 54.2 ms                                                  | 47.4 ms: 1.14x faster                                                   |
| pidigits       | 161 ms                                                   | 171 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                    | 1.12x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 43.8 ms: 1.25x faster                                                   |
| regex_effbot   | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| regex_dna      | 99.6 ms                                                  | 102 ms: 1.03x slower                                                    |
| regex_v8       | 9.59 ms                                                  | 9.88 ms: 1.03x slower                                                   |
| Geometric mean | (ref)                                                    | 1.08x faster                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_generate   | 38.9 ms                                                  | 32.8 ms: 1.18x faster                                                   |
| tomli_loads          | 957 ms                                                   | 809 ms: 1.18x faster                                                    |
| xml_etree_iterparse  | 51.6 ms                                                  | 44.1 ms: 1.17x faster                                                   |
| xml_etree_process    | 26.7 ms                                                  | 23.1 ms: 1.16x faster                                                   |
| unpickle_pure_python | 103 us                                                   | 91.2 us: 1.13x faster                                                   |
| xml_etree_parse      | 67.9 ms                                                  | 62.7 ms: 1.08x faster                                                   |
| pickle_pure_python   | 139 us                                                   | 136 us: 1.03x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 4.37 ms: 1.03x slower                                                   |
| Geometric mean       | (ref)                                                    | 1.10x faster                                                            |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.78 ms: 1.10x slower                                                   |
| python_startup_no_site | 5.71 ms                                                  | 6.25 ms: 1.10x slower                                                   |
| Geometric mean         | (ref)                                                    | 1.10x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|-----------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_text     | 10.5 ms                                                  | 9.06 ms: 1.16x faster                                                   |
| genshi_xml      | 21.8 ms                                                  | 19.4 ms: 1.12x faster                                                   |
| mako            | 4.77 ms                                                  | 4.56 ms: 1.05x faster                                                   |
| django_template | 13.6 ms                                                  | 13.9 ms: 1.02x slower                                                   |
| Geometric mean  | (ref)                                                    | 1.07x faster                                                            |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da |
|----------------------------------|:--------------------------------------------------------:|:-----------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 9.40 ms: 2.21x faster                                                   |
| mdp                              | 1.09 sec                                                 | 510 ms: 2.14x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 243 ms: 2.04x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 248 ms: 1.94x faster                                                    |
| async_tree_io                    | 459 ms                                                   | 249 ms: 1.85x faster                                                    |
| async_tree_eager_io_tg           | 446 ms                                                   | 254 ms: 1.75x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 106 ms: 1.63x faster                                                    |
| deepcopy_memo                    | 18.3 us                                                  | 11.3 us: 1.62x faster                                                   |
| deepcopy                         | 161 us                                                   | 100 us: 1.61x faster                                                    |
| async_tree_none                  | 178 ms                                                   | 111 ms: 1.61x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 147 ms: 1.57x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 145 ms: 1.54x faster                                                    |
| generators                       | 21.9 ms                                                  | 14.3 ms: 1.53x faster                                                   |
| comprehensions                   | 9.84 us                                                  | 6.94 us: 1.42x faster                                                   |
| coroutines                       | 13.6 ms                                                  | 9.84 ms: 1.38x faster                                                   |
| go                               | 70.0 ms                                                  | 51.1 ms: 1.37x faster                                                   |
| deepcopy_reduce                  | 1.46 us                                                  | 1.08 us: 1.36x faster                                                   |
| logging_silent                   | 50.9 ns                                                  | 39.3 ns: 1.30x faster                                                   |
| float                            | 37.9 ms                                                  | 29.3 ms: 1.29x faster                                                   |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 267 ms: 1.27x faster                                                    |
| raytrace                         | 145 ms                                                   | 115 ms: 1.26x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 43.8 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 268 ms: 1.24x faster                                                    |
| dulwich_log                      | 21.3 ms                                                  | 17.3 ms: 1.23x faster                                                   |
| async_tree_eager_memoization     | 132 ms                                                   | 108 ms: 1.22x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.52 ms: 1.20x faster                                                   |
| scimark_sor                      | 61.0 ms                                                  | 50.7 ms: 1.20x faster                                                   |
| async_generators                 | 206 ms                                                   | 173 ms: 1.20x faster                                                    |
| spectral_norm                    | 54.4 ms                                                  | 45.6 ms: 1.19x faster                                                   |
| xml_etree_generate               | 38.9 ms                                                  | 32.8 ms: 1.18x faster                                                   |
| tomli_loads                      | 957 ms                                                   | 809 ms: 1.18x faster                                                    |
| typing_runtime_protocols         | 71.0 us                                                  | 60.1 us: 1.18x faster                                                   |
| xml_etree_iterparse              | 51.6 ms                                                  | 44.1 ms: 1.17x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.41 us: 1.17x faster                                                   |
| deltablue                        | 1.73 ms                                                  | 1.48 ms: 1.17x faster                                                   |
| k_core                           | 1.12 sec                                                 | 961 ms: 1.16x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.93 sec: 1.16x faster                                                  |
| richards                         | 22.4 ms                                                  | 19.3 ms: 1.16x faster                                                   |
| xml_etree_process                | 26.7 ms                                                  | 23.1 ms: 1.16x faster                                                   |
| genshi_text                      | 10.5 ms                                                  | 9.06 ms: 1.16x faster                                                   |
| async_tree_eager                 | 45.6 ms                                                  | 39.4 ms: 1.16x faster                                                   |
| logging_simple                   | 2.57 us                                                  | 2.23 us: 1.15x faster                                                   |
| pylint                           | 128 ms                                                   | 111 ms: 1.15x faster                                                    |
| richards_super                   | 25.4 ms                                                  | 22.1 ms: 1.15x faster                                                   |
| nbody                            | 54.2 ms                                                  | 47.4 ms: 1.14x faster                                                   |
| regex_effbot                     | 1.67 ms                                                  | 1.46 ms: 1.14x faster                                                   |
| pyflate                          | 216 ms                                                   | 190 ms: 1.14x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 38.4 ms: 1.13x faster                                                   |
| unpickle_pure_python             | 103 us                                                   | 91.2 us: 1.13x faster                                                   |
| chaos                            | 28.9 ms                                                  | 25.7 ms: 1.13x faster                                                   |
| pathlib                          | 12.4 ms                                                  | 11.0 ms: 1.12x faster                                                   |
| genshi_xml                       | 21.8 ms                                                  | 19.4 ms: 1.12x faster                                                   |
| thrift                           | 322 us                                                   | 287 us: 1.12x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 45.9 ms: 1.12x faster                                                   |
| scimark_monte_carlo              | 32.2 ms                                                  | 28.8 ms: 1.12x faster                                                   |
| sympy_str                        | 104 ms                                                   | 94.5 ms: 1.10x faster                                                   |
| sympy_integrate                  | 8.02 ms                                                  | 7.32 ms: 1.10x faster                                                   |
| scimark_fft                      | 142 ms                                                   | 129 ms: 1.10x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 62.7 ms: 1.08x faster                                                   |
| sphinx                           | 434 ms                                                   | 401 ms: 1.08x faster                                                    |
| sympy_sum                        | 57.6 ms                                                  | 53.6 ms: 1.07x faster                                                   |
| pprint_pformat                   | 665 ms                                                   | 624 ms: 1.07x faster                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 309 ms: 1.06x faster                                                    |
| sympy_expand                     | 167 ms                                                   | 157 ms: 1.06x faster                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.98 ms: 1.05x faster                                                   |
| mako                             | 4.77 ms                                                  | 4.56 ms: 1.05x faster                                                   |
| pycparser                        | 497 ms                                                   | 478 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 224 ms: 1.03x faster                                                    |
| 2to3                             | 114 ms                                                   | 110 ms: 1.03x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 37.7 ms: 1.03x faster                                                   |
| fannkuch                         | 176 ms                                                   | 171 ms: 1.03x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 136 us: 1.03x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 947 ns: 1.02x faster                                                    |
| json                             | 1.93 ms                                                  | 1.90 ms: 1.02x faster                                                   |
| dask                             | 528 ms                                                   | 523 ms: 1.01x faster                                                    |
| meteor_contest                   | 47.7 ms                                                  | 48.4 ms: 1.01x slower                                                   |
| shortest_path                    | 219 ms                                                   | 222 ms: 1.01x slower                                                    |
| asyncio_websockets               | 190 ms                                                   | 194 ms: 1.02x slower                                                    |
| django_template                  | 13.6 ms                                                  | 13.9 ms: 1.02x slower                                                   |
| docutils                         | 1.02 sec                                                 | 1.05 sec: 1.02x slower                                                  |
| regex_dna                        | 99.6 ms                                                  | 102 ms: 1.03x slower                                                    |
| json_dumps                       | 4.26 ms                                                  | 4.37 ms: 1.03x slower                                                   |
| connected_components             | 201 ms                                                   | 206 ms: 1.03x slower                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.88 ms: 1.03x slower                                                   |
| pidigits                         | 161 ms                                                   | 171 ms: 1.06x slower                                                    |
| gc_traversal                     | 2.01 ms                                                  | 2.16 ms: 1.08x slower                                                   |
| python_startup                   | 8.01 ms                                                  | 8.78 ms: 1.10x slower                                                   |
| python_startup_no_site           | 5.71 ms                                                  | 6.25 ms: 1.10x slower                                                   |
| bench_mp_pool                    | 39.7 ms                                                  | 44.7 ms: 1.13x slower                                                   |
| telco                            | 2.61 ms                                                  | 3.00 ms: 1.15x slower                                                   |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 131 ms: 1.16x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 251 ms: 1.18x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 988 us: 1.19x slower                                                    |
| coverage                         | 26.9 ms                                                  | 32.3 ms: 1.20x slower                                                   |
| many_optionals                   | 195 us                                                   | 242 us: 1.24x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 87.5 ms: 2.72x slower                                                   |
| Geometric mean                   | (ref)                                                    | 1.14x faster                                                            |

Benchmark hidden because not significant (3): json_loads, bench_thread_pool, html5lib
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20250712-3.15.0a0-47b01da-CLANG/bm-20250712-macm4pro-arm64-python-47b01da4ccedd9c00fad-3.15.0a0-47b01da.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.143x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: 1.13x