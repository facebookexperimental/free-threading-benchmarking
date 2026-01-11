# Results vs. 3.12.6

- fork: python
- ref: aa8578dc54df2af9daa3
- machine: darwin-arm64
- commit hash: aa8578d
- commit date: 2026-01-10
- overall geometric mean: 1.094x faster
- HPT reliability: 99.52%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 123 ms: 1.08x slower                                                     |
| docutils       | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| html5lib       | 23.0 ms                                                  | 23.2 ms: 1.01x slower                                                    |
| sphinx         | 434 ms                                                   | 423 ms: 1.02x faster                                                     |
| Geometric mean | (ref)                                                    | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg                 | 480 ms                                                   | 238 ms: 2.02x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 248 ms: 2.00x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 242 ms: 1.84x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 250 ms: 1.84x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 108 ms: 1.60x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 152 ms: 1.47x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.26x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                     |
| async_generators                 | 206 ms                                                   | 188 ms: 1.10x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 47.3 ms: 1.04x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.9 ms: 2.92x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.23x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 28.6 ms: 1.32x faster                                                    |
| pidigits       | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| nbody          | 54.2 ms                                                  | 57.1 ms: 1.05x slower                                                    |
| Geometric mean | (ref)                                                    | 1.08x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                    |
| regex_compile  | 54.6 ms                                                  | 50.8 ms: 1.07x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 94.8 ms: 1.05x faster                                                    |
| regex_v8       | 9.59 ms                                                  | 9.27 ms: 1.03x faster                                                    |
| Geometric mean | (ref)                                                    | 1.07x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 37.7 ms: 1.37x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 56.2 ms: 1.21x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.96 ms: 1.08x faster                                                    |
| tomli_loads          | 957 ms                                                   | 897 ms: 1.07x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                    |
| xml_etree_process    | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                    |
| json_loads           | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| unpickle_pure_python | 103 us                                                   | 108 us: 1.05x slower                                                     |
| pickle_pure_python   | 139 us                                                   | 148 us: 1.06x slower                                                     |
| Geometric mean       | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 9.69 ms: 1.21x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 7.04 ms: 1.23x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.22x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 21.8 ms                                                  | 23.4 ms: 1.07x slower                                                    |
| genshi_text     | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                    |
| mako            | 4.77 ms                                                  | 5.50 ms: 1.15x slower                                                    |
| django_template | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.12x slower                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 4.16 ms: 4.99x faster                                                    |
| gc_traversal                     | 2.01 ms                                                  | 801 us: 2.51x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 238 ms: 2.02x faster                                                     |
| async_tree_eager_io              | 496 ms                                                   | 248 ms: 2.00x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 242 ms: 1.84x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 250 ms: 1.84x faster                                                     |
| mdp                              | 1.09 sec                                                 | 603 ms: 1.81x faster                                                     |
| create_gc_cycles                 | 830 us                                                   | 506 us: 1.64x faster                                                     |
| async_tree_none_tg               | 172 ms                                                   | 108 ms: 1.60x faster                                                     |
| async_tree_memoization_tg        | 231 ms                                                   | 144 ms: 1.60x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 115 ms: 1.55x faster                                                     |
| deepcopy                         | 161 us                                                   | 106 us: 1.52x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 152 ms: 1.47x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 12.5 us: 1.47x faster                                                    |
| xml_etree_iterparse              | 51.6 ms                                                  | 37.7 ms: 1.37x faster                                                    |
| float                            | 37.9 ms                                                  | 28.6 ms: 1.32x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 258 ms: 1.31x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.7 ms: 1.26x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 1.17 us: 1.25x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 267 ms: 1.25x faster                                                     |
| xml_etree_parse                  | 67.9 ms                                                  | 56.2 ms: 1.21x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 8.29 us: 1.19x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 43.4 ns: 1.17x faster                                                    |
| sqlite_synth                     | 967 ns                                                   | 829 ns: 1.17x faster                                                     |
| go                               | 70.0 ms                                                  | 60.0 ms: 1.17x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 114 ms: 1.16x faster                                                     |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                    |
| raytrace                         | 145 ms                                                   | 127 ms: 1.14x faster                                                     |
| scimark_fft                      | 142 ms                                                   | 124 ms: 1.14x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 18.7 ms: 1.14x faster                                                    |
| k_core                           | 1.12 sec                                                 | 991 ms: 1.13x faster                                                     |
| scimark_sor                      | 61.0 ms                                                  | 54.3 ms: 1.12x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.49 ms: 1.12x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 2.00 sec: 1.12x faster                                                   |
| pyflate                          | 216 ms                                                   | 194 ms: 1.12x faster                                                     |
| async_generators                 | 206 ms                                                   | 188 ms: 1.10x faster                                                     |
| pylint                           | 128 ms                                                   | 118 ms: 1.08x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 50.4 ms: 1.08x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.96 ms: 1.08x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 50.8 ms: 1.07x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 897 ms: 1.07x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.62 ms: 1.07x faster                                                    |
| pycparser                        | 497 ms                                                   | 468 ms: 1.06x faster                                                     |
| logging_simple                   | 2.57 us                                                  | 2.42 us: 1.06x faster                                                    |
| generators                       | 21.9 ms                                                  | 20.8 ms: 1.06x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 94.8 ms: 1.05x faster                                                    |
| logging_format                   | 2.80 us                                                  | 2.68 us: 1.05x faster                                                    |
| xml_etree_generate               | 38.9 ms                                                  | 37.4 ms: 1.04x faster                                                    |
| regex_v8                         | 9.59 ms                                                  | 9.27 ms: 1.03x faster                                                    |
| chaos                            | 28.9 ms                                                  | 28.2 ms: 1.03x faster                                                    |
| sphinx                           | 434 ms                                                   | 423 ms: 1.02x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 226 ms: 1.02x faster                                                     |
| nqueens                          | 43.5 ms                                                  | 42.8 ms: 1.01x faster                                                    |
| fannkuch                         | 176 ms                                                   | 174 ms: 1.01x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.01 sec: 1.01x faster                                                   |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| pidigits                         | 161 ms                                                   | 162 ms: 1.00x slower                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 32.5 ms: 1.01x slower                                                    |
| html5lib                         | 23.0 ms                                                  | 23.2 ms: 1.01x slower                                                    |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 2.10 ms: 1.01x slower                                                    |
| xml_etree_process                | 26.7 ms                                                  | 27.0 ms: 1.01x slower                                                    |
| pprint_safe_repr                 | 328 ms                                                   | 332 ms: 1.01x slower                                                     |
| pprint_pformat                   | 665 ms                                                   | 680 ms: 1.02x slower                                                     |
| richards                         | 22.4 ms                                                  | 23.0 ms: 1.03x slower                                                    |
| richards_super                   | 25.4 ms                                                  | 26.3 ms: 1.04x slower                                                    |
| async_tree_eager                 | 45.6 ms                                                  | 47.3 ms: 1.04x slower                                                    |
| hexiom                           | 3.04 ms                                                  | 3.16 ms: 1.04x slower                                                    |
| json_loads                       | 10.9 us                                                  | 11.3 us: 1.04x slower                                                    |
| thrift                           | 322 us                                                   | 337 us: 1.05x slower                                                     |
| unpickle_pure_python             | 103 us                                                   | 108 us: 1.05x slower                                                     |
| sympy_sum                        | 57.6 ms                                                  | 60.4 ms: 1.05x slower                                                    |
| nbody                            | 54.2 ms                                                  | 57.1 ms: 1.05x slower                                                    |
| sympy_str                        | 104 ms                                                   | 110 ms: 1.05x slower                                                     |
| pickle_pure_python               | 139 us                                                   | 148 us: 1.06x slower                                                     |
| genshi_xml                       | 21.8 ms                                                  | 23.4 ms: 1.07x slower                                                    |
| 2to3                             | 114 ms                                                   | 123 ms: 1.08x slower                                                     |
| crypto_pyaes                     | 38.8 ms                                                  | 41.9 ms: 1.08x slower                                                    |
| genshi_text                      | 10.5 ms                                                  | 11.4 ms: 1.09x slower                                                    |
| sympy_expand                     | 167 ms                                                   | 188 ms: 1.12x slower                                                     |
| shortest_path                    | 219 ms                                                   | 251 ms: 1.15x slower                                                     |
| telco                            | 2.61 ms                                                  | 3.00 ms: 1.15x slower                                                    |
| mako                             | 4.77 ms                                                  | 5.50 ms: 1.15x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 130 ms: 1.15x slower                                                     |
| django_template                  | 13.6 ms                                                  | 15.7 ms: 1.15x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 247 ms: 1.16x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 46.3 ms: 1.16x slower                                                    |
| scimark_lu                       | 51.3 ms                                                  | 59.8 ms: 1.17x slower                                                    |
| meteor_contest                   | 47.7 ms                                                  | 55.8 ms: 1.17x slower                                                    |
| python_startup                   | 8.01 ms                                                  | 9.69 ms: 1.21x slower                                                    |
| connected_components             | 201 ms                                                   | 244 ms: 1.22x slower                                                     |
| python_startup_no_site           | 5.71 ms                                                  | 7.04 ms: 1.23x slower                                                    |
| bench_thread_pool                | 419 us                                                   | 549 us: 1.31x slower                                                     |
| many_optionals                   | 195 us                                                   | 271 us: 1.39x slower                                                     |
| coverage                         | 26.9 ms                                                  | 38.9 ms: 1.45x slower                                                    |
| async_tree_eager_tg              | 32.1 ms                                                  | 93.9 ms: 2.92x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.09x faster                                                             |

Benchmark hidden because not significant (4): typing_runtime_protocols, sympy_integrate, dask, json
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260110-3.15.0a3+-aa8578d-NOGIL/bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.094x faster

# HPT report

- Reliability score: 99.52% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.35x