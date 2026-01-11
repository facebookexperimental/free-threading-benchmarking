# Results vs. 3.12.6

- fork: python
- ref: aa8578dc54df2af9daa3
- machine: darwin-arm64
- commit hash: aa8578d
- commit date: 2026-01-10
- overall geometric mean: 1.241x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x faster
- Memory change: 1.25x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 114 ms                                                   | 113 ms: 1.01x faster                                                     |
| docutils       | 1.02 sec                                                 | 1.03 sec: 1.00x slower                                                   |
| html5lib       | 23.0 ms                                                  | 20.0 ms: 1.15x faster                                                    |
| sphinx         | 434 ms                                                   | 390 ms: 1.11x faster                                                     |
| Geometric mean | (ref)                                                    | 1.06x faster                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_eager_io              | 496 ms                                                   | 222 ms: 2.23x faster                                                     |
| async_tree_io_tg                 | 480 ms                                                   | 221 ms: 2.17x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 221 ms: 2.02x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 229 ms: 2.00x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 97.5 ms: 1.83x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 96.8 ms: 1.78x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.71x faster                                                     |
| async_tree_memoization           | 223 ms                                                   | 136 ms: 1.63x faster                                                     |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 248 ms: 1.35x faster                                                     |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                    |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.24x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 37.0 ms: 1.23x faster                                                    |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                     |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 121 ms: 1.07x slower                                                     |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.14x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.1 ms: 2.43x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.34x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 37.9 ms                                                  | 22.7 ms: 1.67x faster                                                    |
| nbody          | 54.2 ms                                                  | 40.0 ms: 1.36x faster                                                    |
| pidigits       | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                    | 1.30x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 54.6 ms                                                  | 40.5 ms: 1.35x faster                                                    |
| regex_effbot   | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| regex_dna      | 99.6 ms                                                  | 95.6 ms: 1.04x faster                                                    |
| Geometric mean | (ref)                                                    | 1.12x faster                                                             |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 51.6 ms                                                  | 36.8 ms: 1.40x faster                                                    |
| unpickle_pure_python | 103 us                                                   | 73.7 us: 1.40x faster                                                    |
| tomli_loads          | 957 ms                                                   | 693 ms: 1.38x faster                                                     |
| xml_etree_generate   | 38.9 ms                                                  | 30.9 ms: 1.26x faster                                                    |
| pickle_pure_python   | 139 us                                                   | 112 us: 1.25x faster                                                     |
| xml_etree_process    | 26.7 ms                                                  | 21.8 ms: 1.23x faster                                                    |
| json_dumps           | 4.26 ms                                                  | 3.60 ms: 1.18x faster                                                    |
| xml_etree_parse      | 67.9 ms                                                  | 60.2 ms: 1.13x faster                                                    |
| json_loads           | 10.9 us                                                  | 10.7 us: 1.01x faster                                                    |
| Geometric mean       | (ref)                                                    | 1.24x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 8.01 ms                                                  | 8.90 ms: 1.11x slower                                                    |
| python_startup_no_site | 5.71 ms                                                  | 6.41 ms: 1.12x slower                                                    |
| Geometric mean         | (ref)                                                    | 1.12x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|-----------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 4.77 ms                                                  | 3.91 ms: 1.22x faster                                                    |
| genshi_text     | 10.5 ms                                                  | 8.94 ms: 1.17x faster                                                    |
| genshi_xml      | 21.8 ms                                                  | 21.4 ms: 1.02x faster                                                    |
| django_template | 13.6 ms                                                  | 14.0 ms: 1.03x slower                                                    |
| Geometric mean  | (ref)                                                    | 1.09x faster                                                             |

All benchmarks:
===============

| Benchmark                        | bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d |
|----------------------------------|:--------------------------------------------------------:|:------------------------------------------------------------------------:|
| subparsers                       | 20.8 ms                                                  | 3.96 ms: 5.25x faster                                                    |
| richards                         | 22.4 ms                                                  | 9.76 ms: 2.30x faster                                                    |
| async_tree_eager_io              | 496 ms                                                   | 222 ms: 2.23x faster                                                     |
| richards_super                   | 25.4 ms                                                  | 11.6 ms: 2.19x faster                                                    |
| async_tree_io_tg                 | 480 ms                                                   | 221 ms: 2.17x faster                                                     |
| async_tree_eager_io_tg           | 446 ms                                                   | 221 ms: 2.02x faster                                                     |
| async_tree_io                    | 459 ms                                                   | 229 ms: 2.00x faster                                                     |
| mdp                              | 1.09 sec                                                 | 591 ms: 1.85x faster                                                     |
| async_tree_none                  | 178 ms                                                   | 97.5 ms: 1.83x faster                                                    |
| async_tree_none_tg               | 172 ms                                                   | 96.8 ms: 1.78x faster                                                    |
| deepcopy                         | 161 us                                                   | 93.5 us: 1.73x faster                                                    |
| async_tree_memoization_tg        | 231 ms                                                   | 135 ms: 1.71x faster                                                     |
| float                            | 37.9 ms                                                  | 22.7 ms: 1.67x faster                                                    |
| go                               | 70.0 ms                                                  | 42.6 ms: 1.64x faster                                                    |
| async_tree_memoization           | 223 ms                                                   | 136 ms: 1.63x faster                                                     |
| deepcopy_memo                    | 18.3 us                                                  | 11.4 us: 1.60x faster                                                    |
| comprehensions                   | 9.84 us                                                  | 6.21 us: 1.58x faster                                                    |
| deepcopy_reduce                  | 1.46 us                                                  | 953 ns: 1.53x faster                                                     |
| deltablue                        | 1.73 ms                                                  | 1.13 ms: 1.53x faster                                                    |
| logging_silent                   | 50.9 ns                                                  | 33.8 ns: 1.50x faster                                                    |
| pyflate                          | 216 ms                                                   | 144 ms: 1.50x faster                                                     |
| scimark_monte_carlo              | 32.2 ms                                                  | 21.8 ms: 1.48x faster                                                    |
| scimark_lu                       | 51.3 ms                                                  | 35.7 ms: 1.44x faster                                                    |
| scimark_sor                      | 61.0 ms                                                  | 42.5 ms: 1.44x faster                                                    |
| scimark_fft                      | 142 ms                                                   | 100 ms: 1.41x faster                                                     |
| xml_etree_iterparse              | 51.6 ms                                                  | 36.8 ms: 1.40x faster                                                    |
| unpickle_pure_python             | 103 us                                                   | 73.7 us: 1.40x faster                                                    |
| tomli_loads                      | 957 ms                                                   | 693 ms: 1.38x faster                                                     |
| raytrace                         | 145 ms                                                   | 106 ms: 1.37x faster                                                     |
| nbody                            | 54.2 ms                                                  | 40.0 ms: 1.36x faster                                                    |
| regex_compile                    | 54.6 ms                                                  | 40.5 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed          | 333 ms                                                   | 248 ms: 1.35x faster                                                     |
| spectral_norm                    | 54.4 ms                                                  | 40.4 ms: 1.34x faster                                                    |
| async_tree_cpu_io_mixed_tg       | 338 ms                                                   | 253 ms: 1.34x faster                                                     |
| chaos                            | 28.9 ms                                                  | 22.0 ms: 1.31x faster                                                    |
| coroutines                       | 13.6 ms                                                  | 10.4 ms: 1.31x faster                                                    |
| k_core                           | 1.12 sec                                                 | 864 ms: 1.29x faster                                                     |
| pprint_safe_repr                 | 328 ms                                                   | 254 ms: 1.29x faster                                                     |
| pprint_pformat                   | 665 ms                                                   | 518 ms: 1.28x faster                                                     |
| xml_etree_generate               | 38.9 ms                                                  | 30.9 ms: 1.26x faster                                                    |
| crypto_pyaes                     | 38.8 ms                                                  | 30.9 ms: 1.26x faster                                                    |
| pickle_pure_python               | 139 us                                                   | 112 us: 1.25x faster                                                     |
| async_tree_eager_memoization     | 132 ms                                                   | 107 ms: 1.24x faster                                                     |
| async_tree_eager                 | 45.6 ms                                                  | 37.0 ms: 1.23x faster                                                    |
| xml_etree_process                | 26.7 ms                                                  | 21.8 ms: 1.23x faster                                                    |
| mako                             | 4.77 ms                                                  | 3.91 ms: 1.22x faster                                                    |
| nqueens                          | 43.5 ms                                                  | 35.8 ms: 1.22x faster                                                    |
| logging_simple                   | 2.57 us                                                  | 2.12 us: 1.21x faster                                                    |
| bpe_tokeniser                    | 2.24 sec                                                 | 1.85 sec: 1.21x faster                                                   |
| logging_format                   | 2.80 us                                                  | 2.33 us: 1.20x faster                                                    |
| json_dumps                       | 4.26 ms                                                  | 3.60 ms: 1.18x faster                                                    |
| genshi_text                      | 10.5 ms                                                  | 8.94 ms: 1.17x faster                                                    |
| fannkuch                         | 176 ms                                                   | 152 ms: 1.16x faster                                                     |
| typing_runtime_protocols         | 71.0 us                                                  | 61.3 us: 1.16x faster                                                    |
| html5lib                         | 23.0 ms                                                  | 20.0 ms: 1.15x faster                                                    |
| hexiom                           | 3.04 ms                                                  | 2.65 ms: 1.15x faster                                                    |
| pathlib                          | 12.4 ms                                                  | 10.8 ms: 1.15x faster                                                    |
| generators                       | 21.9 ms                                                  | 19.2 ms: 1.14x faster                                                    |
| regex_effbot                     | 1.67 ms                                                  | 1.47 ms: 1.14x faster                                                    |
| xml_etree_parse                  | 67.9 ms                                                  | 60.2 ms: 1.13x faster                                                    |
| async_generators                 | 206 ms                                                   | 184 ms: 1.12x faster                                                     |
| dulwich_log                      | 21.3 ms                                                  | 19.0 ms: 1.12x faster                                                    |
| pycparser                        | 497 ms                                                   | 447 ms: 1.11x faster                                                     |
| sphinx                           | 434 ms                                                   | 390 ms: 1.11x faster                                                     |
| scimark_sparse_mat_mult          | 2.08 ms                                                  | 1.87 ms: 1.11x faster                                                    |
| thrift                           | 322 us                                                   | 303 us: 1.06x faster                                                     |
| json                             | 1.93 ms                                                  | 1.83 ms: 1.05x faster                                                    |
| async_tree_eager_cpu_io_mixed    | 231 ms                                                   | 221 ms: 1.05x faster                                                     |
| sympy_integrate                  | 8.02 ms                                                  | 7.69 ms: 1.04x faster                                                    |
| meteor_contest                   | 47.7 ms                                                  | 45.8 ms: 1.04x faster                                                    |
| regex_dna                        | 99.6 ms                                                  | 95.6 ms: 1.04x faster                                                    |
| telco                            | 2.61 ms                                                  | 2.55 ms: 1.02x faster                                                    |
| shortest_path                    | 219 ms                                                   | 215 ms: 1.02x faster                                                     |
| connected_components             | 201 ms                                                   | 197 ms: 1.02x faster                                                     |
| genshi_xml                       | 21.8 ms                                                  | 21.4 ms: 1.02x faster                                                    |
| json_loads                       | 10.9 us                                                  | 10.7 us: 1.01x faster                                                    |
| dask                             | 528 ms                                                   | 521 ms: 1.01x faster                                                     |
| asyncio_websockets               | 190 ms                                                   | 189 ms: 1.01x faster                                                     |
| 2to3                             | 114 ms                                                   | 113 ms: 1.01x faster                                                     |
| docutils                         | 1.02 sec                                                 | 1.03 sec: 1.00x slower                                                   |
| bench_thread_pool                | 419 us                                                   | 428 us: 1.02x slower                                                     |
| pidigits                         | 161 ms                                                   | 165 ms: 1.02x slower                                                     |
| django_template                  | 13.6 ms                                                  | 14.0 ms: 1.03x slower                                                    |
| sympy_str                        | 104 ms                                                   | 107 ms: 1.03x slower                                                     |
| sympy_expand                     | 167 ms                                                   | 174 ms: 1.04x slower                                                     |
| gc_traversal                     | 2.01 ms                                                  | 2.12 ms: 1.05x slower                                                    |
| async_tree_eager_memoization_tg  | 113 ms                                                   | 121 ms: 1.07x slower                                                     |
| python_startup                   | 8.01 ms                                                  | 8.90 ms: 1.11x slower                                                    |
| python_startup_no_site           | 5.71 ms                                                  | 6.41 ms: 1.12x slower                                                    |
| async_tree_eager_cpu_io_mixed_tg | 213 ms                                                   | 241 ms: 1.14x slower                                                     |
| bench_mp_pool                    | 39.7 ms                                                  | 45.9 ms: 1.16x slower                                                    |
| create_gc_cycles                 | 830 us                                                   | 962 us: 1.16x slower                                                     |
| coverage                         | 26.9 ms                                                  | 33.0 ms: 1.23x slower                                                    |
| many_optionals                   | 195 us                                                   | 258 us: 1.32x slower                                                     |
| async_tree_eager_tg              | 32.1 ms                                                  | 78.1 ms: 2.43x slower                                                    |
| Geometric mean                   | (ref)                                                    | 1.24x faster                                                             |

Benchmark hidden because not significant (4): pylint, sympy_sum, sqlite_synth, regex_v8
Ignored benchmarks (10) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-macm4pro-arm64-python-v3.12.6-3.12.6-a4a2d2b.json: chameleon, djangocms, gevent_hub, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (12) of results/bm-20260110-3.15.0a3+-aa8578d-JIT/bm-20260110-macm4pro-arm64-python-aa8578dc54df2af9daa3-3.15.0a3+-aa8578d.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, unpack_sequence, unpickle, unpickle_list

- Geometric mean (including insignificant results): 1.241x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.16x
- 95% likely to have a speedup of 1.14x
- 99% likely to have a speedup of 1.12x

# Memory
- memory change: 1.25x